## `rust:1-slim`

```console
$ docker pull rust@sha256:7ced053d0ec96d243d49a633dd7ee3f25e4055f172a898c8770e8ebc2ef86262
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:9553b8397715ff026f4742266280d2b869de33493dc3e16d92dd8ec3534f6fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314623128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a196e79e4fbbc31618ea373a3e9f9bd7dcee854953803fafb8f07f5f979ac68e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Aug 2025 04:40:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ef421670552f1dbb12574b546209ddfcd18f6e7996cb5692d55e7ef48e433`  
		Last Modified: Mon, 08 Sep 2025 23:45:53 GMT  
		Size: 284.8 MB (284849633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f6bcf9e37e73b2d2a01ec0f0378ce492f829afa29fc21e0c7d7812bfe55a8ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c70b3a668553a0d9d2065bf78298899ce388d1c640376dad6a3affc6b82b6ae`

```dockerfile
```

-	Layers:
	-	`sha256:2061f401d711cf2399724f58021bb0bd40ff61d8366a2c1af6c924dd9ac7c7ce`  
		Last Modified: Mon, 08 Sep 2025 23:44:45 GMT  
		Size: 4.2 MB (4164957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2c60aadbe97c31fa3bc5e7e1cbc89a5e8fcc3731a190cbf3ebf0ff94e206e7`  
		Last Modified: Mon, 08 Sep 2025 23:44:46 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:19e8dd433a2413feb5263d4a7f0f28e3a2d5a9a5916ea967ff4022ed72e1e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324453538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e50656f86488651f62c4a95ac0a3ef44c7619545c9c8cf5e72986d59b73b06e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Aug 2025 04:40:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ad9b8997a1929f3ded3eb66a514d2d26e192f0da94a3cf35d56baec7b598fc`  
		Last Modified: Tue, 09 Sep 2025 04:55:52 GMT  
		Size: 298.2 MB (298245691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ea92f4c4fbd674e696043cbaec8bbc70db76409f5a994eff19910d846120ff73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff548e8dfe654147375672fb78254d2370e22446daeaf0c47089652811045f11`

```dockerfile
```

-	Layers:
	-	`sha256:b4a0d0ebbe79f3cabee07bb2e6c6b8bc6b66c0ff5549311a7ce43dd58a57d5ce`  
		Last Modified: Tue, 09 Sep 2025 02:44:38 GMT  
		Size: 4.0 MB (3969833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1423fce1b3ee5355871cce654719677a9c3cfd61bb791dd2fd5071bf3b94c7e`  
		Last Modified: Tue, 09 Sep 2025 02:44:39 GMT  
		Size: 13.7 KB (13729 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:db8618b62c62103e15e4a30c0a268d96dc5920443cfcfb7429d1f38b4225a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276316177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42265712f1a79f371bc8d2bba60e392da1ae953b511c0dd28d22c4d5f0064b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Aug 2025 04:40:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af92a59dbeaa85bed162a2bd7aca070c1b7884884a3a5ad6088fd5ef644da876`  
		Last Modified: Tue, 09 Sep 2025 02:49:38 GMT  
		Size: 246.2 MB (246179546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4ff04d223a6a1337ddb89a364fbe1c31ccf9b92be320ee92bca523f32c50ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4269943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732eeea4a09b5e655605937144d02118942b6210c4cdbdf502f86b5e7fc20e42`

```dockerfile
```

-	Layers:
	-	`sha256:83393b95af7cdea46f7733e757215d26df0816e9abedffe6a584ae31b0a19ea0`  
		Last Modified: Tue, 09 Sep 2025 02:44:45 GMT  
		Size: 4.3 MB (4256173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ff6bea773e2640f1060ccc6d84253ed7f33e9aa725a37d26c2909de658a364`  
		Last Modified: Tue, 09 Sep 2025 02:44:46 GMT  
		Size: 13.8 KB (13770 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:97935bc68bb816b49d7fa5f82df16c788713bbaf9106a80603a302f9cdc3702d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334824488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7191cdb1596637925130da308bc3ff6554c0a85041a90e1eb18e8ff440ac22df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Aug 2025 04:40:18 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eece2e71f85f54035da71a95f0226625e0395e60e8d6e0aa5da5e7d357aca9`  
		Last Modified: Mon, 08 Sep 2025 22:11:14 GMT  
		Size: 303.5 MB (303534704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5739fe781b055ea8188c3f7ef105a412df37859a79c4822eb0f4b733b2c39c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23ec91e3c070abc8f595ac44cc618bb951493689067011fa68dc535ccd15322`

```dockerfile
```

-	Layers:
	-	`sha256:f375185afc83e0ac4e10b89f1490f0e85ad45dc75782eb8b0396ac7ad48fad1a`  
		Last Modified: Mon, 08 Sep 2025 23:44:58 GMT  
		Size: 4.1 MB (4138470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8372f43a3deb883ec3fee634a61be2e346306fdacb4cd79deab41c5db59f6fb3`  
		Last Modified: Mon, 08 Sep 2025 23:44:59 GMT  
		Size: 13.6 KB (13566 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

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

### `rust:1-slim` - unknown; unknown

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

### `rust:1-slim` - linux; riscv64

```console
$ docker pull rust@sha256:b9e14dccf6efe6b8c190fd91809317f58399bb051d9f74b9951675eac2857b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381560147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd037627f742d7fe0df5ceb6fb79a7935eb0782fb2f1a16b60915c25339aa96e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94c01af45d9cc28a860fa9e935d083f91652da25fd4e55fba6383ac10b0290a`  
		Last Modified: Fri, 29 Aug 2025 17:41:12 GMT  
		Size: 353.3 MB (353288524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:51a17270e6fed0bd5d874035044f34ed2bed0e61fc174b5f6c4b31a259a86df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9272c32656f9d62d196ff5446f70e71923a9585377643bc64c10e7d161087daf`

```dockerfile
```

-	Layers:
	-	`sha256:99fd1700a5a11869e1050324b1a83316e33349e1561d3d3411d05a634baafea5`  
		Last Modified: Fri, 29 Aug 2025 17:44:48 GMT  
		Size: 4.2 MB (4238526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444a100b65108439c2ae5ac1fb7db912ca4761f451a31b67ede1ea9ec0794ae8`  
		Last Modified: Fri, 29 Aug 2025 17:44:49 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:ac2ee2ed23f50bf92f1c6fbb4fb4d5b6ac1ca3f5d9ac343e5f9d4839c144f5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367813458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4db0cc3de2d629186ec0e07201aa42627b8a118214185fa42d6b631b92b1c60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Aug 2025 04:40:18 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 22 Aug 2025 04:40:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 22 Aug 2025 04:40:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Fri, 22 Aug 2025 04:40:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca009538fceb9c04bda6e270da283d45e32cad99d2a4deaee8e9a32f62a466a8`  
		Last Modified: Tue, 09 Sep 2025 09:45:32 GMT  
		Size: 338.0 MB (337980554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a0e6462c0473bf772afb120da24283d5d58f2e01e44c63c3cfefeb10c2f82699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2235b45996e52c988e4ece550a5039b433a1e4bbb7da982f47b7d8b2e600069`

```dockerfile
```

-	Layers:
	-	`sha256:91534033db4a2e07aa2a5fec639c77ba1fbbe5fc80bad9d4d2e6f489bb2c020c`  
		Last Modified: Tue, 09 Sep 2025 08:44:57 GMT  
		Size: 4.0 MB (3982705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce5981c1a90a0e04ae01e64c72c9cb5f342f6b44d19a34583437586bb320ed7`  
		Last Modified: Tue, 09 Sep 2025 08:44:58 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json
