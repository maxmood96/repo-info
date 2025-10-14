## `golang:alpine3.21`

```console
$ docker pull golang@sha256:95b0dc740258cfd003c74b16503c2a916c4a0c6715da753d16640f09ab28e26b
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

### `golang:alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:21ff7555c4fa67b93786eb8957d567e5cb3cac273ed682e0c25fc0139118db23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64084190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a81ab1343a46d4328f484a92f0ce7ac7548e54067013ed2cf7ffd488084839e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acde2ee2095fed96a211e676192f9f9b098313256a1ace9f61fdcb05f902771`  
		Last Modified: Mon, 13 Oct 2025 23:08:57 GMT  
		Size: 291.1 KB (291114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631faa732ae651543f888b70295cbfe29a433d3c8da02b9966f67f238d3603`  
		Last Modified: Mon, 13 Oct 2025 22:32:32 GMT  
		Size: 60.2 MB (60150352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efffc070653a50952b1fe3383daa49a9eaa2d275cea163abdca3b896aefaf3a4`  
		Last Modified: Mon, 13 Oct 2025 23:08:58 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a1b4e0dafca94b835edf6c86119afa14136c1744fef8412e29b3226603a419fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1312101e98e4a9084f707352482ace1d73e3c4bbf60e22de4105bb86460061e2`

```dockerfile
```

-	Layers:
	-	`sha256:7efaef7640563e46ddd9445408da1d0817616d0a4022eeeb93a0a7ca7863419a`  
		Last Modified: Mon, 13 Oct 2025 23:23:28 GMT  
		Size: 193.6 KB (193565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045568663169a4f516e836f997b4443142b26f2ac22b895b4a6bf3730b8a2afa`  
		Last Modified: Mon, 13 Oct 2025 23:23:28 GMT  
		Size: 24.8 KB (24849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:ff2f6100867bb4234803cbeb0c4d12028fc96577c97b4a0ea2c40eacb26dac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62730860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e688922da80e53a7462e1526bdfe190c2ee8a8933e4be629c88840070536a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a43c65d6f796de85d882d64adda76014a990c2b1c31881e521ed346ebb52c33`  
		Last Modified: Mon, 13 Oct 2025 22:32:11 GMT  
		Size: 292.2 KB (292225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff263799f1143509c900145c2d2e0e2d15f119c988846b71974d7007e44bc3d`  
		Last Modified: Mon, 13 Oct 2025 22:31:51 GMT  
		Size: 59.1 MB (59073009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2980cccdff0725e7155d37391f70d96c35641160d69e5c79c68c4daff4267a`  
		Last Modified: Mon, 13 Oct 2025 22:32:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ff173b88dee4da8f8d0f7405fc1d8899c0f2671315712fb726ac6b85cd6d866b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9c6cb12500494cbe6f13b5e2d3505d9a99740d4b6bb37fc5c3de715caa0f34`

```dockerfile
```

-	Layers:
	-	`sha256:90402cc72036592aa5eda71476fa1cee288d311c218276af100eb2caee4aafa5`  
		Last Modified: Mon, 13 Oct 2025 23:23:32 GMT  
		Size: 24.7 KB (24741 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:cac4b1fcfc422254c9c5736b3e09e55ddfd583010e65c836969ddcca138df0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62462870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9c617c9af95653103e4cfe02dd42e874c0894891d7aac4823309d3f7c642dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f51e2f38ac46b2e64c3106ef08e374570e2292a1981258b5bc0783df65ae63`  
		Last Modified: Mon, 13 Oct 2025 22:33:09 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af0985c887920d8ad25f36932e706271ae84032a3ae370b1f5325188b8578bd`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 59.1 MB (59072951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67f0a7f4b35706bc00619d60af8574620a8b9d365f18c7dea31908544b91c4c`  
		Last Modified: Mon, 13 Oct 2025 22:33:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6610c9f23ea01536f7dc4ac3c41b86e987ed6e53173b3d857f8f159b0acce93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf66b0e958cf9e7c02b349fb2aaa32a8a0485baa829f2009e63f460e7f94a5b`

```dockerfile
```

-	Layers:
	-	`sha256:3b015bd7b42e97eac849fd09fd244e78c4e2b88c5496b9c7a9cd4a499cd3b1e7`  
		Last Modified: Mon, 13 Oct 2025 23:23:34 GMT  
		Size: 193.6 KB (193587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d22532deaa901313db65bf772d5518c6b4fafcb7a20e7d1f23429b7a64062cc`  
		Last Modified: Mon, 13 Oct 2025 23:23:35 GMT  
		Size: 25.0 KB (24956 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7099651fe46416e57bd4eaf0b30ec285f8491e1d2a254135915d112dbf284e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61936711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ad3c6b16fceed3f4c8eec76ae7ee06fdba94e9d3c855720e8c50f69cad6351`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f36545d4b594b2d5b8fb8b64b12b160bf5effe94c4116d3b159ad99f4e58a2`  
		Last Modified: Mon, 13 Oct 2025 22:33:10 GMT  
		Size: 294.0 KB (294039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dab1238d3d9c3bd1753609badeac4c19b7239aef9927c6dc13db4335a66b568`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 57.7 MB (57650163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196fd7d83e7df170aefd9a76e75bc29338994ab26c18135fa914eb19fe49da26`  
		Last Modified: Mon, 13 Oct 2025 22:33:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7d562e444e84728410b6f9d77bd38b376e0bc2eae25bd15ba5b4105d403a0c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4e7b6e9558c29f27ffd24dac4c329ce570c14705d10150aaaf7f0205fe98da`

```dockerfile
```

-	Layers:
	-	`sha256:cd2dba5797d40a1b4951dd41b3906bd0fc5bfabe6993076e2771a7a6b04a24cd`  
		Last Modified: Mon, 13 Oct 2025 23:23:39 GMT  
		Size: 193.6 KB (193621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79680b8f08ec7f39aac2dd549c709ee168a5513ee636f89bba19f4f0f9e38848`  
		Last Modified: Mon, 13 Oct 2025 23:23:39 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:9fae6e65bffe8604509991c6f50b5696209bafe24d6124142ed0502dd533bee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62627354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a6a4c3030df8165f68a59daa64baa66378d59938bfa42fc7abd83390905435`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08ccf8c1f52d75316a563e011d61bbb1b7bee762def845c0a675d85ca00b65c`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 291.6 KB (291591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95a97777f39c24f1a92cb9717c8fb60aaa699bf624bf9ea8e2cf61d0d8d4abe`  
		Last Modified: Mon, 13 Oct 2025 22:32:51 GMT  
		Size: 58.9 MB (58870901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd670c92215b0b4a04c31e0cb6e46f1175a7abecdc58fd9a4f6e02b77c25d59`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ca9674013c9a5bcb9ea49f98ab4a3c3e42071d915f7d147dca61b513dfa605a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c1d6de4133fb5263ab53af0adeffb8b6dd1097fae19c0e667552754cd8188d`

```dockerfile
```

-	Layers:
	-	`sha256:f27b41bc8a24be97183674a65f75de9e84edc7b302a236c9b1884307febf1c29`  
		Last Modified: Mon, 13 Oct 2025 23:23:42 GMT  
		Size: 193.5 KB (193526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1d529df77080d6fd467f44cf49cbaca5d111031192da4a7d539f32c22c1622`  
		Last Modified: Mon, 13 Oct 2025 23:23:43 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:9986d3872f7f0b05394e5003916803087f2363ac4ea71303ac199948f55e11d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62003213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c302417cddeb16fdc79099e42abcef6a1de5d829935e5484646387ee1b1696c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73de5935c27bbf53bedf5cf444a1a2d137f0c9fa6be0ac31ba3a0af17a0953`  
		Last Modified: Thu, 09 Oct 2025 03:31:32 GMT  
		Size: 294.5 KB (294519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd79e032fd555b767c904ba3576a69bc211a15c564010ebf1a3788cd00df21d`  
		Last Modified: Mon, 13 Oct 2025 22:32:24 GMT  
		Size: 58.1 MB (58134461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6f29d43c2f44e8592e7c886427a1799a29d7367d7fbbee964cc37c159604a`  
		Last Modified: Mon, 13 Oct 2025 22:35:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0892c561eccdc1c4b607bc41047abbe176ebb4cdad9922d2f8d262ea059b6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb7ce577f037e833cf62c9af120601132865b7a0a586cd72671ab4f6e74d340`

```dockerfile
```

-	Layers:
	-	`sha256:76bc59ec2891cc289fd19497b0066905dbfa3be50a11dbaa62a17d42e7232e63`  
		Last Modified: Mon, 13 Oct 2025 23:23:47 GMT  
		Size: 191.7 KB (191662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775d1aa0b6ace870f9b4f3916ccc7adb926aaaaa783cee1467eeba05d1559147`  
		Last Modified: Mon, 13 Oct 2025 23:23:47 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:ff983454de20f72d5913b13627d071d5d34131e722484cfa5015851732d9d35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62312831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0dc6955fe35a0659bce04690be3bcccc8657fe7e92caf9231a3d7c25930e17`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d54fbaaf4f44943b5fd17aacabad20b0db0f29394c2b0f581a3a300b124c2`  
		Last Modified: Tue, 07 Oct 2025 19:40:12 GMT  
		Size: 58.7 MB (58670209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a68004e03ec64e8a886aabf35878ed99c7a2fa48abb0fc788f7f5fd439dc66`  
		Last Modified: Fri, 10 Oct 2025 21:07:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:86d79cd177e41ac1e20071c7e6bacf630a351fc2da45ebd90b46e4a4bd2043e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553eb9bfcae72d96fe2e9d7defefa7f4858c299ae7b2f5ef12d93c19bf3f6d3b`

```dockerfile
```

-	Layers:
	-	`sha256:2119a8b6ba09cc0605f06556060a207b9b0560adc04b3387afea1f4f120ef830`  
		Last Modified: Fri, 10 Oct 2025 23:22:43 GMT  
		Size: 191.7 KB (191658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89bdcfb3f60dd423709414bc51294a8cf3250b102ea237ed3cc7678b04815378`  
		Last Modified: Fri, 10 Oct 2025 23:22:44 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:7f32f3355f07d039f2291bf175153172aff0fd13c92d225cbd1ebba549c50467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63241801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83deb2e46083c09d50aaf1545f20d12ffbdc79e217246389a3ffba87b72e464e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 21:30:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc4c05838d57ecfe671b31e7400d015d24d81c7ce717be366103b575ebe388`  
		Last Modified: Thu, 09 Oct 2025 07:53:30 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cce485d826b4034b25b00ba2ffd0ae02402af07840c83aa561b76bede0f4bb`  
		Last Modified: Mon, 13 Oct 2025 23:28:51 GMT  
		Size: 59.5 MB (59483110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f9c56fa8a5be95fb4180d4d903bd51154a775bfb4f628eb4a9f84ed52cebf1`  
		Last Modified: Mon, 13 Oct 2025 22:34:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a3a78613ab6413905384cb1cfcf072ccd1be35a81498266706b62fef1ae595ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5360667534ee3acb88af0736a8f373820fba218bc499abaa67ecd30128ad61`

```dockerfile
```

-	Layers:
	-	`sha256:1ed3f3c01d70b5593c32d0a1337200fca49857440d1216317714e85dc566330f`  
		Last Modified: Mon, 13 Oct 2025 23:23:52 GMT  
		Size: 191.6 KB (191614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549015d70cb942670570f93870f0ee1f6057afd58d8af331c40f80fe524b3696`  
		Last Modified: Mon, 13 Oct 2025 23:23:53 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
