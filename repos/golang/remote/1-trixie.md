## `golang:1-trixie`

```console
$ docker pull golang@sha256:3c390549c3dff593d60160a64aeb6b1406232134752d499ffd7fb2e0e405358c
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

### `golang:1-trixie` - linux; amd64

```console
$ docker pull golang@sha256:49f8228cebc91ccf30b2380adb5cfe2d8a5f99fc8f3447e0b6c5a2f9d052d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312222222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae58b994b75be86dbc32beced14e682ed3b3600cc49ec83af0520c8a7dc269d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:36:58 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:36:58 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:36:58 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:36:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:36:58 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:37:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:37:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1df302ac819b7108e83e54c9807ddbad20062015a274e0964633ae316700cc3`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 102.2 MB (102222350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca432a5dbd5f0346230d26557fc3018aa0e515bfb6901a3db05a146470631e89`  
		Last Modified: Thu, 07 May 2026 17:37:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c80fc07c05f88d3fb07dc716e483819cf83d23a0dae6f1fca91f1fc46ae6e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff307b3f692f4cdab639bcf330d96740a25cf3fecbba6c28dc37841ca50f18a`

```dockerfile
```

-	Layers:
	-	`sha256:02584a28adde91e1a81ea5f61089be5956645c6a6e305ac79db87e1601149949`  
		Last Modified: Thu, 07 May 2026 17:37:28 GMT  
		Size: 10.8 MB (10787103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c447ae0892fb2172d66ffd933d8efd1133a4cb060394040fb9c0e6b7fb9f2b3`  
		Last Modified: Thu, 07 May 2026 17:37:27 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:4c51c8e7d02ba8627a70486cc5ab3830ec2b2b37e6873ba81fc77e8c33d927ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270652405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b8bf02892ef66e0c032d31d243b4415107c8dc964896bfe8c8aa5855c68f14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 04:15:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:15:18 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 04:15:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 04:15:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624b0aa4927ac16af36086312095e6ed3b14f62fdd3e3051375e01f62b46df2`  
		Last Modified: Wed, 22 Apr 2026 04:15:51 GMT  
		Size: 72.8 MB (72805007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c9db2c2e213532638f94b4cfaad98960ad1d0f0e36b1f944691e81cc1ad52e`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a8f20c21c5ed109d8e740a3948b286596d42e2b909452139384665bcdbb1081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ed4e59cfee33d3936c185f05adc9a73a447f39b62b3bdece425754d0aace7c`

```dockerfile
```

-	Layers:
	-	`sha256:a0bd4a4da5655cd0b06c64e0f3a7047a5a7e1859c28c3be2f4b68128c4f4aa9d`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 10.6 MB (10583022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d343bc3a02dcdb385b8d899e318b5cba75f08c3c5cec3795b0e0999a5ba7b8f`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f4f6456b04a0bc04e4349eeeb6427f599befe34b3f57348f37b7c55a85fcf1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304812107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e573195e1fe719844054ceb6c4a5e2a91c7503b4ee4a667dd7403864eab6176`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:42:14 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:42:14 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:42:14 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:42:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:42:14 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:42:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:42:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcf22333c3abdf4717294942a9b600cc52e2aabffcb47b0b3759041406cf8a4`  
		Last Modified: Thu, 07 May 2026 17:42:50 GMT  
		Size: 98.4 MB (98366777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c5a499e9e7f109b0f57e8b0dc304d74c6a52a903b5b77ffc8554559b12b4c`  
		Last Modified: Thu, 07 May 2026 17:42:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0897daccda81e89cd6cb98bc883252e1c398db5bfb8ac9fd53834f862583ef2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e125a4f6f0e488cfaead43bb020ce98393231cfc310824e9a1046759fccc25`

```dockerfile
```

-	Layers:
	-	`sha256:0104a7e2fc2603ec1bc8e5d0469c45ecef23bc8120215d481c35f4c63312b732`  
		Last Modified: Thu, 07 May 2026 17:42:48 GMT  
		Size: 10.9 MB (10907606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c313a86e9e411dec4c3741467e76e22bad48efcedb61e49bc75d124a04d1aa7`  
		Last Modified: Thu, 07 May 2026 17:42:47 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:880777fc321a949ff5f7c809f13582491bba1daa94a17068b29c02673121573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313684055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df50ab262a4582b628b88ef90edeb2bae8f724b7d5b118eadc11ccc9abfa0846`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:38:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:38:04 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:38:04 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:38:04 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:38:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:38:04 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:38:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:38:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cdc00799a2a5d425863c783516cdc5139f867d081df458a78cfa749e9d7c3`  
		Last Modified: Wed, 22 Apr 2026 05:03:55 GMT  
		Size: 69.8 MB (69809793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9e8fb8d9fb07a2c97bf5eeaa727828449fe80624d235bf7a8e3d383088007`  
		Last Modified: Thu, 07 May 2026 17:38:40 GMT  
		Size: 100.7 MB (100664764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc861e80d12107db88f4c916c85454bafdb806c3211bf15cd18b7dbb83e91a8`  
		Last Modified: Thu, 07 May 2026 17:38:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a8648dbce2942b8ca9d5f5d1f9b3283c05b1dfc99c64e2c724f96a0795483048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009b998c7b7c01f9cf5f09aae3d7db9ef914be5db1c72095dab79b5b0249afeb`

```dockerfile
```

-	Layers:
	-	`sha256:26c905fb9cea6daafb343d49eead1637310177d82f3014545ca6b10926f483db`  
		Last Modified: Thu, 07 May 2026 17:38:38 GMT  
		Size: 10.8 MB (10758346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2682b7a0a4fa8246410a6c4def57522373313bc20f03413a50dd8c582423a93d`  
		Last Modified: Thu, 07 May 2026 17:38:37 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:4e6c36a09753a467a0d091ad91679c42bdfb01b8e13e1ae525017f4c919dbe59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310806054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7782cd50253089e2f9d6c98c356f77f7f1d9ffc7aa5c180cbc162142064ded`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 12:18:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 12:18:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c23c6f714d67ed8764658fb449b29673238ba8266bef7c97e4c3990f4ce88a`  
		Last Modified: Wed, 22 Apr 2026 12:19:37 GMT  
		Size: 92.9 MB (92870840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08dc199358ee2431a32b4768a140aa4a93a36b209b06f3fa1d6064c90f9ccad`  
		Last Modified: Wed, 22 Apr 2026 12:19:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b04f23ec2c2b481b2f4d634a8e76d9eb1087b42ce29ebe019467aaaa1b84b074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12daab035c52644e7614c1993b667829731e21a364b20ab44368881f7652c95`

```dockerfile
```

-	Layers:
	-	`sha256:df31c87d84452a044c34294118316858daf87225ac0264acdf10491fa201be25`  
		Last Modified: Wed, 22 Apr 2026 12:19:34 GMT  
		Size: 10.8 MB (10782915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7246a485182f2fdedf877014bbd2ed7b1906544a8e9c4f77b275b607783972e1`  
		Last Modified: Wed, 22 Apr 2026 12:19:33 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:8bdccecb00ee4275c285a8a37a24d13d18a3c9e7d6f536552e76b14f311a02e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336145995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8411e919e18d1dfb8f6e85afc7961b791d7624547386dc884802ceeb0dbfd72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 20:31:10 GMT
ENV GOLANG_VERSION=1.26.2
# Sun, 26 Apr 2026 20:31:10 GMT
ENV GOTOOLCHAIN=local
# Sun, 26 Apr 2026 20:31:10 GMT
ENV GOPATH=/go
# Sun, 26 Apr 2026 20:31:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 20:31:10 GMT
COPY /target/ / # buildkit
# Sun, 26 Apr 2026 20:31:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 26 Apr 2026 20:31:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954c4b6ce8f364903d1d8a7ac953d1cbfe6ecf95f3d8c267e0b27a58b6e61bc`  
		Last Modified: Sun, 26 Apr 2026 20:39:36 GMT  
		Size: 131.6 MB (131649887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a30bc4c784e8d92172532942a10dbab8ed4215459d8b93026e0e905719bb35`  
		Last Modified: Sun, 26 Apr 2026 20:39:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7eb1ee1c02d0345efa486ab5585f2ebc0dec86cd303bdc336cd7b76fb1282406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1f12b6c367c82a7fd33da3a35c18ac62b18a2fa81d1dbb1704e6d19d5e9346`

```dockerfile
```

-	Layers:
	-	`sha256:a0ebad59020dee7b23e00789b751a84dfc15d03682e7750023686f5b354a5ffa`  
		Last Modified: Sun, 26 Apr 2026 20:39:19 GMT  
		Size: 10.9 MB (10856748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75476c94baa6508bc82cb6ed5420dc51fdbf317446ed830ab376402333dcbeb`  
		Last Modified: Sun, 26 Apr 2026 20:39:15 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:3f44033286f04c0b1488b9e19b60d550bcd54e9d201b61657f2fdc1fff21500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287225591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81e63f22061f2218ac5097d7438454e0a66d0f6306b9aa2fbaa9dbf3ef241d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:12 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8027314e609c53cba98fd110647ae82f15ca5a14a5ca8b1f7f0efac414d3719`  
		Last Modified: Wed, 22 Apr 2026 05:15:27 GMT  
		Size: 76.0 MB (75981818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c2e1ff04fe5ced2f859f0fa7e592143f21967e1554851814be99c86671e778`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b422e292d58e2a28a79f7b55a76b24213c54834bf7e9c10c7bb71f1cae2812d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711efc5c86a93c7b6c58bffc80dbce2e52a6d217d8856aaad21abc3b352d3fe8`

```dockerfile
```

-	Layers:
	-	`sha256:aad6b17d8f7c5af42fa77014326d90d7a180e8647686cbef532def29e14c5981`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 10.6 MB (10597503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5987e2da20ea0e6e6cb950fbe2978bb4d1e5974725a28803227f48e5c38591ac`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
