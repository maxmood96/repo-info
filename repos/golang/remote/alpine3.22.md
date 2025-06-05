## `golang:alpine3.22`

```console
$ docker pull golang@sha256:68932fa6d4d4059845c8f40ad7e654e626f3ebd3706eef7846f319293ab5cb7a
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

### `golang:alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:e5c2e59960f8636d02f77029c8f0a7a6b882f87fee8d2e4a9ce6c9ff112ed735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83073729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9499354a10c9543db22a053a763cf15e367a858e28e4d5e7748d6f9a9e7586`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3484c2589c81b25b672e9224c8f150a7f93b5eebda948cdddf2a917ca4f826ad`  
		Last Modified: Thu, 05 Jun 2025 19:27:46 GMT  
		Size: 294.9 KB (294914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d891a8207b1f09d068f1f787a771d851e423291ebea483283c95905fbabd385f`  
		Last Modified: Thu, 05 Jun 2025 19:27:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ec565d9f5329f31067b313054856e441192acd603d9c577162ff99d7e7e1e96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 KB (239917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b79bd6eca2bbfc43b500f2f14f3f5196a31d9cdd4ee72c2253dee5550d016`

```dockerfile
```

-	Layers:
	-	`sha256:6dfda6d6d02e8fcc465d7c78999643e49f9889e8c1c22a7b5d058c0bf2a79a54`  
		Last Modified: Thu, 05 Jun 2025 20:23:07 GMT  
		Size: 213.8 KB (213847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e32ba6a1f4315ca412c21524135007f31d72058190099b3d9acd5f03a5ce654`  
		Last Modified: Thu, 05 Jun 2025 20:23:07 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:937665b6ce2e341f0e9952c899c464c4180a53d279d5cc657c44eebafdef6ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80941899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434fa517c013e1d325bbcf7f839f00827bb896190476c3660816c53870d23997`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e48d0e320da61613760ea734e8d4a99f5bd56ccace78ca0d349d7789a1e4e6`  
		Last Modified: Thu, 05 Jun 2025 19:27:53 GMT  
		Size: 77.1 MB (77144520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5598939ab7df010a7c898c4ccd7b1d8086f513252480c77b782a6e04da8c5f`  
		Last Modified: Thu, 05 Jun 2025 19:27:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:acdc7ef245a9e07d6ae10dad4cca4c1da6289e67c7a415d2879ff5ecf698617d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d30cb521eb594ea7c1af3f45b26ceda2a1bcd60b69b128b1f4cddd5b8b3f156`

```dockerfile
```

-	Layers:
	-	`sha256:c1e5dd1ec596b0c8220c901c23b9089f68e3fc07b8091e0b4f530b7889ad8c4b`  
		Last Modified: Thu, 05 Jun 2025 20:23:11 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:5f4319d8fcd7a1499a413b059fb99a5604e43867d7ec12fbc054e505ef1b9d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80658872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e068d86843e74c8fba71bdbd187500f096735b086e5b49bcee23956ec03d519`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf2c10def2d8cf5d99028e57ec326191a0a047212168dca4acb19eaa1e55ca5`  
		Last Modified: Thu, 05 Jun 2025 19:29:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:925a140a5c37e9745319dbc23c80a66a5401ac0620d940fc8083f08e2a610c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 KB (240082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7f7c2663859786bf329a252e1ecf2861ddcad6f4a48d061c1ea7f6592c49fd`

```dockerfile
```

-	Layers:
	-	`sha256:95da069279f5278b96fc96127bd38f0952edafd2a09f741a075c655b5999596d`  
		Last Modified: Thu, 05 Jun 2025 20:23:15 GMT  
		Size: 213.9 KB (213879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de94a4ece41abbc045644cfa78d6831e56b8645bd479eb7bd3f5aff6a461ee49`  
		Last Modified: Thu, 05 Jun 2025 20:23:16 GMT  
		Size: 26.2 KB (26203 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:25f0ae8a9452540a6ffa309395ca983e199b28dae84e9611c99a7587cff38e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79665527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4de6a23abd102004c28f38ecce79dc74a8cc936ea4b787fe1121fba06cc96d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373964117ef6ddcc9d2295f836a878c54d49d139d1981ffedc92cef7282b2a9c`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 297.9 KB (297885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e428c61e03bf0c00f4b4851c31434af33ee7197eea1fff28a221b3e6066ebb`  
		Last Modified: Thu, 05 Jun 2025 19:28:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:c284a5e9fa31d1d74c5ed65bd22714356e4ba6c54c8cbf4b43169e6f7a838d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 KB (240203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d323306b02fea436183a3bc4cb86f70180809641bb8d1c7de840af023792f791`

```dockerfile
```

-	Layers:
	-	`sha256:954eca3d388f47e0bf923b73737f7d0717a0c897db68985ebbe7c49917b0ca42`  
		Last Modified: Thu, 05 Jun 2025 20:23:20 GMT  
		Size: 214.0 KB (213951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d43d00d390713825fcd05279608cc4284887eec4081f546c2fe5f3dbba9aabe`  
		Last Modified: Thu, 05 Jun 2025 20:23:20 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:300d6b8226d8b1f958309b2019418388e43eaf5e38d28ad149d6fef38bfd2941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80812380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335b5c5d81e2ba341666e861f508201059a462d4600f8e731897d114234f106c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070b52c673e5f90ba0a0d8a7a02d0e1203fcd98bf5226d76f032fd0e81c07333`  
		Last Modified: Thu, 05 Jun 2025 19:35:34 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2648cdaf06d027d18fe851d06ee03a45b577e7feb671f0e099ea38bb7d48722e`  
		Last Modified: Thu, 05 Jun 2025 19:35:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6f6f7f15da15d6b3714ff9749be024d3b47f29193b30d2ee66ca792de6813963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 KB (239780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcb7f4212763f21be267c3ea2ee03654d9a557367a961948af672816a47d195`

```dockerfile
```

-	Layers:
	-	`sha256:f3202626bfe1ba74a895223d54fc69e63c1954bfb6d668ce6e8de0785c3c7ff9`  
		Last Modified: Thu, 05 Jun 2025 20:23:24 GMT  
		Size: 213.8 KB (213766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e3e95d679407660d6653bb69353ecfe16391fda5d5fe2c626611ab0215bf84`  
		Last Modified: Thu, 05 Jun 2025 20:23:24 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:afd072e5e2f2cdc55d1a95f0a14b6ee273a30f262e3dffcd722c34551e1f4eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79576254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604cf7ef7548a152649c1c291e1a53385d8b59e2530297672b47c8e90fb3038c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857e797654b7f586891362befa86842c081cc043ee887ea9708f0fb0ac7c27f`  
		Last Modified: Thu, 05 Jun 2025 19:28:59 GMT  
		Size: 75.5 MB (75547589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e21a72bd6353d3d8d0ebd54b0aaf14f3d84194978a75ad9f5322d72d938971d`  
		Last Modified: Thu, 05 Jun 2025 19:29:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:166980b12ec844f419d1c5117d1e3f3f0f149095f17f647833b79ff62692734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 KB (238132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fd197ed60faf4fcf2e17aabed3c6b1d9990cde7e7669a71c5e4a9a6ad72b3c`

```dockerfile
```

-	Layers:
	-	`sha256:4679c16953f16a30d708177082f49f3ed205653a709f14865faf0a5990e4aeb6`  
		Last Modified: Thu, 05 Jun 2025 20:23:28 GMT  
		Size: 212.0 KB (211990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fc04ac558bf6fd7bc3d023d4a2ae5d789603abb2403629ebb57e79422f8a6d`  
		Last Modified: Thu, 05 Jun 2025 20:23:29 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:f72e2037f9cb7cfbba96a097151421b59a57c425fe91b5480d5b26e8c20a6871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80125275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411c29a2f33dda13beb3e25a7ac74de2285bfc0396b951256fec66dce266538f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2ecc1bdf9f9ef88fe34606e57a3851823b4754890f687d2189699df698a0ab`  
		Last Modified: Thu, 05 Jun 2025 20:28:11 GMT  
		Size: 76.3 MB (76315916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647670c8a6b5f33eac2a59a96e098d70e0ea937a29bfa013f8d0b48c7ab0be0`  
		Last Modified: Thu, 05 Jun 2025 19:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4057c4c8a537bc727045df4e05651b3e3ef51295faf97c52a00e59ea2c508cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 KB (238126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d20d3a71a20ee02edac17fac27406dbff0233f478de79c5f0c4c89119f448`

```dockerfile
```

-	Layers:
	-	`sha256:a6490053f31c987728cf03b9464fe148d0d3226861adcfdea60be9607a49eb95`  
		Last Modified: Thu, 05 Jun 2025 20:23:33 GMT  
		Size: 212.0 KB (211986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc27a5391e92cc868e48b22c007edce28e2b3e5158282d5b4bcc309abff8856`  
		Last Modified: Thu, 05 Jun 2025 20:23:34 GMT  
		Size: 26.1 KB (26140 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:9aeae57f7ee53bc4efb95e0a7bda2deb08a08a4f0db06508440598ba14bd1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81731971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e3d567a2064df4bbba1ff1dccd9de8cd8d846a29174e25e83971afd06af966`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 18:53:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Tue, 03 Jun 2025 13:31:49 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14182d78ce72a37aa9fbd4fe4a033502956e576c76e8aecb7ce69961caf57f90`  
		Last Modified: Thu, 05 Jun 2025 19:28:45 GMT  
		Size: 77.8 MB (77788070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550aca782ad6e31be5a8e0b5eb38db79e829507e0182dcc50d5a64d520f40826`  
		Last Modified: Thu, 05 Jun 2025 19:29:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8959cc2ca91f098df254c397eb0f3004de124a321bcd7374c6a09376fb08a2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 KB (237966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b24b8b7e80449f71d5e15541039ea4f80599bdd77219372f34cbded1493fd0`

```dockerfile
```

-	Layers:
	-	`sha256:628bdf9f35bae59b49e2535e6a5d6194247b53e9a0d1bbdc29828ea4b616b1eb`  
		Last Modified: Thu, 05 Jun 2025 20:23:37 GMT  
		Size: 211.9 KB (211896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649e73b8578174133d4f0fd77c3dfab978222dff965b987bf76c2ceb82d0a0bc`  
		Last Modified: Thu, 05 Jun 2025 20:23:38 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
