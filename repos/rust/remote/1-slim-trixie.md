## `rust:1-slim-trixie`

```console
$ docker pull rust@sha256:76008d647e19925e8f5e8f4928bc2a5dedd88b19ff7d361cb9ffce5cc21ab1a4
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

### `rust:1-slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:715efd1ccdc4a63bd6a6e2f54387fff73f904b70e610d41b4d9d74ff38e13ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.4 MB (320421042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa2b05e991d73434e6475d6fb9ade1a1ba7a632a04b7a54c2f287d2a8a1ec21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:13:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 22 Apr 2026 02:13:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Wed, 22 Apr 2026 02:13:06 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319daaf9025bcc95f3e1c68897fb2d07e488c6e866a6506f442ffd03f0ca94f6`  
		Last Modified: Wed, 22 Apr 2026 02:13:51 GMT  
		Size: 290.6 MB (290640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:e71bd2cd558a36a25928c186235df32e8f9e4915345086a982e9385aedf3047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf1c4a20455ad07da51e9d65392a12f34e3b46ca950bb58f77af844346f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:b51ec9f520abc958d586b2b3c2ffc614dd391f5f68a730ccf9166151fe384e21`  
		Last Modified: Wed, 22 Apr 2026 02:13:45 GMT  
		Size: 4.2 MB (4165139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865445a9530919c89cc651b3c459a60eafc45fc1cc23dc4c1b22e370d47f3c59`  
		Last Modified: Wed, 22 Apr 2026 02:13:44 GMT  
		Size: 15.6 KB (15632 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:4ad148c0d2e68403fb8c819da811769f60f8369c845270468d55b0817df4d490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333356526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b6d84df4ebc0df4a69fd4252899b1ac50233c787a195e879ebb67d8eb7224`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:31:11 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 22 Apr 2026 03:31:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Wed, 22 Apr 2026 03:31:11 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfebab29173707ec8cea6e5271f97707d48f34010d1cef8529c18fa8f6dd359`  
		Last Modified: Wed, 22 Apr 2026 03:31:56 GMT  
		Size: 307.1 MB (307141688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:3f48bedf9ba0424585c8a0bf1eaf1113b5b727bdcee84ca56ea594379d4943c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06ca8bb098003249ae90511dd0950042e5a1349e3d8d2f0d1855b9171edf8f0`

```dockerfile
```

-	Layers:
	-	`sha256:2895721427abb4a65624c9404fdb273f65af715ceb402aed4dc224376c2eb508`  
		Last Modified: Wed, 22 Apr 2026 03:31:48 GMT  
		Size: 4.0 MB (3970015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b408d6d04cfe4ebcf63d88b01c25d7d0b0c10fba9119dc0be756e22aeca8ff`  
		Last Modified: Wed, 22 Apr 2026 03:31:47 GMT  
		Size: 15.7 KB (15745 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0efa5b4fa317de37803102856e83251bcdc2eacb01160fa5e12aba06a5953172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279320590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbff6cc0f8fcecce6f3f5927f0ec4a4e56e9de7cc4c0b05b3026f1701b08da9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:16:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 22 Apr 2026 02:16:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Wed, 22 Apr 2026 02:16:18 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3a298412af62f3362bf590768d470414b349a49d3de93f904e9309437dafed`  
		Last Modified: Wed, 22 Apr 2026 02:16:57 GMT  
		Size: 249.2 MB (249176984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d25b24c5f1e2d2d36d702b3d1c36ba9b14013c58f7dbc7682deb4540fc9cc695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe3de78d9effd947b5b7a17563dfe2745f19d767bfe007c24f8bf23d21762a`

```dockerfile
```

-	Layers:
	-	`sha256:19a29cf49176fd87669915cff45f950269d6634b0fb9fac9f3d745c1c1619966`  
		Last Modified: Wed, 22 Apr 2026 02:16:51 GMT  
		Size: 4.3 MB (4256355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33917d578c763a053b37873f32b948366a93690528a508ec7fb2f2e41ea2774a`  
		Last Modified: Wed, 22 Apr 2026 02:16:50 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:4c14d8c9dae6b017c140d993ef7e0c5140d4129606e44e4f8debd436347825bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347406715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282910a12e12a553e0804e8a46ebfde72736b8493f3192105495ff126c7ee616`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Fri, 17 Apr 2026 02:46:11 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 02:46:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 02:46:11 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3ebc45f083c1161aef5ffe8d10c4da169bdea91374818173ec188497a11616`  
		Last Modified: Fri, 17 Apr 2026 02:46:59 GMT  
		Size: 316.1 MB (316115463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d9026be0ac2c87532ab389825b45e6bc84d6e98a1413f0f4ce6cd4723114ca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087e4b811adf3815f2b6ebaff5315b76bdaf298a9091544fea0b8f76f68a8771`

```dockerfile
```

-	Layers:
	-	`sha256:4fe4006d14e725295ab31f4d8dd66e8719c4c18ddf03a62975700ab471fc9cad`  
		Last Modified: Fri, 17 Apr 2026 02:46:53 GMT  
		Size: 4.1 MB (4138652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472b19fddbb70b9c52b2269831451df0c0f387f38420654ff8bf3344c45e22ce`  
		Last Modified: Fri, 17 Apr 2026 02:46:53 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:0143d2ad827707fa2def869f5d74ff9630120a8ec30c6bbd807c62d793da78b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397116009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455e3755143831e19ffa3876f408e2c32c056db76b9100ccce08cc1c2fb86ded`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 17 Apr 2026 00:05:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 00:05:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 00:05:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961210ca7193014d9c55c06ac25886984f7a63123a5fb7c3cf9a488f793f53f7`  
		Last Modified: Fri, 17 Apr 2026 00:06:45 GMT  
		Size: 363.5 MB (363522993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:79454ac4c7e85cef25d6040989dc2bf722390667f03e3089b1184f522c851afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3e4a5f019380bc94b096db05d52960ed7362e8b36cbe8f62626d587da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0df9c36ab541983695d4cc449e969696180ca43a01259fdfeb0b3c692e419c9a`  
		Last Modified: Fri, 17 Apr 2026 00:06:32 GMT  
		Size: 4.2 MB (4161600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee41e2cd68cda03b3988d48eb87d5e06469cc88f4f77af8eb101a9b6433f419`  
		Last Modified: Fri, 17 Apr 2026 00:06:32 GMT  
		Size: 15.7 KB (15700 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:a0095e63f1dbcebdabc1a62552a5d40148a23fe2a9528056ee6d6c238bd702a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 MB (392244054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b711059f3dca0d4e1588337619f1a938145b87df22540eb16b8bc879999bfd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 18 Apr 2026 02:28:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 18 Apr 2026 02:28:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Sat, 18 Apr 2026 02:28:28 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3f62207328abcc472350cbd9ecccfe69d89ac94e2cc3bfe7d7365a8b9e622`  
		Last Modified: Sat, 18 Apr 2026 02:40:05 GMT  
		Size: 364.0 MB (363968276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cd1c72c78cedc0b60c0ca94f6292e0b94479ce88d5b6c8c321734b550f59deb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862d1ddef96014f46d42615d4c714abf7242b4835e9c2950e5cb842ddced88fe`

```dockerfile
```

-	Layers:
	-	`sha256:ea23024ff3ddf37d78ceaa479518b3ebbf4e0c2660d46b0b5a1a25eaa4b69186`  
		Last Modified: Sat, 18 Apr 2026 02:39:12 GMT  
		Size: 4.2 MB (4239556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e506ce1fa113ef134df1223501efcf15d54aa99e93e5e132aa77c344736a09a2`  
		Last Modified: Sat, 18 Apr 2026 02:39:10 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:8d889000f14e98634f7c0c490beddfc51c2d7f06551f8f1ffde093fe6faeead6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379279356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5892d8b97a01ada762b013bb5eab9895f361ffc738e9e42390f0b02a9f05446c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 23:55:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 16 Apr 2026 23:55:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Thu, 16 Apr 2026 23:55:21 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce7e87827dd3ef7cdde70a990703dbab32c068e92399668df511b4f1a3a1d20`  
		Last Modified: Thu, 16 Apr 2026 23:56:52 GMT  
		Size: 349.4 MB (349443938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:33e3f42b9b8d1a1a4dd93363b74d6c35690d955fff4f9cf4240a9918529d3f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b7e04fe1addf0366cff19c048bc7fb6471116bfc9f3455ed74b20e9632be65`

```dockerfile
```

-	Layers:
	-	`sha256:bbf7ccb95f3c996676a0e471494ad9ccec126034a8a67652a967632b0a7884d7`  
		Last Modified: Thu, 16 Apr 2026 23:56:44 GMT  
		Size: 4.0 MB (3982887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50176ed9336d6d1044c6f8958971e1c23f5cff122f44e35d68ba3ec0f5b4e687`  
		Last Modified: Thu, 16 Apr 2026 23:56:44 GMT  
		Size: 15.6 KB (15632 bytes)  
		MIME: application/vnd.in-toto+json
