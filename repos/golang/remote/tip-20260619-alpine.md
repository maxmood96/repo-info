## `golang:tip-20260619-alpine`

```console
$ docker pull golang@sha256:9aea8e47199660d8ca0f7b643d243bcfada9d4bc25204b75be74578e62648d8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260619-alpine` - linux; amd64

```console
$ docker pull golang@sha256:1a29f5bb5c2b1f7f8de5cd117f86537b9967679a8b97bc199138622e53184352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106650997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718ef53ac0719a7a0f7913abec3198ce45561775b41a1bc4ef7c7f1e2a531e14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:40:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:42:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:42:50 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:42:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:42:50 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:42:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:42:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0380c3b83bdf1f1fe2a058c28d7056a74603596dcca855c469bce0ab0ab1909`  
		Last Modified: Mon, 22 Jun 2026 22:43:08 GMT  
		Size: 245.1 KB (245059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ced9bfc2a0ce47376a0e89056fba2dbdc199ef992671e729f2b29cd85c5af1`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 102.6 MB (102559388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05684d241dec2567636266271962470d5046fc01a74a9e403d8439b506a19785`  
		Last Modified: Mon, 22 Jun 2026 22:43:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:82eeaed234dfec6efe84695b620dace831e678fcffd129d29c2d5f5d7448a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 KB (201851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259826974e5f7c7efbe1df9cd65e82d661033f4c5f4c12edea936113d19bd159`

```dockerfile
```

-	Layers:
	-	`sha256:27fcb7644bd307f97ac16e2dad974a432dd0a1be12958cbf29b832f6313608d9`  
		Last Modified: Mon, 22 Jun 2026 22:43:08 GMT  
		Size: 176.8 KB (176752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b64ddf012880f710d6d082ca3f3eb335bf806fd405d855eda70ab93037f112`  
		Last Modified: Mon, 22 Jun 2026 22:43:08 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:50f9fb95c8abe626ec9a4d1da03b3b5733012a62714036d8625621176bb96787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102386313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccd59865631c0edb34187b7546fed5542ab4a7c278324fda7870bea68deb2ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:38:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:41:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:53 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:53 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:41:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:41:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443411d6d4d0648355d199ce53d29bbcca33126b9ba3744c7bea9daa76dc2588`  
		Last Modified: Mon, 22 Jun 2026 22:42:10 GMT  
		Size: 246.1 KB (246130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099298a9b55f99c5c1c21a12818fb4e2eaf7834dca329c07e51b1c2bab857622`  
		Last Modified: Mon, 22 Jun 2026 22:42:13 GMT  
		Size: 98.6 MB (98586575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53007c99a54825cee0b40a09382ecbea08966733b3e373920b0fc891e844d1d7`  
		Last Modified: Mon, 22 Jun 2026 22:42:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d5d36d2d053e17ccd954c07f46e90f65df572f9d25d58753b4c79b67aa9f38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b5c3dd8bd77e67a1d79ea1965c74a61a482ae6a0f4c52019c0a6bfa0f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:3f7370473afbdfd3adea90501bf807c8ea4afe4c3652b38313642a99bb27c0f4`  
		Last Modified: Mon, 22 Jun 2026 22:42:10 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:cac59eec74ee8ca3d61f23044090c80502b92ffc4e86f767b69bd0b5624774a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101782047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17657a365ec4311945409d9432edf1ea1cc8775de8ed3cce9fbdc45b3412137c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:43:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:46:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:46:50 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:46:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:46:50 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:46:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a93f35e6ed9140b158903b7b5abcf9bfc7b2967c3f2c42a50ca1176dfbc8c4`  
		Last Modified: Mon, 22 Jun 2026 22:47:09 GMT  
		Size: 245.1 KB (245111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6c0ac1bf1a1f35e41966874d41949d2c8d30b471f4a54f05d28249cc12bc`  
		Last Modified: Mon, 22 Jun 2026 22:45:14 GMT  
		Size: 98.3 MB (98276162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6351547d2ed433463ddeb021f81d4705c68ad7dab608cd0f997d3c90d231645a`  
		Last Modified: Mon, 22 Jun 2026 22:47:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1b3b2b85e075c115c63916ee50cac8ad049debd70b8320c4d9ddfb6549133e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effd5fc96c275075b52a7a82084d50d55e2f4e258e77bab45fb597c51d2b3018`

```dockerfile
```

-	Layers:
	-	`sha256:d3957865a6b7819bdaa87026bba79991c6b5766bb489dd47afa7d48febece82b`  
		Last Modified: Mon, 22 Jun 2026 22:47:09 GMT  
		Size: 176.1 KB (176122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e6729a9885595e7cf371c6ce3299ed3c20444a566e9547e5b7278e8b20a801a`  
		Last Modified: Mon, 22 Jun 2026 22:47:09 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8671844122b265b0a7bc653299d845b00fdcf44666719eb2dbbdfb59a98557ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101390138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7c8cdf42a9fc8f54c84651e7a077b16dbc2c722d209af4b92a10e0de25998d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:41:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:42:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:42:54 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:42:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:42:54 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:42:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:42:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7ac3a261b10961999af6279adf20d54e31228d1938685ace323bdc45b3c53`  
		Last Modified: Mon, 22 Jun 2026 22:43:12 GMT  
		Size: 247.5 KB (247501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4f06fe9b49ab2b0e448e3bb545bf0083fe0a192a188b8354bf30a5042489`  
		Last Modified: Mon, 22 Jun 2026 22:43:15 GMT  
		Size: 97.0 MB (96959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adc059975c3a633e2e74354a0fd7b8504fdffc99c433645ce538fda6af69d7a`  
		Last Modified: Mon, 22 Jun 2026 22:43:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bc8bc282ae692911cf621bc13c810985db4c29d29700c495b5b5cca991a40012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 KB (201413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453d25418d9d8c5750f7fe6125be7d6fe0334640ce03dd8cc381a8bb1999d3b3`

```dockerfile
```

-	Layers:
	-	`sha256:5b0bc5c5b2e4a478942d4d717af997107fb74ab109d569fbf1863d5b378c2b6b`  
		Last Modified: Mon, 22 Jun 2026 22:43:12 GMT  
		Size: 176.2 KB (176158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a48ddbf714717a55d0a3967d9a317eccd5835aa1509e96b646c58a6f0767ce5`  
		Last Modified: Mon, 22 Jun 2026 22:43:12 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; 386

```console
$ docker pull golang@sha256:91a86e738aeaa261667804acfcc711d8fe2e69b63c7510760d0adfd952f7d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104254888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e78074863188bd417f39cae49f1a3ec52a909939eddb2f8c89ee48d8cf448c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:39:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:41:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:38 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:38 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:41:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:41:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb865b796a7c4b2fbd016fef92bb0148d2d6f8339a9e0c94821dff2bbe1dd06`  
		Last Modified: Mon, 22 Jun 2026 22:41:55 GMT  
		Size: 245.6 KB (245594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675e2fd1600788af1a6ae5db185dc20a1f52bf11f13c9afd16f6795c307c09a`  
		Last Modified: Mon, 22 Jun 2026 22:41:13 GMT  
		Size: 100.3 MB (100338995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd931a963389d5fd8f449c64530636c223a316b930837506f0108170712a7d03`  
		Last Modified: Mon, 22 Jun 2026 22:41:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f9af531a7b22aa825b18042d2ed1e5fd7fd70a41709fd5ebe9344de83d284c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 KB (201767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc60f974054c8e556d1f0e3029e35c9fb6299a5f5f470edbfedff1e1353837`

```dockerfile
```

-	Layers:
	-	`sha256:59896a2a1b28717e91f15a1aafffb2e2e4cf7b5b4cb3bc542bfb4465f3608b8b`  
		Last Modified: Mon, 22 Jun 2026 22:41:55 GMT  
		Size: 176.7 KB (176711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e5741947b796bdc2cafa245f5de5d795b099301db2acab698cba4bacd4192a`  
		Last Modified: Mon, 22 Jun 2026 22:41:55 GMT  
		Size: 25.1 KB (25056 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:2ca2b8e8fef5eea5c4a561223e149db906decfc0ac5634e665b62df837e694b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103006764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de499ae6d2956c27d9d14d25b9c83af9772464f30e9f3d9f5f0627a2375f020d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:43:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:46:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:46:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e5cd9291f73cdfb8a0cc68e49e0664e71ce2e2dca0d970b3b935c603149a9`  
		Last Modified: Tue, 16 Jun 2026 00:44:13 GMT  
		Size: 247.9 KB (247921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91b5f722008c066dd2e397d03405537b7bb55f68febfb461dc3991d735b1c6`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e4bb6a473e664cb2c0e18f9d5a0422ca266d51a0d968d760dc1037257d6b9a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9059ee9436aca00e6bbf7000684d5b386a0fc7157fa264236bdd1cf12db27a`

```dockerfile
```

-	Layers:
	-	`sha256:edd89004fb4aea20a9f7de78fe11276a26b0f0833cb8b7ad28278b378217d714`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 176.2 KB (176151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eb8c0f1304f0b77f65c9e3cc8e1ff051ad111e62779d1c62974027e9d3b36a0`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-alpine` - linux; s390x

```console
$ docker pull golang@sha256:51c6396b4c206c2e022da305a6b33fd9c36314fd9aacac13c53acf09ea20652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104965433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f103c48a8f8b58114b230179e39c761360b50ed14b4e12f9755ce2fadbecf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 22:44:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:44:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:44:37 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:44:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:44:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea581a45d517537b12d2ace25efb5be190f306dc97d5a6254a6958f0786b2c20`  
		Last Modified: Mon, 22 Jun 2026 22:45:04 GMT  
		Size: 246.1 KB (246142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf953c950bf774a1558a2610c27217993faad44f113fb37ad0ee60aef8db0d`  
		Last Modified: Mon, 22 Jun 2026 22:44:49 GMT  
		Size: 101.0 MB (101009813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8d648e3b104c4dfdacc515ea29ca6142da995ee6effadda531d95ffa7049b`  
		Last Modified: Mon, 22 Jun 2026 22:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:056ba727931703015bcf7fdd509f07dfd5bc599174a7ac4439803edd8eebde47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 KB (201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb2c44c1ba9d00b9074e9c136e390c56bcbb86dce45b2f05e7f0e6dd3ad071`

```dockerfile
```

-	Layers:
	-	`sha256:550d5c14627ee80c0d28618967332ac32598d6d9515b387b139e005e45f946c2`  
		Last Modified: Mon, 22 Jun 2026 22:45:04 GMT  
		Size: 176.8 KB (176849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc9af5113f53ce2ceb5fcd0e37513f1ae605edb4eea3c56e62e1b5717935dd`  
		Last Modified: Mon, 22 Jun 2026 22:45:04 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json
