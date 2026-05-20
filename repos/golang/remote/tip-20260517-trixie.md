## `golang:tip-20260517-trixie`

```console
$ docker pull golang@sha256:11e7eab12e19959d16ffd4d9ff9796e059f40ffa066fe40d5d4df7598af65aef
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

### `golang:tip-20260517-trixie` - linux; amd64

```console
$ docker pull golang@sha256:20ff33e2240815d2869914d0531a695c4bc48681c894a3dda42d796eb04e4693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349000638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ae152747bcbacd0baff2b2ed4baa3b2a7e1517700b63e329b042bd5c352d31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 18:44:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:08 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:08 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:46:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:46:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf94351e8e5243a7544efebca8889e93cf9aa3fabbfdc597ca109c8f6be7ed2`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 108.8 MB (108800883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6616f3853b3ecfbe6802f0a5bc39a71a89535589f78590596712ece3ecb87a81`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 97.5 MB (97484964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f70b812d2497635f94e8e32e25d801ac874e0767ab7dfe2a291f76f0b3464a8`  
		Last Modified: Tue, 19 May 2026 18:46:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:39df9c71baf465bdfdbe3668e4c1f8fd57f291b96464e150d3be52609bc61082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e83671fc0fd0cf35fcc4331ccb38bc889ad9ac5ddcbdb2d1bff321f28c4918`

```dockerfile
```

-	Layers:
	-	`sha256:3895a5e28a18668c1299ec213a806eee33a708f2e560625008383bf953fce70a`  
		Last Modified: Tue, 19 May 2026 18:46:38 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c0df4c0062a0bde406305faec85a07153eb5d7dedf9da58a1d913c59a1b063`  
		Last Modified: Tue, 19 May 2026 18:46:37 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:8ca175091a82fe06b4313e14e4c6f0b3ca673f13763ca9615b8ad437c461c209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304285918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f199c38e74db28cb526415754006cdfba7e3873405b0d49e1f20bfb279cc2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 18:46:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:49:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:49:10 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:49:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:49:10 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:49:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:49:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca6886395b5be7ff6f27cbb7276a0443f9f6e99c71cf1f42a54a5790081c94`  
		Last Modified: Tue, 19 May 2026 18:49:39 GMT  
		Size: 78.8 MB (78839879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5478a8019bc908653f4fe6a66ee439d142c623ca5f9ce8029f0fe1b0d2c74`  
		Last Modified: Tue, 19 May 2026 18:49:27 GMT  
		Size: 93.3 MB (93343015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc280b6fc5f78d164e6daecef17307daa94f62710c7b5665b17375122cce4360`  
		Last Modified: Tue, 19 May 2026 18:49:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2785381c14a10c29a8241d278ada7a5d8eb030a62c975cc4464ef5ca85ae9dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af8442576b367937929f3e39321597407d21ddfe607afe443e9e6b9ee32f488`

```dockerfile
```

-	Layers:
	-	`sha256:adf5ee80bc9bc7c80a70bab8031e506634c757be9451623c713e76045b6541b4`  
		Last Modified: Tue, 19 May 2026 18:49:38 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b22358f2f5c76d4fc3968a9b8985bcdd936962e5f439a38fcf3f15b51ce78c`  
		Last Modified: Tue, 19 May 2026 18:49:36 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:196614db797991116ef05b205d2c269c760ecfb442c354fe279d2bb277dad907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332888376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3c0af263a0ce6ebb87db257aaa0f9b9198198a000a594055543d7eaeb3ff9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:23 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 02:19:23 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 02:19:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:19:23 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 02:19:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 02:19:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362bbd9f0ce6dba271a216874d66c447068b7602cd8b802772e26ba7841bc419`  
		Last Modified: Wed, 20 May 2026 02:19:54 GMT  
		Size: 98.4 MB (98376133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ad482d2898f832f866a10e8b2d7cae0b36c78a58ed7da81be2817260f57a4`  
		Last Modified: Tue, 19 May 2026 18:45:10 GMT  
		Size: 92.2 MB (92221410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f618cd4ac99f146ad6910b6a1481713a5cf30df68cec3ac98836fe48a1e7bf`  
		Last Modified: Wed, 20 May 2026 02:19:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9aae4612239f79674824bcec473ea052bd0decf9de9d6ac8d880d82965af2b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db98e5bb5a798c8715ab4eb7d417464814ae4e806ae0b33af5316045af5a8b1`

```dockerfile
```

-	Layers:
	-	`sha256:8e8e1c00f83ac487f2dbf4ec5bbe097fbdc310fc6f4bc68bcb5fbb681f804775`  
		Last Modified: Wed, 20 May 2026 02:19:51 GMT  
		Size: 10.9 MB (10905681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b200738f06911bd3c46f45dc827949ae3f4a3fe9f95518d8193321faa11f85e`  
		Last Modified: Wed, 20 May 2026 02:19:50 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-trixie` - linux; 386

```console
$ docker pull golang@sha256:1afaa2c27aa916d077870db9c84b4f86a6317c5743941a4176a58da9db632a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349587188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a528075b0f9a021c539c21cdc364474b3971b18caaf3b7f38218d4bd103c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 18:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:17 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:17 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:46:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:46:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044346ab4a2aeb8b45da14959a6b11fb7007ddc093f788e1398c4fb3a1769c18`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 106.9 MB (106865416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1c12b1c007dae0ded7a2c5d8a74dfe44bec08363cdf8556a245d7c8b644731`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 95.3 MB (95295509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8578f0e72188f6fa931aa218aaece37ac8e44fec5c2960950cd8a10e98e26e`  
		Last Modified: Tue, 19 May 2026 18:46:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8cd61975e5d56bc98f103e0b37db14bb32b9f484810524bd59ed467ab138ffa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe4321b42ee9e89625a1e92461670f5bcf56d1c8683d29486e852a7449aa95c`

```dockerfile
```

-	Layers:
	-	`sha256:a1a4a25bb33084dd193e2024706407178426e242db8de3eebeb3f4bad820640a`  
		Last Modified: Tue, 19 May 2026 18:46:44 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b21e3c893fa00c1e0c871ef4d53ac06053eb152545e9801cbb0ca6395b6446`  
		Last Modified: Tue, 19 May 2026 18:46:43 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:270b0fbaa0b23601ee03dffc32ad45e84e485a8257facf56cfd0e5f98dc6f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340160686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364f5fd704352223c762dbd6c89abc25439a043513c5485bffec2f06b71ce51c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:48:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:48:50 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:48:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:48:50 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:48:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:48:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994ee9ee43a37b330c0e9ecc8b0d4c61fc214f581c9517cc68b8d35d38579d6`  
		Last Modified: Sat, 09 May 2026 06:14:33 GMT  
		Size: 92.9 MB (92930754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031549f4a149afd12a0aa62ad2634135f41cb41de30ad0670c5e09695e591f0`  
		Last Modified: Tue, 19 May 2026 18:50:13 GMT  
		Size: 94.1 MB (94052228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2833d7407a71a725de77cc09b9bddc23d739b9fd2205274670ff43a50fe85a77`  
		Last Modified: Tue, 19 May 2026 18:50:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d7daa00583c283764f4100250bf2f70c1fa58e46c4b41786b11042ffe7046247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10beb7cdf96fb811ad608959800f1a343cef50bc9e2c910aafbd2c5b8067a55`

```dockerfile
```

-	Layers:
	-	`sha256:2b4f805b3f0d67d99d2ed743b1879124cbcae01b9e7738dc2046dd2cb4638604`  
		Last Modified: Tue, 19 May 2026 18:50:11 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48fc34be4238c560526b825545998db97ce2ee02b461ff40b540cc6a4aa30cc0`  
		Last Modified: Tue, 19 May 2026 18:50:10 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-trixie` - linux; s390x

```console
$ docker pull golang@sha256:295d1b5a4e318b279326397d9bad65372338a96c3be5df201524e204a8788c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316860248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac126c8852c1109b43574a1d4ab58cc94a0a86210816d6c2457add9eaa080030`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:44 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:44 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:46:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:46:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3bbdd2fc257950c611fd6795ac67747b411ad1789b54a283e0cb1bb22d4b2`  
		Last Modified: Fri, 08 May 2026 22:34:34 GMT  
		Size: 68.6 MB (68627825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c775d8e658bec93d151c4a165505e929181b99ac8cccbcfc3139166ff0a26ccd`  
		Last Modified: Sat, 09 May 2026 00:16:39 GMT  
		Size: 76.0 MB (76040301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c82cd174659cb53c7768fbc8389b7b3eabb725a4a95e0bd43007eb9eef0a5b`  
		Last Modified: Tue, 19 May 2026 18:47:13 GMT  
		Size: 96.0 MB (96017021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8d7b175a537cb927d4c1541ac4f3315c915e2edfedc4f9e2709a3096c43e44`  
		Last Modified: Tue, 19 May 2026 18:47:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:803e05aeef0dc2976b78fe43b1e52027b3c56dffbb2e73b0b5902e6eea313f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2949f6f1c149c6e70b69c44a4b3b0c78149842ef90c4ae00d8401c25473e58fb`

```dockerfile
```

-	Layers:
	-	`sha256:5b17eeb0d7aa89bed828d145920ebea18fc0d1b8d9f15e9e48a53156340afa6f`  
		Last Modified: Tue, 19 May 2026 18:47:15 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7003bfc18fa82559f62529194d310484aec0b0e3ec5bf03266b02f26f954aed`  
		Last Modified: Tue, 19 May 2026 18:47:14 GMT  
		Size: 28.8 KB (28791 bytes)  
		MIME: application/vnd.in-toto+json
