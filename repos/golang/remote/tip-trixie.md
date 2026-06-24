## `golang:tip-trixie`

```console
$ docker pull golang@sha256:548264fdbe5a954a547c06e6fae7cce9f9e88114226c1d1e4ef5b61becaad744
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
$ docker pull golang@sha256:f97828f85b279a475cfad101ba58dcdcc3189c96c24e7ee2b61a4488c42531bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347559122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebcb2962046d1fa9cc4eb3a94f784f5981ebde7c8be542d8e59ba5f06c1e91a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:17:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:19:27 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:19:27 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:19:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:27 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:19:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:19:30 GMT
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
	-	`sha256:d7cf9b4a392be785e02a359d01acd3a15c112bdb7e6217e0533f8582d5d8e961`  
		Last Modified: Wed, 24 Jun 2026 04:19:55 GMT  
		Size: 102.3 MB (102269249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ced9bfc2a0ce47376a0e89056fba2dbdc199ef992671e729f2b29cd85c5af1`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 102.6 MB (102559388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdd78cd01faea61acf6aa73c51bf4b94dec1c8c5307822b11d2180c3c968376`  
		Last Modified: Wed, 24 Jun 2026 04:19:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b377e90c03cdfd74049775572913a8a688fb7c72573335ed469aa0eba6def34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62c148a40fd5c3a101b9c0b51376f66b9ec0eaf399bb90448c5af36c4757af7`

```dockerfile
```

-	Layers:
	-	`sha256:0f70eeff604bc03631eeabb596745b5e02e9a8af971b0825c727ce15d553b89a`  
		Last Modified: Wed, 24 Jun 2026 04:19:53 GMT  
		Size: 10.8 MB (10785971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825bab8d244827094b862b76275e4a5c9de43d7a9c3105c125c9679d18a19d40`  
		Last Modified: Wed, 24 Jun 2026 04:19:52 GMT  
		Size: 29.0 KB (28971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d3207cce818c77da7e12728c1d86641d5caf5e5437e0914cf16c43178362c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303319349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ea78e01ca387afbec01190c5ba926cabaa3c215f9eef9b562baf6089b26937`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 05:17:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:20:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 05:20:48 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 05:20:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 05:20:48 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 05:20:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 05:20:51 GMT
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
	-	`sha256:c71dbe107cb4f239febfed78de873fbb0c27801637e4107a0fe8a4738db99e9a`  
		Last Modified: Wed, 24 Jun 2026 05:21:16 GMT  
		Size: 72.9 MB (72912066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6c0ac1bf1a1f35e41966874d41949d2c8d30b471f4a54f05d28249cc12bc`  
		Last Modified: Mon, 22 Jun 2026 22:45:14 GMT  
		Size: 98.3 MB (98276162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f8a1a351d596b7bcaf2a0022784dfd4ba15377ffd29a9b036c1400eb41aad5`  
		Last Modified: Wed, 24 Jun 2026 05:21:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b2ed9043f0389dda134eccb9ea66919dbff06fd90681a0b84554ea3a559c022b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62c2d77110b37f0f9fddf738e3dd2962b8a2022e17985317a360416b7c2a9c1`

```dockerfile
```

-	Layers:
	-	`sha256:bfc031080b3cf46785a5938d34bc51bc7bd91014a0e59bb709e9d706fe4ce32f`  
		Last Modified: Wed, 24 Jun 2026 05:21:15 GMT  
		Size: 10.6 MB (10581858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d745bc8b22196fc6ac8baa904e0eb100c1d0491c2dcec28bf5c8f46102a0d7`  
		Last Modified: Wed, 24 Jun 2026 05:21:14 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:47bcea6bbb8e97aab65ae373c3b6ca6cdda69a4eae199672b8c3cc2e096eaa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337672679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c72f1b3ffe9fd6812c77940e7feba5d4f4091f48a751caccedbcc47015b16fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:17:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:19:41 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:19:41 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:19:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:41 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:19:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:19:44 GMT
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
	-	`sha256:2331f237f8db599fe802d645e2938d48827d3adc720b718308bc5d8f4500a7a5`  
		Last Modified: Wed, 24 Jun 2026 04:20:11 GMT  
		Size: 98.4 MB (98415174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4f06fe9b49ab2b0e448e3bb545bf0083fe0a192a188b8354bf30a5042489`  
		Last Modified: Mon, 22 Jun 2026 22:43:15 GMT  
		Size: 97.0 MB (96959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990fe7b5c08212874cdbc3c58ce38c93669c0dc7cc74fd8fb8173b9186e329e0`  
		Last Modified: Wed, 24 Jun 2026 04:20:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:02c292e25942be39e5f06ec7c5ef82ee761046aeaad1e5ebe81fb124d51ba801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ceb9864bf3fcf462834e2d9d3bc6d3a65e780d0c5c6d141d1e1df10c104304`

```dockerfile
```

-	Layers:
	-	`sha256:3ffbc0f0cc81f9358b84e986e0dc003b1109e90b750600de2d9d0b9dcb54179d`  
		Last Modified: Wed, 24 Jun 2026 04:20:09 GMT  
		Size: 10.9 MB (10905789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc24733dfba206362be1e44dcce900e49f13b32ab4c00f32beaa24303c2bd5b`  
		Last Modified: Wed, 24 Jun 2026 04:20:09 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:41a09b1ee54581133487853db2d55f36c00178bb78bd2b50671e83e17c62f3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348500503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0553d5a2c3da0b86753114fae42dc6d451cde779b9b4cccc34ba96a6ab3be72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:17:06 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:17:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:17:06 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:17:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:17:09 GMT
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
	-	`sha256:e4994120baded3c36a20db0166f192b827b8f88159d7bc6a76a352616487798d`  
		Last Modified: Wed, 24 Jun 2026 04:17:36 GMT  
		Size: 100.7 MB (100710794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675e2fd1600788af1a6ae5db185dc20a1f52bf11f13c9afd16f6795c307c09a`  
		Last Modified: Mon, 22 Jun 2026 22:41:13 GMT  
		Size: 100.3 MB (100338995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abebd7eb2e559abe0dfa3d275dc4dba9b32cda29c712724dc73bd9897678656`  
		Last Modified: Wed, 24 Jun 2026 04:17:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2dba7856fa766806c8bf664d6716b73bd17c1249e4b64f1369073576061b0e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab486c1adfde098c6297a8d9cb399b2cbb5a3760613189e16fe5deee6e544781`

```dockerfile
```

-	Layers:
	-	`sha256:ae623524a9f09390bd2c534de4105fdf7d54017190df6481c83e2c8718471932`  
		Last Modified: Wed, 24 Jun 2026 04:17:34 GMT  
		Size: 10.8 MB (10757234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75fb7e17a558ecf0da558bb7b819691e1d8cc44d46d207756d5521c02f13d92c`  
		Last Modified: Wed, 24 Jun 2026 04:17:34 GMT  
		Size: 28.9 KB (28930 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:029711edbb35129f07cc2c6855b12a9ebb95fade0c12d7a349cc3a62803ed0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345098807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678007cb4c5b22bd8742a519ce53f7e25dfbb022120f19795fd0df91716ac070`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:41:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:41:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ae5d968e23911f86d428bf6a67c0599a9449efc6170bd77e591b9eaf7c90d`  
		Last Modified: Thu, 11 Jun 2026 04:45:58 GMT  
		Size: 27.0 MB (27021977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a68ee36453f6ba3cb200c7dbe5182e1d61ba54c525dacec15d40f163304257`  
		Last Modified: Thu, 11 Jun 2026 10:28:58 GMT  
		Size: 73.1 MB (73050891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057fd15b7ca117f12314b7318acb10a98d15767505a892e8ccdf2f4fa1e2028`  
		Last Modified: Thu, 11 Jun 2026 12:51:34 GMT  
		Size: 92.9 MB (92942557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70a3316b3905923ad611a6c49ef41a8febad5f35cea9ec0a2d4d25d3ae02c6`  
		Last Modified: Mon, 22 Jun 2026 22:42:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:149d13fd52e83cc8176041649ad15dc93bbd8bb75b9e77a5da9a83e635bf4d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85da0579463cdc66e1a282159c3e15e54f250d945250a9b974e73c98a759d0a8`

```dockerfile
```

-	Layers:
	-	`sha256:7296e357dfe2794fadb8db92c5daa4b29bba872b8caffc76af6ea928d40253f1`  
		Last Modified: Mon, 22 Jun 2026 22:42:18 GMT  
		Size: 10.8 MB (10781759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d942b7d06d7117b20068a9083b8aebbfd47f338cdef588022a892abb288d7a2d`  
		Last Modified: Mon, 22 Jun 2026 22:42:17 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:9fce34e58952038cfa3296e478e81f54f5e11fe418e259452e6caa3919a5cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370589400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa2b7d24df5793f5fa6967ed2b93faff746e296dd6fc7e3fe7bc7168a947f31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 04:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 17:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 17:11:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 06:42:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 06:42:10 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 06:42:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 06:42:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d828555072267505fd8c01bd511aa2e85b57db4591d7af1c1c5df9ca568aac0`  
		Last Modified: Thu, 11 Jun 2026 02:59:31 GMT  
		Size: 47.8 MB (47802538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d2b568729c379fb90b9e1cebbb6d837dbce6619d04c8fefdbc963a4896afbc`  
		Last Modified: Sat, 13 Jun 2026 04:46:38 GMT  
		Size: 25.0 MB (24968420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa945f549d69516e9a84b82f6960a728d5cfcff0ade0170a3411238a96eb3a92`  
		Last Modified: Sun, 14 Jun 2026 17:09:04 GMT  
		Size: 66.7 MB (66673413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e605738ec26caec03266e5fc0b8ff626025c1880c9f5890af814476789666`  
		Last Modified: Mon, 15 Jun 2026 17:21:49 GMT  
		Size: 131.7 MB (131720183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dbe4000f17519e4596fa5552054546772fb32ed45b8efd349e760fdf7b0b1f`  
		Last Modified: Tue, 16 Jun 2026 06:49:17 GMT  
		Size: 99.4 MB (99424689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca9f87ee35443e866dc4581fc76f95d1339b7fbe471b7d99a5bc0d7e03fe958`  
		Last Modified: Tue, 16 Jun 2026 06:48:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:22ccca09fd084f24ca066486114acf62549c744741261f5f2ca2f0d8fee68855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e93e63027c3bbe0baecce99a7a49a6ae3499db3b85f0df4e7284ef867a3f09`

```dockerfile
```

-	Layers:
	-	`sha256:bed1c2851b51c2bad829ede8cf5890327427159c2df5e2c7c64c5b558f53e7a7`  
		Last Modified: Tue, 16 Jun 2026 06:49:02 GMT  
		Size: 10.9 MB (10855592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b68621c213b6e875eb8f152b247c7422b7357820c51c32c272b0122c3ff365`  
		Last Modified: Tue, 16 Jun 2026 06:48:58 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:1748e8d5f984bf21647533267ef69c2a04e0e6e3e5cbf1d6948fd295ac3c3f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321926589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beb106095914eef6bad2e2dc3741c6a8dcbe61a0d42927cc45254e54a39393a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 05:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:44:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:44:37 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 09:38:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 09:38:24 GMT
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
	-	`sha256:acf892c33722ea8cde689a58c97266129c7df0afdd2fa621bb19aaabfd5a4c50`  
		Last Modified: Wed, 24 Jun 2026 05:20:01 GMT  
		Size: 76.1 MB (76080942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf953c950bf774a1558a2610c27217993faad44f113fb37ad0ee60aef8db0d`  
		Last Modified: Mon, 22 Jun 2026 22:44:49 GMT  
		Size: 101.0 MB (101009813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b739c578579107da21661938cefdc8d7d8557fa380bad1c8a53443dd4a927e54`  
		Last Modified: Wed, 24 Jun 2026 09:38:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:091a706020c11cf51831ca8385fee5053fc99a5c02a8a7760f8dd0c99ee79148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae40b3ec7e810e0ee4651f69e7b8d090f193e29f87835fb0761f47d565ec000`

```dockerfile
```

-	Layers:
	-	`sha256:0e60f9045b46637ed38900949ac5e81fc5d7bcf43392e6bb16e63f1734cee331`  
		Last Modified: Wed, 24 Jun 2026 09:39:00 GMT  
		Size: 10.6 MB (10597119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb0b1768a81af53fe9a6e6abc73f7213e88f71607c5553904b0206fe21650e4`  
		Last Modified: Wed, 24 Jun 2026 09:39:00 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
