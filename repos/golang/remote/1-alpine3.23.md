## `golang:1-alpine3.23`

```console
$ docker pull golang@sha256:d9b2e14101f27ec8d09674cd01186798d227bb0daec90e032aeb1cd22ac0f029
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

### `golang:1-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:217cb265b15f1bce711dda88e3dd2302da61b8b1096d6afe15727a7e96719dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64310638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce313ed0279d67e9bde51d7f99258da84088cb9b6d3d6d17ac731af364f37908`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:30:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:30:50 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:30:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:30:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd512c54db2cec0e90568bf0289158b823de7349175f3a3621163e770b4f4921`  
		Last Modified: Thu, 15 Jan 2026 19:31:15 GMT  
		Size: 296.1 KB (296086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:09 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd07550e32f74fc2f29bbf38b34a2138634737d53907ad72ea1f4f7923129de`  
		Last Modified: Thu, 15 Jan 2026 19:31:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ed03ea3711be07092d5182a39ed106aaae55cd2fbdbff90c178d3ce1faafe980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3894c00968bfd14caedee5a6f3967a009dbf6d48ae284090bab34eb2d3ff0010`

```dockerfile
```

-	Layers:
	-	`sha256:369f17089ab1f234aa1296059c60fa3bc0d1ceae46dbee3ca90a44d1af0f0c0f`  
		Last Modified: Thu, 15 Jan 2026 21:46:04 GMT  
		Size: 195.6 KB (195551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988e959eb828bfaa5236c89bf481701c7ba8116249bb69cd3a4c0206b7d4a030`  
		Last Modified: Thu, 15 Jan 2026 21:46:06 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:d657e960d465ac59aadf88e61ad5055b8fda1d31720533baf117431fbe807a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62939682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99b6b93e8f43fdf45cfbaae03a2e58817d1e33fb7c012009c78f7eef88c2c1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:01 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826cded2db4457d18ccde45d1148d778163c284ab192b47be22190df6ff01791`  
		Last Modified: Thu, 15 Jan 2026 19:31:22 GMT  
		Size: 297.3 KB (297269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9281733a6226838b038c2bdb015b61227dfc767db0d5160e59d01708503f8e5c`  
		Last Modified: Thu, 15 Jan 2026 19:31:32 GMT  
		Size: 59.1 MB (59073822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df32dd2d1c9739a4a386ae3c7570d64272629b8b46a9a5e0c5b5268cb3853658`  
		Last Modified: Thu, 15 Jan 2026 19:31:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:1971722f714ba859733954409616e0bd6205f641bdf7514d65d616f41cc87b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec14e5ca5816e606077b03700dccdfb7b8d1d6d6f7b1b54ff3ef177267e273f`

```dockerfile
```

-	Layers:
	-	`sha256:d49b1ed254e341a0a85335b5131d9189a9c27016933878b0e5ab60dabd3682d3`  
		Last Modified: Thu, 15 Jan 2026 21:46:09 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:95603c0dccc52ff00b731446393714898a13e441f35f29a3cc5e7386fcd7e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62649560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc264293de85378db937fb3f47fecbc3d765f89a8ec279327671c625dc7ca20c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:30:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:30:50 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:30:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:30:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5bfccbda235de71eebc1678f4b61e83bc7e1c82b96e98a59007c8da5eadf25`  
		Last Modified: Thu, 15 Jan 2026 19:31:11 GMT  
		Size: 296.2 KB (296204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:05 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd07550e32f74fc2f29bbf38b34a2138634737d53907ad72ea1f4f7923129de`  
		Last Modified: Thu, 15 Jan 2026 19:31:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:aa6d0fc8102e4550beafb6def1075232795f137bd76b61260519e028c1729d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba074efef5ee5abfaab952a294c77576ac4d6070f710c57507708fbdbf091c8`

```dockerfile
```

-	Layers:
	-	`sha256:733e2f9990e00ab178e9ded1b126397b9339d56b3eb074815b621e66116e2e1e`  
		Last Modified: Thu, 15 Jan 2026 19:31:06 GMT  
		Size: 195.0 KB (194955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58886dea4faecb61eaa5161737832ec363bb96921e6736eb0253f5668ac84dc0`  
		Last Modified: Thu, 15 Jan 2026 21:46:14 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a158d2c543ac399f000170628345b59094240f7d1beca25879049b1fc77cc518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62153939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ab77e15c4c412a833d327c98d5d4d113fd3fc5b4f4cc845b6d0cae12de8f04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:31:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:32:05 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:32:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:32:05 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:32:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:32:05 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2642103b7af4cd1da0e1674523e74b783480a3de73a8e4ab22c9b96d8b2393`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 298.8 KB (298845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:21 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50983d4c86cfa638eceb11ec552d5f66a2c2bbd7aff0f5561a8799011ae12cc6`  
		Last Modified: Thu, 15 Jan 2026 19:32:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:143e0f15fd9997be658ada50e5f386aac79f36968ff0732e53d375d10829d69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3189838c679d6345e9d42bbdfa782d0f69206c74e8851f8e7b35d8d626ddba8e`

```dockerfile
```

-	Layers:
	-	`sha256:d203b77ef673dd23b810776bed80d681e9029a93fc06abeb3d9f05c891c4739d`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 195.0 KB (195005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280f92faa1e98fe059c829e4e9eaa84b5ba13d2d2d9a5bcf035ab25203d08076`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:a96582f2c7fe446b004c3eee1acdc7566d26838a2e3f8ce025b38ed0bb001ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62854680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f0f9da3f3a476c966df4fb231fe6ddb00e210526f5d97e7b7b2794c17bc274`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:32:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:32:07 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:32:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:32:07 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:32:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:32:07 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df847da8fdd350898a027b4d2bbc6a0904dcbb97585908dde525f5297001258d`  
		Last Modified: Thu, 15 Jan 2026 19:32:28 GMT  
		Size: 296.7 KB (296668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd402dbe928e14f69063c85f23dc6c9bbceb27e04cff93cac6dc77cf1a8f6be`  
		Last Modified: Thu, 15 Jan 2026 19:32:23 GMT  
		Size: 58.9 MB (58871754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9c9e7c5c461641c5d209e42e5c5d1a8700b1eab638c55db763be05f6a4f7`  
		Last Modified: Thu, 15 Jan 2026 19:32:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:3a09816c16c6379ec45389997ad0ed540c0872837d186ae7e4349ec0a87b234d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8593df2398d4c367767e18328f66e66723608c605f0f105c928d821e3cbed7a`

```dockerfile
```

-	Layers:
	-	`sha256:f69c86587c913c1ea61fbdaf945409d4b64af8bc3f9ba6738bcb5646ed88a44b`  
		Last Modified: Thu, 15 Jan 2026 19:32:23 GMT  
		Size: 195.5 KB (195492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335b4c50e1e81d98ef97eedc4efb5ef331f3eef55097b7f485f7024c3b32c502`  
		Last Modified: Thu, 15 Jan 2026 21:46:36 GMT  
		Size: 26.0 KB (25970 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:0fdcc33621f888122638505c836923fc5cbc8fd77786f4ed7c7435000d82250e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62262440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f9fb59f226b3eaeff79f4ee7a79cec2f3f55992a6893bfca4d07be0f611c36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:15 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:33:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:33:07 GMT
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
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:34 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045155b1e1d9bbbcbf57d9a4a1cafd9a01ffd6914acc2a07aecbca999bcc10a9`  
		Last Modified: Thu, 15 Jan 2026 19:33:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d614adbd8bcf5b5d4701c61f20fc73457946f12ad0a87c7e81fa15a2c0eccd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdd1af9cd0901c2d5f53283c1d36b24b10036e245dd4dbec54048cbdd3e78c9`

```dockerfile
```

-	Layers:
	-	`sha256:55451758b84577fc1bfca054a821cf2d39d1e03730b0c1696f02df5652b408e0`  
		Last Modified: Thu, 15 Jan 2026 19:33:33 GMT  
		Size: 195.0 KB (194972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3fade9c0798d805f73fdec29d06aaabe44844e62631c6d861270e95ac8991cf`  
		Last Modified: Thu, 15 Jan 2026 19:33:33 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:4dbab6fca3366f9d80b88b43282fc60f5ed87208ceaf71d195660f816c95ec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62552259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca1e0b285c262993282e867740198b74678f05b480ad10b60edfe6f0f7708ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOLANG_VERSION=1.25.6
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOTOOLCHAIN=local
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOPATH=/go
# Sun, 18 Jan 2026 23:11:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Jan 2026 23:11:45 GMT
COPY /target/ / # buildkit
# Sun, 18 Jan 2026 23:12:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 18 Jan 2026 23:12:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:16 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76383bda51f6d2301c4d245b282d3ec6e006fd6e4d52961e3dd0dba3364c9182`  
		Last Modified: Sun, 18 Jan 2026 23:14:35 GMT  
		Size: 58.7 MB (58671645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7874777c786fe8e291d896218d7b8da26656809b8399dc8c56f3ea70c1caf`  
		Last Modified: Sun, 18 Jan 2026 23:14:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:0b0f1f0e0b4f8769b08149ec465b545f5d3d2ec8f24c8a861e89f4c821a9fa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0dcbc9e79dbfea92564acbcde7942b51dcac78336c90cbce7aaa291c958111`

```dockerfile
```

-	Layers:
	-	`sha256:7a672897f8362ff1405e5ad400c0faf6a6c2201cf829ca5e34cfb888e832949c`  
		Last Modified: Sun, 18 Jan 2026 23:14:26 GMT  
		Size: 195.0 KB (194968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e7a39de82fcd7f3439cc2d21ab511ead5c7cf9457ed897a0ba5982b4f1234a`  
		Last Modified: Mon, 19 Jan 2026 00:22:41 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:df0861018333be4bcafca421458fd9f8f986039d4f5b550003ead2441086b65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63512838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1916629c7d05f684fb97f961b523c2a77b020eabad1606d2e5dd8d4768597245`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:07 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3921107d409df0e99b4231287ce5a7267626ae3ee2e9fb513d5bf7afeeca1`  
		Last Modified: Thu, 15 Jan 2026 19:31:34 GMT  
		Size: 297.2 KB (297197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:47 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90185933a9c8fe485ccfcc7f6b95b0a6a173cadfbb514d9e9955fcec748dcf6`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:063e4b197feedd83ebec0371c6254abe1254a7823eb2bdbe2557354332c054ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 KB (220753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e7060b58db1d19639ff493fa85118358e1db844945f905b013a176ddbb76df`

```dockerfile
```

-	Layers:
	-	`sha256:ba3de884f3aad7f6954a257a1a381816d05099642e5ab4e92727bf67045a8852`  
		Last Modified: Thu, 15 Jan 2026 21:46:47 GMT  
		Size: 194.9 KB (194900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf23e9308b9711c26f58b877ecb72f6e2cebb535736876162ee03b6c8056cdb`  
		Last Modified: Thu, 15 Jan 2026 19:31:34 GMT  
		Size: 25.9 KB (25853 bytes)  
		MIME: application/vnd.in-toto+json
