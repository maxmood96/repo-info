## `rust:alpine3.19`

```console
$ docker pull rust@sha256:7ac923779671713f88771e5e7f90fb00232630a960729989f1ca6daa671f9ef3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cc0da3bb2c453ba8523a9d20494b9e61eba904e69129cc28fedf606d7bdb4e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277952834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa78d7b75547aed4cbce628b66ada2dbe0be904cefd1a7388ceee57816c1f8fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051d54c8ffcb73ea5822eefba0e68f4503dac253db0ad5ebc3afbc90c86a6326`  
		Last Modified: Thu, 13 Jun 2024 18:31:34 GMT  
		Size: 55.3 MB (55346828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8f4d42aa86065829814e507087c34991599af31a6ad88872753fa862714c8`  
		Last Modified: Thu, 13 Jun 2024 18:31:38 GMT  
		Size: 219.2 MB (219197277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:4434b017038690e9adf44afe2e841a30d1b8683853deefccce23756425622671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.9 KB (719890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f702152529c263af3c14a5f1b0c29815bb16c27158653f65c89b05e77105a2`

```dockerfile
```

-	Layers:
	-	`sha256:e555cf812627f6955ba5b60c80972a12cb27b18bcc23c20b885296822393736b`  
		Last Modified: Thu, 13 Jun 2024 18:31:33 GMT  
		Size: 709.4 KB (709416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e3e2d28a173f24e5ee97d8a2db2f2289232d269a12811c901dbce5042e4cf9`  
		Last Modified: Thu, 13 Jun 2024 18:31:32 GMT  
		Size: 10.5 KB (10474 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json
