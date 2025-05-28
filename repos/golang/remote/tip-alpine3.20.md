## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:f75c4058e81489896d2d0dd6f5d4f88d5b39f0c5cd68e5d8c95d320faf812352
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:2ff9c04f6dce9a3b04a1da6aa01bca9f8138ad06ba8cddc7c26d5838d4df679e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130162381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02e4de2a93f007b7cbaca9e7ce6c65a6cfba780380a70d7fe6b04862c66b16d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789c8ecd19fee07ed0173318c2666ab7a23c5828ae5c17e9d96758a52878b93f`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 294.4 KB (294408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37739a11166de3eef493c06e2f945d1e527fcbc7b45049a9bf54b5049c44176`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 126.2 MB (126240918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ff7627b4b8f6ac89a32db4cee0d406b9e9c9ad46648e8907f5a677767f55c9`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:181bfbffbbfaefdc1bafa462212bed94bb71ff2dbedda3b4394b7eaec28ffa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 KB (231403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c53f7198d148c32de5e2f6c47b17932b5537fff1d224263cf7df4ada52db1a2`

```dockerfile
```

-	Layers:
	-	`sha256:44919d3b06e8b89a7296a6a77f2ca535e9918c583c16c22bc5d44a60216b6294`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 206.9 KB (206891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ce0f90f13e4f0cf9105735e7b61a28f438cd3b9f98bceb6cc0788db641b706`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:39f9276ec441a872d4c43bde65b54f22ed5c94857211f0726daf57d71074ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125116992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36474066311c0df91b66fca4c61552aab7483290e9d598f210da8d68e066be67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd0559c7de6f506244fa457bd5bb8e69593e5e2f5b69b52b74b698afed88582`  
		Last Modified: Tue, 27 May 2025 19:05:14 GMT  
		Size: 121.4 MB (121448470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe55757103f01436056637e31a3690d52b9f5718b856fdfa2c1e413929d63b`  
		Last Modified: Tue, 27 May 2025 19:08:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:362f861e382dd449719ac1e03e3a268c431a8c0c21143689257640a7021dd9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddaae0bbac0d5da2325d972b76c0290182804d3500134f3360a03dce96d9ead`

```dockerfile
```

-	Layers:
	-	`sha256:98899bbbd11cbe6d12e14ea6aa8322d8663dbb25585f7a1627e01fa08ec11ad8`  
		Last Modified: Tue, 27 May 2025 19:08:56 GMT  
		Size: 24.4 KB (24403 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:3662c50928f226913aba0db2a02d6635a71ee78192032eb64224d13d22e3d873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124499798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ca2329f2a0a1a45158cf03bffaa4523da529e5fa53804da770393c0a4721c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0fe5e7d3d09e12944b416a2054aa6712ade9bdcb8b3878cad2dddeefd549a`  
		Last Modified: Tue, 27 May 2025 19:07:16 GMT  
		Size: 121.1 MB (121108917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e74dfb94bfbfd503d85d9377943a70c7739a9d59c19304144a73e41f305566`  
		Last Modified: Tue, 27 May 2025 19:19:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:959b44a84cb382f9d3797780f0f2fe8fd3b88d49ea62a7cdd6bf7f2c31956081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 KB (231491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37853a184f7c719be2f47c772182dd57e6c306f76d1080735747bdc1aecf8da1`

```dockerfile
```

-	Layers:
	-	`sha256:9ebd0fd79fcb2e8302e8b730af64e2aca7349368fed4150cdd9901bf66cafcea`  
		Last Modified: Tue, 27 May 2025 19:19:48 GMT  
		Size: 206.9 KB (206871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec385bae9adea1c78bfa5f7c6b2f9ef9c43b945323fe63e42b600804b3d718b`  
		Last Modified: Tue, 27 May 2025 19:19:48 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:23dce6b2b99cf613c1d9e6798d42b670e91262f47dbbfe33d8e3a37ed4af58af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123443076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efc0640cdd15788d0b3a9029d7c24163dece7d6023c6f4356d5a39652d02cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c56e8762dfc22e5eea28a95b136d7a0b7a8984a3a37a98c0dbc768604f0c31`  
		Last Modified: Mon, 05 May 2025 21:15:36 GMT  
		Size: 297.5 KB (297479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33ecb4b895f73f5e4d5736d5a0a4109e5ac27823a9c5ca57f0642e5a3d9a8b`  
		Last Modified: Tue, 27 May 2025 19:23:28 GMT  
		Size: 119.1 MB (119054274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bc662d6a09ac4e3acfb329c478c7ed0945cef7b811675bb0b5a4e72ba0f59b`  
		Last Modified: Tue, 27 May 2025 19:29:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:66119225912b77ad92932eaf37e6e9e3ac2849c95c212ec5bd9df546bf573bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 KB (231571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e7fb20e72d5697e84248eef8f45e5ae08747500d37c5813ae2855e1c074faa`

```dockerfile
```

-	Layers:
	-	`sha256:7c173ea020532e1457e4e153c4fc537303df4c769a6e72496b62c75dd2a56a7b`  
		Last Modified: Tue, 27 May 2025 19:29:58 GMT  
		Size: 206.9 KB (206923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9323e1e0d4024e098fd2f56baa25b504f0a77cdeafc34fc1ea92df857ae796c8`  
		Last Modified: Tue, 27 May 2025 19:29:58 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:a9125f6953cd3b4d85755d1209b5679fe9eb083b05eff4150510b4366ecdc9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127974146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37529b2b4ce28905b9421781753d925be3e79491334a4f9c4b59a71bd572a759`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fe50d0fc6d915d3d689e8fe0080ecc6cadf6d8c7b1f68f2e8aa36a03ce0a0e`  
		Last Modified: Tue, 27 May 2025 19:05:44 GMT  
		Size: 295.1 KB (295142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb63d3af1099d61647a313155e9eaa0aeecda078cbf5fcab7fb7996b234e196d`  
		Last Modified: Tue, 27 May 2025 19:05:30 GMT  
		Size: 124.2 MB (124207178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c271e35b93819fc92210cfd4b3a78dc1f517c851587b45653ab2ae7d27bdb9`  
		Last Modified: Tue, 27 May 2025 19:05:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:54f95b897f1d1ceafd63c0dc2821294b4723e56d28bb5cf82f4b19ed922c5499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 KB (231315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2271c2f272d2ea51ee29d2a65d050cc0a94ca29cb15c6c9235e299219b2a22ba`

```dockerfile
```

-	Layers:
	-	`sha256:37df990e1f3b72d65d946daf2b24ade4bfb962094057e541109c30a8f2c901df`  
		Last Modified: Tue, 27 May 2025 19:05:44 GMT  
		Size: 206.8 KB (206836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411f7b81ff52f7a4543e79f953c25d50b52b2032b1f46807e19d0da556848222`  
		Last Modified: Tue, 27 May 2025 19:05:44 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:5db72cb1f85e837cef52b8e8580283fcb3ae577d08d246e75418f9fdb602ad8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125039157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3322ea535741c4354b4c22bbc82e19911fca1b3265faa151afe15d8be78902`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ae44cb6a22e21c989dc7b540cce14809e91f5f477dfebbdc44d927ba36845`  
		Last Modified: Mon, 05 May 2025 19:04:06 GMT  
		Size: 297.9 KB (297900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275b8143ff44473029dc987922dbd1dd91e814dab86dd3c175ed73d2ef81d1c`  
		Last Modified: Tue, 27 May 2025 19:06:55 GMT  
		Size: 121.2 MB (121165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567008ea377c4fb98485df02697fb07629fd8d419c981aced4a52f023e5cb880`  
		Last Modified: Tue, 27 May 2025 19:13:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:48507a7f89e5cc877192848dcd834e58b3c4246a8c9b87b73e7c2c57a8aedd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 KB (229560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132a0c413ad77e6112613ec8bdd6e3ae858cefdf984ad0ba9d666e9beadb90f9`

```dockerfile
```

-	Layers:
	-	`sha256:b039a46e02ab7c7ad91368cddd5eb4359ccba81fcad3ef06c773bec302d04a32`  
		Last Modified: Tue, 27 May 2025 19:13:04 GMT  
		Size: 205.0 KB (205002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1494120b8e93716fd9ab0c096f5cf442ec2cf4fa88b2b844526bf86b127c5cc`  
		Last Modified: Tue, 27 May 2025 19:13:04 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:de8092a9cb9a4a2c9716f1c91e430b3a69ee3f77326ff1777f930e85d5b90ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125062619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93323cd531a49b5fc6eb212c33fbbeb077dfde224fae5aa4440e55e036e276dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf501e8ac8e034ccf3f3064d2d56237fc55dc6b377839b153c3f162a1fadf302`  
		Last Modified: Tue, 27 May 2025 20:07:53 GMT  
		Size: 121.4 MB (121393782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e35d67cc1493b6fa69a5173b219e62fd1a142ea989e9cf22072b65d12028c`  
		Last Modified: Tue, 27 May 2025 20:44:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:12a17cd2c1c7fda386607d243b6b36e44d6f6eec32a6dafb04f4898e821707bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 KB (228761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6716106bb447a0a34e619280612027efee0c268a0823106cd37141c17cffe5ee`

```dockerfile
```

-	Layers:
	-	`sha256:b79211bace48e4ff1f3cff046f1fb62a81720d1c6e00479f7e2bf78d3444745b`  
		Last Modified: Tue, 27 May 2025 20:44:14 GMT  
		Size: 205.0 KB (204998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f811207a1b2787499e88a2d7eb5293be6446646f725ad448f8af94589fdafe9`  
		Last Modified: Tue, 27 May 2025 20:44:13 GMT  
		Size: 23.8 KB (23763 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:b5adb9d1591709e17e341c0cb8b52c72ce20aadda52d41726c002d040d73b24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a88eab847523c5703531fd04b0f4b90ed8a112ff2c58331da9ffe076f0c20a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79aca9d4815f0afa30913ff64ea6ac6b14fb546971bdd999f2f73d3dc79f0ba`  
		Last Modified: Mon, 05 May 2025 17:58:58 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a53d6c9d36291056f30ae15703f561e0a8333bad5f15ea579763f74d2b6616b`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 123.5 MB (123462542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd0580cc0938c258f1b2956c3920d6507eefc9d818fd0d45a9f854a5e31df9b`  
		Last Modified: Tue, 27 May 2025 19:11:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:63f79f406c6eae30d796239b1a475d61bc352ad28e77e82f0c3a72d6050b92ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 KB (229452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edfc7a3af55123bd5fa7ba9730b4b46f252b65fb2fdae4081958c32bf10d13e`

```dockerfile
```

-	Layers:
	-	`sha256:161483038ba858565928a26ca6799c0ffb367543b4f86ec23ddab58bf20bf4c9`  
		Last Modified: Tue, 27 May 2025 19:11:28 GMT  
		Size: 204.9 KB (204940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de579cff07e7d65ac383cd05b813ad34dbaf5ebaf9d6ea570b7f0724f63e6c4d`  
		Last Modified: Tue, 27 May 2025 19:11:28 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
