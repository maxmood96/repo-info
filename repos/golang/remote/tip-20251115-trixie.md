## `golang:tip-20251115-trixie`

```console
$ docker pull golang@sha256:a166afc588a8f9d93194ae3b3f58ccfa4ae87d3530c53b38ce499742f86a4849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `golang:tip-20251115-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d559c8068eac626fde0c0249f86e4f43a13bb4fa36c1fbce4c09b0e374dfc4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292918663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb914012267ba2dd71bb789f3046c669dc64f9a1353e363eb4c7e7058162aef0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:42:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 07:42:32 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 07:42:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:42:32 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:42:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:42:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972c9339e4005936b30383edb6764583658fae27907f75bb12d2da79bb0aa9e9`  
		Last Modified: Tue, 18 Nov 2025 07:43:14 GMT  
		Size: 72.8 MB (72754072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2c69f85dc047cff5b8e0c725d241fb21eed7123e04e156a844669a6e5e5d3`  
		Last Modified: Mon, 17 Nov 2025 23:23:14 GMT  
		Size: 88.1 MB (88112716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924872edeed37cf06551dc01df2850ee4c1cc99028ae1e99e5fae181b26e16b4`  
		Last Modified: Tue, 18 Nov 2025 07:43:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d4a0958466c646a5bfc8a40ee12766cd5735e9aab3000ffa9400a66f702b6dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d526eb2847fb0d7419adbd93688af306b14a0ed23e0f60542f1e46e7399a61d`

```dockerfile
```

-	Layers:
	-	`sha256:347435f950cdae279ebd9aa7216208c3e69d979b60d884072edeb2cbafe937a2`  
		Last Modified: Tue, 18 Nov 2025 09:25:20 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c04a8e5fc616ecb6d92d94e83b99aa0307f5aba503c9c8b8e8c20d2f51c7fd`  
		Last Modified: Tue, 18 Nov 2025 09:25:21 GMT  
		Size: 29.1 KB (29091 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8cc9bd587b946a8750edae5de10e3a8495abf171d2444356ff709a267f69eb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327688850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15c786360a3eb2011904535b07ae835620356754ed43714004e2e74153fc301`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 07:24:27 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 07:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:24:27 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:24:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:24:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19bc0bcafbcb960845f32457eeefb962030a6cf52d0d2f449ff736cb327ce9a`  
		Last Modified: Tue, 18 Nov 2025 07:25:11 GMT  
		Size: 98.3 MB (98254949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72859aa41c7126c75b0eaa6f62530c6ab6d97e63fe3d290a8c1d237f80407685`  
		Last Modified: Mon, 17 Nov 2025 23:30:36 GMT  
		Size: 87.2 MB (87177738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2560ab449e195415f2023d148f2b1c800bd09cd35501cf14adbee6fb116f50`  
		Last Modified: Tue, 18 Nov 2025 07:25:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e8a82fd10bce541bc339a599b600c855a314c99b33831a01761aa7e3b0e7a656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8346bad444600cb9b29c6d5a54ebd7b347c002321d5c648c9fae10a34a073006`

```dockerfile
```

-	Layers:
	-	`sha256:a940af4bf6d62f2718f31d8378e964f4a88591a5d49c29ded88bbab1f0478fae`  
		Last Modified: Tue, 18 Nov 2025 09:25:29 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae5e2e275b1e50d4146c6fd1e3c986ba3d2ac28f466c2f82f678b2dceee449d`  
		Last Modified: Tue, 18 Nov 2025 09:25:30 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; 386

```console
$ docker pull golang@sha256:dc51cc80ababba7d66940aa9dc85249ca5c560c31c4b5e8c9275e5a0c0b930b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337841637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5102118baba06e72a228ed5775fc277996627bbb2acd08c76ccc79b012276cd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:23:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 06:23:17 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 06:23:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:23:17 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 06:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 06:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818b76336c564e51dd92593b29f27f226f4b5cf99d2e0376c8a808c8cbd56c9`  
		Last Modified: Tue, 18 Nov 2025 06:24:04 GMT  
		Size: 100.6 MB (100555284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb363788838918ac7e550b93200cd675ca2501f3ca5b79cee14723fcfb2dfe5`  
		Last Modified: Mon, 17 Nov 2025 23:22:28 GMT  
		Size: 89.9 MB (89904896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dd482799ee5bfaca32bbaeade08879d55c28f529cf556a56f22359b8ee878`  
		Last Modified: Tue, 18 Nov 2025 06:23:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3db453ac616da6fa2002f9996ca0b8e093e662980266ce9db6d66ac2f64c3459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243b722acdcdb0bfa19d3d5e378c090de4d16f9d85d314b22d1687d5f6bbc712`

```dockerfile
```

-	Layers:
	-	`sha256:9c86815f51f0c41f7a9cc7645fc6b43d616ea4f4ec4e241ac98538bc8a266075`  
		Last Modified: Tue, 18 Nov 2025 09:25:39 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5806b68612698267c1811aaa937aa23772c3742a8ee0e2a139c1dfa2e84c614b`  
		Last Modified: Tue, 18 Nov 2025 09:25:40 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:c1edaff5d35366d9e7c82fe195c4f8d8e760311850e6052af33dc2c5258b6b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334595971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfcfc208f2314616786f0087016a9e90af311a9cbd1403fbbe8854afc4cb7a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 16:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:46:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:46:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbe8662034d4013b7fae91328f939dfb669ce78f36e4a91a9a0c68675f61828`  
		Last Modified: Tue, 04 Nov 2025 16:03:22 GMT  
		Size: 73.0 MB (73035332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf1a7a31596fcf3c8fbba7ff2eb1b660f7e0a6b2bf397a661a0ba4967a80ad`  
		Last Modified: Mon, 17 Nov 2025 23:48:36 GMT  
		Size: 92.8 MB (92815616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38e147750a80771350283c7887ecbb2a94636415349ad0a8d4c2dae0e34a5bd`  
		Last Modified: Mon, 17 Nov 2025 23:48:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2b314f4ba22feda755846f3dedf00a24bbf182f19bce23bdf6f346c769a94e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b1a5f93fcec9188d70ab7fa9e0d77a6bcaa86e3fecadb0b0904f1077a388ff`

```dockerfile
```

-	Layers:
	-	`sha256:7c4360bc1a5f698c1c74aaa7edc9b6dda6c4b319d5db5e96364321c7ef9967f4`  
		Last Modified: Tue, 18 Nov 2025 00:24:01 GMT  
		Size: 10.8 MB (10780246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16acc58efb670e92501a59d2ae014ea227d2a27b671e7f5e3860430b88cc811e`  
		Last Modified: Tue, 18 Nov 2025 00:24:02 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:2dcc7dde88df5479f6648361700c229a28755dafb0cbb4c9836cd89d6ee6fb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360100182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6c636e39b9d40706aec9bedb0f15df8319edd71a3bc18a50055ef1233fb32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 00:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 00:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:22:22 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 00:23:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 00:23:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0e1c49c4b6326e11479d7f89ce5a78336570bca91aa46a373571186f6ab4c`  
		Last Modified: Wed, 05 Nov 2025 12:04:45 GMT  
		Size: 25.0 MB (24953956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed84703a94ab124c54334c41ec37609f785f60feaff7dd12005c2d2dec188e6`  
		Last Modified: Thu, 06 Nov 2025 07:40:32 GMT  
		Size: 66.7 MB (66660260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5117301a45a9645452ed334ab328ee4d4f984f3fd793be3e5538b330d9db70f`  
		Last Modified: Tue, 18 Nov 2025 08:34:49 GMT  
		Size: 131.6 MB (131594683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec3a0230c2d0fb9a920af1a0e3505c5c46ba754e2ed64bb7c5b5268656905`  
		Last Modified: Tue, 18 Nov 2025 00:32:26 GMT  
		Size: 89.1 MB (89120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9498e50ee3bdc17b55733e1c45e1813309477c732d1a1c1ca37a3e682144fd`  
		Last Modified: Tue, 18 Nov 2025 00:32:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a18cfd4dd3e492bd1177ff782f4beb35903910da8d99adedda712cbe61870f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5281ed29beb8902edb23f4e0a21d24f9f825499e6629efa44d8c25747356779e`

```dockerfile
```

-	Layers:
	-	`sha256:d8046cd5ae14f5a7c16afdafabb51c91db47bafb12f19974e93384182e799e18`  
		Last Modified: Tue, 18 Nov 2025 03:27:52 GMT  
		Size: 10.9 MB (10854079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad238755e780f5ab35cdd6a24b14ff486b6f43ec1dccd6aa350d8acff8af0a9`  
		Last Modified: Tue, 18 Nov 2025 03:27:53 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; s390x

```console
$ docker pull golang@sha256:7dbc4a9757e6b381af6b97ee964286798c996121a515d9a2e26095b688d49feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310854401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09651c8ae97c451118b07bc480e2d570f94c3b38773f18e04628a6a8b059113f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:29:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:26:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:35 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 10:46:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 10:46:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a481d00827be55e12947c2019e1ed38bcd021b127ca4508bc3947dfbe02dae50`  
		Last Modified: Tue, 18 Nov 2025 07:30:25 GMT  
		Size: 75.9 MB (75919725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4515f8b1d9cf2143fbca8f466beb9046119009ff0c9973ec41a536bfa5dddca`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 90.2 MB (90177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a06709060637d8ed96b56096b5fe6027b5346c192ee8725b61e297f72c2e1d`  
		Last Modified: Tue, 18 Nov 2025 10:52:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:db50c2eb932451a59dccb65f6a654405500008e729f7f02550fdcd9148e4dfe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36c7d99edcd07e7af719006444196bd536f2c1d33a233bae7bd3163bd9e0160`

```dockerfile
```

-	Layers:
	-	`sha256:6c8e1f4111536ce0a62f4ce484b2d3f3ed993b546e3706c5fd342c40d3a6946c`  
		Last Modified: Tue, 18 Nov 2025 12:25:01 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c263ef05eeb7d3a533e225ddb80226178bebb0cfb5186289e9070d2ed45196`  
		Last Modified: Tue, 18 Nov 2025 12:25:02 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
