## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:649c6a82a89fb471d90984d0aacb5794a1adb954383ad497eeaa379ed02928ca
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:daa735d7bcf0670ed7b37498788ed9df9b7995db0b6993d019ec56d63979d2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359099675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a2a1e891d78437c7b449cbe6092535581f75191e4818fcf159ab64ee454faa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15c8958c801bc940d71ff415934f2711df9853b505fd99ab699ae45a40c3054`  
		Last Modified: Tue, 04 Mar 2025 21:59:39 GMT  
		Size: 92.3 MB (92331898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524ccfca7911a95bdd931ec5651a8a17ad473328384351225aec0dd451c2f73d`  
		Last Modified: Tue, 04 Mar 2025 21:59:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9846b4847814ce6b023101c676610bffde0d0039c261d5ec42bbbe1ce0cefbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95ccc23ab7157a6fc3aeaec83c62b18e61b1f3ee7cef7e483cbf595ddf0ee7a`

```dockerfile
```

-	Layers:
	-	`sha256:232f94a9368670e5c809f8b753efe595d07cbe916d8fc1461eb69ac562463661`  
		Last Modified: Tue, 04 Mar 2025 21:59:38 GMT  
		Size: 10.3 MB (10274074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da464c2426c0caeb72f827238300219cca9a8084529e9f44584b6694ebffd9e`  
		Last Modified: Tue, 04 Mar 2025 21:59:38 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:207302a15de59f597474fb3bd804d6055cdb48cc77145de1ec3c2381b76affec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315055340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1463775c8b75028c3f166182babd993f7db85d12d4814799b8555b9d1135dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654867856e71cf6e49b9c0cd4aa53b8135e92c7f0694dd70469ea7e9aef8a87`  
		Last Modified: Tue, 25 Feb 2025 17:00:54 GMT  
		Size: 66.2 MB (66187481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a4732c96edfeab450050a70f02b158342482c6f2a5dcf7aeba30aac7fcc17`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 123.1 MB (123087551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd1ce312109ed1f0330cf76e4e7beda629dedfabc1527971506afa9eb3e6e2f`  
		Last Modified: Tue, 04 Mar 2025 00:33:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d24429bc349af32aadddc32b0bb39c1689488725a9c7d325e7de6274fbeb8749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10110183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c189a87c85e72c9936462b7abc23494d21b6513fc85d725159a1b41f2f531835`

```dockerfile
```

-	Layers:
	-	`sha256:beb6bf5b7a63d9ca6d9302562b7402403d2d42add5360ae9dd11c849038ae801`  
		Last Modified: Tue, 04 Mar 2025 22:12:18 GMT  
		Size: 10.1 MB (10082396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90524fefc46a579b08b0b3893691641ada8d48cf25e705ae2fafe8e8149b7eb2`  
		Last Modified: Tue, 04 Mar 2025 22:12:17 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:df9d240da7f57345d1442b628a91621e8a2b9d4337120b8a43378562d1e58a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fa6c635eb01f9c4caaa1dbc83bce90f479ae3ae35ea487626ab825444d2b48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5401acdbd47da62354605cdc39280e128c1fda32c0830d209bca96e7352c65f9`  
		Last Modified: Tue, 04 Mar 2025 00:39:28 GMT  
		Size: 86.4 MB (86383185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fb2f15af0e54e78387b98706e083a5882e5cd46c9ae24a07d9c9a7de13391d`  
		Last Modified: Tue, 04 Mar 2025 00:39:29 GMT  
		Size: 122.6 MB (122620567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbf343779f6fd3d030a8d02d6497351ec1733af693adb9fd1c597a261d05077`  
		Last Modified: Tue, 04 Mar 2025 00:39:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:015f4d0457e8c24ab305128f46f98c73d93d808dedb605e3978328549fd17b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0055df897163ef0586fb16ceef36f3dcf5fc893838ad45e00a33c36a8d2a718`

```dockerfile
```

-	Layers:
	-	`sha256:de4f64cd587a723820394db165b078bf55d3141ab33c918ac12a5cf590fbcac2`  
		Last Modified: Tue, 04 Mar 2025 22:18:26 GMT  
		Size: 10.3 MB (10301921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a497214e68358edb6fab3727d1d595e9c66e7dbba2cbedfb4d8b85144944a63`  
		Last Modified: Tue, 04 Mar 2025 22:18:26 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:5bb953359dbff2cc2e1286b6b17a581612776724bcf6d6fb3dc1e559755108a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356798390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddb4bcd2fc02b0da9ffa59b4be830a1ea63680a878ff39366ffa581491810ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c581aaacc4938014fcf31f4e961a756adecbe9086b4231ba332f3ef0ad8c3`  
		Last Modified: Tue, 04 Mar 2025 21:59:19 GMT  
		Size: 89.7 MB (89744383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9ee8d72821956d9b8dcd47918cb2eb2db9a4cc78512d6df96d365608bf2ac4`  
		Last Modified: Tue, 04 Mar 2025 21:59:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d1a26c0de5553d85a0a9ef803b6943c9227fa736d9d1562d2a1e5eac9d5f77b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c02484e91a36e6a92f16e2ed004901753a27ea0275821ef773e4ef9258090a`

```dockerfile
```

-	Layers:
	-	`sha256:71879b1ead64e451baefa00bb0ee91981cbb921ab7340c24b751d9de3eb26c9e`  
		Last Modified: Tue, 04 Mar 2025 21:59:17 GMT  
		Size: 10.3 MB (10254145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf0d1cd475095b8440e1641842125343bba98eededa82f386eb015b6be673a6`  
		Last Modified: Tue, 04 Mar 2025 21:59:16 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6e67127de424a06b10ac793aa8d0a686652a12f172e1cbaca41dc08a10b9b2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325380803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42fdf0a853d93efef65457db6c000499959f1d208c015fb5b675da3239f4bdf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e93c581655a2c5138779556e6b049332bee85d015285d3106e767693cb64d`  
		Last Modified: Tue, 25 Feb 2025 22:26:26 GMT  
		Size: 63.3 MB (63306786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301664e1162c99caec998294841f4102a356459d19e18d2615cfe952fdad457`  
		Last Modified: Wed, 26 Feb 2025 02:31:50 GMT  
		Size: 69.9 MB (69904803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc470fbc3accd92076f60a2cac89a09d11e03f4eeffd4275f69bcb679622421`  
		Last Modified: Tue, 04 Mar 2025 00:50:30 GMT  
		Size: 119.8 MB (119757829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93f9097e350cf5cc525f6d69b611fd7eb284541046844d8a3a26674da713f32`  
		Last Modified: Tue, 04 Mar 2025 00:50:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fce751bf3a388375b0a3fa3bf0547e9e1ec65a9c4ed8c62230aa40a6dcc4a90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5daf70935e6c6945d411cf917484735847a415482e2e2aed927b4ffc25657da`

```dockerfile
```

-	Layers:
	-	`sha256:9fa81f69bde956c019419b13a14dcfa9fc4d94656663ae6e11dd659420963956`  
		Last Modified: Tue, 04 Mar 2025 22:18:17 GMT  
		Size: 27.5 KB (27534 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:710a707264de79da0423bd535346ab7ef8f9948cc395676d7bfdb064b431fed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363179902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65f74b5caf61ee65e5abff5f9839143220162b5b94fe310a111d01fa9c55e8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eddab3d8a04dda752c64b51fbaa29916204149752323327524cec69525c60b`  
		Last Modified: Tue, 25 Feb 2025 11:58:59 GMT  
		Size: 90.3 MB (90316651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de94f4e3ebdd3654e0bb93d6ee292377b5f63d04585b0ae2f0dcd851ba62d914`  
		Last Modified: Tue, 04 Mar 2025 00:33:04 GMT  
		Size: 125.0 MB (124994092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c229b2f5ee6a92b0d69123533ec3f1c2c029a3bca861d6a099535c75f0777d49`  
		Last Modified: Tue, 04 Mar 2025 00:33:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2f0da1dfbf33f4c4232914487296a5ec31a5f8615d823d175a902d4894086d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c015e4a9546dca41a62e6ec1d4a4ed022b547f22ea14fa0b209998d7130507d5`

```dockerfile
```

-	Layers:
	-	`sha256:1e952a504b06fd05d389f80590928bb282c210424f2693fd981bbec47ca174e3`  
		Last Modified: Tue, 04 Mar 2025 21:59:03 GMT  
		Size: 10.2 MB (10246773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3629cf9f578a7d382b7fe69b14346f3c87aa2d506a59a28ab9be6dfa926e9be9`  
		Last Modified: Tue, 04 Mar 2025 21:59:02 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:79d0fb33e6688b982cdcb3ed6f57fc08873c0b5d4d0c7d4aa322525de583ec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330946917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b329f804fbc10a1a7e9088fd05eda07cf901e81dff62d583063f816ebecd189b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16676c94eed4de3ccdb41bd857bcf5d665d34b49ee6681f62964150c8db326cc`  
		Last Modified: Tue, 25 Feb 2025 09:28:53 GMT  
		Size: 68.9 MB (68903037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a90f174e12bc58df6074c85a9d3459219dd43fe7d642ba33065f9e29227fef9`  
		Last Modified: Tue, 04 Mar 2025 00:32:29 GMT  
		Size: 127.4 MB (127357030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0e1531e112657bd2fc984e845e0ecc21156811d31540f5a33b4a625a037a56`  
		Last Modified: Tue, 04 Mar 2025 00:32:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d961171b9168e175237bc43e72a5af14e5366a1e3289fc630862409b3dd055e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10137716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015e95e20c32568ad458cd9775645e19f3b1eee344c5b8d297ab4137f817672d`

```dockerfile
```

-	Layers:
	-	`sha256:94b64bb44b2140fd5382aa469fcb41e16fbae3e32f68cc6eaab138daa507df58`  
		Last Modified: Tue, 04 Mar 2025 22:09:09 GMT  
		Size: 10.1 MB (10110054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:634d5294f8661a956b6caedfe2ffa7c4fce7782932b0c1fd6972398d8818b820`  
		Last Modified: Tue, 04 Mar 2025 22:09:09 GMT  
		Size: 27.7 KB (27662 bytes)  
		MIME: application/vnd.in-toto+json
