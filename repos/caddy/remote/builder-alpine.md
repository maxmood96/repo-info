## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:afedc89367579c34450cdd8434cb6cd695904c78252c2ee0e3c002c33a044ea8
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
$ docker pull caddy@sha256:10e72d55d88aaf0e0c080fa391be15e1539cb9619be76cf12ad34a2fd7a241d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72506880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6021894f430e753ab3b74a77df2f4ed058c1b590b2c610d13ac841783d53b5de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:03:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:07 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:07 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:07 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:07 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:09 GMT
WORKDIR /go
# Wed, 04 Feb 2026 17:07:39 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 17:07:39 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:07:39 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:07:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:07:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 17:07:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 17:07:39 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 17:07:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ce277f7bef343b415398bb29bf0f48b3bcceb80e80a532721e9a06fd08ca76`  
		Last Modified: Wed, 04 Feb 2026 17:03:52 GMT  
		Size: 291.2 KB (291157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdf71b47847e47b44531d019e8eed7d243fd7189fe6b14cf6754724b04fbdd6`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 60.2 MB (60156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e87308bae76cf5b68cf7a2b9decc25387807a4d371b03c0a9128ce7a7a96ba`  
		Last Modified: Wed, 04 Feb 2026 17:04:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e1da59eaca4e546ffe4c0fc604e174a7581f680a5131a41e8acdaa6cf03562`  
		Last Modified: Wed, 04 Feb 2026 17:07:47 GMT  
		Size: 6.4 MB (6406782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674f46e7b06284ee5897888cbe0672e7fad337ebdd4983bcc0d7567b471c67d1`  
		Last Modified: Wed, 04 Feb 2026 17:07:47 GMT  
		Size: 1.8 MB (1846502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad2b021a0bec2fc9b50931714ed0761b0b007e664bf80a04c9299aa88c5eecf`  
		Last Modified: Wed, 04 Feb 2026 17:07:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7bbd0119bbb1851a89e53366c561089bff5365f71ce3cfed146e27fc8b10b4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 KB (300731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada0a5f09b6459296f744d54b673361e20abe0fb6db75f6f3f0477ee40bd5f1e`

```dockerfile
```

-	Layers:
	-	`sha256:ae97f153e688315873300dc2b6a6002d58102c856f98e5acd83cff63146a626d`  
		Last Modified: Wed, 04 Feb 2026 17:07:47 GMT  
		Size: 280.6 KB (280602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f99507958cb1875b608974e981720f54f6ae45d9116f9456c4ee2f5fabd40d`  
		Last Modified: Wed, 04 Feb 2026 17:07:47 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b068219188fc64fc5b2a71ba66c3f39448430b61d28536c3dfd0de0f53dd9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37dbccb5befcbc24ea211bc00205d723c36efbd3abc7ac9a908cef0978b953d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:25 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:25 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:25 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:27 GMT
WORKDIR /go
# Wed, 04 Feb 2026 17:07:37 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 17:07:38 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:07:38 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:07:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:07:38 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 17:07:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 17:07:38 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 17:07:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d8c224ed2cfb95ced59239a93763bad35f41e45df56d3950d7b3775ce49d98`  
		Last Modified: Wed, 04 Feb 2026 17:04:38 GMT  
		Size: 292.3 KB (292294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4a839dcd7f0a026f4b21f2e42b36e1fcba806c26b99b4544e89678a699bf5c`  
		Last Modified: Wed, 04 Feb 2026 17:04:39 GMT  
		Size: 59.1 MB (59076135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c29d68c46bfe3b572eebcb2719522676d5feccc80d0cde1d5cfa7fde6d2bc0`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebb63734660e36cf29371bcd877e923e2aa867343a59c0aa52cb27d74a9aa03`  
		Last Modified: Wed, 04 Feb 2026 17:07:43 GMT  
		Size: 6.3 MB (6325421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80ae185a8bab0d5aa9efbeb7b17669b34fad34ee83a0ea4808424fec7d70e25`  
		Last Modified: Wed, 04 Feb 2026 17:07:43 GMT  
		Size: 1.7 MB (1745000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab657e38f46fd99a95ee76d1e9d11083fb0e50842210879f4745cd86ca11f3f`  
		Last Modified: Wed, 04 Feb 2026 17:07:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:febf263a8c6d6b065870429955ca81c94ee43a1010cc333d8db54e2c35e4dc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31c0db59e49885aa2d0546651c6a45d20288579e96cf822a14b4ee007dfdf4a`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dda97df3636a98c6bd5d3217a9befb8df0f87f8881a099d4703b81d30b7c6`  
		Last Modified: Wed, 04 Feb 2026 17:07:43 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3cfac12e7b3f9da181c44e3b8298f646d57eecd8af59df510e3ca8b67f5ea512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70124810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e09b7636a7cca9445e918feb94f2292f4e0ba89a447a08fdfe9756107838e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:03:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:03:50 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:03:50 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:03:50 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:03:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:03:50 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:03:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:03:53 GMT
WORKDIR /go
# Wed, 04 Feb 2026 17:07:23 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 17:07:24 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:07:24 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:07:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:07:24 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 17:07:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 17:07:24 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 17:07:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a96757a765b01c8bf90d143929cd70172c6f52171487f17c1a1c1fe078987f0`  
		Last Modified: Wed, 04 Feb 2026 17:04:06 GMT  
		Size: 291.3 KB (291309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b7e6ac913cf5db56d036aaf335904f49acbba9f9a6464379470983dced635`  
		Last Modified: Wed, 04 Feb 2026 17:03:51 GMT  
		Size: 59.1 MB (59076165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c9ffbf34a1bad5d46207189d74bbcd58a3144dd619f1478d1b987e4a42b9b`  
		Last Modified: Wed, 04 Feb 2026 17:04:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51118e2c3c37af036b4e725723e4b347f5f866fcd6c4356bea896864a024b79`  
		Last Modified: Wed, 04 Feb 2026 17:07:32 GMT  
		Size: 5.8 MB (5794360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb82db54fe3a2a182ed90dca31e44a7c21f11b89b9531e3bf731b80c4f5710e`  
		Last Modified: Wed, 04 Feb 2026 17:07:32 GMT  
		Size: 1.7 MB (1738757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce0011de05e6d67e61cb92e8d1d19c03b4cfb5d34fc2c3193e67ade71a61c17`  
		Last Modified: Wed, 04 Feb 2026 17:07:32 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3550d9fbd7081506f0ff7137ebfc2192340e9347e39ba6554c17e700c45b755a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ec393a8d407fa0a60413ab43208c27ab4bc6bf91a064793ae836c98715b442`

```dockerfile
```

-	Layers:
	-	`sha256:2fd753e8050aff76c24c7e520fea8484280cd6ab57c3c6efed2a38a15765953e`  
		Last Modified: Wed, 04 Feb 2026 17:07:32 GMT  
		Size: 283.6 KB (283646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480cdccfe97803e7df12b7c8a9748e8cdff317f08161600b8393b95c55cbc5ed`  
		Last Modified: Wed, 04 Feb 2026 17:07:31 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:677136abad8cac225542ed1824e41af477a83f530419e45432e9f596ed8e3772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70266754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fd3b157e927e08b59b4550649420cd6d5432141aca6fdc4b74da896b9d20e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:20 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:20 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:20 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:20 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:22 GMT
WORKDIR /go
# Wed, 04 Feb 2026 17:07:20 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 17:07:21 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:07:21 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:07:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:07:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 17:07:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 17:07:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 17:07:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c208805949d8be5100f2ce83de14acca26c494a469a23b86da08398c037b4a9`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 294.1 KB (294108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fac6022b2ee873ba16b3704e4dc9dfb3d60a32c4c3577bd7c9d971bdb2f1f7`  
		Last Modified: Wed, 04 Feb 2026 17:04:17 GMT  
		Size: 57.7 MB (57653449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98482da0983c1b21bd15286a0cb373f69e581712613d1caedffbad698f3da84`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14499d9facd51e02d54f6046a71b5b11256e80b0a213a8f768f126b2b715272`  
		Last Modified: Wed, 04 Feb 2026 17:07:29 GMT  
		Size: 6.5 MB (6462703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e50d06678e001e431511de35d9172a642025919a881eb072729007b72707816`  
		Last Modified: Wed, 04 Feb 2026 17:07:29 GMT  
		Size: 1.7 MB (1716383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d29094f4ddcbdd0af5836108ea621743283a27b5cf3deff596d0e7fb42afac`  
		Last Modified: Wed, 04 Feb 2026 17:07:29 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:174f72671fa7ab487474d61756d6026b589f425f414c7901dbeab739e6af9e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 KB (301002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b948399b866a7cd2083b22207e0abe40307f7a5d6df0dad3ab6271094219b714`

```dockerfile
```

-	Layers:
	-	`sha256:daa771c8d9996ce9039643955026e4f5a90a63447ee69394fe6677ed3d5008ab`  
		Last Modified: Wed, 04 Feb 2026 17:07:29 GMT  
		Size: 280.7 KB (280706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3d28ad09b4e7e76e8ffc214742925439ed573b1e42bb30a08d38ebd184a65d`  
		Last Modified: Wed, 04 Feb 2026 17:07:29 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:244923b9035f945c55f8ad514184caa4104a8eca232a9450e2cab767328d6d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70626449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265f41c77076e6a4a1306a582291e24ed4ca94c2276b9f2077d72ab58acee396`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:06:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:05:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:05:37 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:07:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:07:11 GMT
WORKDIR /go
# Wed, 04 Feb 2026 18:02:33 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 18:02:34 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 18:02:34 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 18:02:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 18:02:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 18:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 18:02:34 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 18:02:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5da64929a546b25e151c7b89cac4fd99dc41033a2fc1973779548ea5121f99`  
		Last Modified: Wed, 28 Jan 2026 04:07:07 GMT  
		Size: 294.6 KB (294573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69879181021786809c25fc5c953b51116d19e9c3c6d50663a1bdc3a339c1bd`  
		Last Modified: Wed, 04 Feb 2026 17:06:35 GMT  
		Size: 58.1 MB (58136923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3fb7bfe8ce423a42591835c480dfe13c38785ef3f012607a8521215b50caec`  
		Last Modified: Wed, 04 Feb 2026 17:07:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09ece7b5587a78734af3f8c1263f12cffe015a0647fb37937c6f66363f90272`  
		Last Modified: Wed, 04 Feb 2026 18:02:50 GMT  
		Size: 6.8 MB (6754070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ddbd0b701deff17b5356ae373f1ce57e28b5d3a23d8bfe296c36e803f3b17d`  
		Last Modified: Wed, 04 Feb 2026 18:02:50 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8806dc547407529cc8a624b9ce7c5fb0413dbe541cae7fc637edf81b0b7ff65f`  
		Last Modified: Wed, 04 Feb 2026 18:02:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9b66164f25fcd351f37d3df96a3bef31b1ec7ae2f1422244b97b8f98cc82ab9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 KB (298922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2775970860f65ccc8a101e9705a89f80b4b53e8c555c2c7a12bd83fbd14a4b0`

```dockerfile
```

-	Layers:
	-	`sha256:31d456d697c94e8f6f9bbe9c7faf5e488ff3ff24e207e43dabcd0fb2559f4720`  
		Last Modified: Wed, 04 Feb 2026 18:02:50 GMT  
		Size: 278.7 KB (278723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7997eda9352441b8ed61a09e5f646677045e5bf7805c763c6fbf95d9d5d7c2`  
		Last Modified: Wed, 04 Feb 2026 18:02:50 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:19acbf54c910a9b0780b31bf35a76244ddb20265775dfedbec7226a4df3a9fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70776198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1b8e6349b4a3b1ee2e70a5614098935b7b1fafd945fdb890711c987923628e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOLANG_VERSION=1.25.7
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOPATH=/go
# Fri, 06 Feb 2026 12:03:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 12:03:30 GMT
COPY /target/ / # buildkit
# Fri, 06 Feb 2026 12:08:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Feb 2026 12:08:26 GMT
WORKDIR /go
# Sun, 08 Feb 2026 02:36:43 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Sun, 08 Feb 2026 02:36:45 GMT
ENV XCADDY_VERSION=v0.4.5
# Sun, 08 Feb 2026 02:36:45 GMT
ENV CADDY_VERSION=v2.10.2
# Sun, 08 Feb 2026 02:36:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sun, 08 Feb 2026 02:36:45 GMT
ENV XCADDY_SETCAP=1
# Sun, 08 Feb 2026 02:36:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sun, 08 Feb 2026 02:36:45 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sun, 08 Feb 2026 02:36:45 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc7a4defc6ed5152e9b8491720ca46efa70b0fed648253c440f39924818c17b`  
		Last Modified: Fri, 06 Feb 2026 12:06:30 GMT  
		Size: 58.7 MB (58674209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eff26a637849aa66474c90e3bb3ca6ac1fc5c70942edde3257104b65c6c108`  
		Last Modified: Fri, 06 Feb 2026 12:09:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf5efa62f5531061581e760d809db703a6fcbe0ddebddb4871ae552e55e301a`  
		Last Modified: Sun, 08 Feb 2026 02:37:57 GMT  
		Size: 6.6 MB (6568269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee466545f7068bf1f25cc55ae09003f4fc65b0be1ce483340948fbf65e40b9b`  
		Last Modified: Sun, 08 Feb 2026 02:37:57 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311527fe9427748f97ae246d4bd2aad00360d863419a12aaed1afdd5c3edf812`  
		Last Modified: Sun, 08 Feb 2026 02:37:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8d6fb29c2e36908f9b28875d2e49ee057b286bd958aca3b3d344a3ff01657967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 KB (298918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c70d0951a8e0fe42c6b2448b18e5002aee2a034f109c25358bb8de2a9ca461`

```dockerfile
```

-	Layers:
	-	`sha256:52ad1b688ca8265abf793e77fe0112942ab721694aea38ee0a2984f57798b44a`  
		Last Modified: Sun, 08 Feb 2026 02:37:56 GMT  
		Size: 278.7 KB (278719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f762e3ea511a9faa3ede097a853af437406086a29072fd7837b747c1f61e7cbc`  
		Last Modified: Sun, 08 Feb 2026 02:37:56 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:857aa089bfc64b07ed8c33d4d3e1f02d78301123312efcfa76a21087b25eafa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71932960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52166d9868cec952cb62f44781b18428ffde3cdfb3dcec67a8910249c9a8f85`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:08:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:03 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:15 GMT
WORKDIR /go
# Wed, 04 Feb 2026 17:13:33 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 04 Feb 2026 17:13:34 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:13:34 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:13:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:13:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 04 Feb 2026 17:13:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 04 Feb 2026 17:13:34 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 04 Feb 2026 17:13:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9921a09dd19809d1ad973a4576f2b5d971cff57a487d0b65af5145a04bdf06`  
		Last Modified: Wed, 28 Jan 2026 03:09:00 GMT  
		Size: 292.1 KB (292141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8f0a3fdc9e8378ae51ec0652c2aa7b3fe566439364495bae28720620458ab`  
		Last Modified: Wed, 04 Feb 2026 17:04:51 GMT  
		Size: 59.5 MB (59494139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497856e95a7557d1147dd8b153e178e34055ee468bd2510725af95945a1319e`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179f0393e218e62bc78313856e962c348257cd45ac623997b4dd9d81945e00e0`  
		Last Modified: Wed, 04 Feb 2026 17:13:47 GMT  
		Size: 6.7 MB (6712813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eadd6ba9890c2a1112dbf048d33f6e07409fdac0bb7c71bbe7396cca339864`  
		Last Modified: Wed, 04 Feb 2026 17:13:46 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac5b73dbf6532bb75f528c69b076a9a08aeb5c37930da4329fd65fb83a9533`  
		Last Modified: Wed, 04 Feb 2026 17:13:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0c71eb3478b41ce728c2acfc726b1a1afea743b1a7b1819def18b3159117ed36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edef5607c7e2c6ed9e23a0c5625455bc3b05c9dfe4a01ce19a3c3f8388b828d`

```dockerfile
```

-	Layers:
	-	`sha256:08df42b7f5c363937e522afb7c534d45414ee267112aa87dbc346c29557c9fdf`  
		Last Modified: Wed, 04 Feb 2026 17:13:46 GMT  
		Size: 278.7 KB (278651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620a9813d690e39657a381998e40bad270aba203e5808318c64b3a311e75d412`  
		Last Modified: Wed, 04 Feb 2026 17:13:46 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json
