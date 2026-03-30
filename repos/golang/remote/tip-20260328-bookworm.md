## `golang:tip-20260328-bookworm`

```console
$ docker pull golang@sha256:eb030458eb13e13f547e3ecbb9fc3f27fb490dda294412bfab4c6a5f6e471540
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

### `golang:tip-20260328-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:7662583b5a08264d05fc785468c4f042f7ab85592250a62d3e741c0e1f311434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323316104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e081cc98107ba6b78ba387fcc0acfa4cdc84269b456ca5e0a08d4cbf3b7a5ad2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:46:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:48:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:48:00 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:48:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:48:00 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:48:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:48:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f2eab438bbcc340e905789a5476b60c56322db2fe2613cb75ab0d117787ee`  
		Last Modified: Mon, 30 Mar 2026 17:48:29 GMT  
		Size: 92.4 MB (92448667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc94bcc3a046e419ba11b5fddd09ec7514410ba4c53e7ad8d4f5445debcec8a`  
		Last Modified: Mon, 30 Mar 2026 17:48:21 GMT  
		Size: 93.9 MB (93944870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa094e2854ef613e3383140a7dc03dcf1c947805648ab03f9e1b0a196fd6cde1`  
		Last Modified: Mon, 30 Mar 2026 17:48:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1cc10dc0d4715ff294166aa8b1713ce0c030365cab5a3480d63b1f926618d9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56e8e2bf558145e82a163cb4d77a0eebfd516736b4f4f1af00c227988ce1fe0`

```dockerfile
```

-	Layers:
	-	`sha256:e07dc5f12b8fb72c5c635770387d0a98e8714400a06c103c3f7f53ce795f70df`  
		Last Modified: Mon, 30 Mar 2026 17:48:27 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff666905c805715babf4a6b564a617c751915ed0c450c606993ca439a9c4b16`  
		Last Modified: Mon, 30 Mar 2026 17:48:26 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:7c033051bd7e4fda77b41b497740e47b99622c317582219d3367c6c942756609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282175963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc681694c9bdcefb1092fd6307cd549791d01d68e360cfb89b74bdc69bb9f06a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:50:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:50:56 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:50:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:50:56 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d6199b61ae70d64ea8ce2109b323949373a5900bc60ecf81abb4173c4360cc`  
		Last Modified: Mon, 30 Mar 2026 17:51:23 GMT  
		Size: 66.3 MB (66305286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a0142adc6609c1699e104cbb6d09e5264e25e4e76c071ff20b820aebd1914`  
		Last Modified: Mon, 30 Mar 2026 17:51:02 GMT  
		Size: 90.1 MB (90068807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d5d4cab1342d99f5fd676c9d79441c93f0cd90cd6e90de2da5b4e9f57043e`  
		Last Modified: Mon, 30 Mar 2026 17:51:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b52daef7fa8a0128c3f40eb956fe54947d2db87f92346b267804007def7e8844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f738ff8156e718310016de7a05b8ea4d5efbbf10ee39731f55b9a67f759fddc`

```dockerfile
```

-	Layers:
	-	`sha256:44f1b4d6d7b9145e9a72542d1790b291b587b95375d3d88c33fbce492dffc6cf`  
		Last Modified: Mon, 30 Mar 2026 17:51:21 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aae9dd4d142ee29cb80a6b1e65a006f0ebdb311c51c374db1b5441fea55f3d6`  
		Last Modified: Mon, 30 Mar 2026 17:51:20 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dcf9487b5742d3bcd0c31bc8054fa1f1164a7fa58bc5864a8d13262ec2ff2825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312004729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f0b6f12dbb6d2b0c5a5867b595fdee1ee2c2e81f9744b073bf48826759d32c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:47:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:24 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:24 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a894109b71fb24195073fc37e30ab8cecfa7a2cbec8d58ec8aed3f4894ae833d`  
		Last Modified: Mon, 30 Mar 2026 17:49:53 GMT  
		Size: 86.5 MB (86521430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111f485f6c4b82dc9f58e7d75c491e9181371f2ac26e7bd1ac582e69f4e4bb91`  
		Last Modified: Mon, 30 Mar 2026 17:49:51 GMT  
		Size: 89.0 MB (89025966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585c25ffc8793a592970b2752490c742adb0007e09b71feaa7da44f828db91c`  
		Last Modified: Mon, 30 Mar 2026 17:49:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:edb25a45d062458c6eee08dde623d2204cece918dde883e855228fdec1d67126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f1b139ada653da66bc815d16a85cdeb12d523cc71a6f85d4f16c096b43c586`

```dockerfile
```

-	Layers:
	-	`sha256:969a15c7219bb2776ec17b696912d81dcd76177cb69044bb527e792933180a17`  
		Last Modified: Mon, 30 Mar 2026 17:49:50 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407a09f4d3d85f56fd33d85e3554879201b9a9ff1fc58fb7f4c46a94dbb52b12`  
		Last Modified: Mon, 30 Mar 2026 17:49:49 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; 386

```console
$ docker pull golang@sha256:b2a7d3a9d04cf72cce1d8aa97deff5f66bd6dbc76c5cdc14abeecbc8096bbd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322224691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cc2d107c85e1a7793f547ed858b0bd03ef25fd6623fdb35ebe9b89d80bbf1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:50:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:50:41 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:50:41 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bee325dd3a9f224e5f7543d600a7e5ec17a1643860b46860077b090811e8cb`  
		Last Modified: Mon, 30 Mar 2026 17:51:10 GMT  
		Size: 89.9 MB (89871212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cd517d6dba9b01cd366f9de5344ce7d7604f0621cccf254c2d056e36d9d4f2`  
		Last Modified: Mon, 30 Mar 2026 17:50:29 GMT  
		Size: 91.8 MB (91769368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b6351e45868a3ef9a21a5ca16ba017d3bb0dc6e74ef7df66ebc6c23e02d278`  
		Last Modified: Mon, 30 Mar 2026 17:51:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a103509a90babc2044db7dd184c2d58f89f4743e60b9e4dabec027b59e3e4da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54a95ee6f50681883ca002fc52550130689e18084c896de732a3719d76aefdf`

```dockerfile
```

-	Layers:
	-	`sha256:cdfc6b598e98bd4c3f5d9be260cf19039d663a9176a8e6161a7568f5ba7a8656`  
		Last Modified: Mon, 30 Mar 2026 17:51:08 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54e4ea8c4f48321c80da1ffe77032e6c49b7c5f83ccc40962916c65c19897d4`  
		Last Modified: Mon, 30 Mar 2026 17:51:07 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:f6545bc4066c10f80175f23cdd36f9c6dd97650b42ac3a50b8e83d8be097bcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293502143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c708fad9f18925585ef9651c2fdd846ad486e6cd19860e5a4ba2ee7aa401d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 09:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 15:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 16:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 18:09:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 18:09:11 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 18:09:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:09:11 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 18:09:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 18:09:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55bd01c42402ce77937fae9abfba9b351fd4b3fab7f1f58eccf5b2fcf0ac8978`  
		Last Modified: Mon, 16 Mar 2026 21:51:11 GMT  
		Size: 48.8 MB (48782288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a46874b19723e755d13ba2292477f479fd221937f5480b97990afd32f94b3d6`  
		Last Modified: Tue, 17 Mar 2026 09:32:54 GMT  
		Size: 23.6 MB (23615153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510757183cb1996fa93fc6110a5644d68f4a47cbb4c8f08c9a7376b57b6600e1`  
		Last Modified: Tue, 17 Mar 2026 15:10:46 GMT  
		Size: 63.3 MB (63310157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a828b5f824da9f5aea9f29bedbcb4f1d9ba92baa7cf5754cbe01210a2d907`  
		Last Modified: Tue, 17 Mar 2026 16:31:43 GMT  
		Size: 70.1 MB (70051096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395405fc05d594366b3fd75c181425568be9906f35628e5124e07631495d71a`  
		Last Modified: Mon, 30 Mar 2026 18:11:20 GMT  
		Size: 87.7 MB (87743290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e7ebeb5c8c9099b31c205f30822d971673b48d8ba61cff425f49e24cd82d9e`  
		Last Modified: Mon, 30 Mar 2026 18:11:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1069212ecf787b2aa57e3b38b5732fd90a547864f3a1a02a6c5c75a362279900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189cc145c1b569ec9cc61dc9f6fb85c2849de30a6e5bf1e314a57a9b005e1a38`

```dockerfile
```

-	Layers:
	-	`sha256:be23ca63cb21f105a60fdb8d62d20b05f24d419f8fedb0b501fa3b4fedac0310`  
		Last Modified: Mon, 30 Mar 2026 18:11:11 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:241db1ce50afbe0d33046b95215f5e878fb0da338bc92ab51be55339a6f27e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329049830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f085bd27da2e4fdbc3c5bca215ac92733df855ac6a18e4c7cf34e9377eb45eb1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:52 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa85d4ce5e832d1d4657e93cecd987718fa0d7c00ae8a0ce1f712b8250b7c0b`  
		Last Modified: Mon, 30 Mar 2026 17:51:17 GMT  
		Size: 90.5 MB (90462716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111969b1f573be958af91f197054c394fc84f73b452627519be6a7f12a1bcd78`  
		Last Modified: Mon, 30 Mar 2026 17:51:17 GMT  
		Size: 90.7 MB (90732531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a887ed363f401a562960d14422e34adf137f6168f3ff6d318bcf0dc1405e0dc`  
		Last Modified: Mon, 30 Mar 2026 17:50:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:eec2aef674e6e4fda611356436efa38ad86e3397e16b59baaf836579ea7494cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0414603b0e95ac6d0605192df53695d882a23f2f53156445567d35b604495a6`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e4288d454bdd179b86b76bc7a63ca25f1ff75903742b007131e12a708075a`  
		Last Modified: Mon, 30 Mar 2026 17:51:13 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20789a37cf65411859cc976915d53ca71af7873e47f6be65ea5e092a843b80a0`  
		Last Modified: Mon, 30 Mar 2026 17:51:13 GMT  
		Size: 28.4 KB (28430 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:bec9a50c34ed2da640bc22e19d258e197c0ffac2d3cabc46fcdf117601fabdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296862464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f218fd38e5d45e232fed2f3d9904fcbafe2896fe8893acaee525a9460eb571`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:53:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:53:05 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:53:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:53:05 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:53:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:53:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8729c50a9715cd51767c0928c4780679919845023acd274c5d9bbb94de067c`  
		Last Modified: Mon, 30 Mar 2026 17:54:39 GMT  
		Size: 69.1 MB (69055243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77473e8e347c240104f79da8f95d36830a796c56bf93ad436d6a5a18785036`  
		Last Modified: Mon, 30 Mar 2026 17:53:56 GMT  
		Size: 93.1 MB (93124064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c258f2e43be73e9ce4f5a4b159dc59d829297a2247c796b8c43c224b4f74b7`  
		Last Modified: Mon, 30 Mar 2026 17:54:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:16ecbec5c4ffa83193f196a31c438f56ce078520e8401eb2d507d266b758b1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace60839d339437d13729fe474ac12377a3b5f3afe01b25003a08814d1fc0a05`

```dockerfile
```

-	Layers:
	-	`sha256:018bf8e4dc9cfe86e0da0637423890558024cbacd8b8da2ba63c599853b8e9a2`  
		Last Modified: Mon, 30 Mar 2026 17:54:38 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c95c1d29f88c4f47bafde303186dc7406539ba43b2c2dd74eca06d360f40b96`  
		Last Modified: Mon, 30 Mar 2026 17:54:37 GMT  
		Size: 28.2 KB (28213 bytes)  
		MIME: application/vnd.in-toto+json
