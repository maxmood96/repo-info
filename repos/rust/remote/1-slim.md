## `rust:1-slim`

```console
$ docker pull rust@sha256:af95fd1bb203d15e0e82a3c2ade1799767aa99dd91a652ce044533d6582d7415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:74623cf14bec67a03b1db2f327f56fc22b481448c364818b409f14140e809efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318554417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99346b7f2e3220d358697b4709f0d28d01e8a2c39d6b8db78dcd2dc461c31d38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 23:54:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 23:54:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 23:54:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d62a8912a60985c58122dce04a9c7ad38977b6be35c28403797230ce96f830`  
		Last Modified: Fri, 31 Oct 2025 02:03:43 GMT  
		Size: 288.8 MB (288776493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:090f7786227752172a81ceda58c95fc5064e741445fe6a618a70cc9bc5e901d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49f362945b73e6bd1e3a1a93bcb232303c1a9e5ea97903af972e3987bb87d90`

```dockerfile
```

-	Layers:
	-	`sha256:6ad151e18e0ecebf8361a3e286e6b71b17336f2340ece76ef439245a49fe5ef5`  
		Last Modified: Fri, 31 Oct 2025 02:45:07 GMT  
		Size: 4.2 MB (4165011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dffafedc3286bc53a33bc2f973361af6661c76179d5b82dbf543106bca5f4ef`  
		Last Modified: Fri, 31 Oct 2025 02:45:07 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Fri, 31 Oct 2025 00:34:47 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Fri, 31 Oct 2025 00:03:47 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:62f0d8958887d451eb68146c2f43afc1903cc0de92e364c2024ba97b2092595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.5 MB (395469804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152d7dfce8a682613304de5082afa01cad372a8436e25461176e0f9e7fc486d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 00:59:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 31 Oct 2025 00:59:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Fri, 31 Oct 2025 00:59:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a111edc6360b1dbf96c1146185c3734f5db3ef7ef33430baf890bf7a3d7f5be`  
		Last Modified: Fri, 31 Oct 2025 01:01:01 GMT  
		Size: 361.9 MB (361871286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ecdb8add5556b8e8839d488bb9e42b416bf823e2694c0d8d69f028588da1243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0191dad5934128279637c869063bf6ee350a01f52680394cedea190de69115df`

```dockerfile
```

-	Layers:
	-	`sha256:12a8d0093d1ee3a1a824ad3e7e0b01a11773dc6d6c551632a03f174c4db586af`  
		Last Modified: Fri, 31 Oct 2025 02:45:21 GMT  
		Size: 4.2 MB (4161472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ec4b0ba5b26005040d87a90ca84a08982d813f02ef3d11198368e0a35b686b`  
		Last Modified: Fri, 31 Oct 2025 02:45:21 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Fri, 31 Oct 2025 00:34:53 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Fri, 31 Oct 2025 00:35:48 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json
