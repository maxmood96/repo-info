## `golang:tip-20260321-bookworm`

```console
$ docker pull golang@sha256:7e5eb8c646f090e363dcf75c3a2e4d267f30d3befea46ed5f1514d9cc63e2e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260321-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a5a60011a0b1761634c4a946c5e5a04d3d939fcefb14f1c9a2f040d322b1bd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323298074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d206040d5c2566d3509cd223adbe4b245c5504d32dd4b0dfaf6dc80d5d836e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:11:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:10:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:10:26 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:10:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:10:26 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:13:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:13:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9513cbc8be80ab10ae8c4bacb751751bb15e5d769ab5b00ec4642eb913fcd`  
		Last Modified: Mon, 23 Mar 2026 18:13:44 GMT  
		Size: 92.4 MB (92448627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da6971e9abc1b6c7a1372792a609e9cf545f9f36ce489f1bdacf534e2c8abe`  
		Last Modified: Mon, 23 Mar 2026 18:10:59 GMT  
		Size: 93.9 MB (93926880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc77ad8578a0947ba97bc0e6b65fcf1bc3d7e5f7a56f432f82fb95bfd771ec4`  
		Last Modified: Mon, 23 Mar 2026 18:13:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260321-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0bbd7ba163922f8526365b649c9df464598adab00e2c4745bee781b56974bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326d0a0640d4c9e3a0be7a13b4b49922e13673bb56654aaba334a479deb6bf17`

```dockerfile
```

-	Layers:
	-	`sha256:43a6a0b88a3105770028d14576e75e2d296ca9097b4827ffff73c5b82384661d`  
		Last Modified: Mon, 23 Mar 2026 18:13:39 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa49a32c898efcd0dda8e961260887636f7653272b44385066c084fcb56f0b1`  
		Last Modified: Mon, 23 Mar 2026 18:13:38 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260321-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:c5728309971b768ade5c71200613b9aaed3175aa1514a0702b16f4f64ea50c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282150046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62d6d5296814dcce2cd5883a3c996da42043474e7beffc0406a455e48f116df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:06:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:09:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:09:40 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:09:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:09:40 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:09:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:09:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d83cf3e2651316c35359ab7a5be5d7e2739d967a4ee347c83f4e324cc7cf50`  
		Last Modified: Mon, 23 Mar 2026 18:10:07 GMT  
		Size: 66.3 MB (66305313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3fe8212a49eb41f6a4366c38fc20cb7c161e830a9074b4c7ea09f324d1f7e0`  
		Last Modified: Mon, 23 Mar 2026 18:09:57 GMT  
		Size: 90.0 MB (90042864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5769c7b74d0606c8d27ade6099b85105132ea90ab7221fa99497aa2e1d4a9`  
		Last Modified: Mon, 23 Mar 2026 18:10:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260321-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:84af7867333b673649dfbfed9ab0fd381165a060e10d6326f2f982a46aa349f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774b3ea0064dcfd5d28bdb243669e6e7439af92ee63d8e1bcb19447b65b4b6bd`

```dockerfile
```

-	Layers:
	-	`sha256:1a31a8e931bf09338e981f4f034b44ad4b4a51d047e510bef0d3d476022a3527`  
		Last Modified: Mon, 23 Mar 2026 18:10:05 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47c45754ca64ab41b30f38a9568f9d30e918602681a4c2af85c661f9af5a0e5`  
		Last Modified: Mon, 23 Mar 2026 18:10:05 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260321-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9ba9f66f7818c508d767562ce724b018a67cb79c232d24512f27eb8ba4ba5276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312011590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3aa2728aefb1219828659faeac15c3ec382e5b6aa1035deaad0ead7f27b06`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:15:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:15:33 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:15:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:15:33 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818ab6de96ddeec30066d2b25fd29627f00b2d155180210874b24c414ea7d115`  
		Last Modified: Mon, 23 Mar 2026 18:16:02 GMT  
		Size: 86.5 MB (86521358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d89156bf69d73fd72aeaeb2ffe43a084d18a5918673e90973fa80f2bd1106c8`  
		Last Modified: Mon, 23 Mar 2026 18:13:03 GMT  
		Size: 89.0 MB (89032899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c218e29310673d5a01c0f70eb1bb182e2266d66e8cd5927f573d9033cbf1fec6`  
		Last Modified: Mon, 23 Mar 2026 18:15:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260321-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7642e74b7432c3d2f19094fd46011b023609980465d0fe41b75d8757bad0345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c00224c5a4a8e274f05bfcf652a7c11e309584e24bb90e9187b3a5f26b4337`

```dockerfile
```

-	Layers:
	-	`sha256:a36cb52e7aca471d3e998c54eb4d7a78fc0ac23bff58c250ed846d0d4dd8045c`  
		Last Modified: Mon, 23 Mar 2026 18:15:59 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45f647ce7a63137d6e36972a71481e5872c20408d6cee5056338751127078c4`  
		Last Modified: Mon, 23 Mar 2026 18:15:58 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260321-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:071fce16199e6e01181f1870950dc9b44c76e767fc5fadf0b964840e8aa9a751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329042572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67661ee878c53b98056890d1254a5bdbe01b51aaa6cb7874313496dbe36b8def`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:33:46 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:33:46 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:33:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:33:46 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:34:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:34:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f650603f8d0e18428c1905147e851a6141c48ce2c07ea4bc2c40ab57b56ab`  
		Last Modified: Mon, 23 Mar 2026 18:35:15 GMT  
		Size: 90.5 MB (90462649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70a7a68b066f9965e7b26b52317270613e7319f2d2ec75b34f1e502d6ba09c`  
		Last Modified: Mon, 23 Mar 2026 18:35:15 GMT  
		Size: 90.7 MB (90725340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ef246157a854db39941947cef9d760768d3dfc8b7ef70465247170fffb7d98`  
		Last Modified: Mon, 23 Mar 2026 18:35:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260321-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1700e595f8828222d09b010279bb214175a6ce0f36edd2178ac1059761991368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d1d43591c8d33676cc65c476c60e32e96acc08d89bfb20ec4d098b121a4149`

```dockerfile
```

-	Layers:
	-	`sha256:7fd178879d8c53d2abb82df1722883ef2d923b3bc461c1e637f83d1ea30e5c4a`  
		Last Modified: Mon, 23 Mar 2026 18:35:12 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c31f27573de965fc01e494afb65fc242564c1490265dd1e356a858810c7e7819`  
		Last Modified: Mon, 23 Mar 2026 18:35:11 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260321-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:3f215cb5f6712581d31711d186987062c7aaf545463d49b955bc70e726f38f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296857291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ca745814728062f431c961917aab2558a361b813798c1c8f85272352ea6b5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:10:43 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:10:43 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:10:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:10:43 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:10:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:10:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f573b6961192e478084182f03c903189a08720a84360f156636b47d959044b`  
		Last Modified: Mon, 23 Mar 2026 18:11:27 GMT  
		Size: 69.1 MB (69055019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ef3b2e5174bcf54b94b5b8caec33835ac1e023d73b8c9e7be52d6d2ef4659d`  
		Last Modified: Mon, 23 Mar 2026 18:11:11 GMT  
		Size: 93.1 MB (93119115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5225c67b3497684ba65406adb77dbb9293c7c18c9f3381e3ef6b67b82e298`  
		Last Modified: Mon, 23 Mar 2026 18:11:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260321-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a23056d68f43305c499040bbe069b0ce508ebde772c03e3c4917f389bd94707d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbfc2dec65e5aed955e61b2c6fcc854f5b3a4b5a89894d3c8b41eea3c24c359`

```dockerfile
```

-	Layers:
	-	`sha256:6cdbb1ce30c58bc8b2a7a2fde611194e6c666946a8c1255e87790e8385b1e1f8`  
		Last Modified: Mon, 23 Mar 2026 18:11:26 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4060a1c68bd4dc4a35062c7c2ceb7366a502d9c4a071721e903f473ce1f7a719`  
		Last Modified: Mon, 23 Mar 2026 18:11:25 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
