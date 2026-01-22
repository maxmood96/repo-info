## `rust:1-alpine`

```console
$ docker pull rust@sha256:d776c22db3cf28689f145615e7deab6ee7496cfc7d6cdefde3fc050d05e4a4dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:959b2a7043a93389a01169c094e356e1a3ac75723e894b1e896db988c2786b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346351175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea791e681c18263f2930e8a41f9d0d52a6d3eb6fa40bfbd446211fa715ca4ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:02:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:02:01 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:02:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:02:19 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddaf2de686a967c71e2183a61479ec97783a3cfafc6833766327a5471274a50`  
		Last Modified: Thu, 22 Jan 2026 19:02:56 GMT  
		Size: 75.1 MB (75119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5281218459a78f9d3d3e884bcec474e3de643f113753e97e97d3d68f9c0abb`  
		Last Modified: Thu, 22 Jan 2026 19:03:01 GMT  
		Size: 267.4 MB (267371982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8e27f4a5f639c0885ff6a63acd6f45cfa619e8ef58fa3a8d0d0655c693200fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1021805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5443a2818cd4030921ed6aa22b6e35eacaf341c69abc09057db86a915273e66`

```dockerfile
```

-	Layers:
	-	`sha256:87ec4cc4c6063899aaba315b49ede23428121fe90db0bccb436902439670ffb5`  
		Last Modified: Thu, 22 Jan 2026 19:02:53 GMT  
		Size: 1.0 MB (1008415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc7c8480497b0a6d8a207d48e861494f7c8442a9e1aae2d1720899b2d6f9793`  
		Last Modified: Thu, 22 Jan 2026 19:02:53 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c53cb8692019abd84f11e7875210087a8a06463a7b1bb981ef86928a80f890cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344535125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87401aa80834d1bd8c5630ab71cb8a075e5ae06cc29b35bf564a683b2dfb1037`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:07:03 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:07:03 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:07:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:07:19 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c418724e4e03660fd1fa22cc61a55b16ad2f7dfb9ae122e9fa975ae3ac889f`  
		Last Modified: Thu, 22 Jan 2026 19:07:55 GMT  
		Size: 66.5 MB (66542917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e2704f91d59f2f9ee3ac6f9f0bdf51ab5797fecc82528d65a2bf043b2866c7`  
		Last Modified: Thu, 22 Jan 2026 19:07:59 GMT  
		Size: 273.8 MB (273796469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d338ac916f9d8bf51497dfb3e267228d2f206bd6a55bf3831de630c1e8834b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1081031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f06cb66c7126ef7d27e496ea187698d4fdca36421e54ec3fdbe4daf4b0ff6b`

```dockerfile
```

-	Layers:
	-	`sha256:d58a4d709173c77efc90198b4e291f14817c7a73bdad44d8cecde310bb240ab5`  
		Last Modified: Thu, 22 Jan 2026 19:07:53 GMT  
		Size: 1.1 MB (1067474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2ae7baab70b28c87d336b85522e16afa3e9b9dad3f726fdace74b78fc572ec`  
		Last Modified: Thu, 22 Jan 2026 19:07:52 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:af593a0ba63e12e364f9fa534690026becc2fbbee9d26cb7bf4531a99109e07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362619845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828f35c15f711d557023a2b2a8a8c73f736616e0c86b2a39e50dfd7ff8fc526d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:42:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:42:06 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:42:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:42:40 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9708fc86e3513dd34d75f37defc99e917a10ce8f4bc14926a7484be6b28dcabd`  
		Last Modified: Thu, 22 Jan 2026 19:43:56 GMT  
		Size: 66.4 MB (66425989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc14d7dffff9e78da032f56de1993b195f1b7ab7f722d465df0059d69f383b`  
		Last Modified: Thu, 22 Jan 2026 19:44:00 GMT  
		Size: 292.4 MB (292366101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07a081bfd9dd51d8548cae93daeeeeaa58bafc31e095c22812c900e1c08d5941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf80fbd963f83dfe5cdd28e3e4d6cd0b28141b961047a9f6f3c7fb92284949`

```dockerfile
```

-	Layers:
	-	`sha256:480b13e2926db2396ee974c4ceebb39e85c6aa9502f829fe71f014428758858e`  
		Last Modified: Thu, 22 Jan 2026 19:43:53 GMT  
		Size: 1000.8 KB (1000761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30fa808f9c8fc1884982ff5f554f6f64db0a62e91b8c71ef427c42b4bc3067cf`  
		Last Modified: Thu, 22 Jan 2026 19:43:53 GMT  
		Size: 13.5 KB (13459 bytes)  
		MIME: application/vnd.in-toto+json
