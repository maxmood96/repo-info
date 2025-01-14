## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:8b2e66b58b7b5a0181019e2ac12d6b4c2e550b2e6889ecfc2a12d10f4579894a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1a866b68d2adb80492e3e996f84999d692c20a34c3ca1a21d8bd2b448993a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298337931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7ee796e3d6fa94b33642d35bf166294523ccf3a26389f8228de309940821`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff15df1191be1ba73e0551f9604556c59601352359b9ddcd56df3db87838e3`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 55.3 MB (55315358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cfb1a53cd02005ecbbef1bf5c7908122591c89f17c20073a82364a982bddf`  
		Last Modified: Thu, 09 Jan 2025 22:29:55 GMT  
		Size: 239.4 MB (239396313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:609a9e76a5909373fe3ed8f7b522150f67e80681ceb707ea9a5677692d239a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46a007e2e5a282e2ab6fe96bec9e3e15b65a8a803bd9c29e506a009e90910d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c6a5a2ada3ef89e80c205bc878b8be8f529a5f096b1dc60fd7a94db1b6442c`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd25cef9e4659903109b2c2b5cef038ae26f5cad4d5ca689fc8b7aaf77ca5fd`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8d98865f36d4249e0faa69209325e70adc561ac43355de0a1469cbb04b12479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300990769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d1fb945f7649689a77349b66020e055e8362f207aa387c94cb30a12d615de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b4f23fe7caefa44f7fedf6c6ad6331c9647daa81ec320381013cb4987762a`  
		Last Modified: Thu, 09 Jan 2025 05:56:18 GMT  
		Size: 53.0 MB (52951004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f078a134c6d3bfbf3e51f6cf7d7215b3b9a168bfc794609656888a9123c68f5`  
		Last Modified: Thu, 09 Jan 2025 22:46:24 GMT  
		Size: 243.9 MB (243948996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8eb282a9a9f00e4c2eafa1071b34f2dae2b421ae503a972eb948197a6b0d89f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a939431982c0dbaf5b921fb551b6df6df396a5d3ad4341bdb440eb5c687fb9`

```dockerfile
```

-	Layers:
	-	`sha256:131c73a03f3ebbeb19acca7099852ab177e0165420ebbdfad542fa4fcae54f98`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083bff1fc4a6ac0159bd3b6bfb7e2529474fd78d774f9e70650e53a48ac7aaca`  
		Last Modified: Thu, 09 Jan 2025 22:46:18 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json
