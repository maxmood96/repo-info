## `golang:tip-alpine`

```console
$ docker pull golang@sha256:62cf1726e3715a0a57bcffaa2e60ccae6f8d1af9105a142e589c9f9028208ac7
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
$ docker pull golang@sha256:89c78ed2a03c4c19d1d202ff2378764b7bc39342823cdf238ef51d84dc770e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133469743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64240af97bda98591585bf058d6c59b71c276560bde4c2c28a84ca350c000bd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b639484f3d1709b49575007df75ec67daea71be112a7effd12284220e011eaa`  
		Last Modified: Wed, 19 Feb 2025 01:11:25 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc5764bfa5625e90d4c9d1c4bb7361ceb8d3451c8f3534f5e3a80e9f8aa6e4`  
		Last Modified: Wed, 19 Feb 2025 03:27:14 GMT  
		Size: 129.5 MB (129532433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0c3d76493d4f1d54ef0ced70658b3b9267448f559b85d009cec48d8d7b6676`  
		Last Modified: Wed, 19 Feb 2025 01:11:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6fba389655059e75065466a3b79a501acc501975ac7fb1e6332cf67d8322e635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 KB (239653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dc2b80699a58c711d71b1f6173d2db7efad0f4be751c703cf79ac1749c0cc9`

```dockerfile
```

-	Layers:
	-	`sha256:caf8355301ce48454dce652a5dd420f7a2f2731c507bf65ab6426b4b976f5716`  
		Last Modified: Wed, 19 Feb 2025 03:23:56 GMT  
		Size: 214.5 KB (214512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20c5b32da109570d6dc4fadee961a1774f3aa37485da60135fceb9494ac9278`  
		Last Modified: Wed, 19 Feb 2025 03:23:56 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:b6a903174aa74a89073b8102de0bdbfe93eaab3d59b28767667080600a3138b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126787865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9297941f0c0cbf6bfb680084d2805c82de108bb7e05881890dce77399e659fa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7c753da18c6057d83b6779f1713789751ec28a11c5c844455cb3e349d029a2`  
		Last Modified: Wed, 19 Feb 2025 00:41:25 GMT  
		Size: 123.1 MB (123126724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a577884ba070900fef6d822a0571e84028f07c54f26930d9b4305b20de713b0`  
		Last Modified: Wed, 19 Feb 2025 00:40:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bfd419be20f57f617ac8f7d274d2b7fae0c43822aba0f8a750a7c0049ddc3d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc06b361ed39445a0316539c346287f2d07e880386bc0443d7cc5b7a142bfd8c`

```dockerfile
```

-	Layers:
	-	`sha256:89190a8abb3a8340cdd2e1f11c2f7edbe26ec70ea5ac1132faeb9f589752b455`  
		Last Modified: Wed, 19 Feb 2025 03:23:58 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:134b15cbe02c2475a58e27c93a50e3d662f73b2154e7bdbaa4716ae976a9d134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126191746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3297b56c222ed21792e1528cac25419ce86bebb1f14dbd563629fa0915b9a6ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbce18d551f744b2f9a445aaedbcd8c5e283783570d9da4735469555773098f`  
		Last Modified: Wed, 19 Feb 2025 01:09:47 GMT  
		Size: 122.8 MB (122798265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffbc2ec7c3c32908d2d9906add3ebb18b2867012408d5f3a86eef4d729b8804`  
		Last Modified: Wed, 19 Feb 2025 01:16:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d39b5b8f2499412bd9ab9106532907a888e37298ad54423f9496403cf3cb9b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 KB (239774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208d3f58f89b6673db4d84184f86032a0d99487e79d573feee0d0fd424386a50`

```dockerfile
```

-	Layers:
	-	`sha256:c6bd31decdd65314ba36547e8d928f02ca9c5a1f3bb19af44dd5e70ad318e437`  
		Last Modified: Wed, 19 Feb 2025 03:23:59 GMT  
		Size: 214.5 KB (214508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b98de6a0055164ee3d9dbfe1b7f25bd5ed4e499bcfb4b373e7b850fc30a6e1`  
		Last Modified: Wed, 19 Feb 2025 03:24:00 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a1f38cdf1f779f3f22194ab02c9e8d6f8380d5ee9113f56512e3c41c47358117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126644321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dbadd61f729b83bd00c327b8254c36fca142e1199b011a0b4a2b6cf649b98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa1d43e92f86dc074668d0ee29a76fd40e91e4c4142a8f0580170417c1a1e6`  
		Last Modified: Sat, 15 Feb 2025 00:23:39 GMT  
		Size: 297.8 KB (297842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5298385c49d911d309658b69d6f0a6876dfdb4d5bed9f2c1fff825ca2fb2fcdb`  
		Last Modified: Wed, 19 Feb 2025 00:41:18 GMT  
		Size: 122.4 MB (122353292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c7e39536c14ab9ebd11af88c4bc55b0afee23b6797970554678aaf15f27bd0`  
		Last Modified: Wed, 19 Feb 2025 00:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b738d517e3dd27e4a1325c0612f83203bc168c32bdf3191c346b5e9095fcd002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 KB (239870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e49f3f3bef5217c4f2d33a5d7ffdcd9aabb38659e896558af6a88eb8d5319`

```dockerfile
```

-	Layers:
	-	`sha256:8f27a16c0238306292f132ed7e1f3f6c53d146e1fdfa9326c20247ebe869b6bc`  
		Last Modified: Wed, 19 Feb 2025 03:24:01 GMT  
		Size: 214.6 KB (214568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23bb81e9f6fc2c9513fd2264cf82b7aa1263806a88de5212ba7cb6e14d72476`  
		Last Modified: Wed, 19 Feb 2025 03:24:01 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:530bab76eca437fa427a16d88b862e88c6f6d0aa74f4c83a946bedd4d94debda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129926314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e254774309742e51a68c27c136bd9c9aa92fdcfec520297bf925db824a60fe8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0205f928731eefddbb6a451ad0dde798d79b9f9516d8307115d38b491217365`  
		Last Modified: Wed, 19 Feb 2025 00:31:47 GMT  
		Size: 295.6 KB (295595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865367c21802db35d933085cc324482ddcbb8bd28bfbcd89b6ea5d6a248d00d`  
		Last Modified: Wed, 19 Feb 2025 00:32:09 GMT  
		Size: 126.2 MB (126166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e08cbe9a4023c0792bb565bc8629eafe793a9b9f59851e0b38744e198d9d70`  
		Last Modified: Wed, 19 Feb 2025 00:31:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:51d9a74fcea2e1d9776f5b7f58e23706ddb4f2396c4af42c08c8ea7441ae5480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 KB (239546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520e2a4ddc8461c89528ae632056365b14b017d130d81602f1510b21ba3371e2`

```dockerfile
```

-	Layers:
	-	`sha256:c30bfd343f07b2c0851138955c6826878185048673f33fd841e865b48b9c8d41`  
		Last Modified: Wed, 19 Feb 2025 03:24:03 GMT  
		Size: 214.4 KB (214447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd97ceba161dca7d4343ff6cb84d230ef4859389ad1e5d2fe61af1eb22429050`  
		Last Modified: Wed, 19 Feb 2025 03:24:03 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:cf658e7c329cf676de0569e9d013ff51f24c0dffaabe994c95d583eee7e830ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128565767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2b5c3859e407f7f9d94eaecf7fa659830965292d5dff10f7bd96a91b02343d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Sat, 15 Feb 2025 00:31:41 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c08a2f45c0cbec2efd7e342b73e4171953b8c39e916958809f4e692e3c7803`  
		Last Modified: Wed, 19 Feb 2025 00:37:08 GMT  
		Size: 124.7 MB (124692997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864270ef519ab7522b7b303a58b80e03852266e3742349feb5bf2d0058352507`  
		Last Modified: Wed, 19 Feb 2025 00:40:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:757f3c6a75f45dae54da162d07974143be141c2d60b0ef1aab7cb82e9c38ba8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0104315344a824c383a707fa7b822986948a6dc0e1db55407523bf0b1c994edc`

```dockerfile
```

-	Layers:
	-	`sha256:7923a8edb9177482fe852084e84b07792c3855090422ebb527882a84bf103bf3`  
		Last Modified: Wed, 19 Feb 2025 03:24:05 GMT  
		Size: 212.6 KB (212635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3a49009e593569b1cf86fd226209ec021168f00f380729da42af4537633e62`  
		Last Modified: Wed, 19 Feb 2025 03:24:05 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:004725b83c69bb3e6dc226ee6295fc2b6e593fd6ece49082e82b6594d45334ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128753725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bc2e19e6bd949a247ea04626708d57ca8bbfbfd2b90e67406532b78adf87ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7eb5cf1a2de3fe410bd8c107c6d71f5982e896c65d9c06e257a35dc3749937`  
		Last Modified: Wed, 19 Feb 2025 01:24:07 GMT  
		Size: 125.1 MB (125106781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df2b2050cf66b18f1a1c8d013797c382c45c7639610d5d93f9f54f44d3733f5`  
		Last Modified: Wed, 19 Feb 2025 01:23:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:97ca4164b9b49293df8dff8907a7757b799ec70644ed02ba0236a458345d3d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5673ea587eabcb4db96dbac8ef3edef864d42d6219c82469794ea735b69254c`

```dockerfile
```

-	Layers:
	-	`sha256:8848eac57fa56bf3fb9aadc5dee32dcf5324b022629f311f1d666152e50d980a`  
		Last Modified: Wed, 19 Feb 2025 03:24:06 GMT  
		Size: 212.6 KB (212631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0516755250f44d754382fc7ab670a18ab6f99c8c3cf36b5aa88a50d040b73f9`  
		Last Modified: Wed, 19 Feb 2025 03:24:07 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:ade7bb14369ed1d68c6bed093619e1deab26066b347f77738a4d01057c322177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130861055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7602a029d44c2e41d626939cccbdcd83f9c1f72a65ca3c5b99f7a89cab7911`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:02:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311c8f145699dc7db93b7bdc96735f262ad8c55b79caa71a6a51467909f939e`  
		Last Modified: Wed, 19 Feb 2025 00:48:55 GMT  
		Size: 127.1 MB (127097152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e11b852f1783d6b547e795650a10b3a3f3bfb4b02f788f3c77ff31134b44e07`  
		Last Modified: Wed, 19 Feb 2025 00:52:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5637a4b9ce8be9cd868b1eccccb480faec56ee06960a8ced27357871b7c8c59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d071b9c25fd3cb797d1cf8e7f0a21300940be9fb59bc0de06919b140647b1aa`

```dockerfile
```

-	Layers:
	-	`sha256:bda7842915148ee6b2462e0a8ced9e15912cd6dc635c69a17daccbf39f5fdb57`  
		Last Modified: Wed, 19 Feb 2025 03:24:08 GMT  
		Size: 212.6 KB (212561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a12622a4769cdff7629e4e4d064e4b80eb300f9c117b1cf229ce9616b737c6`  
		Last Modified: Wed, 19 Feb 2025 03:24:08 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
