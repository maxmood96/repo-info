## `golang:tip-20260517-bookworm`

```console
$ docker pull golang@sha256:b355be0997cb6f27b59c918221b72d80d55278c81b3db4d24a5d3717911eff9d
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

### `golang:tip-20260517-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:1bf51504f75ec90cb83accd8fa67f5301e2ca69075f87cbd83a751f69e18f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333306725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabebce39e80a5e547186d326a28653e5c8ec38dea34dd17dedd84ea1704faff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:44:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:20 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:20 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:46:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:46:22 GMT
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
	-	`sha256:15ea54fec3639c50241e9e85a10a0a5c11d05399853b156e1f05b924a0217afc`  
		Last Modified: Tue, 19 May 2026 18:46:50 GMT  
		Size: 98.9 MB (98893712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6616f3853b3ecfbe6802f0a5bc39a71a89535589f78590596712ece3ecb87a81`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 97.5 MB (97484964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976f0902a8b81a455306f44a2c9c27621fff7befdfdfa096156c86c0acf6d8b`  
		Last Modified: Tue, 19 May 2026 18:46:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1294bd862695d5d491bb7f5f03a6ad912c85ecfae8f95049a46abca95ed5040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e604fba5330b81ddd188bbec0b38247263eebe88b068b43f3d641341b37bbc`

```dockerfile
```

-	Layers:
	-	`sha256:d2bbc3ca5269502cfcaaccacb322484b94eae5aba0b5e0c429a2f88ba8dc5877`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fc378cd53b7587616ca0c96a6205ca4253858a7d6d059238f0744d8e06cdd6`  
		Last Modified: Tue, 19 May 2026 18:46:47 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:0fe20730509b3ae9455eaa4aa6889fd9c2e54d5b3d300891456ff5d6c3649930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290479958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace445c0823e65b023d1ab36682ecda3fa90c3abcbd5686b476e348564e095f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:49:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:49:21 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:49:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:49:21 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:49:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:49:24 GMT
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
	-	`sha256:eeb5e22520e2354db76d1c8562b2d5570c0604b53edc48ece220ccdf461077d7`  
		Last Modified: Tue, 19 May 2026 18:49:48 GMT  
		Size: 71.3 MB (71329154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5478a8019bc908653f4fe6a66ee439d142c623ca5f9ce8029f0fe1b0d2c74`  
		Last Modified: Tue, 19 May 2026 18:49:27 GMT  
		Size: 93.3 MB (93343015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321aa33a35803a2d93ce5663744a99ba6ad158bdc8a5865ad0f18275b336b40d`  
		Last Modified: Tue, 19 May 2026 18:49:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:677255181dc78c40f3cf560959c6d8bda6bccfbfc3fac911944fb9b0240dbae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8707334f3d3dbdbc96c183667fe9c00c78359bf3c475dbcc3b938ec0607f016`

```dockerfile
```

-	Layers:
	-	`sha256:e16413ed9c775b43e756bb4db917bfda87623e8bf049bcaa2c074752aec74156`  
		Last Modified: Tue, 19 May 2026 18:49:47 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6475aa9c90b4397c0e64a91cec68c684eab961086db8cce606c79f6b2a8254f3`  
		Last Modified: Tue, 19 May 2026 18:49:46 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1a3706686afe5d14acf6c8095595307210474eb057a40b866d3dcd9786d10563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315255912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2560b7226850ebb8823c04491232936533e4479deed9e407a06200c831fb357`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 May 2026 02:19:37 GMT
ENV GOPATH=/go
# Wed, 20 May 2026 02:19:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:19:37 GMT
COPY /target/ / # buildkit
# Wed, 20 May 2026 02:19:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 20 May 2026 02:19:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb14b640a36236c6c116254b56d6f6dc3bf5a116b2ed02892f75505e68017e40`  
		Last Modified: Wed, 20 May 2026 02:20:05 GMT  
		Size: 86.6 MB (86553863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ad482d2898f832f866a10e8b2d7cae0b36c78a58ed7da81be2817260f57a4`  
		Last Modified: Tue, 19 May 2026 18:45:10 GMT  
		Size: 92.2 MB (92221410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd922d2d7a3d27fd058cb30752b71947eeea07f4bf278da1a4f8e75fcad8c1ea`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7ad0abc1df9e019225e42ed4a54bb2fefeffb377f600e3e862fdd50332c8975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f3b01ac59c45d74839dc13ad58b44726b92c71508fe49a787ef282e03b118f`

```dockerfile
```

-	Layers:
	-	`sha256:df8d8b7d317d4b07156880381501fb2532731a80c6e2328dd2906325cd24510e`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece06cf1bf3491512876e65395885e920ad0e8bfe77218dcd6d77771b8a0e894`  
		Last Modified: Wed, 20 May 2026 02:20:03 GMT  
		Size: 28.5 KB (28520 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; 386

```console
$ docker pull golang@sha256:19027551b6fd74961b90fd7c8d3b9dbee4c0e8077ada9107873f5696c3a30fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331805864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd54557e227d6d08a5258ce6a20e489d043c6da035c5d801bb5dff4a1bb2d1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 18:47:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:47:37 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:47:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:47:37 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:47:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:47:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c4c78b842a600b86f5f6446efc3bd0e383975b503d9d424b2fa6514ef50eb2`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 24.9 MB (24875736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd29fc1efdeca894dc5760aafe435a0b88e33948dc45f4dbd0a3c9db72c550`  
		Last Modified: Fri, 08 May 2026 23:05:03 GMT  
		Size: 66.2 MB (66235145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a62bdc0d06980e10dbd31e0cdf9f08d15002cc5c00870ab2272dbe8f3edd39`  
		Last Modified: Tue, 19 May 2026 18:48:05 GMT  
		Size: 95.9 MB (95921518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1c12b1c007dae0ded7a2c5d8a74dfe44bec08363cdf8556a245d7c8b644731`  
		Last Modified: Tue, 19 May 2026 18:46:48 GMT  
		Size: 95.3 MB (95295509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527f4f2bae867589b6a33666c00086344f80b9cda6802bf86191ef8d501b34a2`  
		Last Modified: Tue, 19 May 2026 18:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f5da203f2ad67e8c80ab2f933bcbae2eaa03496ae1ef6e552786320a483b6410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68982ff11f803b731a1aaa7c911908d54e64d313df9fafe5bdb0dade80688236`

```dockerfile
```

-	Layers:
	-	`sha256:e9faab57a423072a62ffbeb61e0f924b0817b3ed5531494b768004fb971deda6`  
		Last Modified: Tue, 19 May 2026 18:48:03 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd583b0910f8c8f2f06ce102f0b5be3fd092ec18e85a476ddee2691de24b3619`  
		Last Modified: Tue, 19 May 2026 18:48:02 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d2ef791c7e1a07156dbda90309b4382051a39513a3ff7d831205a7423c2042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296946128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05f42bb524fa3ee175383330f4899a774dea84fabbb9a754924d3ec1e3eddb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 06:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 11:38:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 12:25:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 19:06:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 19:06:47 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 19:06:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 19:06:47 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 19:07:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08baa8fe1f531703c14c631b772a987ffc44ae832951ae77c2cf756cd9309b97`  
		Last Modified: Fri, 08 May 2026 18:19:35 GMT  
		Size: 48.8 MB (48782513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35895719420bc7ff8be1345d21e6969bcbf53abcec5b59c476a0fa55636de`  
		Last Modified: Sat, 09 May 2026 06:28:59 GMT  
		Size: 23.6 MB (23615685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6733e62261bdef4b105b9d3a88929418fe62b78559d54a4e8e5768eaa929d6`  
		Last Modified: Sat, 09 May 2026 11:39:51 GMT  
		Size: 63.3 MB (63309897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0597812d9d9ff7a1f06052e0ac78d38dc20231c03c4d4c2602a450e3436a8b`  
		Last Modified: Sat, 09 May 2026 12:27:10 GMT  
		Size: 70.1 MB (70085449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53f20e8901af388e8277adb933a3ae58abffbc3e51d3a641b11354bd33941f9`  
		Last Modified: Tue, 19 May 2026 19:09:00 GMT  
		Size: 91.2 MB (91152426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089d8b95867f43df47dbc53a4ac603d917c826735bb3d803620343f71a9d2a55`  
		Last Modified: Tue, 19 May 2026 19:08:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:17ca810fef108092869dd0137e33d2865aea416f7b0fc599c4f46769f196f6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7897ad8765d1e221853bde31ef8a268961443ae6f331a206e66377f55ff28d20`

```dockerfile
```

-	Layers:
	-	`sha256:f962e134604c37e7f755ff4a8727256bb2d03cbc96bae8128340e023ac54b2d5`  
		Last Modified: Tue, 19 May 2026 19:08:50 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:0b8c8aa634ccd2c84173a437de2e0df5ae406d1e4240917910f285ce9e34ea9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332404392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4211370d155def5c3ad28506b68ffc0a7c924bd9d783640e0c271b7bc70f68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 06:12:44 GMT
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
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76bedc371abd17d2a145cc444214f9d4db5b827f6b018dfa08217a285aa62a4`  
		Last Modified: Fri, 08 May 2026 22:30:50 GMT  
		Size: 25.7 MB (25679486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12437260b341898b5eafdacd454cf094e6357253f008361a2200d2d98887726`  
		Last Modified: Sat, 09 May 2026 03:27:08 GMT  
		Size: 69.8 MB (69846587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ec4dbf644bcf257e161f5313a10dd6252193021f042ed6183f14c9719379df`  
		Last Modified: Sat, 09 May 2026 06:13:40 GMT  
		Size: 90.5 MB (90489146 bytes)  
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

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:60ae3477437ea3d6d78c03934155ee430f10821542fc6ca2ba629af9de731bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687bdc33cebf0507f6c7a14d02e8a59001b677d8142740ecf3ba5104ffcc9092`

```dockerfile
```

-	Layers:
	-	`sha256:78b491cd5c6fb68271c7be8b5e5935761cd160a2738c4269e41da4a0891b7b3a`  
		Last Modified: Tue, 19 May 2026 18:50:11 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03754ac74b2b6a5a58febd967375127379d77f4881196cbe945a347f5a065295`  
		Last Modified: Tue, 19 May 2026 18:50:10 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260517-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8a5178b625c3ec573159c5851518ce730aca10b94e9a75fc5981d9c5bba40c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299782685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0705229bb43171a6087b01630e2c62b9576ca13686b1b5899d5b5deedae29e1f`
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
# Tue, 19 May 2026 18:46:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 May 2026 18:46:47 GMT
ENV GOPATH=/go
# Tue, 19 May 2026 18:46:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 18:46:47 GMT
COPY /target/ / # buildkit
# Tue, 19 May 2026 18:46:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 19 May 2026 18:46:49 GMT
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
	-	`sha256:58c82cd174659cb53c7768fbc8389b7b3eabb725a4a95e0bd43007eb9eef0a5b`  
		Last Modified: Tue, 19 May 2026 18:47:13 GMT  
		Size: 96.0 MB (96017021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a40c1c41033f5a04d99bd232799d846fa68c988b7ee6db56d2004890a39d159`  
		Last Modified: Tue, 19 May 2026 18:47:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260517-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3843fb558510edadea4b03ef0926598b9acaf93fed9fce9e79a84733ea7e9711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73efd904be76ecac8f8ce1cf2a431e08afa484f7f4d38f48e8803c286de0d654`

```dockerfile
```

-	Layers:
	-	`sha256:8df51454c1e8292225561f6150e58204849c3b2a70145c01e90156f69abc3ba9`  
		Last Modified: Tue, 19 May 2026 18:47:17 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b26a1df71e55050d689352b1433f232f855a196171936dfe7876049c5c653eed`  
		Last Modified: Tue, 19 May 2026 18:47:16 GMT  
		Size: 28.2 KB (28213 bytes)  
		MIME: application/vnd.in-toto+json
