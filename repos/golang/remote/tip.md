## `golang:tip`

```console
$ docker pull golang@sha256:9fdf2690f1e769fb871f043e0a4259932b17a3fe542c84d6ae8be6360929dd3e
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
$ docker pull golang@sha256:b61bb7ebcfbe6c9f95c424a280e37c1e568b495415917d64ac032a53a65563c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328427338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4293347eaf15f779a2b8d2c3bd1d8cfb27734f1014fb70ea3a4b4fc28a67ad79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e30b784c3126791d206f9599b4af53b6eefd56a87c26692eb1be04cb57fa7`  
		Last Modified: Mon, 15 Sep 2025 21:12:44 GMT  
		Size: 102.1 MB (102072088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8084ae79718311fedfafbc5a50335db8ff6184359260f7408a58117f5eecec`  
		Last Modified: Mon, 15 Sep 2025 21:12:40 GMT  
		Size: 83.7 MB (83685170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6101884261fde8df1a4a6739974efb0d4b4a693641095fa94de12660c8723a15`  
		Last Modified: Mon, 15 Sep 2025 21:12:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:856d3c69514b6b83a7694181edadb25311b4017487cdb9fc510a5e71caa2e6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e249da9dedbb2b96611b2c8d3fcb79363ae1c0c3b930f9a576cce32e446dee47`

```dockerfile
```

-	Layers:
	-	`sha256:3992350470a20dc6e77fbb5fdb20ebb9e8f167698cd1203b335e50e9368e875f`  
		Last Modified: Mon, 15 Sep 2025 23:23:33 GMT  
		Size: 10.8 MB (10782934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a1262a795ffd4a6fd54e5af9dc4d25fc3fad015d12b4d37657661afaab467b`  
		Last Modified: Mon, 15 Sep 2025 23:23:34 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:5408f61a41e70850a22e69e516285083203390135bf6122c72ea18f92ca42a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285494618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c2d9425da0e8b6d9eb7357d0a22d0733ce6dd184a555033aa48de5e57c4dd0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f6e94900330a04b307ffe12bcaec67fd2a54043ca5c4579326450c98004576`  
		Last Modified: Mon, 15 Sep 2025 22:09:37 GMT  
		Size: 72.7 MB (72717364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b987a50b9955c225cc2849c41b467e101fbe92c91e3dab2be8fb2645bad265`  
		Last Modified: Mon, 15 Sep 2025 21:13:14 GMT  
		Size: 80.7 MB (80731747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0934b43fb3ab7e04e874d17609e032ce2f89462f774520f2926622443ba83e`  
		Last Modified: Mon, 15 Sep 2025 21:59:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:81461e921b1fe4fa151c00c8b13cff86ad5e3e45dfb0c908d133857763e6c023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10607957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1eec4abb02c59147bce60b506d3af817222a3f74fe2fd0ce9fd12356025a84`

```dockerfile
```

-	Layers:
	-	`sha256:c6c1e18baffc703b742c3748b580c6445cf87f3c1cb7d95335f3a8328abf49ad`  
		Last Modified: Mon, 15 Sep 2025 23:23:43 GMT  
		Size: 10.6 MB (10578823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf631252825b3ba84216de28ebb1e18d9ac9a89c2fe7eb5540e127c79c930d5`  
		Last Modified: Mon, 15 Sep 2025 23:23:44 GMT  
		Size: 29.1 KB (29134 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1f588f6525f15268031afa2b1b62e4d39658860dbf97fca68662ff98a33a5635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320139247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edda88a13c7f2e963ef0e9007465a6064a2c83ea9e8a5fdf300ed123d429a264`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b188073c073431ca4cc05d7005317dfff5c773f2074870345a7cdba3f538418e`  
		Last Modified: Mon, 15 Sep 2025 21:12:12 GMT  
		Size: 98.2 MB (98218155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a2c01c0918250210240d30defa285fe0edf22dfb1aaaf2291b5e92b61a74a`  
		Last Modified: Mon, 15 Sep 2025 21:11:43 GMT  
		Size: 79.7 MB (79678746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1af36b6d0d05230b8cace5c851e1785398965fc9249d0ddfe124a749dc3ebfb`  
		Last Modified: Mon, 15 Sep 2025 21:12:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a6ca93ae3e1ad4a13d2ea73fd31b22f76402f1a8822dc4c8f5527373335c27ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10932556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1176f9458c42825744f7c4b8d9bd465af1f7bd1348f18db64c2e60cc3cec336f`

```dockerfile
```

-	Layers:
	-	`sha256:c1e20abfbf4a9277e8a9adece852b2f357024e2996b80f038a6630c7f2890c3e`  
		Last Modified: Mon, 15 Sep 2025 23:23:51 GMT  
		Size: 10.9 MB (10903389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82dff2792b52e62606fa6420a00595a7f7235364fff5afc742406dc8f00280e9`  
		Last Modified: Mon, 15 Sep 2025 23:23:52 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:61d2352cb80235bbc5e43acb95caae17ceb1d164bcc3daae53b6888a0ebcc345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330252106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc8da069424863997d0366c2f0f74f11bb827f685f6784afc91e700f79a3a06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4adf19bf3e6f542f3c00d3fc4bb83f2ec48ccc9675502c518d9eb368d0232a`  
		Last Modified: Mon, 08 Sep 2025 22:13:48 GMT  
		Size: 69.8 MB (69794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd6865a0489e0714e17fe2221e786d1e59a7b329d5cdc9c3abe7ba39e741ee`  
		Last Modified: Mon, 15 Sep 2025 21:12:54 GMT  
		Size: 100.5 MB (100516841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2aca1e976b6789d4066cf350d8d9b9afb301f494e0c2483f001f1e2c4a7034`  
		Last Modified: Mon, 15 Sep 2025 21:12:39 GMT  
		Size: 82.4 MB (82372393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccabd9c2e0713975086f0e770a542484601739935f013b1d2c61cd6d16313fb8`  
		Last Modified: Mon, 15 Sep 2025 21:12:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:517db9a66d802354d2eff4d7b3bdb663a5275b4fd600a149458a42990aa7f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10783169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2574ab49c113dffdce728d03e11147fe6f71c47b1e4e78780bfd2fffe0354a38`

```dockerfile
```

-	Layers:
	-	`sha256:68e5f1b2405cee5b24e646bc59f43b6a5af5ab6439839a3990033b9bc1108688`  
		Last Modified: Mon, 15 Sep 2025 23:23:59 GMT  
		Size: 10.8 MB (10754200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e13f7edfed58ddb491f234e58675899eb6256a4d4a836eb54c33939485a4e38`  
		Last Modified: Mon, 15 Sep 2025 23:24:00 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:371d1ebf1e714dd40032311b07144531de3b7bcdb13be455084aa86448045a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326949313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f99da479e0dc61753c643bf2a741744c1a18b7bf7ecde850df0e4eaf68d040d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77bc0ffff5d7f31b9325d826f76add9c63b94cb3a06eebfb5bb1f541f562407`  
		Last Modified: Mon, 15 Sep 2025 21:15:44 GMT  
		Size: 92.8 MB (92778794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb324782f5e8e3887f0d55cc6908c033fff6444770b36972445edcc39d815f`  
		Last Modified: Mon, 15 Sep 2025 21:15:44 GMT  
		Size: 81.0 MB (81038429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab14476a3f5acd9f3727438b294c7736dab29bbdc57a000a48f9964e8d33e8ef`  
		Last Modified: Mon, 15 Sep 2025 21:15:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6387553f54233b6e53a38d6ad63ebaa3fff8a0ea05ae3f4ce484783a8140f682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c416e36afaaed7dc8245c81f761684987b5bb50b23520f990b9ce752632e14`

```dockerfile
```

-	Layers:
	-	`sha256:d459d30ff23814c9e59b488a863d5c47c770babf475f4f429081060beb77dff3`  
		Last Modified: Mon, 15 Sep 2025 23:24:06 GMT  
		Size: 10.8 MB (10778718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289a824cb4b9082d830f6c789b1651d269408b52509b86a5671e1dca868d0741`  
		Last Modified: Mon, 15 Sep 2025 23:24:07 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:d89b2f9b7d33343eee0bc9974a9ff7cbd9a6e18476deae8e5ab37b0caba0d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351985636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1940f609d48bfd78052d08aecfedbaef65e286813c588e59e33a5d3f7989c508`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1afb27b72dabce7ba373ba8319bd1ccd2205d7724f23909527bd3da7476b1`  
		Last Modified: Thu, 11 Sep 2025 01:43:59 GMT  
		Size: 25.0 MB (24952790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32856986223852ec3f854d1a7c152bc97555c3c9e06114ce074d65dc96a8dee`  
		Last Modified: Fri, 12 Sep 2025 02:24:28 GMT  
		Size: 66.7 MB (66660361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ccaac1efde5b5edf5e06fc7214fdc1986a9341055511d69b9c3f5e789f783`  
		Last Modified: Mon, 15 Sep 2025 06:09:44 GMT  
		Size: 131.6 MB (131561217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829abce40c6e676411d0af62b8c004ecfb77ea108ba2632a87a5640426b84be`  
		Last Modified: Tue, 09 Sep 2025 09:50:53 GMT  
		Size: 81.0 MB (81045663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4e8c28257ee0925f22ca025d5b3488d90a2f3e76a04643566955326fcdd500`  
		Last Modified: Mon, 15 Sep 2025 08:30:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b803594c84a24a37a6356564528fc36696b24a2cf36fc21d98db7c0a98624c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10881621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed82655877c89eab38a1cb6911dd6b985b88a9671fd0043bb8dda09bea8bdf2`

```dockerfile
```

-	Layers:
	-	`sha256:6d4bfb3f5f756a87c65fb2984b92154b149b89ff9557f025439aaae1d5c38180`  
		Last Modified: Mon, 15 Sep 2025 11:23:45 GMT  
		Size: 10.9 MB (10852551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80f041459ee363171c3f5b9a7faa1e5bdd8ebf8b7ed211e6ca30a1424c901da`  
		Last Modified: Mon, 15 Sep 2025 11:23:46 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:1ab8eb307d812d7b8791298c9d7ddc4172bb81d8956ac4a0ac97934f64ab13fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302904630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e47194680781a0adbb8d603a9c87012b0a8506dbfa700476e84568210dc73e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a39cd1cfdc3ff7bd6d9eea04725dda8f73ff83159d133cd556b4ba6a9ac85d`  
		Last Modified: Mon, 15 Sep 2025 21:20:05 GMT  
		Size: 75.9 MB (75883664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59bcd7ca863be9aebc61665811bb8814298aa2a6542f87325c4770560068944`  
		Last Modified: Mon, 15 Sep 2025 21:20:05 GMT  
		Size: 82.3 MB (82258083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21eb7fba7c09b4a6b8ae18db0f5e4b993f2e8c97667d2b4ae334c1f9bf88325`  
		Last Modified: Mon, 15 Sep 2025 21:19:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9a28846971c76b2308dbb278683f1a4d58acfd6c270d50fddebffd1c8b249017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10622341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2839cc7f1d9908acc6e8293abe4e5857935f431ead56e64ecf91f388de5116`

```dockerfile
```

-	Layers:
	-	`sha256:e7321bd3529f4045a5e7c11e8a31c6637d57e3b6598a3c323f31efc5b673846f`  
		Last Modified: Mon, 15 Sep 2025 23:24:23 GMT  
		Size: 10.6 MB (10593334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335507e6977836d30eac3eb55ca4c0969497ad6e3207cba73149ecab2b651e36`  
		Last Modified: Mon, 15 Sep 2025 23:24:25 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
