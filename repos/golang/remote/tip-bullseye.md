## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:624696ba3e2b20e57c575e911e4178412e080f9475eb23af3e60008ca87258b8
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
$ docker pull golang@sha256:34dcb71526413f5f4904dfa4d52eadbf5f8cadba54b483c0c1a4255e73552856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293492580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0455fcc8dd232f330776f1b46a9dd7b77cde748ed3a6dc2e09530d49188099fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3219ad8de12a7bcfc8f0fa39fc87c6d824f2e7f1162a861fb7488de288285d25`  
		Last Modified: Mon, 23 Jun 2025 17:35:45 GMT  
		Size: 86.0 MB (86021989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553943e6d01c9acd45d693254df521c1e8dd5f2af99f49bd85cc6c44cbb632b8`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 83.2 MB (83193149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff696042f3c2ff2e533e89e4acc78eedcdb90f17d60ed73be15fda9711ef27c3`  
		Last Modified: Mon, 23 Jun 2025 17:35:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d403d75cefa9c2e806d2beb782d348d19f8a55c7dc91cbc32a281baeb0998a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3fce5a03e497548b879ee519692b70320adb613353fdd53be732f425e35a6a`

```dockerfile
```

-	Layers:
	-	`sha256:e95a9a9ecd9987e362e23a71c4d5594056be33e0bd1b7ede2240a622c3c01605`  
		Last Modified: Mon, 23 Jun 2025 20:24:57 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093e6e19808d58de59fc4fb0a30712ae8275220a8ff1cd7ba09a3190bb588c28`  
		Last Modified: Mon, 23 Jun 2025 20:24:58 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:1f62418f3d4474bf9e15a85e601a49666e0cc825c2cdce316e6f827c5c73dff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41368b378a94d6acd5cde6281ffc29bfb12e1a00aac8863534dda2c32a598143`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f7feeb0b6a1c7b2f8058fc4bcf8523950540bd39c01231df0b01c7791add68`  
		Last Modified: Wed, 11 Jun 2025 18:28:34 GMT  
		Size: 64.9 MB (64942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c23b36edc595b524e22ac037644488010f16b51c7c2741b5377b0b7319594`  
		Last Modified: Mon, 23 Jun 2025 17:37:09 GMT  
		Size: 80.3 MB (80276441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3e88be4091e8732497228c4a2fdbb7d25b22831da4a4d31c1012535741ba59`  
		Last Modified: Mon, 23 Jun 2025 17:40:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:3366d64bb2207fb55b98d840e7e8af51cc8f1ad0795f2cafdd7c6fce3d0f44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10316330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4404538bde558f51ce8b2f7a37d43baf8962c1a9e202d579883da64710b053d6`

```dockerfile
```

-	Layers:
	-	`sha256:e0ebeeb67371faa5e2776e395f7d496cb6cde87e529c08f2243d2a48e274a653`  
		Last Modified: Mon, 23 Jun 2025 20:25:06 GMT  
		Size: 10.3 MB (10289165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6397e83be313df45a22ba15520fa8d90114601db6424800a662b02aec50bced`  
		Last Modified: Mon, 23 Jun 2025 20:25:06 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5862e6ce45457b5799d627b7e9b31e9befb353c3f960ce7188321c9aadbde50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283456426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b175c0e230b96275556490f6599282394fc4edef3991d25e6734988223b5f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44d5956aed85d3d6d2c696b8489053af4a6a4d168314e425819189773cd2fb`  
		Last Modified: Wed, 11 Jun 2025 23:10:33 GMT  
		Size: 81.4 MB (81431904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b77692401f3ea137343bd9363ea145d89603d5742a3fff804ed8b3a2b6ef06`  
		Last Modified: Mon, 23 Jun 2025 17:54:19 GMT  
		Size: 79.2 MB (79168414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a9483cae5c156a5399c90a3618c0af958861f77681895368ce2492f80be14`  
		Last Modified: Mon, 23 Jun 2025 17:56:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:be81c3d8be79953b4db90c82756c90a5de49a503f02feb3de530d0aabca848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9ca2f6d88675a5ad9b37062bad31df9291ca21ef712c74a2851f8211acfc1`

```dockerfile
```

-	Layers:
	-	`sha256:1e01aede27ce7446815cb8032fb4a0682d11458f6a1e8e80b64cac3f972eee95`  
		Last Modified: Mon, 23 Jun 2025 20:25:30 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1800188eebd8c33660c8b065ba5f6b8ca9066d3c93afe965bb392b2208bb5122`  
		Last Modified: Mon, 23 Jun 2025 20:25:31 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:ac5411265bcea569249ad64ff1b29ff708c8e124c79215c244f39fd88650e20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296385206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09e3ee356c58bd53d40597d194e347962d00b10ecced0b8224b30b62bcee29e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e132c9ad59ecdbddb91c829dfc238edc489498ff5268764681fddbdd3b612fa8`  
		Last Modified: Mon, 23 Jun 2025 17:36:14 GMT  
		Size: 87.4 MB (87448140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c3a68cf208e712d48fe5a3cca6178d38afd0dcfcac42ede03f6220d712b15`  
		Last Modified: Mon, 23 Jun 2025 17:36:27 GMT  
		Size: 81.9 MB (81928340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673be5e899baa817ea43d63de560e147ab0961136ca4b9bd84aaec6fd52e5694`  
		Last Modified: Mon, 23 Jun 2025 17:36:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:28732ef8e1b6375a952398f9d67043a36e1299d786de8bbd08fd2cd9587a334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c8dfb57f34af216b060bfb7be62945d1e8d6067db3310897ad36f8ca68d6a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4fecd60a75503cc6af5373670880c126130128ace987c8e1c385ed7e82c9385`  
		Last Modified: Mon, 23 Jun 2025 20:25:39 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418df16150169129a8b27c81e68576b2c9ebe18256373eed73c2cc330cf2cc03`  
		Last Modified: Mon, 23 Jun 2025 20:25:40 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
