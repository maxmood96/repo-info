## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:68142f487f68f281bdc7a1e751ec5011e8c000550e60affa89b1e4a5ad80e06b
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
$ docker pull rust@sha256:a4b59b37ea8358e0c5f0d16bf865c791e09d27e36626ea9f9fc09bddaaa9c179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290247522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f463501841cf1014b89fab320d78ac9f79e8b2df384efa0a78d6709a3360b99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Nov 2024 14:36:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a87695fe58a8a13797d4191a945c5f261d74c0c350be93a70ea07a0465e349`  
		Last Modified: Tue, 03 Dec 2024 02:35:15 GMT  
		Size: 262.0 MB (262015942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b32d2712021035b5d54b6c335ee3884b39f1f11cb3803a14f53fb6eb2042cfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c8beb14fe84959b105283f3f42a3543f2f044f2b2068d28f59dc9860efd8e6`

```dockerfile
```

-	Layers:
	-	`sha256:1a6c93cd72ef381e0bafe1e53134d50c54553add292d66a67ccf9e55bc7236ad`  
		Last Modified: Tue, 03 Dec 2024 02:35:11 GMT  
		Size: 4.0 MB (3959668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5677444d9f54bce99de37a67a1a2b6cb0640abf97eebd3f180994e971983b951`  
		Last Modified: Tue, 03 Dec 2024 02:35:11 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:53f2331e1574f095704c0a25b03b9bcede3f296a729288f76e1844827cb805b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300753906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84eb97d517fb001c71195ed49d1f08d2cf7f15e616af078ca2af057798a1569`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Nov 2024 14:36:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f033d021217436244b442b4c568750b1db62d36c98b56bf78162555e10ae491`  
		Last Modified: Tue, 03 Dec 2024 02:32:09 GMT  
		Size: 271.5 MB (271548419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:69c10a0f1f348bcc4f945757b2d13697bfdcd77d9ecd887ecd8139f5e4a7bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703b444be24a975b204379f2f41913e89ca90018be97fe4a068360364e0f8601`

```dockerfile
```

-	Layers:
	-	`sha256:9e34b316ddbd47f9eb91eb2babfbe090f4e30ebd6c3317dc082657b1517ee4f2`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 3.9 MB (3939581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ef75bd5420ca3776ce7123d2342045f5ade5b991dca845c64b501afa3e5a7bd`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json
