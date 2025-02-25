## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:b48c2ea93884465c7bf6c65708d3e49cf53b30a3887f64410ded77d959873fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:5f019cba43ad0dbec1bf32dc2594a0e00401c8e2cb05406f639b44372f7965a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339556016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fc9e88358a8e4940e7a29b87efbdf9f721760690468fb34f81cf73e10366d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dc29f93ae4a3e4b56a6b3e324ac4a50b328ec374686d1432617f3488c69a5f`  
		Last Modified: Tue, 25 Feb 2025 05:13:49 GMT  
		Size: 86.0 MB (85971517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc5764bfa5625e90d4c9d1c4bb7361ceb8d3451c8f3534f5e3a80e9f8aa6e4`  
		Last Modified: Wed, 19 Feb 2025 00:31:23 GMT  
		Size: 129.5 MB (129532433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4a505fcb168e1abd1151fc8765bc2bc79e1d29ee69de3a0f9a8756dce7c35`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0c5c83093e661214f2bf7da8e176f0b95d5fec5be87397a422cc5ecf64753d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b29ca5cfef6323be8694540d9e9fb0073992bb1a0de3f3f2c2cb6330527f82`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cee0f54c8c102d64095a88650cc1f01c6d6a81033c5ac7dd7aeb7396e6628`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 10.3 MB (10267086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a4d3de8b2cabde5fd8e0a05df56f699cab7b7089e7f3d810a07c4090d8fdf7`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:68ed1c3dd696e08a72bb68b38154616ddd3b01b6d96fff51fdef1ecb57ac2a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302029595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca707221a36d73e3cedf95ce974aaa645d123920f4157cfcbd362d7d82c662c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Tue, 04 Feb 2025 16:21:50 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d641c4fb5f7d6edca115cf3c6db8bc11e32ec83c49422dab7839f4914e1a2`  
		Last Modified: Wed, 05 Feb 2025 00:36:13 GMT  
		Size: 64.9 MB (64892491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbce18d551f744b2f9a445aaedbcd8c5e283783570d9da4735469555773098f`  
		Last Modified: Wed, 19 Feb 2025 01:09:24 GMT  
		Size: 122.8 MB (122798265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf714c2f9c8e71f7fc0357bc7a7b5d441ea1cf1ac4d50d656c2fa5d2b8ece60`  
		Last Modified: Wed, 19 Feb 2025 01:13:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:3a2ec0ff2c49b2bbf05e734ec1e84fe67bd3a8677fbebe8d861b9d3d07891a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10100595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523cae93e5a1f9b3471a697d251a83708920b5f8b84b985c551fc02fd4c6c4b`

```dockerfile
```

-	Layers:
	-	`sha256:ada491dc9f80a3f4ef15756fd67f2e870ce829981c3942a4f30f1e4d70235ecd`  
		Last Modified: Wed, 19 Feb 2025 01:13:00 GMT  
		Size: 10.1 MB (10073426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4878aaa17422d40af91fa3489bf4b520820a4f2acb04e7b5f7f03eb4a00086`  
		Last Modified: Wed, 19 Feb 2025 01:13:00 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b0b907b2a27ffe2cd7e6cfc3df776c788fd692021248a0f50e8025a280080c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326378121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4e7f884dbda59c21fc126fb3661b53c789046a9630d9c3511427a0ea6ad3ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f8f0990a7270606266e36ae54950c498997c10e31242c830d3106f5fd7ed4`  
		Last Modified: Wed, 05 Feb 2025 02:02:38 GMT  
		Size: 81.4 MB (81382226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5298385c49d911d309658b69d6f0a6876dfdb4d5bed9f2c1fff825ca2fb2fcdb`  
		Last Modified: Wed, 19 Feb 2025 00:40:43 GMT  
		Size: 122.4 MB (122353292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d905b978651aa6c656ce0dc724a81185ca9f4364e085f45dcb88e2a7dd8ceb`  
		Last Modified: Wed, 19 Feb 2025 00:43:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:fafdd5dd9cc3effb4b8c60cf61e219c61313053879fc2a4b5754a6aaac8ead8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e170f26e1b55572e3234d6a282f4c26e796e99a8cbbee240081b2693f2b3d59`

```dockerfile
```

-	Layers:
	-	`sha256:86b85570b88d716dfd7df720ef6b00cb40df2b55257e770fd9c885ea47c96454`  
		Last Modified: Wed, 19 Feb 2025 00:43:09 GMT  
		Size: 10.3 MB (10268658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4416271fb0f2b4e5b66b45135b9e1de02ab2d52bd2f0203101fcf461984ffb3`  
		Last Modified: Wed, 19 Feb 2025 00:43:08 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:1e5fca4543af3c0aee73dcf5d0f4a53fa11831884e77ff4ae7915e54306969fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340336146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a298fc23f24eb2ddc4bdc9f00d0a1c07419ef974f832e2b72297974509e6f9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9af4ec198fc9298147d65e6f399f6f943d41330f1c58e2faaf968b360bd5e`  
		Last Modified: Tue, 25 Feb 2025 06:14:46 GMT  
		Size: 87.4 MB (87397986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865367c21802db35d933085cc324482ddcbb8bd28bfbcd89b6ea5d6a248d00d`  
		Last Modified: Wed, 19 Feb 2025 00:31:35 GMT  
		Size: 126.2 MB (126166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc23d3755cd37e37e9559025e523c5b7a6057f1d8a20c81aed7834e3aabf7aef`  
		Last Modified: Tue, 25 Feb 2025 06:14:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ad67486e2d2fa6e240f85f5e1179c53682f4b66f122a91b7c824ef9a9033d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eeaf7c7e8f48eb0d1cd19a61fc11a74fbd37ea2811e6404173c0c4add8bee8`

```dockerfile
```

-	Layers:
	-	`sha256:23779a568b10f4324f26d3808323982f4291e1742c40a196485d4ad6ad019e45`  
		Last Modified: Tue, 25 Feb 2025 06:14:44 GMT  
		Size: 10.3 MB (10256877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2636d69ece919d3254df29f48e97ced2019dd7778fb28adf432cf8efb994d8d8`  
		Last Modified: Tue, 25 Feb 2025 06:14:43 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
