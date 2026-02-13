## `rust:alpine`

```console
$ docker pull rust@sha256:4fec02de605563c297c78a31064c8335bc004fa2b0bf406b1b99441da64e2d2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:2249050332b405613b17fa96bef438b9b92569d76b3e1f64cbb7fb603abb713d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346349610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66a01b01df697a7f5802462d8558408a0aa6c81eb3eb9f8860b95a969979527`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:52:14 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:52:14 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 21:52:14 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:52:33 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cf86143deda979ce07685c3f8e323ad60dbc3149f98cf950163fa103599da3`  
		Last Modified: Thu, 12 Feb 2026 21:53:11 GMT  
		Size: 75.1 MB (75119134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379a1168b9c0d28ee381476b804af38bb2782c614c564e80833dcd9b5d46e214`  
		Last Modified: Thu, 12 Feb 2026 21:53:15 GMT  
		Size: 267.4 MB (267368655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:a95275d549cdae6966c3aa9f6f6dbd39141f5b8179ac78466e99eeda15ea1dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1021805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ad1879177634014d9e341b67ecee0e370551a055c62a50f95fcaffbf3b20a`

```dockerfile
```

-	Layers:
	-	`sha256:6f0cc844df9d2b8fc94cf6aeb0ab45833f465ad08f211b6af36ee139db40ba62`  
		Last Modified: Thu, 12 Feb 2026 21:53:09 GMT  
		Size: 1.0 MB (1008415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d671ef000884f5c41c3eb9cf00b897413a7f057da56299804b76dbe0b38ac7`  
		Last Modified: Thu, 12 Feb 2026 21:53:08 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:df077ff90e524c878cb6d0fec884856af9ebda7512988db2f4211b8ed8131107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344551303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c55fd8327d8b0df0a0dc4fee8b59a60ae90f148cc3cc1fe193eeb7cdb6f57da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:51:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:51:42 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 21:51:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:51:58 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d0f492e3eee564f632ad61dbefc39701b58d50970b70c76a1f964ff2b94373`  
		Last Modified: Thu, 12 Feb 2026 21:52:34 GMT  
		Size: 66.5 MB (66542825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e223fe76695f60d5514738da4216ecdab8939f08eb69777a9d3a4a70555dbbc`  
		Last Modified: Thu, 12 Feb 2026 21:52:38 GMT  
		Size: 273.8 MB (273811387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:56186c445649cad2f64bdf51900bb4bed6a99de061a7d4d31ff42e6f71dc1046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1081031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74568f84fb31b397cc229c941c3af532685421f75c911b3bfcdf3e21e49607f6`

```dockerfile
```

-	Layers:
	-	`sha256:6fa3ef39a4b602afd17293ae17a3c9b9e35287f1b37209549c170dee187a6157`  
		Last Modified: Thu, 12 Feb 2026 21:52:31 GMT  
		Size: 1.1 MB (1067474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b33c2fa7bd7bf42576b307173f699d0af94b7c44754aae95d7b0aa2b707b57f`  
		Last Modified: Thu, 12 Feb 2026 21:52:31 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:e77da576b29b573a20657be34720dd26796849a03c520892f5a5a46536f182ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362612523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a993f6418fa0232b59eda50e1579f60821ad8408c6ca4c58bde9388cf0466ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 22:05:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 22:05:56 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 22:05:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 22:06:29 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cedb1f5c0f661bbc0a0b9ea8b2b6844cd4bb75ecb5909a8e566ae056e17424`  
		Last Modified: Thu, 12 Feb 2026 22:07:53 GMT  
		Size: 66.4 MB (66425976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0a612e40633d83cfca871576921c574f567796a4d3fbb634aafebb7c536f63`  
		Last Modified: Thu, 12 Feb 2026 22:07:57 GMT  
		Size: 292.4 MB (292356904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d78475275135a0216f17fd436a62065330b732da211eac7da86363d8fcb8ea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ffc6180c903d1da67b14be888bb5ce270da5826951851d9d478cc23458f816`

```dockerfile
```

-	Layers:
	-	`sha256:583179d4aaa7b3ec89665099e6e311e827f1a98c0e82b2ab63c661a1cb552b0d`  
		Last Modified: Thu, 12 Feb 2026 22:07:50 GMT  
		Size: 1000.8 KB (1000761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e69ab19e7c0b658ebdb5fea444cdea7c308ef8af1f71faa67075bbefc1c76f8`  
		Last Modified: Thu, 12 Feb 2026 22:07:50 GMT  
		Size: 13.5 KB (13459 bytes)  
		MIME: application/vnd.in-toto+json
