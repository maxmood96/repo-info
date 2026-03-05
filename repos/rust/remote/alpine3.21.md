## `rust:alpine3.21`

```console
$ docker pull rust@sha256:40844f780f5f9b6b0ec9b82007284ca8b8dbc3ea6ac3b4a3dbc211245eb00f22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f95f3358924b025234501ce1a42a289a28a78d4759a0245c2e5bac65c7b5f508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335807888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dfde25709e16ac1661066c261b76915b472eb20919057f49e7a4fb11c9954a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:02 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:56:22 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b56a67de431dc394f15c17c0097a730740e02a1c1b67c2f5d3ec673c5fd3ed`  
		Last Modified: Thu, 05 Mar 2026 19:57:02 GMT  
		Size: 65.0 MB (65032061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c5a03740ad63da731d06f89da31c0f4591b9df0d4ca30e521e8bf70f705c77`  
		Last Modified: Thu, 05 Mar 2026 19:57:06 GMT  
		Size: 267.1 MB (267132085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:2d7037845c5edd96fd4469dc5111785c811c3c4a70a379dde8012ec156572391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.7 KB (973715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72150ffb91abf09182d7c32e75266cc0cf78ae9ef6c7e8bfcb0a61604cfcfdb2`

```dockerfile
```

-	Layers:
	-	`sha256:6e1a98866aa55d814ddb82de0162635ea8aca6f7a017852b3dc8cbefcb58ceef`  
		Last Modified: Thu, 05 Mar 2026 19:56:59 GMT  
		Size: 961.5 KB (961530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d9f0d2bf9bbdca8dd0db194d39ecfd662214940c3c9635545894df6db028a69`  
		Last Modified: Thu, 05 Mar 2026 19:56:59 GMT  
		Size: 12.2 KB (12185 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0b734f61a0ec0741c613f5538c2be391460137aacd89061e0c355786c8cf562d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338806204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cdc09848acc2d9c1e6b49c24325445eb696516c70cd73abf1b2a8ead1b22fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:54:41 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:54:41 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:54:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:54:56 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a848961f57dabe35a0c43a914b0115f7ae49608f67f8641256beec51a4e1cf`  
		Last Modified: Thu, 05 Mar 2026 19:55:32 GMT  
		Size: 61.7 MB (61703472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d3469aef1334c37a95707711f0a3023fd1435ff543f9b6cb9c9162f66f79a`  
		Last Modified: Thu, 05 Mar 2026 19:55:37 GMT  
		Size: 273.1 MB (273109852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:a3c05b3653d5ca4b8a9aacde8ba34af1180e5d0ea634c379b95dd626bcd830b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1053161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c815116f66604bd58cfc7945461364972892d4790c352b2a094274f2d0dc6`

```dockerfile
```

-	Layers:
	-	`sha256:f95639104a07d24a1e232b77699c503f60c608596a600577056e852e11d2f786`  
		Last Modified: Thu, 05 Mar 2026 19:55:30 GMT  
		Size: 1.0 MB (1040856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c160d10ba90403aff18884ecb898641a275968ef02a55495b7ad881d975a898a`  
		Last Modified: Thu, 05 Mar 2026 19:55:30 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:28591d8f6e465dbbd7451c150258ae72964cbeb8e6bcf7e124f43f6972f9216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357386254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825f6a3a3e92c9f31f17ad46d9acbaa60012ba169acceefd65f3ef96f7c4aff5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:53 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:53 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:57:24 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee925e0ee799b4a5c3719c8e7c64607aef954f2f829b505c4a68906f552a837`  
		Last Modified: Thu, 05 Mar 2026 19:58:33 GMT  
		Size: 61.5 MB (61515268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fc34cfa7d3d953228afb94b5f822a881b82aba53b31b6415ab9380b2609ad`  
		Last Modified: Thu, 05 Mar 2026 19:58:38 GMT  
		Size: 292.3 MB (292295551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7e0a7258d7e62d07c5fac778ce8c64cbf84c6af658db923b239a415b4d750085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.3 KB (986306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e276c7ff0935fab270fe129e895f081a385b514fa863cadcd121bf0fac56c9a`

```dockerfile
```

-	Layers:
	-	`sha256:88be4d73bc757a1055abc0339416de7c0dcebb81eeec50d7efeedff0ff1d7d67`  
		Last Modified: Thu, 05 Mar 2026 19:58:30 GMT  
		Size: 974.1 KB (974074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090a9ebacfeb4708b98bc56ed5925000ce68d17983a2831f0c5af210145997fd`  
		Last Modified: Thu, 05 Mar 2026 19:58:30 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
