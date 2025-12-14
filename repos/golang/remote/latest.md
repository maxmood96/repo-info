## `golang:latest`

```console
$ docker pull golang@sha256:a22b2e6c5e753345b9759fba9e5c1731ebe28af506745e98f406cc85d50c828e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:828328b1b4b24d4ed279e22e8585f6f4f54af62404d484a0e71eadeb2c18efd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304942067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f02847b4be43a1c4901d0f1457f5685e24e2357ed7787bb2f4e589d7bb1c01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 00:46:16 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 00:46:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:46:16 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 00:46:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 00:46:20 GMT
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
	-	`sha256:dfe0f9d3557d0d7bae81e9248d9b3dbcf4bea111897f7b681ad95869d3931e3b`  
		Last Modified: Tue, 09 Dec 2025 00:47:04 GMT  
		Size: 102.1 MB (102108565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a77c8f945b182238059746e5d5e82689a78d8c65fdf751d1d0e659935b04c1`  
		Last Modified: Tue, 09 Dec 2025 00:46:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:f63cd56f0ed4dfe07233903c505e6d8ebb0f278c3ce29734ccc8a351bca76115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4bf089873ff1855462f19dfd56be13ee650d06c8729d85cfb98012d80795b2`

```dockerfile
```

-	Layers:
	-	`sha256:83f8a6843b683d5fcccc85a4b22b795051917b6a549339130a6d1bcee6a5fc28`  
		Last Modified: Tue, 09 Dec 2025 03:23:03 GMT  
		Size: 10.8 MB (10784428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2506c7fb833b96c0bb1240d559ce63a3641897ed6b41258cc3f1bd9f449c272`  
		Last Modified: Tue, 09 Dec 2025 03:23:02 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:2f81eb3d3b9ddfb694cd597250a2d23515607e9426084629cb7d816f63122e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263878124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bb69337a0a782137b562fbd75f2bc5753faef6e7fbca7882f014f43db67fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:18:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:19:49 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:19:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:19:49 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:19:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:19:49 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:19:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:19:51 GMT
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
	-	`sha256:a0f8625dd5fb958f8d1fffc03a2fdf6e9d20fe660ea12f5d13444575e323bf56`  
		Last Modified: Tue, 09 Dec 2025 02:20:28 GMT  
		Size: 72.8 MB (72754037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9948efd9c729fd84124e6c81d7bf0a94250e8bd9568e31bcd3d9b558d3a1f6e`  
		Last Modified: Tue, 09 Dec 2025 02:20:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:c6a8536bcfa6386ec71a705246c88485b05fa97162cdf7c5cfd30529f6e01d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b07062b3891f71340b0e63132640fcec5e5581d0d73d15818573dcb08be04a`

```dockerfile
```

-	Layers:
	-	`sha256:76710b507c221fac012c71b5e6a50253d2770d857430146e2c7c9d344abbc53a`  
		Last Modified: Tue, 09 Dec 2025 03:23:10 GMT  
		Size: 10.6 MB (10580349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7af0bedde07bd8ff11a5e2f4a8ce81911bd320428edd89748cce2f235ff4005`  
		Last Modified: Tue, 09 Dec 2025 03:23:11 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9260375c5c24a4a33a14c8d8a8a0269874c7476399e233f7fc8025b3257c41e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298161834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e455f98fdd4bd5992e554a08d6d6bc4db8556ca45e037dda19ef50477d85b55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:16:03 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 01:16:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:16:03 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:16:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:16:03 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:16:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:16:11 GMT
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
	-	`sha256:5d8f80478dcdbc8299326198864f22f7c6c95c5f08fa05336d6f0ebe69a5fedb`  
		Last Modified: Tue, 09 Dec 2025 01:16:55 GMT  
		Size: 98.3 MB (98254578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db9d549d16dae22ae4a7c277a4217d8db4b173c6345ccd670f74b5670730778`  
		Last Modified: Tue, 09 Dec 2025 01:16:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e1a5350910efd8ee63c6d9b185c770cc448281cfe5b9e5e026b52a6d3015bb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3817472ce62bc42d7da4714126376c48bde891ca6ed6f192ba46cbb9d49125`

```dockerfile
```

-	Layers:
	-	`sha256:2810dafdb9cef68f01293edd8c3816f3e15951082ad345062ca43192e3c2cb59`  
		Last Modified: Tue, 09 Dec 2025 03:23:19 GMT  
		Size: 10.9 MB (10904931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cadbe0814660fe98e34285410157e72cd72c936438bcdec7df3cd463bb17788f`  
		Last Modified: Tue, 09 Dec 2025 03:23:20 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:1f5efa2bc9f8c3ff582e84fa68e467ed394a0c34e1bb9617a4e3b78dc219927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306799948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ded91e89d6092826d0b7b81a7dc67fb92190a02789b0ea0c13ce360fc0a83d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:18:38 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 01:18:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:18:38 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:18:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:18:38 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:18:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:18:40 GMT
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
	-	`sha256:7ea3367d9986c7827fe281a47bca9c932100cf4ce09f8142ef14d3d9a12dc541`  
		Last Modified: Tue, 09 Dec 2025 01:19:33 GMT  
		Size: 100.6 MB (100555248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e63e00b786dae319cff4582a8c304a37ca763fff0685ab1ed1f696343dcff33`  
		Last Modified: Tue, 09 Dec 2025 01:19:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:ac711279d784223198bd68bd86224f04df48e4ef5d4992f7e05eea23d810e9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a326c0afa7789ef37c35ea08113ee07fc6df78ffa6f24993fbd841e1948a705`

```dockerfile
```

-	Layers:
	-	`sha256:f85a404c3495582fcc60ddf8ecc752e762217fd97a70b5b25be3ac00b1cfa31a`  
		Last Modified: Tue, 09 Dec 2025 03:23:31 GMT  
		Size: 10.8 MB (10755674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aff0c50c993bf4b7ac453887b835e9438cd2c07adbbb39ac6389399db208711`  
		Last Modified: Tue, 09 Dec 2025 03:23:32 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:edda83f1c330d90345cca76d1383b5cb5523b5aa9b481b1487be4059b72f0984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304078218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461c7db1331b19e172169e7312b31426366775a7635368ee57b90039298379f`
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
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:12:05 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:12:05 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 06:20:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 06:21:00 GMT
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
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6849ad71391fbbeff8d3472dbaf3d868186dc95123c70609a1adde617759e1ac`  
		Last Modified: Tue, 09 Dec 2025 06:22:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:0df8c06a7aec2e4ec38f44656ab30d04a0e6cfbc01fd857463e692dc4d078265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc0ea5c25eb7d1fdf78eca32487758741ba89c533f4f8f1a157b373321c2d5c`

```dockerfile
```

-	Layers:
	-	`sha256:fd7ba604dfe0652a6c107f74a16e99c4d148aa256b5bf017d2e5bdc093a7f9a7`  
		Last Modified: Tue, 09 Dec 2025 09:22:58 GMT  
		Size: 10.8 MB (10780236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37d00d6023ca454fe54a45729be587e4a531f26ed20aad02672f290a21c1a86`  
		Last Modified: Tue, 09 Dec 2025 09:22:59 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; riscv64

```console
$ docker pull golang@sha256:a9ef5087916536ccf73d37ca013eb543d388c08328128d11787509e8617a7928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329652894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81732d9e38d2ba4f4f45a32a30029a841f1fb72568c98c5ff5ec397aa8b15de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
# Tue, 02 Dec 2025 17:47:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e0bd57f07edd1f2c8b8856bd692a6771cc3266d609122cd7d402e0c6f3e3b5`  
		Last Modified: Tue, 02 Dec 2025 17:54:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:fd99a4ad4a79541622523fc85b0232c6ba9c023d2026aa3cfa40193a14675143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e685c65cabe935e4eaa808a78242d3b2b89668219606249dd450cc46f72814f`

```dockerfile
```

-	Layers:
	-	`sha256:956be67dfa65107c67bf03b80e858103ee7bfbf7d4da0232d29859900fc99bd9`  
		Last Modified: Tue, 02 Dec 2025 18:09:47 GMT  
		Size: 10.9 MB (10854069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1700a1f0447258c0fb6474ed381051bdcabf607364a539523700aa85a5e8ddc8`  
		Last Modified: Tue, 02 Dec 2025 18:09:48 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:8e612b7aa289e9adfc9d7ebf758e773772283ad5001a00c01d7e5f0df0081b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280163602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c6f589aa3269204b9a2cffd8841408da19f832f8e775a295d4adae8b8f5ece`
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
# Tue, 09 Dec 2025 02:59:28 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 02:59:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:59:28 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:59:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:59:28 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:59:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:59:30 GMT
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
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a9e961325948363100d5bf4169ac5a2766670063f6aa5d0860b8ed7f03d0b2`  
		Last Modified: Tue, 09 Dec 2025 03:00:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:866476b6405d21e9121a8e6952a69e4d0a8dd9fe6bdb4b68729b5528affe5728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146637d5f45edabe69713bc1007ffb29eafc03744b756bcaf57639a7cf41ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:c28e78f5457bc3963bafaa56ed6586f2a1a334fcf0a4644de495b1f4f6d53161`  
		Last Modified: Tue, 09 Dec 2025 03:23:53 GMT  
		Size: 10.6 MB (10594828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7742e5e1ba6aa2a09a3ef3a9d0d030403983f72d69e78059b1fb856129652fd6`  
		Last Modified: Tue, 09 Dec 2025 03:23:54 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull golang@sha256:7a4e9d5bf345ac16668b0e1ccc76c207c139a5003038e26970041a88ea39f8d8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3367249447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4579d7383536f79932f503558d5703d1911e210f98c6b3d1843dfda25e8b03`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:22 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Dec 2025 20:45:23 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Dec 2025 20:45:23 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Dec 2025 20:45:24 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Dec 2025 20:45:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:45:36 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 20:45:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:45:42 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 20:46:55 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:46:56 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a65c5945d6a62fba2ec80d5ba8557ff15b9221af5c1a340771dcf96df595b1`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9a4fa9c9ac64b71ccc2fabadeecb13af75450cd7e311f804f50e4bd67d2b9f`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5077794eb2c12fd6b4cc6e7fac06a6f7efdfe3ede5b40efd0ebd364dc5dcd308`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8840b213f30390e857d141451ac0a43281e75242cb2518129c634c2e0c07cc`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715838288520ed30f0461c463620eff73bea39c9e8a442ec9bcb47ed1af4377d`  
		Last Modified: Tue, 09 Dec 2025 20:47:26 GMT  
		Size: 51.2 MB (51219379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8149f62c0cdd569980796b1e62b492c262c217cfd51f6651656eb178b9f78061`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a31222f73ee68aab83a8205d925974262f03852ffe9bdc5f499cc33961d5cc`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 343.4 KB (343378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb72f61a5d963bf1ed66d5ba6b41a713c01955422d11000824ff4d9d2e182fc`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b6808e90e2265e2c4369b29bd9c548203728aa0f8316616c98696f616e03ef`  
		Last Modified: Tue, 09 Dec 2025 20:47:28 GMT  
		Size: 62.6 MB (62555607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933ca3a51b8c7d4ca0ffd4e53bd8537791de8a22ba21e328576ee7ff96aab88d`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull golang@sha256:354e8d7b54665e69421d8714a55cfdb9037ab128a432cf766053320e7089ece0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1894105562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671b49b0f8bbbac978fe909f8a52e822b4988563ee973acad2bd2809068476ee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:41:43 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Dec 2025 20:41:43 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Dec 2025 20:41:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Dec 2025 20:41:45 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Dec 2025 20:42:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:42:13 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 20:42:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:42:19 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 20:43:55 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:43:56 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6381426f6db953d9a70cba6759e20f0456f0b12bdb617e9dc982295e4d1c410`  
		Last Modified: Tue, 09 Dec 2025 20:41:33 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f148c26323c93f615ca508b193712a39f7c1a253217ee17b536aa5333db5bf16`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0678a53d729d5770d53e0a2df79db61466f0731975e73cd61dc6d8f34f478caa`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85501a3ac4a80ddb1616e95f5465e32a289be5754e2bbd34c4c84a8117edca`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28613216243e696ea74ce0587ccc8435639adc4efab69c086bd2f08818478f86`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adfd8afb28d6c19753b94a29ee62ffc3239782f87d168cbd2bb219ca08a2645`  
		Last Modified: Tue, 09 Dec 2025 20:44:36 GMT  
		Size: 51.3 MB (51330976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5983c826c590b9d992c4fbf25185d44eafd4459604413aac5bd615dc9c40ca`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6339af4cdc57a9413ae462f51e3bff8b6bb130c058c821e3415cbde286d05d6d`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd165d2766362e7b847e3f2d63c43d2bd269075fa0bf7b7b56b7821a23bcec1`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714939082fef4f8863aa9a64308a8815dcc040b0a831d71dce144724da0354bd`  
		Last Modified: Tue, 09 Dec 2025 20:44:35 GMT  
		Size: 62.6 MB (62556260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd79dd767758fbe9d751a512e4d6f551afbbbcb3e663f7f540293316b10d1ae7`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
