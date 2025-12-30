## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:db59307cce622fdcd0ced9a8d16460e712d97267b9239a4daed27e912101ff3a
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
$ docker pull rust@sha256:150570a6de035cfd3414953e33573f9589aff4d136d068623fde84c8e3f3bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303620999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c5d2fe62ffcbc166120edb47c7bf45824a0884f4bc5d16dde4a4fa83a91f4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:47:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Tue, 30 Dec 2025 00:47:48 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6415b0a047281c256aec96d0dfa40aa2799bb36c25eeff44616fae6484209ba3`  
		Last Modified: Tue, 30 Dec 2025 00:48:47 GMT  
		Size: 273.4 MB (273362558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7aa6753b85288f3df1d090a019bdaa99ba1f37ae272411c4cbf63f1a963e93ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9e81fe2b4c1c0aa42a9291e0a3ad76d9b44d0c57354f5ad3f32218c6060062`

```dockerfile
```

-	Layers:
	-	`sha256:4cc6be099675fb5804519205c0a89ccfb9d7a44d180e70a1f6067e496d70fca0`  
		Last Modified: Tue, 30 Dec 2025 03:46:44 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa594c84ed60d552ee90d02c9fe99bd6d6ffbf1de2ac77202860bc1371370912`  
		Last Modified: Tue, 30 Dec 2025 03:46:47 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:c35cb0b1fd62492131d3771d705f391e4c40c076336591ba1b316011e4a48a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325583401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3515094d2bc76db97d4be0ca3cb1d7006837e55a924aaab7a0ed3c3d7b8720e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:45:29 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Dec 2025 01:45:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Tue, 30 Dec 2025 01:45:29 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2a8bd9cac183a5aef78511c4c21902da16a7694ab5eb12418535753521883`  
		Last Modified: Tue, 30 Dec 2025 01:46:25 GMT  
		Size: 300.0 MB (300037176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1d9e5e718f0339ec7425d40f49d9c251b393bb267f2d4b0668561ad93f4f9540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f643a86705b3a3cbcb2b795bff9eb69ef7a8bdfd7742f5342babaa95531ccb94`

```dockerfile
```

-	Layers:
	-	`sha256:20977f8c05a33f4fa0178ba852f37505689fb3717af617b62c567b427815b9ec`  
		Last Modified: Tue, 30 Dec 2025 03:46:51 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fca1f41c0d0801c80aad279a197271eedde9b473c8a72208e0e83bf8764f91`  
		Last Modified: Tue, 30 Dec 2025 03:46:52 GMT  
		Size: 12.8 KB (12793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6bc849b9aebdccacdcdbc49691fc26e3b9b6c22fe82af3aa42ec10c31b089024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264867973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce09587a7e7620ec25b74d43460adecf56f006c051cdfb009587cb43084431c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:50:59 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Dec 2025 00:50:59 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Tue, 30 Dec 2025 00:50:59 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d00b9e0fd4a05ec6c9f1ee3c6bd617280d119df3744ecdad4106b8b40b7eaa3`  
		Last Modified: Tue, 30 Dec 2025 00:51:55 GMT  
		Size: 236.1 MB (236119511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4d12bc1731f86aa192cf3b7612f15e7528b1b68521cb7477beb51261f5c360f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb01ad7e786ac19589f35b574cc71b2d9abbd7547235d0c838a66174c19f4f49`

```dockerfile
```

-	Layers:
	-	`sha256:0ea8b5d9a5c288e6c26abe116546cae37194679816cfc414ca2dcfa972ce1e34`  
		Last Modified: Tue, 30 Dec 2025 03:46:56 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a323f4e0faaa03d7cd3513d1e3f5624efdd1db47fe462f0b40193c30d1a551`  
		Last Modified: Tue, 30 Dec 2025 03:46:57 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c1cb0dfebfe9526977ecccd3af60e3f154dd1f3eb41198d27191059d14c6ca87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330025685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99f3d6f266ed1c3deb265b0c016a3354adcccee40c8147920e10e83d43a4930`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:15:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Dec 2025 00:15:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Tue, 30 Dec 2025 00:15:27 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fa566a3e7b480e5bbc6006ae0d5a282051a1a92c7b8994dd11343ec7ed054045`  
		Last Modified: Mon, 29 Dec 2025 22:25:08 GMT  
		Size: 31.2 MB (31191561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc4fab15126a63a6a74079d935fd833b8e4d6b6b0096d24a625b71d91807987`  
		Last Modified: Tue, 30 Dec 2025 00:17:09 GMT  
		Size: 298.8 MB (298834124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:669e64f51e9a23b0caecc580207921867b13124ad172bd64a743f6a0c6d69733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4cf1bc1888b3142a1c053e0588539cceffdadac65060e62913abc7a8eb3dc0`

```dockerfile
```

-	Layers:
	-	`sha256:9b2cc9d108a490edd3e12db02c887ce1920f3754767fbb81dda14c89632478d4`  
		Last Modified: Tue, 30 Dec 2025 03:47:01 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc73f6c8593f0cd5634269008fdcbce94b40259695ed990e3db7d8975f4c6543`  
		Last Modified: Tue, 30 Dec 2025 03:47:02 GMT  
		Size: 12.7 KB (12681 bytes)  
		MIME: application/vnd.in-toto+json
