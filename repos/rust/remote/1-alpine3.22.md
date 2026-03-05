## `rust:1-alpine3.22`

```console
$ docker pull rust@sha256:f495b500f1d599f0ac3717c2b051d7777ea7863e351aac977c243b697d328082
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
$ docker pull rust@sha256:1a6aa724bed8cb5233585da7c21aeb66cdde148053157c2f73962364ba8c4a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (336019877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6decc4959b0ffc34fe4fa7b9efa260372760fafd842369a7ba3b3e1eee59c163`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:00 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:56:20 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f803f7f9d67528d9bbea92eaf3e369e62721c417f1bee11c9179dd101be7dfab`  
		Last Modified: Thu, 05 Mar 2026 19:56:59 GMT  
		Size: 65.1 MB (65084139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee20cda5353e1e18362d26694b20c444eb451fe8bda2a4cee36ae0213783207`  
		Last Modified: Thu, 05 Mar 2026 19:57:03 GMT  
		Size: 267.1 MB (267130863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:655d70c69bc98b44bda83e3b4349099bc5dd756d92d25fdf4a1fce665e3c61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.5 KB (974497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdebeb82183283cca1a7cff5a2c0694d9697f07f86de38991a8f61d2d36440c4`

```dockerfile
```

-	Layers:
	-	`sha256:4be376dbf85d26baa885c7cf9d6ee24ea7a9ead28df5208a5f87bcc890db5222`  
		Last Modified: Thu, 05 Mar 2026 19:56:56 GMT  
		Size: 962.3 KB (962311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857881a19a65d7041587d1049f48b3ce789fefa67057e1c391d10efda87783d1`  
		Last Modified: Thu, 05 Mar 2026 19:56:56 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9198c3d77b42805169617fc92a02514cf2e0914b31a32923229a213a34831560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (339006380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a15a5e4351ea6b416046c1039c3d4cc9fb2dd0857780b0f96e34fab7b1a88c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:55:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:55:13 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:55:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:55:29 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f91abde9cdc6e6a335af9359fd3247efaffda7e8e5de8aa9a8c830b327da56`  
		Last Modified: Thu, 05 Mar 2026 19:56:06 GMT  
		Size: 61.8 MB (61758606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332cdb2fddcecc1b926cd2318c20846e59dd903900fea66ab93e8e17f3fb0a77`  
		Last Modified: Thu, 05 Mar 2026 19:56:10 GMT  
		Size: 273.1 MB (273108255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ec25a7aaad385f50d9703658f3445bdbc8e7e8e609726315325eb0b758780968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1053942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fa9f4af2aaa06270d3b65c18ef70b2404d4055dc1d2b28e962e75a4210eff8`

```dockerfile
```

-	Layers:
	-	`sha256:42b0f87ce74c73efa1423eb66c74de8c3eef428c3950c0f4b89dae5744e80c01`  
		Last Modified: Thu, 05 Mar 2026 19:56:04 GMT  
		Size: 1.0 MB (1041637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5e7c072108ef4dfb2d47bcfd1f5298de3a58fd4c4143e024e9edb61ab5b768`  
		Last Modified: Thu, 05 Mar 2026 19:56:04 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:29897becb3554f191285ce126f3531adb98515e515de95c9796af8067bea9ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357601418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21b538719ee9a59d69c32f2e4c8260e26509e4db8a1a13372aec5ead9ed9767`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:58:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:58:46 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:58:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 05 Mar 2026 19:59:14 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19b58d4c49a4c9435a41a6bea841bae678e0a4dc4b978bcdc48b95ebc72737`  
		Last Modified: Thu, 05 Mar 2026 20:00:25 GMT  
		Size: 61.6 MB (61572689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90421f9ade0ccc40b34f28b1e7122268300f62377837318028aaee2ab07f067a`  
		Last Modified: Thu, 05 Mar 2026 20:00:28 GMT  
		Size: 292.3 MB (292294432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:e1ae814aa393c83ea6be3f4c51f823ebda8d22a4050f40a1e946c204e62a5dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.1 KB (987087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fd5dc4b3dfad1d58d4715dfa46e9062075157f7ccb3d3214963afdba73742f`

```dockerfile
```

-	Layers:
	-	`sha256:1f35c313e585fc4f6af3e3ce2fdad9520d14d45049c46d9c77ae7efb04504cac`  
		Last Modified: Thu, 05 Mar 2026 20:00:21 GMT  
		Size: 974.9 KB (974855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d57814fc7cd64d3c8052042ab7194bdb44d6bf505e06a73a8baf249683f2329`  
		Last Modified: Thu, 05 Mar 2026 20:00:20 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
