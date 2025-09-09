## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:5bc71e28ba09338f60b7f541d4d07df3a6dfb0b89ae49f63ab5d2a39d7a7f5ec
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
$ docker pull rust@sha256:294917190b5a3fed18d3303213943f40ec9b644b3cd6e5cdc8cd029334a770b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308426587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4894a80c681567a132f49725f3fc179d12a004160f4dfa83acbc3046257dfcd7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe8ad7f7ce9c2d9d7a78b6760d15fc86790e78879651520447ea1813744a0c3`  
		Last Modified: Mon, 08 Sep 2025 23:49:25 GMT  
		Size: 280.2 MB (280198241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9d8268057465411e1b2973adeb0cadae5d1d5f30e87d69455303252f8f95dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef047c172897636369942d88da29fc2dbd57d9137c16f949350e9ea3878bef`

```dockerfile
```

-	Layers:
	-	`sha256:edc836e605d0b73033225af2da940be913f7c793e03f35c95eef955e2d9799be`  
		Last Modified: Mon, 08 Sep 2025 23:44:54 GMT  
		Size: 4.1 MB (4095479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23ce23b8618027b46335df4d7e5963dcaf963c450d1bf7931135ba341356c6a`  
		Last Modified: Mon, 08 Sep 2025 23:44:55 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:e8acc5e3bbe3cac1ebab6f9fbc6a5bb5def1804ff9c4f99b207a9638584bea72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.8 MB (319763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d63940a3384d4245ab56e96df42c5708c16ebce43ff8fabe4a8177944467af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8461c69747357981bb2cc2c7d2c5a0b1f510673807effcbe3d189c544099e22`  
		Last Modified: Wed, 13 Aug 2025 05:27:51 GMT  
		Size: 295.8 MB (295824265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:84ce35789f11d9cd1aafcb17e0a546bdaac8cbfab20d7b833ed205705076cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609d46092e353a23c70e25cd44f18e2b731fd2e100e8bbe09bb8ad8a0248eed`

```dockerfile
```

-	Layers:
	-	`sha256:60ef332c26f4a85a3f4aeca18cd7a9cfd518e8dba9937f32cfe1734a140fb7a1`  
		Last Modified: Wed, 13 Aug 2025 05:44:27 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aaca0e6a7eef7e265efcad90a1b6c94fae787287e02a4b6d0e67cf744eae753`  
		Last Modified: Wed, 13 Aug 2025 05:44:27 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a99273a02196f70530451dbfbba0b1991b9aa2d98a94815ecb9a275de91d2484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270439441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a004802119cbf1ec1e3080a21a456320d8b9b44a1bc74cbd6d60b9e699331969`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d7924ec4dfd5eaded86acef17564df2f9cb263b339cc69ea0a20eff9b2f1dc`  
		Last Modified: Wed, 13 Aug 2025 13:59:43 GMT  
		Size: 242.4 MB (242357440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:64d3e2c9800f4ee48f2c09f34934e4551854812af1e0fdf3b9b0b71453cf6b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8e69b967bb2900e7fb149a993ddb560e7a6e083c4c343a53ac70736baa1e43`

```dockerfile
```

-	Layers:
	-	`sha256:1a6a06b13023507f67c35e431d035019f4c86c9c09716f00b428143aef9b450f`  
		Last Modified: Wed, 13 Aug 2025 14:44:30 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528f7c730d5d85219847d594c3263799eb6dc97e06b35fadf235c79c6a7bdaee`  
		Last Modified: Wed, 13 Aug 2025 14:44:30 GMT  
		Size: 13.4 KB (13422 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6c387ae4d98d23544f489340df8699773c249ecf82f628884164aa9002fd9cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327872088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e7d77b0eee2de4b1062583d4940c361b58f0ac0981c774870241c6c8543ea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bc42234f8cad30c72e77775cbc0cd08d0fe6cf11554c948c694d02933f0294`  
		Last Modified: Mon, 08 Sep 2025 21:33:26 GMT  
		Size: 298.7 MB (298662454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:462829ebd23dd5b90e3bb6d0a4f6f02b4e26298445ed61e9a7060db359f9704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4086914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a82120079c1776cbe08031d5a8276629ed58eb66668d0be1442acab432690a6`

```dockerfile
```

-	Layers:
	-	`sha256:68c0205625b956839814361a5d1fda44c32a496e318ad24daff5ee632d1299bc`  
		Last Modified: Mon, 08 Sep 2025 23:45:08 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c9a360b0f4ea783b4b9a190407995f14cb9bf33b5f6d82b328f9c1d4210c38`  
		Last Modified: Mon, 08 Sep 2025 23:45:09 GMT  
		Size: 12.1 KB (12052 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:32be70c3795fd46e2f14a929487bb97b87851c354823596fcebe2aaf177430a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.4 MB (377447910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72049787b993ad089f7c62bb5b20ce71d7d100a3a04ef186f9e213d0e9601d7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e17dbf5f074e15ae2b56b462816a6f6e2bbb217034f3af7ff3d2a459362448`  
		Last Modified: Wed, 13 Aug 2025 19:11:52 GMT  
		Size: 345.4 MB (345374490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:62f5fc1e7841f588b13f39fc8c100a89b08153358bdcabe50e92ee49e6d4481a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513e93505a74d4d15ce224b213e203145d66da98613215f71fe27de3583a3e62`

```dockerfile
```

-	Layers:
	-	`sha256:74eb8afaa571666f4419cab29e046bdfd780db8c3f0637055c405a17042396fc`  
		Last Modified: Wed, 13 Aug 2025 20:44:39 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a2eda7248e8c7740790c4cef628b318023270b01aebcf90a62de927db53072`  
		Last Modified: Wed, 13 Aug 2025 20:44:40 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b44737a5fef65e7b1c7544fc879b54f66bcad463bb2ce76d9cb69d58703df3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362625959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d42923346c40858992b2b2c25a7fc274e4328a57ee9038a0da4ea0ebdfa30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060beaa48bbcfd9c40d5ef8cefec1f34bef8f207ab08228cd807aeaaeb077e24`  
		Last Modified: Wed, 13 Aug 2025 19:16:27 GMT  
		Size: 335.7 MB (335738123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e027cfde7512e3e9fee4a937709670fc3c30806070efb622143ced6a33cea6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57b0147ed9e93ba03b3c4cbf4425f57a17998e79139a8b0d2a57b7b185dec0`

```dockerfile
```

-	Layers:
	-	`sha256:32c3aff913719472027ddb3b551671a4280f000f91b48dbfa4131a2da08a8b13`  
		Last Modified: Wed, 13 Aug 2025 20:44:45 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e843caae4543d7f70262bb5cfefa23088c3050edf1c955858ca7ac1c54939d63`  
		Last Modified: Wed, 13 Aug 2025 20:44:46 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json
