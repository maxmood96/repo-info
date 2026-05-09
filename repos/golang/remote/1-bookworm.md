## `golang:1-bookworm`

```console
$ docker pull golang@sha256:54f9adee34a50b158bc58658902690689583a9a43a4a54160c937f05477104f3
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a567df5a098a72d98eabf2f123479fca825d47adfc67b14c95a4236ac28bcd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296693025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77083f2b8a33634467acf3c28ff21bc4020080b6ec7e43ee69ebd27c12745034`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:50 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 21:17:50 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 21:17:50 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 21:17:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:50 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 21:17:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 21:17:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c132d33ee645182f5e3c7bb7e0762b9a929c0df2e5a9335dc9eaf90ca9e403`  
		Last Modified: Fri, 08 May 2026 21:18:21 GMT  
		Size: 92.5 MB (92479894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a442d8bab40c23911f88e2ab7883ab5b7bfc6c3d530d9d5874d41f9e4cdf7a1`  
		Last Modified: Fri, 08 May 2026 21:18:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0e2abecb5ff534716ff765e5bba1a9a3cfebefd7d38823ff4692285e20ae8087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c752620aaf392c59d199c1ffdc39d9228887e5e2ae61c8a60965f0663074b6`

```dockerfile
```

-	Layers:
	-	`sha256:9fe75bf2478c42b00430d66d4a8dc73e283f869e59da99d01ba178288bb56791`  
		Last Modified: Fri, 08 May 2026 21:18:17 GMT  
		Size: 10.5 MB (10497855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b670f952f3b23481435183428c00528935c10ce47802e1a7c07c75f9b56d848`  
		Last Modified: Fri, 08 May 2026 21:18:17 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:b030fbc230c3ac38679178f05813e67790bc9514a13e3483e5993d546ec47b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257936437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756c44e6b8bab4d721dfcb5e3e5b39d3cde987e210be6d9618f67510daa18593`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:13:23 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 22:13:23 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:13:23 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:13:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:23 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:13:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:13:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef2e4eed112ac2d8730e2603fe97cab1d0ce708d52061992fd2f72e1db7e12`  
		Last Modified: Fri, 08 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59653543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e366aa11b1c7b90d4aa743c79b1e38e63c3e694fb1f0ef5461e4223462b630`  
		Last Modified: Fri, 08 May 2026 22:13:55 GMT  
		Size: 66.3 MB (66342172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e7137c96fc07d2fc9e87f7cec43a327dd6c1385057f6c469907ef731cca2c`  
		Last Modified: Thu, 07 May 2026 18:01:49 GMT  
		Size: 65.8 MB (65786476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ceae8ce0b4f9223bb83dd7c2b52a5726e838d984d196b6cff45a74f58e4e77`  
		Last Modified: Fri, 08 May 2026 22:13:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:60d3264ee77c173ab208a62d532a2640e77587174a2f833eecd8cbd1811174d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9819da7fa3d81e399c1f8a2225e69e837c63fa01e9400d5eb2b18194007124`

```dockerfile
```

-	Layers:
	-	`sha256:dca9c035f4ba50a2acee29f80806e3600cea609b2c7126b931138d23f7d865aa`  
		Last Modified: Fri, 08 May 2026 22:13:48 GMT  
		Size: 10.3 MB (10304567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6161429a2e88b7e328a1d06707d6313a50812da4e8d6e98460c09641b4c8fdd`  
		Last Modified: Fri, 08 May 2026 22:13:47 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:519114ff1aa6dd6af622824f1cff611e1a3dc5582acede013495f82d0843525d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287185670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff68555eb5f82fc5410aeb3f7a439f5b3f5dd846995fc148a0d97bc4b901854a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:26 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 21:17:26 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 21:17:26 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 21:17:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:26 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 21:17:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 21:17:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5b71d08511537910256dd369d97ff599afa038eb82ea0b5f09585c2bb3663`  
		Last Modified: Fri, 08 May 2026 21:17:53 GMT  
		Size: 86.6 MB (86555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0329f9bfefbf52f9c7eeeee3bce3970cb4e615b2fc03fc40ed3a7baaba1abd74`  
		Last Modified: Fri, 08 May 2026 21:17:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5924babebc9b7c171566eca27fff79e6396c06afe92d46bc85529f08b877134d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559c6f6ec21a1146a606735695406dbfa7d5679f3cf663f56305299cae6609fd`

```dockerfile
```

-	Layers:
	-	`sha256:42f16250871e6d6a874a8f4f5d0d683b597975a7d018ce5ae61ff34eabdd3da0`  
		Last Modified: Fri, 08 May 2026 21:17:52 GMT  
		Size: 10.5 MB (10525703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdcb8ec622f830c3ed8911278d1958c9503164d3d5b590cf1fb71308a8c81727`  
		Last Modified: Fri, 08 May 2026 21:17:51 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ae41f395d9fe501b3fb5e5d5a28e40fe330cd31a0021a4b02eeec1fcdce0c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296088783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e076bdc71dc9c1a25cefe1309b9365d816aa6a993f36725a78e7ce63cd9027`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:38:05 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:38:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:38:05 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:38:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:38:05 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:38:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:38:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6d01b133789f75623659916cfcedb43da7a191bea538eeed2549ef6b98f791`  
		Last Modified: Thu, 07 May 2026 17:38:33 GMT  
		Size: 89.9 MB (89900952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0413e4ee35a538aac4a3382028eaf90d09fd7d9898a52025b54c9567daea2e45`  
		Last Modified: Thu, 07 May 2026 17:38:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a68dd0f564b6d7b8a952873322d6fc6076c67b8623f0c619c852ef0dee630d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad5764f62b73c5c52da89b9f0b7365e4c6b0be4de99fa3695a6f3bc44d5d1bd`

```dockerfile
```

-	Layers:
	-	`sha256:a2b0919bf88e5525f6da6c1e4eca2a017c1c73873248b2ee26665d4d219aab55`  
		Last Modified: Thu, 07 May 2026 17:38:31 GMT  
		Size: 10.5 MB (10477425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf289ac37104344d853f82cad4c5293afd36c42afecb2fe9d41f9498d28a109f`  
		Last Modified: Thu, 07 May 2026 17:38:30 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:9940958b8cbbdbcbed0efd5552dd72c620c5b0d02e51488721bda78af4c80204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268674681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34071b69cef7ac34bfd26f30a5572c6583187c6a67a4035bb6397f1915f4cb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 18:49:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 19:35:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:25:33 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:25:33 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:25:33 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:25:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:25:33 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:25:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:25:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fafc394c7107b6f97558e80faf7c6aa5a2d625bf130259c59cbe1f85ed9fb`  
		Last Modified: Wed, 22 Apr 2026 13:39:30 GMT  
		Size: 23.6 MB (23615606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e7b3cb9c9d1c48a12fd45433b4710af87bfecf6744a09df7916580c67c305`  
		Last Modified: Wed, 22 Apr 2026 18:50:27 GMT  
		Size: 63.3 MB (63309466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d9d3dbe215b8bcf0455f627ea3048e9af9e774f3f36403e2e0c26f0767680`  
		Last Modified: Wed, 22 Apr 2026 19:37:24 GMT  
		Size: 70.1 MB (70051299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6589a99be6c3c8bcb9aa89f20361aac7d4b27c383823ab13763f291107f004`  
		Last Modified: Thu, 07 May 2026 18:27:29 GMT  
		Size: 62.9 MB (62915708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6d5f316ffc2a4515a215675fe8ee03edbb8d1e6999b4527d4e8ad2930c8e1`  
		Last Modified: Thu, 07 May 2026 18:27:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:231773e2d765e1252a0fdea7e50d3842021756e41eeb4de3ef481483c5de7e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f190c36cdab675b8d318d8e4f5ef9b6e0742c20fe38a9e4a4ec05be1c694938`

```dockerfile
```

-	Layers:
	-	`sha256:87d7726bc63073ce7db89210b81535fd524aa16367e509b30be58a604603169b`  
		Last Modified: Thu, 07 May 2026 18:27:22 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:16adb5350ed6ade8d6c6603ca7fac52c5747fd5140ffd8bc1fb56609b2681d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303194232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695a9783af3077dbcead7c621476f4f12be217cd28ca63fd6514bd95a194e662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:19:35 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:19:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:19:35 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:19:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:19:35 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:19:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:19:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5543a629afcc86e06f307e20d98c8cdd9f2490908cdef00122fb2daf671594`  
		Last Modified: Wed, 22 Apr 2026 09:37:35 GMT  
		Size: 69.8 MB (69846406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1c452e78180d60e24977df1dcb4ebc1677454892dc72552b751eef112e143c`  
		Last Modified: Tue, 05 May 2026 23:42:40 GMT  
		Size: 90.5 MB (90488872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677743e4af652dd79f8723ff89a284363d59474b87d72b559faf60d691a51c58`  
		Last Modified: Thu, 07 May 2026 18:20:28 GMT  
		Size: 64.8 MB (64842692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f59e980b1c73cc66461323dabef4d59b2f517e64b44074819862911aa09017`  
		Last Modified: Thu, 07 May 2026 18:20:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cf056c99b8169e820dddbbfeb2e51fd640c42734bf016cb0ea6a2ae5cac1e88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd6aa8e733829ac470409b3e43de31cb28d6e8d5b4e6828e8a11862bc0695e`

```dockerfile
```

-	Layers:
	-	`sha256:cda98f252065dfc027ec70fab4de414fcc1d77552af0bbe23531b76d2033090b`  
		Last Modified: Thu, 07 May 2026 18:20:31 GMT  
		Size: 10.5 MB (10470352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b751b35abea49e4ec09f37ed779d00172e7c8170fcbaafad01ec45a6b28220d`  
		Last Modified: Thu, 07 May 2026 18:20:25 GMT  
		Size: 27.7 KB (27672 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:030bf3e5a7f9085a324ee59bd5f7e63277d72bd253697f7faa6e7c16d78d37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270281789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998365354ed0bf99595ba983958361a144edcd3318326ae8bbbcd2dd2742e7cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:34:27 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:34:27 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:34:27 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:34:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:34:27 GMT
COPY /target/ / # buildkit
# Sat, 09 May 2026 00:16:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 09 May 2026 00:16:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff8edb12d0e4a9c32ee4c3e2a16590b1236e70a297fedfff3debbb7297bb6e`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 24.0 MB (24036421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8415cd4e27961a67eff09b7f658209a310ebce2d9bf3e1cf2773aa7e405d5e`  
		Last Modified: Fri, 08 May 2026 22:33:37 GMT  
		Size: 63.5 MB (63500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ed1d14819ad17ebadc592338770e92592ab67cfa52d2e43878b8b4b1626a1a`  
		Last Modified: Sat, 09 May 2026 00:17:01 GMT  
		Size: 69.1 MB (69080942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585ea404f5b1266beca471637498b2c7b5b5d49eff5d438b1d1e375a59498340`  
		Last Modified: Thu, 07 May 2026 18:35:38 GMT  
		Size: 66.5 MB (66516126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0be2f63d7b0b10e9e602755af2a92ff58e836af99f0fd3fa576449dec51002f`  
		Last Modified: Sat, 09 May 2026 00:17:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:636b09915b5cbf5fe35a6e7b02f0088970fd09ac53117267d5a054875d2b51fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de3dffcfdbdff0b65e084933f80bed6a0815cf660438e0e4b3587dcb610b445`

```dockerfile
```

-	Layers:
	-	`sha256:3e61ce249ae7b103912072af9ab6e60ccd6b4c63862b4bc63da4c38a7bb743c6`  
		Last Modified: Sat, 09 May 2026 00:17:01 GMT  
		Size: 10.3 MB (10329613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d972f23426a966bfb4916d6bc0981bea75cb99d9c52cbaafdb79766264adbc6`  
		Last Modified: Sat, 09 May 2026 00:17:00 GMT  
		Size: 27.8 KB (27793 bytes)  
		MIME: application/vnd.in-toto+json
