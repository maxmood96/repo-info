## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:7c8e975c046cd66ab4180a81db53198726bd29a35e6799d8aa8b229d1baa7c72
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:7a744e35aa17792d292692a0f8356d9deff7f1bad13431be0268cf478b3ed6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87605317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a53e29125d7f1fa909d95553eaafbf8b7f23bb38e47fd4928f8b26040956758`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883912046db21eccb015aa7350ed568d3ad17864ae70b619674d0d5c816e05ee`  
		Last Modified: Mon, 15 Sep 2025 21:12:40 GMT  
		Size: 282.4 KB (282419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8084ae79718311fedfafbc5a50335db8ff6184359260f7408a58117f5eecec`  
		Last Modified: Mon, 15 Sep 2025 21:12:40 GMT  
		Size: 83.7 MB (83685170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867ebc599482c1fa843505af4f10b0bdd6314a1460f87266e66662e99a3f7413`  
		Last Modified: Mon, 15 Sep 2025 21:12:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8a3a062a7cf2ebaa4da9ccfce5bc0590aec5beb4a9ce02a3eef4d2c659afe5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fdb034ae2ccf7dd2fd9fa13b47c3ea411ff3840b444c6b8415c89f518e98eb`

```dockerfile
```

-	Layers:
	-	`sha256:8484729953cd6f575fca2f72cbbcc6641f4fdfa960775981a4387f4030197d83`  
		Last Modified: Mon, 15 Sep 2025 23:24:18 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ebd49d0b7eaee75f85fa375048674031d8586d3d5577a36e8476647bbb999a8`  
		Last Modified: Mon, 15 Sep 2025 23:24:19 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:f17c866c4b3518dfb35cf640842ae612cfc8e1bea15191ae61f288ee5ad4f886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84722892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424b2a62710336f27e16e5e25809dd8ac6eaedf448c9cef930b771059f01f58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f5b879ef640d8b19652062ae76608a00f57dba5b1aeeb54541fecd88fced88`  
		Last Modified: Mon, 22 Sep 2025 22:15:56 GMT  
		Size: 283.3 KB (283285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667cfeddc27e53555bca4026de0a43b07fc7f2fea60a4d56cdbfb0279068e3f4`  
		Last Modified: Mon, 22 Sep 2025 22:16:12 GMT  
		Size: 81.1 MB (81075635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de985230079be7681677009b5bc920a9132179fa8874dbb9dd568f835f52d78e`  
		Last Modified: Mon, 22 Sep 2025 22:15:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8a8728d5e5ebf0defc7e1fe49f0151ddf788c44896abdb8167556de22c516578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2225e14c4f11e1a0c9a90ac8abc5b1eec3ebacb6158eb59ae3528ef2175514b0`

```dockerfile
```

-	Layers:
	-	`sha256:09d2295ef237d17a807f5237ddbac1195083c1661d2e0b9759336e79001155dc`  
		Last Modified: Mon, 22 Sep 2025 23:24:10 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:49e7be621c17977c46b3d831517364425a1b8991e20f9f71398e5fa1e6a15276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84234313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ef462964ad85443a2fb038cbc4ea685f5a643caa8c5b7a6a2ba0008fc75c3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370439985b75687abc6ff25902abd20d23b2e00fcf28bea7c3aaec906bc6deee`  
		Last Modified: Mon, 22 Sep 2025 23:09:45 GMT  
		Size: 282.5 KB (282472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b53903587a634418235ca9a2a24afbf265d09dc392f55b668e6b9d3c5f19d2`  
		Last Modified: Mon, 22 Sep 2025 22:17:28 GMT  
		Size: 80.9 MB (80854813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290c7c441531eea3e9dc2c6a90c17e213158b188b4dfb2e3b061d834bb880fb1`  
		Last Modified: Mon, 22 Sep 2025 23:09:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:5006ddf2ee59c93c7b2fed7a9e550e05a0d388902a56344c49aae5371ae33178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148706337a05b061893a06366026991e21ecd44f5a1297ed8984a7805fb78637`

```dockerfile
```

-	Layers:
	-	`sha256:1e2de538e7bffc8d4c2ed48d70f9bf5441717cf25fd4b2b4c736bbf7e780377f`  
		Last Modified: Mon, 22 Sep 2025 23:24:13 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2068a3a2c268aba445a9a9c13fc9e767b6158ad35e65c6386a64e697d43e0f0`  
		Last Modified: Mon, 22 Sep 2025 23:24:13 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e4413666373addde0d7b1c0634596c11521db1d323d52eb66e5baf7db89e41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84039054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d55420feed47bb1eac2964afac39d92c88332993ec382e8bd90ce8978eaff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81a24a53636aa97473008c3b32b580ede0567e93a5b1e7996ee31f8af8e8e6b`  
		Last Modified: Mon, 22 Sep 2025 22:15:53 GMT  
		Size: 284.7 KB (284685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3b299721a40c4d6ce1f1cb5eea411e8ebfdde21f8badd13b95f602420e920d`  
		Last Modified: Mon, 22 Sep 2025 22:16:02 GMT  
		Size: 79.8 MB (79767276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1409f64f0b66479b55066d46142c19c7b066411fa00f45950783096cb3e95e`  
		Last Modified: Mon, 22 Sep 2025 22:15:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:87145de97c5f3ceedc4c22a48a11d59ece08c29abe8b26a321e12f9cb7ec14d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e8bca97d9f4200c60558b3a4361fb2b5b6af7fd98800e8253e9bf1390f6c60`

```dockerfile
```

-	Layers:
	-	`sha256:66d9806d201fc981d82e9eb27fffdbbed3b73e494d809d1d184123d317584eff`  
		Last Modified: Mon, 22 Sep 2025 23:24:41 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efa4964e076f7012d29cfc1ad901ddbda4169059e0142fb5d16f64586141142`  
		Last Modified: Mon, 22 Sep 2025 23:24:42 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:a34ec382af36163f6ff8c322c98d5a4a7d275f6a7399bd48833aaf4e05f339f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f868ca2918633ba626024b24f44839433b90c4a194475fce7c6b66cc2f255127`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55b358246ef46c70a5a8cc56f2a313ba78f5e2b5771acf4b8b3d71a6938f914`  
		Last Modified: Mon, 22 Sep 2025 22:14:26 GMT  
		Size: 282.9 KB (282884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3896767490999bcc9dd9f56984e3a495c1802d5f9283b126ed682e5e7c6e34ea`  
		Last Modified: Mon, 22 Sep 2025 22:14:34 GMT  
		Size: 82.5 MB (82473451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b61c0a95fb280ce875c2cf25297adaaa4ff697d11c727300add1e56e9fbfe`  
		Last Modified: Mon, 22 Sep 2025 22:14:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:626b83a28e8817d2fa854dff77f3d4d0b516ed65f37e1f740320dd90e5a028b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e805dc91be9b9a00b87b964fbf617f348557414a47039afedc84fec2b31876c`

```dockerfile
```

-	Layers:
	-	`sha256:39026b6b8c6535db624773c1e0be4e876637f251f2ca8767f2968c033fc255b8`  
		Last Modified: Mon, 22 Sep 2025 23:24:45 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be84f2bc88b93c3d57526c9cc2ef498a33c0abe144e58a43b4912565b6931d4`  
		Last Modified: Mon, 22 Sep 2025 23:24:46 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:c3febe5fbbcbde4c1da8d2e84873aec6aa2a68e0ff1257bb8e5f347df60aba7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85010224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8604e985d1fd41e369260bed5fb60a9c0dc4b2d7a2ebc6df33b0eef3ce603c2d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05343cbd8895ac16fca565a0ad3f2f6a0dc20e79a602738d4d6b870a682cd2cb`  
		Last Modified: Tue, 02 Sep 2025 17:40:55 GMT  
		Size: 285.1 KB (285075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde134c38211f8221348f6d1f1e1ad94732dd62caecb5c0a2623dc2674afdd`  
		Last Modified: Mon, 22 Sep 2025 22:19:09 GMT  
		Size: 81.2 MB (81155866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d7833ed145899817abbb54cbd02e41ed220da725bcee607ee7a6a32e15319a`  
		Last Modified: Mon, 22 Sep 2025 22:31:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:7ac6f0908a4818f73c1c32f8dae2c116efdc3ef5b3a0f85c19609cebab6781e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68897eadf03eb1d10e6c69b6ffeb4a4712dffea2d6d26955840f66150d7d53cd`

```dockerfile
```

-	Layers:
	-	`sha256:9bf783c0105343c9614edc1a85dd6fac618b6793638a247aae5f6c08be3478f5`  
		Last Modified: Mon, 22 Sep 2025 23:24:49 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da88666423f249f9a615643a3b38ed1882409de0e9204ceab0ed160c8b2450e`  
		Last Modified: Mon, 22 Sep 2025 23:24:50 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:2bf3f60c4efc6fe9b96dc2ed1379a1fe69c4dcd890a7292de8098ae981043e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84977205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3dd37c30d9452e897d1ab54ac60b3da8baee572c11a5d34ca7e50ab1c7ad91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8d07cad9e20eb82eca55470c44bb00c784ba041cde1a36f0b2f92a234216b9`  
		Last Modified: Tue, 16 Sep 2025 20:34:48 GMT  
		Size: 81.3 MB (81345205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f7d61b936abed383155351c8619cfed324028e24ce10b5ae40bdaeb765a39`  
		Last Modified: Tue, 16 Sep 2025 21:43:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:53543fcf2e125f6b7c8cf0f78ab1b05b90eea4092200e26cef1f1a4953e1adbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b7c92a9589c4147409f20c270aa6c3534b2da619c9ef88748cbe8e44525725`

```dockerfile
```

-	Layers:
	-	`sha256:4016cb1d55c15c433b107f73a092e41ed2ec7c387222a84e21b89d01d5f69582`  
		Last Modified: Tue, 16 Sep 2025 23:23:41 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c22c60ee13885f02afe8e2a56289f93c665e33d120632ebadbed64bee96251`  
		Last Modified: Tue, 16 Sep 2025 23:23:42 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:63c51c2506275f365d644433ef68075f88e9ba6b1ea11b713105f0dc34c231e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86123904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85ca716116ecc4e3a1ba68c377114ecdcbc11709a721c408f2c14d0b0a2a45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baeff4e12a448b03c9a0556e687e666d81fee45be531e32b6b5f75090e58bce`  
		Last Modified: Wed, 03 Sep 2025 20:25:47 GMT  
		Size: 283.4 KB (283440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378803bc6cc1e0c01f411ee825bdc456b59e4a7d5184c546614a84a4ce15dd67`  
		Last Modified: Mon, 22 Sep 2025 22:15:10 GMT  
		Size: 82.4 MB (82378206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a048925bf0ce3fb4baa6bf26dcaf7036ce9027fca53d89595738d6e6a6a6e4`  
		Last Modified: Mon, 22 Sep 2025 22:25:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:16e1e8dfda9af68119dc14e63a192de27283283ef4d47357a0da640cab6a5d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3125963e81057e55e67a91a4e7f28520c5352cb6d68b353c84db9e989b347e`

```dockerfile
```

-	Layers:
	-	`sha256:22a015ba044c8479798e9dfa69763c3cef4d2db451e4cc92f5cd2b9e5a262e21`  
		Last Modified: Mon, 22 Sep 2025 23:24:53 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723bb77591324d251185d6c7a1622aef871572b68391726ad5e15b2dfb4a93fa`  
		Last Modified: Mon, 22 Sep 2025 23:24:54 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
