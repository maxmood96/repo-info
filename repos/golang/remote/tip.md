## `golang:tip`

```console
$ docker pull golang@sha256:269106f8071efd212a3360e23b3527a07f3de0a3011758ed32cf6159a36b750f
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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; arm variant v7

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; arm64 variant v8

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; 386

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:a9c28777fab2c497c3056b8349ee96e1f5b8615cf728c1622096230d79bc2c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337598525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09889bb1707f24978da604f1af9bf8e2db9d33b4deadee75e3b71213f70b68d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 06:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:34:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:34:00 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:34:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:34:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62094cf6808b342239ceac9c58c9096b769bf275793baaa6699740b93ef88f7b`  
		Last Modified: Tue, 09 Dec 2025 06:22:27 GMT  
		Size: 92.8 MB (92815776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de3a0302474d051f06a0dba49ec72e6a84fba75a10ec5c8dcfe3ca9da396d`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 91.7 MB (91655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c94c99f27d1cfbe02effe868908c59561813d2dc6f8a09e09c5a01d54fda1`  
		Last Modified: Wed, 24 Dec 2025 05:35:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:30c390c6493e88367f86bd759e35aa3ae4d5918a144ddf74cc72c9a8ee22ce2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74a76dd3b0ad62f293886311c491cc047f8eb64982afa74678acef126ed4c1`

```dockerfile
```

-	Layers:
	-	`sha256:ba7907559710dff4f02811badd97b83e7275d846c7f6a380f0ae9cf70bcb9acd`  
		Last Modified: Wed, 24 Dec 2025 06:24:29 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772d904105f26427c92b9e7c8f8bb916854db9263aa0324cbfdc908c689e19c0`  
		Last Modified: Wed, 24 Dec 2025 06:24:30 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:57dc55808c4a5c88127ae2058ba38176e0f76adadb8247fd115cdfd252bf2be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314875221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350bf60ae1561162d97c85cb79e1014947b9d88383a93b46908ff65d73ab8d4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:18 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2be274f95003449a8278cbc7ab315c7bcb675710ce099ea39eaa8742edd0f0`  
		Last Modified: Tue, 09 Dec 2025 03:00:19 GMT  
		Size: 75.9 MB (75919454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eae26383a5ec3ad19d41ec233e74f5aea1ebfab7013779b5b7f518483b785a`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 94.2 MB (94198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6034d6bb260ee37a79a943ccdd639854251c8c9114a11d483872c70a7d15b5`  
		Last Modified: Wed, 24 Dec 2025 05:17:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b2ead00a4d7fea96d80fe37d9edea44a059725adf2d56df88e2332a740438f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d56d16a50f4f02c6c95f502c8153a6a1bc8c31db58eff1a2f7948ac96c90e41`

```dockerfile
```

-	Layers:
	-	`sha256:30b420beac0fa4c147d2262578ea58fbaa97d4b72319ab6b302fb708e0340ee2`  
		Last Modified: Wed, 24 Dec 2025 06:24:38 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f08cbc7dc6840b4aaa21f02cdbe1d789de6a738f157bf461e1bfbf3c302c57`  
		Last Modified: Wed, 24 Dec 2025 06:24:40 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
