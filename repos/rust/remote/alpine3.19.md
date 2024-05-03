## `rust:alpine3.19`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
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
