## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:9855fd1ecc573f4687ecb7b1d345e22efc1f8a5fa962e02bc21cb3f870a7cc63
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:e23a4746087535febe964f63c712d9a44b2f13af95a5f83a7d3e20b387a1fb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320934822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451916c7d0f21652371158f6fda8031b66cf01a310ffa0563bd01c3d749a6b14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:06:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:34 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:34 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:07:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:07:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2468f1f7041dd9870cce2055b79fd556be727c87039442fa7b6e5c900b8b8eb`  
		Last Modified: Mon, 03 Nov 2025 18:08:13 GMT  
		Size: 92.4 MB (92402129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ddc1baa3c54f33af374bab7f0bc2d92b2abf14d2efc6c30e66401dffaa233b`  
		Last Modified: Mon, 03 Nov 2025 18:08:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f6dfbd653b1f14e3519505c852f032b79ea78573e3b2ea62826a411331f798e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffa3b8fcaaca835cf87fdd1b38315013aa3b9e1c069304f07ce6e83a3d50df`

```dockerfile
```

-	Layers:
	-	`sha256:eeb8127cd09fa04e9fd519e1de5c5ca51bed1a17a136fd109416d559227b281f`  
		Last Modified: Mon, 03 Nov 2025 21:24:45 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa140ecbde3775e844c538dde0df1d65d1bc4bbb6d678d1718c015998f71b2fa`  
		Last Modified: Mon, 03 Nov 2025 21:24:46 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:c64a00f57269d640e8446a9327a68dfcb070f0dfdeca0ec9d87d5ed359df9132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279845461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baabdc9907b7ae55602bf4d0e6ef95e4647d1889b474a82cd35b17d015824fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:09:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:09:36 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:09:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:09:36 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:09:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:09:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264520927e14a358fcbe294108635a668d055fd33a42b4721a5e7eb4022c023`  
		Last Modified: Mon, 03 Nov 2025 18:10:21 GMT  
		Size: 66.3 MB (66255521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22f91d508d2b8d688535beb13855014e64270130e5d7625964e4dc19fafecaa`  
		Last Modified: Mon, 03 Nov 2025 18:10:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e681b407066b1fff3bb5c5bef99388a4118a84be7e5484d1e7bf3a236e45fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da019e6af9cddbad21bc4238a1def51bb46a567b05eb9a48415c46f09c3f90`

```dockerfile
```

-	Layers:
	-	`sha256:bb1318860f285e718823a50833655c2a7d59c1942ebe88e270605240f73119d4`  
		Last Modified: Mon, 03 Nov 2025 21:24:56 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cc0f28c1246ae5080124009dc1237cb21f3c35040b327eb2c8ac93f9bd271f`  
		Last Modified: Mon, 03 Nov 2025 21:24:57 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:816f89474fca362d6f353651f1ad149563aae28f45302b579f0637cee72ce0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309678180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3828a21f443045c2631dfeb0e143aa52b1a2815f75b7939644eb67c4e956a393`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:47 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:47 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:07:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:07:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac7089cdd278662d5a07e38b25e60db323d1af92a5874ca3fba88488bf3d12d`  
		Last Modified: Mon, 03 Nov 2025 18:08:36 GMT  
		Size: 86.5 MB (86471532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430491499890162858da1bc477b3b1fbef031b5f72b7dae4e74bd22fe5b053fd`  
		Last Modified: Mon, 03 Nov 2025 18:08:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0ddcef331e20c6517bc82a951bb394c592c96b639649cf5df2d7daf9e2479b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6116b360eea16efce18d08955196e1412151c030772989583b4bbdd6d0fd4f`

```dockerfile
```

-	Layers:
	-	`sha256:32ec0f9c7dd0da3819d4726ecca1b9346927430d65b30b4593bce59d2ca0b64a`  
		Last Modified: Mon, 03 Nov 2025 21:25:06 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a8e6657a4bd781792b1d5d6c06109ab562c08c3ff25dcd12fc6712bdde3e05`  
		Last Modified: Mon, 03 Nov 2025 21:25:07 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:99b4f4c215f7e3a10cee60136f04f242c3312823dd1895488a89f9d7dc4fe63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320001856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f179f79bd4ca2dd1476ec31374ede8a1723f2bab9d90afc0d6e3ff80ea88bc89`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 03:17:38 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 03:17:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:17:38 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 03:17:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 03:17:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b596182a9b4836dc17a3bc5eadc1e2798b0aa5aa0c8f50fec56b60d802ddb375`  
		Last Modified: Tue, 04 Nov 2025 01:32:07 GMT  
		Size: 66.2 MB (66233815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035d668f3d0cee78b1e6e409d066db558c08d74e955f89ae8e0c7e0caba876d1`  
		Last Modified: Tue, 04 Nov 2025 03:18:38 GMT  
		Size: 89.8 MB (89823373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa89e75c0c953319d9bff7e39d68ebb6f7b9628befd4d9afcd44ce4625752bcb`  
		Last Modified: Tue, 04 Nov 2025 03:18:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ea5b86cf6d5906bf8f5c0bb07dd52552104213a98d394b16a129da39d374d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e25fc0e0004bc68551441b305d62b481152a4546f8f09e3c8638544e983f97`

```dockerfile
```

-	Layers:
	-	`sha256:d0a111a2f545045fcc0b1581612e8c45646fa56d793e0337f66400369b3facc8`  
		Last Modified: Tue, 04 Nov 2025 03:18:05 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91ed3908d18781d09d81c6f408f1f6344a04d063bb6c1c5a292b62e44c535a3`  
		Last Modified: Tue, 04 Nov 2025 03:18:04 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d011a6b01b93bd831802cce3e8f8889729936097c798ab9fc910a64d29f4ac87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291258703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d236c5c6c78645d50928faf5d1cbece1e5adf476696444cde910e68681a534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Oct 2025 01:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:30:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:30:42 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:30:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:30:42 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:30:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b8b987535d1ca746e1df1d7a5e1bbbe17811a45d2a394c4b90bfa962bb4cb`  
		Last Modified: Wed, 22 Oct 2025 01:07:48 GMT  
		Size: 70.0 MB (69997127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1ab417de53c45975d074e15d8a2784ffc35415dd457eb8b64a5003a76fa88`  
		Last Modified: Mon, 03 Nov 2025 18:33:12 GMT  
		Size: 85.6 MB (85577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528cd1f90bdbc4cb79582836a13ed72ac50ab9030537170cf285dd020075779c`  
		Last Modified: Mon, 03 Nov 2025 18:33:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c110eb1696594ed6fa1c723b971a08eaea556027ea898d3d57d64783a48fb26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d1594e699507dadd5a747042315c06641bafed7b3b93d56e57a269dbb9bad7`

```dockerfile
```

-	Layers:
	-	`sha256:4b677abee1335d54c4a7a19dbb3d7b329bb7a7cf970e7fb9f3929b511036c4ba`  
		Last Modified: Mon, 03 Nov 2025 21:25:24 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:9bec222a8c7dc39a0cecf71fb7e3a91914786654099a6959bc53c7692a270f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326554393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e237afc2805334976c53fc85dfaccc3b5bcf722015dc8ed0b1e629421afa29c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:13:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:13:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04d953bc0afef745a3953fa8df1889906decb886f69b2e0f1dddd428304c77`  
		Last Modified: Mon, 03 Nov 2025 18:15:09 GMT  
		Size: 90.4 MB (90417832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d9f54e97ecf205f2ef4a1c61973f3cb75b9f1d82bc6e244f9ae64a40d14f5e`  
		Last Modified: Mon, 03 Nov 2025 18:14:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:65df137c0154b83adde8b9cdfb423b248e3cc36cf5f44cc3bef57ef46453300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb502156cecefbb0db1e29901af19cc5fd8f1e29914b3228fbc98c5def51c7f`

```dockerfile
```

-	Layers:
	-	`sha256:7e5feffbfe6156f20fba19c6bc92f4f2d2536bac47a16bfff900d36f1dab8e22`  
		Last Modified: Mon, 03 Nov 2025 21:25:28 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e35dddd45b93327122f98395e548e5416c5bb80b5236eabecdc288ae1dbb298`  
		Last Modified: Mon, 03 Nov 2025 21:25:29 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7e2ab9486e1a9ecb75d079ff8f7754f1d7c204c78a3ddfcb24010eae2b33cc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293509250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6838646d980ffa422db3d7fad7e0ade5a429b192c40d33112145146918018eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:11:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:11:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:11:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf804e47683c20db733d9e6818bc93d28616af2adbc4f703221ee8c9dfe09c`  
		Last Modified: Mon, 03 Nov 2025 18:12:00 GMT  
		Size: 69.0 MB (69006468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27665b1ca1f4878aea3b0aaf64c4342038dfeac7ba27def228ea78d9ee8384b1`  
		Last Modified: Mon, 03 Nov 2025 18:11:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:01144710c64cdccc6582829db56153769d12513e2355b30b6922e82125c8ea2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd75720fa4e794829e00cf1019d45cff8560950779af66a52808db0bb1744f2c`

```dockerfile
```

-	Layers:
	-	`sha256:fb15c6d5ee49747949c0812a8c3364d5a3312b3bd9f79b2f1aa5882d6131c72a`  
		Last Modified: Mon, 03 Nov 2025 21:25:37 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99e91bf2876ea15ca2f677c2637eb36c905507943234ed5fa796c91e1cdb521`  
		Last Modified: Mon, 03 Nov 2025 21:25:38 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
