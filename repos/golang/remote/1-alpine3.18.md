## `golang:1-alpine3.18`

```console
$ docker pull golang@sha256:45319271acc6318e717a16a8f79539cffbee77cebd0602b32f4e55c26db9f78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-alpine3.18` - linux; amd64

```console
$ docker pull golang@sha256:37b8d207240206f52620b62a9777ef7682b0bcb29556c9d3fee33922a694300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73027181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eefd9364cc8c9c9ec3eeba1dcc292c4814984bfde569624030c27dfef1eb082`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddd2bae0483c55458dbd912f7f69ed12965b8d87bd18bf321a6176af3803f87`  
		Last Modified: Tue, 07 May 2024 17:31:01 GMT  
		Size: 69.3 MB (69339737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7c121ad313345f45c8a8ff2381920daddc565d7767a2526646ef7324862c1c`  
		Last Modified: Tue, 07 May 2024 17:30:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; arm variant v6

```console
$ docker pull golang@sha256:84fb4a79968847aab5614ff1ea7e3a0caf44ba18a6589aa9f55d4a314b618fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71147233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a5638f6bd12d03c675c599ef5b1af102380e5eaaeaf7624daade0b89e455b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a62ca3b7ec271b904695d96f4ca628e05c0d9ab644f163c18f5422394b583d`  
		Last Modified: Tue, 07 May 2024 17:52:37 GMT  
		Size: 67.7 MB (67715088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3114b746e750d1a5039b16ead669d03cc2bfd99d552874afb0dcd039c00f5b1f`  
		Last Modified: Tue, 07 May 2024 17:52:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; arm variant v7

```console
$ docker pull golang@sha256:2e57541bf401b95bb81bf87459ac80d5e0875339aa877543d865c543bb8963e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70900714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40410a0646662330c22bc56628defa06f6e37f7a322f4f810de6c32de3358b55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b4809d7be867dc48eeaceb719e94f544b1169dce59a9a9c08766e4243de04`  
		Last Modified: Tue, 07 May 2024 18:30:43 GMT  
		Size: 67.7 MB (67715033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f78d50d16ddc626b592984bfd646d75740a6eebf44e6f37e92b808547aea395`  
		Last Modified: Tue, 07 May 2024 18:30:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:64cf4de143277bb4a62dca75e283a956d15da7950b2719fa505b7d9941a49b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69891979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15764b60211e4ed4dd88e24a5be66d933a068343e01ebd53785a8e166c83c49d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaa103b63dd745d677f7cb9d35c5d6e22d449042087f38a5451c5175341412`  
		Last Modified: Tue, 07 May 2024 17:43:15 GMT  
		Size: 66.3 MB (66272097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4b0ff524f9482b91f8b30048629a4d585b1a760aad57f8941ab53e9c21c33`  
		Last Modified: Tue, 07 May 2024 17:43:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; 386

```console
$ docker pull golang@sha256:a39cab6f2cbaac1731c49794ceb882b8937411534ae4bf07919eeb54815517a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70866650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecad2406681963e51a289ba6ba012732eefec5db7293bc881775ca78211c1810`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad99eb137f50aa798a99a3c38ecc849cc342af7b25aa96234a6fff61c914372`  
		Last Modified: Sat, 16 Mar 2024 00:01:21 GMT  
		Size: 284.5 KB (284492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c734c25548b187f7b1a5058ae3b484e84ed1df8d306b21e14051d95a9132ba37`  
		Last Modified: Tue, 07 May 2024 17:43:39 GMT  
		Size: 67.3 MB (67342888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d6138134f81e6db44da98b59965c1fcf3e0e006ac600fda90cf5097848e2bc`  
		Last Modified: Tue, 07 May 2024 17:43:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; ppc64le

```console
$ docker pull golang@sha256:dfd2d6fed1b31dd49fd7fb2c4cd50256e2ec0a50bd8ad6217812296d415a2726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70063465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6c9178221d7f4b2c87218178d797c9313445d0c775dd5df0a3d1afa1cf39a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e98c55e4a7bdf760c7d2ed441eaadaab9516a6b9d5e268c3cd14788d28efb5`  
		Last Modified: Tue, 07 May 2024 18:28:24 GMT  
		Size: 66.4 MB (66428102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500f0051b3b7a629a2d76e70af38eebc2bf3341770573f439130981f4713789`  
		Last Modified: Tue, 07 May 2024 18:28:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.18` - linux; s390x

```console
$ docker pull golang@sha256:1e32086bda536bef67b78d56257c89fa5ffb2e1fd30551639329de311130cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71899016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa71e8ced800e334dcc887b2817fc4081bd765517a4a6ba88b3f9dd4b6eed5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b9333c3f568da7d935fb17d75b0886b0cc18d28a8dd82c54bb454842e7c811`  
		Last Modified: Tue, 07 May 2024 17:52:42 GMT  
		Size: 68.4 MB (68396191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be3c6f74bec30d11798824821e85574298742da4d689c2d4d57d61ffdb730a`  
		Last Modified: Tue, 07 May 2024 17:52:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
