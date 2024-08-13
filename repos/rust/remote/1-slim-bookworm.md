## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json
