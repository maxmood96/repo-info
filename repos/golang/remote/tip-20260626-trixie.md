## `golang:tip-20260626-trixie`

```console
$ docker pull golang@sha256:0fa761abe74020032a0fbdaf0ccb486f4a4e3dbeffff43a008bf93378f605aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260626-trixie` - linux; amd64

```console
$ docker pull golang@sha256:36935c26dcb75dcdb85fab4be3ed830e9d069e70fc62cdc881719652f66c216f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347607769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1deaf611b32f8d583f59a7eb17144b51cf95a00b8c7810e21b73a649b1f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 00:02:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:07 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:07 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0db852850114cc79598cc8ab1ec19da54691d9e3267288bb3458d7488f125`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 67.8 MB (67778134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a777ba1e9b0cbb3c02ab631c54c21445f918d877a1ae7c15fc5e0020873e57e`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 102.3 MB (102269360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96112613ca74dcaf72b29b75f1686921a6f92c1d50000e911abd31cedae3173d`  
		Last Modified: Tue, 30 Jun 2026 00:04:41 GMT  
		Size: 102.6 MB (102607925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8199e47a70028b9984343191665df9fae065f72c9e3dbc492504cd7de80920`  
		Last Modified: Tue, 30 Jun 2026 00:04:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:761792c9d60095ea3e8b510d1e962496ce6f2714659faf07b8ac9eea19ab4bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2dd88651db3d0bfc6e718070e8f672b726951f8f39c7fe11b309ababf850d5`

```dockerfile
```

-	Layers:
	-	`sha256:9f11e192e68dedad1c474a9539c47bfe3606dcf7be308cbac064e79b96667223`  
		Last Modified: Tue, 30 Jun 2026 00:04:37 GMT  
		Size: 10.8 MB (10785971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc4647307158d5f61ca026b6387679f2c6a12d62b5ff27e4c54ac257b329dc9`  
		Last Modified: Tue, 30 Jun 2026 00:04:36 GMT  
		Size: 29.0 KB (28973 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d4c67714f875f4660d3c6e6ffb6aa69be53ff2bf5208e45abb8b2ff8f182fd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303357759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f7e2e93cd93dced895eb579b4449015f37fde17e0a17d2b737121acf83e36d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 00:03:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:06:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:06:28 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:06:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:06:28 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:06:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:06:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ec13525e08787ad79558c5631e8f1a1fa24a87872974d31cec094e902b73822`  
		Last Modified: Wed, 24 Jun 2026 00:28:39 GMT  
		Size: 45.7 MB (45748717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5391dda58327007b323e3f3d892147e59e5e36215f08b370a235cf10aaf0a`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 23.6 MB (23635872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0beb5aedec8fb711aa9d2285593f5263bc56957c577c835eda5256d1d6cc6`  
		Last Modified: Wed, 24 Jun 2026 03:55:30 GMT  
		Size: 62.7 MB (62746374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fe5ec7b6aba5c5370a426f42c4c351c5477423fac7521cdb88fe96be306cc6`  
		Last Modified: Tue, 30 Jun 2026 00:06:57 GMT  
		Size: 72.9 MB (72912275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea34c6465040d9a03784c749dc96fc02b642a3007f305eb3e72609624011a8c`  
		Last Modified: Tue, 30 Jun 2026 00:06:17 GMT  
		Size: 98.3 MB (98314363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec82fc54b8857791962311c9a1f2470c5222aad3a8ba8ff7e54b6fb66856ede`  
		Last Modified: Tue, 30 Jun 2026 00:06:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2f9a23a05852c8c6ee437473b43163d20a86b3bd67b30b4c05b520b5e7a5e0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b6805fbbb8e940e2aecc8b0626b77b6e527af60a777d36713e9f4e9fb7c9`

```dockerfile
```

-	Layers:
	-	`sha256:c89ee8b79d71288f0f343cd35a501b156cb32a6f9b6446906459d085ef44da08`  
		Last Modified: Tue, 30 Jun 2026 00:06:55 GMT  
		Size: 10.6 MB (10581858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b991066e25b8d6cb39861aa88d127bb799530e60480d920026e48745c3ee4583`  
		Last Modified: Tue, 30 Jun 2026 00:06:55 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:60a37055e7a5d927a39876ac4be2f0d265ce47b064dce3b49a7419fcd94db091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337699232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083c5a82a3ecbc8d26273cf99af0beb93cb4273b87c020c8261c1fe11d8630e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 00:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:03:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:03:28 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:03:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:03:28 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:03:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:03:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf605f6b62a65326644e598c84134d29702579734c83dfca4cedf5dad7fb6d3`  
		Last Modified: Wed, 24 Jun 2026 02:35:43 GMT  
		Size: 67.6 MB (67592645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9ef4c940b574b63e5c11008592cb49dfd2853fb46029a1db5d1b8f6b01a63`  
		Last Modified: Tue, 30 Jun 2026 00:03:59 GMT  
		Size: 98.4 MB (98415235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc19bf506b072ad4aafc8fd4d3064dd82a2aad3673c0290669bfd12b0d5429a8`  
		Last Modified: Tue, 30 Jun 2026 00:03:59 GMT  
		Size: 97.0 MB (96985935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09430abf1ec05b8ea3ebd9059eacab1e033e66a5d49b90e3a0508728b3961768`  
		Last Modified: Tue, 30 Jun 2026 00:03:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f11e557925c1e72de7be86f1b379492fbef62f4c0e53b6c9fe62d5d0262fe8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdcfee7fb4dc4e9bbf9b4d85444ad1330cac594d5ee072a2a314e064b4656ad`

```dockerfile
```

-	Layers:
	-	`sha256:2334dbc834e01d6603544e7af8d5b23cd81680c3f67aa6bd5aece63e2b29d108`  
		Last Modified: Tue, 30 Jun 2026 00:03:56 GMT  
		Size: 10.9 MB (10905789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd71d88acf3883a3d6fa054bd80cd3bcd0970e333c772b63f103af712978961d`  
		Last Modified: Tue, 30 Jun 2026 00:03:55 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-trixie` - linux; 386

```console
$ docker pull golang@sha256:3685d04759fea112b858229a09285c4d66b900a9f14328c1b3011f802407519e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348555205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aeeb4be1271240bce98dc7a26f7bf587b26aa483d5911d593ef3bf51c06cb8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 00:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:17 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:17 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae12c2ff3fb5df23b854f2a97ab858f54bb2f71491a9276fddf8be7e76d3182a`  
		Last Modified: Wed, 24 Jun 2026 00:28:34 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429f3d50e84943497f0eadc90e14107210f6f5e2fba29257d54a1c7858400bdf`  
		Last Modified: Wed, 24 Jun 2026 01:44:16 GMT  
		Size: 26.8 MB (26797404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296cd1d205c61c3d8ebf0c638f588eaec576bb036a91f5b50f8b6183fc3010e8`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 69.8 MB (69817498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27caa07c27bc4f3830fad31cce6baa28ceb0f45169219ea15a51ed92df1f49`  
		Last Modified: Tue, 30 Jun 2026 00:04:50 GMT  
		Size: 100.7 MB (100710798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe287f4fcc073ba1e90b598305ae90f45e8a3339ed6d99366e8996528c1a25`  
		Last Modified: Tue, 30 Jun 2026 00:04:49 GMT  
		Size: 100.4 MB (100393692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340b014a938aef0616c424746dd1a27d520e1d5dfae1f909d2f5b4afaf8a0bdf`  
		Last Modified: Tue, 30 Jun 2026 00:04:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7a68f047f5d80b466a96a5da875b42c009a3262b6920ea1c5e0e082e8cea655f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3835f8b87e4a14d360182ed8ea54569772bdc9c2bd8c4056aaa7d1e367c958`

```dockerfile
```

-	Layers:
	-	`sha256:371105b0c32f472b926c8444b1b9e164dadee0431f762fc8583738e2e002a7f6`  
		Last Modified: Tue, 30 Jun 2026 00:04:46 GMT  
		Size: 10.8 MB (10757234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c164c739c727747630b0a154116f3e53a3a626240bf906090f302e492e475443`  
		Last Modified: Tue, 30 Jun 2026 00:04:45 GMT  
		Size: 28.9 KB (28930 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:8175350c24867ad664ff69bfb95f053bf21ff9fc320d69c7a96cba83d4605139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345148906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b53512347bb05e6020bd76fabd4ef68fc7cfa041840927d6d7bcb128c486f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 09:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 11:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:54 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:05:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:05:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f80d2a3204cde8ea1e7cf5156c0b0e385216cbdcc894bd75c3d81ec51271e`  
		Last Modified: Wed, 24 Jun 2026 03:26:58 GMT  
		Size: 27.0 MB (27022027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d839bd23ba3483deaa2fe15c35bcf5914f88e1187bd81dc630463eccbfa83ab`  
		Last Modified: Wed, 24 Jun 2026 09:11:50 GMT  
		Size: 73.0 MB (73042732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ed5e38143201332b94deb1de4d86e0ea7e941dbc7b5d2be2a83cc8b919f4fc`  
		Last Modified: Wed, 24 Jun 2026 11:44:51 GMT  
		Size: 93.0 MB (92976176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea8767a8a0a93030114399f1f19e8f448718e14ab3c948bcc8dac1be9cf2f8`  
		Last Modified: Tue, 30 Jun 2026 00:06:26 GMT  
		Size: 99.0 MB (98969745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec822c00916a11e41a267fadc669fdaff526bcb2060422f2589032021aba2b2`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:07e1c3f25006f7355c2843e1835a3abd38f35b2ae1ad197ca0b9fbb576a5b56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd54e2f2f291a81a4fa4a64efef1d60e2487fa9b700e6b60e52223d6bef9a47`

```dockerfile
```

-	Layers:
	-	`sha256:60913fdb5f6e3d51208cf83edabcef9876bde99e3e4fe95d21e93cf6ef680922`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 10.8 MB (10781759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af145e2b8431d037a2cb411686a6c3822454007e554e7eb12dd6243d83478450`  
		Last Modified: Tue, 30 Jun 2026 00:06:23 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260626-trixie` - linux; s390x

```console
$ docker pull golang@sha256:c529b4dda28f19a2efb3ef06ebda2b664c52a45f8a95a2ecd638db8c429bd36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321960707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d539cb9865a59cc19a14d04474328ecd4c15d5d12b842a04b273697039f3ed80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 00:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 00:04:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Jun 2026 00:04:48 GMT
ENV GOPATH=/go
# Tue, 30 Jun 2026 00:04:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:04:48 GMT
COPY /target/ / # buildkit
# Tue, 30 Jun 2026 00:04:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Jun 2026 00:04:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ad8b668881e5b88baa7f13010c93f1bce4021cd7e873db608fc3d64c83f78`  
		Last Modified: Wed, 24 Jun 2026 02:46:45 GMT  
		Size: 26.8 MB (26803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2467c361ab8894fdba8935a4c045eb8f691562f8d8866636ae12b0e066b40329`  
		Last Modified: Wed, 24 Jun 2026 04:30:46 GMT  
		Size: 68.6 MB (68645672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba01797f0882bd2be0740120045ce9b50fbd82d27178b77711fb50a54069397`  
		Last Modified: Tue, 30 Jun 2026 00:05:32 GMT  
		Size: 76.1 MB (76080732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdf657db5fc71df443dbbc81704a25107962ecb9a4a8f16c3715658947e80b9`  
		Last Modified: Tue, 30 Jun 2026 00:05:12 GMT  
		Size: 101.0 MB (101044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cc61c084399c283751f4a29ac861f35d6e95d46dbad69ff04a954a8d3a942b`  
		Last Modified: Tue, 30 Jun 2026 00:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260626-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:97fe7b51364a6110b4ff74e20a2c13d58680804d2e00142cec75511a2c59683f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc382f2ea2a70cf43be650f8bf25c6dc3c13c8cbfc2cf556b66fb50d5588ef9`

```dockerfile
```

-	Layers:
	-	`sha256:408c959bfd5d5d41e89cefa1848796e332d72dd9a5d6739c5f20834ccd4eff16`  
		Last Modified: Tue, 30 Jun 2026 00:05:31 GMT  
		Size: 10.6 MB (10597119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bddfb20a69ed617bf01598fa7c68819a28406dfe597301d0064a2c2be7fd72`  
		Last Modified: Tue, 30 Jun 2026 00:05:31 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
