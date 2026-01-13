## `golang:1-bookworm`

```console
$ docker pull golang@sha256:93760d0a33d57d7a9e635803f6f5642f3da57296fc777030434cd0d3cb04a956
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:8da4c17b6cb6fb3d645e9510444b78ef0855ee24d67cf6200831ca19c13594ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289499355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184304778316cc55ed98da8455fc80ca053956afecd10d28c57c33fdcd7df347`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:53 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:51:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:51:53 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:51:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:51:53 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:51:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:51:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:38 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38536feb7ac4cc0a822ba6a2aacf88899f14f90a9fd0f73ad08507189d712f94`  
		Last Modified: Tue, 13 Jan 2026 04:52:32 GMT  
		Size: 92.4 MB (92433561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be202417b238c354d2e10eda3603156fff2a6cdd4f090ee120273a31a213e361`  
		Last Modified: Tue, 13 Jan 2026 04:52:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:84468ef44727efacc6d9d2afca40478c8fa2decdab7897819f40a8f74da0ceea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0a19a72d21681f7b2e88c4babf9272ab3a0718386f6289ff916e0fac7b0163`

```dockerfile
```

-	Layers:
	-	`sha256:4228a5bdffe7e93140a32fbdebb0ee38baaa0c2017306b953f977485b0cef0f9`  
		Last Modified: Tue, 13 Jan 2026 06:24:19 GMT  
		Size: 10.5 MB (10496383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1673d5da7dd9a6a28340e02bf9a649ff771dd9b07122d646656412899702b9bb`  
		Last Modified: Tue, 13 Jan 2026 06:24:19 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:9e37bfc3b9d5aa99dbbe5be02f2ca9e6080135e0f64d951d5dd63992c09e60ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251153255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c6295d004167a8c5c33f725e167bb5fec010216a625270841907e2b800fabf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:20:53 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 05:20:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:20:53 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:20:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:20:53 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:20:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:15 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:25 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:12 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179428a4c4a0806b1c3107291d4edeab994573cbd759ac5f8e278e47e287f809`  
		Last Modified: Tue, 13 Jan 2026 05:21:30 GMT  
		Size: 66.3 MB (66288696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655a62a2d1048eac885d7eedd123aa296813c30a678f8fc8656b34d2726b8e4b`  
		Last Modified: Tue, 13 Jan 2026 05:21:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:05a9ca9f60ac51b2a5720f90f1b11fbe617a68e135332dcc3c6427d77c73f191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eaece07d6b00b15d03a44c359f836ed67b8eb6a3dc569cf9833421a58e151a`

```dockerfile
```

-	Layers:
	-	`sha256:28dc92c64c9d68b10b3362cc894f3ec77635f8b33c1235ddc01842bdec11c841`  
		Last Modified: Tue, 13 Jan 2026 06:24:28 GMT  
		Size: 10.3 MB (10303097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eada957992044ec5aea4457c5cf182d7e04cdfdf1233abf20d96a9524dd442ed`  
		Last Modified: Tue, 13 Jan 2026 06:24:29 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6402b8db13f79afded7f9264e7cec241e4d9685af7cd29c9efc2f2b24461d3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280607621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe28da521a74fcaf78a654f8421581dac98e043eebe6b289004126e9d1f598`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:53:32 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:53:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:53:32 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:53:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:53:32 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:53:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:53:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d85501cd63a5d1b44f7f3fcb036fc9f6c9d4a9fd4bba527925eb1c3a900fa50`  
		Last Modified: Tue, 13 Jan 2026 04:54:26 GMT  
		Size: 86.5 MB (86506198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46da1a3f8fb8c0f3865cf4d6c90934e4fb74c45e4b1c54517d099a18554dd20`  
		Last Modified: Tue, 13 Jan 2026 04:54:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7b5bab3d06db966065d75d2b6ebfd9cc288ab3566c2fde821b12c2425a1c883e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e660c1ead456ed74b6bcafaab4cb8ab621ddb7b156f45176fc42e5710e5e375`

```dockerfile
```

-	Layers:
	-	`sha256:01ade88377e6aefd79267585220f4a9ce4df6e183241ad7264cfc1a7d1d6ce50`  
		Last Modified: Tue, 13 Jan 2026 06:24:38 GMT  
		Size: 10.5 MB (10524231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a74e14f67f4c552e7acd0f56cf996b4a382880426220ab78d2bbeeb002ea72f`  
		Last Modified: Tue, 13 Jan 2026 06:24:39 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a23c7a8e34583b5beacc65d5956acecc3932d8fcd7c987141248117a0644836c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289305113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731772eb08133adf74f1f74cd569f4110f42c54fd577a9f1da6022152323c6c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:58:24 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 03:58:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 03:58:24 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 03:58:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:58:24 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 03:58:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 03:58:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:23 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:50 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05def939697e31c8901c8a952062b72614c708fd44e768f5c5f11c36e1f0b36`  
		Last Modified: Tue, 13 Jan 2026 03:59:08 GMT  
		Size: 89.9 MB (89858833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2ac38b629ecd41f2633d3e0448f39e3d0df879fad35cca3f2f4f45fd5e34d0`  
		Last Modified: Tue, 13 Jan 2026 03:58:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fc84a241f873b8bd1964eb3f7d6a3ac34e6f972508fb29138372faf817a8a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f461fa8278fb0b9000693838778417a0c59777eebebf7f6408da72b25ae32c80`

```dockerfile
```

-	Layers:
	-	`sha256:99995842c5b3e7de1f2c96def63b193a563558ca4cfdcb6552f275d81b4be4b3`  
		Last Modified: Tue, 13 Jan 2026 06:24:48 GMT  
		Size: 10.5 MB (10475955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67cf0cb3b4d26d330c8083c3d0154f4c5d55b37a0f6f1357460e4f958c2ea55c`  
		Last Modified: Tue, 13 Jan 2026 06:24:50 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:95058cc80901d89a4ce8b426f5b412eaac3f22f3cad845ede6a471fbda0c2d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262275767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e9fc736465aa3da46b2576ca2f460bd992c4fccf70bde72518039843b08c5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 11:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 18:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:31 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 18:24:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 18:24:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec26c7ec0c76b4716fe076707c8489ced71c06858c4f9f03f18c306cb4344cd`  
		Last Modified: Tue, 30 Dec 2025 11:50:06 GMT  
		Size: 23.6 MB (23613812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2269474ce0b0fca7a225e6021a034ce6b526a7a59bdba22d740e8cee0614ec`  
		Last Modified: Tue, 30 Dec 2025 17:14:42 GMT  
		Size: 63.3 MB (63309491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89852c6abaaf7d3796bc5819d2aedcaf5c64f4004295c9c5b5f990b11c07ba`  
		Last Modified: Tue, 30 Dec 2025 18:23:03 GMT  
		Size: 70.0 MB (70016959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a811f73ff0cb3df64f15904472d8c052172a4266c947c138019cab5cd2bb575`  
		Last Modified: Tue, 02 Dec 2025 17:48:38 GMT  
		Size: 56.6 MB (56574424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9869221fa88959a214d04edc898041432f07c627c8ec4b2abb3829593f6f4d20`  
		Last Modified: Tue, 30 Dec 2025 18:24:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2537e09389004dc505c4cdaa478014b04a9597817093116711fc95e9cad81083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9e0d8564b95f354c7fd90529cff070fa8beaf068791618a06890a289570ae7`

```dockerfile
```

-	Layers:
	-	`sha256:23020219753b47b393709cc0c7c8bf1acd7adf03c903ecb26687e9adbbda2bff`  
		Last Modified: Tue, 30 Dec 2025 21:23:03 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:38d94189fc989cb4669cd1e0c9dede128d779c1ae7922a518ca293c22d4cfba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296399627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f43d390026dd361d5f29d6b1281b3446814bcdba8779b58f01b9204a2f7206`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 08:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:38:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:38:02 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 08:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 08:43:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff2cfb691fedcba1692cb13fd0632001d1a876833f4cd2aa52eba87257a8f`  
		Last Modified: Tue, 30 Dec 2025 03:17:48 GMT  
		Size: 69.8 MB (69845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3fd09a1e6774e533a42b26351be92003f5bdea475b8caa70173ad58b79d9f`  
		Last Modified: Tue, 30 Dec 2025 08:43:16 GMT  
		Size: 90.4 MB (90419830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693eb291fd37cdf058fb56482da756e64e2b2e28c0a084790b4bba6d73d47d9`  
		Last Modified: Tue, 30 Dec 2025 08:44:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:13c9b232ce5bc5e21833509fe7098aad08da59ee1e752328777adfa4d917a39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba7ccd450406b2ce1ba2a42121ccaa55389c5da662edd0a2a8d78ed9e635909`

```dockerfile
```

-	Layers:
	-	`sha256:87df208d0395c75ef8e192108b85abc0404e28a1904f930f603014af5bf76d7c`  
		Last Modified: Tue, 30 Dec 2025 09:23:07 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6ef4d6d953659578b9845d136f3d0126eaade6659d8060bf825b5c778eb0a2`  
		Last Modified: Tue, 30 Dec 2025 09:23:08 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d5f4635585c1e654be1dc78b1d6123b922e5cc232857841a5b003bea62f3060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263178121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49a9c9dbbc54eca522ca0131e6f16118c29867e09c364ed8e8b976ce6fbbcc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:20:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:20:14 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:20:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:20:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:10:04 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:34 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a209651d1af40ce971d50b5508cc34ca07fd4a5566fd652d2b96f937d0320e57`  
		Last Modified: Tue, 13 Jan 2026 04:21:44 GMT  
		Size: 69.0 MB (69018545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75675f5c85205e80d4d654ef0c0001e64d45f6a465e5cc2507f5d7d475d2f3c2`  
		Last Modified: Tue, 13 Jan 2026 04:21:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:459a19ce75b208b3b7efa8a894e594399ce50fa4985774fad1c9e197c6351b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b4e6b44c1c45c81e85be1ba1f338bd12d1cb6174747c5f1c58e1a06a2ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:e37af87fa289ce47101745b2081bc277bfbe79dd29b35517038639a7ec7be497`  
		Last Modified: Tue, 13 Jan 2026 06:25:07 GMT  
		Size: 10.3 MB (10328141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3226f6bb0c9ac0328c50b7f886f72769f3fc21dbe4ed51db0c3fc77781bed493`  
		Last Modified: Tue, 13 Jan 2026 06:25:08 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
