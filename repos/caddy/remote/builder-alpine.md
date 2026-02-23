## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:a807c727b59ca710be0562e3466f46cf3d2257a215f31958fb3a1a8ff28303af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:05a7cd7bab2e11284ca0d3863919f7bc3e5e51593b7ae6f15d6b817f6b7fc488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79756965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765c3f0160700a43c209ad593cf093902c37d911ed9ee1318df02d63883b2d77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:26:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:09 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:09 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:11 GMT
WORKDIR /go
# Mon, 23 Feb 2026 20:04:17 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:04:17 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:04:17 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:04:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:04:17 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:04:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:04:17 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:04:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e3cee16f61a04c1478b0bea063f6591a583f68c5ec96ad17bd6022fc6cf49e`  
		Last Modified: Tue, 10 Feb 2026 21:26:25 GMT  
		Size: 296.1 KB (296076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620ce275e86ec364135f603517679f51437c2da390313e710d0f78203dbae68a`  
		Last Modified: Tue, 10 Feb 2026 21:26:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93ca6407d9d5493df1c5ff7dbc24933abbcc0e09e49b01bf9c20e9550b52f8d`  
		Last Modified: Mon, 23 Feb 2026 20:04:26 GMT  
		Size: 6.6 MB (6575298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00175f00e306947d6768e9d22881590dcad73cf05caf3dc49d5c0e8bae9f780`  
		Last Modified: Mon, 23 Feb 2026 20:04:26 GMT  
		Size: 1.8 MB (1846507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114819bfe44ca3df319862e7bcca170de02f8368090fc066c0a4b08d9a467e02`  
		Last Modified: Mon, 23 Feb 2026 20:04:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:fe0cb49d5604f4160b87981b1bea4c981956d0107772c71097d1ac24d238aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 KB (304454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412e5f9f422fcfbd51e2325ff9d1513fc807fdb7021c8aa5ad843332b840e218`

```dockerfile
```

-	Layers:
	-	`sha256:1f697b4e2fa88aa93c545128a66565a5f6a64a4c0dc5670d3c2c05f285a02ae4`  
		Last Modified: Mon, 23 Feb 2026 20:04:26 GMT  
		Size: 284.3 KB (284325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994733b84a6ee90b937aabf7fd25ac78035eade9302c3e90624998476a6b80d`  
		Last Modified: Mon, 23 Feb 2026 20:04:26 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eda156eaea54eacc33b2d07ef1a92df962e8e873784a7980e840876bee812b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77830227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed453d182853a3a41327bf220ed9af7fd869e29f6a25553764988174b1835375`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:24:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:41 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:41 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:44 GMT
WORKDIR /go
# Mon, 23 Feb 2026 20:04:03 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:04:04 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:04:04 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:04:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:04:04 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:04:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:04:04 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:04:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82476015721696203da6d7b187ce059aa1747497aecfa10aab0ad0d3d8de072b`  
		Last Modified: Tue, 10 Feb 2026 21:24:56 GMT  
		Size: 297.3 KB (297256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8c7cfc344092b4dd309b4dad51d70b234cbf828cceaf1db4ff123fb24a325`  
		Last Modified: Tue, 10 Feb 2026 21:24:58 GMT  
		Size: 65.7 MB (65732874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efdbe5ba0a73b91f46539c38bdf47319b90f50d65f7b619c548c3964edaa16e`  
		Last Modified: Tue, 10 Feb 2026 21:24:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569a610b2c11a5103c9af3e584ae7b911e53703cd3ffbd0a5dada778426fd031`  
		Last Modified: Mon, 23 Feb 2026 20:04:09 GMT  
		Size: 6.5 MB (6484682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e7802cc04f86f8769059541b53521097725c355c09704dd0e696a0d8d4c6f`  
		Last Modified: Mon, 23 Feb 2026 20:04:08 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e45372867467b0dac5b0c0541352173e6509f01f5243fe58d4fdf4235925e`  
		Last Modified: Mon, 23 Feb 2026 20:04:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6f4a55738be100ca0ee35140f6f780880e9e2d5d7a4db01248839e5f546f1f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df9d053b4e7fca4e26f7866d14295741c9eec42371f813d413188cac9aad42`

```dockerfile
```

-	Layers:
	-	`sha256:55de99849544d57bdc18ba2199189ecfd3a5cd3af0f5f5fae5781fa8813fb1eb`  
		Last Modified: Mon, 23 Feb 2026 20:04:08 GMT  
		Size: 20.0 KB (20037 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2bd12e1ad180778fa72b33d3c4f92973970082768572eb3ada8e1e2cd24c0e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76984511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0b587e21a4dff257c923fc139b61fc5d3ee0dfdf04ff9bc668c1208aa5a030`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:25:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:53 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:53 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:55 GMT
WORKDIR /go
# Mon, 23 Feb 2026 20:04:02 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:04:03 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:04:03 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:04:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:04:03 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:04:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:04:03 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:04:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa6b9decca076b24306c10519b00d1508eda1afea03f299175186aa4610dd9`  
		Last Modified: Tue, 10 Feb 2026 21:26:09 GMT  
		Size: 296.2 KB (296203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6118fecef0033245b81c35f0d4b7665697c66691d88f774978bf9f5cce7b267`  
		Last Modified: Tue, 10 Feb 2026 21:26:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cda08d910cc4d22cda723a6f68264cb35133b891fa80ab8107b1cbd1d9c2944`  
		Last Modified: Mon, 23 Feb 2026 20:04:11 GMT  
		Size: 5.9 MB (5934351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4990eadf0c159e699553f976d0b9ec7b7a17905ceba2bfc7d80968f130cdfb5`  
		Last Modified: Mon, 23 Feb 2026 20:04:11 GMT  
		Size: 1.7 MB (1738758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d7b3bfe5f00852f6aac739db70c4dc06c693226501ad0813a01476d7af816d`  
		Last Modified: Mon, 23 Feb 2026 20:04:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ade33ff64f6ffa07bd96d8bf54f198818b2def1c00aebf1bfc58c3babf618e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cffe6922ee684c33b687464ad158e94269d2f940927ac366590200e09ba5c3`

```dockerfile
```

-	Layers:
	-	`sha256:87cec11254b46bd6d6f891430cbd5e12b8520d323c898ec146d9f73c0094abc6`  
		Last Modified: Mon, 23 Feb 2026 20:04:10 GMT  
		Size: 286.7 KB (286717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c725ffa1ec2dcc35d55337afbaedca1b5258ac114d0fc640808d7572d64f8b71`  
		Last Modified: Mon, 23 Feb 2026 20:04:10 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c32110f58438f8983e080a56a5922d586e57c1a5d3cb0c4974e57dc13422826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76955133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3404ea4a3f868198e64f75f5f19c8bae12c182efbdaf4e2e975fe8088423df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:25:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:06 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:06 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:08 GMT
WORKDIR /go
# Mon, 23 Feb 2026 20:04:13 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:04:14 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:04:14 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:04:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:04:14 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:04:14 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:04:14 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d9c3a927a28ecf581a47fa574a1a5538d465afa93bb1a79f5a436b7216ca4`  
		Last Modified: Tue, 10 Feb 2026 21:26:23 GMT  
		Size: 298.8 KB (298830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a52d54c85405c1aaea781ad1b2d56b6526341e5815e11e25961b7cdf03b5ae`  
		Last Modified: Tue, 10 Feb 2026 21:26:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02196d05ca904cb57e16638e5e34876f73816e6ec1a19646687c78d35f5e2435`  
		Last Modified: Mon, 23 Feb 2026 20:04:22 GMT  
		Size: 6.7 MB (6658237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b41fcbb0dbe479df0487c13fe3b97d6e0509b3b8e48c6f7140fdf836c0031`  
		Last Modified: Mon, 23 Feb 2026 20:04:22 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d999cea3da8dfcf2daf5b9e0077607d0c18455f87a5155b53ec84cf5a6a137`  
		Last Modified: Mon, 23 Feb 2026 20:04:21 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1d370bd7efc97849e465f0fe55d428c79eaafaa51c3208f9e39f6c23b31e5775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 KB (304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae672718a6cc4b6758029926f76bc734a4fb4583a7dbd7fbd826be07dc1e85`

```dockerfile
```

-	Layers:
	-	`sha256:9dc2ace8da23d7dd59dc10c0fa6133c89286d2c227507122e76f7b9f9528f7a6`  
		Last Modified: Mon, 23 Feb 2026 20:04:21 GMT  
		Size: 283.8 KB (283779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec54496555df48c5858680c904125d9c67e76d9aaa2032bbce4aeb738c1debfd`  
		Last Modified: Mon, 23 Feb 2026 20:04:21 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e91c2501af76f299ae3b4912fee49558ee2f9ba938ef936b9f1d59aa8b2493f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77559291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974639ed1554df9a86d24944a54eed3e173e47936918e1ab5730878a248ec3a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:44 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:26:19 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:03:15 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:03:15 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:03:15 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:03:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:03:15 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:03:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528c55315b3e5f2f548755f16a234f2386736177558710d4d0c6eaf02151f69`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 299.3 KB (299264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ec74696c53556914cd1f79d446767190917d608aabce7f4b38fe71a197a05`  
		Last Modified: Tue, 10 Feb 2026 21:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55ee0861271f84f5ebc790f96a35795891c99745108b88bf37e0dbf3a0507b`  
		Last Modified: Wed, 11 Feb 2026 18:26:45 GMT  
		Size: 7.0 MB (6993188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce8449ab7a021e8af32ca815aeb38bb4dadf2b0e9d8f5b14af881bf532842c6`  
		Last Modified: Mon, 23 Feb 2026 20:03:45 GMT  
		Size: 1.7 MB (1705998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37368feeedd88cf36a3ecd9c92ce8d54d37118651cde28d5a85729490604310c`  
		Last Modified: Mon, 23 Feb 2026 20:03:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:bf33fb9f17837f0be139ed82d36d31e26b4d352030b58458d01558920062ac1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355b0ffa3cea55f98e2792f2ab6917e7738f6a0e01e0c056f0f9132abf3e7cf8`

```dockerfile
```

-	Layers:
	-	`sha256:0100c374905232924492ab1fad34ac508dec08d6f7a3f9a4a520f161200d764e`  
		Last Modified: Mon, 23 Feb 2026 20:03:44 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3218c9829fcce7d9d2c756827eea077c1464d7664823a50c27b910ef645ac30`  
		Last Modified: Mon, 23 Feb 2026 20:03:44 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:455158c87246eb41745685414641a5c2de39af90c4db36b61ba156f29e6d7c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77413349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc81982de821c1e32061e1edadc3e7bdb3cc2967959afec2d32e6398f31cd35c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:13 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:35:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:35:42 GMT
WORKDIR /go
# Wed, 11 Feb 2026 18:30:06 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 11 Feb 2026 18:35:30 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Feb 2026 18:35:30 GMT
ENV XCADDY_SETCAP=1
# Wed, 11 Feb 2026 18:35:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 11 Feb 2026 18:35:31 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 11 Feb 2026 18:35:31 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e59666da981e3405c1b7fd86ade4932c92816496358034a16d9db56a3633b7`  
		Last Modified: Tue, 10 Feb 2026 21:32:56 GMT  
		Size: 65.1 MB (65055611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e55455435872cd4c1ef9316e502246b291158a9caaceb025496243cd1b415`  
		Last Modified: Tue, 10 Feb 2026 21:36:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a4f2ae0e3d68dee53846ccfa4cc3232831844e786dbafe470c465a777ec5d9`  
		Last Modified: Wed, 11 Feb 2026 18:31:34 GMT  
		Size: 6.8 MB (6751132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27ec770ccdbfc136a7d76267c2b766bc2954a81a75cf1354accbd0d9126a6eb`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 1.7 MB (1724221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e07161c5503128c3bf2dd29288ed307650240932a87fd6331f91151e22829`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1418e0a047c09934e63d62f4fc8cd99e401c5b064900f57a41cb8190ef547702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bc7bc13609979518a3669aeedf998f177fbe18351fb9f015ea626c31fd717a`

```dockerfile
```

-	Layers:
	-	`sha256:d31c59108e5a4a5cfea80984b8887fc0964a396ce6baedd77efb3a3a7349400e`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c2a0807b422fa1b85ba1a5c038de2a5266b754ea7a3fc88ddbe08572001686`  
		Last Modified: Wed, 11 Feb 2026 18:36:51 GMT  
		Size: 20.2 KB (20197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:1a1058d77406e3d29a50cd7dafc1166c8073bbff63240320605738bfeac747cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79070389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f148288c889a75caeb9847e6febbc87ba3875fd99e4bf13def7caabf8a05e4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:12 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:18 GMT
WORKDIR /go
# Mon, 23 Feb 2026 20:03:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 23 Feb 2026 20:03:49 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 23 Feb 2026 20:03:49 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 23 Feb 2026 20:03:49 GMT
ENV XCADDY_SETCAP=1
# Mon, 23 Feb 2026 20:03:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 23 Feb 2026 20:03:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 23 Feb 2026 20:03:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96012aea906c12635dfd37f261776f274a7fa57e016424f483ebb57edcd7c898`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 297.2 KB (297174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205873404541dd80f26800fffdfe4f93fa3bfaa4d5558142cbf8b4d08b79941`  
		Last Modified: Tue, 10 Feb 2026 21:24:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fa3d700433a648470ca50d2d723601e76f015648401b076c8f37ec1a624d46`  
		Last Modified: Mon, 23 Feb 2026 20:04:14 GMT  
		Size: 6.9 MB (6861678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae863d52ed62c1997edbd7ed5ca2f252b460a48d0343258f7fb5c7b62bb4ac`  
		Last Modified: Mon, 23 Feb 2026 20:04:14 GMT  
		Size: 1.8 MB (1782856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1aa06fc3b3699cb548851baa780aaba3576aff66b0690cf7ff9de1929f23f0`  
		Last Modified: Mon, 23 Feb 2026 20:04:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7ce2b6a97f3f0a40baf9a5ea078c3f5b16a28c44cf6ed5751d9524079ec8415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39e310e33e92a215d5a937da3e1aed397db4e047bfcd749451e572f0b126a97`

```dockerfile
```

-	Layers:
	-	`sha256:27d52a560b575d06e9f5c3412520ed35e4235c26eae8f7719ed162ba4730d6c7`  
		Last Modified: Mon, 23 Feb 2026 20:04:14 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3df47938827a2b72b2028f79032404216a2040783329c8563881a2e6f88c09`  
		Last Modified: Mon, 23 Feb 2026 20:04:13 GMT  
		Size: 20.1 KB (20128 bytes)  
		MIME: application/vnd.in-toto+json
