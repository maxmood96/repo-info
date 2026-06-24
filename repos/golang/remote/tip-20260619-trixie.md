## `golang:tip-20260619-trixie`

```console
$ docker pull golang@sha256:03c74cadc28b131de65fb557b19c732c7bae1d9a32e7edb1f8da0f29abab4b99
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

### `golang:tip-20260619-trixie` - linux; amd64

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

### `golang:tip-20260619-trixie` - unknown; unknown

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

### `golang:tip-20260619-trixie` - linux; arm variant v7

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

### `golang:tip-20260619-trixie` - unknown; unknown

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

### `golang:tip-20260619-trixie` - linux; arm64 variant v8

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

### `golang:tip-20260619-trixie` - unknown; unknown

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

### `golang:tip-20260619-trixie` - linux; 386

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

### `golang:tip-20260619-trixie` - unknown; unknown

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

### `golang:tip-20260619-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:3998afffee8a22022243844c36bbb482b38424c958ba94829b5dce58c4559740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345124446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2be907e69fa24e63451ece9a2de1d8c94ab3a83a93216ae4d0cb218e873c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 09:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 11:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 15:29:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 15:29:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f80d2a3204cde8ea1e7cf5156c0b0e385216cbdcc894bd75c3d81ec51271e`  
		Last Modified: Wed, 24 Jun 2026 03:26:58 GMT  
		Size: 27.0 MB (27022027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d839bd23ba3483deaa2fe15c35bcf5914f88e1187bd81dc630463eccbfa83ab`  
		Last Modified: Wed, 24 Jun 2026 09:11:50 GMT  
		Size: 73.0 MB (73042732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ed5e38143201332b94deb1de4d86e0ea7e941dbc7b5d2be2a83cc8b919f4fc`  
		Last Modified: Wed, 24 Jun 2026 11:44:51 GMT  
		Size: 93.0 MB (92976176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04cdd8261955889bf060cde579c9248c9fbfe9d7fb3dd9affc23080d37909e2`  
		Last Modified: Wed, 24 Jun 2026 15:30:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:549f4f97cd61519b0b4e06c00fb9de63c7ba82bdbcc355a2f0a1c72bb27a2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61371ea10e42cc927981aeda905539fa70b0b5ca8a96ace168cb461c93135c56`

```dockerfile
```

-	Layers:
	-	`sha256:26391af5a5a26973e5207943314fa56584d346b89b8a8cb80e80c9b7e88a661d`  
		Last Modified: Wed, 24 Jun 2026 15:30:19 GMT  
		Size: 10.8 MB (10781759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5ea701191dd883702fd6938aa9f06e38bb47804d6d931dd338d0ceb05472a1c`  
		Last Modified: Wed, 24 Jun 2026 15:30:19 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-trixie` - linux; s390x

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

### `golang:tip-20260619-trixie` - unknown; unknown

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
