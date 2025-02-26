## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:3da01bd76e6c9ae6069c82e1bb964fca47cd82549683fb5070636b9a41e1d11f
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
$ docker pull golang@sha256:b81553eae3f4bf62ab2a690890ee8b4fa2943933eb5f75a1b131f685795447c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133665290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a7280d2f009d6bfc0be7e53dbf58c5f99d5b2ec2fc993489f255463a330e21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5c6c16682b04cc8e7d7f438cd117a5503a71f10bc7ee4c3aa49f425cc11036`  
		Last Modified: Tue, 25 Feb 2025 23:30:28 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a93651a1e507b5bd3cfde19fbfc91acf223de81d90d9e07fc812851aad09e7`  
		Last Modified: Tue, 25 Feb 2025 23:30:29 GMT  
		Size: 129.7 MB (129743852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec8907f053d0d0dbf87334bb00bb5d348a16640610a3709769c1958b32f2d24`  
		Last Modified: Tue, 25 Feb 2025 23:30:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f34cddd6d3de4994b84b55e54002464c3324e2009eca0089573b5604e65c2f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d91dfd5f12f1321696072b42bb1b3bd654f5d6df06b3526399b095b2d3372e`

```dockerfile
```

-	Layers:
	-	`sha256:226b55d10de1b85e92fabd405730f46f5af2e31302b52d0a0c4ad15ab160da78`  
		Last Modified: Tue, 25 Feb 2025 23:30:28 GMT  
		Size: 205.4 KB (205355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233f1b1c66f56088dff6459fc7ff8c12dbf27bb358b537433c2cb19f83e4e8b4`  
		Last Modified: Tue, 25 Feb 2025 23:30:28 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:fa35a4674bf72706b18e423620ef12c7b430ece5f5178976d2163dc05177b82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127030407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe944057accc31321115d563e8926cfceb7d414c780bdcb3722f4f735de72015`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:8c10d33f52a0d639e250df7f8e253e1910c94bdaf30d4e34b190895d9f138d27`  
		Last Modified: Tue, 25 Feb 2025 23:31:13 GMT  
		Size: 123.4 MB (123361886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bb0048983bd461bda0cf723a7c0a40f96baed3db7902e73283db7c5c0627`  
		Last Modified: Tue, 25 Feb 2025 23:34:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:67ca15949ae55ef88f3ec2aa109b88f002c7d4648db2f670e14ec2245fa83961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d72577643f1b94f6e34fe0c1c430ef02e1304ecab82135bb2edd092ca2f1135`

```dockerfile
```

-	Layers:
	-	`sha256:10bccdc3ff9a03ca41bb6f963edf60f761746e4689a18594d64e53acb2135730`  
		Last Modified: Tue, 25 Feb 2025 23:34:28 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:8935c8756b41086c8f23abb4cbf3e3f964dec72ed57e660101a64f1b342a59d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126425854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5032cade43795c18318655be45a44a0f53c2b256c8adf5854323cde47f7fc0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:cbe77fa27af7b36c34f8f11e6bd2bd4b9ddf9e28c094fdee1cc3b2735243e847`  
		Last Modified: Wed, 26 Feb 2025 02:56:52 GMT  
		Size: 123.0 MB (123034972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f1b63b729cc7b54d4a58d2fb27ee3683efedf31da76f1a3fd12d363499004f`  
		Last Modified: Wed, 26 Feb 2025 03:03:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b12c639fda2553cd0c45b06bf8bd9f91dbff21640f3fd5344bd0bfac94620df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86b5a32562d346cb69d8241e8261d1c381e2e44364b1b6e34a4bff661860fea`

```dockerfile
```

-	Layers:
	-	`sha256:0c843aa7c513b66523b91c05585b5bba618f8878b1f681cbfcdb1d1785a4e54d`  
		Last Modified: Wed, 26 Feb 2025 03:03:15 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef7e1d23ebd17f9bfef95570982acec81cb4cb8aeff8becf69137b68363b7da`  
		Last Modified: Wed, 26 Feb 2025 03:03:14 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2693af432dc4fe94b34167c35845d253ad8fa17eaeefcee8a17962e43378f4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126953559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c205c8d45b3e3bb4ae8e30529e627e483fec990208499be5b827ccc7f9c38518`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80759e590e8e3c48fc0aec3f03a2c66f281d0b1749e8673f0abece25ac95150`  
		Last Modified: Fri, 14 Feb 2025 23:00:09 GMT  
		Size: 297.5 KB (297467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e46df0fcf6e0e573af560112ea65411de1e4c09446bfe2aa5c396181b055ef`  
		Last Modified: Tue, 25 Feb 2025 23:43:25 GMT  
		Size: 122.6 MB (122564769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825771a55f276985ef7047fc91186e16448747f101ed82d350064106bfc198d0`  
		Last Modified: Tue, 25 Feb 2025 23:49:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ad116189cd12dd1e09530580bf43b1d70e7c6cd896a131a6b59a7539c90aa491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d44a709dc9af75c951e705b914d435acfa12e2c7fb9c6c74dfdd5c4068ac12b`

```dockerfile
```

-	Layers:
	-	`sha256:2eff833ccb511df7b053b4724ed989b68f1d3ec2f8d2e9235a3ad64c3350eec5`  
		Last Modified: Tue, 25 Feb 2025 23:49:20 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa54fbd646cc440a9ddedb9ae480b3b87957aeda3718541bdc001b132ab08fb`  
		Last Modified: Tue, 25 Feb 2025 23:49:20 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:caac32f2b8412d22396a0869fb7d4db68970107b7254a2a647b2e47bfdeff5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130169749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56351405eaa63bf5d4f5444dad5b63f6ef61baf476579bbbefa9d78b7b093f08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25045481df7a5d89289e36a7389bf9abdb2aa2a7550f77c6a9284723e66abad1`  
		Last Modified: Tue, 25 Feb 2025 23:31:04 GMT  
		Size: 295.1 KB (295129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ea1fd7113951d2f0ff9a9824c4749a117ae67be28d96b0ab33e27305a83954`  
		Last Modified: Tue, 25 Feb 2025 23:31:02 GMT  
		Size: 126.4 MB (126402793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486048da9a6c8e883bf9fcd4cd011391ca9302bf758301ce0c0490176bf3cf55`  
		Last Modified: Tue, 25 Feb 2025 23:31:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d42391a3e293bd2a04874bba23d7a42a598628d8d258bffa48b43551b25cf2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 KB (229779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e776e0ca0a146803b87861ca4dd4c8161cf20ccac49000806971f0f6827f9365`

```dockerfile
```

-	Layers:
	-	`sha256:c755640860b68d81ea0c65897e17da6a5d5bd1159798544f8eca624ec1464ce0`  
		Last Modified: Tue, 25 Feb 2025 23:31:03 GMT  
		Size: 205.3 KB (205300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060145bea61c094503aadbdd737c0ddbe62a15b27ad51052dc153e4c9f5548e3`  
		Last Modified: Tue, 25 Feb 2025 23:31:03 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:3bed7f63b6833c4dbd55455935a7ba7826d7a9a40fcc5053b95cab79d891f580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128825595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d833dbf1a102d0184eafda0a02765f14eaf3a6499cde59ea73bd5500502cea2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed507fc5d64b2e3137d471f9a078a4add3c6cf38450cd6a53d7d3aef6ffec60`  
		Last Modified: Fri, 14 Feb 2025 22:08:09 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d28a5af7632832dbf0a9896248be932971aba4af06c89b659315ee4a42081`  
		Last Modified: Tue, 25 Feb 2025 23:32:05 GMT  
		Size: 125.0 MB (124951869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9966541db0043c9eb8eb3f165b45c4b049c0d311d3922c4f8f9e988d1ee7fa9d`  
		Last Modified: Tue, 25 Feb 2025 23:38:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:550196b7e0a2a941f498ac9e74e38f7e0b67215e86454156ec303994a547b454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e080c3fa16b6097f46263f8c14001582de9f577be6f999d196600d6ed254a80`

```dockerfile
```

-	Layers:
	-	`sha256:174472a0f8990374a0cd5c195510dd3863dc602af61594b1714b0d3e3a3996ed`  
		Last Modified: Tue, 25 Feb 2025 23:38:38 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eddc6c000cd22fe3c90660a54c16115eb4c198d7e269e9ce12e0f6ee9e364a8`  
		Last Modified: Tue, 25 Feb 2025 23:38:38 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:b9c49069db7ee80c3f67a2507a20a3ccde838ab7890a6e6f73f423cdfb0de75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129007496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305bd88e28364d1cee1fe9d8a2ce5d062cca1ccfecde5ef2e52f4084488953ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:0cd9ffc10fd27eaf00487a985d3d6937522e17c7cdf03f77def367bc29eb78e7`  
		Last Modified: Wed, 26 Feb 2025 00:21:32 GMT  
		Size: 125.3 MB (125338659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a78cbca08c7d85a9cc7d9fe43be83625f77c61d66d0ecb776e3898e07025cbd`  
		Last Modified: Wed, 26 Feb 2025 01:13:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:422da056f3c94f0ab6f7e6ab63fd5baad8d7e410f061ef08ab779af7fd48ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19d44309c3009bc04480aa3d1c13599f6271f44c0bfb7f926b92c4073ad297b`

```dockerfile
```

-	Layers:
	-	`sha256:699e5056483aed23fa1b61a168af43eb8154e35146c72cf05ceffc3f0ba33c5b`  
		Last Modified: Wed, 26 Feb 2025 01:13:40 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:747ce66c1259723f8aff63ce7c93c6aedef425f0b893019d7890c1861f2ce6d8`  
		Last Modified: Wed, 26 Feb 2025 01:13:40 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:42099984e51155f477847f9b6e5cc4b44ec00946a9a82508078150e69570c418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131094724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e075cd69ac5d913bb2f085b7d6cd0df51c68cc406327c9117eb4b01b10a232d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709930918ff9545f85bd2e4cac3925cbdbb8c11ea2e9a6b1dfe4c10549f601f`  
		Last Modified: Fri, 14 Feb 2025 22:45:22 GMT  
		Size: 295.7 KB (295701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0708d6fc70d6c17d917a582922c9c9c869293636d289db2a690696469b90d8`  
		Last Modified: Tue, 25 Feb 2025 23:31:35 GMT  
		Size: 127.3 MB (127334743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d4640bd7c855caa925bb2cffc2099abf8b0c01f0d2a33855b8379530eba14`  
		Last Modified: Tue, 25 Feb 2025 23:37:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4e905e717d7eaf8a22f4dfeab5b085a2ae8c8a017e5393483e7fbec039d9cb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef2d4b6305d1d0247b4711fda87c81e558ce5819319e2d0e12bd365aa7da138`

```dockerfile
```

-	Layers:
	-	`sha256:6ba18a599840fcab2d34a8708bc7b7db18776f86891c5475a0b2ada5d51d9b1a`  
		Last Modified: Tue, 25 Feb 2025 23:37:36 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8bb274268af85e8a117dacc4920a427429c405487de573876d633bb2805aca`  
		Last Modified: Tue, 25 Feb 2025 23:37:36 GMT  
		Size: 24.5 KB (24509 bytes)  
		MIME: application/vnd.in-toto+json
