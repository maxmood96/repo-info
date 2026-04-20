## `golang:tip-alpine`

```console
$ docker pull golang@sha256:92ff9584940a487c953d6bef7129b80fcadd0150fb775fe89126ad7798279710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:b1a0b724689623bd25b1ee62cd97da09feffbc8aec9b4fba80ed69aff821ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101487994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a873544fa6337f1c178c0ab58789d0e593ee203216d28dfb4ddc58cb0f653b6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 17:40:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:41:45 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:45 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:45 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc27dfb0dc794d565f3fc0252244caeb6ccebbe5c6b83cff24a78e8e198b827`  
		Last Modified: Mon, 20 Apr 2026 17:42:01 GMT  
		Size: 290.2 KB (290242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9800fe1d00fbf93fa3af2c224e36eef8eb15b87c8b6fcb13141f73eb2f1ed`  
		Last Modified: Mon, 20 Apr 2026 17:41:31 GMT  
		Size: 97.3 MB (97333404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a629de58b9fcf19544b435784229c79631619f621d411691ba516a296b56446e`  
		Last Modified: Mon, 20 Apr 2026 17:42:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b5ee07766088278ac735b6335e1436beca8a2f848bb987eed3e4b0a0d17f59aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eeb8977fb4afcbfb6e6438d5d7f78ca2facf503c3e94bbada1c1722b02c2be`

```dockerfile
```

-	Layers:
	-	`sha256:9d1100b7b55034bfe93287de1383b8ccfbb64a2512566608a9fc2c6522b0e614`  
		Last Modified: Mon, 20 Apr 2026 17:42:01 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724c1850713e28674ab52d2e8ae5a74663eb57d04f07a2dd6d4abfa6079790da`  
		Last Modified: Mon, 20 Apr 2026 17:42:01 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:3467aec39ed1ba85fc919673decc1718ffee02857a6c80b0155a02b1b45e879b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97306411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000f89d40b5294cd8e7c577c070c21b7aac154049aa7a048eb14ade1b7601a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 17:39:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:41:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:57 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:57 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e149075c526d7d1c63a3f204fe3743b1a44faefb0cf95f12d0d2c5ce0d67d3`  
		Last Modified: Mon, 20 Apr 2026 17:42:11 GMT  
		Size: 291.0 KB (291030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f306b2825701e0ccf21cd12d3cf6b5050ea862a687be88b3f13ecb09ad2e3d`  
		Last Modified: Mon, 20 Apr 2026 17:42:14 GMT  
		Size: 93.4 MB (93443360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dc553709af703b706193ad54aa0de25ad795af1e870bb001ac5ca420e71506`  
		Last Modified: Mon, 20 Apr 2026 17:42:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:90a70fd2529e29497877b70e8c4f6fd721632a29f6417f385ceb3284fed38e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e00213ad21c7b656ec902057f2275bc08e44f7e6cdae7302b88f722aa85237`

```dockerfile
```

-	Layers:
	-	`sha256:73e06f3e96c3d6f79f2be23ff69fa47657dbde963d0e6d97ea31990b1f66dece`  
		Last Modified: Mon, 20 Apr 2026 17:42:11 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:20147037786434180449358a1a6204fef14891462b314a7f43da8fcaf74bed8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96735620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20bbc3a0af61452eef75f01376f666b525f65067615ee6ce9710368800fa102`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 17:41:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:43:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:43:53 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:43:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:43:53 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:43:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:43:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77c22a987a0538937f830a18629002dcfd91cb403ca0c85f777392c2250049f`  
		Last Modified: Mon, 20 Apr 2026 17:44:11 GMT  
		Size: 290.2 KB (290159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42fcfd73df1c3c4e864c147debb0154bf1e1c38912174f3d52a47a654a9641`  
		Last Modified: Mon, 20 Apr 2026 17:43:22 GMT  
		Size: 93.2 MB (93162179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556db0c7136d710e858fbeb962ff748c8dcb990d6679c7b86398c041991b55a`  
		Last Modified: Mon, 20 Apr 2026 17:44:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:97cc3d1295e49ca50a314963fd76bf73e31c35bf721c4f9eff1079712d8dc3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cad8662268cb321d4616a45e8fa2f753ed3659d831dd54a35cc172403caf37f`

```dockerfile
```

-	Layers:
	-	`sha256:47b1b730d49826783613ae61aa05c200c0f74d5ce372c7c94a93ad3255c4a734`  
		Last Modified: Mon, 20 Apr 2026 17:44:11 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f388d72a06d4791291cb56f409859fa167869684483d9492a0a765673f353683`  
		Last Modified: Mon, 20 Apr 2026 17:44:11 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8594a7f6e43f93c3101201ba830ee8d3f3971e0a49ad482fe9eb62744e642c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96513520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bbb7d7b1a937dcebe12312bfad00275429b089688c7fa8bf13bc5006e12515`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 17:40:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:41:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:57 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:57 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:42:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:42:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6f0b9a280e8607d76c0b1793877c919ce294cbc70de6a87d1834190975543f`  
		Last Modified: Mon, 20 Apr 2026 17:42:15 GMT  
		Size: 292.9 KB (292863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9da8d3894800a39f60fbfd67e48a2654efcedecf176b3e40f1e07ab0291557`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 92.0 MB (92020630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c973157e3996c1f2e62aded5f5e8328b265a156e96b259ec4e7b0a845fe1e631`  
		Last Modified: Mon, 20 Apr 2026 17:42:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:119dbdfc8f77216b1fa416346de0c74fed5d2b8f415683c3b8ad2bbacf81e83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c19c1eab841f4e76afc467b255a3a655ac7eb8f667fddf548019a97fc4b136d`

```dockerfile
```

-	Layers:
	-	`sha256:87a3ef75fa6b08eb22d51bbfa4ae6ad35708cfbe923fb369138a5d387c87ad17`  
		Last Modified: Mon, 20 Apr 2026 17:42:15 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ca55f2212ad801d0a65f64bf92851645474f3cd98d4b1f01da7c165955de44`  
		Last Modified: Mon, 20 Apr 2026 17:42:15 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:a96ae2c3a750622b82aafbcf93ef9f6da9184ab00453942edd104c1c6f5df973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99053748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c5870e42fbe09abc686cb4300eda6145f8630d4b97cda8f850b521e75a6912`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 17:40:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:43:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:43:11 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:43:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:43:11 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:43:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:43:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343f3755a0af4d15a772e220db918d012e9b91daa75b4a2ef0ab6cd1bb4094f9`  
		Last Modified: Mon, 20 Apr 2026 17:43:28 GMT  
		Size: 290.6 KB (290634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ee3233bce23292707dea9900b4db989f25efd70edf364d9cfceefc1e3441c`  
		Last Modified: Mon, 20 Apr 2026 17:42:46 GMT  
		Size: 95.1 MB (95072511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9d52a53cb67d1ebf725fa63c6d2a48156664006bfb12758b54458cd0a30e25`  
		Last Modified: Mon, 20 Apr 2026 17:43:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:78b48d2a7ce68f2fe58092f0dd2da56ccc2af48d5d87677cbbe014d6325ff0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19ffecf5bc689bb32aeafb9dc70d523f509fc1a62f83f43283e9a7fff2d0adf`

```dockerfile
```

-	Layers:
	-	`sha256:5ddf4a6ced45eef820d74531d7dfed49af884f47feb2811737c674f17dafb3e9`  
		Last Modified: Mon, 20 Apr 2026 17:43:28 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb410c6d9ec875fac35d4abfd0c368552b46925c1af6b55bbe2b1bb2cc83fe0`  
		Last Modified: Mon, 20 Apr 2026 17:43:28 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:9b9e88141f21fb0ce0dd4f73b3f5f306b90d2cc14987616896c9b7b39b1eedb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97997007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55c8829711fedeef8ecd31c98406ba2661eeb153b51a609a012359c5f461314`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:28 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:46:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:46:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f72075717c40f723c05a62a7b4daebee738f45ad2854cdb0f9f31a6113d444`  
		Last Modified: Mon, 20 Apr 2026 17:42:34 GMT  
		Size: 93.9 MB (93872555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c3aa755b684c4b0fad11d1a868c97b1c1cd58327d49afdd0e814c16c3d6be`  
		Last Modified: Mon, 20 Apr 2026 17:46:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7a63a195c707872e57ad6c4b02740e884d0d08ba9b93ee691104233412ee651d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873efd8e1d9a2ec37608ef45844cfcca2f8b9c7113511927a811ff315b23032e`

```dockerfile
```

-	Layers:
	-	`sha256:bd480e2f6cad7f97eb3d4357d36e6895753061c3297750bd11e521bccbda0ac0`  
		Last Modified: Mon, 20 Apr 2026 17:46:37 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b90e47818d7ce2dcc3dc978bd50d3c74a0802d108b738314f6faaac6df28607`  
		Last Modified: Mon, 20 Apr 2026 17:46:37 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:83bf42cca33bce656461495df2cb7e7f89a544b6736ae364eabadfb9c8096cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98284679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e924092ce959dafb5c89d349f175cd08db709211573daaa4032fed98d14753`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 18:17:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 18:17:57 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 18:17:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 18:17:57 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 19:04:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 19:04:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a410f935145df1e7078db1622c7e4b5b67ab66721f524e15a78ee2440fd23`  
		Last Modified: Mon, 20 Apr 2026 18:24:58 GMT  
		Size: 94.4 MB (94406306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb9e65089092ac35fc2249d3db2b7b974785c09c5ee940a92659330dff0c337`  
		Last Modified: Mon, 20 Apr 2026 19:06:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dcb03e993b05443617dff6aa0ba7ac64bcb600f9eb90a00574002619bc792e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0608b197024b9293a654b79c053f47d65ebef930f342121d0fa2b527c42ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:e14678750d7bab0dfe0290989d15ebf7391ea24b4c0f7f8e5c1649ea08cae773`  
		Last Modified: Mon, 20 Apr 2026 19:06:03 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b25d9764eb472ebc414dda57146bddbe5a92ed9ec22266837d60d8aa34e350a`  
		Last Modified: Mon, 20 Apr 2026 19:06:03 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:c140a4ff3355393da743777824b919ee502e29d3aa88644a8fc47965cd34a633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99870288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f878b48b3e47dc55ee19bce9e9aeaef1ecd2e6c275cad9050827cdb169c62182`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:48:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:48:01 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:48:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:48:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc40b99896e610d7e8bfd78ceac0447cbdeee9aed83f1c52c72fd167c0ef6be`  
		Last Modified: Mon, 20 Apr 2026 17:47:23 GMT  
		Size: 95.9 MB (95852451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05092bc6a03e282849941cf36199ae0362e8f0a0514a85858d631b720be2ccbd`  
		Last Modified: Mon, 20 Apr 2026 17:49:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7b0683d5d4d71a353e132acc2034b82c26201cbce34a3c0806ea952a66d20a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c563cffe40e1c38a730d3aedca1fa528b226cdc2f2a2622886da724bb2f7201`

```dockerfile
```

-	Layers:
	-	`sha256:56c83d9121001da834a7b31133a40e184a52d25c36e0f6019798279e89a89f71`  
		Last Modified: Mon, 20 Apr 2026 17:49:36 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055bec75dac5e18d9c6ea1daae4c6e6a7428ed5f4a7de9c16e09e9a9055e1d4e`  
		Last Modified: Mon, 20 Apr 2026 17:49:36 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
