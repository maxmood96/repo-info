## `rust:1-alpine3.22`

```console
$ docker pull rust@sha256:fa16d058a94f0f1cf86cbbbd181a2ea2a0001e1fba1e93c366821a58f3e6c8a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:8b5aee3b8fb41756d8447a47f96edc87a21f1e0c2b5ad2f3059542637d6c9b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339354577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47642e1259584d131aa2fb81b4d0090a7332f7ac4b564af0a41b53d0f5d3da10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:43:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:43:04 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:43:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:43:23 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5f57d73b85dc79de4c10db12a401a0405464fbdd4f54354d987ae7a14a5de3`  
		Last Modified: Tue, 30 Jun 2026 23:44:03 GMT  
		Size: 65.0 MB (65037685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d5d4de8d61f8e743150c006aa23ef8518f63409f4948bd35b7c4314c07711b`  
		Last Modified: Tue, 30 Jun 2026 23:44:07 GMT  
		Size: 270.5 MB (270529297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:72c978925b3eba9fa7f8674613b056c5e52d61f8b3580642e66dd118b5275cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **956.9 KB (956923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e54c1e0e2c4eab0aa1b0eabbd423b938c3554a739f39fde750ce4f9cc071262`

```dockerfile
```

-	Layers:
	-	`sha256:9f0d26f2f1990fb5bbad5b904606ee9fc8b1e9fa9ef5d9c634ebd41b93238d04`  
		Last Modified: Tue, 30 Jun 2026 23:43:59 GMT  
		Size: 944.7 KB (944737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19da99927c8bea0963db258cf34823166e50ed3f9e7a53e8df8c5a446d8bc78e`  
		Last Modified: Tue, 30 Jun 2026 23:43:59 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:48a6b2b25ee4940672e3d178c73a07ddd7de54358a52ad5ddf4ffbec390f888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340221057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abd980fee62a21f48e66f5a2d39b7294bd1a804ee7cfb2c8a4752a2c51f11fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:12 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:41:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:41:26 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610525cb754ed0590f9fff1f1c31bc9d8f2ff94be998ac3707995ee78fd9db07`  
		Last Modified: Tue, 30 Jun 2026 23:42:03 GMT  
		Size: 61.7 MB (61713175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c41552b3cad42b6b596ebee759906ccc6883134d705c89d5447e8f92374f33`  
		Last Modified: Tue, 30 Jun 2026 23:42:08 GMT  
		Size: 274.4 MB (274387396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:c8f66933cfc326aee2ced414b3eff55939ac22a52a6a928a99fa7584570b0fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7e81494908e8c40e6a3ce6efed7f75d3b739dd70d8cf2cef4e9b13ebe379cb`

```dockerfile
```

-	Layers:
	-	`sha256:8d8a934c817525542e80c35abcb8a37b8fa60fcc70511b660b94e886c9b93067`  
		Last Modified: Tue, 30 Jun 2026 23:42:01 GMT  
		Size: 1.0 MB (1024063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac098e5dfe502a289eaef6753a39e9673212367f0bef6d498eaab540757c08d3`  
		Last Modified: Tue, 30 Jun 2026 23:42:00 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:c9d52959b798b3882b9c097ccf510fda5ad6cb6c3c6c230032026d4948ea038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358674151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337c090769a98238dde3e7e2a9e40ba96dd5b8f9bc00100a4e31c4399118eca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:47:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:47:04 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:47:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:47:25 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f4e8a2d47b12c8068b87265b2bea3fbeb0e94e1364ff1ec1fed936b57ae3d8`  
		Last Modified: Tue, 30 Jun 2026 23:48:35 GMT  
		Size: 61.5 MB (61518385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34db11dec3ca468dbc6ce74a694ab98a9984bf4ac5957429795bdf225942cb5`  
		Last Modified: Tue, 30 Jun 2026 23:48:39 GMT  
		Size: 293.4 MB (293436534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ac02b9fa594ed9f7034410979403f7643736ffd774038a4c6ab67be18089abb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **969.5 KB (969511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b25d1a13d5a2d1a3f04b79e2b6ab3e22646dcdd9c0980f10e93ef1d54166471`

```dockerfile
```

-	Layers:
	-	`sha256:27070b5c5d419d859588c8580c6c63ab07d51a81fedba59732f61d5be80f5de6`  
		Last Modified: Tue, 30 Jun 2026 23:48:33 GMT  
		Size: 957.3 KB (957281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e62399bcf53b34cbdd767182cfc22d1cae418d6ba97c5fc27ad45138d5569c`  
		Last Modified: Tue, 30 Jun 2026 23:48:32 GMT  
		Size: 12.2 KB (12230 bytes)  
		MIME: application/vnd.in-toto+json
