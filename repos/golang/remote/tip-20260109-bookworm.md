## `golang:tip-20260109-bookworm`

```console
$ docker pull golang@sha256:059a8f7ba6789cbcb4cd4dc80b18af0709d9e73e07f3f82c0fe36274a2ee9bdb
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

### `golang:tip-20260109-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:cdbabafc18c6582d2d0872416bd182a418f902003cedf28c939873c0277ca615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324399780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c96d947ac7192610aca5d5a1a9cd4b5ec97fd4c005139d12d408ab87893976a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:29:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:29:28 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:29:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:29:28 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:29:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:29:31 GMT
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
	-	`sha256:4299cf5f64c198ad48a0234b99707c3e097beba0fb165f0d1ee2892a2e65a8dc`  
		Last Modified: Tue, 13 Jan 2026 05:30:13 GMT  
		Size: 92.4 MB (92433449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8211fec439494ad1d4d3234293c9458bafd5cbd34bfe9931a50d398b25f9c3b`  
		Last Modified: Tue, 13 Jan 2026 05:30:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f60bed9bb02f98403cfb53cc40fe091f2e44dc489d6869c3ad42f3d0926fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529a43f166ff0d0ca5695a589a8266b5892e203d9d0f163e7f382fef07291cf1`

```dockerfile
```

-	Layers:
	-	`sha256:fb8fdf94ac3ceac5907fe3ac6d53ec2d4cdfc3f2e157042243dda63bde1b96c5`  
		Last Modified: Tue, 13 Jan 2026 06:27:44 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6495c82f825e3aae92de20a28c3270300abbf04e8cc9e337fdf30f23f160cf`  
		Last Modified: Tue, 13 Jan 2026 06:27:45 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:9dd69be76074c3d2d7399d5cf1d1e19a55600e2465d479f853df41d064de2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283206545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c848998be06062e19637bd13b48798edd85556534682dfe01b262a68991793`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:07:53 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:07:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:53 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:07:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:07:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc98fc7c621e14d0e6742f2184cfb67e65e411577d2485fec3e824a7040cfb3`  
		Last Modified: Mon, 12 Jan 2026 20:08:47 GMT  
		Size: 66.3 MB (66288717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:47 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f68720b240cfb31363476f9d1fffc1d41c95a262797bf9066e6824140187d`  
		Last Modified: Mon, 12 Jan 2026 20:08:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e2c7396e974ee3e679b8255d08ad4e7a7c95cf921d106703beb254eb4b49cd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51cb3469baf5a002f31cea61de26f2ec4971c54cbaeaa3d6fbd9988ad66efa0`

```dockerfile
```

-	Layers:
	-	`sha256:551cc8ecb5073d9edb349675177816479d4189f844a5ea0b5c90327e52ed2752`  
		Last Modified: Mon, 12 Jan 2026 21:25:29 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7d27dcc81b184809c58ba9a6790e1793656ffd4a3758b2977a9de2a154a77c`  
		Last Modified: Mon, 12 Jan 2026 21:25:30 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b17ac782010b19e6dabddc7f06beebbf8aacb7d2206347e2edd25c910235d53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313094680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36c3abe64aa411100240fb01acdc709327b2a513b6b9b5c95c7063ad052bc39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:25:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:25:52 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:25:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:25:52 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:25:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:25:55 GMT
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
	-	`sha256:50ae73af34c9abcc2760dfe4be1c44920b921064b0367eb5c2b33639aba9c4f1`  
		Last Modified: Tue, 13 Jan 2026 05:26:33 GMT  
		Size: 86.5 MB (86506865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d1a2f3ae73143290ec48bd21a83a63dabade3e675b02c3d4b120514b8d86d`  
		Last Modified: Tue, 13 Jan 2026 05:26:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:36e36551ea32b3f2e174b3b67a37d30221facc73c6707c9d6f711c4e61c8f3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c589fda26c79335960d405617cb4a7188dcfd029990acf7c8c35cc9cd04c496c`

```dockerfile
```

-	Layers:
	-	`sha256:c11f3b0750ba34044de71c1df9f1864c26db8f83b65ad91d066ba84c7bb888bc`  
		Last Modified: Tue, 13 Jan 2026 06:28:13 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068b34e65034390b5ef497ea0074b020af88c8da4bfdf74bbaa2295de3369d6b`  
		Last Modified: Tue, 13 Jan 2026 06:28:14 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; 386

```console
$ docker pull golang@sha256:bfe87e030d6be2ba4b11878b2293c457b32f7280560196edc9e71e4dbfe53af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323378723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627cbd4c6ae5a3439d56b6e2ce0013f63db7a37abd469b81032b8df28264631`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:26:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:28:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:28:00 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:28:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:28:00 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:28:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:28:03 GMT
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
	-	`sha256:c57c42cadd0dd13ad08f9e8e9323e64056920397b9207c1624367e060e79bf7d`  
		Last Modified: Tue, 13 Jan 2026 04:28:42 GMT  
		Size: 89.9 MB (89858825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:45 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0acf0e31f72e2a557f9c213d87915a0788ef52f47776223f379be8ce71a296d`  
		Last Modified: Tue, 13 Jan 2026 04:28:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dd0556611b350803f1670be33a77895abb777885a976db737e8d287f6cee2e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b320eee8153527aa20ef4ea72d86d999cdcf6bfae39046a8f9aa6942d545f`

```dockerfile
```

-	Layers:
	-	`sha256:cc6f6f575a6752f93e482c88e53c925370ad75385b18cf5c403e9f428fb5476a`  
		Last Modified: Tue, 13 Jan 2026 06:28:24 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeab3c9b383b078e8a69234d5ec2a5bf9be43c02b4303bf8cb7b9160c41214c7`  
		Last Modified: Tue, 13 Jan 2026 06:28:25 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:8389923f0f4ca7c206e7c1d69deb89378bfc20880bb3cd10f2a6b69e5336aa8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294510604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ff74b9ef73d44f829632144f6ec2abae1db156b1e2c17f2653d0b9fb10201`
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
# Mon, 12 Jan 2026 20:22:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:22:47 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:22:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:22:47 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:23:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:23:04 GMT
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
	-	`sha256:a831f31f3ccc6903fefb1751e80553dde8e9c3ac9501ef429ef0c2121806bc98`  
		Last Modified: Mon, 12 Jan 2026 20:25:17 GMT  
		Size: 88.8 MB (88809259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c0a75bb4777652600df46c93da7678b8ae65a2c4ed72c1e83286bb0e7b790c`  
		Last Modified: Mon, 12 Jan 2026 20:25:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2b053cf570d7f83880d0962dcbf17ee7b7476523e408ed20c47e28f8cc6cc28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73eca29ffa102dd9dcdbd68b2260c16cf3d0d8c8cfff16e01194cd46a2767e8`

```dockerfile
```

-	Layers:
	-	`sha256:7d04c080019303bf736b6414743e287cc99fc578fd34315c3a5b656246b420f6`  
		Last Modified: Mon, 12 Jan 2026 21:26:01 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:de8ccd310ed5eed26b7b5a2fc0628862894054849c5bc5681af69fabd06533d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329948599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a655f951a980f6d47931f3be4e514a2ae60d566043d9476c296147ea9d120`
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
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:08 GMT
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
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7819a636ad71abed7becc2cfb517aaa851c7f08a6fa01a34bf7568fad5926`  
		Last Modified: Mon, 12 Jan 2026 20:05:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b65a5c63282001f32ee106dcb7a4228116d709af63712a1aaef3645557058789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d42f656d58d6d0c711d84d2b76b84d0403bd2fbc537ed4a98c3e906e72578c`

```dockerfile
```

-	Layers:
	-	`sha256:bcfe82eb16619fa9188d628a0d5912b770372cb2e275b2d9371328b8aae476a4`  
		Last Modified: Mon, 12 Jan 2026 21:26:06 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8a6c4142dcddecbeb1421d1e9366c8b07cf5d0065748b84441e955dd26a249`  
		Last Modified: Mon, 12 Jan 2026 21:26:07 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7649acb2caa2430585f357819fea71e50c6de3c7f32e80d3e3a3bdae531fe9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297907031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa8cd64fb3f1bf0393261213c111bd1a746654a8cddddc8344e05864588751b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:19:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:19:09 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:19:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:19:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d337299523414af9c112b1b1a1d201a2c6eaec2baa26798cdadeeaf575ed2`  
		Last Modified: Tue, 30 Dec 2025 02:20:20 GMT  
		Size: 63.5 MB (63501425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cade7c11e2a384e856bb2917369c47ddecd37868c2ef72ed6042a2765c4308dc`  
		Last Modified: Mon, 05 Jan 2026 20:14:59 GMT  
		Size: 69.0 MB (69010692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:21:03 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4d53ea7b41f31103f69f94e440f8cbc0cd52474ac3cd07a9e06d1e1b7ef85e`  
		Last Modified: Mon, 12 Jan 2026 20:21:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:00519c01f565c62d45b6351d43231ab611bc0409922d6c3e3662f7143087e923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99953584771449734d007cab5676f0573564d94785705b8f13dd5ea0e258c3fe`

```dockerfile
```

-	Layers:
	-	`sha256:96cb7aba3ee74a2c132985fb7696af89cc329a0ec1bb1c057c6242eb72231873`  
		Last Modified: Mon, 12 Jan 2026 21:26:18 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede8099b4642c36e6d2007e00da1eae6fdf14b5e17e90f1544f3e4d59f3052a8`  
		Last Modified: Mon, 12 Jan 2026 21:26:19 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
