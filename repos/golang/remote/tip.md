## `golang:tip`

```console
$ docker pull golang@sha256:aa0a629ce96089ff65aad385fcbd0c12d6ef68260cb5399ee000bb143e4964cc
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
$ docker pull golang@sha256:25f6bda2b048ba57013a6e159308dae26dbe420b01a964ef088dd58aa66c79b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342441249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfad0e96c7aaaa455364dfed59a298ff5c3711e1612a60458330950a380d0fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:35 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 02:19:35 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 02:19:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:19:35 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 02:19:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 02:19:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05f4af01a15a87104d0ae614ff841b4395b037b03208e3cc40b46e1443f07d`  
		Last Modified: Wed, 20 May 2026 02:20:02 GMT  
		Size: 102.2 MB (102233857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6616f3853b3ecfbe6802f0a5bc39a71a89535589f78590596712ece3ecb87a81`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 97.5 MB (97484964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721a7585b464c5ca397e4ac5da873611c048e930fec8af4ebed79ba82de94b71`  
		Last Modified: Wed, 20 May 2026 02:19:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8b8dc376152dd2232f4b647963a27b188f348aa282ab75a046cd2ca3560c3604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3b03cb74d7822d18ed41d2a2046189fa1a0a9e6725702ffd38d8976bd810b8`

```dockerfile
```

-	Layers:
	-	`sha256:eba8e0eecb4a7490eea98700dfec91c3acbe1d3a1e14f5138e6b8db8fa1f7ead`  
		Last Modified: Wed, 20 May 2026 02:20:00 GMT  
		Size: 10.8 MB (10785863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61731f139ac3f8d04f291b7974ffc80e1171be69cf38e5b5abfb7d6454f6e4a`  
		Last Modified: Wed, 20 May 2026 02:19:59 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:b70f72487375e2ef758416ecad1b121ce78f9654096c75255b7dbb5e17a9dceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298335358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae036afae73ee10dac01054a757f11b3b35dc5470eb02e5d50696f005d0cbb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 04:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:17:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 04:17:37 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 04:17:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:17:37 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 04:17:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 04:17:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1112356e272bc3f668c06a972858c09d95b65310f443c3e4e13c2824752854`  
		Last Modified: Wed, 20 May 2026 04:18:04 GMT  
		Size: 72.9 MB (72870485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5478a8019bc908653f4fe6a66ee439d142c623ca5f9ce8029f0fe1b0d2c74`  
		Last Modified: Tue, 19 May 2026 18:49:27 GMT  
		Size: 93.3 MB (93343015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd1fb820febd42b12d175f8e57ab45cb02d9d148ac872b3ff1e8d3b342c222e`  
		Last Modified: Wed, 20 May 2026 04:18:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:18a4afa97d3cc35b93a61c44c0926ab7bb705fda819dffd525e7ec7ff6cb77e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48faff7960790f6b30991b6172848a70553073e9950aadc0632d6e4eff38b0e`

```dockerfile
```

-	Layers:
	-	`sha256:18546f655f171840177a7e95e10bd9b9c34b8fecaa1eca32761bfb796f68390b`  
		Last Modified: Wed, 20 May 2026 04:18:02 GMT  
		Size: 10.6 MB (10581750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b022db9d537be15ab551f41eeb5e75b0cbf248b95a087f6d381a7602a35c67d6`  
		Last Modified: Wed, 20 May 2026 04:18:02 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:fa1784381597a8ed18151fbbcae05004578ab7f57bcb672479c68c5ab868845e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343417972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366715e7eaadba5287e46b2fa50be51ded99a227339f5006c870d181f88bc5d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:15:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 06:15:22 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 06:15:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:15:22 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 06:15:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 06:15:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c138e2e16ae5793d076cc5f5dc83794bef7dd2237bed3aea8d99c682533d9cc9`  
		Last Modified: Wed, 20 May 2026 06:05:20 GMT  
		Size: 100.7 MB (100672943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1c12b1c007dae0ded7a2c5d8a74dfe44bec08363cdf8556a245d7c8b644731`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 95.3 MB (95295509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d636b48ffeb7b711e1e5bcf0b0af86e953dc4f25d89715911640ecf241de37`  
		Last Modified: Wed, 20 May 2026 06:15:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8d9c5fe142a67a1d59f709b8c0bdd5170f4284584284d87d6e45602d07cc84bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fbd4e652c7c99ed1b6edb0154d88e8b00bbec027b6934d4b2656c2d9ae377`

```dockerfile
```

-	Layers:
	-	`sha256:56f1e8f8e051f1ec9faacb01792ea021d1e4545fb4c7550c0f98bec4c8d55f57`  
		Last Modified: Wed, 20 May 2026 06:15:44 GMT  
		Size: 10.8 MB (10757126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30b9b73dbc9482d0f4766231bf0ad71d6667d15bb52e60bd3a8d001f3e819f5`  
		Last Modified: Wed, 20 May 2026 06:15:43 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:27a0cd55e41b975b7c1bcc5601d48a98c33191e2cd33a34b38c22518f37e8e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340185944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7873f4a010baf09e04970071d6f34444db87d2fb04d018cf9d261cfd0b2fdecc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:12:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:48:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:48:50 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:48:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:48:50 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 14:13:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 14:13:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae4740f965f90ea724577a0b30441b0aa762e95b519406aaecefffd2cde70`  
		Last Modified: Wed, 20 May 2026 09:13:07 GMT  
		Size: 92.9 MB (92937768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031549f4a149afd12a0aa62ad2634135f41cb41de30ad0670c5e09695e591f0`  
		Last Modified: Tue, 19 May 2026 18:50:13 GMT  
		Size: 94.1 MB (94052228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e373bc8d300f7d65d840d53262370e11ed465e85ba1bcd6685a75a0bbe45c1d`  
		Last Modified: Wed, 20 May 2026 14:13:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1ad9c7ece66cba63a74c68b78de81934c96946ebf7f2aade5ed4b8926f861980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4a15ca5c2dc2d985f597f42a5e3b37d20881eb8c46323e9446bdc3426c98e`

```dockerfile
```

-	Layers:
	-	`sha256:e425f1b00621e33dff8dd6014c3c9c5cf9fc622a1e5c25ff8bfe8a48ead8ba0e`  
		Last Modified: Wed, 20 May 2026 14:13:48 GMT  
		Size: 10.8 MB (10781651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf2c41f152964f0e373d54b22a84a5dc71b4f3e6cad4afc652bf1d3abdd3d7c`  
		Last Modified: Wed, 20 May 2026 14:13:48 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:2fee745c2e846c3fe0cf4a86f32a4ff67291ec445b7651ba4c17edff6c38fe5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365633601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c9e7993586f04bf5a18fca364d003ac205dee26772aa67927722687dbeb444`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 00:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 13 May 2026 15:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 16:08:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 13 May 2026 16:08:37 GMT
ENV GOPATH=/go
# Wed, 13 May 2026 16:08:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2026 16:08:37 GMT
COPY /target/ / # buildkit
# Thu, 14 May 2026 10:35:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 14 May 2026 10:35:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16def90c932096937daf06d99b8e59a8b74b84aeebf2940aac17817b2f543a80`  
		Last Modified: Fri, 08 May 2026 20:37:07 GMT  
		Size: 47.8 MB (47798394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7692e383ad230da32926d42cfa98b11eb90f51caea79109b6a826b07b59addf`  
		Last Modified: Mon, 11 May 2026 00:57:03 GMT  
		Size: 25.0 MB (24956029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04052f76d54a3689ae0d16f104df08fec9ed091da2d2a2abc27589c5c3d933e7`  
		Last Modified: Tue, 12 May 2026 00:51:38 GMT  
		Size: 66.7 MB (66663509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbce5efb3f62044384ac4495e0b4dceab3ab756ff9db249c026ee1bbc4ca373`  
		Last Modified: Wed, 13 May 2026 15:20:51 GMT  
		Size: 131.7 MB (131710099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d47e378dbd0b7bf645831e9840670b418c2e00a7d67e6b9db247ed04df4c4`  
		Last Modified: Wed, 13 May 2026 16:12:01 GMT  
		Size: 94.5 MB (94505412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c33942f807c2494268e263a84c52548428dc80b22059c881fe52c36fa71b01b`  
		Last Modified: Thu, 14 May 2026 10:40:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a808425399f542d34e796fb298624886684356fbd3ed7dfdf622f471efeb2a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60744bdbea114647ed974b4415611c372ff04082c5f06cca4d11a85ecb188dc`

```dockerfile
```

-	Layers:
	-	`sha256:01cfd1d67102e7d514646821c006abeabcb0af1ae67636e6e8456fda4ef6d38a`  
		Last Modified: Thu, 14 May 2026 10:40:04 GMT  
		Size: 10.9 MB (10855334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911bfc3eca414630b84a35a80dd98b9404ad302b391ed9daad32a591491013e0`  
		Last Modified: Thu, 14 May 2026 10:40:03 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:9baaf6029c962c6f5e8bd41596fd50ac832eb5c0a51e9a3724ea0790427c3d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316887497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad923b167b722da710f90203d5884df4c8c7663eab4c28acea68d9c2d67d091d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:44 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:44 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 05:08:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 05:08:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dc30d1971b7c7a1fe17c3dfa79f0dade75a1a47c28b2d58c76d2276b9b532a`  
		Last Modified: Wed, 20 May 2026 02:46:44 GMT  
		Size: 76.0 MB (76047674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c82cd174659cb53c7768fbc8389b7b3eabb725a4a95e0bd43007eb9eef0a5b`  
		Last Modified: Tue, 19 May 2026 18:47:13 GMT  
		Size: 96.0 MB (96017021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d95c718e7126e2ae9d4017eb50326fece39bea260a88065f2289eaf091fb33`  
		Last Modified: Wed, 20 May 2026 05:09:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6f77c802bffcba05482a6b8af54251fa5880a66951870fa8cf66cee02d3acf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb23e3f7584ecb441de0906df608c36317320f5547152447fed28b61a199025`

```dockerfile
```

-	Layers:
	-	`sha256:6b441f85a9ca07c094822b0aac325abed97f88d08edd9a4ba2a2250f28779ecc`  
		Last Modified: Wed, 20 May 2026 05:09:24 GMT  
		Size: 10.6 MB (10597011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba0569cb5a777bc8acaba824a5093ba6b0ecc5252a7b202a9758ad04dd3b9f1`  
		Last Modified: Wed, 20 May 2026 05:09:24 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
