## `rust:slim-trixie`

```console
$ docker pull rust@sha256:6275519394d00d1f0a9ee15894c5851f4d6fdefc30648bc446b39c6eaf29c364
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

### `rust:slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:f9ab60da9c7296b7b1d4c9bc89b56900ca86ee4994133d5431d08d3565f02bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314620313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a61024eb09ddaff67d7a63205eef099f7e4471120cce4e1b1b508119bf40a7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb4d6251970d0781673d24e049f2b090f3a888d19382d3e2dbc88b3e944e3b8`  
		Last Modified: Tue, 26 Aug 2025 22:56:27 GMT  
		Size: 284.8 MB (284847028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:6de6f71c51468750dec60fe5e27534f3856579a3d4ea0dd953ae1f92d44b9647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687f7dd43f3692d4fea970b153a40079e56a1d8cbb4a40509af5728cf059443d`

```dockerfile
```

-	Layers:
	-	`sha256:42d1ecca1d3acbd14b383943b7e29f9419e09cb207afa25db73d727a34508b6a`  
		Last Modified: Tue, 26 Aug 2025 23:44:55 GMT  
		Size: 4.2 MB (4164109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c30b21be85b78ab304a8de70591c955ed3fd2dff9884e52cbdfd33a34738bee`  
		Last Modified: Tue, 26 Aug 2025 23:44:57 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:281d28160e8d61a8beb0ff68a4776f46ae543df8017605915839a9912c10b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324450316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8476f5a9cf8ca360f0088145b541c7fa5ad2b36badedd6ac550b41449f7715`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de201129545c2c712807a1483160b2949306b218e50b47ba5cc54829a3fdd91f`  
		Last Modified: Wed, 27 Aug 2025 00:40:58 GMT  
		Size: 298.2 MB (298242828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:17fa536b8f3cae8052150cb76233fa79372d5bf106835cec05fd8c00f19274de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7992c5231331c496951c6ba5bdf1723184603417fefa773af1df69be8964eb`

```dockerfile
```

-	Layers:
	-	`sha256:0285be76be6f571b99179d85102043ec280c3f7c130a17ad43f5181dc969d24f`  
		Last Modified: Tue, 26 Aug 2025 23:45:02 GMT  
		Size: 4.0 MB (3968985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b249589b9fd2ec6d725b13f5b951a066f8914fa75cfda835b589cd446fe2f`  
		Last Modified: Tue, 26 Aug 2025 23:45:03 GMT  
		Size: 13.7 KB (13725 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9305b07550ac721195dab1e3b3c011bf5fb75f430c97666cac69ba021e61374a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276314410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e73f2571ca73ef97fb0711dec4da23d25d13f25f2f19569b72399349502eefb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0835c128e52a991f492f5d4db3f5659ad0ec42a496fb6e3b1e5e75c01d2f3adc`  
		Last Modified: Tue, 26 Aug 2025 23:54:39 GMT  
		Size: 246.2 MB (246178366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:9c8e12cd90666e97537e575925d1e9e6bece3c1577dc8fd1274648343624ee9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4269094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88fe084bcff0641f19d4587fbe1a03c30101d690e3f3b8407efc4189c2169c5`

```dockerfile
```

-	Layers:
	-	`sha256:6b5b3cdf6ab6dabb40b41da3a54ef9a1d296802e4b7a4805d61df6fd23a16b23`  
		Last Modified: Tue, 26 Aug 2025 23:45:08 GMT  
		Size: 4.3 MB (4255325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c219cc578f46c09d0e8945b3f79bacdfc3b4dfe6d69baeb9fd103917384c5a5`  
		Last Modified: Tue, 26 Aug 2025 23:45:09 GMT  
		Size: 13.8 KB (13769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:df4553ee9b8d52c18718761624861f1ef1035036c2978ec7bab04b27314dd563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334821801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985ef45e68f41ce67ed824e2ee79f46b73acf34ec71db1c7f8ce0af963bec972`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387af528e01b19fad247ce195e775d5cef08b21c75f0487a2a000064f10f977c`  
		Last Modified: Wed, 27 Aug 2025 00:41:16 GMT  
		Size: 303.5 MB (303532423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:be399ce1c0f5f9d209dcd31a5ac778a11b2fd41095cd71530bd310829c6754ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fed0c68dcf006c15336f4267aa2d735cf9ae93859815fff44740dbf61633b64`

```dockerfile
```

-	Layers:
	-	`sha256:f238080b329cf08f8b89383258b64a489a9cde3bdd38feb0442e515eeb4cf1f2`  
		Last Modified: Tue, 26 Aug 2025 23:45:13 GMT  
		Size: 4.1 MB (4137622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c963c710c85c7957f3185da78051a490bdc9531a9be4734efc8075d86643d1bd`  
		Last Modified: Tue, 26 Aug 2025 23:45:15 GMT  
		Size: 13.6 KB (13566 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:b5af61f8062103ada7415109c011eb1825a9c02fac6df520aa23c4223e36a936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377083202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73e48bfbab191e79a4db6850ffa78ba80ab8dd3903668b73c5604056f0377cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d45055bc3a3955730e2954da735d1d4beb457305d3e9a9e1c3cff662f796594`  
		Last Modified: Wed, 27 Aug 2025 00:40:55 GMT  
		Size: 343.5 MB (343488989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:57c7e7c1f7d80b14a3ae38fe20ac889be19131e9c9629d36a78fa97c3e0a5de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a983ad4e05e9965d91d43a99481f98edaaf1d1c2de62fc6488b6ab8196c0b03`

```dockerfile
```

-	Layers:
	-	`sha256:531b736944bdf800b7566c0bfaa5626dd8a38cfc2d984415c1361d33f6145948`  
		Last Modified: Tue, 26 Aug 2025 23:45:23 GMT  
		Size: 4.2 MB (4159257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f14e8f743db92c7a167a39b8e01eb2209efbc589dc4c265a2dd58be237cd175`  
		Last Modified: Tue, 26 Aug 2025 23:45:24 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:b666ff375499950b38953a06410a0bc9828c3ee6a3278c2fda43ae08f2660b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367811574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e93e67a27df4760ae95c91e71a9740cb6667ea5d9725d80814a924521a122f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63acb2145e2e667dd8d17046fc6e3728a6b2f7a36d3d44bd72d38c1d500d52e`  
		Last Modified: Wed, 27 Aug 2025 00:41:58 GMT  
		Size: 338.0 MB (337978517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:63edfb6b0e4b4da47c97d3d1aa63737bc59638b37cebf3c3138547b0601daab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ba06a6ff8549bea3f7fd90b1edc2dc5761028fb38cca1aae849e6dc9a572c3`

```dockerfile
```

-	Layers:
	-	`sha256:ed005d666c5a93e9fe6e182830876a795d33a26e6e6b31fae5c9e376215815cb`  
		Last Modified: Tue, 26 Aug 2025 23:45:28 GMT  
		Size: 4.0 MB (3981857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7546641b9d96143b944435aca85c1c801366386a05b9560746b5f309e214a1cd`  
		Last Modified: Tue, 26 Aug 2025 23:45:29 GMT  
		Size: 13.6 KB (13617 bytes)  
		MIME: application/vnd.in-toto+json
