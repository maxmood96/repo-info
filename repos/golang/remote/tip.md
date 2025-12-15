## `golang:tip`

```console
$ docker pull golang@sha256:ed018a40fd7dccf489bdce84a06cbfc338814ea884e8be89924041552bce562c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:b89a43385a16d918dcc63abef0094b8e60bf076ae0754c5e56b1e74e8c356dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339177920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451b9c2c7516f7634227118d907a5758844bc476894a7b3beda6865bd70e6dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:28:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:29:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:29:46 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:29:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:29:46 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:29:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:29:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d5c94dd194f82bda70a7d67eb774ff8206d42ffee731ce6939c4115e156da8`  
		Last Modified: Tue, 09 Dec 2025 01:30:31 GMT  
		Size: 102.1 MB (102108744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949364a36b81a9ad117004649aaa40ca173e0cb5059f62e3ed14f9d09d82b4b7`  
		Last Modified: Mon, 08 Dec 2025 20:07:50 GMT  
		Size: 94.4 MB (94386989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831d9794b26033c3a1f88a658e9f87f9fcd31337bc724eff6b62a5d7302e7022`  
		Last Modified: Tue, 09 Dec 2025 01:30:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0676961a8a5ae3a1759d835f7f1ac8f8151844ab33c0b17f741dc6d07f444141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe74e44ac67ff02b30f5a5ee0210ad139f291045f37e2b7a057ff173d2ed3d7`

```dockerfile
```

-	Layers:
	-	`sha256:feb4f18a98d650ec33772f05de86b400a5a63733d8ac83ae537984dcc4d0ba30`  
		Last Modified: Tue, 09 Dec 2025 03:25:27 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:010364d2a81b4d816e31d211da16bac836d7aa1592f15df82bfeb210f7934027`  
		Last Modified: Tue, 09 Dec 2025 03:25:28 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:3df4c266566bed0aeca59f37b951da238c6a3cecc4ff50baf9825ee32f86ce0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295257494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997c9d63ff2f56ce96447d80abe8c3cd122438027560802f562e976cb3419a0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 03:26:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 03:26:31 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 03:26:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:26:31 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 03:26:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 03:26:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66d15d11ddc46d002295b2c9a7f478cb3a58caad88c0bdde8a6c29dcd998542`  
		Last Modified: Tue, 09 Dec 2025 03:27:14 GMT  
		Size: 72.8 MB (72754196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa0b6c68e96e333f64da015866d36d22ecf4302421d4e561b2c28faa5b8bbd`  
		Last Modified: Mon, 08 Dec 2025 20:20:43 GMT  
		Size: 90.5 MB (90451274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2b82f489002b504e0d240f76098e11bbe30da85a1934690bea8f22c27959c`  
		Last Modified: Tue, 09 Dec 2025 03:27:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4dbc84c8ec2e88441d4149182d6176183835ccfde87ae6a62bad701b99fcde2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bade469372fe4b159e9d1043802205dc0ada770780ce2b5ce4de55b881cbd357`

```dockerfile
```

-	Layers:
	-	`sha256:8801549e2121fee99df9e0da75c9fd4bc2e42202479658c4aa905004a320bc83`  
		Last Modified: Tue, 09 Dec 2025 06:23:30 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2a6c3f4a5a2f0b4fac3e2ebfdbfdae5ff5000ec5421318bf6c1154bda40b4c`  
		Last Modified: Tue, 09 Dec 2025 06:24:59 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:37ca9e1e01b68fc07d035fb5fab0f860ca7b7e5d3745f27b9480bc9b9c203ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329965758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8484c2b310944370b976a04521ec999820efca8449152159c27f9faff92084b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:17:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:16:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:16:37 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:16:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:16:37 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:19:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:19:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e70492a07fb4fbf4dc1bcdfa473e728066d073b26f641582ec1aeed87741aeb`  
		Last Modified: Tue, 09 Dec 2025 02:19:57 GMT  
		Size: 98.3 MB (98254414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2568df0f74d7435ccc404d81d30d0f293c9c2980ac0f029d1100be5d1622d029`  
		Last Modified: Mon, 08 Dec 2025 20:09:47 GMT  
		Size: 89.5 MB (89455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acd1f90779ed2cdc75315fe49814313ecba4918c412feccbc7b99ae912469bf`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:47fec42e130c6386ccdadc572ec28ba1a4313c354e48a34929fd1376e92c2adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5264f41d2389f7d43aa5720db175a5f3fb8738fa841e928a9e4c7e2d667b13`

```dockerfile
```

-	Layers:
	-	`sha256:1a4ead5d599e86da14a0ce14d402e66ecb5515427495df1ae30e239beb057ec6`  
		Last Modified: Tue, 09 Dec 2025 03:25:40 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2c0e8c3e5493ca116246289079f059aa82b6194491662daeaea6969b21a70`  
		Last Modified: Tue, 09 Dec 2025 03:25:40 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:f8772e54f1eb19bd9fb0bfe3c1f58ffdffd693379887bf27a152b3e75f7bac14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340205620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9513ac53ba334279cf9d3b39cae5b6114b96e567a041b9fb63d6cb743e481551`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:16:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:18:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:18:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:18:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:18:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:18:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:18:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d1731e98c6e5aff4c28a002263af9a4fc5c06d23cbc860d258dafbd603ef2`  
		Last Modified: Tue, 09 Dec 2025 00:24:53 GMT  
		Size: 69.8 MB (69794656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649148f62cbeb2ca6e60acbac9ec1b099d4a2584af0b0c9a189940b091c7bff2`  
		Last Modified: Tue, 09 Dec 2025 02:18:51 GMT  
		Size: 100.6 MB (100555337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714e644cc32cbf0646554d2bf879368eb0872b6982a8a69088b6c556adfd2f1`  
		Last Modified: Mon, 08 Dec 2025 20:08:50 GMT  
		Size: 92.3 MB (92277519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda41c882a5564542827f25295b9159fe0c6e7c9db83220ea72626f1f02bc648`  
		Last Modified: Tue, 09 Dec 2025 02:18:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:244e8ee7a5d4cc28786e475138b97967e8e2ed7c77316b4b4ad6249fdc4c9c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e84a76ddfd64980a4f15b37ad21a26d247bb61b31758981fadbff2af3ead9b`

```dockerfile
```

-	Layers:
	-	`sha256:d5b888c08a9f1cc855e50e54c7a27134273c74aaa02affd993f6dd6c33b78bb3`  
		Last Modified: Tue, 09 Dec 2025 03:25:47 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e022c300f74383e26b7e11efe2711eaa60e371e6819078858266697c39ce67e5`  
		Last Modified: Tue, 09 Dec 2025 03:25:48 GMT  
		Size: 28.9 KB (28925 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:c390bcb2d225d9b6c65499dc3903a5701cf18ce71c1090b6832821fa88ed72b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336939600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca4afb7ab58fd2ab5dcb1c928acd07abfe53f438a055667c069ae0000433c2e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 06:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:23:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:23:03 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 10:39:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 10:39:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62094cf6808b342239ceac9c58c9096b769bf275793baaa6699740b93ef88f7b`  
		Last Modified: Tue, 09 Dec 2025 06:22:27 GMT  
		Size: 92.8 MB (92815776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f78d7b3fff51dbf03b6fcb119f6f6c12d036239dbfd1e84cb159ba6461fe1`  
		Last Modified: Mon, 08 Dec 2025 20:25:32 GMT  
		Size: 91.0 MB (90996328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c0d81e52f9f643cc36452bcff401aa77639ec30f5172fde0fa94e9913baa2f`  
		Last Modified: Tue, 09 Dec 2025 10:40:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c79a175948185a6136c51b02937250e48504f1ddd3dd80da20d54113c468679c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860d9dc24a321283ce8b7c456b70d9ed0ec0ed9aeaa592f3a261579c88925224`

```dockerfile
```

-	Layers:
	-	`sha256:f75c107832b210d8c08638fa215f14cd432f1c3972686576409b3356ae7e57ab`  
		Last Modified: Tue, 09 Dec 2025 12:23:39 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735417e9be18528702446f4b6e172c987ce64ecbe7f4e4f9fce6e7b340b8b1c6`  
		Last Modified: Tue, 09 Dec 2025 12:23:40 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:ae3e3fd5785413bf99d1ad8b2f395cd4f2ef9ba6745938c6f3798af249ef6397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362622489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeccb940274b5f362495172040eea419aa958eef461ffc055ae098c79c7f187`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 07:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 21:37:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:37:12 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 08:47:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 08:47:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4af291d8cbdff6d28ddd144cb820c9d50e09d2eefe7cf2deb9f3384fddd0193`  
		Last Modified: Mon, 15 Dec 2025 07:10:40 GMT  
		Size: 131.6 MB (131594746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305a0d5488487114fae9eff5e7d2b05535888e36450abce33d63c253df6ef6b0`  
		Last Modified: Mon, 08 Dec 2025 21:44:31 GMT  
		Size: 91.6 MB (91642118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ebba4711edf4cf34d59677da175c4666de0f41be0cf6a27ceb4a3d5d5c2dde`  
		Last Modified: Mon, 15 Dec 2025 08:52:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f8510e825cfc75a16827f66614bd325f1c3c88b18fd18548450dfd47839ad76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c6758784be05d258400eb01fe40db647b8432d99fbb457753b975632d2cb41`

```dockerfile
```

-	Layers:
	-	`sha256:225715811d96929c75225e03386dcc6a6a3ca228501f74ef03b80c895f923190`  
		Last Modified: Mon, 15 Dec 2025 09:24:19 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa0dafa5238ab7a2b8acf9bafb8186e5a97c4262b04ff0d22734f0ae9600f70`  
		Last Modified: Mon, 15 Dec 2025 09:24:18 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:8ae050a35f7021fc08791b5d9b99a8dfdbc5cea7f8cb04c4e274a3454f10e043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314229508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfaa6d819fac12ab1e654016e221ee8066bae1b6e161b40b2b0b44a7ab19237`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:10:22 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:10:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:22 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 04:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 04:53:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2be274f95003449a8278cbc7ab315c7bcb675710ce099ea39eaa8742edd0f0`  
		Last Modified: Tue, 09 Dec 2025 03:00:19 GMT  
		Size: 75.9 MB (75919454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d45aee96e59637b1f14b3eb6f81f4f4c64edb3653263ca9a0c489bd88115cb`  
		Last Modified: Mon, 08 Dec 2025 20:11:07 GMT  
		Size: 93.6 MB (93553127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176d32c812f573825f8b2b2e54d4692a8b85184e2bd965510f17fc60ecbc180b`  
		Last Modified: Tue, 09 Dec 2025 04:54:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:224eab314dd91cb39ab1a937fb87a95e10e0cc1a3b823ea8763df08a7089d19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff3e8fd56dbee9babf48b40c690e5038c4b18200834ab9806cca8d06e966090`

```dockerfile
```

-	Layers:
	-	`sha256:d7deea3e5f7ff927da2067dc0ab4fe0b0046a0604c7dc88b771caf2f8dac9509`  
		Last Modified: Tue, 09 Dec 2025 06:25:30 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c160792638a28f438da6518bd12244dfadd515a605af5c549a0c76358b9b3d57`  
		Last Modified: Tue, 09 Dec 2025 06:25:31 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
