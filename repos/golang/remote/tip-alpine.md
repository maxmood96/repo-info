## `golang:tip-alpine`

```console
$ docker pull golang@sha256:a8668b5f84cdb18f455c53df7ddc09153c737bf5fb6b26d9a7983f751d221a7a
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
$ docker pull golang@sha256:68f6b7090a8186ea8a662252f754f387e075451f4cbb8179df0999b00f0cac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99186278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e23e750b9ae34bd065640a9627dea28d32357b02cd29397093edc9c20cc86a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:19:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:21:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:21:05 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:21:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:21:05 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:21:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:21:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8346bc679b90ee20d9ed40f904d72c249c5bcc9e70a9131539106a8b43dbbd00`  
		Last Modified: Thu, 18 Dec 2025 01:21:27 GMT  
		Size: 296.1 KB (296075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc02f84f9201c7821773dd34545e63ce7af776f9b234f6a13b2589fafa66eab`  
		Last Modified: Mon, 15 Dec 2025 21:25:12 GMT  
		Size: 95.0 MB (95029942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0f97734736aede261e62097f844a743ef959dd36428ecf1e5c202f0e5b7936`  
		Last Modified: Thu, 18 Dec 2025 01:21:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2831f6bafa1f8b5250d30647e4b705586b444dd2a6bededfd83f71251abef99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291c4dae2f4c001c051be92b5f7e4e1b01689eef1ea355368791e79f0784b037`

```dockerfile
```

-	Layers:
	-	`sha256:0769b67a55ba9b3166254a338c73b9dce0d5b874ebb581f116e17e91c69f3b03`  
		Last Modified: Thu, 18 Dec 2025 03:25:19 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece3256b33cf01c73d524c2446bf9f474f00fd5f989b90c338acea52df8c8abe`  
		Last Modified: Thu, 18 Dec 2025 03:25:19 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:0602fcee66b563a4e3f30f3576ab4330c4bd3eda7539f15161472f78b016263c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95237567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41390dfc4a712c569f48af9b201c6ec2410698ed61c01ac07800e4fc880100f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:39:06 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:39:06 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:39:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:39:06 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:39:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:39:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad105ceefb29a5f03c3fb1da61d24a5b81080860f044bd6f725eaf3aabd355e`  
		Last Modified: Thu, 18 Dec 2025 01:39:27 GMT  
		Size: 297.3 KB (297258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0cc28daa6cb71c3b81eacc797539f92a25b64ec51c9f53341c37ef04e417d`  
		Last Modified: Mon, 15 Dec 2025 21:25:29 GMT  
		Size: 91.4 MB (91371719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c1f0061aeb7674b4627caa33189ccc5c07477850da9aeafea37745b7fd070`  
		Last Modified: Thu, 18 Dec 2025 01:39:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5a0621d5704392eb9d3f203bcede5d11aee3736051a759d9b0f79b07a86a13e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4eeef1dd89de15525653649de4a63c2d9d22178361c05c34e8aefaa9f987d2`

```dockerfile
```

-	Layers:
	-	`sha256:867e09e98fe2541bd493ea3c3fa94aed3adec5f19e6b80f1bcb0c9984c3b2c80`  
		Last Modified: Thu, 18 Dec 2025 03:25:23 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:f92176a3c5dd01b77611670043e1f2e244dd4f708d74502c6c450c3e809e2cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94676971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080ef4db41372a6d2275a8adc169ad75423844be410403676e7d423aca2d2149`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:38:56 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:38:56 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:38:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:38:56 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:38:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:38:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1852698eff83b9141ec3c3bb4a339a83862ac4d34485268cbe4b6b255b66eb`  
		Last Modified: Thu, 18 Dec 2025 01:39:21 GMT  
		Size: 296.2 KB (296194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb87a632660b1037516c680a04b7758d1bccc030a199d5938a3d13de229878`  
		Last Modified: Mon, 15 Dec 2025 21:26:06 GMT  
		Size: 91.1 MB (91101231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80caa4b79f4b68a939fb0b31d34bf6563e48fc35f93cb17347082a1c2e8faaeb`  
		Last Modified: Thu, 18 Dec 2025 01:39:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:90411836a9545000c15203a4122a3e6789250a6cca05182d15f8a1630fbe860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbbf4e1e87348e0daa63ccec2274bbc1e2a4b7645defecd0897cb8253833110`

```dockerfile
```

-	Layers:
	-	`sha256:c7d1444787e2204692aedd3ecb8434ecb9d30a4ca2ae1f437a8704cb16be8e2c`  
		Last Modified: Thu, 18 Dec 2025 03:25:26 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649c78690e66765577c78ceceda70afe2711466d36a831e8341df657ff9b4eb4`  
		Last Modified: Thu, 18 Dec 2025 03:25:27 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:42ddf9f98336b4d5253d2b7cd93ec6ab4768a7373aa225744294760d88842af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94603117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06227f7bb6f53f731934b54fc890ab8855d70613e78f9f7dd7398f155c4c4124`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:28:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:29:43 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:29:43 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:29:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:29:43 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:29:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:29:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d062f9abc4f2601f024607747e031dadd390ffcab62558482a99237f0e99c`  
		Last Modified: Thu, 18 Dec 2025 01:30:07 GMT  
		Size: 298.8 KB (298842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7781f7b0020f1ea08137b4961d1e1c8dffbf5d0dd96335fd03fec85f64136`  
		Last Modified: Mon, 15 Dec 2025 21:24:55 GMT  
		Size: 90.1 MB (90108378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16a4571b969009edd28b9466c839d1ea5f980b92eeb7e84e01f9ef5ca03cd8e`  
		Last Modified: Thu, 18 Dec 2025 01:30:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9c4fd0504721f6e1840da6baf0fc96efaf2bd9be542f951f45cb09daa6a5ef56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda7bbeef847fa150fd810700c8d4dfd7460029abaa12a7cbc68c4485b6c47f`

```dockerfile
```

-	Layers:
	-	`sha256:682cec9f3ad246d5c0597f16c7a64de9c412cae301dd40edefac0f57b6c2b7b5`  
		Last Modified: Thu, 18 Dec 2025 03:25:30 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f25547e449c38624e9ba9ed102371d01d46fcc53d7ead4c94687f29c67d24d7`  
		Last Modified: Thu, 18 Dec 2025 03:25:31 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:3aaa73c56bafa8932c889695820526f95cda8777869b6c738c93dc9cb643d3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96901248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa32ebdb4410bea62cd732007228a681bc45f1d80798e356074bbf7738c3848`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:17:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:19:11 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:19:11 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:19:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:19:11 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:19:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:19:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c73076ca0895a59d4ed43c82e81f24388428d8f38726746b1c0b612e05778c`  
		Last Modified: Thu, 18 Dec 2025 01:19:32 GMT  
		Size: 296.7 KB (296657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f38140e210287454904f48ab9f4aea2db0ef2d57fe485fd6478e18a07aa5b9`  
		Last Modified: Mon, 15 Dec 2025 21:23:21 GMT  
		Size: 92.9 MB (92918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5082e8f68473233c579503de9154e20d76eb5810b983950d4edfaf0f75865b9e`  
		Last Modified: Thu, 18 Dec 2025 01:19:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a75ec734eaecfbf0c525f5fac011540eff32816fb79201db6b9b7bae493c3bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfb01fc762dcc7737006bfffb545d958aa3c5afe35c22763b7dbca2c7a43702`

```dockerfile
```

-	Layers:
	-	`sha256:832b24b32b8d3bafee98bdaa759574b7d473416e41001244ceaac800055d66f2`  
		Last Modified: Thu, 18 Dec 2025 03:25:34 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834f820a513cdcceaf59fc34fd5de657824c5f62fcc465de1c7e1ea0f9f14fee`  
		Last Modified: Thu, 18 Dec 2025 03:25:35 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:dfa129c435efd80295bff2c0c912aa68a96094b73e9487034620e26c7eae2876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95776676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fddd5301d0908eb29b43383dbbd89692d313fd4bea58f2f413fb8c4abdcf77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 02:49:04 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 02:49:04 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 02:49:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:49:04 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 02:49:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 02:49:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14547495cfe8d3d44ce957beb44799d810dbc881ef14c6f75d1efdc8e9917f3`  
		Last Modified: Mon, 15 Dec 2025 21:34:40 GMT  
		Size: 91.6 MB (91649505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f129cc78c1e5c47152d8e37f9e77dda47f3c3f3910680b5b416c969f6cc11`  
		Last Modified: Thu, 18 Dec 2025 02:49:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:59ab6ea89a3e73285cebe404b9a9fc44c0e203873b626db37ea033ac153517dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7321e094535ac507e35619f53cd21b51fe54e8d09c5e5ae7e6fce918a2b90348`

```dockerfile
```

-	Layers:
	-	`sha256:88769203a9abddd81ba5b3baac04abd334d465088acd1f2a7c1359e0ccfff727`  
		Last Modified: Thu, 18 Dec 2025 03:25:39 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c03d26555b3c5fa2f0a5aa275f3c671f7fdd97875e7bf4e699cb7d3aa5ba89`  
		Last Modified: Thu, 18 Dec 2025 03:25:39 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:b72361cf1275aee5aa853e20dcec2625db35d69a8c22385fdff48f81d662d56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96169692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b776260175ab3a88ddbf8e81c345ce5ceaaa63c6cd70b0d479a60b5b209578d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOPATH=/go
# Tue, 16 Dec 2025 14:08:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 14:08:40 GMT
COPY /target/ / # buildkit
# Tue, 16 Dec 2025 14:53:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Dec 2025 14:53:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2260aaa09ba7162340fe5926c0fe305f447e406ba4020d7a84ed8048186cd`  
		Last Modified: Thu, 04 Dec 2025 00:35:11 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ccfd6d0019903e9f30a7248d0011153e90d92f7a748480439ea4f6363c5dfa`  
		Last Modified: Tue, 16 Dec 2025 14:16:03 GMT  
		Size: 92.3 MB (92289512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b1aee4eaccef7eebf4ff1c618e7cab730ced64d0093d134367706ce96d0e55`  
		Last Modified: Tue, 16 Dec 2025 14:54:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a8a38fb4699c2c09e6978680e5aa9441f082170bac10d2d5bd63a9d9a942d2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2376cc56a4a296c0ad01e4dc23f87aea08c7c7480164a4ec3570d4adaddf1e`

```dockerfile
```

-	Layers:
	-	`sha256:68b324447979b896997f5f6863914da4ed1a8607ec0bd9dc1c537690d56ee41d`  
		Last Modified: Tue, 16 Dec 2025 15:23:43 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b57d263cc83ccf95e5522b7993e0dc6f5b7ecb96da55fd40558b75e0dc1a1e`  
		Last Modified: Tue, 16 Dec 2025 15:23:43 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:45ce3d5eab37c4c8305d06bb51e1706f1121ab078e5ca0d978cb7f2246b52620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98219600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e98ac1aba360ac291e77ebafe32d96ca932b7814f3a1dcafc1ed1186eb26154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:10:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:23:24 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:23:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:23:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0495a965cff38fffc5035354b088c3d76314e583d7e3003bd53417892d478`  
		Last Modified: Mon, 08 Dec 2025 20:10:51 GMT  
		Size: 297.2 KB (297177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a1c518cab5112d07a0a3193c5ca3ef905e28d8e262915c8e207c186ea2395`  
		Last Modified: Mon, 15 Dec 2025 21:24:04 GMT  
		Size: 94.2 MB (94198456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe83f6ce0ccd65e37520a4e1571cbd5e865ea2d50329c47c67b99b3d304b5e`  
		Last Modified: Mon, 15 Dec 2025 21:23:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c512fd29691ad611c7ca636cdc699cad67857730c816c18f19fbc1cda7a5c291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26e664a7a38678a9104d3c2b27b098a1dbcb43b63e7f895a38b4fd0aba9b62`

```dockerfile
```

-	Layers:
	-	`sha256:1a797738067dccdd70f27cc3d0762aa44a64e0208113aaf4f74f10e45960a811`  
		Last Modified: Tue, 16 Dec 2025 00:24:15 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4153569cf7f035b8be9a715d30aa065c20b7e6058a0ed75a26e4316f60e21a23`  
		Last Modified: Tue, 16 Dec 2025 00:24:16 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
