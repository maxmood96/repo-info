## `golang:tip-trixie`

```console
$ docker pull golang@sha256:7408e5c39a79d07c8c3126ae7d273df48382b0ff281e46c97bd3a333eed500ad
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:e90c37e19e748e0d837dfc6d4e30910ce4359fb94d90ed8b6e5459485e85c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339834061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777dceb5dbe6a1a8a85a07af35dbc2f0319a7132d9d961e09ce77441f34049ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 03:20:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:22:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:22:21 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:22:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:22:21 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:22:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:22:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4927f1668e89693486beae36dc16c4932ab7290953d26f6f9cf8625d4d6b7b8a`  
		Last Modified: Tue, 30 Dec 2025 03:23:05 GMT  
		Size: 102.1 MB (102108481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c54e75f0355977f49fd303fcd47e9c421e5cb4ce0639b9b1710d2f526d135`  
		Last Modified: Mon, 29 Dec 2025 22:17:03 GMT  
		Size: 95.0 MB (95044613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d7b518d7c256742bb9893ef385849cd1621bcaf20e3d1e9ba44ee597c775af`  
		Last Modified: Tue, 30 Dec 2025 03:22:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b8039db94d9c9ce7358c2da95a7adaea9b8ca726d19f27ef79b7cd07255758bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178690526da9e67b2b5e3929314d26d57ebaeeeac6558fb61eaa25fc371f95d0`

```dockerfile
```

-	Layers:
	-	`sha256:484f4fd856448313ae8f61104118954bda164bffabc2f2f9dc3355b8efc4bce9`  
		Last Modified: Tue, 30 Dec 2025 06:25:16 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0eb3a5b9770c4bda6433f01a03f9edd0df5ab59b27edda7c3b63ad8ee544cf1`  
		Last Modified: Tue, 30 Dec 2025 06:25:16 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:8e54353da3a503965aea2bdaf397b176bbe4923ba5ff7c0b0f629c238e04d1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295920725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f4008deaa60938a0ea63be8332477610677fd95ea70f4e6a21b4d3944d869e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 03:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:19:34 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:19:34 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:19:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:19:34 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:19:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:19:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c2e360b84ae7701db32079eb301ee96231fbcf01d7fa944a62dadd713f202d`  
		Last Modified: Tue, 30 Dec 2025 03:20:16 GMT  
		Size: 72.8 MB (72754144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a592f218adec4eba0bdf6f4ba76e47643fbd079be331ecdb85fd7600664dc026`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 91.1 MB (91114533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73614c36a4be88086bf0c28c2ae13e0b2aa5b730b66e28b01814b27c8f41b75d`  
		Last Modified: Tue, 30 Dec 2025 03:20:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0bb257305f9c92f7bd66d68ad727a9e072723f4e830645f4d62f7b36d33cbc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acc56b97777a57ef58390ad191528a8df222f542fda3f12d9ad73c59bde7bf9`

```dockerfile
```

-	Layers:
	-	`sha256:0321ed381ace79f29f2036167a8415ee0fc2d8b23c3cb42368b2a76f22615ee2`  
		Last Modified: Tue, 30 Dec 2025 06:25:26 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716aca00aac10b6d5fb5190dd7f09ea8b441d7cda52fd755f368b00c47556a7d`  
		Last Modified: Tue, 30 Dec 2025 06:25:27 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:cf1de7c83c2cc5c5792386a71415d5d3a6b0a609c2177d86b929e069c4c260ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330634629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5422923a2413ce76ad9180ee6259259fc5058423b213c8fb51825be23174d9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 03:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:21:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:21:57 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:21:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:21:57 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:22:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:22:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f8ee413c8b61fbc518dbac58a0ef16f0d2d7c8b7596ac08fb400cb31c128a2`  
		Last Modified: Tue, 30 Dec 2025 03:22:39 GMT  
		Size: 98.3 MB (98254466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff2a18ac08f0eac3e3d9e16d67bcab1f49cd95a40840a22cede89724436815`  
		Last Modified: Mon, 29 Dec 2025 22:16:45 GMT  
		Size: 90.1 MB (90124983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30de4cc044aa33b3d973409089a99ee554b38177b914080f1c5c8ee728f862`  
		Last Modified: Tue, 30 Dec 2025 03:22:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:cc4fdfcd84338fbb73990afb04e384940053bcdb62b8df07b610edeeabfd8ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a74dc299ad63e21a884f4f542f8b0f29e7e0d550aca3a6144bd049568fa0dca`

```dockerfile
```

-	Layers:
	-	`sha256:1b19196b950d7c5cf568c883956d0f791ebb46d2556c1689da90336ec57c69d5`  
		Last Modified: Tue, 30 Dec 2025 06:25:35 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd12fa5dbec82f519117ac2b1d7d31f28b0620da35498e2dafe5f6f3d8daf92`  
		Last Modified: Tue, 30 Dec 2025 06:25:36 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:bc8740b0a23438fababc25ef7b02eddd568039eb44d06eafca9989fd93419fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340867058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebed657f9fe3d6d305e93ba294fc1f076307d4b991d41f568fdad334cb3b617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:19:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:20:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:20:54 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:20:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:20:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:20:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ade73e32bbbd03836491e06521d1ebd5a0fba60e525afdeb3262e68c8b12d8`  
		Last Modified: Tue, 30 Dec 2025 02:21:36 GMT  
		Size: 100.6 MB (100555344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a65206a294cfa58d808be4d6044b7204f516d26da0fec139e2c57b03be9a1`  
		Last Modified: Tue, 30 Dec 2025 02:21:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3bc67aadef44dc3ad0700152f0bfd453c7993fac049bac083f047862baecbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90c97ed07c1ad0155a5249054172c4e109379c387a5897912febee0bb27ab5`

```dockerfile
```

-	Layers:
	-	`sha256:1c749b3b4963e1aea78097fb43c83853339e3f9046ac18c21de8ae2a2521aaae`  
		Last Modified: Tue, 30 Dec 2025 03:25:46 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb1784d9e4461ec2c758c3a218ee7e821afd14cab59868c8cb3cd07edd94a60`  
		Last Modified: Tue, 30 Dec 2025 03:25:47 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:55086367f34b60d1dc9e4c3e2d603d00936e38a2757666796703686f64e6a5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337609975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c08fa2593ae88b07190e5edb57dd19d1100faa11d22d16ecd37012a656e25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 10:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:29 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 13:28:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 13:28:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c305b2563d5a320b2f5d542cb42b58b482a07941244656f1dd066b0fb90900`  
		Last Modified: Tue, 30 Dec 2025 10:25:02 GMT  
		Size: 92.8 MB (92815505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98e6a9db6f27c232427cc65a14243d3dc0a9f5145a0455e78bccfb2bf7249c`  
		Last Modified: Mon, 29 Dec 2025 22:17:47 GMT  
		Size: 91.7 MB (91658002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9fd986a13e3fdd23262c438f77fe657aac9617865572a4073456ca9eb13164`  
		Last Modified: Tue, 30 Dec 2025 13:29:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bda77287fe0a12973af04198b40d8a970f1c66aabf1efb13495b917617687542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548edc68a5b1c9dd8e881601a4ac2f51efdc81c5690a70d6937023002f682180`

```dockerfile
```

-	Layers:
	-	`sha256:25668f57112327f304e0a20b652098937de023eb55f3c1d1946bd4cecb44ef9c`  
		Last Modified: Tue, 30 Dec 2025 15:24:00 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60adf7a0141980361dc7388a6c243c2f19964ee47492054f6c907734d47245a`  
		Last Modified: Tue, 30 Dec 2025 15:24:00 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:7952b6372477c6d07bd3099ffefb74cd51eb30854438c9240fd9b6e6494bb17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363279010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce951910c1f9f828dfdb57255fb0da99fae679dafbc70efc653cebaa1d591c30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 07:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 06:56:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:56:42 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 06:56:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 06:56:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4af291d8cbdff6d28ddd144cb820c9d50e09d2eefe7cf2deb9f3384fddd0193`  
		Last Modified: Mon, 15 Dec 2025 07:10:40 GMT  
		Size: 131.6 MB (131594746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efbeb47d67a4f0f513126184055d20de04c0261cfdbd8b06feaf3a27c3f0eb2`  
		Last Modified: Wed, 24 Dec 2025 07:04:00 GMT  
		Size: 92.3 MB (92298638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be72a4e09c8ffe6f8ce6556e995fa8ab56ec582d1f2b14a2864dc979ca88ec42`  
		Last Modified: Wed, 24 Dec 2025 07:03:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6d38cc12d2f36c041c99a1f950b63ef191ed2c3b33e6cec769d7a65e580055b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99edd8d350026be9177f1067a1ec6e85b7f736022a00d76b647e8f9ccdf7e06`

```dockerfile
```

-	Layers:
	-	`sha256:eebc122be4fa3e0f80e64faedb8c04a7a7a0c3147caeba5aa00a9c900dcd2a29`  
		Last Modified: Wed, 24 Dec 2025 09:24:03 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a56a7dc2f384f11c5c114e514fd0ea65638e1bfaf2742bb04a7519f51d78f79`  
		Last Modified: Wed, 24 Dec 2025 09:24:03 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:268665c6fe63ebb4626772e1e8bc4f9b43edd1f6d273b3a1beae17b777f3a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314886102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae29dcbe3e131226c95de84ee0ee73dad47db5c4ffd2c84a44daafb8488dd4a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:12:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:41 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 07:12:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 07:12:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ff73de1940cf169d9834c4cf953c0cc9c72c478673013d2a8a22a41944f8f`  
		Last Modified: Tue, 30 Dec 2025 06:13:25 GMT  
		Size: 75.9 MB (75919327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ce8a7fa174e9abbfa1259cfd0fba44c900e27f7f4a5ae1c83f6fe0801a275`  
		Last Modified: Mon, 29 Dec 2025 22:17:17 GMT  
		Size: 94.2 MB (94203858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961a381ea386f40ac884e157460ec9b52b0cd75b46f5c81deca3f9d89f95c201`  
		Last Modified: Tue, 30 Dec 2025 07:13:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4dfa01fe7be4346b077aa3754eac5e327c44984a0ac772d8e07be886ba30d42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca5a6964178444b2ca2558f0def37290d831e2ce3c969061449b5436afdea92`

```dockerfile
```

-	Layers:
	-	`sha256:3eb816c04b3e038b7612a0704ce24be0aa2789410116d5f99c4e252d90858e95`  
		Last Modified: Tue, 30 Dec 2025 09:25:26 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17981e22892b8bf61de377c464379e95f80d059c34f4633f04379fad656d5f44`  
		Last Modified: Tue, 30 Dec 2025 09:25:27 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
