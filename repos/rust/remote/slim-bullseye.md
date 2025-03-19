## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:d28cb53460af69241b4af695b7cbca8dfea1dfa0439a355ccdc04c347f382605
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
$ docker pull rust@sha256:94205f90cc51967908954ffe6188bbdbf7dc0778488d00d813f4f1fa1892925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283905874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40c76342b68b9e48eca0b9927f215b8ceac3f366f9b723cc6fdfe087ac995fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d519d1c337fc634e4fb6f37ecc86f4a1e2ad491ff41ed34cdddda0ebde631`  
		Last Modified: Tue, 18 Mar 2025 21:46:57 GMT  
		Size: 253.7 MB (253652038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:78b7369b066da8bfd3494f6ad8007f65246b3c3851feaea1b09cc7a108a221d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ba45674a14de34e537f3d28fc3e6ca8c297ab37fab71bb8d1bfdbd43f691fc`

```dockerfile
```

-	Layers:
	-	`sha256:9d376c5f07e5c9094412ccf0e96f8bb2220bf6ad975aa2232b7e25849027a0a9`  
		Last Modified: Tue, 18 Mar 2025 21:46:51 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c57772a7058b56b4eafeeca42c8899076421e177c3f32346691d4717adda3af`  
		Last Modified: Tue, 18 Mar 2025 21:46:51 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:9c7d08046cfd02760b12a2c94dffea27a6194e2efba278d8a9a0564a0de7264e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297900890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412ce5b41698f46f474642a5014a35e5dfcd29954da4d25c5d33a3328ed85135`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Mar 2025 18:46:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4706bf18ed3d7a4d8c978c51ffe46aee6552784376cc6daea0e760827323c60c`  
		Last Modified: Mon, 17 Mar 2025 23:39:57 GMT  
		Size: 272.4 MB (272365546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4f2e5cf7498d6c247ef31ccc29ea5b73c486f0c2dcb8f1b585f49b87afce0069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cc8fb213e9da03e365807535a5538707adaaad375f199d8e53faa768776a0b`

```dockerfile
```

-	Layers:
	-	`sha256:57bcb07fab63fb34e121f5ca5d29fb38a4e927af6689beac6384f9bf4c59718b`  
		Last Modified: Mon, 17 Mar 2025 23:39:50 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7f71d567bb5d3e1ac241c677fe6c395dc8bb6cbe435263625552be8106ecc1`  
		Last Modified: Mon, 17 Mar 2025 23:39:50 GMT  
		Size: 11.4 KB (11429 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0dbee5740e8de8a5919b86a38cea1d147c8bdda60e27fbde76a9d261708dc06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343064410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db88627ae13bb0df99afe68c0be10fbf89071aeb2a9a8fe43802efecc191107`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Mar 2025 18:46:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a0b83d78cefd7317f64beb82d1cf5f46d451422c51bd01eec1ed38d00b55a`  
		Last Modified: Tue, 18 Mar 2025 01:17:54 GMT  
		Size: 314.3 MB (314318487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:33e5fc21abc2a215080c90f7ff0447f5b252b197f6049ccbf4b47e6f8d301292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25367db37a277f2124deddefbda132c30d18c3ccf957e323a4316b93ba9534b9`

```dockerfile
```

-	Layers:
	-	`sha256:c91c9894bac202514b9ca22d405cfdb4ced3422fee5084939093fa5949a90e28`  
		Last Modified: Tue, 18 Mar 2025 01:17:48 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2af04a2b58d24752f33c03dcecb866c138f9f4ec898a91c3ddc5c554149994`  
		Last Modified: Tue, 18 Mar 2025 01:17:47 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:178e05ddfc8fb33730da345d14d9a95e2e63885c4f9d139d47ea59789065d71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302600543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7caa4c4e11371fc433d2ab6d0d64390fb4db5ec9030ae5763c64074d5ccaa1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1258eff17ee897d4d30552460fd5e81ea59b325cff186ede829a46b10532941`  
		Last Modified: Tue, 18 Mar 2025 21:25:36 GMT  
		Size: 271.4 MB (271420206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0ea3c64fc5d767ef994e7c6c5c90ab59ea87bfe3469a0b5a1d690da24a866d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5616badd6a87822c7a88fb90a1e9f497873f574dbc8f08d3eaa743a0d096a2a`

```dockerfile
```

-	Layers:
	-	`sha256:e5acfde952b22fac7ae9aea6a67a4cc173d3e39c5b2cd2006942f29f72a51d7b`  
		Last Modified: Tue, 18 Mar 2025 21:25:35 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0aa69b9a3ab1076873d38be70b0df3bc207f52fdb5d814234393da20c51d60`  
		Last Modified: Tue, 18 Mar 2025 21:25:29 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json
