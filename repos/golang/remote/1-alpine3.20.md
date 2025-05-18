## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:9f98e9893fbc798c710f3432baa1e0ac6127799127c3101d2c263c3a954f0abe
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

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:e9879caea745a1826ca257e89e9c047d6c2e6ea785edb2974e7a69e6c0235e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82903023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25afe315cb50b630260f517a6c4b84f5478ce857f425e52e6ef187cdd6f16e48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a1c36948bf6f54191eeec841b0fd71195c6f3ffd97ee4eb2af2e77046a1539`  
		Last Modified: Thu, 08 May 2025 17:05:14 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7f35356a247cc18152ab0dd81696f75d037f7d53ccf7f14d23b8b7213e199f`  
		Last Modified: Thu, 08 May 2025 17:05:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:138e77201c639fd93330303f22845e7e5c48b6e2ef6bdb1035845e62dff3751f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 KB (229381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c08b15368113e19213c4f616822b57d7209de348d6a703b535132a578dbd8f0`

```dockerfile
```

-	Layers:
	-	`sha256:a97160c70282accbe647d8d23895fdbb3366655b85691d8d6efdb39778bfe6ee`  
		Last Modified: Tue, 06 May 2025 19:25:20 GMT  
		Size: 204.5 KB (204531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e13d3f7c1cc0697ea99d3cfe507d5f3b159ff51fc0e8a1ec6d30c0d5eec8e95`  
		Last Modified: Tue, 06 May 2025 19:25:20 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:ab594bd93054c312b63938c4b65f83c930dc93dedd2a0a67f6ecab29f9f6f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80813026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecbac2d21fc3335cb8986388a82770dbf96e1e985ecc6018b6bb886caeb5e88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Sat, 15 Feb 2025 00:23:02 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897536fb13ccfca87cac1110a2b716225d73570f890064e1f163d9b5875cd3a`  
		Last Modified: Thu, 08 May 2025 18:18:07 GMT  
		Size: 77.1 MB (77144504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fea7092f52a888d967904f6fa489ec3ef38650982185dba25f239783ce10f08`  
		Last Modified: Thu, 08 May 2025 17:10:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:0c200bf192e7e528031ae5034b04bf563e38be08ae75d3ebeabf99a938268621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603f7262e4dd426940f99404dc9a82891053514c1b280f60a1e8049754dfefaa`

```dockerfile
```

-	Layers:
	-	`sha256:42c4dd4d69aa41a299dff73911919b8797e0e91646895464d8e03af0c971a20d`  
		Last Modified: Sun, 18 May 2025 08:02:06 GMT  
		Size: 24.7 KB (24737 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:78cfd9790f151b80938580454b33713878f97a714539e7b4da928227be83c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80535321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74d24bdd3f3639b55d0c1410ac759c0a6fce8b16543708e54db28f241e95dcd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Sat, 15 Feb 2025 00:31:29 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7db61b2ede8094d4feb2dec397bc88747a3b3d4edee2812f4e17aa1e80697fe`  
		Last Modified: Fri, 09 May 2025 01:30:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8e22dd3177d6e5fcceb3fdb039e94655f73f8245ac56741ad476da2021286d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 KB (229483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ce0818dc9445356ff1bb6f2af4e05b3a3ce361b95bfed243be65b5c41ef3e6`

```dockerfile
```

-	Layers:
	-	`sha256:8639c230fcf5d97da2d5028fba07a9ec34042d12553ca654322d354f3b036b7c`  
		Last Modified: Sun, 18 May 2025 08:02:08 GMT  
		Size: 204.5 KB (204531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7f8343a6a5d4169cb29669eaac92e4f58d0b599b503af3972a386341c7574c`  
		Last Modified: Sun, 18 May 2025 08:02:08 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c5c0465ad81d839638b53fe5c85382f44eb60d119646dc97b8293daa2c6495de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79619356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd45f4763b05bfdeb6b4e22611489ad8ade0c8df0b3113203de9d1561915afd9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c56e8762dfc22e5eea28a95b136d7a0b7a8984a3a37a98c0dbc768604f0c31`  
		Last Modified: Thu, 08 May 2025 17:15:51 GMT  
		Size: 297.5 KB (297479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6688b7e11d532d8a19128e44d9ccfd2bc873010fc1c895f9055eee8d5aea35a`  
		Last Modified: Thu, 08 May 2025 17:31:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ba79b84d4477261d640dbdd23aa86b464e09f238d01626918a3bc1f8ca144772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 KB (229571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a393eed99b54fabe154651a657894409038f0ea3558024630ad69ff704b68`

```dockerfile
```

-	Layers:
	-	`sha256:40702216aa87f0f115aa69c3b403f94b992e53435fb9038bd447720f0ebfc226`  
		Last Modified: Sun, 18 May 2025 08:02:08 GMT  
		Size: 204.6 KB (204587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81da4dc5a05de5f53e6e35df3049446dedbff1dcf13ce6814d0829dffef04e8`  
		Last Modified: Sun, 18 May 2025 08:02:08 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:236292e74649ac0e23ddfdaa4b32399401784a63f4b3ede220170cecde0346ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80666846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c1cdafa52122af9db81b474e15a822e8767fd48d1cfeb7a893e0cfae89f108`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2977f3b0d62092d95d32c932833969ab6ee3cf1bdbd0425bd03f030d0b036c`  
		Last Modified: Fri, 09 May 2025 15:54:21 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db714197af43811f01d03462392675e848884e82b9483811c21c83a08d3e7834`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 76.9 MB (76899879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454edcabdde1aae999d6305bb67d9fec7c5acb17f8c85ebd83d8fdca651c2827`  
		Last Modified: Thu, 08 May 2025 18:17:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3ea22a856250f3e019dd2c5ac1325dc8ff0f430e6d4287cd9538f962b7511053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 KB (229284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4188986d2d1575aac7687444cd99581f667397ba12a059a2c063aee6bb3b84`

```dockerfile
```

-	Layers:
	-	`sha256:09f18fcb8b3dc5dac1b8cad72f5418f2a190fe6c83185273e33c4a23d4742d07`  
		Last Modified: Sun, 18 May 2025 08:02:09 GMT  
		Size: 204.5 KB (204470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8fe4438a65482b5497cbd015460b59000b3d4d970206d2541320b87fcdc91`  
		Last Modified: Sun, 18 May 2025 08:02:09 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:11ff3dc3fa2b77a68920680574f8a0810347995f7974110bc2936afac4dc5ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79418231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecbb38e95694d27ace0717e82e8dd0417883dfedeaed784b02bb5fab188889c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ae44cb6a22e21c989dc7b540cce14809e91f5f477dfebbdc44d927ba36845`  
		Last Modified: Thu, 08 May 2025 23:17:55 GMT  
		Size: 297.9 KB (297900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f44821f8171df650a338e8fdd3b017af075382eee8cc2d34256864c2264897`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 75.5 MB (75544493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58029d41af0374b621997af24cdf6e04acdae86abd4578185143d62807f12cc6`  
		Last Modified: Thu, 08 May 2025 23:17:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3f9fd991c7ff51206d7afd08ef0bf0b4c83b08b9caeb0f13671ebf5a42d4c3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 KB (227547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777fbb02eb540169f04868a4edc86043d8028164218e475c0220f158286915c8`

```dockerfile
```

-	Layers:
	-	`sha256:8e23c9d1c28094b481d25403819d9c9b2205e4b4af8a8d9ef96b8a5bb4d2ca67`  
		Last Modified: Sun, 18 May 2025 08:02:10 GMT  
		Size: 202.7 KB (202650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5679c4dff2581dc0d6c3e441c6a753b6b4f610f7e21fdd83a48a82a290d7a7b`  
		Last Modified: Sun, 18 May 2025 08:02:10 GMT  
		Size: 24.9 KB (24897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:40e9c6161ad9536daed403d1202c26a612b08380fd20f5481c612d18f502be48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79982711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad09ae6f1d393b4b5e8b763c3aef5424d119b1c9049a4bbde4d01e5f284a5bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 09:31:09 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4ce4a757d65543eb38e825fd00a5434bd6efef264c5b31052eab1a8e5fa09b`  
		Last Modified: Thu, 08 May 2025 17:12:53 GMT  
		Size: 76.3 MB (76313875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b542ec840dcbbd4cb5f00529a3a9a6840c1d2a1e109dd51f8fd275e3a2c45`  
		Last Modified: Sun, 18 May 2025 08:02:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7cd5d61eea0f4c5447f3d05f582b2c9fc0b6a307caf6db386c1e75c3ace9c6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 KB (227544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123ce22ad5357501845fc49bdaf9ceb7d0f39b1ee4dec64e95d354bc6ae61ff`

```dockerfile
```

-	Layers:
	-	`sha256:1d16a0af77b51dc36156eb07b02e03510e9d94ae5800e011d5269adb10bcdb7c`  
		Last Modified: Sun, 18 May 2025 08:02:10 GMT  
		Size: 202.6 KB (202646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726a8b821d0fa2aeb6009021de2ea2f53089cedc42645f84ea68eaacc87c47e2`  
		Last Modified: Sun, 18 May 2025 08:02:10 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:26bec5aba10dd992a978c2b3ca0417be9a71be3e7e82d124543cfd88a9c4f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81547890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e0ce9c58daf8ca40c967d7c41786e8832583f173664e67ae34fe0e9a82f7eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79aca9d4815f0afa30913ff64ea6ac6b14fb546971bdd999f2f73d3dc79f0ba`  
		Last Modified: Fri, 16 May 2025 18:21:47 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e83890111f2cfa590a0023450ca3f44d60d123d688835ec1c4ba557b336f8`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 77.8 MB (77787898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d42bf7b8a4afc32df5b53a0f4cca52a8b265a3bba994bdbddcdca5e45282c03`  
		Last Modified: Sun, 18 May 2025 08:02:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e09a27d7ba50f911f2ddf0e6bdee209ecf0dc2548bf4b24382e79af17baa3060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 KB (227430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d09cde532e74ff77d96de984b2083cdb486be0fbec8d9b19a0c26e15ec92ea3`

```dockerfile
```

-	Layers:
	-	`sha256:01675e4ec2b9ebddb6080b50a0860bc5e426e1647e6041e3858342a1465889fc`  
		Last Modified: Sun, 18 May 2025 08:02:11 GMT  
		Size: 202.6 KB (202580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e574e65c7709afd97cd550b33a0dee004a38421be21d648c87268fb2e5dc0a5`  
		Last Modified: Sun, 18 May 2025 08:02:11 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
