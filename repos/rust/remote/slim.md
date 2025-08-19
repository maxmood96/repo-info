## `rust:slim`

```console
$ docker pull rust@sha256:6c828d9865870a3bc8c02919d73803df22cac59b583d8f2cb30a296abe64748f
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

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:cc16d5a8dda1ca7ea097ed2c88027ea68b178b8e98f496f15e50a544c52dd291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314620826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fbfc7a6d8e82635b7ef1cce35341ba2cfde128769fd721348ba2417a92f55c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2728dc4eea9db5a61561a7c7beecf9d14bcf93f235a7a55c4a7cf4a61ab89dd6`  
		Last Modified: Tue, 12 Aug 2025 23:50:14 GMT  
		Size: 284.8 MB (284847541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:951685148f48e9130158af00eb7db9e253a35877b57b3fdf93741a5cbccc47be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f748eaf727da57e99d93e3286fd4b09cb475a60ad0b99e006b2eaf7f5b5d2a06`

```dockerfile
```

-	Layers:
	-	`sha256:909616a274ebc82ba4a187808a048d3a50d5837423b8b0500a587ee096d6dfe5`  
		Last Modified: Tue, 12 Aug 2025 23:44:58 GMT  
		Size: 4.2 MB (4162921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b21db6beba48255a3c69f8ccbab2e48c3a5dcdbd472002dc6a76cea7ed55d5`  
		Last Modified: Tue, 12 Aug 2025 23:44:59 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:bb8110db64ca55891773ffbda75484987353d383fee84ee113f85225e3fd1fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324448734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47a3b9ee2b0b51901c2ad296e269ef4afdc327e447c218dc20f9671511a06c2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03da1bf74e9da7051efb63b052b674b3cf90bddb8d7505e14a6f76a86b0590f2`  
		Last Modified: Wed, 13 Aug 2025 06:48:00 GMT  
		Size: 298.2 MB (298241246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f9e6f37d1c1abff09512ce8697ff789556462dc7fa76e2ffe41885aadcdc73b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50764c914069d8d68414a4545d8db78d905810e89770ba014fb2ff8ab1756072`

```dockerfile
```

-	Layers:
	-	`sha256:dac32f79f26a5f49b8eb4130d5100c19c850e14ab9eb8effbfeaacc8454ea0bc`  
		Last Modified: Wed, 13 Aug 2025 05:44:37 GMT  
		Size: 4.0 MB (3967765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ce7e6bcd0032ce315e0087d914b92eeb0399ca7cebf01c5860213ad1400573`  
		Last Modified: Wed, 13 Aug 2025 05:44:38 GMT  
		Size: 12.1 KB (12138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4604d36b272de689219620ec7e5f639026f936d52d7346751a6bc7273c08e8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276314249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9b82b35560a2c95ba628f38065971674f422e12ad9b0cd8fbd1d3ec7f79c48`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6d35b4a5416a594bc9e824c8090407353bf85f9fe4fe0bc3bec7a7ab8028dd`  
		Last Modified: Wed, 13 Aug 2025 14:46:01 GMT  
		Size: 246.2 MB (246178205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f5fcb4d8d08959c8ddc77157f1dbc6b4377a33a2f752df6112bcf9f19f5c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907acadb85813c8e06a4102f9e44628e3d0524c5ed1fa6460ff868ab77442f17`

```dockerfile
```

-	Layers:
	-	`sha256:cec0af7201717c94a4fc6c8e0b27ca21bd879e6766027ff3b9db9a6f73d87e99`  
		Last Modified: Wed, 13 Aug 2025 14:44:39 GMT  
		Size: 4.3 MB (4254089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a0a8cbcbdd03b99d2ef291845f3c0ecf57d6ec41341501c6dd196f165c9f55`  
		Last Modified: Wed, 13 Aug 2025 14:44:40 GMT  
		Size: 12.2 KB (12166 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:c6763d2cef7d4038f85ede39979254e366dfab3b508dd0e1450b052e32c502da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334821489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b618a3f4e593ca4c584ecccc77e1de1245ac12fe1ca464e2a69f64cb3ae5fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029ac57c1a1f2fb6b38f93bffd4bc8eb87d2bddf491344be7d7b95c52579f97d`  
		Last Modified: Wed, 13 Aug 2025 00:07:25 GMT  
		Size: 303.5 MB (303532111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:71f6571f9b72cc86d5c44c58b27cd5fd083412e9de6b671cff86a312f5a179b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff97bc9382a4bface1e99249f58c7cf8642be05fb940cffcd18d6b22ba73a4`

```dockerfile
```

-	Layers:
	-	`sha256:66fd19be128af0b0e505cbff2050e8514a81e3675f1aafd6869cdfe3c6c056c6`  
		Last Modified: Tue, 12 Aug 2025 23:45:14 GMT  
		Size: 4.1 MB (4136454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b5098add244582c287a680c533b438b9bccdedadba43f0c1f8227ba508c0d`  
		Last Modified: Tue, 12 Aug 2025 23:45:15 GMT  
		Size: 12.0 KB (12029 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:38626cf3851414a27e07f18f5e86d5f2129073fdcc8d9f4553c40abac1ddfe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377082877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306279cd4dff32299b47d0f95b3f17982a2b83412dd94b1fe30b8e4c749018c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ad0d31f28599bdac1dcd1d6d92752b3b0cd4e4b9a4bc588b7b482228c0d995`  
		Last Modified: Thu, 14 Aug 2025 02:21:29 GMT  
		Size: 343.5 MB (343488664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:83482322f9ffbd827206b77de639e930305fac6c6f9d51e0510fee46e66403d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a53ae952cfd8c8a8fc38c6451d382b22b36d421bda65a50c33a81ff40f3a8`

```dockerfile
```

-	Layers:
	-	`sha256:3f03aa8c068c17040f5390b891747c1512e9d61696d9b5a4787ab532e60f34c7`  
		Last Modified: Wed, 13 Aug 2025 20:44:47 GMT  
		Size: 4.2 MB (4158045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f951aa6d7b8a5147609a52b090d6d9f400c1486af179a4a8572dbb32395935f`  
		Last Modified: Wed, 13 Aug 2025 20:44:48 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:0a777d8ed6595d27c2ab1b46dfa2b05da43fa0cba00a6821177e82dacbcb950f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367814098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92eca4a2574b21c723a257134b6f43cf6cb3c15a1f5f2654e11e40a75dd0648`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff531dad89e2bed20a6aea2bef025296a6e164a153902e15de1d46678cb3c050`  
		Last Modified: Wed, 13 Aug 2025 07:38:09 GMT  
		Size: 338.0 MB (337981041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5902dcdaaa8dbe0b078c7c66cb0ea91d829e3777d1e9e0a4dee5a41c8dbb4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf03ae498a0554baab03e0dddd88b19315497fad306474306e3262b1cbc09be`

```dockerfile
```

-	Layers:
	-	`sha256:179c6b195260c7c21d7a55f397f8676642f17ae2e95206d3fa3861f3c6bbceeb`  
		Last Modified: Wed, 13 Aug 2025 08:44:42 GMT  
		Size: 4.0 MB (3980669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c033972753baa83cf09ce94b2e5c7091491ea6be091bdf77019fe381b497e0`  
		Last Modified: Wed, 13 Aug 2025 08:44:42 GMT  
		Size: 12.1 KB (12062 bytes)  
		MIME: application/vnd.in-toto+json
