## `golang:tip-alpine`

```console
$ docker pull golang@sha256:0011051de061ae4a4665bb3caf190aca3b8715e230308f631d049d6129af7316
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
$ docker pull golang@sha256:1e1dad52b563c1091329784cbea19249d82cda46a8191c4652b6b29ad0e23f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106699533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3321cfa11f14739e3b9b1a902aec8a9ee46e91d258b1c3da8a1b2f83dfd652`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:02:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06671144a144c48bb4b53d51c77b13e9bdacb38793d8d6aca32b52e487b81242`  
		Last Modified: Tue, 30 Jun 2026 00:05:13 GMT  
		Size: 245.1 KB (245059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96112613ca74dcaf72b29b75f1686921a6f92c1d50000e911abd31cedae3173d`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 102.6 MB (102607925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc89362cb5643caf051e7b04269c016a9d0a46807950ca802920f2f705edfb2`  
		Last Modified: Tue, 30 Jun 2026 00:05:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e7fd8ddcf170daf9625d95f2ad352fc2a9546ba33588988188581448eb5cd340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 KB (201851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd84cfbfb5592444e3b49a5b9a64f1b0a6a482c10c1a395e7bb3b42fbf78510`

```dockerfile
```

-	Layers:
	-	`sha256:e67b84801b8bc55a296604df1f02b5c7f5c539665c082b4d589ed0f98b80f4af`  
		Last Modified: Tue, 30 Jun 2026 00:05:13 GMT  
		Size: 176.8 KB (176752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114e30f594393a0d3d547e879d0b035950ed6744136e34b1ad4ea51e85433af`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:fcbdae98cd29583c5756f1406d858e69277cf3968b6e8d6b02b960ad4ea94fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102426173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4995821d49e1016db0753e57e2865084347f5ad0c3fcca143e1230a7bf37e55c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:01:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:04:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:28 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:28 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90ceaa7895be7dea4af18035f154dd1ccc4a1e013a764f6557c95e1ba45d52e`  
		Last Modified: Tue, 30 Jun 2026 00:04:45 GMT  
		Size: 246.1 KB (246143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a02819539d055ae9fe41dba60a3333bac513373fcd44e702d1f5be6b4e9c2a`  
		Last Modified: Tue, 30 Jun 2026 00:04:47 GMT  
		Size: 98.6 MB (98626422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aded220dbc75236e736b0e27af7ce9ce65ee17d9608164bb6b2b6b2adc21308d`  
		Last Modified: Tue, 30 Jun 2026 00:04:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9d9c7bcbe543f8c06399e2bdcf835e2268735f26a6dc9b15c0ba2a8a0c40e38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0bbfe23d7d75e5ee5bf6f500532086f6097e6c0695ee5b27f768189ac854a4`

```dockerfile
```

-	Layers:
	-	`sha256:c3f641d80cd52c73d31ddc2b65a106f6543b0b08c1e96f479a98b3df77e07b46`  
		Last Modified: Tue, 30 Jun 2026 00:04:45 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:6736a28f945e2e1b5e841b8172e365885ef6659e27d13b86493f77da760dadef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101820257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be856bc34c02f9bc744340499fa19f1bb1537b4ac90c407a067f81c53458c4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:03:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:06:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:06:52 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:06:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:06:52 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:06:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d67969c25a61949fc46d78713a9787a80abef3b1b0c27b9c5688cf608bf802`  
		Last Modified: Tue, 30 Jun 2026 00:07:11 GMT  
		Size: 245.1 KB (245121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea34c6465040d9a03784c749dc96fc02b642a3007f305eb3e72609624011a8c`  
		Last Modified: Tue, 30 Jun 2026 00:06:17 GMT  
		Size: 98.3 MB (98314363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c36814178e51505207a80e01189d80bface56e918205489004f4424f9e5006`  
		Last Modified: Tue, 30 Jun 2026 00:07:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3418261402abea4f570f3cb2ba711ed4a2f353bc94843475d940c085e6d2f012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be071b5ddc203c65aac3a2821f07cc13078b8c93c8f703860e2a4721418d18c3`

```dockerfile
```

-	Layers:
	-	`sha256:368a36c7275f14245e5a2688f008ae8f40acfad29c1eab4b8464dfd7ffab3da5`  
		Last Modified: Tue, 30 Jun 2026 00:07:11 GMT  
		Size: 176.1 KB (176122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1d4b122883662cfdfc9b23b8e97a499b838eb9d0b2e0d05c9b091c05d7c051`  
		Last Modified: Tue, 30 Jun 2026 00:07:11 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c799c827c4e38303432a3155938eed110a3ce1891c73232e9f3fba6a2b18032a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101416629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9ec4b80935f45c9383f4d0fb946bff19d5d8e6c3c50281d8852a2312550dc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:02:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:04:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:24 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:24 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0ea7162d5414674850026872aa3eba3eeb80b6cebca7e005f0730a800e4a59`  
		Last Modified: Tue, 30 Jun 2026 00:04:42 GMT  
		Size: 247.5 KB (247499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc19bf506b072ad4aafc8fd4d3064dd82a2aad3673c0290669bfd12b0d5429a8`  
		Last Modified: Tue, 30 Jun 2026 00:03:59 GMT  
		Size: 97.0 MB (96985935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cf7546405ce174316caa0cc2b2448216546bcb2fabf9b85c98d4a3cf77b56a`  
		Last Modified: Tue, 30 Jun 2026 00:04:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4f7ad154d1edbeae28d3412a3dd4140ff0cddb2236eb38a80ecfdfa4eb16eaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 KB (201413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea8f05aa009ce8fe89c42dbe2075e271efd93c56fc9dccba4386b4581cf8d2c`

```dockerfile
```

-	Layers:
	-	`sha256:5c613729d05f8048397e0e639e56cc76b25c0c4bbef053f02c73f4be2e99cb68`  
		Last Modified: Tue, 30 Jun 2026 00:04:42 GMT  
		Size: 176.2 KB (176158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f2f0ed722edb3e43eb4a3faadf36a26cc249c923b6bc79ce3bc29d32f4807e`  
		Last Modified: Tue, 30 Jun 2026 00:04:42 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:82cc05c11baa88d9dce5dd6075ba72b30495340d92fce7b91840c94d00652771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104309586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a018d3107e1ee8bd345355b54a92b2d1692a12f26f92b8dec2b3ea067d001e2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:02:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:05:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:05:10 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:05:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:05:10 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:05:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:05:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b58c90e8ff578a8f703c67e99dc252760dc6b64c18eec451121b06140557cd`  
		Last Modified: Tue, 30 Jun 2026 00:05:27 GMT  
		Size: 245.6 KB (245595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe287f4fcc073ba1e90b598305ae90f45e8a3339ed6d99366e8996528c1a25`  
		Last Modified: Tue, 30 Jun 2026 00:04:49 GMT  
		Size: 100.4 MB (100393692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c687b3280fce005ed5177408fc6f07121cbe831b09baff0dd65a7e770ac3a7d2`  
		Last Modified: Tue, 30 Jun 2026 00:05:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cf7a247df5cbd519dd511aeb6ffb6c48c8498cdc61f478fd5a865cf4eb368a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 KB (201767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49c3a8f39fa8281f09e53613048f7ecfe564c158893a9184ae22924ba22d9de`

```dockerfile
```

-	Layers:
	-	`sha256:08f6a3f8039d00d541f69881f66c52cdf68fc29dc3aaf750b8962d4dc557feac`  
		Last Modified: Tue, 30 Jun 2026 00:05:27 GMT  
		Size: 176.7 KB (176711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a096f78c35aecfc5c4261adfc6adee2f8de92502aac9be13e2f7fc26935c5a`  
		Last Modified: Tue, 30 Jun 2026 00:05:27 GMT  
		Size: 25.1 KB (25056 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:7cad4e7e7e01617e425ef4196f70cd8cf1c44ca728fc944d0cfbffa55d517435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103031224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44880a2358bbf731af06a69abbe08a4a4f6bb3e4a4ed5a2229887b3152a39ce9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:43:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:10:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:10:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e5cd9291f73cdfb8a0cc68e49e0664e71ce2e2dca0d970b3b935c603149a9`  
		Last Modified: Tue, 16 Jun 2026 00:44:13 GMT  
		Size: 247.9 KB (247921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea8767a8a0a93030114399f1f19e8f448718e14ab3c948bcc8dac1be9cf2f8`  
		Last Modified: Tue, 30 Jun 2026 00:06:26 GMT  
		Size: 99.0 MB (98969745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aefcb0e4f2c6d4a4682712707f5ae6c63d5f6685d7400ffb3d21dc00b03327`  
		Last Modified: Tue, 30 Jun 2026 00:10:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:165369d89d31576a8b454abfe0d916a642d0c8d9e8cd35c3575606965b4c4697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e2c1996cbcb311b7c2cc2992af1c487290ebd94cca09321397fc7e7957f019`

```dockerfile
```

-	Layers:
	-	`sha256:86fc1dea3c717a1cdd4cf284e329dffd6468f63bd01981c679577eb5ab8f2eb9`  
		Last Modified: Tue, 30 Jun 2026 00:10:49 GMT  
		Size: 176.2 KB (176151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530102afebe699feee4a79157eaee046722b03c8fa83d76d697d8ac3ce6b54cb`  
		Last Modified: Tue, 30 Jun 2026 00:10:49 GMT  
		Size: 25.0 KB (24979 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:26d9f4e41ea1334f415fe21a39234db40d77ed0064c6356fc2c07cfed6827e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103741518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0209303a87270f01e9fcdf6b13e41b64107c6da163e854a8ee13a6bcc334c6c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 07:35:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 18:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 18:13:58 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 18:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 18:13:58 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 18:14:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 18:14:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2021d7589f6c18103a6d7e004a2611e54bd2e48edc8f74827e7357bba545c1fe`  
		Last Modified: Thu, 18 Jun 2026 07:38:04 GMT  
		Size: 245.5 KB (245484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d11c7942d435cc548ce25dc3507d8ce30ca618e0f219cecb9d97b255ce78cec`  
		Last Modified: Tue, 30 Jun 2026 18:17:30 GMT  
		Size: 99.9 MB (99921518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01245c649887ff03fa5221cc69c9f2c15106c52afb0762428ea89fba3faa4cee`  
		Last Modified: Tue, 30 Jun 2026 18:17:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:58063fa69b686f644b5a9494b05d30839047b02478c7281d614b53b786a75a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0162c2c5b11d767e8c489376858a6f48eaa216eee157f7fffed210c2d56d644b`

```dockerfile
```

-	Layers:
	-	`sha256:77b096b524206dd5c2dc877a1b05194388f3c82e61c860ff0f0d96a9f47563b3`  
		Last Modified: Tue, 30 Jun 2026 18:17:15 GMT  
		Size: 176.1 KB (176147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d574fd7f3ac95a429c48247a87ea7a2664558887d96e07d425bf73d931b4139d`  
		Last Modified: Tue, 30 Jun 2026 18:17:15 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:cc85295fb0d3734cf681c6bbe3ee01c1bf9c860846cbb971cb7b0959de1018b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104999768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ef5398a3275d45fc4197422c4f670aa989c3eb7c92bb1bb1a29796dadcab41`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 00:04:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 30 Jun 2026 00:04:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:42 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:42 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cee98e99408817c5ab9dd70b01b7c104a3fca1433455a6d7fc45f2442b72ad`  
		Last Modified: Tue, 30 Jun 2026 00:05:10 GMT  
		Size: 246.2 KB (246150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdf657db5fc71df443dbbc81704a25107962ecb9a4a8f16c3715658947e80b9`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 101.0 MB (101044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746c91707a4bc198957349ec33f87418dd43e426b859490d992954b9b9ec23a1`  
		Last Modified: Tue, 30 Jun 2026 00:05:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0b0a00b3f4cc675146684278c49e221b6abdbc294b6e3b3f3f92ce144f8fde5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 KB (201774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044c6bd2814f963ade0251dcc4f2a60505a1d948a679d304bfe9943a6a0ed359`

```dockerfile
```

-	Layers:
	-	`sha256:6159ccbf5f236115730c65f13cb856b7d0e5a539bb4a92e57737254cddaef5ce`  
		Last Modified: Tue, 30 Jun 2026 00:05:10 GMT  
		Size: 176.8 KB (176849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c823bf335a0c813e6b965a2412fec51af777a6be9f4177d253324b1463a052d`  
		Last Modified: Tue, 30 Jun 2026 00:05:10 GMT  
		Size: 24.9 KB (24925 bytes)  
		MIME: application/vnd.in-toto+json
