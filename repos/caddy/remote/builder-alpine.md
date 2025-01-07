## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:1f95e0ce702a9f6f00d55d0fcc93446f659f4bb09e1a0000d25426058c01163b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:35753d0d658ae5ccb73f70a88e75bf2413faa5b1bd6d7a7bf4183f46b8d02319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85715778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb49d7f06d4bd5bd04b84ef1f6f05bda30fa71b0978aff70262bdddc951e97b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b581ca1e7ae37167d239ef52de4f3a732e969d9552d16ef81ab3c276e88b5f7`  
		Last Modified: Tue, 07 Jan 2025 03:32:01 GMT  
		Size: 279.1 KB (279140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513f2d688ac1d4fcc2bcb605b972cdf759ac2e6e5fca8f3cfce61cd60f567e3c`  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eab3d55a5b4549c6d596d5344097b5ce234c94811256e4531217eca14427df9`  
		Last Modified: Tue, 07 Jan 2025 04:22:48 GMT  
		Size: 5.9 MB (5939563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228b0a499ed2399d063afa20fcb396b31786b9d641edef09f27951fd968e022d`  
		Last Modified: Tue, 07 Jan 2025 04:22:48 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb041f5361714be8ebb4d4a21edb1ab52ecb37fa2fe0fde5aef2dfcceb858f84`  
		Last Modified: Tue, 07 Jan 2025 04:22:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:bfb524be8f08148a650c5a8a3dbf93ab398836be11dcaed9e84b8a3b3f8a5af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 KB (307748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183518e81f2e0d30e1eeb081bd013da32d28d804f55339fc989c05df0f75aac`

```dockerfile
```

-	Layers:
	-	`sha256:f7da9b04169a4902cd68a5a8a4c769de0c203716e3d09e169ce40f44b2a21df8`  
		Size: 287.6 KB (287645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5afc64672aada462c68416dca4bdbe5247ac38fe5afcb23613201ab2b378187`  
		Last Modified: Tue, 07 Jan 2025 04:22:47 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e19de3c7d95d0d31e6122c35078b85101e857c01412e32bcb03bc64ac815a42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83470034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d848a25ef2037a242be85b9e25d89f3ade447c7704ff2878db5685e900568ad3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09660efa60074dd6fc7ed0eaa983537498c86f66f4ce6ec6fd9caf5018feac3`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 291.8 KB (291778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7fe4b05e3f7753d356e4efa5b383d0a712d2663f8dc7c0713449b5f23c865c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64425618603480cb10d15d61de60fa02f4b17ab5735f2f545b6a3ac01364918`  
		Last Modified: Tue, 03 Dec 2024 23:28:27 GMT  
		Size: 5.9 MB (5882233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd18add16ed85d6ea08f5a65babcee8bacf1ac776ca3e4167424a96e1a40f16c`  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b008f4349f7cbfffde88e470a304b25d309f65a33dbed0fd3c5ca37ea794a914`  
		Last Modified: Tue, 03 Dec 2024 23:28:44 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f9bc235f6c0c0175da6b401917392882442f5d689eb95ea4da259c5818b2b6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ad433567208d8d40ed5e945d0d3df49bdd2063d30fbce52b9cf294faf3ddc8`

```dockerfile
```

-	Layers:
	-	`sha256:72033070b671d29283cb45cd4f0c01ae115933247e7eb5afad74ca416ecfc469`  
		Last Modified: Tue, 03 Dec 2024 23:28:44 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ea0d82d2fd556d98be80cec50225db88bf0bdf4d07dec22fb1991923ca968a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82676950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f006240e2f4ee3be40e9c5fc2acdedb909715b9fd376b8973b48d69332374f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7356de11a86ffd0370f043cbae8db3544365e081a72fd784543dc2b9d34c435c`  
		Last Modified: Wed, 04 Dec 2024 07:18:46 GMT  
		Size: 291.0 KB (290956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34694fe5ab5f45ca25bbc7925d9fc49b2cb7c6a74bd96b76a141cf03c10ca0`  
		Last Modified: Wed, 04 Dec 2024 07:18:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7770c65806119884319aeb81cbef2c728bf86fa5e1d0d160c5898119d212f5`  
		Last Modified: Wed, 04 Dec 2024 09:59:28 GMT  
		Size: 5.4 MB (5367207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799da4396d8b93f366789c08bba994a739e25273c47addc9f8088e514d146ab`  
		Size: 1.7 MB (1724265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379422e1fc2ae10e604ae7acd4c05eb2840b72bcce3dd13b06b6ffb63f63ab12`  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:67c8de0cecd12860b9bda8ae0270c3d82499a4a89a3dc39e3d0d870a68c9b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 KB (315426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c50d39024c193bf9bbf3be5e6c69f6af4f2b81dbc423335f9be1e87bb29490`

```dockerfile
```

-	Layers:
	-	`sha256:14bf06e4a8a0395211c4c7da779d86cf294fbe34ee68962b014257156639f427`  
		Last Modified: Wed, 04 Dec 2024 09:59:42 GMT  
		Size: 295.2 KB (295202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92baaaee9d7fd96e70a25b1c885c7535d92673a04f23383206e14852b15deb04`  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:24378d9940ae5184ea9a97a8e1fd86f45e151c9828ed8739c0aab9a7c499a9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82648041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05138b8f61fff6d74e40305857715d3e3996bbb3e715ef44e78849721f420093`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9faf9f6de87bdbe386e2feec24afe73e25189e74524f5edca5544d4c4c6b9`  
		Last Modified: Tue, 07 Jan 2025 06:34:15 GMT  
		Size: 281.8 KB (281782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4105e48f862c95e3929ec860f34d6c01a6cae0b0a2fe1b5e80281e7f1b92686e`  
		Last Modified: Tue, 07 Jan 2025 09:48:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81bb655cecdfb38428c95f5e11d0502782e69ecccedfb0b54a58b7f85cc23f1`  
		Last Modified: Tue, 07 Jan 2025 12:25:11 GMT  
		Size: 6.3 MB (6261807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa965853bb170c75168bc1d0bf7ad8c421587f9978e38ab86ab31ccd2ff29b16`  
		Last Modified: Tue, 07 Jan 2025 12:25:54 GMT  
		Size: 1.7 MB (1695590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d0d49dd76ef4e25a724093a3e57348bd9de2f27f3ca5d8e254ce03a81c7c1`  
		Last Modified: Tue, 07 Jan 2025 12:25:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:5e2f4b81d7cf3a02c54f77685fd7c35c299d057110bd8279530f624fbe9f34ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 KB (305961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb2881f330c4aaa594215c6680b457b521ada526b45191d2753577b38d68b27`

```dockerfile
```

-	Layers:
	-	`sha256:ac3812c0e26f6c12aaeb0bbd690ae8f3dc21127565ba4fb813564b1ef126b0c6`  
		Last Modified: Tue, 07 Jan 2025 12:25:54 GMT  
		Size: 285.8 KB (285788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20f97c41be9eea51f93011420110045d4a672992950287f2865c80add7c1711`  
		Last Modified: Tue, 07 Jan 2025 12:25:54 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json
