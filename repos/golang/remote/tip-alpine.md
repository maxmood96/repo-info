## `golang:tip-alpine`

```console
$ docker pull golang@sha256:53cea4e23fff6d146b8e449310bf6ec7fd9e5b4c46b3c8b31add5b2b4993390a
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
$ docker pull golang@sha256:8d6bbeeb9e23ddbe114aac1ca189e91c4d8411c004eced68b2147898948778a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99185505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205cc1a37cd0cfd556215274a7dad40cc3bf5f453ee3e9928201e318f40bdb64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Mon, 15 Dec 2025 21:22:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:24:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:36 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:36 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81a14145f4fb617e99ef287ff52f4c0ef59b3c9cfe910e805ee9aa4d43ce048`  
		Last Modified: Mon, 15 Dec 2025 21:25:00 GMT  
		Size: 296.1 KB (296091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc02f84f9201c7821773dd34545e63ce7af776f9b234f6a13b2589fafa66eab`  
		Last Modified: Mon, 15 Dec 2025 21:25:12 GMT  
		Size: 95.0 MB (95029942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874f5e2e2a5b78b5b9513a1a2bd69b7431effb3196d720ea058bef334450754`  
		Last Modified: Mon, 15 Dec 2025 21:24:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2fa43d8f2c77f64ea5d646d874020e01b7f12fdfa1342016f3ffa9a3735b4d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cea07ca324d9839c48e5a48bfde10e8886e87a6633184f2989c6b75eaadf71b`

```dockerfile
```

-	Layers:
	-	`sha256:04785495a6f63acf61bdcffd18dc0636fa25778b661cd365bc1a43b5c3a9ef09`  
		Last Modified: Tue, 16 Dec 2025 00:23:52 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b09f70fd295b79cdeb30ed103ebad9b59b528d6d961f0afed02414611315854`  
		Last Modified: Tue, 16 Dec 2025 00:23:53 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:a89a75c03ffb3e97f5df8a022d942e2482d8aa44e8ecfdc97322920511d47f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95237050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bab407e9ebd46568b1c36b7e2a74a84f3b602c9ba46477f577cda0bfbdd441`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Mon, 15 Dec 2025 21:22:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:24:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:53 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:53 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fdee579c3c4db0a94f5f4266eddc7c38eb8888a64b29e04ba06a87c04dfb45`  
		Last Modified: Mon, 15 Dec 2025 21:25:17 GMT  
		Size: 297.3 KB (297280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0cc28daa6cb71c3b81eacc797539f92a25b64ec51c9f53341c37ef04e417d`  
		Last Modified: Mon, 15 Dec 2025 21:25:29 GMT  
		Size: 91.4 MB (91371719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373bc49a97c4fd5a9d6d126068e21392914ece642ebde47189918103dac5c52d`  
		Last Modified: Mon, 15 Dec 2025 21:25:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8c0cae6c50ad9fd28d13a5213e9acfcb3545ca26402072dd87df7ce60d981be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2605c8b0d044488e30f17b9641a931c2d4ee4f97459564b9785c95e0b1006df`

```dockerfile
```

-	Layers:
	-	`sha256:19146bcd060f528c22e0322d8ba37ad7930f79c60a22b744379929219ed4d59c`  
		Last Modified: Tue, 16 Dec 2025 00:23:56 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:d08723e515b4abc92c8b9f45c7b0dfb41813aeeb42b57363975d50d7247c22d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94676045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f140a6d38fbaa2db483ffcfd0dec20c94bbf9b0ef46fcc47162baab4eb098b3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Mon, 15 Dec 2025 21:22:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:25:32 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:25:32 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:25:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:25:32 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:25:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:25:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9efa8b45add2445c2e0c8367e3e196347580b237b2decb8f59dd16c2f412ab4`  
		Last Modified: Mon, 15 Dec 2025 21:25:59 GMT  
		Size: 296.2 KB (296191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb87a632660b1037516c680a04b7758d1bccc030a199d5938a3d13de229878`  
		Last Modified: Mon, 15 Dec 2025 21:26:06 GMT  
		Size: 91.1 MB (91101231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef1b0d686fc28331c0afd467893468f74f7d253e0625e002782b7aa151f194a`  
		Last Modified: Mon, 15 Dec 2025 21:25:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ed644f2bb42332f176c0045576e19ba74cf80ee934320bcb84167f6dd5c115bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b89c1b25a2ebdb51f9b1c39ef742c6b64b54cf586f04e354de8f4d84133cb3`

```dockerfile
```

-	Layers:
	-	`sha256:3bccd2a6a553c0533b3f101c973090a3189c86fc5e8b619743608be68e4ba5ca`  
		Last Modified: Tue, 16 Dec 2025 00:23:59 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce7c25cdcfb757b63d662ede2c8be744245d724ef011bc698b9451685bea251`  
		Last Modified: Tue, 16 Dec 2025 00:24:00 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f5dfbba269fb70c0c0db4f578210c92ebca889c80711470f24409b00bd8266ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94602547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c6c9bd9b280f2397bfd70b437989a0ea64e6e0c5b6e41df1ea053984dacb0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 15 Dec 2025 21:22:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:24:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:15 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:15 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b27b6074337d03e4d2f3c52ca5db141de116f1bf2ee228b4e01f1b60839146`  
		Last Modified: Mon, 15 Dec 2025 21:24:40 GMT  
		Size: 298.8 KB (298812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7781f7b0020f1ea08137b4961d1e1c8dffbf5d0dd96335fd03fec85f64136`  
		Last Modified: Mon, 15 Dec 2025 21:24:55 GMT  
		Size: 90.1 MB (90108378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddf59fae76e8891c0f1795492e367198476ce0d83019357c50e2d5e44f3a598`  
		Last Modified: Mon, 15 Dec 2025 21:24:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:52d2078f022b62466762b1ecbdf27ab7d8fe575bf3989630757cd71def4c5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a674e4b1f3a7e6b067f8e5fa2edc965afdeb005edf74e0161ebf35262af30d17`

```dockerfile
```

-	Layers:
	-	`sha256:d7a76fef6f2f63d5db0fb663b536ec9855d06c555062e8eee6ef0af78249e7c9`  
		Last Modified: Tue, 16 Dec 2025 00:24:03 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9242a418648384a17f9fe91a87e227444bcd4a0113ec73166320d750e86209e5`  
		Last Modified: Tue, 16 Dec 2025 00:24:04 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:56c24cf160d5927d3c7633acea4e8ac305f0c46945bf6afdd767e7f88078cfdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96901017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fce0d319b0dd7124af00184ff40f89d2a72b3c0b0d6ec4dec1f25fa9f633f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Mon, 15 Dec 2025 21:20:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:22:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:22:40 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:22:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:22:40 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:22:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:22:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8333dc90fdc671c104419686ff586eb730c98976f9be6eb29edbcba160074`  
		Last Modified: Mon, 15 Dec 2025 21:23:04 GMT  
		Size: 296.7 KB (296673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f38140e210287454904f48ab9f4aea2db0ef2d57fe485fd6478e18a07aa5b9`  
		Last Modified: Mon, 15 Dec 2025 21:23:21 GMT  
		Size: 92.9 MB (92918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b07899b079fd602d7d6bcb4d194c6d85260a3591ea33c6efecc84d10991271`  
		Last Modified: Mon, 15 Dec 2025 21:23:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5c3e5c642f06d4b1781bcc880cbbcb38189fd1895a9d60662e51c291a44e3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6eecc2d037f0ceaf4a0fa2bd528ad94e552d28584cb068678b15a6ce87ae361`

```dockerfile
```

-	Layers:
	-	`sha256:611563d422c906f7e001633dcebb2cd665ad62c18bcfaecb8fa26d426c0bc8a2`  
		Last Modified: Tue, 16 Dec 2025 00:24:07 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c174f03b243ede57f97753f4d5992321de07acfdb1069ed3229402b5ae828a`  
		Last Modified: Tue, 16 Dec 2025 00:24:08 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:8070436390e82176966dc8651943ea931b5c9fc8939a8e16908a986975a983fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95775928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e9a442a75a6919aad419000b5067457a79ce08f57bf4c1e82939b91db591cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:29:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:32:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:32:59 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:32:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:32:59 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:38:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:38:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d26687d4427959db5b2394319b9ac21d2338eaf775321e4a8f305c1ad04364`  
		Last Modified: Mon, 08 Dec 2025 20:29:33 GMT  
		Size: 299.2 KB (299248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14547495cfe8d3d44ce957beb44799d810dbc881ef14c6f75d1efdc8e9917f3`  
		Last Modified: Mon, 15 Dec 2025 21:34:40 GMT  
		Size: 91.6 MB (91649505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596e491651a1ac8d4fadfbad766014fd725dc86cd1228004ca3f2a50ebb1bf6b`  
		Last Modified: Mon, 15 Dec 2025 21:39:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f90e1107139f047dd4082e975b8a2090f88d4ed8c08fefbe0765c480297b36ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (219980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e511c98fe97d1ff0bdb79816486a2701a61a7550d52915e7f96c7394730758d`

```dockerfile
```

-	Layers:
	-	`sha256:f9f98f59ca1ee31bf663b900b79505fb93214ee28ac16abec7ec53197ca02b5c`  
		Last Modified: Tue, 16 Dec 2025 00:24:11 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9013d7a23c9f822c17ef2bfffc052f6d92864df62e1e09393531c8c6a5a233da`  
		Last Modified: Tue, 16 Dec 2025 00:24:12 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:b72361cf1275aee5aa853e20dcec2625db35d69a8c22385fdff48f81d662d56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96169692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b776260175ab3a88ddbf8e81c345ce5ceaaa63c6cd70b0d479a60b5b209578d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOPATH=/go
# Tue, 16 Dec 2025 14:08:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 14:08:40 GMT
COPY /target/ / # buildkit
# Tue, 16 Dec 2025 14:53:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Dec 2025 14:53:26 GMT
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
	-	`sha256:57ccfd6d0019903e9f30a7248d0011153e90d92f7a748480439ea4f6363c5dfa`  
		Last Modified: Tue, 16 Dec 2025 14:16:03 GMT  
		Size: 92.3 MB (92289512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b1aee4eaccef7eebf4ff1c618e7cab730ced64d0093d134367706ce96d0e55`  
		Last Modified: Tue, 16 Dec 2025 14:54:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a8a38fb4699c2c09e6978680e5aa9441f082170bac10d2d5bd63a9d9a942d2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2376cc56a4a296c0ad01e4dc23f87aea08c7c7480164a4ec3570d4adaddf1e`

```dockerfile
```

-	Layers:
	-	`sha256:68b324447979b896997f5f6863914da4ed1a8607ec0bd9dc1c537690d56ee41d`  
		Last Modified: Tue, 16 Dec 2025 15:23:43 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b57d263cc83ccf95e5522b7993e0dc6f5b7ecb96da55fd40558b75e0dc1a1e`  
		Last Modified: Tue, 16 Dec 2025 15:23:43 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:45ce3d5eab37c4c8305d06bb51e1706f1121ab078e5ca0d978cb7f2246b52620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98219600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e98ac1aba360ac291e77ebafe32d96ca932b7814f3a1dcafc1ed1186eb26154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:10:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:23:24 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:23:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:23:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0495a965cff38fffc5035354b088c3d76314e583d7e3003bd53417892d478`  
		Last Modified: Mon, 08 Dec 2025 20:10:51 GMT  
		Size: 297.2 KB (297177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a1c518cab5112d07a0a3193c5ca3ef905e28d8e262915c8e207c186ea2395`  
		Last Modified: Mon, 15 Dec 2025 21:24:04 GMT  
		Size: 94.2 MB (94198456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe83f6ce0ccd65e37520a4e1571cbd5e865ea2d50329c47c67b99b3d304b5e`  
		Last Modified: Mon, 15 Dec 2025 21:23:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c512fd29691ad611c7ca636cdc699cad67857730c816c18f19fbc1cda7a5c291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26e664a7a38678a9104d3c2b27b098a1dbcb43b63e7f895a38b4fd0aba9b62`

```dockerfile
```

-	Layers:
	-	`sha256:1a797738067dccdd70f27cc3d0762aa44a64e0208113aaf4f74f10e45960a811`  
		Last Modified: Tue, 16 Dec 2025 00:24:15 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4153569cf7f035b8be9a715d30aa065c20b7e6058a0ed75a26e4316f60e21a23`  
		Last Modified: Tue, 16 Dec 2025 00:24:16 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
