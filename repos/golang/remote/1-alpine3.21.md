## `golang:1-alpine3.21`

```console
$ docker pull golang@sha256:5ea2a92bd01024ea2e0a6daa8c57639835bddbec87c0e6b30332008d37424596
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

### `golang:1-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:49c785b0dbb5ef5df65d52fed1ff6f272099a30618812ba33d076acdfabaeb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64078076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d40af0f83d4caa50f5150bfcc4c579abaf3499d016c81098958c750f355e607`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617057392911e052ad1ebe431dbf9707e0fcaccaa7b7c93ef3917ddd224b6c4e`  
		Last Modified: Tue, 07 Oct 2025 20:49:06 GMT  
		Size: 291.2 KB (291171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2aec7ef170b5f02e240ef6c8aac64fb96a14688ea0750c962c145c141f3830`  
		Last Modified: Tue, 07 Oct 2025 20:47:28 GMT  
		Size: 60.1 MB (60149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efcd63d87324e13c89d32f86a907b81c5dcaff02bca3d40e05334eb75011a7`  
		Last Modified: Tue, 07 Oct 2025 20:49:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a76067f2239749637d38ea975bbb5bca971331a80fa46171b31a4b038780a494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 KB (219498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56de9942638c1d8df95132886cc51701b39c729c7be32dccb55f4fa0ecbf239`

```dockerfile
```

-	Layers:
	-	`sha256:2816b5344a1448028b547d5535c14dc5dfe7579f866aec14073962bf42b0af44`  
		Last Modified: Tue, 07 Oct 2025 21:18:10 GMT  
		Size: 194.6 KB (194648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1773bf67b8358ee7ef34ef35dd412613d44d88a96718f5acfd1c9945996b85cf`  
		Last Modified: Tue, 07 Oct 2025 21:18:11 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:8379f24185fe82a12b0a23130ae3c78e7cbc4249d6a5387459cda59dbbc82c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62731882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a63bb2e8637c929e9888ba85a520181fb514bd3e73c63ba5da02416bcd33388`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c990b8d0645da44b2573863fbc2b2d5d456f8e12a29f68cddc22822113cc5d7e`  
		Last Modified: Wed, 08 Oct 2025 22:38:19 GMT  
		Size: 292.2 KB (292230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729a3e231583976ae1f9cca817bd27dd00673c51d31bb2652e5b51a3d2ea3d`  
		Last Modified: Tue, 07 Oct 2025 19:34:35 GMT  
		Size: 59.1 MB (59074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355d495650491e9ca03fa1a70f509bfc0c7a968846efff01c154b6a5f1fbffdf`  
		Last Modified: Wed, 08 Oct 2025 22:38:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:5b3e1598509e140b0297894c141a965c5e3ef3786010feccfa8995199f4835ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7958e231f1ec12b35cf144eed0029a98a99b8fb225069e84ce8ac5baf94a2e20`

```dockerfile
```

-	Layers:
	-	`sha256:79be56ab6e846c41d96666b4b67681a2b31e1eaeb55dae60f7a952a62530fe4c`  
		Last Modified: Wed, 08 Oct 2025 23:22:46 GMT  
		Size: 24.7 KB (24741 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:e3dd7f662c04009b9d3b656505e074929f99835f1d9bf4f62411112dd6da0b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62464003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4d8ba037de4567d12cebd15e43e8b70ed25c4c59d6d3db5be5a93f611ac55b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cf808b5988ae45b458634d15385b8123e0c72ff0a8082d6be2a3ba7260c0d9`  
		Last Modified: Wed, 08 Oct 2025 22:13:18 GMT  
		Size: 291.2 KB (291152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f4a6af62e4857e5ec3a224e59b1969df2cbb9b46b38acfb18dea0ddf371f7`  
		Last Modified: Wed, 08 Oct 2025 22:13:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b311421e9649e63917fd2abb71490cd0d29cdb948034a119161670d0926283b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bce4c4af975dc07a6fd7d1c737c0a578b5bf8874094a4c0ab8585dbcb7167e5`

```dockerfile
```

-	Layers:
	-	`sha256:b10054f65a113431d26ecaf6284bdd7024234febc46d8a5dc5435fa58019d5c9`  
		Last Modified: Wed, 08 Oct 2025 23:22:49 GMT  
		Size: 193.6 KB (193587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df411063b21878d590d4ee42101db8aaee32f3d7da06c25a0da1215a3a96003d`  
		Last Modified: Wed, 08 Oct 2025 23:22:50 GMT  
		Size: 25.0 KB (24956 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:68cedc783a4005de557271e7aa349e2040b1f31d8c86e9d35c671244aaf91f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61934377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1d42043aea21f51cb12e94f531c9f006b2cdfb2571f483b3b4f02c45fba80a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f186327ac80f2ae875251e6baaab31c886ac833f6f80a79ca50eea116cc06289`  
		Last Modified: Wed, 08 Oct 2025 21:49:28 GMT  
		Size: 294.0 KB (294047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3a03536410776fc083e4699681f0a76d2629a5d2dd9afef1ce8c124bd2989d`  
		Last Modified: Wed, 08 Oct 2025 21:49:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d9846b50ac204d6747c2e9f682270f0cfae76ed949dc9b9723033e0663e310f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be13c29aac2ea6b2add5faa505c6a7e14e5a4edb04b3cd4d01913e00cd7e6e8`

```dockerfile
```

-	Layers:
	-	`sha256:26cf0d38f1ad2ff203825d72b1262c7f50d30a07b5948651e88578864d1f3fa3`  
		Last Modified: Wed, 08 Oct 2025 23:22:54 GMT  
		Size: 193.6 KB (193621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179c5b608cd711802bea36985b23e73b0c6759c2f0070789396054869c400d0d`  
		Last Modified: Wed, 08 Oct 2025 23:22:55 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:500d7890966f420584f97b7e1708a4de94514bd94ee4b118100d86b1425624b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62626313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1409dad70102b3f4320352575092779aeef2b7233cbf0f3a059883c3653752f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736224cb474507a2c478d79f54a0b778519e5b15e2af332f387f01d39dd1231`  
		Last Modified: Wed, 08 Oct 2025 21:41:17 GMT  
		Size: 291.6 KB (291589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1303a4fd3683897bef6c94e29bf9e3651f1c90c65f26cacc89697c837708724c`  
		Last Modified: Tue, 07 Oct 2025 19:34:26 GMT  
		Size: 58.9 MB (58869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a8334d8958f772a3fc7d274ae61539246bedb07eb0f40785e5ef293fe2a38`  
		Last Modified: Wed, 08 Oct 2025 21:41:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d01c1f880e27cad5fca364a8e29b4c4fa6153668623ace6400e08799afc86b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274627cb03c0f6464dbce8ae796b741c222c3048c97332088b57be5184223627`

```dockerfile
```

-	Layers:
	-	`sha256:4d44b0f42ecc86ab541ee79477e802065fdd4e4724e9e3b3b8c95b69a4fa69ac`  
		Last Modified: Wed, 08 Oct 2025 23:22:58 GMT  
		Size: 193.5 KB (193526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58881b89dca38e339ebdc8189fd8196c1bb32cf52ef3ae6dee3b44efcfffcfbc`  
		Last Modified: Wed, 08 Oct 2025 23:22:59 GMT  
		Size: 24.8 KB (24813 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:4dabcf670faaaa4b705d9465eddeb9cbdfa976d53278ceb710bbed622c373c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61997657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e46d5f8deded1cd17a52dddceb576f49bb90abde9a679d4d677fec52edaa5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c72ed30b4440614b477e3a87c9a33476b9d0b437a968436db8903fed6fcee5`  
		Last Modified: Mon, 06 Oct 2025 21:18:20 GMT  
		Size: 294.6 KB (294580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9de43ff0121077fb728d1a905dc3dccce368d7bc632d0dec0fb5b840ff88e7`  
		Last Modified: Tue, 07 Oct 2025 19:40:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:913dcc7d442e5365dcfd1ce9e46d1cb0af7f1807dddf1e054d46160a21d6c52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f49bede53d0ff6e55f45e85451f3c7efc65aea636a075b01a4a063f6738719`

```dockerfile
```

-	Layers:
	-	`sha256:2b2995d962b017d595cce753b0c920645e112cec6ee9c8505595d00b47bdd5c5`  
		Last Modified: Tue, 07 Oct 2025 20:25:14 GMT  
		Size: 192.7 KB (192745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ece0e73733871897cbfd1951bc296650cf4bfe01338d37daa117e151a3a0ade`  
		Last Modified: Tue, 07 Oct 2025 20:25:15 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:6e108139dad7593f27d4dd81b4778deb1c071a271142813f927e805b3c1f59dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62310975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca2ec17ac755a2051599239d045b90f67db3f1027ec2eba727f302b9adfe10e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66587a4ead2af4b3777a88f71fff7f8fb2d28fecc6835536cfbd5f10d19b67b0`  
		Last Modified: Tue, 07 Oct 2025 14:56:06 GMT  
		Size: 291.5 KB (291518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d54fbaaf4f44943b5fd17aacabad20b0db0f29394c2b0f581a3a300b124c2`  
		Last Modified: Tue, 07 Oct 2025 19:40:12 GMT  
		Size: 58.7 MB (58670209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eee845e6f41bb06db8858796f0ca70a84ad1b7a7196168825e0d9f4324707dc`  
		Last Modified: Tue, 07 Oct 2025 19:45:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:38d33ababa290a7925c3984d5645b4dd7a09dae867f73fcdd4c4346e6d147d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07f883f69aaa2a632c04480513501afbd484c66118fd4dc5d0e516cd9d81228`

```dockerfile
```

-	Layers:
	-	`sha256:9cb1ca94a6e54534687cec4c11da77762ec6f21372eef3096ff55a69731777fe`  
		Last Modified: Tue, 07 Oct 2025 20:25:19 GMT  
		Size: 192.7 KB (192741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d5eb1e5ca19def5c87ab896b796ce91c25188fe4ca0e10800f611c14d8139fb`  
		Last Modified: Tue, 07 Oct 2025 20:25:20 GMT  
		Size: 24.9 KB (24896 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:c9b3f911b334d03c4aa3a093394b301e9edc699c32e64db8fcc7899663364715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63233215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c542ab2a6f220ea11cd27c0f05d2833384b699d57cdbea32c45f761e7c1ae7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c0d08c3945d6368d73f257f34ee298e8dee1cce97a4a8bd5b3c35a4f5ab3ee`  
		Last Modified: Mon, 06 Oct 2025 21:15:07 GMT  
		Size: 292.2 KB (292152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf285b3a214f4b3582f8a22e6938132a42b39ad4578f93f0441c33815b3f79`  
		Last Modified: Tue, 07 Oct 2025 19:41:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:fd8173ae6ae618a3afc4f7e4b6f963bb639503200ba6b80924e3b7b4fe5bb1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b962ef7e0a9366f6b5c465ddca709a2475896c0fdeec01c1f6f82d3e4db2cc`

```dockerfile
```

-	Layers:
	-	`sha256:b971162620cfb3ed917d119c7ac2bf0ce3cd4a4a1fe1ffc653eda835bd30a2fa`  
		Last Modified: Tue, 07 Oct 2025 20:25:24 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9246b9797e8c7b0fd3641c6cec6e4f84e0bbe8e687cc1137b58b00c3e12b08`  
		Last Modified: Tue, 07 Oct 2025 20:25:26 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
