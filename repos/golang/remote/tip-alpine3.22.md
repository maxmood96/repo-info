## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:d78e23c6ce8a5a1b9e8a621e79afbd611b3dd42774d2fe08093f1c799cf3a950
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:78670d24683dd246ae3336fef0c51d60a7c0f8cc5becd18af59b03ec11d2cf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101636605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709d86c63238da2eb276944a26332f321d12b4729a735bb837f2ae671868e782`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:45:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:45:19 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:45:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:45:19 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:45:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:45:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235209cdc27e38f4b87fe0bc3618cf7cb15826e83e164f1805ee5c64c514d07`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 289.4 KB (289449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c99e1b92b356e29ecac9571c34c4905b5ff2fdba07c55242d418ca6ef2372fa`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:97eaf99b1d995cc089b15fd0b9fd49279fa57e5f2a4620798a00e59e62e32c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7400ca78d13e8b3feb30dcd86415095cce1dd1838e594602f55db11b85aa83a`

```dockerfile
```

-	Layers:
	-	`sha256:f813f9ed3ae16747f8f6ef1603f83fe81a38ff34d0b7aca6c0be753d1cd22cad`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 194.3 KB (194297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4065f070773485d20e8fd41f0404651eccee44905d03ecc559a1dfbaee90e80`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:d74d4b62dde8577a81dca723a5f74fa9c3191fb0d762a68bfdb46079052cc8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97459995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358ecf9ba599c81dd9cf33427edffe45f4f1e5121d8febc1cb94d0777cf2a575`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:01:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:05:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:05:00 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:05:00 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:05:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:05:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f710dc877954a31c00d16b788afdc1619e4230ca64f90cb2ec05795e52c9a7`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 290.3 KB (290329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da960de4dc7ce914df12e6e4e0869a4439909a8959fdba48a5cd0d07b76f40`  
		Last Modified: Tue, 05 May 2026 23:04:58 GMT  
		Size: 93.7 MB (93662126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1648e65472d4df9b2bd978c08c8f58448cb9f240f39a1220bdee46b412ee6216`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6ef7b49119f542d5d84d5150b9920205b4d673adf7ae5235a673f628a6bd3424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3286e64b13dd891152bb53fa62d093e23690c2214adcaabc6ba3c8405dc75cac`

```dockerfile
```

-	Layers:
	-	`sha256:96411c1387e6ca6949d410a02b289e4f041d1f5b5632afe093b99a1715b5ab4b`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:48d249a81ed6f20f29e1bf69fd1041913e988e14e16612c799aacc6655af5ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96894527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853366586dc9633a4c046de2ea46d3324168471f90e608592d318b52932a3070`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:06:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:09:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:09:20 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:09:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:20 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:09:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:09:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b27107484f6c337e9ce6888f3d2cd0bd1b20c6cba90a3001d07dbb2414e48b`  
		Last Modified: Tue, 05 May 2026 23:09:38 GMT  
		Size: 289.5 KB (289510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bbdc86693f16a92884867fe88e3f0552393622d7fbb939ee6f6410622ecd43`  
		Last Modified: Tue, 05 May 2026 23:09:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:48c81831b14be86d32df76292c692fead4a4a4d9e78eee47e73c7d6e147ec913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3150851f24846744980ffa191d0fbd04f1888b2e1c0b65525ec34739112751`

```dockerfile
```

-	Layers:
	-	`sha256:4c6b54ae40b213917efb87579799a948febcf416be5cb478c2017c15457e8825`  
		Last Modified: Tue, 05 May 2026 23:09:39 GMT  
		Size: 194.3 KB (194301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450bc47cc2e54516eae09de4964bcad7188f77d2f924a1cf4f92e05f16438a28`  
		Last Modified: Tue, 05 May 2026 23:09:38 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:abfc92e2cd76f3a9ffdd8efa67b5aed4f8c90eb3c7308d64ea9d82c099f33d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96676314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed544b2060fa3cbe9fce3072b20726a2637972deb303a2c0d64e37d62ef62ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:02:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:04:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:33 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:33 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ea45246c6bffc0e6f37bcba8e06f132cd56b4b8fb0a58acdeb738e38ef847`  
		Last Modified: Tue, 05 May 2026 23:04:52 GMT  
		Size: 291.9 KB (291899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9c2c8ebc4692849ef898918dccad1847ea4d5878cbe8582f3ce65dda08d77b`  
		Last Modified: Tue, 05 May 2026 23:04:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f96633632c81ef686aca29e09d493b442b62060c7797de88f32da0ed663be4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1961c4134f35c2e34011004620d7607c8410c408fda483719bd42732803b5a58`

```dockerfile
```

-	Layers:
	-	`sha256:5138c45dc5161e9b22cf5732ea3d96023ae371bb6a2f67e388e9d03891ddb43a`  
		Last Modified: Tue, 05 May 2026 23:04:52 GMT  
		Size: 194.3 KB (194329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a021445dd395ab8197d165221527a531f525c0c43bce466921d8014eb4387ee5`  
		Last Modified: Tue, 05 May 2026 23:04:52 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:bbea760f04e05202002c6b1cd944ace8dcf7fd142f00616ad91e7e25246ade19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99194639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cdd9318277ef671ab5aa35274a8b3a0b2852bcb8552ba0093277fce1edc75a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:41:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:44:24 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:44:24 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:44:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:44:24 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:44:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:44:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e261e5065c975cb92426a8cf830ad063837106e0a1fbfc1dbdadad65c2ac55c3`  
		Last Modified: Thu, 07 May 2026 17:44:41 GMT  
		Size: 289.9 KB (289932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cb41c15328706dba900a9f656becdec2f7f68ebfe3e0af0a0d83537c2f3e4`  
		Last Modified: Thu, 07 May 2026 17:44:32 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4236621af88866a19f5b84d918b2abe1c88b4b6af63a96d4190ef2da6989ec6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2b8d76e93da12b57ec23828c58a23deca3277de53c5c032146984132e55ed2`

```dockerfile
```

-	Layers:
	-	`sha256:7b640eaf40321ab771e20c98742ec8e4d86dab67451ddf092f3c1068e7c8ab03`  
		Last Modified: Thu, 07 May 2026 17:44:41 GMT  
		Size: 194.3 KB (194266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0d196309930cf05e81845d24bb144f53d6aacc78347dec13920d77ebeac967`  
		Last Modified: Thu, 07 May 2026 17:44:41 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:1661517020bb5e02c62b2eb408cea52338460065cf55f9fa3a9f6b7ba59e90cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98157931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202b6cdaf4ec5abb44217536a90e7aecf1448e4d81f8ff04eefbfa87cd9c1a18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:17:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:46:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:46:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573996c1704299f203b95192cb9a61f40867e3dd7bfdbb9d3428c371304bd492`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 292.4 KB (292441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990706889925169367565c114544ddf3300e65851445e5dfeb25beb7f00fae5`  
		Last Modified: Tue, 05 May 2026 23:46:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2bf1d5965843588b489d00c5e3f5f7939acfe8f3a093c0182a28df8e4e41d9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3874a16b84e7bf98fb21b1bd4e9883117306b090ae7c0862cfd673d9b18cea85`

```dockerfile
```

-	Layers:
	-	`sha256:e43d14f8bff9b6fb577f721d8092a6e155d0b213e174f9f837f657ae366e8324`  
		Last Modified: Tue, 05 May 2026 23:46:33 GMT  
		Size: 192.4 KB (192384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a306ee324d15f177667cc70890384f0c991d8dd4ddfc579429f8d21bd7f6bc9f`  
		Last Modified: Tue, 05 May 2026 23:46:33 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:5efda6998ad329edcd874b406680f575f0fd4f7aaccb582c617d2b331c336e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98432277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a9448b3975e839d738c4751489fdfbdf73bcefe1f9242d2ec8026296ff8705`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 01:45:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 May 2026 06:45:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 06:45:06 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 06:45:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 06:45:06 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 08:04:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 08:04:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e48325e06ab8f03302d19014bd8681498f11993eba6b2fa96b633d7c283c8e`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 289.8 KB (289807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d77dd072bbe9d4ad01204d701c796e83867bd2e370f7f50879f12652b55ef`  
		Last Modified: Wed, 06 May 2026 06:52:06 GMT  
		Size: 94.6 MB (94621433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f660e5cf8cccfa8a481c39591e955bd3d5087ed13191c9ac95d317116f6e5bfa`  
		Last Modified: Wed, 06 May 2026 08:05:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e38c7eb7bde92eb5205605a7547caf7b90c315b6cf066b4a560516e582f52e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d089c3200088c296d204c2cfccb4fe63314221b6177ad2ae0c8da08644fbbdaf`

```dockerfile
```

-	Layers:
	-	`sha256:3d4f2c456ad17fef2ea127268edb7e8b660d5bd0cb6249413800885b685f4d26`  
		Last Modified: Wed, 06 May 2026 08:05:24 GMT  
		Size: 192.4 KB (192380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40855c8eedd7a604c6b8c40bdc2cfb377a09720167bbcd52b103104d883932b9`  
		Last Modified: Wed, 06 May 2026 08:05:23 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:9d57cc0154c93306caf129e7c8f7bce827784bf97a002a2be7c8b48b0ba14861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100050089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf5e2e32e0f3cff827e720e181aec4b101b5c957c0282cfc7c3d436d6b303a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 00:01:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:58:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:46 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:46 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 00:05:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 00:05:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0b12310626fa8235af46cbc071f95db3829e79b0bc5117a7395ef8ff53bb2`  
		Last Modified: Wed, 06 May 2026 00:05:31 GMT  
		Size: 290.5 KB (290468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524c45e52405959a1eabf3f6d0d048d31a00681f648b2e3ea132d2f0d646cc88`  
		Last Modified: Wed, 06 May 2026 00:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5652fa28dfb42494fb4564d5e58f1542f856d0c62be13f46d1d54c86356f8977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee700a235dcfc20de41e750552a09e6f84c9c541916cfe3d047b8cf7db3e366`

```dockerfile
```

-	Layers:
	-	`sha256:e142644ed4ba6827c46948115dc432bac89916a47caaee00a35fb64584145494`  
		Last Modified: Wed, 06 May 2026 00:05:31 GMT  
		Size: 193.1 KB (193094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199b55af3a29dbdcb7a3749198de0116b27778491cc726b9bb38c60a7363dca7`  
		Last Modified: Wed, 06 May 2026 00:05:31 GMT  
		Size: 24.5 KB (24464 bytes)  
		MIME: application/vnd.in-toto+json
