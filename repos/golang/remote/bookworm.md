## `golang:bookworm`

```console
$ docker pull golang@sha256:3a9cb553454690232efc72058d811a676893d950e37d35ac2214c8151d821632
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:8de916b1ba0de2fac0924150854d2e8ed8d3f022b483ef066bdb4ba020abef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303105858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b602ca28639bc2d3c0f7839a4a62391d78de5d359cf93d29a9699800cb40139`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3c4910674529b10db5c7c3f10361aa6a9c058e9ae6f93b1d5714d32915c95a`  
		Last Modified: Tue, 03 Dec 2024 04:31:47 GMT  
		Size: 92.3 MB (92312107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e4f3c05344ca2519bf38ee7a3d434664d8bd18483d614cdb8830241c800ec0`  
		Last Modified: Tue, 03 Dec 2024 04:31:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:539f6ac01a6b13aefe12ff8e59df62b93c2ec5419f0e8a121178c112172b9577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10320538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90be9511a3e601d5a47bfdcc59d86c993bd9ffd788617d3fbb6a59dcdc873d4a`

```dockerfile
```

-	Layers:
	-	`sha256:4fe1b89f42e8e206e498aff260d41ae38d98197efd61c8bb439d7adc3f4e0f6f`  
		Last Modified: Tue, 03 Dec 2024 04:31:46 GMT  
		Size: 10.3 MB (10292892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772e733e22e59e4fa7084a5ac099efa5e2a58c2d24194651b240aafac8630723`  
		Last Modified: Tue, 03 Dec 2024 04:31:46 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:6ebf8b07cf1559c29dbadc1bec7cd36147b42ad947342cee9713159f078723cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265085888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e146329e05ac178000d718f440ada1321828528d4f85643b0c7155c5949c6f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efaca926219995f98eab37fadc294a1f7c7dfeb2509ccf4955298c4b9d15d3b`  
		Last Modified: Wed, 13 Nov 2024 15:34:29 GMT  
		Size: 66.1 MB (66149571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29986a4aef62845cc264a8697ac5fe09037f6d2ab1877dff15c025a0258a7564`  
		Last Modified: Wed, 13 Nov 2024 15:34:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b19571ca0cb50196e511b2ba04859fbbbc7a2d8e6e77ebf1a4ee07cda5cc5d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10130019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461563d864e4d92ceb0daa83e07db6e19eb795be7758358da0726ccd22710b0f`

```dockerfile
```

-	Layers:
	-	`sha256:dd0b2bdd1d63188a30062bfe9cd534e285515bb88358100609a2baa5b768f28f`  
		Last Modified: Wed, 13 Nov 2024 15:34:30 GMT  
		Size: 10.1 MB (10102239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834137c12b63fc95daa366dbc51e89f01abec4051eb6c9bda7f81059bd514f94`  
		Last Modified: Wed, 13 Nov 2024 15:34:27 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:53a9c8dafa550eb772ff742e0a8b80a5cfabd7fdb7635fe0e5e5fa413c85a848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293092624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874a8b40ad6058f3f160636c61946394559b067562d7478cc3f9cc500794e9aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332e0182773167aa8111aef327618ba02538158e60e78f224f3dc66898e65dae`  
		Last Modified: Tue, 03 Dec 2024 16:34:44 GMT  
		Size: 86.3 MB (86344174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1052ff2a0a28ce0d821c81e124df8aab1d2aac30042eab2d08696d8e62e48e5`  
		Last Modified: Tue, 03 Dec 2024 16:34:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:61235ee32cb2127bf2054046c05ad88c82c84409355f245c632a270a5d9cc788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12340fd0397a2cec4cdb0b95529e1495f8d85e24d16a08fc093e7c2963da259`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e3c4c30be53cdf6cda02b7c448e382c9db1024aacd3c6c97fa4d985f9a830`  
		Last Modified: Tue, 03 Dec 2024 16:34:43 GMT  
		Size: 10.3 MB (10320818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790c5527586192996ce006c2429acb8022a2e59c9b7fe4f18c67d9507c8dc27c`  
		Last Modified: Tue, 03 Dec 2024 16:34:42 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:16c87be4c0525d8d078e03fdfd41ede742eb54ca75731bca3ab39c414bb49153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302010588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d5ab0602b8c401f3777fbae8ebafd1f05dab1690e7ea53c4a4c6f3500cb6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bd268cc4f2585d70f2adb8cb9444f9543cf7161ce32bda41c5496801463528`  
		Last Modified: Tue, 03 Dec 2024 05:13:39 GMT  
		Size: 89.7 MB (89708175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d309da02a5efef0a1926ae8de3247932524a303115a90abb23504c4cffb291`  
		Last Modified: Thu, 07 Nov 2024 02:59:09 GMT  
		Size: 71.9 MB (71908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a168fff9ac7939af35545db5aec1ceba912afb817ceba2228256a0249053363`  
		Last Modified: Tue, 03 Dec 2024 05:13:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fb96fd6366ed48961a0e777e5b6def6552c8c32860e2f8b759fb31c09c055fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10300525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794c946ffd0c4cb4af9c60ce660f3fab7fec7fdc8380fed46870285a8d7a9e94`

```dockerfile
```

-	Layers:
	-	`sha256:076939dd56db77569a7bc56b6f4c71018402aa4d45a2550bd0c4e87058846abd`  
		Last Modified: Tue, 03 Dec 2024 05:13:37 GMT  
		Size: 10.3 MB (10272936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b1ab64bf8db83bab67e185b85c7101b5d8eb90f7e481de91d09247c17ada2`  
		Last Modified: Tue, 03 Dec 2024 05:13:36 GMT  
		Size: 27.6 KB (27589 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:59b77b35a3d6c3a4c295d6d5df69149b221a3e5ba41b7bb00c3a24c74609f3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274672531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde1e77d951a4386dc56391ef48dae68cc4b6f1821e152e30d528808c6779fd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aa8c732dc480c917c006c596db2d04829d92a5899b87a988672ce7b03cfd6e`  
		Last Modified: Wed, 13 Nov 2024 02:02:53 GMT  
		Size: 63.3 MB (63281490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1f6f25ee4e0c7b1ec6d148ab77c50136bdbef9e338e495fc099aa79871dfa`  
		Last Modified: Wed, 13 Nov 2024 07:25:48 GMT  
		Size: 69.9 MB (69865831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f81694bc2d6f633d7ccbad361e1e6ae621631bf889fc11bc127c432c7d8965`  
		Last Modified: Thu, 07 Nov 2024 03:03:54 GMT  
		Size: 68.3 MB (68313700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efa916d122a23b333bd99f4522bc6a29220a831b64100cd1fc564826210d04c`  
		Last Modified: Wed, 13 Nov 2024 07:25:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b9eba0ee8dcbd968db6b4b24790668000936a7e5751533631bdf084421f24f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969f51434f02e0bf745cf19c01c60cb87eff4d1ff7711cd140754b8cf1204370`

```dockerfile
```

-	Layers:
	-	`sha256:917a57fe7bca9e2a2a5df27049ccaf50be13a09344916c5eb268631a0e72fc29`  
		Last Modified: Wed, 13 Nov 2024 07:25:40 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:271cd0ba276befc685c380a08f7f902091374aaec3e2e1161e19c540cdca47f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308782357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd8f20aa0429cee6d2a0cbc6b8cc9b39d97882ef54d80411a9fe675fb16d5b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d70c79056b0a3947fd7e791e4ef06a40f2032e4fb8fda3cb9196cf1113de0ae`  
		Last Modified: Tue, 03 Dec 2024 16:35:30 GMT  
		Size: 90.3 MB (90289269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41324e03ab12f813b1cd5e31f13c50ba90ab3db5da49b19e83a370ead2686a`  
		Last Modified: Tue, 03 Dec 2024 16:35:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3f16747357645d377826939d64d36b4bc5a57e1d946d137e5f0bde547c05be76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688d8f4f7016f5d02130553c2c5b40a8b49c89f74e696766ef7025ee94df7b5b`

```dockerfile
```

-	Layers:
	-	`sha256:d9caf34d3fa73ba6c6df57232b55d03741f74b8846f6209a467a30894b422a24`  
		Last Modified: Tue, 03 Dec 2024 16:35:27 GMT  
		Size: 10.3 MB (10265535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e37a2918d29857b55764d8c8428336846cc26fe3a541ba89877129c97c76750`  
		Last Modified: Tue, 03 Dec 2024 16:35:26 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8758f4d2da369c28514d3e84c054e90b733c6a36ca92d341c3a432f706862c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276314528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b80f599b48b3dce89bcd5350ce66b7efa26323d0b3940815503c2bc79843884`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1aae87a204413459bf91274f58e9c4ca1ffdbc9f4c277d39d7c5cbea26f566`  
		Last Modified: Tue, 03 Dec 2024 11:01:38 GMT  
		Size: 68.9 MB (68876869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10532dfab6a350299d039988d07ad43c97ba4c2b7d094e44c673803c36f2bd6b`  
		Last Modified: Tue, 03 Dec 2024 11:01:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0155fcd91c56bddc7f0bef126ea57a54d583afda20f42d8ea725bfc39880248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10156300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b684264bb9c6c274cb5254acd94e07830632c9a8d9f6567890cec8beeca138b`

```dockerfile
```

-	Layers:
	-	`sha256:269b86818fef8feb68caaca7cc1cfcbb13edb919d6a25087e3346cfb10847e90`  
		Last Modified: Tue, 03 Dec 2024 11:01:35 GMT  
		Size: 10.1 MB (10128655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6fb74a1da86d8c3f2124bc7c846b882845b6645d2344cfe24efc17ab4936fc6`  
		Last Modified: Tue, 03 Dec 2024 11:01:35 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json
