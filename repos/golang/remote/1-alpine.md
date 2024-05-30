## `golang:1-alpine`

```console
$ docker pull golang@sha256:7e788330fa9ae95c68784153b7fd5d5076c79af47651e992a3cdeceeb5dd1df0
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
$ docker pull golang@sha256:3183a82802a5c55c19b5640dc0183353b363892a058a68c923f26f2acb37f651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71374053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d664ede61421975ae3aa83755daab1d30687afe532676e1f36be7e3c74bbd07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:aa7b0abfad17911a6504f33d0109cd44efcd02575daf4ab9f82e2501435bf57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c7f3b70c17a4171694acd21953937675ce531292d98fcbe5e41f421edaebcf`

```dockerfile
```

-	Layers:
	-	`sha256:66574e25db66b13bfddcbda278a10257801e0a780fd272a18fcdd40b5c358d0d`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 23.8 KB (23807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:5e57aa99281c3ec63bca5261a1f93d77d65218521c46238add612a2b6c0377f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71101868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506d521e8197448ed607a252ce7241fb5cbdbee78f282303dd4af735a3d812e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dcdc524c6fb1376c9a25fdc7b7b00f47da12fd063092a2dcedd9d8036fca148b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf289d989d90fa3c8818fe6883aa80f8aaea8f83a7d188db76b0018ab0930a39`

```dockerfile
```

-	Layers:
	-	`sha256:0f6522bc718b5bed3b65968b313ad9f060dc3f838431d5309a11d33fc071487c`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 23.8 KB (23806 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:638709d35305a16b38f575eabe97e2cab3229169cf555ebd5e98630f794f595c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70654417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2a7462eb04ba6b0b64719de897a917431010ff74291ccd619423414cb62432`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e6feff72e44b3a90aa8df43db17606970ae86ea4d8bca7381ca36eb677e743ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e110c69f328847fe84b1f26b823ab5e6e042f6b2bb457ad84038824120a8c`

```dockerfile
```

-	Layers:
	-	`sha256:8c86a93f44580abb3028a08486875f6cb9bb717d1ef29872bc4601f93710047a`  
		Last Modified: Thu, 23 May 2024 06:26:55 GMT  
		Size: 23.7 KB (23697 bytes)  
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
$ docker pull golang@sha256:e88b9c5f48e387f911449cf140141a8dca18d4ee87125aeb6823300253b31401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70295950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2858b212c6a122229e73e973a56fe0882c886cb82d1789c72936cfc6f151f93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:87a7e4767879bc652058b5cebbc947c594178b070efb0a43e43e8d8a1d39e3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5c85230d815ebe7795ff86a1852e6f50e8a2cfb3b5a4b3e1e5b47b4584b5a1`

```dockerfile
```

-	Layers:
	-	`sha256:b8d3af3a84597aa726f51114077e2d635504c39cd43d67f33e8cb15fa2cec628`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:ee784839d81b1c63684846ca08e421df2e9510e2bf25cef351b039b61707d5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70539342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad12416c5903450d058cb5a5f95c68a4d36f6c2ed17c99713d8181dec17dd90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
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
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97854906558cbdd4f8b30d48425a9d6e12b615ee656e80e1597a268df53d0e1f`  
		Last Modified: Thu, 30 May 2024 07:18:02 GMT  
		Size: 293.2 KB (293171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1606ae9bc76bef6cd7d6184c6ad942cf7020da041748c3dfcec791c8210a5e75`  
		Last Modified: Thu, 30 May 2024 07:18:12 GMT  
		Size: 66.9 MB (66877453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c0500895860c9dde3b3a653d6b5866d10e8ee3aa5e6a81f05f11a45d18a49`  
		Last Modified: Thu, 30 May 2024 07:18:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:113aded68982efe4948733bdf42efc9e4afe1c54336615c6d4ea45bacde95c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fef9e72988867d56048186bdf8262755eb42840b207dc3e91c974d3ab7549c`

```dockerfile
```

-	Layers:
	-	`sha256:66837caac5b53686d0a5902ee6eeefd3d65faceb5a8e678a485c1559c255cf3d`  
		Last Modified: Thu, 30 May 2024 07:18:02 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:b121b1ec284faa85ddcb896865995c0a77e996172abda14b84bf44dfd16419ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72152978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48816ecd8dcd17e6434952e590b7f0e7022a0bbef3eb40d8777afc81ba8fd09d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:761a1ed8b6aff9e8d483d929102ec73068841012ed61fe2628c934c84759ac97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0307bd9334a4fee50a3a69d740342df83ea43151ff5540cd0c3b23b33b6256b`

```dockerfile
```

-	Layers:
	-	`sha256:60936c9ad58ccacdceb9d0d6914fb9cba21551eccda9671ed296411cfac69dd8`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 23.7 KB (23678 bytes)  
		MIME: application/vnd.in-toto+json
