## `golang:1-alpine`

```console
$ docker pull golang@sha256:769c0a3571477715d919360cd58b4300c47b1d9a868c072a6e16bd45cd1e49e6
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
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:1bddfed44ff69c533c0ec006515afb7350986b0d7eb7383f780ab5525f4f06ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73257368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0594d7786b7ca10f1be62758b4f14a2c7d104de1977858d6aa20b1e076fa100a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:13210402d18f2c6a89eea7ff260c2b510644af46435318194001026305ba73eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e17ab9ac2fc9ab2dea4b95a713101986545a3b726c44a259f3fc9c411aa9cec`

```dockerfile
```

-	Layers:
	-	`sha256:dd14b9784986b259e7e2d9089901de7031b8f51b6f1e2cbaf97112bd6c233816`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 23.8 KB (23844 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:b34e66c3961169336bb03ad1548ae874571c1f74a74577fe1b43cc36c80613c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71175107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68310480aebfa05a75a050c8a799c31efe8ac700eb79aa9767567733be0ed002`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad27ef8f58290014492c74a7b2f956cb2cb25394a5098ce6da1e33844d12639`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 294.3 KB (294336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87622d8ade59df0daad35a20a0a1b816a8c25ed474cf6048473d6bbd0d46f2`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 67.7 MB (67715217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310eb826c90e6f890ea6ae063ba343178643fcf5b69c5543af729af28cef52af`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ede38240e04f2650dd1b2db98d49228eaf375739134fdc75dba27d1d9129a6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb3e1217a5184955d1165a6cda0761b72b8f09ed28ae75f33da4b0883f1dfe`

```dockerfile
```

-	Layers:
	-	`sha256:5ec34ab1776beab827b2374e57e985e06f4893d91786c7dd2c43609af01c7b77`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 23.8 KB (23807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:20b4a52834614903826fc043859f35653a4c568098b3ac5a1e28dc85994f089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70927455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddaa325fb310831bde97c498bdf3a7b8cc5e084cd3848f891f49c808acd8f98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5bc8c8a85a004d09793602cc73eb5cdd7e51489747e55adbda95159c328a70`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 293.2 KB (293185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd578652b0fd72238bc2565adcc2bf2716995c086d72609492506b36ddec660`  
		Last Modified: Wed, 15 May 2024 08:36:50 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2149779e1ffef1096a27b02d94b473a272e256d5c015ce287a5ca9a26bc0171`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e95360c59613517ad8544fbd1c9c42af4fbeb3538a4ec24c12b0ef36f22fa800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 KB (229107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4334dc07c9c4a2f3881cdb281972e3973a96996d5b2688a0bc7d6bd109e254`

```dockerfile
```

-	Layers:
	-	`sha256:ce7c85b82f26648565c904781ed7c8670935430c86b8f402fca263cf581313f3`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 205.1 KB (205081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844714ec76764617fd1395ed8dcf25e4331a9f0732e6637fbb1413e53353ecff`  
		Last Modified: Wed, 15 May 2024 08:38:48 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8d1654b2a3b86c5c7e4f53f2028b78ac7908b9e29bc18f01ae4cf578d01419cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69915980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47435cf6488c31f9fc75d0e7579bd00ef23934081bd610d1b9f27fdb943ecce4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e3f50b898a3ae6cfe23ad1a18c4fb0bf0e08bb7feb5503a4b7d6a65e6f31bd`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 296.1 KB (296070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df936e3f0526d99820dadd5ba236ab92b125bf8f10cf6f450093350d9d53af4`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:22c03a5b12bc2b66393386ac38b23ca722fd3cc0dcb7d1bbd0e731839a97216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 KB (228982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4072648c026afcb8a34f422c7100706682fda10101f4960de624290a98421753`

```dockerfile
```

-	Layers:
	-	`sha256:b8b1359a78ead7806e03d3e6b8be725ccd62fe0739a85299db881b98a6acbe87`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 205.1 KB (205066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb62db786336498e2892bbd7afc131a056a9ded197194e18088e63bc77296c0`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 23.9 KB (23916 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:c22e3c6a61734265c5fa044b4feecdd14bfc0d02cf208a4028e05945b1742419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71103540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606b385368ef7601d908287957af6cb66bd7988b6d11c5d63c88a4b1e07ccbee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636e6cae80696e05367d32690db4a8577dd0a3c759d450e134975a03bbc5afc`  
		Last Modified: Wed, 22 May 2024 22:55:01 GMT  
		Size: 292.9 KB (292872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd3d68e21a67472f9828cf1f154f8f9b2784731bbf6c1491c371acb44f7e29a`  
		Last Modified: Wed, 22 May 2024 22:55:03 GMT  
		Size: 67.3 MB (67343328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2fb62a4ab8844a7f8050a32d3e249c3c80b3b0874cf190b814216d3afa68be`  
		Last Modified: Wed, 22 May 2024 22:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bfb4dfa5dbbb979f9879f070472876c384231581c295fcc5a123eae6188aec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1d1ace2ec5eb90227588b05427ec430439a71857eb7c704a9466a6ec669917`

```dockerfile
```

-	Layers:
	-	`sha256:a6708b731df9c47ff12e2d35730eb7e7cf00288cfe74bc572e047d761cbdfed8`  
		Last Modified: Wed, 22 May 2024 22:55:00 GMT  
		Size: 23.8 KB (23792 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:66906aeebaf2d2e4c78bb39784b783d77246e455c17395d646f57b7b140354ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70085062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6247326d46566e3b6eb30059ae26bb56c0a4a0a4ca62d2ee6eb2db804c9c0a02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d82ce8dbc35c2b54369f84f5d1cdca1f43f171bafaa35b9ece60118143b6960`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 296.5 KB (296495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f690359b53e53fdcdeaa9654150463f063113662b6108d3988eef4548dec7c`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a63d2fb17361b3f07519111bc2d832ec5e2159f3bfe144f3ea14e469ae623652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 KB (227148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe1d5d5d1f7dcd4377674b848b70f778ab20e23452370b7828ad5586795cf23`

```dockerfile
```

-	Layers:
	-	`sha256:5b6e13df040a73bd7afecf419ed0d024167290c565920d249fb8ca868cbbd4bf`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 203.2 KB (203185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c1e0edb1c99bffaac347b13878e824eed860cceebc6072892fa4cb3b2bf6c6`  
		Last Modified: Wed, 15 May 2024 04:46:36 GMT  
		Size: 24.0 KB (23963 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:0e5bf747efb8a48b77e96bece4ba3a02ecf5d28c2b3daf2144bddcfc5a848a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71935986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbe972317b1bf6233bca9a319fed2c3b57fbdd6bed22da237ed8622886c9bad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57cebd6cab112aa720ede5bce8aa42592bcc9ea99aa91ade3eb03d2ecbbce8`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 294.1 KB (294116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b267d7cbedb48e683f15d12454c6aa505137bf49f9e3258cbdb09690fc056`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6bb3dfd9218309f0a526787a94534b73fc6f45f0f60c19d5377551d81d70a073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 KB (226989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7337811b79414e4bbd74a8eaa285168231fca74c9af13b40a96b30be94fb652c`

```dockerfile
```

-	Layers:
	-	`sha256:d98603c001669642404e9484bcaa6adacfce98d0d7a38c1a12950971d187d088`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 203.1 KB (203091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a6895d5759b60d87b16ae5b0133aaf02bbb9bd486561a67b452c2accc9703d`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 23.9 KB (23898 bytes)  
		MIME: application/vnd.in-toto+json
