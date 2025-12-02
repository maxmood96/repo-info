## `golang:tip-20251128-trixie`

```console
$ docker pull golang@sha256:0cd2ebc0a7d7c68678895cdd5522924b283a18ae2edbd89a387bd9e868bd4b61
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

### `golang:tip-20251128-trixie` - linux; amd64

```console
$ docker pull golang@sha256:85dbb2b60a5f09533f3a04b4331f0eb821436936414d3400a9157cedc2de149d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338904720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4cdda3f728deeb8e6ea3a7539ed195ded0d16e95fd6240cdef1b71eae1a759`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:57:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:57:01 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:57:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:57:01 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:57:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:57:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c575c96058c85f6740e9f78093c82070bbe6723249e88f8ae41ae5b68582d00e`  
		Last Modified: Mon, 01 Dec 2025 23:58:00 GMT  
		Size: 102.1 MB (102108871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc7a3ade8c1cdba7bbb9423268ee2a9ae507a29f6b78bd9ceb33fc75b61bb8`  
		Last Modified: Mon, 01 Dec 2025 23:57:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:746a0bcf50d7c61fbe43b6ca4fed2f8b27a6c19592a2fdc276354f8533456f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866eae83f223cc04712b4dc46d541faf69ed4d2a7a6d4345bab3b4e12e278bee`

```dockerfile
```

-	Layers:
	-	`sha256:ebc5949514cc88cdc83d4d0a331cd7c04cfa16ce833e2b6e01bbada75d2c5824`  
		Last Modified: Tue, 02 Dec 2025 00:23:24 GMT  
		Size: 10.8 MB (10784510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be27b37132f6bed24c1a4c67c15ea085f1d1f68ed46b9b9f6ef79b84f783cc27`  
		Last Modified: Tue, 02 Dec 2025 00:23:25 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:84199c977c37dae397cb9dc422c8a5b7f1ea417745b7a5875b9bc091e157db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295004324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7c6d24a46d747439432a96c3e87a534e3ade3b06a2a72ceb7ea8a0c605abe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Dec 2025 23:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:00:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:00:27 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:00:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:00:27 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79eadd0e78439f089e9d633a6b207111c85020da439d79a64c37fc559cc2030`  
		Last Modified: Tue, 02 Dec 2025 00:01:20 GMT  
		Size: 72.8 MB (72754105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b9318cc1b35d0eaaa98124c74fc172cddd78a91fb2766fe7b19eeb635ffadd`  
		Last Modified: Tue, 02 Dec 2025 00:01:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6c9f62752daa937388adf0c3fc6676059e04b02c18fe262e52fcee85cdac2b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423ba64119610e0a0933f9fc8e029b79e4703edcfe8fff3007cb8464dc76d6ac`

```dockerfile
```

-	Layers:
	-	`sha256:77360857714834d4897157d938a414025afb5abfc705f7fcaf52c1ca6d76dca9`  
		Last Modified: Tue, 02 Dec 2025 00:23:35 GMT  
		Size: 10.6 MB (10580397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a2ff9ca787caee697456b93ef8cbbf20706ca92aff67cd4014f28936ae8e8a`  
		Last Modified: Tue, 02 Dec 2025 00:23:36 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dc2bc5036693db0e5aa06a0a91b0f1fa757af814026b6110abf65f2bad900f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329722160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5477830091e98bdc4320b6ad8ea385c061e57df25acfbedca55a984e9acdc7ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Dec 2025 23:55:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:56:47 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:56:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:56:47 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:56:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:56:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac92d1aef3cc5f5ffd36885e763424786af9fb8241417612d191b8c3b9d462ca`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 98.3 MB (98254592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2edbf0bdf04c494275535bde4fa2876727413ff8ae38dd169263a4a4ab0db1`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ef5440b93b973c5343424bdd0ccf17a64d6b3235a79b947de9ac47b1af2e52ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35090e7c675a0ce3806cafbf8cd25b64af3757babae9204f38e7fc2a8ff5240e`

```dockerfile
```

-	Layers:
	-	`sha256:cc8ce1acf9ee1b532dec40f451fad94dc5b0a0bba3512cef07d0b57bc00ddd6f`  
		Last Modified: Tue, 02 Dec 2025 00:23:44 GMT  
		Size: 10.9 MB (10904965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5e866461f5657dcdec48cb8c3cc5d629b004eb5e7b771b09c4a2fb031ce83c`  
		Last Modified: Tue, 02 Dec 2025 00:23:45 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-trixie` - linux; 386

```console
$ docker pull golang@sha256:ffaf0f60c933943ca989a6ed73da5bdf7145fa01d45586c31edc9353cd1035e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339965286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef3c60aa4ceab0ba4649d052fb256a8faa6ac8adea0ce1ee9485faed31a9fee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Dec 2025 23:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:59:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:59:19 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:59:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:59:19 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:59:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:59:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ffda96455ec1fb669c6471dd21a576b35020bcbe60b105c4f8f78e036b08b8`  
		Last Modified: Tue, 02 Dec 2025 00:00:10 GMT  
		Size: 100.6 MB (100555424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e158baf905b797d490e5c8a1e9b289b688ef3e407f3d18975f9aee4e83eee97`  
		Last Modified: Mon, 01 Dec 2025 23:59:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:234c9a5005fc0b142727701463e61286abab771e27f38a22e614729c143001d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de497c290f6e8554c3ac3882d0725504a5f2bb042e54ff7a858e5b9b2398e20e`

```dockerfile
```

-	Layers:
	-	`sha256:9fa5997b9c046c36c619cdabcb320924a31f719a221602d10b3517ae908ebf0a`  
		Last Modified: Tue, 02 Dec 2025 00:23:56 GMT  
		Size: 10.8 MB (10755774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d851ffee0d107a0001969133ca5b8d4bd4bf640d4a2b88bfc9b54d47cae628e`  
		Last Modified: Tue, 02 Dec 2025 00:23:58 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:157363fc54834097c6bf7c4a300dd77c9d31699e9b25c3a223165cd2aa5478bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336684119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f606fab4265ae9826d6506a37e0a93618fc192aabacb1081df0b2be8bdafaf21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 02:50:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:50:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 02:50:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 02:50:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f27d1d6766589192c9783cd48677f240bda846fcb9b1b3cc7956e55f813b1d`  
		Last Modified: Mon, 24 Nov 2025 22:47:08 GMT  
		Size: 92.8 MB (92815523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ee4242807d5eec61fa095a5c2f00f155044d9c099f2f96b9280a66eec7ef6`  
		Last Modified: Tue, 02 Dec 2025 02:52:27 GMT  
		Size: 90.7 MB (90741131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48deb93f3cbb45b7edc6ca2db63735814f002cd7dbbf1968321d2fa3ce51e7`  
		Last Modified: Tue, 02 Dec 2025 02:52:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d0681be89c4bed518bc9a8fc1fe8c9b51cf6eb4e6a4579ffee018af9d91fa99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd7ff4cc05ef0cbc54d79c4631eee027f02b9e5f1b141e8fb41ad839e545c80`

```dockerfile
```

-	Layers:
	-	`sha256:b0987ba1588bbe6d4471805e3cc5650cde7d2602acd2e214a86e6854c19cd7fc`  
		Last Modified: Tue, 02 Dec 2025 03:23:46 GMT  
		Size: 10.8 MB (10780296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4238851ebfcb1cb859bae167356e13d5e4dbfcb744335bf04dc42df822f7fa8f`  
		Last Modified: Tue, 02 Dec 2025 03:23:47 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-trixie` - linux; s390x

```console
$ docker pull golang@sha256:52f8f3a14109331265df0200df852baf1e6122962b24fdb671040808293b77d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313962149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f4a20bc6408728548972fec2719a685d62d4c191fe3fc6887044d6bb471154`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:37:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:24:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:24:38 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:24:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:24:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5391d091a5bc1ee814ac074a3bb08930ad54989e68737b6f3ab762b3833788`  
		Last Modified: Mon, 24 Nov 2025 22:38:37 GMT  
		Size: 75.9 MB (75919106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d587a6ce9332cd64ade4d6449590e6112812b54bfc350eb8b57100babd31c208`  
		Last Modified: Tue, 02 Dec 2025 00:25:52 GMT  
		Size: 93.3 MB (93286276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08440b358baed72456badec2929b9cfc484572f9545f484bfe295627a36acbb3`  
		Last Modified: Tue, 02 Dec 2025 00:25:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8a9ad182176e320f4c7059083ae4b5d4a2145ae1c47b3e1c579c535bb6b90c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12176d9f85665599a3eb4efa4259358d30d4c9a8913fccbb7da048fa09b819eb`

```dockerfile
```

-	Layers:
	-	`sha256:5238fb5dfee513c78bbcf6acfdc217087f6e7d29bdeb1f5b6005cfabd4935ea3`  
		Last Modified: Tue, 02 Dec 2025 03:23:54 GMT  
		Size: 10.6 MB (10594910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc50892474c067a4a7cabc7e2cad1b8f3555a94175c6a4f308d816bb5cc427b4`  
		Last Modified: Tue, 02 Dec 2025 03:23:55 GMT  
		Size: 28.8 KB (28791 bytes)  
		MIME: application/vnd.in-toto+json
