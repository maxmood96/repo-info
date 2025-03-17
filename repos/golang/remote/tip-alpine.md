## `golang:tip-alpine`

```console
$ docker pull golang@sha256:c281e5d3511dad8d5a95f03cfac4a52c2318ec85004b740ded10a3127f776e37
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
$ docker pull golang@sha256:f1bd3a3c0ae9bb2ea406a4caac9006bc97c2819f272ec0a6974bc6e3506c2ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129903095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f184e5d53658a1fcc23ea8bd41257ff90d6598c2d1e57667485109f3f41157fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20e8551bdcac550fc09257dbd22a4d8eef1f3d650c769f181a079b764341087`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 294.9 KB (294897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a83b25ec0e0c49ecd36fb9980281b7ce15ce7da6877f867a2e7766c298175`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 126.0 MB (125965793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3279598e7b927e75b676194957e287b500b37c88f0d9f2f7427a8c5dc18b2327`  
		Last Modified: Mon, 17 Mar 2025 21:13:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2c6fa01b98f3dd6d8c30ea2f8247ed10af1dbebc26f3d27411c4fd461dd4a83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f027db2596c4fb88c2e1a15af131692515a3ed4778cf1c8216979f3af1b18c28`

```dockerfile
```

-	Layers:
	-	`sha256:7f3427c7ac22dc8599a92cff472dc03a442b3654f20aef9072967a6dce0b3ff5`  
		Last Modified: Mon, 17 Mar 2025 21:13:25 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07bcf40ee7adc14954c68fdfc9219874dcb11193eafd66c0a3cab96298e528f`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:3aee397e64dd02398be8b108575dbe65c5f18cbf6346636b5e1330e8123e1f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124904469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa81675ace08e918e0db25c8d8dce3324405375c42453de62d887318acaff9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b09b35c999cf106d7ea623032afd4055be03b660fb3033618d47d166fe8b4`  
		Last Modified: Mon, 17 Mar 2025 21:13:06 GMT  
		Size: 121.2 MB (121243328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f709e5a44aa748c50b69375d4c015c4f2656e110fecd2a09650fe357497316`  
		Last Modified: Mon, 17 Mar 2025 21:13:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fd24afca4be32878d2ef8ba55ef39d067db38d419fd94e8cfd9da53f359700ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10706eea21003dcc5ea35debddbedfd41ab4d6e321a122039347b98e1972b4d`

```dockerfile
```

-	Layers:
	-	`sha256:1c6b5ad86d7573a2c287a4f879aa5b4d8311e0bc884e27a2b0888530584e80fe`  
		Last Modified: Mon, 17 Mar 2025 21:13:02 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:46b6e499d13934659942bb1d8bfdd34a12e0594c6e9b033ee24a1766afceae62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124295732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58329fb5e0bbccee757201822c1d0040611a16a138d3df003a7c91e6c332bba4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9907731a808176d84faa4a85282ae07e6a64aaf01c56d48e45253723c692ebf9`  
		Last Modified: Mon, 17 Mar 2025 21:14:18 GMT  
		Size: 120.9 MB (120902252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b1755f82b9444ccca7731d1583b5cb002705238d734cda2244f6fa70cc4b2`  
		Last Modified: Mon, 17 Mar 2025 21:20:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7fb8079d67a3c353069eb4d5a1ac67216af9c111f6ff152b7a57d46851e7252a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c35689e4649797757586a3235678f7e6b164f6a51a584807d8e63693307320`

```dockerfile
```

-	Layers:
	-	`sha256:7838ad402444602887bc06940d81523ea09745b72a0438ef0f941a1695830c42`  
		Last Modified: Mon, 17 Mar 2025 21:20:54 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5288908d2e0d082e89daacb6ef079b3129bdd6699540a4678bd253628f7a826a`  
		Last Modified: Mon, 17 Mar 2025 21:20:54 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fb5feb2dd2dabb34667b9b42bb7792b0d7b9f6f63af6103118621ffdd4dcdc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8555cd1437fc92bc93fb0f66d3a52414a66439f41482028c8c5f838c2ce0f9b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a2359180f5e29bb26ba5ebe6478f9c3cc6fe1fcd38d94f7289b2ab44088bb`  
		Last Modified: Tue, 04 Mar 2025 00:44:39 GMT  
		Size: 297.9 KB (297859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fec41d8cea8d405aa42d9093a8aac6c3163d9643759441cd5e55b364f8ad55`  
		Last Modified: Mon, 17 Mar 2025 21:14:15 GMT  
		Size: 118.5 MB (118503866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6001b1e53ac073ae35fc781d5b511195a37aaa53334b9a3234805751162199b`  
		Last Modified: Mon, 17 Mar 2025 21:18:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d4c5e712976c3c4a0e0f3259bba2ddf319c0d6ec777918ffbe534c2b5be23908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df295914f6f1d7097570903e15ed6f74810d970dccaa5d76e83bbcbb70838b55`

```dockerfile
```

-	Layers:
	-	`sha256:684f859a5cd8b26defffd8a4bb9a80c69bd5b184663ff73768f11e126cf03ae7`  
		Last Modified: Mon, 17 Mar 2025 21:18:37 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156c7c8bed5d007160d1cd4617fceed206bf059d9b44d7b92333172ccd66ebd5`  
		Last Modified: Mon, 17 Mar 2025 21:18:37 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:5695146873a3eb65cd1b4800e1e9ee6a415bac0047c79639cecb1f482896a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127827964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e7337146e47f32fa1c6733cb53e5c624598ee1feb2e231dc57c73633412b35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a589e6890869a1a20f83d52351e00d069f83a62c8516f06fe4d00ad4bfda4f58`  
		Last Modified: Mon, 17 Mar 2025 21:13:56 GMT  
		Size: 295.6 KB (295601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a94495553b1c250ac72571d6400e4136caa9f00d345a28d3faea166cf26f298`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 124.1 MB (124068582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a665e3d5348654953da966cf4de02cd9a18924a5a911c6f71bb077d57ef4a289`  
		Last Modified: Mon, 17 Mar 2025 21:13:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:224450db74d11be673280ac3039522a28ae8ef7af7cdb4132cfef5f97a050dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3993da9bdc03c9a3b9a63fbd849473320ea78904aa4a72c6de5f5e7ec5cebea`

```dockerfile
```

-	Layers:
	-	`sha256:354f9204cc3499dc88e8f4ac0d5a761bd31958d8a67b7ab380c1d9501fd6e2c0`  
		Last Modified: Mon, 17 Mar 2025 21:13:56 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437fcdc8c26e15fa3585411ae54bb83c755bce147247a6bf30f5e65b33141003`  
		Last Modified: Mon, 17 Mar 2025 21:13:56 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:aa36ac35be273d7642764ea4ba11c68615be7cccdf70995852ae52f4b1a81a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124666331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772e94fa01d367aeb45d657e2315b01d2b9bd93d9eb8573b321f49e01424554e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Fri, 14 Feb 2025 21:50:57 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c78cf9a0739a8dae1dc72464edfce0456a58eb76be29f8acb49a502b699b46`  
		Last Modified: Mon, 17 Mar 2025 21:15:53 GMT  
		Size: 120.8 MB (120793562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4bf650085a56cc713e275347b4b3eb1fe572e6104dc25e78264a66dca35864`  
		Last Modified: Mon, 17 Mar 2025 21:19:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c045d271743b2788123a41742dee429740e73548d5f056dea37ae6fa2b168e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb3df36fc88288779feec6e07cb547a3a297ad94cbb6a4ce07ee80798e948d3`

```dockerfile
```

-	Layers:
	-	`sha256:957f5ca1e56f18fb9618c144edc8bb87b85a931bd38717a924907bd527a8773e`  
		Last Modified: Mon, 17 Mar 2025 21:19:04 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d49c8c8b0f3d8488a5c1c5b4aaaf1ed22508d31a8f16920b7d2e0264c96359`  
		Last Modified: Mon, 17 Mar 2025 21:19:04 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:98cf6ef4e673d3f92f063e0fc84ad11abff31026222929bc0ff9826e65bdf5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124763023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fe2f892ac2321ef31eb1d1b4a25427212b689c6b0883bc22bcbc14c232c4cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23c3d122e10f89f67d5f0d04fc58493a27c641b4150f620cf4c1351b302229`  
		Last Modified: Mon, 17 Mar 2025 21:54:02 GMT  
		Size: 121.1 MB (121116083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ab20a7627e35c223d02c82fbf2f04a929726fa2a60a7edae419a03600ff123`  
		Last Modified: Mon, 17 Mar 2025 21:53:45 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:50ba4a64c6738fc5759da49f31a17940c5e53550b0c0dbf3abd69d1500ab7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b686f745fbae78d3a41280d139f8973b1484973c5d7f5f7aa853cede965573`

```dockerfile
```

-	Layers:
	-	`sha256:d83571ba5449997d409952bec376885c27ef1522c9a3d5f9f1728c4b7d3f84b4`  
		Last Modified: Mon, 17 Mar 2025 21:53:45 GMT  
		Size: 209.8 KB (209830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da512a284e8dc06aa4351d84703ac1d3746b6c28bdcf31ba6454a5e5e4f5ba7`  
		Last Modified: Mon, 17 Mar 2025 21:53:45 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:880c083636b3a1d383cdc5322cc28f7ae0885e581087c196237fe3692247e5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131323007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cc75558abff51cf75b0ce310c493fb3ac4d10b862d7d888b49a07183fa888`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 10 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Fri, 14 Feb 2025 22:24:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeba62321e032790263a70e54013602b15b70d9827bbb67e4e5c952c8d15c8a`  
		Last Modified: Mon, 10 Mar 2025 21:35:35 GMT  
		Size: 127.6 MB (127559104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aef555edc64afa92ec2e34ebb0430a8511b8c29a835437989bf39ad25b4654`  
		Last Modified: Mon, 10 Mar 2025 21:39:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7930b15e4e9c2f7fadef694c5613dfc73b62a1bc16521d12fbbb567ca144734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973e6d4968a5ff216bda31d65d103e29b4bf438960062085149083ec0c96dd1e`

```dockerfile
```

-	Layers:
	-	`sha256:987e9716d8f16a1b456871db757f31e5d8dd3ec32f358d0259eb66fbe03739a8`  
		Last Modified: Mon, 10 Mar 2025 21:39:00 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d30ebd30d4b7ab821453bcad7ea54ec5c007635d00b5cc216f49abed71e64cd`  
		Last Modified: Mon, 10 Mar 2025 21:39:00 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
