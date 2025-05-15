## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:e81c5ddc78568bdd33d73c427948f0083102ae6633266c244ac41abd0e8ed28d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Thu, 15 May 2025 18:37:42 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Thu, 15 May 2025 18:37:48 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

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
		Last Modified: Thu, 15 May 2025 18:37:41 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7549dd113e878f8d612b8ddd89c0c5036e2e3832fce79290d8419a2ecd438b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313499849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2889844f7970951c15a7dfce1ea34469790c6171d1f92f90d2ba989d122c317`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 15:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 05 May 2025 15:33:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 05 May 2025 15:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Mon, 05 May 2025 15:33:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Mon, 05 May 2025 22:58:37 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de54c26c85593c332923d16cb98665baa07ea43f092ae57ab6d0a834d239df`  
		Last Modified: Mon, 05 May 2025 22:58:42 GMT  
		Size: 256.5 MB (256458407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:9e254ab669ac5b9c61b9dfd61aa33180bf364cc94ced19f6b41885c99ca060bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5860d27b36fe60c6fba00f5c5ea78e664ee7ddfce231ca7c18dcbb7e99059`

```dockerfile
```

-	Layers:
	-	`sha256:b48163a41e4b9c4a52befcd4b5f90b4790d768b55e8c7838b08213df40986642`  
		Last Modified: Mon, 05 May 2025 22:58:36 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef75e0516c318edacbacdcb3d77a3d09c2ba0965d2a8d6b4ca24939eeb83b5c`  
		Last Modified: Mon, 05 May 2025 22:58:35 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
