## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:e17d08fdc087534d545ed9a4b2f466f59fc45ae7c00ff71e991e7ce2f62ba513
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
$ docker pull rust@sha256:3f8d03edd149b07ea3bb05c693b6c7267702fb339c96c6044777433c8591f6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305635767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110b949ef90dace7ace695b4ceb7c6303de08fb2ec97e95da790a8f89ab6b91b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Thu, 16 Apr 2026 23:55:15 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 16 Apr 2026 23:55:15 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Thu, 16 Apr 2026 23:55:15 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c276b078294b4740c8955c6d1e741625b60558c79d4da74aabd35d029d29469`  
		Last Modified: Thu, 16 Apr 2026 23:55:56 GMT  
		Size: 275.4 MB (275377748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:087ef9ef9c4f6d4833f7a241bcf030dec5866ee721746cb09775e0b12a444da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bc1a7184a24113312ef89fcaeea2287d079318194663f7c185d6bab47ce605`

```dockerfile
```

-	Layers:
	-	`sha256:d5fa5761397d3481bff835df384557542f1f19c3501f608ebaca931bf639ad6f`  
		Last Modified: Thu, 16 Apr 2026 23:55:50 GMT  
		Size: 4.3 MB (4312022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3625b28d40e307924482f5d75a6b66e8044836685320d6a5b39c49997c146de2`  
		Last Modified: Thu, 16 Apr 2026 23:55:49 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d4b3a5b0cfb946b92ff06fa4ad43a9e9edfa52ebcb0ca13f4b6c8b57263b3667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324739042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85a04a558c0e06343721442e741e5977238275120204fa67b0881dcc9278d40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Thu, 16 Apr 2026 23:56:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 16 Apr 2026 23:56:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Thu, 16 Apr 2026 23:56:27 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc083f90b0e38b1edd3b6ad7ca63526a89ca8d71a3fdaa1caacb21a07ba44a`  
		Last Modified: Thu, 16 Apr 2026 23:57:08 GMT  
		Size: 299.2 MB (299187554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c169e1c88b854f2ef991925d657accd5e8650fa17c935fc2364fce74a12635bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef61abf2d21baf0af9250bd79b58f99c6839c55c78d9d7324e629e513c33a45d`

```dockerfile
```

-	Layers:
	-	`sha256:d1a8600aad8c2384a49858816219a716a17a830cf15d19af5bab3d4544ffe7b0`  
		Last Modified: Thu, 16 Apr 2026 23:57:02 GMT  
		Size: 4.1 MB (4120015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543df6556c12874d48f7a1269b60ccfcf7a225a054b6a63a8a144e653ef41a5d`  
		Last Modified: Thu, 16 Apr 2026 23:57:02 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a4eff121fa5d9ef3cc600615771265c851c45a10d46ae7c371983e40abc76ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263999544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a13633d8e91b63fd15ebc805c13a7237fe800c7ae9b138a5d1a0e0e8727970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 16 Apr 2026 23:55:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 16 Apr 2026 23:55:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Thu, 16 Apr 2026 23:55:02 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdc2f5ace30818c46ad7fad40b6a3e95b93429e4e28b8ba0fbe69e759b0b187`  
		Last Modified: Thu, 16 Apr 2026 23:55:36 GMT  
		Size: 235.3 MB (235254856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4848404b6e1a1cdc460de445e8852e38db7dc63a3d664fd45d4e84a60e7955c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f2d0851139dfb24484bed17572c4a597014fb7470df84970cccd97263bdc6`

```dockerfile
```

-	Layers:
	-	`sha256:a31ad75e80defdbf8656a94a8ee894a522cab444253e731786f3dd57f32c2123`  
		Last Modified: Thu, 16 Apr 2026 23:55:32 GMT  
		Size: 4.3 MB (4308411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42007d49f54b26fac87ad9036778647127d98ee813e7134eac5eaa333c8c8a9`  
		Last Modified: Thu, 16 Apr 2026 23:55:32 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:4eda8526133dc64ea39799926cc59e47b1371d2381862a698b5e7b75d3691ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.7 MB (332721195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8b5ab37c0a90f140edee1056ef4785422e3b64a89f5f003c84486562b4f166`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Fri, 17 Apr 2026 02:43:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 02:43:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 02:43:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:829e928df5d3a0d826eebb9db2afcfac51736338a5db0631a2852b75006909fb`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 31.2 MB (31191810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842a801ccc58e69c7d89117231e4ac8f0474ffbfcb8e3821ebd8708e36d6ebf`  
		Last Modified: Fri, 17 Apr 2026 02:44:00 GMT  
		Size: 301.5 MB (301529385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c7de73c410d5d1bf040b2705d4ad68b9fb6715d4a072ae1fb92287b02e916820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e532c2682004ec0bfffbf7ba8ce8676eb1373ae289f4cd345bcee76d22baa0`

```dockerfile
```

-	Layers:
	-	`sha256:5a7900088b7a16eb16541b2f5a000af8cbb3e5c23f167667201cd57e2c08630d`  
		Last Modified: Fri, 17 Apr 2026 02:43:55 GMT  
		Size: 4.3 MB (4301764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1303657cb35aeb592deeb8e960d4578d956d54f83539a9a58daa833b4865b214`  
		Last Modified: Fri, 17 Apr 2026 02:43:54 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
