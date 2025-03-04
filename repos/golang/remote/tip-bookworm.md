## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:4858b3ae1e9dbf0652101d77744d1795da70ed21363bf8b0d4b3dd45694a6061
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
$ docker pull golang@sha256:d4ec0d6cab7ed7e8baf6a93caff732121db605d98baaf4625c526c25a5aed47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359100283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d39d9e1f4d01bd24a33f46d590012facb4fc42bfcf92e1d946154a5d4e88c13`
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
	-	`sha256:a576ab018719c0d79aaeea8208ec1bd09c1be5013645b00005e526af398cb0c4`  
		Last Modified: Tue, 04 Mar 2025 00:32:35 GMT  
		Size: 92.3 MB (92332506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c747812028fbb9493b8656ac31b2188a182bb084b8c0960979bae72b536698`  
		Last Modified: Tue, 04 Mar 2025 00:32:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b760c0dfb6c8a6ea912c98782b58e372d65dc880080c01e366ead3a9e3fc8e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d136a828a8f4101665810b9e013357fc6abca3377d585dd2702642e6b66c0bca`

```dockerfile
```

-	Layers:
	-	`sha256:5783b7033986ec4fc30f15187ee6941c4adb6c622c06f09aaedc9f153c4082ca`  
		Last Modified: Tue, 04 Mar 2025 00:32:33 GMT  
		Size: 10.3 MB (10274074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb1eb4e88c6d35201513edc01798c428978e0cd01814d8eb146a1a188fe4b5f`  
		Last Modified: Tue, 04 Mar 2025 00:32:33 GMT  
		Size: 27.7 KB (27662 bytes)  
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
$ docker pull golang@sha256:ed6a516dcc82253c3d9a5997a18fde65ddd53348a28d8d4364696cc3dc77c10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10109067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67747874b423a8528066bd60459af9be5479322d873e95da617163e1c8ee0ce9`

```dockerfile
```

-	Layers:
	-	`sha256:000451064eff917cbbe961b9fa4c24acbb8e24b6ebbb883ea0e4ae81eab82410`  
		Last Modified: Tue, 04 Mar 2025 00:33:44 GMT  
		Size: 10.1 MB (10082396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c07143492411970b406e90a231c15a01b4333398e205773226dbedecc77723`  
		Last Modified: Tue, 04 Mar 2025 00:33:43 GMT  
		Size: 26.7 KB (26671 bytes)  
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
$ docker pull golang@sha256:afc8b7783fa3d1f0b0f68aa153ee94d8593519a70b1919dff1d11963cc169eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881cbfe0378f2f8e942ac6a880a1c68c8e3dbae336cff851729547ed02add3bd`

```dockerfile
```

-	Layers:
	-	`sha256:260f3ab641e72ca47fd348d1f8649cca163f2ec9df2d4306adcbcdce84365c1d`  
		Last Modified: Tue, 04 Mar 2025 00:39:26 GMT  
		Size: 10.3 MB (10301921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54d056ca35cedbc047f6dda00bb2243958b9c8a0ffeba904b8ef461e2659637`  
		Last Modified: Tue, 04 Mar 2025 00:39:25 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:00905b197b1711bf793ddbfa56eb0d962524e6cdba62f019474f7240deabc190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356798391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fe723249067b7dfdb213c72736c5caf562c2983bcf3d6b1fbd10e419599223`
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
	-	`sha256:87284ceec69f2f79109ac9774d6ee4b0b3a75768377c9e49c977cdf129fb0e69`  
		Last Modified: Tue, 04 Mar 2025 00:32:54 GMT  
		Size: 89.7 MB (89744383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17356454033c6476ebf13676b512abd328bab7413bcfa4d49852335dff81f26a`  
		Last Modified: Tue, 04 Mar 2025 00:32:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:03a50c65702357d998bc31e98e0a34eb77c4cfd46f0d6db9016ba2a20ee36706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ecf2faaac8000914c789afe2ec36d738cbd7468defc6e4906e24b6df49f93a`

```dockerfile
```

-	Layers:
	-	`sha256:02ec53663f94245bad8baf7c4fb9f7c8f46e73d887c79239d86e2063f29dccea`  
		Last Modified: Tue, 04 Mar 2025 00:32:52 GMT  
		Size: 10.3 MB (10254145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2d26247d3461a342ce259c39bfe594def83ebaecc757268bf7ef62e4a1f7ca`  
		Last Modified: Tue, 04 Mar 2025 00:32:51 GMT  
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
$ docker pull golang@sha256:e429417bc3da41518dc7bc26380297a6db60f33df21392f33cb76d446963fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860bdd4c5706ea1c79ba840a8d96c20c6d4754c537c3770aca6874de6332c78b`

```dockerfile
```

-	Layers:
	-	`sha256:e8894259e20c74ae83598513bea68b4fff9638071acdba387ea589e17699ba9b`  
		Last Modified: Tue, 04 Mar 2025 00:50:19 GMT  
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
$ docker pull golang@sha256:0b1518b8b776233d4cc4d897d1998a18c893a1a34a95b05edd7e7010548d5293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425af05706e55caea1987c1cfe70a62363fa4981092ec201d3e92a2707cd5f0a`

```dockerfile
```

-	Layers:
	-	`sha256:fe55158a8a09f47ddcd658c179ff5872b83b64ce2f01d7d3db8e0d35c755f40f`  
		Last Modified: Tue, 04 Mar 2025 00:33:01 GMT  
		Size: 10.2 MB (10246773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc24826888d12373d129e625da8c3828f659195b1c295ae25245799f899130f4`  
		Last Modified: Tue, 04 Mar 2025 00:33:00 GMT  
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
$ docker pull golang@sha256:fc627f52fbda7c33ed9da8e6975b7135f7bc738c23e00872c8750e082723861c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10137717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c048b13e09d7b83fc04d6c36d76659dfdc710bbe809dc8fc2dfa0d277d627f4a`

```dockerfile
```

-	Layers:
	-	`sha256:98ccbdc65426074da28edb502d33d0cac6ac002ffb7968c71c28e4ffec8accfc`  
		Last Modified: Tue, 04 Mar 2025 00:32:26 GMT  
		Size: 10.1 MB (10110054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b1f9915986f2af70fdd738bf3a7eee5881386028b89dabf5e5f1a929f9bb47`  
		Last Modified: Tue, 04 Mar 2025 00:32:26 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
