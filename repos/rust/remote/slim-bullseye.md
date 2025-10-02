## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:320058cd73954e0a15239944acffaa3c68d795c248ef69fe5cd9a49f6296dfdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:597296a0c01707f1d3cc107a3f1eec8e6657d73ce8a0ce3bd2106b41d4dbef02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301488309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63548207d239a72f97401a403546be89a5d495e18066e67b97a0d85a9a56743e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605634d4ee0d7641d98e8c84043633881cebebe77135e370f7ab0c9ffdf01696`  
		Last Modified: Tue, 30 Sep 2025 20:46:22 GMT  
		Size: 271.2 MB (271229946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fc8ee9176faf9d772ab9920812b83d92720bfa7087ace371d1ecb89e3bbbe825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f42a688309371e1763ff4d1dc2734a4cf8cbd0b113fec357c111eb399ac1bbc`

```dockerfile
```

-	Layers:
	-	`sha256:515dde754ae892e82a94b0f24f2b668519bd60cc3ffe512198237ec7a8e41ae1`  
		Last Modified: Tue, 30 Sep 2025 20:44:42 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175c109a73a5e4356884596b41f041dcc4103141bb2a64a4c5b8d52e3ab64c29`  
		Last Modified: Tue, 30 Sep 2025 20:44:43 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:61e8e7804fc1774e0c7a2c29500c77b1b28f0198c0abe90b0981c340a85539a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319207289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebcc4ca14779b4b135b7da36820e38ebac82bd8db7dc69c8d6e20f0fda3ceab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1759104000'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fd02432a38a6f4fcbeb76d78429da603f9b7e720b1f0286bfa8996e0e4914d7`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 25.5 MB (25546170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84c8fcb3db5cbc7fea407658c05c25f69fb4cf0bf30a927a3569b41ab5e6c91`  
		Last Modified: Thu, 02 Oct 2025 00:32:44 GMT  
		Size: 293.7 MB (293661119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bc33ddfc4c1b27ee66d431fb241c762584768830f551016896806b7960136ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27107f8bf56fd1897e335860cffc959a66fe7a4663d09b74544af6646661f05a`

```dockerfile
```

-	Layers:
	-	`sha256:7b79ea1288c619092ab1025810a197cbd31ee8510a6f7fb96177b827f1b88c94`  
		Last Modified: Wed, 01 Oct 2025 20:45:10 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3881086b230669f94c306c6611a192babe78587578bf3f17ef9742da7a5c3ae`  
		Last Modified: Wed, 01 Oct 2025 20:45:11 GMT  
		Size: 11.4 KB (11436 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5c9580a767f0eb67f11a0adb7e18c161b7dce90c9b023c36ec31fa5ce5ce24e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262584800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77ba1dfdf20bc27c3de036e59193165c894beb18bd496dbffac5180e5bf69d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34319bf66ca15e48d0acb1d5258a3483be04fb4b1bbbcfba61ce63a733d82cd`  
		Last Modified: Tue, 30 Sep 2025 12:09:10 GMT  
		Size: 233.8 MB (233836373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8682f8afb6f85f9c683ba4b529dbc9c15e8b368e0672e97e2d009ef331d79293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64cee3a25974a3129107b3f940a61166276ed8668f46811f4f6143790bffe42`

```dockerfile
```

-	Layers:
	-	`sha256:6272f77bb37395eae87cca4634ff427b791fc884fbc45b3c745a4fcb1aad2803`  
		Last Modified: Tue, 30 Sep 2025 11:44:44 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581ba00124f15a8cfaa8de6561fbb3566630e793ebaba57e5c89497c0ecbab0d`  
		Last Modified: Tue, 30 Sep 2025 11:44:45 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8b11419236afa764e5e35b5f3b456faffe6cb4d9135389324902dad7ee845a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.2 MB (325186498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5782b1d5b75ba08b2fcf559407b91742f8d9fa70723a4ee82a50b7560c895`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0a8d04f8b3b8efb8c05f12e9dcbef34bac52ffba0be154d98198a7faaed142ed`  
		Last Modified: Mon, 29 Sep 2025 23:35:31 GMT  
		Size: 31.2 MB (31191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ac0caf72ba158a1aa2b4d5ef465a95b2250fc188c0ad78491a80842b148a65`  
		Last Modified: Tue, 30 Sep 2025 15:06:45 GMT  
		Size: 294.0 MB (293995022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:18f1040964744edf0de4131e98db2d15662b8d2b7d61f9a7a2e1e85df1d181e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc5220dd9d1943794b0e685b659b67fe359933803bbb9911320a391b0924c21`

```dockerfile
```

-	Layers:
	-	`sha256:820bb09e434e6a7364d0408c8f05b8ba94ef0ac215712fe9f57a992edcf4c333`  
		Last Modified: Tue, 30 Sep 2025 17:44:58 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce128129a121e271fa6e912262de9e945998c2db3e977ead3e3cc2dea7b2a7af`  
		Last Modified: Tue, 30 Sep 2025 17:44:59 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
