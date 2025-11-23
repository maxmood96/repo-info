## `golang:tip-trixie`

```console
$ docker pull golang@sha256:45554e7328d7eae6dbf929812c7b02188cfbcfc5727648bddddf25fb6bd80f2c
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
$ docker pull golang@sha256:0d425c82a279c69b0d66b86b51c678362f7d65cc605c4ec9e8ca9610096c1c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336755806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e0c17bb4fbde4e024146afbbef2a26da9b87373ef54339e77b3e538e1c280`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 11:17:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:18:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 11:18:39 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 11:18:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 11:18:39 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 11:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 11:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645c83611e00ca7c1da0a65a6a3f7b05c542d6d941bbccc4c4b53b33d8ff78d6`  
		Last Modified: Tue, 18 Nov 2025 11:19:27 GMT  
		Size: 102.1 MB (102108890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7b3373fee62cdb53f94efd45c65db5604e6edbc40b8d907723c04dd03d3e5`  
		Last Modified: Tue, 18 Nov 2025 02:42:20 GMT  
		Size: 92.0 MB (91964299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d95c4c3b7fc31bdf6d5e3d8e67c2ab4ce3737e123cb8d5270be1c8ee746ccd`  
		Last Modified: Tue, 18 Nov 2025 11:19:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f1b07998a08fb6658f8f2366ece3ae549e1285e132105cf65a42345eef50a41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d36fd39dad57d92cf59aa1bf13e120720577f25d490c5c46c35a9a53ed47abb`

```dockerfile
```

-	Layers:
	-	`sha256:f4446effa5a2b729ccb165c920baff1b054ae802dc3e9593e07295f5c76376ba`  
		Last Modified: Tue, 18 Nov 2025 15:24:56 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d7d345eeed8d1b39db1875ab02b94616b71dd9e4fe2791e0c7a751b63835fc`  
		Last Modified: Tue, 18 Nov 2025 15:24:57 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; arm64 variant v8

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; 386

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:8e35e76482bc7353426bca987b0a8710aa870372b936f251081ffee2be40d666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c1c814a928627c9bc06aa1c9a9bd582fc33193bb7f97618e9a6a015c74a4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 13:00:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 13:00:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7756cae789e79571b10ebdde577e95b06e8789c77b7c86e1f13d466fd5e8d9d`  
		Last Modified: Tue, 18 Nov 2025 08:21:51 GMT  
		Size: 92.8 MB (92815805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bf767f06980acf1f8853ce51af733c99a2b6d24e85cd252fc864241862d8ac`  
		Last Modified: Tue, 18 Nov 2025 13:01:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c4032777912033515934440e1e2dc77f94b93ca4c18cff80e91c0e1add212b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0ba36ea1856b7720b8c0de3a57a30a253abdafcb163492aef683960fe6ebf`

```dockerfile
```

-	Layers:
	-	`sha256:995e7380e2456cce83fe9a2fc209732fa92c5aee562ebaf3809cfc56c0599708`  
		Last Modified: Tue, 18 Nov 2025 15:25:30 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1d9ab67388025e3c4dce3186a26095e1f57c6bba1803b06e4fd0e5f356e40f`  
		Last Modified: Tue, 18 Nov 2025 15:25:31 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:96d8b51046ee3009d5ecb385f521e8c0ce73a53a2dbe53debd76de13173e9b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360100653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc42bf1393ddb5578846657ee8c12af49d04decce7affe0cf0a28343b7afc3a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 00:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:22:22 GMT
COPY /target/ / # buildkit
# Sun, 23 Nov 2025 06:47:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 23 Nov 2025 06:47:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec3a0230c2d0fb9a920af1a0e3505c5c46ba754e2ed64bb7c5b5268656905`  
		Last Modified: Tue, 18 Nov 2025 00:32:26 GMT  
		Size: 89.1 MB (89120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66588ce513d5466daf62b78790efc7ad99fd5308057e64f24170f95ec1e0221`  
		Last Modified: Sun, 23 Nov 2025 06:52:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4584db39fbf4beadfe6df31816a44394d8c00c7a5f78dc2dc2ad089112aa8a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886507cc72c07fe9306e0c160f739a0d7044159db602b058f7d0e35a776fbf02`

```dockerfile
```

-	Layers:
	-	`sha256:a2ba16b3e1aa2deec045a0a5bde839b02e3586a2b97229c2bd1684deef127d7a`  
		Last Modified: Sun, 23 Nov 2025 09:23:45 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20c45223f502201da9ef32aa4eadd1b864cffd5de7f99e43b97009dd594fd0f`  
		Last Modified: Sun, 23 Nov 2025 09:23:45 GMT  
		Size: 29.0 KB (29026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

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

### `golang:tip-trixie` - unknown; unknown

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
