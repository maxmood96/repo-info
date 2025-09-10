## `golang:trixie`

```console
$ docker pull golang@sha256:5d4aa31f5376306d310fba62e962c564c9986c1e3853b5867432ccdf3b815838
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

### `golang:trixie` - linux; amd64

```console
$ docker pull golang@sha256:9c0c9e535601de9c1dd1e8a4dddbce5830359782f700291175ca47c1ef1a6e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304787553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417bce5853d5974dc6738af12ca64ef9d3236a8f6102f19f16d1825bfb76972c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:1c315634bf9079ab45072808dc1101241352a3762e0bb1ec75369a0f65672ab0`  
		Last Modified: Mon, 08 Sep 2025 22:39:29 GMT  
		Size: 102.1 MB (102071864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ee02be966963d69210ed8243baa8f322661858bae69d1c2d5d13fe4dc92ba`  
		Last Modified: Mon, 08 Sep 2025 22:39:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4c734f9ccdb5ff98810c1f1d677702fd85e2ec9f851925038e7b1b61e7bea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc6c57fe15c0e81ea8b2b7486c40f110afc23fcbbe254f4c874bcafc92ff784`

```dockerfile
```

-	Layers:
	-	`sha256:7d768157506e220ac5f0f21a290ab48689bd0f0595c694ceb4edcac926ab2821`  
		Last Modified: Mon, 08 Sep 2025 23:22:27 GMT  
		Size: 10.8 MB (10784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a47fbe0254091199a45eaa2b62d7e4320b97dbe93570993a93aaae3a67ed87f`  
		Last Modified: Mon, 08 Sep 2025 23:22:28 GMT  
		Size: 29.0 KB (28996 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:73e34c9994d2257b83e213f2b9f4b91d8aceaf07f58ca07d9e4a81bff52ed077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263740827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2122886a933c7eb6c1d627596ebf69511b5ca524f3e57c9dcd4a8bdbb2c935d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:801f62404fad4539bdb87044903458f0826f3095ed6666d0566f7cd4de544c4c`  
		Last Modified: Tue, 09 Sep 2025 07:10:49 GMT  
		Size: 72.7 MB (72717144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2bb1f595dde7284f1b328ae116b47960d80d852b34ac7c04e556e122cad126`  
		Last Modified: Tue, 09 Sep 2025 06:27:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:da21cde4b25557bb7f67c58aa4c493fcdb6ea43663845636fae346e07ee6d446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05f982b7d7139ac4b224a5cb291847283a2ed4d052163684eb5ee2bdc6f8937`

```dockerfile
```

-	Layers:
	-	`sha256:da054f0aba4c02761705c57321e0dddec8db1a2897d23302370d160514c33a84`  
		Last Modified: Tue, 09 Sep 2025 08:22:36 GMT  
		Size: 10.6 MB (10580247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabe51898cb5004f5c748b6d1a7b7dc1f22b5d5fd3dc12aa164565e5955628d9`  
		Last Modified: Tue, 09 Sep 2025 08:22:37 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:739770e153fc630f83791423e0bc213fef46e6d25420f2df61d00062f6dca7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298016005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be0d2f67cae5ca4f622fc3deccdd754d8eb5a6d2f9034474a29f01c69470439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:f15d40c2dc72fc622c663b60b41c630deba5e76f8f49e48e1778c5853390b39a`  
		Last Modified: Tue, 09 Sep 2025 03:12:25 GMT  
		Size: 98.2 MB (98218179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305f4a85377aeba9757d958fcb1a1eeedb04e03dce9e2e52615b678166d4fd2`  
		Last Modified: Tue, 09 Sep 2025 02:49:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:24b81792a5f68198e17ddb0da198eb5bd7f795f29d5e447884607026620bd439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61f6af905eb0fc56e1ee9544f7dea718a0415cb546d75c814201c92f9df7270`

```dockerfile
```

-	Layers:
	-	`sha256:ee64ad8a651619f4bbb8ff6f96837cda424bc22e1538ceaa84a32b3fb850c5d8`  
		Last Modified: Tue, 09 Sep 2025 05:22:35 GMT  
		Size: 10.9 MB (10904829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9290e83b7f7551c6b0e88f16eb5c4337e7ca25a282240ad7c7d2d6bc1f7a2195`  
		Last Modified: Tue, 09 Sep 2025 05:22:36 GMT  
		Size: 29.2 KB (29174 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:757033aaff47d764c57e9a0c0f04f2fda9960539cff3588d46416933a6480157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306643757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae059e64211de99135055c28f1c962691884e1a72b6462169fefb0fc21852afa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:1eefcad9c736bf257328a528bcf28801a5b86020d749062daf4b6c126a1a595a`  
		Last Modified: Mon, 08 Sep 2025 22:39:32 GMT  
		Size: 100.5 MB (100516836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8134730600d4cfc74c5293aacb74478de1de4810632b08ac46dafe23f69bbce`  
		Last Modified: Wed, 03 Sep 2025 19:04:05 GMT  
		Size: 58.8 MB (58764049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e23bbe0517a0617a2e2694315bfb0600300b10126c97f7df8459b1b84dba56f`  
		Last Modified: Mon, 08 Sep 2025 22:39:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6aae4bca8af06f901eeb824aabd177398780ba095979224e7e60dd048fd7a06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145b62a759e7c0d5adc53983b55521b1ca7feb6e56a496749e6c4eb84b52374a`

```dockerfile
```

-	Layers:
	-	`sha256:1a8c348dec43587a3e72dbcabdba36b8fc7cdea8e3ee949c0ca8d10795f36cc6`  
		Last Modified: Mon, 08 Sep 2025 23:22:48 GMT  
		Size: 10.8 MB (10755572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84f36ab7b87aa492eb736a90359cd00d72b5242ad6cfa33f0708e94910b172d`  
		Last Modified: Mon, 08 Sep 2025 23:22:49 GMT  
		Size: 28.9 KB (28940 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:c1f2f56301eb1e6514ecac25a14aa59974bcb2024a083d2394d3162c8c9261db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303946737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59c5cdc94faf17ce9c07b9a1ea10192086a7f6b197b72e60df727a8b67e846e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:2782245989e82f9bdf3f30b697ffcf7ba53b44245a4f85508ca455383c3b5b8b`  
		Last Modified: Tue, 09 Sep 2025 21:53:05 GMT  
		Size: 92.8 MB (92778482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab050f02485e9e591cf2d38532d3b9a1b2f56a6a7a89953f8620b4559ad2910`  
		Last Modified: Tue, 09 Sep 2025 21:52:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b79b52869edc506f3ff4e363987912470e305ef6148915abd3ef9713805888c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb2e423695b9f52fdd7dd1f82f71e0d05920ef92320a6ab8fa8589eed3f5d36`

```dockerfile
```

-	Layers:
	-	`sha256:d044f33fb5aeab0af9f70a55a4ccb183944166db8f236f6a30e60806ab372aaa`  
		Last Modified: Tue, 09 Sep 2025 23:22:52 GMT  
		Size: 10.8 MB (10780134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c6a3cf836babd0ffc632d05b5f8cde1b5f9a122a604484f12e25a705e07819`  
		Last Modified: Tue, 09 Sep 2025 23:22:54 GMT  
		Size: 29.1 KB (29064 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

```console
$ docker pull golang@sha256:6d19652b3fbbbc22b9ee4d585909ee98775b7894b0834107bd58a20bd6fb21fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329488175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036a329c9f50b513dfd38bcd94befd5a52bcafb461537864b30894898902817c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0b64daccd6b787f78c1a1622c08097763f53e2dee005bedbf3141bbaa8af2`  
		Last Modified: Sun, 17 Aug 2025 07:49:06 GMT  
		Size: 66.7 MB (66658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633618253f092f4a4acbf99fa7a220a8363959887159df8b8feac3518e23d810`  
		Last Modified: Mon, 25 Aug 2025 01:07:47 GMT  
		Size: 131.5 MB (131541938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41271712fdf69bbd5435fcdb57d1cca7c9114e983cf470cc61ed6e9d72e6a385`  
		Last Modified: Fri, 05 Sep 2025 14:47:51 GMT  
		Size: 58.6 MB (58572885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1bd5de98a23f9ba94d04f7adcb3379acaa366e087c5c7d791e4e581fed28ac`  
		Last Modified: Fri, 05 Sep 2025 14:47:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bc065b1f670036522a8711b47a5fe9de3faf1879c516a7d40a691afa4ff7043f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57527bc7f641df8a6d714b23cfbf393945d24070e0e41a3f29cb3644e54e6f9c`

```dockerfile
```

-	Layers:
	-	`sha256:d79385b84e72adee00efec7dc7ce18e61c11999d9d568e47cacc716621ae10b9`  
		Last Modified: Fri, 05 Sep 2025 17:23:01 GMT  
		Size: 10.8 MB (10849343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21e42578c9f68a247e58cda84cf9b6acb2b6585b58a218d628a13269b29c1100`  
		Last Modified: Fri, 05 Sep 2025 17:23:03 GMT  
		Size: 29.1 KB (29068 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:b2d7f6aa0794e1a95bdc5d5f015cb62640a5c8a249429a4d5e14ae12de73795d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280025108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82d8950b10a6a443c3938033e7a721376d58eae8e2d835451cd31c6a4dcb1f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
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
	-	`sha256:50d9e119d66f705cea108e7054879c3d8408dc2e03d0268a41dc071faa0643e6`  
		Last Modified: Tue, 09 Sep 2025 17:35:53 GMT  
		Size: 75.9 MB (75884036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af48389d563ccb39441056114ee8bb4fefdded621ed594eb028cdf9787ad997`  
		Last Modified: Wed, 03 Sep 2025 20:23:25 GMT  
		Size: 59.4 MB (59378188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a985312c36484d649b8d5cc10443aca4c43bee0ceb7c7d6cb7376dff12be425`  
		Last Modified: Tue, 09 Sep 2025 17:35:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:137e91a6fa11bdb3a08a86f4be0866f2abe6f472eff5d2f699b28c807677acac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4753c150e4eaa4d827698c515904846524b6bf23fe03ce5e3cf9ca3205f678`

```dockerfile
```

-	Layers:
	-	`sha256:64c55c2ebf9c6709480ed93237c63f0ea9d0a2471cc1a8a07f81febfa9a2861f`  
		Last Modified: Tue, 09 Sep 2025 20:23:01 GMT  
		Size: 10.6 MB (10594726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e6af195e8b43c9e318ea34f324771248149dcaa3c50deec46a176c618c6aed`  
		Last Modified: Tue, 09 Sep 2025 20:23:02 GMT  
		Size: 29.0 KB (28992 bytes)  
		MIME: application/vnd.in-toto+json
