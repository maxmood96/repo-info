## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:1bf538b6b2931ea86c4761e7f979dc85ebab6af2ac905b039fd36e6a23436365
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:7d3b454cdb871a9bcad9a4584dc3f6ed301097955d7966ccbc764aacd0e029e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299831773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c84ca01e3bb96482bcd8b3f8e4371f519de2113799569011e4b9432a92f1ae0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6156fdefed72d37a6f0d7e0c838dfe89e8fb2022a88fe9910a05b0fa209c7a`  
		Last Modified: Tue, 12 Aug 2025 23:46:30 GMT  
		Size: 269.6 MB (269575655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e64e25fc7c5080643c5ecac0a11ba9db424c4a5bead733bd9e56c8483e4c472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f63664c265ded1daa7accb7bbf4cfe48ece3885d3eb6913ed74159f9ee1f4`

```dockerfile
```

-	Layers:
	-	`sha256:f4786753361aa046666eb91f1810515998700f201c071d44ec5e84b40df57460`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98005521014010c53df5496afb5c3647661e51335d891888bfd517e3ff253289`  
		Last Modified: Tue, 12 Aug 2025 23:44:50 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:056deab4d006dbedde3336b534cc0b99fc2f7edb026ed9a2dc8e6befa901e60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 MB (315791030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266737bd4f410276a4b4736468122d497b4a17aa79f012d5f14f40f6015c9ba2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dceb61d5a0cd40a4fc7b6629327699f80e4e3781a42d496ceb2c4934b0fe8523`  
		Last Modified: Wed, 13 Aug 2025 13:01:30 GMT  
		Size: 290.2 MB (290246913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b09c11c859d53582193bbf2a47760c8987587f173f5609693a535f8a4cb63370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1db04d2161e401bc219bfd4da915b03a2a7e307c361cc884ae3ec6695f8ad6`

```dockerfile
```

-	Layers:
	-	`sha256:d2e755b4273dd05505378bd98ce7157f4da674ae01511926bbd2d9139851ba20`  
		Last Modified: Wed, 13 Aug 2025 05:44:32 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be599b526986fb3a14f4af02bea8dd95dbbeb2397eae1c50d92496d124760230`  
		Last Modified: Wed, 13 Aug 2025 05:44:33 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d12cdcd25cc06e8acfefbb4532b63121a4c4a6f394932f73fb2f4067c23f766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260974260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d29d3c3f8a5294044ed06d85dbded35bd8d0e08db1d7503b4abcb0f39d41ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac61d04e50e2f4702fe5c5d00ec7eabf2b63305ea36fcd3177c64ad69a07a2f`  
		Last Modified: Wed, 13 Aug 2025 14:51:49 GMT  
		Size: 232.2 MB (232223769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:559b77ad8779870e8245e7a1586800e078a851071214c9b7e6f1ca46b0efad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9f8e678473f30172076fcc9244531a8db963d4cb5d4eebfa3488a6fedc580b`

```dockerfile
```

-	Layers:
	-	`sha256:aba284a19945289693242bfdafb401fd6c042281793ee1a52bb090950f6e6ef4`  
		Last Modified: Wed, 13 Aug 2025 14:44:36 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0000cd2ca3501f0499c3f18e2c2e749fa2bb7e71f54c4b2a28572c2b8e0aeed`  
		Last Modified: Wed, 13 Aug 2025 14:44:37 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b58e553189f44f02b8e67a32a5ad6dd2bc699de8498cb13d67cce8a724767351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322996876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea7335e98d97b603e2e00aed46eb9543bbc0b043890fdbc3673a124fcdc15a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f952d923c30616dd90d420b9958914d214065718a4cbc33bd4dbc7e5e35712c2`  
		Last Modified: Tue, 12 Aug 2025 20:44:50 GMT  
		Size: 31.2 MB (31189737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139257ff1019505afd189f60ee7b1ea670a92f93da32e95f40f16c5c601e11d0`  
		Last Modified: Wed, 13 Aug 2025 00:46:04 GMT  
		Size: 291.8 MB (291807139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1406362434e50d5326e9d5dcca1b449fc57b9644d86b4b694dabdd1eea3685fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac5ea0a8fbe426c78768cf9c92acbdaf81c24208adf8766a7c59edb1d5b367`

```dockerfile
```

-	Layers:
	-	`sha256:e253001ab5419b56d07e35d179c1037f5defb674c7df30d84093a0e47f58dca9`  
		Last Modified: Tue, 12 Aug 2025 23:45:04 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcecc75cb6e218150dbe20aa500c331dcc93772eb25d65e6adc36afa6fb2688f`  
		Last Modified: Tue, 12 Aug 2025 23:45:05 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
