## `rust:alpine3.20`

```console
$ docker pull rust@sha256:5b65959f00c8fcc9bfabb76644c4eefa0b97f8af37040dd163592536dbd6e107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:90846f2d591b7df8b6a24acf0b3b49b7c6505703190371f40d2f442498d2aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298316995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfb378cd0fe965ee75d63fe3291757ea7876f5f7a4663e818d135f8ff2fbdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77927bf1e96f21719646e6bae28029a1ae3f345fbe3909a6339189205890e1a`  
		Last Modified: Fri, 31 Jan 2025 00:27:17 GMT  
		Size: 55.3 MB (55315542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f429e09b0fa861e6542ecd21fefac35a3c2b405055fd9b74e31db3677f9db3`  
		Last Modified: Fri, 31 Jan 2025 00:27:20 GMT  
		Size: 239.4 MB (239375193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:03c2f4be77e68d8908fa4675b8cd24b056465943604991e23d40ae0961f1eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b5a1a42abcdcd793be2182d1682cd4e866f179bcebde2d0ddff81565cd141`

```dockerfile
```

-	Layers:
	-	`sha256:453fda6d733a61c5795fb7921bfbc21174ce9d1a30bfd83612d6e2e341b4028d`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571392ac9483c44b5395d2f6c12baae68eb19d840a081880a6c4f3194dc317ee`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:59d7abf2b2cdc63cd4917924cb23135299f18b1aa5152baddab0fc0db9d851b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300949670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6582639290a8a26ebbe011b767cf366d257472d3b950df2bbeb6c91b2cd3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f023fbab63b00375fb771d16cd745c9a1ff513cda460f1e701e3b66e9ff86d`  
		Last Modified: Fri, 31 Jan 2025 00:36:11 GMT  
		Size: 53.0 MB (52951018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f22d4c62442d75cfd04ad26c9c5455e25bebf3384ec4e5be257e364d6aeb4`  
		Last Modified: Fri, 31 Jan 2025 00:36:15 GMT  
		Size: 243.9 MB (243907883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c87b653694e961dff4fcbd925991fb2db9f8afbf3a05ace8351287adc3e8f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea31be4c87b9f661044c3b4d19d40df023745400966e4e2ddbebd135a3f62b`

```dockerfile
```

-	Layers:
	-	`sha256:2371f11175124cfba85292d79ffac38eea16a98d653da2f12fc5e9ba206099e4`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10caafcae281ac20e919dcc1e71c9cb267ab5d223ab59cffe4fcf159262c0fa5`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json
