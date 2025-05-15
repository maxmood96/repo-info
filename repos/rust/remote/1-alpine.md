## `rust:1-alpine`

```console
$ docker pull rust@sha256:4a222be5276ac329839d338935709f91be4d34e972c02389406c18f82155b0c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7f81e1ca5c870031b91135fe95a75437f8e6af2bb14b217d0c015953a682cb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319553705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324423ca17a744e2a5abf36b62747fb984f968abeff8107ed92e3c0909220df8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e565cca94b661582fa0c4f08b135ccee978ceff37f179c6816fd41e5be72ac89`  
		Last Modified: Mon, 05 May 2025 22:59:47 GMT  
		Size: 256.5 MB (256459313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:c66662b8c6924073aa9a7973d42e114e2818163799a10f4860ce4eceddc7c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7f4754a2b640d80bf0dd593e1ccd7b7596e391c4fe5256a231347ac66d49d3`

```dockerfile
```

-	Layers:
	-	`sha256:ede09653cd86444cfcccdb324f662a4915c51d95fce2dc2ebc66111eb9460246`  
		Last Modified: Mon, 05 May 2025 22:59:41 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533c8326acafcc08dbc22db49c386d4960b16673eb94f34f3f9a190840fb13c1`  
		Last Modified: Mon, 05 May 2025 22:59:41 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
