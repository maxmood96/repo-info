## `rust:alpine3.20`

```console
$ docker pull rust@sha256:5ac4a15484719c0a004f8dd6b6a6a4a12751b1a67f92eeb4d100e39fa6df842f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:723d09dce89b5802d549b020617cc6d7accd476b18ef04f7f0e917b851281ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329778390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115932f6f8102792caf337ffc6c2a2d6504b2a945f2217d380dd497240fc351`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:52:11 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:52:11 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 21:52:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:52:29 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542f36dec3d2838bafb7d816406aec0c694bf954ae8b830cde620027e32ec4`  
		Last Modified: Thu, 12 Feb 2026 21:53:06 GMT  
		Size: 58.8 MB (58781883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a025e16aa4d0f7fa9e75edefaa102477c447c76ece74223361b80202572eb14`  
		Last Modified: Thu, 12 Feb 2026 21:53:09 GMT  
		Size: 267.4 MB (267368643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1950d547647207cd8154882d38aa828a12a6e8414c120b463999e786a2c378c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a229883269a117ef94b56e36a2bad7a741b8bfba02a228b83620e4f390158a`

```dockerfile
```

-	Layers:
	-	`sha256:411af86d3d93f56bd1b38b7b31d5ac00be5f7f7493721014a7bb36e9aea15293`  
		Last Modified: Thu, 12 Feb 2026 21:53:04 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd730ac812d478695dea029a8f3a1d055ad973282a64e32ecec55db420b9f8e8`  
		Last Modified: Thu, 12 Feb 2026 21:53:03 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:376328d1c19748d419ea0f0b8eae8e499cc8dab32fc2dd5ef834bc66c1900fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333458923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25984ff661d7152c0dca1e9abad32fdb29a25027ea6348cabb6701574035dca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:50:43 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:50:43 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 21:50:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:50:58 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad687e77d4b045653e98048660a7d45fd68875968a25cdf60bbba1663837ac`  
		Last Modified: Thu, 12 Feb 2026 21:51:35 GMT  
		Size: 55.6 MB (55558427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4c820fc69873ee920394f9f8713b51b06d5f7961ca17bcc00a013badffb196`  
		Last Modified: Thu, 12 Feb 2026 21:51:40 GMT  
		Size: 273.8 MB (273810538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:60fba11584faadb05fffe5c4e0b8c56acb52c0afa0babf03405dff464c735074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8069eafa5133a85a9bf0714f8e9697e475f12c00c16cbdf3eb68b9f75af52`

```dockerfile
```

-	Layers:
	-	`sha256:ef9db21196598dc559096a0b25d8811fbc3cd22c0c542825cd93b23d76e95c4a`  
		Last Modified: Thu, 12 Feb 2026 21:51:32 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2cbde15589cd72058822ad834e44de31ae18d4ecc9b6f92014c286769949ea`  
		Last Modified: Thu, 12 Feb 2026 21:51:33 GMT  
		Size: 12.3 KB (12304 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:451e9b68ef6a399565ea3825f5170d05613368ab0e9b30b65f06bb5710c090ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733adbe26d3c4d8da25250629140b474e2cfb25cb72f24c57de751ae589b33b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 22:01:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 22:01:52 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Feb 2026 22:01:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 22:02:39 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d019af52e42916bbc9f1cc6952d130a0991b94e27de18f99508824526bdc2051`  
		Last Modified: Thu, 12 Feb 2026 22:04:13 GMT  
		Size: 56.6 MB (56619684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7872eafd53f17c7999b6281926fe2a8cfd47208d75886b44cd182951cf6e644`  
		Last Modified: Thu, 12 Feb 2026 22:04:18 GMT  
		Size: 292.4 MB (292357580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:3cb313d0e83baf91412534b515f5d9838a14235b3c284387989d5178192365b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8155fb06b203d57020f01489347a5ba6c057ba24506ee06d7b86afed6a29a154`

```dockerfile
```

-	Layers:
	-	`sha256:eecd3ed00bda7f0dcb917e9757a47a4e96b36a943b19c5bc65870d2bdfcd4f6e`  
		Last Modified: Thu, 12 Feb 2026 22:04:11 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d26dc712bdc6dd5db862d04e85ef72b0c1c0a0e5edc7bc1babca80f7d808102`  
		Last Modified: Thu, 12 Feb 2026 22:04:11 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
