## `golang:tip-trixie`

```console
$ docker pull golang@sha256:1c185f37d6060bd097ee6f5aeed2985594b4e5390eeff4d2a470402b191efb08
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

### `golang:tip-trixie` - linux; amd64

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; arm variant v7

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; arm64 variant v8

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; 386

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

### `golang:tip-trixie` - unknown; unknown

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

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:812e6c29f83c02e6bf97f6894e92639220060eed0c9048ae15fea8ae403e6635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (335015416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1894421886e03893424152ffce92c01217bf4d8a223aab5bf70a33a7920f51`
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
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:19 GMT
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
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b525e17e7137fd229da32d2a7096f84f7388f0c19a95ebd4aa468127bbfb03ba`  
		Last Modified: Mon, 24 Nov 2025 22:39:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8a6f9d66418d0ff0d3a33c85138872dbef0d05f8b91490aa2fdb69ea20aa770c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e516c8c92327104e22f50c669be8d8f7bcae57abc9503961d603385dae2fad`

```dockerfile
```

-	Layers:
	-	`sha256:069c1c8c5f81f2b716a7b2158f03c85df8880cd0a900a2f2bc5171c228293cee`  
		Last Modified: Tue, 25 Nov 2025 00:24:54 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6a3fcfe6cf0d51603dae12114760d84e3d33f6cbf82dcecdd56f97132e4b52`  
		Last Modified: Tue, 25 Nov 2025 00:24:55 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:2bccd04dda994c93a1e8b8b57d5420f5d28978ee725a532b9acce42ac0b0a9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.7 MB (360659192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2169f3c9530cac6879360ebc4d6fca11ed770ba9491b59609b1435412e8973bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOPATH=/go
# Tue, 25 Nov 2025 06:38:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 06:38:29 GMT
COPY /target/ / # buildkit
# Tue, 25 Nov 2025 06:38:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Nov 2025 06:38:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737de4a2a89a200a514c4bb9d33946647ec30322b982a3272843e60840a135c`  
		Last Modified: Tue, 25 Nov 2025 06:45:54 GMT  
		Size: 89.7 MB (89678738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8b4a6dc3553e5332830083275a80d1003edc99a4ff6995f70b8030c856aa6`  
		Last Modified: Tue, 25 Nov 2025 06:45:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1360cd946ac4113d17d9e1f9a44b4b0b553ddd6af1657e70e9d78f5710237ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb354b97d10cdd79bb519299450684aa6b7456d73c52766a870d3be530830d1`

```dockerfile
```

-	Layers:
	-	`sha256:63197e752608866fb011fc9c05e3f1ed11eee0ffde60bcebe8ac1418665284ab`  
		Last Modified: Tue, 25 Nov 2025 09:23:41 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1b820d4899b7663101108f3a9a02261f463356efe68076c83be852ea6d3e18`  
		Last Modified: Tue, 25 Nov 2025 09:23:42 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:21913d62ff0f28b17a79145ab41dbe5d7797a5110727a14189ccdda3a2f27eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f135c375a7e3d75751728953b31790670434cc239fb783565956c7ca3573a89`
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
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:19 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:33 GMT
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
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d99ac0b0e47494d2aa39ee729c5bc0a7aa6524f62afcb7c26c08c6c25c1aca`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c36e4dccef71e613dc7c816c7ef66347523737d7078caed3e277a5982d64be6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b177af9fbca0868a1b5a0af5b0b96a6e808903935dd573663f7fb53bf0d2626`

```dockerfile
```

-	Layers:
	-	`sha256:3a35c157a4a759e214afa5a7be7b01ba2b2af706e4d2eee40013492360c3d3a6`  
		Last Modified: Tue, 25 Nov 2025 00:25:49 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d615f7daae6d48aeab9a79cc614756f7213c0479c1a0bfd52dd9c1bc58ae32`  
		Last Modified: Tue, 25 Nov 2025 00:25:29 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
