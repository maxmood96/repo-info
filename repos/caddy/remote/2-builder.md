## `caddy:2-builder`

```console
$ docker pull caddy@sha256:ccd4503985eaa4aac67dcc75632ab9e9df5bfb55241c95dcd7654f7e986883d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:757db01697633c7a88078b90988a2be2903180fd3708cd194916437b7a5e5e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79800752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4fc52b7897cc9d17dd24adfc4c4d43f3080165453b12e356dd02466c57192a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:04 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:06 GMT
WORKDIR /go
# Tue, 07 Apr 2026 22:01:28 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 22:01:28 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 22:01:28 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 22:01:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 22:01:28 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 22:01:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 22:01:28 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 22:01:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d8f694c0bdd364dd5408954388b3f41362d164547ee1220cf63228070797e`  
		Last Modified: Tue, 07 Apr 2026 21:14:20 GMT  
		Size: 296.1 KB (296072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e09229ea5a178f7882e59cd830c6d8179c2c018c6bfb99f585cb87a716c0ad1`  
		Last Modified: Tue, 07 Apr 2026 21:14:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54efda26b9affd27345edd647672e7023d112863e2100a8131733ebffd0a453f`  
		Last Modified: Tue, 07 Apr 2026 22:01:36 GMT  
		Size: 6.6 MB (6575263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b83ee6ff1dc2472a4ee48cb4c967382433a55ec4f856c97acbb082f2135597`  
		Last Modified: Tue, 07 Apr 2026 22:01:36 GMT  
		Size: 1.8 MB (1846503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73d152f50dda34dd641f9ff79c4fc93bb034fd52373c76884b47d2435bc3565`  
		Last Modified: Tue, 07 Apr 2026 22:01:36 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1ffc319f55f1eeff848902fcb426216afcb25113caffd7d2037f0e153461d76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 KB (304454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff228394eb07ec33dddca75f163fa755544adb0aab47c5ed7ada92908bca08c`

```dockerfile
```

-	Layers:
	-	`sha256:b4484b533a60f2748b81154e17ccc9c729bb600686ccb7983962add68b4e8d85`  
		Last Modified: Tue, 07 Apr 2026 22:01:36 GMT  
		Size: 284.3 KB (284325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77a27d79f71ce2c931d8f3d229bdfe64f6cef8459ea21ee35ebd8fa16a5a2fe`  
		Last Modified: Tue, 07 Apr 2026 22:01:36 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:377dd57913b640d9421fab15f4ec803f27622c99a64d78ec38fe5d9d2ab7cb53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77848724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0ec3937b183baf62431885c47bb7c573a40e78a77de1793f22064de0bfed4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:16 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
WORKDIR /go
# Tue, 07 Apr 2026 21:59:42 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 21:59:42 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 21:59:42 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 21:59:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 21:59:42 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 21:59:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 21:59:43 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 21:59:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e87b3254de769a256e43be6b111c8d3e8808cd67aad52a0b72e430d18305691`  
		Last Modified: Tue, 07 Apr 2026 21:13:30 GMT  
		Size: 297.3 KB (297257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5a4e2604d6b26da5598245b3c1e539bc25abbe79f898b39130896e768b62e4`  
		Last Modified: Tue, 07 Apr 2026 21:13:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcdddc3b0f0027694250604597d2c52b204c11891c7ce5cd48bcac484bdb3d9`  
		Last Modified: Tue, 07 Apr 2026 21:59:47 GMT  
		Size: 6.5 MB (6485030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca592296d205adec95d7fbf7730c05b4c6856cd343ec0246ef7f7c682eb776cb`  
		Last Modified: Tue, 07 Apr 2026 21:59:47 GMT  
		Size: 1.7 MB (1745001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899073f8ac8b8038ebf12c54ede5f346e865ba541f3d8e23a23ddfed27baef2a`  
		Last Modified: Tue, 07 Apr 2026 21:59:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ffb692b1b76bb0c86e6ad7841df5792f0157a25d59c0f7b39167e0d2a78bd962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014378501012f010b2cec08042c65ffd40a47dd4bdd232ca2165e3c7cdc00a16`

```dockerfile
```

-	Layers:
	-	`sha256:54cbd3cd1c56eea724d1e3e25071e11f950afe99ff8d22e7b889dbf57e9c3e22`  
		Last Modified: Tue, 07 Apr 2026 21:59:47 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3bfd9284a3d2fb6aaae0d59cb3690efe6cb366b9df52a4c1d016a056d64f27ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77002683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8243c8229b977312a8e17e005d3a68bfd589c67f42e6aa360b820943edf7ee0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:14:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:12 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:15 GMT
WORKDIR /go
# Tue, 07 Apr 2026 22:01:19 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 22:01:19 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 22:01:19 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 22:01:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 22:01:19 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 22:01:19 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 22:01:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b3d19c8966500e34df8c4d763f6c1a8f37be1de7321cdbcdefb9d01c6a70c`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 296.2 KB (296196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b788dba2764741459e09a0ea7605019deb67fbed88a9a86398f61f23be05dfc`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec140e3680fc04a5f54d26e533643dea53f16b22894dd0eea34e579e77ec90d`  
		Last Modified: Tue, 07 Apr 2026 22:01:27 GMT  
		Size: 5.9 MB (5934440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baedb9103b543cb12fc90df77e35aa75b5fffa67282b9359c35c46d3a66316af`  
		Last Modified: Tue, 07 Apr 2026 22:01:27 GMT  
		Size: 1.7 MB (1738754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4e139d2b5e8bb8b551a627f2d70c97f2bb3b36cd4db8b525425c016e70bc`  
		Last Modified: Tue, 07 Apr 2026 22:01:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:067812d053f31e304356014720d9565c550cb11983bf5e4d04150d39379a8c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f03bd17115bb30e5d0a8e24f3d5afa4ca1ae4ac8c04096909b5a0e9ffa284fe`

```dockerfile
```

-	Layers:
	-	`sha256:733a0217925b995e6a025affde4b2954634500884f81dd6f4ce805f110f10b74`  
		Last Modified: Tue, 07 Apr 2026 22:01:27 GMT  
		Size: 286.7 KB (286717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485628dcadaaebc13eef53177aa2958fc79d45aef76a7d684e03bc877674e2c7`  
		Last Modified: Tue, 07 Apr 2026 22:01:27 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:08dc70cd2be4cbd0742d5a5619b137f6ae16e3f98a6a654f0d35126c755f39ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76979904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b93c589e4c275ed272942387c3b0a6346415a68c2edb38185ea614b4969af8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:48 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
WORKDIR /go
# Tue, 07 Apr 2026 22:04:14 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 22:04:15 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 22:04:15 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 22:04:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 22:04:15 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 22:04:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 22:04:15 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 22:04:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1f5a7ce8cd2196e4ce4b6d177083870b0457fefda71ebf6f3eea195fb8fca1`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 298.8 KB (298845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9954570ab45fb86f36b4100a20e81ac2a3738a59e2c42f9de3d1ef5d104f5eec`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f976473ce6fd3084451526513c0d475899f7128057eca22b7220aa593c778e5`  
		Last Modified: Tue, 07 Apr 2026 22:04:23 GMT  
		Size: 6.7 MB (6658238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a674f34e13dd7d4f559d11d6d0614ac28d69132d0436d8dc17c06c672ca050`  
		Last Modified: Tue, 07 Apr 2026 22:04:23 GMT  
		Size: 1.7 MB (1716380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca591a345b463ab2e6a876b4c4300585a51de5c774fd389a21c2ae7e565048`  
		Last Modified: Tue, 07 Apr 2026 22:04:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:529117a86bad0c47a49ebfd72443e4dae9f4400d8899c2bbeb2f17b580763d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 KB (304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e426134dc0d92ca21f6838fef7a09bb0dfb31d76a0e6e0381d48ef81169b905c`

```dockerfile
```

-	Layers:
	-	`sha256:183dacf90569daac98dd834a275cb84256abe78e22cc071bddee3f31b2611700`  
		Last Modified: Tue, 07 Apr 2026 22:04:23 GMT  
		Size: 283.8 KB (283779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98ab0b5641e6634c4181afa529a1f1dad661b2ae28cc4bc4bdba31c846c32b4`  
		Last Modified: Tue, 07 Apr 2026 22:04:23 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:63b759413cedfce94857f811ff24bf4f16722ba78f52f2d6fa932636e37d8077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77586607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c16a668c0d704966b7aee5b27f48f5e6c597b77bd23bb8ce4c7c01776d3041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:28:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:28:49 GMT
WORKDIR /go
# Wed, 08 Apr 2026 02:40:53 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 08 Apr 2026 02:40:54 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Apr 2026 02:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Apr 2026 02:40:54 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Apr 2026 02:40:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157c37b8ca35f88bf66161b72bc1761ade8e543ac3a14868075a68b5dff95e5`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 299.3 KB (299270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59cd64739ee2c1db9b4eb7c08338d6773eef47b2c94a225b64cb228ac665cec`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7660240a58a343791f9ddfc593fed679ae836be1f5efebfdd6c616d996c61`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 7.0 MB (6993346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3367975427940e88bc1d08204bc0b02e3d5825c56364e6c9d4c4fbabea9e42a8`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 1.7 MB (1705992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9459b8d487af4148880bab184d49b8cc5d3cd615a2b79b4bc57198594109b007`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e24b0b95b5c9fe33e5128c1c08cfca98e2d51b29ab6b4b419b981340b9989e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788a1a3c73ccac753cb34992ca5abe9acedc402f240ba6ec60c211aa65c01bab`

```dockerfile
```

-	Layers:
	-	`sha256:01cac4bdcfc723c6d6bf41140df184150407905a42d81a66c7ec9ca42136f591`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acbe01d6b3aba68e1719acfe1806d184952ff5eafd14a564dacd6744586d81c1`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:061764f40bbb07975c70576eef0ba931894ff4be8adf309d33d2a92cd4f90c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77451742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638708ebdea0f4f9ba216b2947c6112c4a1ed589aa89bf74c0ca1d5cd745763b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:31:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
WORKDIR /go
# Sat, 11 Apr 2026 21:09:24 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 11 Apr 2026 21:09:25 GMT
ENV CADDY_VERSION=v2.11.2
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_SETCAP=1
# Sat, 11 Apr 2026 21:09:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 11 Apr 2026 21:09:26 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 11 Apr 2026 21:09:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18820a12075d850af6085d052799ca6c42481c33ddc318143f5caa48480e4d17`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc15650f7980fbf7a29c9e27c7b1c34c70c9e717c7e182174c904a0c55105760`  
		Last Modified: Sat, 11 Apr 2026 21:10:47 GMT  
		Size: 6.8 MB (6751286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3749dd26165bd4355faf91142f39910cbda5876e1dc4cf4dab9fddf2554fd`  
		Last Modified: Sat, 11 Apr 2026 21:10:47 GMT  
		Size: 1.7 MB (1724209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a25c28e9947ea6e2c6000af587456747f7aa3e55efa5c7eadf4a007e844b3d`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:cc81ed4864c4f09898f412d01a8eaff9537e120ba4be38a625b82a6ee7addefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9def5331bf193c0ea89a0eccb20423a36caa6cc7d600ff96b97342b281b6039`

```dockerfile
```

-	Layers:
	-	`sha256:d19d6adde38b5da7d5191598e003d9bb649d2083eafce71d538afdc41b8df1d3`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae938f7d1610628dd37ea8092027495f22925a718f97c11ca6796d6c7b1f203`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:eb106425c2387dbc6faf5dd55a484ef040bf0cfa8cc00f67e20d66124ae964ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79099900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9c84295d8be77d8ae7ac50aff7ac12c9bf4eaaa26b76cc49c7fd1a3105cbe2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:40 GMT
WORKDIR /go
# Tue, 07 Apr 2026 22:04:17 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 22:04:18 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 22:04:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09b3320db87c0fbe713adce5ff43836b299964a204ab829de72270c3d2d4c3`  
		Last Modified: Tue, 07 Apr 2026 21:14:59 GMT  
		Size: 297.2 KB (297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b98e3267789cad196300f0ede7760a8353c331b3221d7fb9a3a72d8fbfdf`  
		Last Modified: Tue, 07 Apr 2026 21:14:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b737ea8ec9d63365ff60c8b99e726ff26aa8514f669bb267ae37f69899128`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 6.9 MB (6861734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b7ddcbac288653a375c431efa9f8af6443cf4a3c5ae9782b10be536504644`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 1.8 MB (1782858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f29edf9e907c0fa4161754bbf36af59b2935e2c722f9fb74dbcd3a6a5f1544`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ca448a2154011b1db01eda252697e59d68aedcdae5e41b7e88a50340a6b7313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e0ab570344fecd612ffc77eb9ca78f2ccc6246f882cad274c477a2ded8192`

```dockerfile
```

-	Layers:
	-	`sha256:6676fb82501162c57b41e7f1c6453d26500db360347fbdf3179464bf46be0564`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632d4c353f354beac0125d53b75d1105e3ea2144de4689874b46f12b90f6c591`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:2db6f5b2d72b74a60424ec6c12d7ed592bb0cfce8472fa224379d8e952dd0feb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253777028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decd5897c725561f52899ffa5305f301f1b7a3c40a3cc8f04fbc28958a21e511`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:11:49 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Apr 2026 21:11:51 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Apr 2026 21:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:12:04 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 21:12:09 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:12:09 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 21:13:25 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:13:26 GMT
WORKDIR C:\go
# Tue, 14 Apr 2026 22:15:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 22:15:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 14 Apr 2026 22:15:19 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 14 Apr 2026 22:15:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 14 Apr 2026 22:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 14 Apr 2026 22:15:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00876c5c306a40bdb91b29e1bfe5c5e3a30957345f5b4217492950932921f085`  
		Last Modified: Tue, 14 Apr 2026 21:03:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab6f7f8c04a918d6984281136988db80e26d2e49e506c24235a6aa24d3ddf8`  
		Last Modified: Tue, 14 Apr 2026 21:13:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9a4de2d156c81a0b97862c3aab31aed462414093a7a3548c0e075dbff4df45`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905977893c27c80019254fc21606d27924fc7e8f15995ca1e93d995d0f9da1e1`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11d045724382783805a4ed4a39e0438de91e10ce9ca26c4c1386c8c1a42022`  
		Last Modified: Tue, 14 Apr 2026 21:13:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517fa67870dec0ffc5542cea5ab7d6f5965077f9b323899b2c9e3c769823b2e`  
		Last Modified: Tue, 14 Apr 2026 21:13:38 GMT  
		Size: 51.2 MB (51227687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0c782a756fd5efe99734cebd326bfa111492e8514da6ba7ff44f2f23b0781d`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897c264ceb6ee8f252b0fdd9730a6339aa994740a00c6ecc3702353781a65dd2`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 359.4 KB (359353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afaf9528a576024002874bdb07610060adbb25dcf8cee62e667f97304a75e6a`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd318c5f8d24379da8ea97d3b862c1a1c3fe17f62a8c3168da4a9fdccbcfa1a`  
		Last Modified: Tue, 14 Apr 2026 21:13:41 GMT  
		Size: 69.8 MB (69844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccfb531c02a788d97bfa192c0263ddafe73165dbf8bb40ea3cc1195581d6fe`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e486e126769f091a2aeb3ab6ea4ed235604973febecc511d3b769d2dec609`  
		Last Modified: Tue, 14 Apr 2026 22:15:41 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ed23f5627c457b711d5889338f163eed880706ec2f89d1933f68438c2da592`  
		Last Modified: Tue, 14 Apr 2026 22:15:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d7fbfaf5e06548246bbfce7c694c04a15b0c188ca34fb99d3c9604be5cbd88`  
		Last Modified: Tue, 14 Apr 2026 22:15:39 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b5c3a89dc4dfea341b06aefb5204962a7ec0724eb001689b4e96ec2ef1ab8`  
		Last Modified: Tue, 14 Apr 2026 22:15:39 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c37053655b582896b9926dd0835c1247c5323ddcd21177f337866bd03542ce`  
		Last Modified: Tue, 14 Apr 2026 22:15:40 GMT  
		Size: 2.3 MB (2341993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6251418a0bc6618b575326052dfb21a42a7d479e0f5264813fb8a93fb6093808`  
		Last Modified: Tue, 14 Apr 2026 22:15:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:f406c29bbd1ea56fb076dd361d478b75cb19f044bea97ee87db6c4a4077219a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2194040548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478629b7deb1f75e139d42cb5604ad8470cdc0676f154b1cf09078d0674f7013`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:27 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Apr 2026 21:16:27 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Apr 2026 21:16:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Apr 2026 21:16:30 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Apr 2026 21:16:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:16:54 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 21:17:00 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:17:00 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 21:18:42 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:18:44 GMT
WORKDIR C:\go
# Tue, 14 Apr 2026 22:17:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 22:17:11 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 14 Apr 2026 22:17:11 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 14 Apr 2026 22:17:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 14 Apr 2026 22:17:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 14 Apr 2026 22:17:20 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebcfde08590ee1d8e1fc13f10328237120c5059d4cb5fb9cca78ef9475f3a62`  
		Last Modified: Tue, 14 Apr 2026 21:07:22 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d090b769fc5e142d320bef003f0bdb353b56d05203a83f1583a9d263e6a20303`  
		Last Modified: Tue, 14 Apr 2026 21:18:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579af4f3a0b4882445e7c4e593e5cc4b68b5cc575937bf85d22ed7c0a469115e`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726be3d7369a0206806f3dbb666744d68c9a77a4d48528dee84fbf4af0e002cb`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a477df0158ff310f6e299e9b273e3f64da64606f523131ab2f45f07d27d90`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f0c7a95636b85106b0c191c8d9ec0d8b5a492e0b44b05329b8411b8b68e8f`  
		Last Modified: Tue, 14 Apr 2026 21:18:56 GMT  
		Size: 51.3 MB (51347005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2299b8256c980a964ef2eb57ce33daafbd269dd7b9c23c12c9ec51c1cb1fc1ef`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e5548fbd84ada2f921610c3795968099a10dd5656ad21960a6dfdc6c8df095`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 335.8 KB (335788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf3b50d1724544802ab699d194893340124dddf14863ecee5182cd9c144293c`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50c3513b2c439439a0494bb8443f20c22b1bbdf00fc0f378332c5e2deb545b2`  
		Last Modified: Tue, 14 Apr 2026 21:19:00 GMT  
		Size: 69.8 MB (69837725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04d5273101b31beed5f88bf60da131b30ac28731b927c7e024e8942a216854a`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613956ff8d54b52ee2aa12091fcef4d0254c5057a0bee47c80c39cfe26a2ef2`  
		Last Modified: Tue, 14 Apr 2026 22:17:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7d4aa2c1dfa6e3f66309c09f16c25fd1b8b3851c72e4fbfc645f62604a60db`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa8eb8e0843dd0ec8c326d18f75aa21c10b0046297e51e4f89e4b4ed9ae233f`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8e16bd0b28709e68460e16339f49ab7cdfa4f5ed0fc6a0e1f7003008eb3b6a`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11acacec55a29ea94582e7a1e15c915c6d7d9f1c208fe004676cb222386bb8d0`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 2.3 MB (2291602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52a3926feb603f3e034777e4c32c145a48d8ca78cb213695116cfa05ede3de`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
