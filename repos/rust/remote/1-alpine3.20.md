## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:a46751942490d71329159dfa88c88fe47d5f7da0fc8b24b7c062b882ddf3190d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:dc12c979f3ce500d3e2395af78b4563349fc78f9930668a341e6693d359985e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329541442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26aa7016238ee9dcbf9241521b6c47acb920a9d12c26e1e893eeccdbcefdac5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:02 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:56:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4084b864c5741a063c95dde56466e13b666cd6b16c95b3b2f7eb1fcce98da6bf`  
		Last Modified: Thu, 05 Mar 2026 19:56:58 GMT  
		Size: 58.8 MB (58781765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11047165f927ec2e7a83c25d6dd129c883c6893b3b204f34d6e26226061ce6d8`  
		Last Modified: Thu, 05 Mar 2026 19:57:01 GMT  
		Size: 267.1 MB (267131813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b092541c4521f405d2b9171bada527d2d5888cf69aefae4c80540302488e9acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f520dab443221366b6c2dd79414b5a9afab8d81e19398fc09b0f955eb751c1`

```dockerfile
```

-	Layers:
	-	`sha256:123097cd5b138999ef1e4978ce13f81d8725f16773f0323a77db081ee4537573`  
		Last Modified: Thu, 05 Mar 2026 19:56:55 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:405155e9f45cfc21cfd90dc0e06f87777b1854678c84a455328d8ef009ef472e`  
		Last Modified: Thu, 05 Mar 2026 19:56:55 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28e66de3ba2c6ef674d0500a691cc7e45ff920b27c76f23f0d7630d5d569e448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332756514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc0f2519f8561fe367c9f270a55d51a8730860fab54fe848be56e37ff94059f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:04 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:56:20 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1026c98fee3ed1ed9e600a8225ee76f7ca184e5d4d594c34c1ad9555b4e30407`  
		Last Modified: Thu, 05 Mar 2026 19:56:57 GMT  
		Size: 55.6 MB (55558382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fcd310fd50b3e4525ce454a738b520f4df1b4db9f7fbed3cb8107ad08cac4e`  
		Last Modified: Thu, 05 Mar 2026 19:57:00 GMT  
		Size: 273.1 MB (273108174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6f4d2fcde6437c0455e89c58f1af63d3dbbd61c5c130e81a3ea87c9204c5f3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd28703966e2a4466b18eadd62798836ce15b2137a8c8a52a63e45597da7cbfe`

```dockerfile
```

-	Layers:
	-	`sha256:e78072eb7ccfcf5a5d158870ae412e8e76d90af40fcedf2c7287b17fb3414523`  
		Last Modified: Thu, 05 Mar 2026 19:56:54 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe46f07d9847336b0a21d4c84413b01c378cd9cf2b9d1e924c8b34318c1ee61`  
		Last Modified: Thu, 05 Mar 2026 19:56:54 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:025e1d35ea018ace63fdeca133da20899f620b3b3db8ed1973b11e21f154acf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352491419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be373976bc5a525b2b421d8eb7255427baef6cda3274a73065f66ba0c9e7fdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:26 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:56:53 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33f18efd80ab9e3f3226192e424a82888219c8b6ae0d2a2e71437b45ef8dd6`  
		Last Modified: Thu, 05 Mar 2026 19:58:22 GMT  
		Size: 56.6 MB (56619708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa815b3e6545484d0f4d7507e6a6fba1e0d1332e940387e4d2ac56adaabbdbc3`  
		Last Modified: Thu, 05 Mar 2026 19:58:26 GMT  
		Size: 292.3 MB (292294201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:a61b98328d44cc28cfdc005a41c9e547a6bec4f5595841ef8efd434eb6a6c4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772a39d83399473612457513a8eb9ccb590b5569c2e1ef76a8433c0e841c8d24`

```dockerfile
```

-	Layers:
	-	`sha256:97b42ac6bd95926081dd2a1e4b8b98eee8075bb0587b00732d6907e0463a5ec4`  
		Last Modified: Thu, 05 Mar 2026 19:58:19 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cebb64303501b97c4b559aa846978299bcfb0576dc3927bee5e5c4bcefa7ea`  
		Last Modified: Thu, 05 Mar 2026 19:58:19 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
