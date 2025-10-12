## `golang:tip-20251003-alpine`

```console
$ docker pull golang@sha256:800ecc96e27e3e1e34afb22f1a713022cdff2969735811880f6c8888bd86e3e2
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

### `golang:tip-20251003-alpine` - linux; amd64

```console
$ docker pull golang@sha256:f9ba3c0d8788c76374f47831b1ea1aeb3af095fb610c84350ebd503b6f98b2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425cb5fda151c68a6fffda36f0729aae6dce6980519f0a5c8099d346cb0bfd04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6d56e11053706c324d1aed9422637a5eae839388b3a34f2acd2108e15e8bfb`  
		Last Modified: Wed, 08 Oct 2025 23:40:03 GMT  
		Size: 291.2 KB (291159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a225db047f32dbd84f4590f2b6c32b9ffa9de20cb9b08f648341a3ad3cf52`  
		Last Modified: Wed, 08 Oct 2025 23:40:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d70f3eb8c4f6086c737a10d62ae37e8b49d0c18622840f53f04d42c58166add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364cda6a411d2358f63062f98314514a4a317068660123d83f945e664c5d316a`

```dockerfile
```

-	Layers:
	-	`sha256:27f728cc18f8a8f04dd90f25f94e2d9becf41c30a5e2e0d50a926ec6a9abeecf`  
		Last Modified: Thu, 09 Oct 2025 02:24:03 GMT  
		Size: 194.1 KB (194140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea83d94915eb483a9e9f9699ffaa11ac365dbdd47305870e0027f4a0eb2a4ad3`  
		Last Modified: Thu, 09 Oct 2025 02:24:04 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:4c3c67faeb9a7fe2abe600a875b248949142b7b114faba9c8a204e13ae2581c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85597718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe2ab3c536874cfdbe65964a818d2313d45fd76f364e080d2cc3ad1e7e5f950`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb71e16498837f48c0e0d291d7500f542d73ab453fb47a2414bbcfe6e3beb0`  
		Last Modified: Wed, 08 Oct 2025 22:11:05 GMT  
		Size: 292.3 KB (292318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ca929e1e82e3da2a8d3fe64f9852116fdde16db4405daccb287d008513ea4`  
		Last Modified: Mon, 06 Oct 2025 21:06:14 GMT  
		Size: 81.8 MB (81801162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a3be72d481ca99c3c2d7998283904fe2fc9d072198c404eb651179d999ea9`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:78f65e9db2fcfe5606adc3f330e781a572f2ba3afd14a71a7f8f53424171e791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb3f9474c448519ce4059280e33ffadd24c5732b0c2d4a73c372964c173f05b`

```dockerfile
```

-	Layers:
	-	`sha256:9e3f122c79c62dc4e5d89b0ea05be9e20023cb8fff39530ce67d79e1db0e8b1f`  
		Last Modified: Wed, 08 Oct 2025 23:24:38 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:0ee7fe54ed3f90050d1a225db163c3f15b312f37938fdf80b9fc2c38fd5ba9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85062810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17785a25227f5d9d26ced4e3be76a1ae36199573f110b572c9137e6d3c15dec5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d6a2039c5982f2c099995d87813c6b0a98a90f1cc4fef437eac357d308456`  
		Last Modified: Wed, 08 Oct 2025 23:52:01 GMT  
		Size: 291.2 KB (291206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a4fb268af1d4a7218f40758b666caf1786ae937a3e5cae0bc495aaf5f82585`  
		Last Modified: Wed, 08 Oct 2025 23:52:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:efa2bbf003896669bd81b9c48c97f18375fac5cb129bdc800e4859224afb87bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2ea52b479a32363b9bbab9d6ea7cd35ff90ab244551d3b05c5f5db69dcdc9a`

```dockerfile
```

-	Layers:
	-	`sha256:5ae82bd71de0e45b534db7d1ee2dc007b75c353220bb832dda71cb5b688e3b84`  
		Last Modified: Thu, 09 Oct 2025 02:24:09 GMT  
		Size: 194.2 KB (194162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85322ab05b714119134fb6483497e3fcd7e7fbcae3200c1ba42bc9538c948c47`  
		Last Modified: Thu, 09 Oct 2025 02:24:10 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:81d5c20c9543d0e0789e0b87ed8c9c069ddd945f5130d4db491d63ce2cf6ae02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84964168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35507b06614488ca8bbbc66101f38b1fe3963f230b08d3e10bd29f95df0f95c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e5fdff75799ee65513de89c53c54729ff95530bc7c9a8a4adf6507287531df`  
		Last Modified: Wed, 08 Oct 2025 23:19:50 GMT  
		Size: 294.1 KB (294091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77588204035dac43d8c7a701e00358863db09814b22c1a312bda83555f6fc5b6`  
		Last Modified: Wed, 08 Oct 2025 23:19:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bccc5d1f7db494e79959a23a635aa70cb74d58b80d0d82242430512418934274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 KB (219493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3190e0be889efd9bb93104cf169fb6220416ee51840b5326f6a4aa3778fae0`

```dockerfile
```

-	Layers:
	-	`sha256:6dd230eb5d250f3707d937cd73bcc2d714ad6a2609b4f3122b622ec4f48189c9`  
		Last Modified: Wed, 08 Oct 2025 23:24:43 GMT  
		Size: 194.2 KB (194196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85225971ffb157c6a8e44652dd726b7fd031c056a98204e190462e398c5428cb`  
		Last Modified: Wed, 08 Oct 2025 23:24:44 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; 386

```console
$ docker pull golang@sha256:21b12ebb35df84777d2d21426a412991ba8447b140ad68c9bf1458aaa33b46c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87056184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef2659688e72b1b48a7966f8f33baf065f73280442c993ee8321803c136507`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba57c3504a135e148a8137fea542dc0cfc1322eb4bea926373d68b1e7be1a18`  
		Last Modified: Wed, 08 Oct 2025 22:22:19 GMT  
		Size: 291.6 KB (291629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a1b609ee72d4061a430bbb8dedffd6d2f13ae0f08f98500436d98dd9614588`  
		Last Modified: Wed, 08 Oct 2025 22:22:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:17e46ec35e0ccfcd9cff34c9ab2e9d8d249487402bef1f3326edc2727a2431bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 KB (219196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc2493ffeadfdfda67c4945ec206ca881e67f76dc68c5fb877d988a50efebf`

```dockerfile
```

-	Layers:
	-	`sha256:446cbfbf5a147b14b0daab33635e2fc650622bbbf4df9b00b884c4e108946938`  
		Last Modified: Wed, 08 Oct 2025 23:24:47 GMT  
		Size: 194.1 KB (194101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb797ea53a28e573fb60d358a2fda28f83f59dfc2aa5c8560ee93aac2630263`  
		Last Modified: Wed, 08 Oct 2025 23:24:48 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:0e1ec58f1bba9b969f169e433a19e146dee84bf90f0dfef37fc7d1b6bf2537e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85894409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103df350bfe0eb7aa3e123ad15f460799c689947e423a7f6f2685f97856cc7c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34403a3833161e7317f5f43c031b3114df383a82ea83c5851edc4d5c8b921a`  
		Last Modified: Thu, 09 Oct 2025 04:12:57 GMT  
		Size: 294.6 KB (294579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b417a178381cd9043f88ddd27873050cd89a4596091c602032cd923a7d21934a`  
		Last Modified: Thu, 09 Oct 2025 06:07:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c72d7b3b9e28fc665080230f01d4e2b6d487358d0dae9bd77f9b3592919317e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b62f1d6dc786435be378c5e579bb61aebe2f4c3f5522846f78353a865c1784`

```dockerfile
```

-	Layers:
	-	`sha256:d881abd840c41da7da0e0a94d6d65e07b20cb54651f49eab6a68488f6378bfab`  
		Last Modified: Thu, 09 Oct 2025 08:23:38 GMT  
		Size: 192.2 KB (192237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad02a46a0235e22bbb3aef17ab2943f59e70ace56a6d5d063effd24dd37bcb7a`  
		Last Modified: Thu, 09 Oct 2025 08:23:38 GMT  
		Size: 25.2 KB (25195 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:6c7a2e45e669e5b57373db7d2dfa54b60304f0a423ade4073ac8e397f1633290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86038454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6bdccfca802d3182be3e30763847e4106233e8b717c72dd725f65f3cfbd2cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 18:59:57 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc4f79972d3401fde161bf76b9618d80cbd1ea7fcdbebdc630185f4cf612cd`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 291.6 KB (291608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7013078b33acf26229a2526e4fd4d754f4be2072520e015f94acacdb5d700e09`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:945b1878e26f6c2d84f08d2d5421ed7f95ce4b93f101f9c5848df30ca1ce38ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d9ffe93531a480551c18fc09a3ca63f7c75af3d8bd270b5469eaefc00608d9`

```dockerfile
```

-	Layers:
	-	`sha256:5cfabb3d0f79fc70b5aa7e76cfe0d5513c2d0593781a3ad9c276bbb486cf7c17`  
		Last Modified: Tue, 07 Oct 2025 23:23:39 GMT  
		Size: 193.3 KB (193316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247fc38600ac27ed9397efc20d1222c97f2fc882f53bba03035169076b9d1522`  
		Last Modified: Tue, 07 Oct 2025 23:23:40 GMT  
		Size: 25.2 KB (25195 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251003-alpine` - linux; s390x

```console
$ docker pull golang@sha256:440e9b278c5cd045ebb798f4ec263a0f5d6e4a3400a99e588d0a7645c74c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86995561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88525ba918094080e931a936bf6e45abcd4da5c332960bffb32030d9027392b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2de0d30ada31da192f5016a4897bdd65bd1ab1a8a13dcbc1a8bf1e887eba8f`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 292.2 KB (292158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e761818fa418502102920fe969da99f93163aae8ba0e75df0ab3827977da7915`  
		Last Modified: Thu, 09 Oct 2025 08:23:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251003-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:48bc28923b0d293ef92e9da0162ff57d04bf1ebc33d0e5775e3b4a3edd9803d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4837e513d4d8dffd0d82c37e57064083ec8530c8f86fe68a0dd181d3e6ab546`

```dockerfile
```

-	Layers:
	-	`sha256:67f7ff4a8a081feec215d7caa81a57499b64881cb62ab89871dca1925bd55937`  
		Last Modified: Thu, 09 Oct 2025 11:23:49 GMT  
		Size: 192.2 KB (192189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f9fa648ab0672aca7e942ef68d192b56e873696636af0babdf17163288f0d07`  
		Last Modified: Thu, 09 Oct 2025 11:23:50 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
