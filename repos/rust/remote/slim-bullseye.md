## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:0f96cb289c31dff9a02ee097fdde11201d21551cfe34133d14713d77ef9dd598
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
$ docker pull rust@sha256:bc812cd958e30ce3c73bfdd41ec8e61ad24036b4ec443e24114f65a12105d98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319206455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9c46a003f8f190f5701cd876c32af35fd607064e2e37b3ffcc6715ca7766d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6789b7e16cde7889c8185f42572a9d9ed2fd5bdae2e758865ed6a6efac2d771`  
		Last Modified: Thu, 18 Sep 2025 21:05:45 GMT  
		Size: 293.7 MB (293662376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1cdc17c49b03c78be2c826dcf43ff718d48b8cace9111a6bfb4394c14b294641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205dd3fb1e04da6b18c010b074e4271a489389ce81c80465d1dcfae68a384576`

```dockerfile
```

-	Layers:
	-	`sha256:afd3013c614f5ef27b798e4e92bcaa8fb5828ed48d097a86fc552dcc88cf91cf`  
		Last Modified: Thu, 18 Sep 2025 20:46:32 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f54aa3905616222583845dad90596b50a1d69efb8aade340c409dfe72b8e4d`  
		Last Modified: Thu, 18 Sep 2025 20:46:33 GMT  
		Size: 11.4 KB (11435 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1013ce2ec43b2b9bbce86e05472b58b9e0c228762737ac857de3548afac795ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262589572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6a5e7627b04ff00cc84e0f9acbae51f1766ed32a29dc4ba79d9db84462337`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ebc060b2f805c2dcb5254a7f3e3b083f83167791a319237810faee3a845dbb`  
		Last Modified: Thu, 18 Sep 2025 21:01:09 GMT  
		Size: 233.8 MB (233839115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2a49b424e2fda92b5e97913c1d18b54f6a502227939629cb9da33405964bd188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794f20266bc34ce2eb35b3f99b3c34b811f49092b2bf377a5cfa5ff99740971e`

```dockerfile
```

-	Layers:
	-	`sha256:cf1c88d6205d65c0e6fa68bf232823d9d6ca4f9a96bcd44148e8887f0e7c44fc`  
		Last Modified: Thu, 18 Sep 2025 20:46:37 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9089323cc93ce5fb1c9c67e3a875586d5ce09fb8a1d56c8eac2a0f4aaf7e0e99`  
		Last Modified: Thu, 18 Sep 2025 20:46:38 GMT  
		Size: 11.5 KB (11459 bytes)  
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
