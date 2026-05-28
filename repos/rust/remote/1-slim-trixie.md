## `rust:1-slim-trixie`

```console
$ docker pull rust@sha256:26abcef3d79b8d890c4ceb17093154573e1f6479cf6dd7c1450043b8458350f6
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
$ docker pull rust@sha256:90a8054f9939fd720f75f428cc9a4003020c0a9d257f763dfa6a5b962c940f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.4 MB (320413827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f474c709fbdbf67d851441a75952c5a66532ec6f6b75287bd01e697720dcd496`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:48:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:48:45 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416f65722211687d2137a8084259f0f1f62c89f8d6912405f2b716ea8f7b64d0`  
		Last Modified: Thu, 28 May 2026 21:49:29 GMT  
		Size: 290.6 MB (290633901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:7b012c593f04350403ccdc7cd307eba253fcfbd270f4afd49a1e12be6ab36c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536ff2db7455cbeb99e15efaa6c162c65df98d0f00d93350af2849482a658c36`

```dockerfile
```

-	Layers:
	-	`sha256:51347a5480f4b80997b07a2bbfec49193d98cd24ac40a6e6e1dd1278b185a9e7`  
		Last Modified: Thu, 28 May 2026 21:49:23 GMT  
		Size: 4.2 MB (4165181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67cde6295abf0f9406b5d0d1668e6fc79d814a92c0fa1b13c1028fbac5a2f83`  
		Last Modified: Thu, 28 May 2026 21:49:22 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:c6fa18b3663dd1f766708efbbc2e1364f4ef79d5ff70069f2afb63666214ecc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334267956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b97b3c37516b3f3ed88cf42140331db492bf361fd3a4ef156d13064c9841f90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:41:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:41:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:41:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee547d7fa56c627822401ddd185212c9218ec7e52d30ee28afbc4ea51f1543`  
		Last Modified: Thu, 28 May 2026 21:41:46 GMT  
		Size: 308.1 MB (308062125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:9b8ac612bc7dd61f03194127269c5cb73ace37b036dd340651d8d2738e90ecd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a662d7c9c4f1b69786729fa50791c25604cdfbcb80d8a9fe2e05bb3b3ebde0a`

```dockerfile
```

-	Layers:
	-	`sha256:3fbe6331647e13b7b09648c18ca14d770708c4b0da278e88987c949c1e9ca56b`  
		Last Modified: Thu, 28 May 2026 21:41:40 GMT  
		Size: 4.0 MB (3970057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934e26a2570270959c047bd56319d193758415a8fe95e2994da3962d587a188c`  
		Last Modified: Thu, 28 May 2026 21:41:40 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4e95154ea3475b14efd687f423f97bed992a484e7c61b18d3c3086ccc5f31306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280032290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d1d3e5b2f218b9166a6f029fea9ed3956b281eb4acf2cf64ea002a029160df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:47:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:47:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:47:00 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b262b302f79fa9698508e3a164cc7e9361938eba0d0e412d2b767e4193c3f`  
		Last Modified: Thu, 28 May 2026 21:47:37 GMT  
		Size: 249.9 MB (249890371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:2e7748c22b66da1632d17a6d83a5f9d15e4f0de17adbab65a44508ba92b08881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85128db0183174e607878dea487b586897aa1d2ddf23d3f06510034f81e8e231`

```dockerfile
```

-	Layers:
	-	`sha256:90f179d57d48dcd963588ac34a02d5b39cb5687ba8164eaacb3232f5fe1eb5b7`  
		Last Modified: Thu, 28 May 2026 21:47:32 GMT  
		Size: 4.3 MB (4256389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c381fbd65555734c50bfa482de0f1b2b618dfb6c47930e832f92505d9743764`  
		Last Modified: Thu, 28 May 2026 21:47:32 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:7be7e62dbd0954a32c340afe3df951d75dde2859549b2b72fdd4a8c842b37534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345273154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1355611e542616b62090e6fd05c96b8b200e4721492f1d52d2f98d28e9670`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:41:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:41:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:41:02 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7789adfc86150f77c2b22e075e84be8775e5327485624d0b878ac2daaf5e6`  
		Last Modified: Thu, 28 May 2026 21:41:48 GMT  
		Size: 314.0 MB (313977819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5ac4b9d258fe6b3d277041b652cec13919b893eea7812f771d1b7d0b39774fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c7c727bdecd448cd41b2db1babd26869ed5dd689cef8f34f8a8db9da1cfa42`

```dockerfile
```

-	Layers:
	-	`sha256:5ea9f7c5214a2a704f96c66a9423de05470a13f866678d0998642b7f6a16cd5d`  
		Last Modified: Thu, 28 May 2026 21:41:41 GMT  
		Size: 4.1 MB (4138694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ede53ece93a72374275b791f7552d66f141b9312a03447756704217b6999f3`  
		Last Modified: Thu, 28 May 2026 21:41:41 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:d001ffa5d726176e4a75bc6632bdc8592826b71ee1148e8483be805a24ead017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394707615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be33e98e21d615a81fb529fbd0ba79a021b38085c1f798d557ce8ee866f5c391`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:41:29 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:41:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:41:29 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b87f7531a42367a164dcb7d11ec449e44160fb8ea2f00864f720d37a6b33dd0`  
		Last Modified: Thu, 28 May 2026 21:43:06 GMT  
		Size: 361.1 MB (361107162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:2429920d92cb7e1208b3da1a5431d20d3d2e1a6b8fb2df4cb6b81bc64f68cb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbd802a06d424aeff9805d8d1aff9f7226b57fc17d93371ccea3a0934b2ce41`

```dockerfile
```

-	Layers:
	-	`sha256:d9f6d345f8c8447e8813197e862d221d029f6262bcab06e63821ab80b67f0353`  
		Last Modified: Thu, 28 May 2026 21:42:57 GMT  
		Size: 4.2 MB (4161642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5ef949c5d4fe8dc00acfce805888e19cf58de8fe3aa9812e9ed29bc9124da8`  
		Last Modified: Thu, 28 May 2026 21:42:57 GMT  
		Size: 15.7 KB (15700 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:42fa2b7ffba2f97e9e843afe585d1fba136d63bedfa3e4b441bd957f3c2deabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390582436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee1ae3994132343fe5af92ed73d4871e138954cd5698b1f249856a7f45ae1e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 22:01:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 22:01:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 22:01:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a7c03298947cc0053f0d22b392b960b9510510597c432126ef280d2c15c52`  
		Last Modified: Thu, 28 May 2026 22:13:26 GMT  
		Size: 362.3 MB (362304838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:af26002518718d55c92da93f72829342894c584026f2166e1e0ccd8ff7a16ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5590b16af7c383e0c3f448caa94c5b24a027175858d2a52f9ab2ecce138c37d2`

```dockerfile
```

-	Layers:
	-	`sha256:6308315709a0822251e44d4b1788c0c4cb179c7a2f1dc100bc0a27bd9b61b0fe`  
		Last Modified: Thu, 28 May 2026 22:12:34 GMT  
		Size: 4.2 MB (4239598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed92d9af0a0460535a9f6d9222a9dfe25eb32e7e889e84307d1d7b6605b7480`  
		Last Modified: Thu, 28 May 2026 22:12:33 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:cf48b8855f627904ca5e0e450a8e4e4a554d6183eaf0533af8df42e3b04b53c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377525209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc8ae6dd314dbe33f0e108d3f33486cd7fbe3a67f431bfd160b172d3ab25269`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 21:38:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:38:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:38:26 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d755ee2dddc27c0ed6166b0d0ab58c6996fbadc12426f29bacb12343815c6fc0`  
		Last Modified: Thu, 28 May 2026 21:39:50 GMT  
		Size: 347.7 MB (347679285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:33bb7d7fb75914954ab798d5044f0004d7eca639a044ec59ef951dcea4d54a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec4bcb6beba091421d026e93727825f50bd9505d9b49ba38d7fba37af6d327`

```dockerfile
```

-	Layers:
	-	`sha256:5c24ececd079707fafe86095610da972603f450fec1da9e897e275a21508e6b4`  
		Last Modified: Thu, 28 May 2026 21:39:42 GMT  
		Size: 4.0 MB (3982929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122fd3e2adb74da7d681d686f245f79c789f45b424b9feef9aee497ca128397f`  
		Last Modified: Thu, 28 May 2026 21:39:41 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json
