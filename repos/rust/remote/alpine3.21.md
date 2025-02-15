## `rust:alpine3.21`

```console
$ docker pull rust@sha256:fdff417c3845c92360b439382f7d6dabca6c998f59c8dce6cd2a16a2e9e85498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:74f39e6bfe58a1b610fdc5e6fa67468bc73140469f2090411d2f242d2c9ff407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304582444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458995c03409bbcd98aad3f8d98905aad5e3ed17a8af75404444bf1c40a44b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08914ee27aac92b9d51d0c254e4096fa3710954855f469d9c033328b88aa4`  
		Last Modified: Fri, 14 Feb 2025 21:46:04 GMT  
		Size: 61.6 MB (61564943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577f91cc0333a6bf9ba25ba636393eac92318cad2029d3f7ea1956977483e153`  
		Last Modified: Fri, 14 Feb 2025 21:46:13 GMT  
		Size: 239.4 MB (239375254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e2b417ba07db56ecfd570ba4ba06415b6bcb9c6223bdc248c256292641022c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936b868032fad12549752a349a5ead0978114cd00a432ccc00b3096a11c03d3f`

```dockerfile
```

-	Layers:
	-	`sha256:f6c7849321e26ea20adf4e93b140974a1c9bc65a302ddba1829fde840c5a1cf1`  
		Last Modified: Fri, 14 Feb 2025 21:44:20 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab9bfd3f0d1a3397928e694479a8d3acb066f8cb0d7bf72a8f60f07277b9b10`  
		Last Modified: Fri, 14 Feb 2025 21:44:20 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:88837029dd140a2539340dbae91d3c8e5002d9b5a01b19a1b4a38688d80f2763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307002123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abe4f794562caf363777a6969a35b7770c7310824cd64f5b3ea82304d10e831`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7995ad51d7f8137de2d089a046c47c22b794e249fc189513b6f32c0d853c292`  
		Last Modified: Sat, 15 Feb 2025 09:53:25 GMT  
		Size: 59.1 MB (59101131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f8b6ab05e117423717c6cd16be2f50852594b915b57f20caf75c2b098105d2`  
		Last Modified: Sat, 15 Feb 2025 09:53:44 GMT  
		Size: 243.9 MB (243907963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:2f1b15b56b9c5adce6d276fb10dbc6741e1a66912cb8ba4d859f9ba50051fcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581aa1dab8a12370fbfd7dbb1000c24a339c709bf3eb3233f6e3bf038d61d423`

```dockerfile
```

-	Layers:
	-	`sha256:1ac3583d4112c1f11888136e9c8937563e3db64409eaf5658d1529cddbe99ce7`  
		Last Modified: Sat, 15 Feb 2025 09:44:18 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f3d3a22a27927cfa842f81383799b8be39e39c7c52b5992188777c00ef4020`  
		Last Modified: Sat, 15 Feb 2025 09:44:18 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
