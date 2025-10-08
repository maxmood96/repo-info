## `golang:tip-alpine`

```console
$ docker pull golang@sha256:4e600afbb13f9735c87167420f035593592ad9ff39ab190626f149d34b0790ac
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
$ docker pull golang@sha256:db67e61d72240c7d304e53a3454dafef60b2f214c8ddff445959d29777098e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88691062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe523579ae13d380e29ea3a3ec0c25cb2d4daf76368283a9123d66d2d9073de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fff3f8430afdf202d1259066a2f6229efed835cec7072b4f86bc1a1bbb06473`  
		Last Modified: Tue, 07 Oct 2025 21:16:03 GMT  
		Size: 291.2 KB (291199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2359337f516a8ae9dbc401db1a30747bdee2967111d1cf5ef6007b2078d1631`  
		Last Modified: Tue, 07 Oct 2025 21:16:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8ef7a0613c1730ebcb04b8aa5195178e4180cd8c58d524b1708b0ee8693fee3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 KB (220361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007715e95496a2a2211ab42357ebc985282a3fad174cc436844f2791084104d6`

```dockerfile
```

-	Layers:
	-	`sha256:78955e555652f0dabaad123ea10bab5df54649ab9a9a22440bc9ed4ca46c5198`  
		Last Modified: Tue, 07 Oct 2025 23:23:25 GMT  
		Size: 195.2 KB (195223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a983f313580f7b5f34858f8e292c9f7db306871ca4eff890065b650e6173cb1a`  
		Last Modified: Tue, 07 Oct 2025 23:23:26 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:a353c6c255e799dc24e070304a5165dabee9ebf0b27e7403a0718db3fdc7b4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85594627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a82851e23ea282a2dd9cf854fcc13423104248f6aa3e0ed01a16f1ee27aca1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40096e1014bb7aabf190941aed00603827c68ed7a4dc0f3e23716e7d930f5d9`  
		Last Modified: Tue, 07 Oct 2025 20:12:05 GMT  
		Size: 292.4 KB (292397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ca929e1e82e3da2a8d3fe64f9852116fdde16db4405daccb287d008513ea4`  
		Last Modified: Mon, 06 Oct 2025 21:06:14 GMT  
		Size: 81.8 MB (81801162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f622e7eb3d2b650e6b0a90bee3d2f87e492ef2365c951991737ce3e2ffa1080`  
		Last Modified: Tue, 07 Oct 2025 20:12:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d5bb9d11eef8c986fcd391774bc28a3d345bd34c0fe8a760264f84afc09cfa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a4648058884b724e517dede29e67245831489082c4ade445827d4f1d248a54`

```dockerfile
```

-	Layers:
	-	`sha256:e5a927547682d49140e4130acbbba4ca5b304147dcf7cc1da8e3a4b66b15323e`  
		Last Modified: Tue, 07 Oct 2025 20:28:38 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:94dd00e198ed26e7dcba5f59c7c66658f834b60f87d3f6c8ef3a6ecd8d12cea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85060335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29590756f2628d1d1f64cd27c139614c19a5f3359bf53420c2bc7a515fd32afb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c2a873c95334b8e252450c323f795315649060840334449a95d11aabc2af41`  
		Last Modified: Tue, 07 Oct 2025 20:15:08 GMT  
		Size: 291.2 KB (291248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3744e969118c8670a28fad21e798357759121ccfbe844938fddafa0eed7844c`  
		Last Modified: Tue, 07 Oct 2025 20:15:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:658a07f1587b921411499d48a6d8f460e9dda8b9bb0a082050db1162bfe24928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 KB (220511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0b14b0bacad5cc4991755086f143bf137b4a7983928e8726f4fb95f94f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:2eab6547a6756b6a19fdbf0ed1c8aabb8cec1a53c7f37f3c066cc5561354eea1`  
		Last Modified: Tue, 07 Oct 2025 20:28:43 GMT  
		Size: 195.2 KB (195245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7de8c78d51a756fa47f49ad543360e928613671e955934d19e3aa90f137e83`  
		Last Modified: Tue, 07 Oct 2025 20:28:44 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b64789914c13af57ef9ee631ebc5d47d31b8aa33de263acc358c5e9239a97e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3067984145e50a11d5ef3023147eca8c1bafda35c875881bd7c552b4e4a36194`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1d5d2b8b46b0e172b456d2c806d4b4f09c1d93e67acb3938f629c400d7c4dd`  
		Last Modified: Tue, 07 Oct 2025 20:50:17 GMT  
		Size: 294.2 KB (294166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f9c5cd044ffc4c8df323cc4b003445908a15f9ede7709b380edfdee1d7d4cc`  
		Last Modified: Tue, 07 Oct 2025 20:51:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bacf270c829d7bc04141ae4e0a5a74278b8fdf1f3116179196c00660f2cabdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6686afb4904267685b0984680c8d67555bd7f8d473a8b6b44c98fd1acc75e2e`

```dockerfile
```

-	Layers:
	-	`sha256:baf6d3a38f07ed6c86f2e88b930ede372c7c35c5b6567b14fe0ff4f241ef25cd`  
		Last Modified: Tue, 07 Oct 2025 20:28:48 GMT  
		Size: 195.3 KB (195279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59268a22b91dbb6098956958513c2b56e54211f2f41092a76041bfd700e6facc`  
		Last Modified: Tue, 07 Oct 2025 20:28:50 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:f3543abf046ad5093f50b8256f8fb59c9f2aced9d6f8341b5ef731a8c123e1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87052299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d1a928b73e789a2bf3541bf9f3b4cb0c3e3f7920389718c2b27d3e27a93c68`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7859faf784948e9db8e1b41f100605d7f35c199628aa67ad507a926930696fd8`  
		Last Modified: Tue, 07 Oct 2025 20:14:07 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9a7bb0025d27718215b29ef2878d27dfd93976736f548d5ae2d65209d13c8c`  
		Last Modified: Tue, 07 Oct 2025 20:14:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6c255349917159efc3d7d7fc6d980ec1b8a10da31664b9440ccc38064907dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386eeea51aa7820876c316fcd6ca01583a61ba059211f78fc7466fee23d51ddc`

```dockerfile
```

-	Layers:
	-	`sha256:c66db2e5e69749e33258e2c0783ed325297ecaffe35430ffbb840bc303557d9b`  
		Last Modified: Tue, 07 Oct 2025 20:28:54 GMT  
		Size: 195.2 KB (195184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6fab7768b24a3b1c138c55218f9e9eef3509eb6e3478fdba96e7cf68f366b9`  
		Last Modified: Tue, 07 Oct 2025 20:28:55 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:b6ae5051ea0a36914a00d697e5f72abec01f7e4eea835703046e6bb79739ca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85889337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29a508502791a2d401e2bc9a73ff834c709d22a21e25c80557dd48a4acb1b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca2bbec3cff414f53adc5e9634f07a3fa7f1e3320dcbcc3b9d03910b13002d`  
		Last Modified: Mon, 06 Oct 2025 21:14:02 GMT  
		Size: 294.6 KB (294637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff7b705ba466b31cc39644cffa73218dd7521874b1e22293a6195689d04d1fd`  
		Last Modified: Tue, 07 Oct 2025 20:24:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:25a4e67617c1bbff9e8187a987fb089b3ef3924d74b577ca01454d73dda31de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab256413744fd908ab25dd05e75b72a63b558042b57d2aa7f294ce5f7f81a45f`

```dockerfile
```

-	Layers:
	-	`sha256:7f1f85c54d9bb25a949bd52d49ca427acb3d164a380484c16c35e575905380bc`  
		Last Modified: Tue, 07 Oct 2025 21:20:41 GMT  
		Size: 193.3 KB (193320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630cb54fbd2ef2f9cc2acbeec1b765ccc10740c399ff177e68147e3a2f717e2f`  
		Last Modified: Tue, 07 Oct 2025 21:20:42 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

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
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

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

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:ab620ecbc13df0c51060331635688f6b7d08c0dd1b19280178841c207559b37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13cf1e4dc80d2e6d634e6115e2195c6a9e366f68fe2e616679b914524fdfb623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a4b5681964cbbac71727dc93824660a7b57f0fcfeb79eaa856084f3c55796e`  
		Last Modified: Mon, 06 Oct 2025 21:12:02 GMT  
		Size: 292.2 KB (292182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0b5932aab13e283bc32b668927249f478267a5c013a25f5ea442d1f66bd557`  
		Last Modified: Tue, 07 Oct 2025 20:36:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:116668a60c166126b168bd684c326e3011ff75b53eb0a880a3037f9a881d6eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2480e12f6c75d85d25729704cc945ced587df32c9d5a66cfa1e78b54716f7a`

```dockerfile
```

-	Layers:
	-	`sha256:a514063ebdc350eb4044d61e6d43634c50aa385924c23a0b481248c4707959b3`  
		Last Modified: Tue, 07 Oct 2025 21:20:48 GMT  
		Size: 193.3 KB (193272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f4ded8340647d262e2adcb66f7229ae757ca671de8ad8a46e321b25d0e8fb2`  
		Last Modified: Tue, 07 Oct 2025 21:20:49 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
