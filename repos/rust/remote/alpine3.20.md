## `rust:alpine3.20`

```console
$ docker pull rust@sha256:126b44382fa926ce41eecac3ef4628de508f0df8556fe43e8d64cdcd1cbbe40b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a6e21abdf25464282e9ebe77b75a597cbd0b21d375eafa86c38af1e1cb8a2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (317984256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198b701be7dc50b960f31ef7f4fd2764b266e2d8adaa0bab88ab59ce2b2bf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Fri, 16 May 2025 14:17:43 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Fri, 16 May 2025 14:17:57 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:279079ce7141a696c62912e2b546d3b1db80da36385b8291b96bd87b06a333ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9514c3a9ca96fa531c453a6086450f8357d88a8602759b77fade775484d62`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4df00128cf574a18437ccce5e6d348c5ac96f9e656076475640bc336b72b8`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2881015e0b8d0d3e45e40cf26cedbea750dc4e4bae1f9492ea6ea20c3c478296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320946007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f9aeec89829426e53d9ec2993f49c4e8add3c62bbb31e1a8833ca8f6bba7b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Thu, 08 May 2025 23:40:24 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Fri, 16 May 2025 14:28:10 GMT  
		Size: 263.9 MB (263904565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b8cb278c3d3464f502ef0c4e303cc516cf61210f397481f3f916b0efd803552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465991995a77f18ceff0792501f873542ee79e340b0bc4e6a168e2d55cf0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:13318289bd5cbf3b293bd9e48b8d9dfb9679941c1b10fefc888f757d08695f98`  
		Last Modified: Thu, 15 May 2025 21:26:00 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Thu, 15 May 2025 21:25:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
