## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json
