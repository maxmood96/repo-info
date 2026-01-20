## `golang:tip-alpine`

```console
$ docker pull golang@sha256:740884132d25bb57ef2f2464984f38ad4021714c9c8764a103178a888fc7f20f
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
$ docker pull golang@sha256:1ac3d30f9af28e3783a527afdb81b06f2d23cacd6fe3b1389b64a5519e74d78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99208198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17774990179bbd3c1c716de330708b0b9c3ae672c710540dc958205e86c2ae2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:43:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:44:50 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:44:50 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:44:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:44:50 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:44:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a8c966669f93a193835cf66ef8a66221e7c838b59d3e2d35a2552cbb19d98`  
		Last Modified: Thu, 15 Jan 2026 21:45:11 GMT  
		Size: 296.1 KB (296084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:04:49 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b9eeca84b835522716ab43a7be6508e29103f154bbd80fde8cc7ee4984bf8`  
		Last Modified: Thu, 15 Jan 2026 21:45:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:828b3473a0b1f8097fc3585bf6e9e952c3943f9efbc600268ff12a14b938abb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767d20225798d41588ca287f00190659cc521c59022d2d0b95901051ebc01ea`

```dockerfile
```

-	Layers:
	-	`sha256:1ff9b2ceed65d064ccd8b1566b4107dcf05833f4e76dc7a78868f55d9fa66236`  
		Last Modified: Fri, 16 Jan 2026 00:26:12 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c1f79aa4e5c58c40d852a9d093a8eb17a4a35012a1f5db5031c14593d436df`  
		Last Modified: Thu, 15 Jan 2026 21:45:06 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:97be738817448d93ce6581a781b3f31c2ee4d01deca0f747a00fc81bd58ac527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95266874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addc536380320b6b05187f06f732936cc3611644e34e79803017cdee7abda85a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:42:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:44:44 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:44:44 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:44:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:44:44 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:44:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:44:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b80adc792bf6b76abb73918ee0fab55376ab9c45c58c508ecf24858e7dd604`  
		Last Modified: Thu, 15 Jan 2026 21:45:06 GMT  
		Size: 297.3 KB (297276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fafe2d1996fb8d6337cd2dcb6acca5b8c22581c5ef4fda1f58bec46f2b5c18f`  
		Last Modified: Mon, 12 Jan 2026 20:08:13 GMT  
		Size: 91.4 MB (91401008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79928608291634dcc5c60722ea335518855ec19357ab66a4499cad18a95f819a`  
		Last Modified: Thu, 15 Jan 2026 21:44:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6b8d7ac4df91f306013ca79de61fd93ffc5e2695d817c1da3bd2551d23b8931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cd19dae3dbb1c39dadfb5dc00907a6fd86c7f8909fadc17edaf1e9644033d8`

```dockerfile
```

-	Layers:
	-	`sha256:002973bb19a957a8dfcee8900c3cf48fcb0e241c422083aa9c7e9da1e5768364`  
		Last Modified: Fri, 16 Jan 2026 00:26:16 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:b066e85da815be024965ac54a2089feadce87cabb8795262adbe61014152b847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94710136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c30a0a18d3a175cfe1ec3c9c9cc513fbf4505f9b0ad5d25183751cb97ab68e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:45:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:48:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:48:09 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:48:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:48:09 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:48:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:48:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a4ee94697b27db10ec32442064518bdb992a2e33133ff6ae4bf6387573795`  
		Last Modified: Thu, 15 Jan 2026 21:48:26 GMT  
		Size: 296.2 KB (296195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:47 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4092feeeeb30e33748d34368da26869464f9e6cadcece46f92e7d003e6915b53`  
		Last Modified: Thu, 15 Jan 2026 21:48:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:55c81026e79a28e00a03c7f6929e27c1e38f8fb9c82157115c81324f7da3838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d9d965d76eaf90000b02774da040a186e53dccfe91fec747823da13caec5ff`

```dockerfile
```

-	Layers:
	-	`sha256:367932ac08f33ed0c31faa7f0b031fe378aca9c4ab9dde3c8c7481d1a56195a3`  
		Last Modified: Fri, 16 Jan 2026 00:26:19 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164b0c92923f3d60f0c0836e31f449a693bf9788b207fc14d8294b04a0e7ac21`  
		Last Modified: Fri, 16 Jan 2026 00:26:26 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9e268e4811163b7be5ea97884f02651547dfcc125803d8b2d09376f8c8615061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94632056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec89c116a3ffc2d229f656542b342612e0bed1af78d3e720668e971e6a7fb85b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:44:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:46:40 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:40 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:40 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:46:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:46:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1c9d19fd22a63d12997d368a4fffe42e7cd0feeaf0a1050e4b5bc1d390af0`  
		Last Modified: Thu, 15 Jan 2026 21:46:58 GMT  
		Size: 298.9 KB (298850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0be75f244433c4779b5f63e3d917ba4b261bc0fdfbaf1e886c462b6b45ff5a7`  
		Last Modified: Thu, 15 Jan 2026 21:47:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:94c339a47df2fac80f5b7a88c3a385f8a07742b5986b481851ef3562474da124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2676d312893819fb21e41308fe5fdd0b29b5dfe557bcddc47aea24bfc9b7898`

```dockerfile
```

-	Layers:
	-	`sha256:62b2cb44dea685faaadb0a7597322b2e98da22bd565c7d052add83d224f3701c`  
		Last Modified: Thu, 15 Jan 2026 21:46:58 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9805fa4b0037800b11ff9cd154e6a0abefca83d9bfc74dc37e75c94d7b8b9e`  
		Last Modified: Fri, 16 Jan 2026 00:26:30 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:8cd1b3397bc0760b75076999c27a56795f59e80d7ffed41664bf390474aaafd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96928472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fc9983d304fae332fb5b4af18bce54f2e7de7f916486334267cf3bd34bdadb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:43:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:45:39 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:45:39 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:45:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:45:39 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:45:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:45:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639813b40c9134d08a7b6d23435e671c55539e60c1aa3aecfb3c7fcb4a8553d`  
		Last Modified: Thu, 15 Jan 2026 21:45:56 GMT  
		Size: 296.7 KB (296660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:27 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bf3cf74d0df092c2bebe2ea24098f89961f700772fab852e2a187a7a42d677`  
		Last Modified: Thu, 15 Jan 2026 21:46:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:18dfed80b2a6a6dd06da58215f4700d92ff430efe79dcb4eae4be62869228577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28e10c26aabf557f6659289243705fa47aa13c711a983960532024026de4846`

```dockerfile
```

-	Layers:
	-	`sha256:a1374d650a322e7f8900ea87fede46c39a6c065d5ccfbadfb4804d0464512b4d`  
		Last Modified: Thu, 15 Jan 2026 21:45:56 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5dca71353212670cc8890f217688b125ad8b0f18bea61625db7d2f58240f73c`  
		Last Modified: Thu, 15 Jan 2026 21:45:56 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:702b64c1775cc0455661e628f68d4565556bc821c75534eaf4d781254bd3055c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95811091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd7a18c3efdd04d20e7d24e4f6669abc600790829802d31eb70b113513f1b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:52:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:52:30 GMT
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
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e7d150401bc06e61da1573622e2ab3fdaa26222e69815b78d5664117909987`  
		Last Modified: Thu, 15 Jan 2026 21:52:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f595df73bde7f0030f7bc966612b3cad6937e227c604b39d69b3577f8bbbc94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e25b7063647da041e918bf970a97c7789b09161369cc8f477081799a4059b8`

```dockerfile
```

-	Layers:
	-	`sha256:62b54019c3df66f0edecc57d41f099e36b50c59172396bf098f325d78aab2db8`  
		Last Modified: Thu, 15 Jan 2026 21:52:46 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f32de090a786d023f10117486764a66340ed8319b6a95c3bce57a9e689036cd`  
		Last Modified: Thu, 15 Jan 2026 21:52:46 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:1112467c6f8dc6c131eaaaf3c10dd61aa4efea6d864503705a777f9d388cf2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96196492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cb3ea042884f7dc2d6ff19c36b19aee9a4210dff0e30b74856dd651809dbbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOPATH=/go
# Mon, 19 Jan 2026 21:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 21:38:33 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 21:38:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 21:38:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:24 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a3cc83856871e3a177f0a6b27128217f73d5993c49818bd1374bd92a6bcb48`  
		Last Modified: Wed, 14 Jan 2026 03:12:04 GMT  
		Size: 92.3 MB (92315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7242b94826dd420ff8c2d4627119cbfee3a19b68631deed9e43378fdc64a07`  
		Last Modified: Mon, 19 Jan 2026 21:41:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dddc3dc1a0341fe9af936a10147a2d07116f8e88d81c0c7e2b70091c61b6bd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410373d1530b7ced2347df60dd704f87f0860989be72439e903566ddd260bfe4`

```dockerfile
```

-	Layers:
	-	`sha256:2ddda32af16ff3032981d9b9f3eff0f3a6e583b38978a985d0b01abc6efca828`  
		Last Modified: Mon, 19 Jan 2026 21:41:47 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40868836c9697a635b369afbea4702d5bce3da5c83bef6056e5ba3954043bb16`  
		Last Modified: Mon, 19 Jan 2026 21:41:47 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:08e8f97b397149eebb126dbe85c23683b1dfd8dcc21108c049eadd005a72ecf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98251563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7648b4f5b2fe66c169b6b5ad4ad1332751bde9f39c4528fb63de14b2d4081774`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:47:38 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:47:38 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:47:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:47:38 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:47:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:47:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:21:03 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dfdd4a62fe49efeb3c0d33cd231f1d8c03f56fadf239b292808a4d2b7fd334`  
		Last Modified: Thu, 15 Jan 2026 21:48:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:78ce518a0262bf14d86c96022db4628ae7f5ec784f3c4ba03641bc6ef2d4c2ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4056b52c41277b37bfb3f2ff0f999592fb085817c44d63f05032f01ba89f05d4`

```dockerfile
```

-	Layers:
	-	`sha256:28bdcdc8863c1105662503d472c9b6771463b86c70475a3b2243c9f2d6efc1b7`  
		Last Modified: Fri, 16 Jan 2026 00:26:43 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0851ae6cf591feea632ca40262550f516589cf1b42008f1c75e3ae119d58e618`  
		Last Modified: Fri, 16 Jan 2026 00:26:44 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
