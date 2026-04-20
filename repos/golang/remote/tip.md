## `golang:tip`

```console
$ docker pull golang@sha256:460ec303d9d47e1e462d182db2ae4df7a754d4bc41da03c235fff0979273c1d0
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
$ docker pull golang@sha256:5509b66e275e2b8dc12e081ff387dd28c8cd0cdb7d8b9d39e2c4548c7af2e4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342203110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73e532e0843f094157478dffe3f5b7b4bf4ff092009aa722169879fecbd181`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Apr 2026 17:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:01 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:01 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a0beebd0694376ff12047b3e35a6a7d260d2a8f299549df340cc755ea7f02`  
		Last Modified: Mon, 20 Apr 2026 17:41:31 GMT  
		Size: 102.2 MB (102169329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9800fe1d00fbf93fa3af2c224e36eef8eb15b87c8b6fcb13141f73eb2f1ed`  
		Last Modified: Mon, 20 Apr 2026 17:41:31 GMT  
		Size: 97.3 MB (97333404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d838892c2e2b08650117ace212245ea36e127449c820a0d5c67b95c864b618`  
		Last Modified: Mon, 20 Apr 2026 17:41:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d363ac563ac30d18e8e3ef60dc049ef3a0db7c746720f5782846888799425bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762d75549799fbae1dbd6203fe20863dc2ee265e9e4c1a4d41c38faee9b67484`

```dockerfile
```

-	Layers:
	-	`sha256:4c0fee3dcb7294b4ddef9ee987f06135c8ea2c279357855e6a4969e7728e834e`  
		Last Modified: Mon, 20 Apr 2026 17:41:27 GMT  
		Size: 10.8 MB (10785659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fbfecd6824dbd6b3657675b4a745f1fb5e3f5ae32189d35e7caf2823f91d41e`  
		Last Modified: Mon, 20 Apr 2026 17:41:26 GMT  
		Size: 29.0 KB (28966 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:25ff7102d6f49f2a6ba7ccb3350e159d9fe8ffe72f59848e8c0c3152e4a86c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298060134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7e7d40feea97e32abc6ff937e5762ad8efa7f1ae329338e4f93035f8c00c92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Apr 2026 17:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:42:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:42:51 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:42:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:42:51 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:42:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:42:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868f799858ac0f14507e60a2ff0757894394681e874e60066914254664b5431`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 62.7 MB (62722704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa6acd2eded0479748785ea62353f21fd0b5abce9e31ef172e4cee475d3f2f`  
		Last Modified: Mon, 20 Apr 2026 17:43:21 GMT  
		Size: 72.8 MB (72805123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42fcfd73df1c3c4e864c147debb0154bf1e1c38912174f3d52a47a654a9641`  
		Last Modified: Mon, 20 Apr 2026 17:43:22 GMT  
		Size: 93.2 MB (93162179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e45f86261ceecde055ca8bc0906d10f2ab715d66b59dc4e26724d0bd52aeef`  
		Last Modified: Mon, 20 Apr 2026 17:43:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7d505236059f48eac7b6b3e7b4dcc9980bdbbde6ad855810dfa5c97766642c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3501832f5618174c4a9a74acb4ec7a51d28ef4e9dd2217a1ca641a0701dddd3`

```dockerfile
```

-	Layers:
	-	`sha256:960da34e7f37b1cc3cadf75af59590357647598a415d9c237c6f6aa1226963eb`  
		Last Modified: Mon, 20 Apr 2026 17:43:18 GMT  
		Size: 10.6 MB (10581546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e556664ecc13410b25ab1a56bfd664cefd7db507bd949ed8bf2e4ca652b6219`  
		Last Modified: Mon, 20 Apr 2026 17:43:18 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:cfacc405fb3e6b1b23a9c346b9da3b11d95c9de443e1678c32e89a08d9eb5685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332611658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da6ccb54fa50763740dec2d2db6948c073c0f01ae6383717c933ca2d53f9c65`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Apr 2026 17:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:02 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:02 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d76a6d41cfcad47f35c38888a9e2e01ff007f452cc0c1979db1eb31d25b5f7`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 98.3 MB (98310046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9da8d3894800a39f60fbfd67e48a2654efcedecf176b3e40f1e07ab0291557`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 92.0 MB (92020630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9949db5618a36982b4710b6e37ef4b868fc1645998c12116e2498c9991f13c6d`  
		Last Modified: Mon, 20 Apr 2026 17:41:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d24c5ea0906e3c79a3c46f808f690cf9055750cd7a8a0e17cac200bda3058cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0f7c2c8242bb31a44d6a7868bb9cf6b79f7bb56dd8d1f0f7bb9a7f41413ec4`

```dockerfile
```

-	Layers:
	-	`sha256:dc16fa190ce5da518ab3264ba330662e78e4958a8d9a2cdeccd8ecc5a75b14ad`  
		Last Modified: Mon, 20 Apr 2026 17:41:29 GMT  
		Size: 10.9 MB (10906114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40f3e7abb19ca3fc63ad43ee5a6880472467e815073ad1f2ff2316a900985ab`  
		Last Modified: Mon, 20 Apr 2026 17:41:28 GMT  
		Size: 29.1 KB (29123 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:17b608f4ffa0426dfa5e0ec9c0a7425526c1225c61d846a1fe48e60c54a75732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343078943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747d9d1a8af7b63f9fe5b6046b1c8aa0d071db89b9069ec1a959eb034a9392d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Apr 2026 17:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:42:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:42:15 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:42:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:42:15 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:42:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:42:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad960cd98db41fbb5a1a05583ed95d984d756e7059cddccc290fd0bc4e9175b`  
		Last Modified: Mon, 20 Apr 2026 17:42:46 GMT  
		Size: 100.6 MB (100608506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ee3233bce23292707dea9900b4db989f25efd70edf364d9cfceefc1e3441c`  
		Last Modified: Mon, 20 Apr 2026 17:42:46 GMT  
		Size: 95.1 MB (95072511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dd3e957711e7b54e0bc91ed41294e973c05ee20ea8efd0a60e74134407e724`  
		Last Modified: Mon, 20 Apr 2026 17:42:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:13dd726ae22d110c576da6c93dab981f48fe287e2b067c1f3d3145e337f81dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d745e07af5750edc3b457df4626332777393455fefc94cc489214d0d9c54fc`

```dockerfile
```

-	Layers:
	-	`sha256:d645bf40611e0eab4761ecc9e778722beac55b1180898c32e3559722abf02bb8`  
		Last Modified: Mon, 20 Apr 2026 17:42:43 GMT  
		Size: 10.8 MB (10756922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3866f8c941195ddf82eefc4669c33071dca766d8390656968cfe68cc4987026f`  
		Last Modified: Mon, 20 Apr 2026 17:42:42 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:f69ec40072d53361378467d2843efada3ccf71c9df1ee286165a4fd551dfe18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339910227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bce740db9f18b3589c1c4ce2dd3907ae4d5822e8d39df190ec2dcd2cd8e895`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:21:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:28 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169353b9ab6307e2b065964fc878588895f32907dd884c905868bc86f58edd0`  
		Last Modified: Tue, 07 Apr 2026 09:55:34 GMT  
		Size: 73.0 MB (73033989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb540501f7eb5e096f520ca2cb5637ef4c3bca5b6d3ccbe7a39cc10f271f5f7`  
		Last Modified: Tue, 07 Apr 2026 18:22:27 GMT  
		Size: 92.9 MB (92871008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f72075717c40f723c05a62a7b4daebee738f45ad2854cdb0f9f31a6113d444`  
		Last Modified: Mon, 20 Apr 2026 17:42:34 GMT  
		Size: 93.9 MB (93872555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efcabef6e283d5bcc78bb9abfc58b745bff2a831e6eb81d3934de39ad4fc63`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4fab101c006b48bb157d47b203d4a0eea685338006e0834fafc4501e21afb23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d3863c7076e371ad6056c3d594036ce1bf911f54e46ea49e046ed1f53e4f5`

```dockerfile
```

-	Layers:
	-	`sha256:f167f01b61498da9607034dd6dd7955f63c1a15f22c50ef002a75e6b416c59b7`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 10.8 MB (10781447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f556bbbb1461ee6d00385210bcdd9e52bdb45aa26ec92230bba54469823e2051`  
		Last Modified: Mon, 20 Apr 2026 17:42:31 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:f3d72eefc4ee158152b2ec2c11dfda7a6c40b9127e49934ca5ba3d049278f7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368630301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30701f05e1b7bbc687078629a902b20c6a1ee2536d57695ba9291e578773bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 09:59:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 18:17:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 18:17:57 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 18:17:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 18:17:57 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 18:18:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 18:18:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacec47fc648b6d60a98d7ff6fd4e23039ac63553f44613cd15e968e674616e6`  
		Last Modified: Sat, 11 Apr 2026 03:02:36 GMT  
		Size: 66.7 MB (66662977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ae371f482aac04d17f4b10d6a0cb36e2673a9d5a8d69e7d7b268296cad8a`  
		Last Modified: Sun, 12 Apr 2026 10:07:19 GMT  
		Size: 131.6 MB (131649469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a410f935145df1e7078db1622c7e4b5b67ab66721f524e15a78ee2440fd23`  
		Last Modified: Mon, 20 Apr 2026 18:24:58 GMT  
		Size: 94.4 MB (94406306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a309b77edcae5048a4efeeefbf6df2fc7bc40efd815ef587463ad61456a3361`  
		Last Modified: Mon, 20 Apr 2026 18:24:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1980b64f8ec4637ae73b65968e61ec9d701c4cec0936ccac74b1ea882275ab7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fb34bac7f2d15ab16933df5307438c0ff49bfa355149d70e233f83df3c8d84`

```dockerfile
```

-	Layers:
	-	`sha256:699c8ef651be599d35dd2376e1d6418b158e4837b9c5f17d18524a19e2566317`  
		Last Modified: Mon, 20 Apr 2026 18:24:45 GMT  
		Size: 10.9 MB (10855280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d6f290311b5cb6bc8538eecca3e30affde7b6341b302bdeb69ccd1009e1913`  
		Last Modified: Mon, 20 Apr 2026 18:24:42 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:1f2c1e473575482e5a66c5a67df6c06db326fb172efb5d8775fe98fc29715f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316630570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695f15ea8de9e95dc0c65448167f26b72d268d9f9f980b2b12a4670c657f9081`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:15:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:45:30 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:45:30 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:45:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:45:30 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:53:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:53:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b42c01b5de7637ae2e011d2f9775f913b01f72b9797773d410bb0d8b437e3`  
		Last Modified: Tue, 07 Apr 2026 04:55:14 GMT  
		Size: 68.6 MB (68627207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d238309bad3a5eccfd4206504a4b2b322fc3d481e6d5359ad31c9f8e286eac`  
		Last Modified: Tue, 07 Apr 2026 21:18:30 GMT  
		Size: 76.0 MB (75982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc40b99896e610d7e8bfd78ceac0447cbdeee9aed83f1c52c72fd167c0ef6be`  
		Last Modified: Mon, 20 Apr 2026 17:47:23 GMT  
		Size: 95.9 MB (95852451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2d0e2f7a062331a25be05322e112be34ef0e0307cfdb96d4546473147f16a3`  
		Last Modified: Mon, 20 Apr 2026 17:58:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:eca4df8e9204239b475dec6e1cb87a51019bf6452213126bd03d61eb9fd4fc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c83552cb7b7a318a0b25ca670cf707acad8e7979f50bedaf6a1a5eb682a7190`

```dockerfile
```

-	Layers:
	-	`sha256:84c319796a04941e6070ec9ae670391d59935a3ff71afbe8859cd503b0a82ac9`  
		Last Modified: Mon, 20 Apr 2026 17:58:26 GMT  
		Size: 10.6 MB (10596807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50048c6ab362c38e2279f6b0b3c28ac597c524bb3c82e8336b76a24439531835`  
		Last Modified: Mon, 20 Apr 2026 17:58:24 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
