## `golang:1-trixie`

```console
$ docker pull golang@sha256:3c69d72833046dc2fda795c57b7a44f8b4060d5319f0a066ad72812b96c0f70d
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

### `golang:1-trixie` - linux; amd64

```console
$ docker pull golang@sha256:42a6459ee5ae70dd490c6b6164bef32b064a66b4f0a9744105969883b8b23840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304770279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba81a847f6b20b63eec32f2ee16fce0385e8b06bf5789a66d4e51aae215e8cd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70dc87628705e52d31a6bee046711fe5dd4d9d73e7cfd02aaceec20b352ca48`  
		Last Modified: Wed, 13 Aug 2025 18:08:49 GMT  
		Size: 102.1 MB (102055737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9463fe86d3b832fec17e98dd4dc2def946be2ce83848b242e45383fd2aba0d3`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c2f44494df707a4f1b93e46b09d19a6788706df78ba1086426dcb6538063cb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d788b0789b1186b2938dc77dc64d28993b93984a851b3b1d87a03aa708b9fb2`

```dockerfile
```

-	Layers:
	-	`sha256:1338b5ca471b8c4600997559b8b3d81682f58d7ef6f73d7981c03854035e1857`  
		Last Modified: Wed, 13 Aug 2025 20:22:34 GMT  
		Size: 10.8 MB (10779702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e9864da0ecfa25114d8a1a8421ab971eed2dfc2e776e53f4aae914c9e07f98`  
		Last Modified: Wed, 13 Aug 2025 20:22:35 GMT  
		Size: 27.6 KB (27619 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:8e427a719feb8937ff9fbcd5855200e84566d29cea31902543e68d794140f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263720334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe3db22fa9dea736b82fc129406cfdbb42cb5f7bf733e55526422cd1e6dc4be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf1e0378255d85ce69e42b8c2b4e52765a17bb9940e69e2993debcac329de3`  
		Last Modified: Thu, 14 Aug 2025 05:24:37 GMT  
		Size: 72.7 MB (72699087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c703f6c50724eb97f6a66565f1c7808fbfc6ea42ff17ead3c57f21bf55f34c`  
		Last Modified: Thu, 14 Aug 2025 04:29:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:aa530f96e1856b84cbaf14b41d6f7f571fbb671f912b37a8441f0e57dd97f574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed9cda9f291058018753a454878dd5bc10965db5d62ecd0c1ee81582d5685fb`

```dockerfile
```

-	Layers:
	-	`sha256:2e827d50b86fe1d116605426e2c742ae2a55f4def49d8544d8a5866b394e1b60`  
		Last Modified: Thu, 14 Aug 2025 05:22:27 GMT  
		Size: 10.6 MB (10575623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f1bd941ea459b178b2e0b5e2562d4ad4a5f3741c7c02bcabbc196366e66618`  
		Last Modified: Thu, 14 Aug 2025 05:22:28 GMT  
		Size: 27.8 KB (27750 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d9a24f529255422e943588a1cee714b8a8a5b5a4f4ec65ca03da02f8813915a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294587842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e6adee78999ecbc83db1f1f39bae538672757c0978cb0643cfef972d5a7069`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37d0607fbadafadb0268414200aa6130cd6c0bae8f71fd256b7b553f69c7c0`  
		Last Modified: Wed, 13 Aug 2025 23:02:50 GMT  
		Size: 94.8 MB (94782268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011ba51ee5a6fed7c7d5f0a18316d9f6cb34cac7bd9ab9a88bbfa83406ac0786`  
		Last Modified: Wed, 13 Aug 2025 20:54:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:17cacfce77a50073977ef9c07ba586f6c873021c92ab7eed360c5c4b4028a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10906199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7d96f7ff925f4aabaf247b46cac0124f9062a4294e229d0edbfae6b7f19384`

```dockerfile
```

-	Layers:
	-	`sha256:0be32189c64510c4844122e0b071b01e5dc405a4e1887296cc811c10c276a9f1`  
		Last Modified: Wed, 13 Aug 2025 23:22:37 GMT  
		Size: 10.9 MB (10878401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b54e6da510a774d1adaf55c9a849d5ccdc0992a440d89dbf04d63e27fd76d4c`  
		Last Modified: Wed, 13 Aug 2025 23:22:38 GMT  
		Size: 27.8 KB (27798 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:e00c323b68ba409da4ff9b9b235e9ef0378b4cebdba8e92dee128ffda323f54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306623563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388ba1ad1da93f4b100ab9e4552eaae4b5224ef249512984d1216d2695b64302`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cfa3d99852b1a9601b0daf1182a7b357b02003d6a94d288a9d9a81d2064985`  
		Last Modified: Wed, 13 Aug 2025 18:04:48 GMT  
		Size: 100.5 MB (100498738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c63a4b9dc1f72141c9a2ae757dabf818be084da59430ae2f1f1200a26ac66c`  
		Last Modified: Wed, 13 Aug 2025 18:08:47 GMT  
		Size: 58.8 MB (58763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4bc49dbe90b65b82349bde68539bb54b456c40b48c6b317a4bc48b8e13031`  
		Last Modified: Wed, 13 Aug 2025 18:04:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:156935525d6e8c0ee0dc02e3bf4297d30e77729684ecfa5ecc8ceff8e57766cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10778511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfd0bc473014ed16fbb0a23fd70c472b64d88b3a9caa8066f86941367c0e651`

```dockerfile
```

-	Layers:
	-	`sha256:79ffae552c877974cca086873201781d64702153545e7ac5c167717719fcc287`  
		Last Modified: Wed, 13 Aug 2025 20:22:58 GMT  
		Size: 10.8 MB (10750948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e57bbc65c50bd06cb29edff8a36e671dff83c3cfd8080b4961aeaee962882f1`  
		Last Modified: Wed, 13 Aug 2025 20:22:59 GMT  
		Size: 27.6 KB (27563 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:1b387b4172cc166bf35a70db9917de4742eb870d3e39d06567dd71bbd524f57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303910921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f549c085f037e7052183aea77f69b27118f84892d08855a05c94d03f583afa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8871c45a7119988c7d962199f82d487aefd5e752fd9f98ec06c4c6735662dba`  
		Last Modified: Thu, 14 Aug 2025 05:07:23 GMT  
		Size: 92.8 MB (92760751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab2e5ff787e1179d756ba4efce4d0d780ec06870eb0d576cffeb58322b701a`  
		Last Modified: Thu, 14 Aug 2025 05:07:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7fec38f2f6447e3fe202739c855102136e6f4f576e077698087b5d8c412b360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10803198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f9429bb991b88f96dd99043a964ff70daa532a063a64b5a556cfde697b05a7`

```dockerfile
```

-	Layers:
	-	`sha256:7bf86636ba312a7f2e8e9e3f7ae605453d68b2f00e7c6f8295c470a941586b45`  
		Last Modified: Thu, 14 Aug 2025 05:22:45 GMT  
		Size: 10.8 MB (10775510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a9f50b2fec9255ddbac2a43b4d85f788be0a946ada931e19e9910b550f290b`  
		Last Modified: Thu, 14 Aug 2025 05:22:46 GMT  
		Size: 27.7 KB (27688 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:daa11e57043625c57a1375467464f6a367f02ab05f7e7565706f44eb9e1e33cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279990695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee682eb93ea9f0f00744cb0662c861fbf889b357cc2a62faad498b4161f2d05d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8a5c04d7aeadb022d07f505d9b83a50ffd376444c5e618b1f58391961e8e9`  
		Last Modified: Wed, 13 Aug 2025 22:24:01 GMT  
		Size: 75.9 MB (75869997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8daca573a2eb6571030172e0e32cd66cc2938db208ecb1dcd2ed6f4a23a4f3`  
		Last Modified: Wed, 13 Aug 2025 22:23:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:630f566bfff331ddad4908a8a5bfaf940f8f711394dd378be697233ade01679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10617717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf497fdc2a92cc38ede9130d50906015b66fbdf5a7d6323852f0b85e705a33b`

```dockerfile
```

-	Layers:
	-	`sha256:88cdc4f989a818003918c38390f3fbf8134b5ff31fbba44faf2e5ca7010f2826`  
		Last Modified: Wed, 13 Aug 2025 23:22:59 GMT  
		Size: 10.6 MB (10590102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e829716039109b6900f69df59cc200af007514b4ac57d20f987e91531b431551`  
		Last Modified: Wed, 13 Aug 2025 23:23:00 GMT  
		Size: 27.6 KB (27615 bytes)  
		MIME: application/vnd.in-toto+json
