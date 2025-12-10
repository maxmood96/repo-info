## `golang:1-alpine3.23`

```console
$ docker pull golang@sha256:26111811bc967321e7b6f852e914d14bede324cd1accb7f81811929a6a57fea9
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
$ docker pull golang@sha256:6d6d1e4e530e8512543843504590c86b30524dd8644953c3435fa5b3396ae39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64306870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b00cbdd8095aa0e4a76b2b35c4448f1605d8d47a664599f6c20e63925fc90e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:34:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 00:35:00 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 04 Dec 2025 00:35:00 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 00:35:00 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 00:35:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:00 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:35:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:35:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80e74d593b62cc59d61ecd95653cb3d0dd0226ae6359525c776cc9c688119b9`  
		Last Modified: Thu, 04 Dec 2025 00:35:21 GMT  
		Size: 296.1 KB (296082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6da02310d1c3c4cad24b10d7a7d3b8d336907c0fde2f65770e9b8a4b509962`  
		Last Modified: Thu, 04 Dec 2025 00:35:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f6ef5fb9ff440345ff4cc972a9431434b349f27f7cfce65f82c97586f1a09b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292b2bf2cca6dd23322190ac7b36073b479292ac59a551f10eb33dd1343fb2cc`

```dockerfile
```

-	Layers:
	-	`sha256:d70ab9b92cde3d789c14b535e051b73105e265d4442affd2a3d4561821ecf45b`  
		Last Modified: Thu, 04 Dec 2025 03:23:17 GMT  
		Size: 195.6 KB (195551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340eb631e291ba570d9942831c68ba118e70f2ab497ca6fc6677253233d1a30d`  
		Last Modified: Thu, 04 Dec 2025 03:23:18 GMT  
		Size: 26.0 KB (26026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:c07ca287f049960e8b699d433376d879b7ee3e576b1e0239c476d9b28c6343c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62937277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694770bd0d061052c3442d0ca00581742faf7ea63bbc08ac1796a288ca5d37f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 00:35:06 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 04 Dec 2025 00:35:06 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 00:35:06 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 00:35:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:06 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:35:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:35:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5873fe854771c78c6ae5603250e1828e1986589ca7ce818c9975908be736a6`  
		Last Modified: Thu, 04 Dec 2025 00:35:24 GMT  
		Size: 297.3 KB (297269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd4211ee5273ca0c5772840c1a03b86bde39c606d1c608d88cc81d6d76501`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 59.1 MB (59071955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99ba0a71ac8ce5b03105ea0095ba5e728dcf2972d1f89b80df3f5362036ccf`  
		Last Modified: Thu, 04 Dec 2025 00:35:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2c8760908f343d584ebdacf32e04423e4b55a98662fa884abd01730d12d1b575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3accc155cf21b8b8dd65b2939ad50ad2400a79b9ee4b1a9b92a38ee1b4297229`

```dockerfile
```

-	Layers:
	-	`sha256:711f3949549284216a5161cd4663cf4c596cb57f1bdbd9ac91af9be61843212e`  
		Last Modified: Thu, 04 Dec 2025 03:23:20 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:7ad239754266f1df6cf3e66d77ff30ef4f9be70c4f08212eadcf4c1320a9bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62646871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0344e4a1bcbd41e8a7b2a52fa1e05db73b038b00caff647c1796082401af04b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:35:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 00:36:51 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 04 Dec 2025 00:36:51 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 00:36:51 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 00:36:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:36:51 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:36:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:36:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9368362609f566aa3e6028c0ef382cd62fac2bdf04e93231c48bf387fac3f9ca`  
		Last Modified: Thu, 04 Dec 2025 00:37:14 GMT  
		Size: 296.2 KB (296184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fe74b46dc289f91b681e2a71e8e2e9166cf429f96ab9e99fd8e72a49b668c0`  
		Last Modified: Thu, 04 Dec 2025 00:37:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:56ff68a4c9d03b62384cab97b91631eb528c535ea6c7d2f737edaec85cae55d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a84a59218ef5bb9dc94053c1726251437e0dc1b7ae78a4458f56978b308ac7`

```dockerfile
```

-	Layers:
	-	`sha256:5e571cb2a8e1724365786111673ccde04b8cb5c9c66810358b710398049a9a27`  
		Last Modified: Thu, 04 Dec 2025 03:23:23 GMT  
		Size: 195.0 KB (194955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d156cd0251363d248aea98889373ffa3ac2161a24fb93997f978b22aaf264be4`  
		Last Modified: Thu, 04 Dec 2025 03:23:24 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:61d787e34e3c42e178d475d8ba5cc900d993320798ac2e96bb1f0b5ff4ba74d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62145088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bad32bb6f74773f2cb5e68bf30b7454d0505b18fd21db4d7a7d96c1310083b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 00:33:21 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 04 Dec 2025 00:33:21 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 00:33:21 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 00:33:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:33:21 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:33:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:33:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb58e72b5cd2098cd4f120c6a4026cd0f0ddd4495dc4d8d9e77321768ff61272`  
		Last Modified: Thu, 04 Dec 2025 00:34:11 GMT  
		Size: 298.8 KB (298812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505fea3824f0bb50ba892599fd8ee835c3321d58158efdaed72a23626947d28`  
		Last Modified: Thu, 04 Dec 2025 00:34:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:90cb45ade9d7c57ce83649ea75b45b76f6e58db87530387355c6de45468d5d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b96123396969a3270fc71656e6945f362b88b78ea6fe24de40468c22be049`

```dockerfile
```

-	Layers:
	-	`sha256:b159056852e2603a5d983e50c4d1268fb3c9343f5d2044269a313b24c2d47c56`  
		Last Modified: Thu, 04 Dec 2025 03:23:27 GMT  
		Size: 195.0 KB (195005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becf6849eda8acbaa3b25f582c2b1a84bca7d403ee21134b1d0a26ec76c6b8cb`  
		Last Modified: Thu, 04 Dec 2025 03:23:28 GMT  
		Size: 26.2 KB (26208 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:e25f467a5d289b25197a26f3d964dc23d67179d952464cbea2aee261c646ee74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62854630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b36cbbe60ea10b4088bc54c09b01350fb7826d2d23a9fb9569fa14d050370`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:34:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 00:35:41 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 04 Dec 2025 00:35:41 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 00:35:41 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 00:35:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:41 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:35:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:35:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83cf786400950939c3307afe35487d339b945967f484abe23cc6c9681868ad8`  
		Last Modified: Thu, 04 Dec 2025 00:36:03 GMT  
		Size: 296.7 KB (296677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd768d222d67c1de37c0910ccf0820e49305f1a100eb68a6f3b50c97bcd82d`  
		Last Modified: Thu, 04 Dec 2025 00:36:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:76b48724f2eceedece82a3e7c6369211fa649a59f2f8389d66b4e0545450c26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6af20afa290bc4fd8a4c8d8ea46e8837329868e11c8f4814dbccda6914c7d0`

```dockerfile
```

-	Layers:
	-	`sha256:316e0c05705747e155d94a3c5d61a0b335f268921459916abbdf58d8d04884cf`  
		Last Modified: Thu, 04 Dec 2025 03:23:31 GMT  
		Size: 195.5 KB (195492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef8cf86c106cf8d0e0bb5f016c67bc93b9e180cd32b00204d8a08e7090893d0`  
		Last Modified: Thu, 04 Dec 2025 03:23:32 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:d5256ed4d19fef8e601feb46540c79422fb7b4dbe795a71fac3558ae82bb2745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62261366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a46c974f0780a6bbe8a2968caa42bea46beb0a88837a126f6cb00b2d1fdc1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:09 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46fe31eb99c053ebac4e4c6c1a45a59669d0a894f8d034aa0117e8363cd3e5b`  
		Last Modified: Thu, 04 Dec 2025 00:33:51 GMT  
		Size: 299.2 KB (299245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402132cc1cfdaf9f5a53a67553cd2c688a690a0225ad3a0c33ef1d870320431`  
		Last Modified: Thu, 04 Dec 2025 00:33:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:9b100930a1aee21597266bd38b0931f3071827c5c6983c31803d8a85575b2c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3631f97119c3ebeeae7aa9936834cc2325fe1889cd2fabc9721498f64b6d3b1f`

```dockerfile
```

-	Layers:
	-	`sha256:1777139d767fd08d6b3ad90d0f3afceeb96bcf1c3d90bdf0f082f5ceaa780dea`  
		Last Modified: Thu, 04 Dec 2025 03:23:35 GMT  
		Size: 195.0 KB (194972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be166a53723c2baa45800b9260f30d333790c99bbf69dbd647e50abaad79244`  
		Last Modified: Thu, 04 Dec 2025 03:23:35 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:009cd01eccb1b02c7cbd68719992b3cba77079f7bde5d72595bd7cd1e34555fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62552624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6501029fd2cbbc6751b4e5eaf2e7f1f24d71f28dad61a8bcd35f4bd604c5e67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:33:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:33:57 GMT
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
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d978112d183a69e7d1bc8e0eef2604cc2b23d417a71ea00afe822473ce9c84`  
		Last Modified: Thu, 04 Dec 2025 00:35:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:de6d74cabdb803d8b5f00ddb797c5afa0bb10e79dd3ad1e448271b157a567023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6360eb0c1136d1c40197a0e068088cf9d1ce83475db78e6877fad41225a698`

```dockerfile
```

-	Layers:
	-	`sha256:0eec3f22a27652a8b3204658719b421d90d4069304d93d5a0c72af9ad80e0f13`  
		Last Modified: Thu, 04 Dec 2025 03:23:38 GMT  
		Size: 195.0 KB (194968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d873a2a6807fc61f86582e681d4887592b8754e5cc931654997223789642305`  
		Last Modified: Thu, 04 Dec 2025 03:23:42 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:0d2f65482db7e5e90671c3b783af236698b1c9a6572cd8e0e4bc4745fc24d1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63508372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9060e0ae302c9ba08333e6a00c3a322fdee514ea23eba9c27f5aeba1a6410ded`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:11 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:33:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:33:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d25c90685dce29b188b5f808186e13517aabb2fb913b72d7b196b20a0850dbc`  
		Last Modified: Thu, 04 Dec 2025 00:34:26 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117955573446184fcc535c2bd9853095d14c620cb9e72162da062f7d550d9b6c`  
		Last Modified: Thu, 04 Dec 2025 00:34:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:3830cb35f90f3c3cfd73d94854d5b8fa24748390f1dd74dd9b5b529cde17b919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012f7346817234795ac51294aecff569d918c4db9c74db7f31397348cae550d4`

```dockerfile
```

-	Layers:
	-	`sha256:93353f41aedc02b0537a7eed1d89b53bc4d6102c9d741dce3b10789cb9eed6af`  
		Last Modified: Thu, 04 Dec 2025 03:23:45 GMT  
		Size: 194.9 KB (194900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020eefd6976fa3b4da4d0958d7faf44b0880fe1bada95d3a2155e808fd29e7c6`  
		Last Modified: Thu, 04 Dec 2025 03:23:46 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json
