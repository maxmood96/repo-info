## `rust:alpine3.24`

```console
$ docker pull rust@sha256:a41f7740f8b45d45795624eec13a8b42263cc700f19f7e4e86e04d3dda08a479
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.24` - linux; amd64

```console
$ docker pull rust@sha256:f5c84c3751de59f0f318acfbed8b2d04693a12d9171f15835d9c11c9ddcf52db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349455443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be1484b093e4b27fa7de92c29073126617f6a72d428586fe4b782a6e21dccdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:43:40 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:43:40 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:43:40 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:43:57 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9a4131e96b01688c4e6fd3400fd8ec85f23f1cb606d1b92364345a6b96764`  
		Last Modified: Tue, 30 Jun 2026 23:44:34 GMT  
		Size: 75.1 MB (75079295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43c54cb9b8ea310a3730234455f912038e9194b4bce20da9e9f9448e2d9eb42`  
		Last Modified: Tue, 30 Jun 2026 23:44:38 GMT  
		Size: 270.5 MB (270529757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.24` - unknown; unknown

```console
$ docker pull rust@sha256:3dd723e42e6af08c5dcfb40433f2a58f4411c15bb7cb79ded382be29a38b20c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7c7e96ffa1ea7014399a702938a07dd185a692928f13cf7b2e1b2136e2097`

```dockerfile
```

-	Layers:
	-	`sha256:4f80505f251702d1930721db6ad88480158d927e3891c690b982336cfca297b7`  
		Last Modified: Tue, 30 Jun 2026 23:44:31 GMT  
		Size: 990.5 KB (990501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbd4740e108a6e36df2b81a7c549ebd1100e4af96ca70aeae1649c954960226`  
		Last Modified: Tue, 30 Jun 2026 23:44:31 GMT  
		Size: 13.4 KB (13388 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ccba3c5d98fc76a5ac6eade9bcbbb946635657457c3d269982396633a66da08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345077547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd3d45841e4e3dc66a46f939ce846575a08024b3af496986e404112a47e7051`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:41:10 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:10 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:41:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:41:24 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538661f218cd4e60de084491e8e3a35de6a046b1bf6629a2cfcd7e071a475733`  
		Last Modified: Tue, 30 Jun 2026 23:42:03 GMT  
		Size: 66.5 MB (66507131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5d354fe3e18cefa9d6abb58dbd1ee8b94e686655bc442974054ad13f931ec4`  
		Last Modified: Tue, 30 Jun 2026 23:42:08 GMT  
		Size: 274.4 MB (274387379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.24` - unknown; unknown

```console
$ docker pull rust@sha256:f5abec2d2b9b8cf81fe03f9d842839bf846720844d2893c1f1dc9496b4fe871f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed991754e793a88e038ca5715b9d55f306c11173b10ac856b93260d8079429e`

```dockerfile
```

-	Layers:
	-	`sha256:c9bfc4f94fb748a26fd763c53b5e0dabd4ec59c9e7d8faffe6e211b9f0f3be2b`  
		Last Modified: Tue, 30 Jun 2026 23:42:00 GMT  
		Size: 1.0 MB (1049454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d51ad22e1685e782f46c191678357cce2ea818aa2ed540f42d43a33aecc573e`  
		Last Modified: Tue, 30 Jun 2026 23:41:59 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.24` - linux; ppc64le

```console
$ docker pull rust@sha256:4140e5804a1f62768698069c2132af1cd6b2396f73801132a2e14b6739bc886e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363644421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b07d4ced549c71179c5957900257e588cca0d3638f1cb40d88547762c01fcc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:49:03 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:49:03 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:49:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:49:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62da8e3dccbc51c69986848041d9e9ae77da645be996989fed8e9cca52cdc69c`  
		Last Modified: Tue, 30 Jun 2026 23:50:34 GMT  
		Size: 66.4 MB (66394546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a83b12f2bec426b14c69a573217921b8544047753ecf84ccce093456ea3f046`  
		Last Modified: Tue, 30 Jun 2026 23:50:38 GMT  
		Size: 293.4 MB (293436475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.24` - unknown; unknown

```console
$ docker pull rust@sha256:c79ef3fe7e8b5d73feaf84c1104cb14100c0e13b2444f4c3ed952b649e12552f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.2 KB (996201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f992c1703b33a154de6dcc47951553e902cec4612190df5d07a4114d8e2834`

```dockerfile
```

-	Layers:
	-	`sha256:b791b0a4ac011c8f09e1fcead5e43569e035503ba000deb161ddf7440e30854f`  
		Last Modified: Tue, 30 Jun 2026 23:50:31 GMT  
		Size: 982.7 KB (982741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dbe751a497ee8bf364f0dd4ab26601a917239c51ee804e9d7d1abf385f5fa63`  
		Last Modified: Tue, 30 Jun 2026 23:50:31 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
