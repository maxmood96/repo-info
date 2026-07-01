## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:bdd51fa1f2ff1b9accee5224246e39f4817228ee1c20e335635e8e55badec324
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:138d97c279ad440ac738f2d21d955d4d7301c68574742ef27a8e0265db5fa038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339205399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fade43faf35675821a6105724d6af6e75429028bd8afa5d693cb880d3b1e6528`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:43:30 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:43:30 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:43:30 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:43:49 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15c387f739445af4a538b39f85c9a8b306c9552db06af7d7bc14fe04de2f1a2`  
		Last Modified: Tue, 30 Jun 2026 23:44:29 GMT  
		Size: 65.0 MB (65028721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09161f1ca7cc3f589e76dbb84d09b82c14d5d31d62bd2f754f3d9d541f4c9bb`  
		Last Modified: Tue, 30 Jun 2026 23:44:33 GMT  
		Size: 270.5 MB (270529803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:4aeb6ea4a2ec5cc4d0dcdcde7f86387ba3b4f2615e69c5c11f3c8379df96d6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.0 KB (973035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b006475ebbc2c0222f8d7c96cb0a1be5a3ee1a96bb3e9cb023fba0b8dd905506`

```dockerfile
```

-	Layers:
	-	`sha256:b144cad7dd5b66ac0edc394abb14344a0a36f72a66ec904f79a79a9c6a9acdea`  
		Last Modified: Tue, 30 Jun 2026 23:44:26 GMT  
		Size: 960.8 KB (960849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f9cca1adc4a813dd10874b3699000fa1da383f624979f031fbbd7d61f812b0`  
		Last Modified: Tue, 30 Jun 2026 23:44:26 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e43795e70a61d90a365422a2caaa2523e36c0ee17e2bdb947ebac8852259c10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340082104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237c1eadb3e068c6a0168d866eb1bcb56016b26adbef5da799ebc3f07a2ba1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:41:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:48 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:41:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:42:02 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6e446fc5543c05c8e67db707e7961d2605a06d77075e530e8527ef7b00a200`  
		Last Modified: Tue, 30 Jun 2026 23:42:40 GMT  
		Size: 61.7 MB (61700223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63875bd581d12fa423eac144a42c48a9964e49ddc616d03edec54b63920681de`  
		Last Modified: Tue, 30 Jun 2026 23:42:43 GMT  
		Size: 274.4 MB (274387416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7c91fdf19310223f04e80926fbe96ed4866f3934e313e0697a23d1c1dd28c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1052479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b46979ed91bdec6714a215cecbd40cc04d7835c542c7905200fdb23c06a6c0`

```dockerfile
```

-	Layers:
	-	`sha256:0505aab31f67fdbcea04491186733493f043d7698175c896c8e0001b208f403f`  
		Last Modified: Tue, 30 Jun 2026 23:42:37 GMT  
		Size: 1.0 MB (1040175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e28f28e019b67e641f4173a32b86d77ca27e8d1a87acd0862a3e56069ff8fd9`  
		Last Modified: Tue, 30 Jun 2026 23:42:37 GMT  
		Size: 12.3 KB (12304 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:9b2fe155572da4ae6a9a69b2c4cf2c96e5c0410c4dcb7a9addb69428afd5fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358527711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9313226ecc03e77d96c99ad1ece37f38e3319f8b9be12cd15840d132d9d3ded2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:31 GMT
ADD alpine-minirootfs-3.21.7-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:31 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:46:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:46:39 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:46:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:46:57 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe51ead1f71865857c2c015e74518a0be9e72c6a70a845d843f7dd0cd2ee6e2e`  
		Last Modified: Fri, 17 Apr 2026 00:00:41 GMT  
		Size: 3.6 MB (3578920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421da62b2f652ea46b355c8ac0e33872ceaa7128513aa1ced01021f6356e1db7`  
		Last Modified: Tue, 30 Jun 2026 23:48:11 GMT  
		Size: 61.5 MB (61512260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902357bb24da9a937516b79d1492b548f83aac12f08437e9d77ec1058bd025a5`  
		Last Modified: Tue, 30 Jun 2026 23:48:16 GMT  
		Size: 293.4 MB (293436531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b8b1b7af7110113b6511d023e9f1d34e169d67d46106ea1759b291eefeb79de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.6 KB (985625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e397eae4196b395184d340547c0277846581306ebc8aac1c095d1ed962cb20`

```dockerfile
```

-	Layers:
	-	`sha256:0c16b234330aabb2dd8ebc8a06f6e54246a26c752076f78e28d674878be2b200`  
		Last Modified: Tue, 30 Jun 2026 23:48:08 GMT  
		Size: 973.4 KB (973393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a71d42d9bc8fdd870c2bd2ec268bafc5f21c96fc64d618486fce82c6b22b47`  
		Last Modified: Tue, 30 Jun 2026 23:48:08 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
