## `golang:tip`

```console
$ docker pull golang@sha256:2ae681a8cfeb0b91c2f5770d8e58f40f2715eb7343053add9e13b69f8bc8b98b
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
$ docker pull golang@sha256:a3915978e33e261317b89244d8cf41fdacb5e07455f261fdc8f94c4b53e6356a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335412742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a68981eac29c026a00fef9d0c8135a0e85064e0f1881569f52d12f70956a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b35d3b8620bcde4ca6e72ee99be5c681995df357f36e9d70a95aa5ebddc7e`  
		Last Modified: Tue, 21 Oct 2025 11:18:32 GMT  
		Size: 102.1 MB (102088374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5533a24a9e37fce0b0e949796f7edef8b1aecc8af44711d2767f0566cd2c9677`  
		Last Modified: Mon, 13 Oct 2025 21:02:56 GMT  
		Size: 90.6 MB (90638837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc312b8768e6a009122ffeaad8e2244b173dbf0c2b069183e74298c197a119fb`  
		Last Modified: Tue, 21 Oct 2025 11:18:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6bbe83d0b67626a84a8393d3835d39ff4d3a72fe43ee4c1e70fec70c0c403242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49837a83fb32849c4b336dd7f1503990f14515eae602f9d75df9973a88009363`

```dockerfile
```

-	Layers:
	-	`sha256:cf413f2913fb4b62cb7ae9502c3c372f1e86e5b5082c692186383a6d9c5b8e52`  
		Last Modified: Tue, 21 Oct 2025 14:23:12 GMT  
		Size: 10.8 MB (10784460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b16fa26ec3316f230f035db35f2505cd66fd04118290ef866e3ad8424d3c4c`  
		Last Modified: Tue, 21 Oct 2025 14:23:13 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:81fafae640198a4331beaffa2155c84fed945f72c73da358979472451a794a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292617845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7becaa88d3495ecdd83d12d203862305f014553476658ff066ca420f72117356`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb493dcf3b69e9a1db697812a3fc5bfe7fcb242df4acefdbc52c83061a17b0`  
		Last Modified: Tue, 21 Oct 2025 18:15:32 GMT  
		Size: 72.7 MB (72733669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e37a565b466ff673d6eaad95f7f918df4a47f13ea7ff94f9312bc4a254253fc`  
		Last Modified: Tue, 21 Oct 2025 18:15:25 GMT  
		Size: 87.8 MB (87837459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a856dfd500b2aa8241f23d4669787e93188d793c824341ec59103ce815f2e6cd`  
		Last Modified: Tue, 21 Oct 2025 18:15:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:371e9e28dd2efc8fd1bdc5dd63a865e31e93d647025ad9e02085f57e2542f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbad00bc52e3733c59982fdf4904cc813ed4aecda26975610e2915ec9eec649`

```dockerfile
```

-	Layers:
	-	`sha256:d52001bc3ad5f4b4c578a5d2b3fbed554197b08cd9d0f2387f5451f54af513fd`  
		Last Modified: Tue, 21 Oct 2025 20:23:21 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82be58608af11df0966bd94327550281a5e4aae9a4d90fb18b2fc0cdb633d879`  
		Last Modified: Tue, 21 Oct 2025 20:23:22 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e2525ded3c602b9a736006ad95be6ddb8e0a5b924ea232f773d570ffff220100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327273357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b856be8164e60d280650f21d5a0d0ff45391505d377b5583de62f55bac9e4926`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a2979d3d2873337872b28636ebe83674827dca73806746af98a4a1108b939`  
		Last Modified: Tue, 21 Oct 2025 18:13:55 GMT  
		Size: 98.2 MB (98234205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c596fe60daead99d920e71d2cefb1c0329c841dbd8772728b90e497e3f4f21b`  
		Last Modified: Tue, 21 Oct 2025 18:14:12 GMT  
		Size: 86.8 MB (86788679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c7592f4866fe7dd69a089d41d99689231559236c387e2a7cdfae60c70663f`  
		Last Modified: Tue, 21 Oct 2025 18:13:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8b2912e70d9b43faa08841ebfcd084980cd5ad74a0e9b907f5234a33cb86ef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40301f124d2cd3e43066f35f1535b09fe3956942051cb4d6c99f7aca0190563`

```dockerfile
```

-	Layers:
	-	`sha256:22f49855aae0cb8fbf66e8c16aa23c8e720fcf517154ec8c45bd1efd89d86bde`  
		Last Modified: Tue, 21 Oct 2025 20:23:30 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6527259ce91a601728b92a1fd301be5392eda55f261a09a8e6d04724e1c5ea81`  
		Last Modified: Tue, 21 Oct 2025 20:23:31 GMT  
		Size: 29.2 KB (29166 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:8e6af2ac9a6abf4088c422b6ed5975ea36b64e25a872ee90c91c394caec218e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337567965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba876d81e88cf9fd65d99c700ab6a18f9d60400635b0aaf0ef39aa630f2b69f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedac785dced647bf1c5e3bebc7774ba100dbbbe98decc8a71b09a04910d1f2a`  
		Last Modified: Tue, 21 Oct 2025 18:13:43 GMT  
		Size: 100.5 MB (100533198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f21a8159428f1559d656875bfece2dbae3e195e6c40dc6a160e07432d96a1ef`  
		Last Modified: Tue, 21 Oct 2025 18:13:42 GMT  
		Size: 89.7 MB (89663317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2ae2e87e35026c7590fc9e60523518ec8ba6f329c01ea2f61f3fcf2fd87edb`  
		Last Modified: Tue, 21 Oct 2025 18:13:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ee36a3fdb2643e91230e18dd26530325fac8b2275e74f3dc4f76fc4021bde289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc1f06b8d686ebd23fc862bcaee23759023fee2ba959f452d62ed6ed5b8b20`

```dockerfile
```

-	Layers:
	-	`sha256:6f95392db2d725bc8faac36093fb78a71061714a34c5836eee459814eb20507c`  
		Last Modified: Tue, 21 Oct 2025 20:23:37 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2997047cabc8076ff203b172e7c57e20555c046dac743aa8a99cf9abe5e8ab37`  
		Last Modified: Tue, 21 Oct 2025 20:23:38 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:bc82323ffff3ada7aef163565fb1c3be10b58dda2b305fcd66378d64a891bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333376268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c11a2b284e1175111a02d99740f1e14ea99d8c4d9c9fcf8f53ce0a2e7d0df7a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed492992022fa9e4a253b427574c9ab21d82072f73e353ad6f09e1555a92cc4`  
		Last Modified: Wed, 01 Oct 2025 11:14:56 GMT  
		Size: 73.0 MB (73034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39ff1a0b943456854e6b1ed7d946a7e67cf44c76fe8ec18f870bf569ea577a6`  
		Last Modified: Mon, 13 Oct 2025 18:24:18 GMT  
		Size: 92.8 MB (92794871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a59992ca0e08825ec7e153d7b4765b1eda5f370c39d6ec414f6606e002f92a`  
		Last Modified: Mon, 13 Oct 2025 18:24:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a6633968c6f319489862182820e6b29767dcbff018dc8a10e9736bea6b4a5de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60181d9a6566f2459ba30bfc1e48f519222ecff13b38cf766c43f027178d3ea7`

```dockerfile
```

-	Layers:
	-	`sha256:8a3cee19dab0c7553961899b3aab8488062a2fc9e70c814269140fb74a5a55df`  
		Last Modified: Tue, 14 Oct 2025 02:24:30 GMT  
		Size: 10.8 MB (10780192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5acdd1ca779b177d8ead0231d0cb3b84cdcb10fad8ebb5c20e6f9084aeface`  
		Last Modified: Tue, 14 Oct 2025 02:24:31 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:c2ad7ba1a4c1d7b8219649e1c4c3ded7889ac2d7ed0607248fba2345c4c8ebb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358859190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387129908e565149a2d060f48b4de01584c48a5d0df1cd3bfe6a3504493d50d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c645409e32b37950d400f06f75fff87e9a716322f248e5d01d290689226a51f`  
		Last Modified: Sat, 04 Oct 2025 03:44:05 GMT  
		Size: 66.7 MB (66659977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146033d470e9e45a40f2f8858ac379252d8b815c5b3ca04f3f509638a2ed95db`  
		Last Modified: Sat, 04 Oct 2025 11:31:35 GMT  
		Size: 131.6 MB (131577430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2d5d7683a75ce062ee755840019c59bf7ca74ff155b360004efb2f79df7164`  
		Last Modified: Wed, 15 Oct 2025 23:27:21 GMT  
		Size: 87.9 MB (87898833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df439653f7b652e8205d268b8e47de691d128119856a5ede128ab5f557d915d`  
		Last Modified: Wed, 15 Oct 2025 23:27:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:77aacc66cf22fd81e105b913d385dc20a6b98b5b1bf3595f1a810ee72bfa7fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5162af81b0124ba5fc57dd97130a1f9bfdcbd5c31e377e120e3d65b8854106d2`

```dockerfile
```

-	Layers:
	-	`sha256:e081f0239efe9282f9c6a5a698f1b2543b0bd1e6fb0b0fec65fbf68e6bca9762`  
		Last Modified: Thu, 16 Oct 2025 02:23:47 GMT  
		Size: 10.9 MB (10854025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9424e6b4b035a9f098e6d8043e203664094b66d594910b67b7f2d20b17a4dc`  
		Last Modified: Thu, 16 Oct 2025 02:23:48 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:4cfebce8e9ced5bf36f4960687d503699fce38831eed50917522aa23c30e5a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309464953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ef4fecf6fb73aaf59fec6caf30c6017c8efc998a34e9238a579a2f8a04428`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2360823d72f62f7ab99d1125b961476d915cd531da8e87d42d3767dfd3b86d6`  
		Last Modified: Tue, 30 Sep 2025 15:54:22 GMT  
		Size: 68.6 MB (68637856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a77bd0f38ef8a06aa5c038a198543d87d293c0d046b35c3e41c08fb8c27b73`  
		Last Modified: Tue, 30 Sep 2025 23:49:14 GMT  
		Size: 75.9 MB (75901079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb375f85b16f323994bc2fb7d3430268da4ef6454a80ec345f8bfd588fc5195`  
		Last Modified: Mon, 13 Oct 2025 18:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:49d2148238b32cf5c6328ab07d30e9c1a1227601d8ee2cc303f3e8b13bc401bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa726bf78276824b0540f6c7dbdf1cf29ebf9f09b17251ba33b6052e836d6b0`

```dockerfile
```

-	Layers:
	-	`sha256:253c24c55a6d1c77842dcaf206878316fc2b6a077ccec4472c120473fc2a6650`  
		Last Modified: Tue, 14 Oct 2025 02:24:40 GMT  
		Size: 10.6 MB (10594806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a955de6f99e604d619bffa91468611598dec1550e0b9fd454cf5023ea60d5ff`  
		Last Modified: Tue, 14 Oct 2025 02:24:42 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
