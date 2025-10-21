## `golang:tip`

```console
$ docker pull golang@sha256:b06626a2bfa7bdce549bff2b3bb4a6b27ad38bfe811d6df6c46c028fb0dac9cc
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
$ docker pull golang@sha256:a5382494e26141ea5f5d2b765251bf1237776f2bc490d920e099b7009b729002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335411720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb440a9855a8ca1b4194bdc5866ded22ebf464975e5c9953b6eea93ab7dfa565`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a20645b75da3eed5d944c0669145843ece564927dea79268517333c791e7b0`  
		Last Modified: Mon, 13 Oct 2025 23:11:28 GMT  
		Size: 102.1 MB (102088340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5533a24a9e37fce0b0e949796f7edef8b1aecc8af44711d2767f0566cd2c9677`  
		Last Modified: Mon, 13 Oct 2025 21:02:56 GMT  
		Size: 90.6 MB (90638837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc1a489b9aa89d9f0d3ebb45cd00f077c1e7dfe3834279e929c9115a37d4db`  
		Last Modified: Mon, 13 Oct 2025 23:11:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:040eb27f881b7bcd5e62e6ca55ba7c4ab25d41690f69d2b4ff077cd6a5efcf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d38b4c8a91eb318d190c7b7e18d4aff138784898b58625e2a5b9c3d1c4048a`

```dockerfile
```

-	Layers:
	-	`sha256:4b83238a201807863c92be5302d6fd62f897d9c39a3dc7cd320d7bde862419f6`  
		Last Modified: Tue, 14 Oct 2025 02:23:58 GMT  
		Size: 10.8 MB (10784406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d350c035133b30abd56dd1b498903a12b2d55affac77f2b126435b2bdadfb3b2`  
		Last Modified: Tue, 14 Oct 2025 02:23:59 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:e4e200c60610948f29a48759ca66b55119e054db1cf0a5ee2d8f24626274e7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291854921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc89d3ad0ab9f6c1da059eab23bd61de8cd8e408113d32b3c0549b464cd051e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980cee2e23d26ccf9098baf202141f33b3a05722868ca329f4612e3730088f7`  
		Last Modified: Tue, 21 Oct 2025 05:19:41 GMT  
		Size: 72.7 MB (72733704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b3f77f198194af8440022630b5f3555d19874bc1b8dcfcdeb4ff1346ed16b`  
		Last Modified: Mon, 13 Oct 2025 18:23:46 GMT  
		Size: 87.1 MB (87074499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36578683c2117ca2df2480f2c5fe0941c96485445068ce5a3cd88bf507bbe55a`  
		Last Modified: Tue, 21 Oct 2025 06:22:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:62da2a68946f70a587653e505bcbae81e4ac0952ddcab5e3b0a74d5690b11c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7398910eb519df50aba27df3ab81ed299708e7c7e4095a5a0df03cafc8883f`

```dockerfile
```

-	Layers:
	-	`sha256:9bd0994ae6517060c6944f9fd7348830e25d696e79344e8d3dd61d706a2d5050`  
		Last Modified: Tue, 21 Oct 2025 08:24:22 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b0e6f7c324c197c4f9220f8f62ff3c528ede27d90e7220123885119be94a42`  
		Last Modified: Tue, 21 Oct 2025 08:24:23 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ced91d4acfe9c7db1dc2eb8eeecb1c2bdc9f7ab7069a1ee499ff15e200fe30b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326526845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d99f18d61f9a91847aa7eb6465a70ffe59fc229b35fac4af661b2c27ab3621`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a186c14ef6e6e568acaf6d3ac17dae1cf3538072ac97ad3700b52b114917ee2`  
		Last Modified: Tue, 21 Oct 2025 04:21:21 GMT  
		Size: 98.2 MB (98234280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad87b7b196d7850da55968ab4ea8d2e74337f796a2dda3e1e502c848906a7`  
		Last Modified: Mon, 13 Oct 2025 18:26:56 GMT  
		Size: 86.0 MB (86042092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d1300efb9f15f98696a541eba3036c64fde21ffcd63c3452811ff5e9953e3`  
		Last Modified: Tue, 21 Oct 2025 04:21:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:500437bf139be178a6112a9f40c0bfb6776233034b017fff490dd7f3e537aee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e109798170d7cc16fe2b928783614a8b16464ad63d205a2504e98921c39e4c`

```dockerfile
```

-	Layers:
	-	`sha256:2f307b5720003556632110d100929b876eed36d0bf8894a4ba9d969fb1f0ebfd`  
		Last Modified: Tue, 21 Oct 2025 08:24:31 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee52ec73498adfb1a9575a625e3ab3f029761de81d4e85eb811db7504d884f50`  
		Last Modified: Tue, 21 Oct 2025 08:24:32 GMT  
		Size: 29.2 KB (29166 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:28c746a4ecc7984664b92e45939ca0a8e2a6450e12a7516f102bc6797aadc2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336756536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0b029f411e8cb662c191bd67aed8c9d8edc80562157fe28f86de9b08c0b969`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19e7e954c8f25ab0ef04cd3e168e1dccaab6cfd9a3a46ffa555ba4bf34e885`  
		Last Modified: Tue, 21 Oct 2025 11:37:38 GMT  
		Size: 100.5 MB (100532990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc457dc23d2f2501ae16881398a5b91dd66079c5042a578bb1e723668e7c145`  
		Last Modified: Mon, 13 Oct 2025 21:20:42 GMT  
		Size: 88.9 MB (88852096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5a702901cda8cda4d7fcf21ed965d669da2f72fd69f9b099d4761880b4a26`  
		Last Modified: Tue, 21 Oct 2025 04:27:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:33729d316fa8e8b7b8e0b3e2c53da025c99e678e588d3106849a091de28f2c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57832067a1bc21db4f3946f409bae3ebc6d1bb8ad8ea7fb9345b3e20f32acdd7`

```dockerfile
```

-	Layers:
	-	`sha256:1929e99591dad1a05178cd9ca170617c52339ba736a23decb45d60a2ddecb119`  
		Last Modified: Tue, 21 Oct 2025 11:24:40 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8db92b513fed00a8a2236b98165e8fd4d367031239321ae2cd91fe19b0249e75`  
		Last Modified: Tue, 21 Oct 2025 11:24:41 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:bc82323ffff3ada7aef163565fb1c3be10b58dda2b305fcd66378d64a891bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333376268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c11a2b284e1175111a02d99740f1e14ea99d8c4d9c9fcf8f53ce0a2e7d0df7a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed492992022fa9e4a253b427574c9ab21d82072f73e353ad6f09e1555a92cc4`  
		Last Modified: Wed, 01 Oct 2025 11:14:56 GMT  
		Size: 73.0 MB (73034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39ff1a0b943456854e6b1ed7d946a7e67cf44c76fe8ec18f870bf569ea577a6`  
		Last Modified: Mon, 13 Oct 2025 18:24:18 GMT  
		Size: 92.8 MB (92794871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a59992ca0e08825ec7e153d7b4765b1eda5f370c39d6ec414f6606e002f92a`  
		Last Modified: Mon, 13 Oct 2025 18:24:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a6633968c6f319489862182820e6b29767dcbff018dc8a10e9736bea6b4a5de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60181d9a6566f2459ba30bfc1e48f519222ecff13b38cf766c43f027178d3ea7`

```dockerfile
```

-	Layers:
	-	`sha256:8a3cee19dab0c7553961899b3aab8488062a2fc9e70c814269140fb74a5a55df`  
		Last Modified: Tue, 14 Oct 2025 02:24:30 GMT  
		Size: 10.8 MB (10780192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5acdd1ca779b177d8ead0231d0cb3b84cdcb10fad8ebb5c20e6f9084aeface`  
		Last Modified: Tue, 14 Oct 2025 02:24:31 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:c2ad7ba1a4c1d7b8219649e1c4c3ded7889ac2d7ed0607248fba2345c4c8ebb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358859190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387129908e565149a2d060f48b4de01584c48a5d0df1cd3bfe6a3504493d50d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c645409e32b37950d400f06f75fff87e9a716322f248e5d01d290689226a51f`  
		Last Modified: Sat, 04 Oct 2025 03:44:05 GMT  
		Size: 66.7 MB (66659977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146033d470e9e45a40f2f8858ac379252d8b815c5b3ca04f3f509638a2ed95db`  
		Last Modified: Sat, 04 Oct 2025 11:31:35 GMT  
		Size: 131.6 MB (131577430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2d5d7683a75ce062ee755840019c59bf7ca74ff155b360004efb2f79df7164`  
		Last Modified: Wed, 15 Oct 2025 23:27:21 GMT  
		Size: 87.9 MB (87898833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df439653f7b652e8205d268b8e47de691d128119856a5ede128ab5f557d915d`  
		Last Modified: Wed, 15 Oct 2025 23:27:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:77aacc66cf22fd81e105b913d385dc20a6b98b5b1bf3595f1a810ee72bfa7fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5162af81b0124ba5fc57dd97130a1f9bfdcbd5c31e377e120e3d65b8854106d2`

```dockerfile
```

-	Layers:
	-	`sha256:e081f0239efe9282f9c6a5a698f1b2543b0bd1e6fb0b0fec65fbf68e6bca9762`  
		Last Modified: Thu, 16 Oct 2025 02:23:47 GMT  
		Size: 10.9 MB (10854025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9424e6b4b035a9f098e6d8043e203664094b66d594910b67b7f2d20b17a4dc`  
		Last Modified: Thu, 16 Oct 2025 02:23:48 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:4cfebce8e9ced5bf36f4960687d503699fce38831eed50917522aa23c30e5a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309464953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ef4fecf6fb73aaf59fec6caf30c6017c8efc998a34e9238a579a2f8a04428`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2360823d72f62f7ab99d1125b961476d915cd531da8e87d42d3767dfd3b86d6`  
		Last Modified: Tue, 30 Sep 2025 15:54:22 GMT  
		Size: 68.6 MB (68637856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a77bd0f38ef8a06aa5c038a198543d87d293c0d046b35c3e41c08fb8c27b73`  
		Last Modified: Tue, 30 Sep 2025 23:49:14 GMT  
		Size: 75.9 MB (75901079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb375f85b16f323994bc2fb7d3430268da4ef6454a80ec345f8bfd588fc5195`  
		Last Modified: Mon, 13 Oct 2025 18:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:49d2148238b32cf5c6328ab07d30e9c1a1227601d8ee2cc303f3e8b13bc401bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa726bf78276824b0540f6c7dbdf1cf29ebf9f09b17251ba33b6052e836d6b0`

```dockerfile
```

-	Layers:
	-	`sha256:253c24c55a6d1c77842dcaf206878316fc2b6a077ccec4472c120473fc2a6650`  
		Last Modified: Tue, 14 Oct 2025 02:24:40 GMT  
		Size: 10.6 MB (10594806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a955de6f99e604d619bffa91468611598dec1550e0b9fd454cf5023ea60d5ff`  
		Last Modified: Tue, 14 Oct 2025 02:24:42 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
