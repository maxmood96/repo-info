## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:c593596210f729542a92aced6a8b0812bcc8d04c5f1b238e663b800d0e2e17bd
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:b1bd9c1f48801b68b585071556d04e4737ff680e5feeb90e585571591236aeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305672436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb27ac28d506a692188e106bd391a48641f12e3714b3922db8ad3bf5df03644`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Tue, 30 Jun 2026 23:41:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:41:20 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2c6a69d039132205a906bf1258d39ecbcd635bdb6dd4745a4e5a70da2cf540`  
		Last Modified: Tue, 30 Jun 2026 23:41:58 GMT  
		Size: 275.4 MB (275412989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8742be5bb56127510aa0f48527fe6cbfc7f8f9907773c269676a3292c82a3c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef545d60ee189739fc18495f185307a42125118c64d3a18e11bce3b180a19740`

```dockerfile
```

-	Layers:
	-	`sha256:385bd03e9b09ad7e8c07aea3dcf0eaa447830106b5c045d00db4c76ff95e5931`  
		Last Modified: Tue, 30 Jun 2026 23:41:53 GMT  
		Size: 4.3 MB (4312026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0e53a84e0827d8e079d76b80ad10d77acd91bf4300a3303808b237c3d1c3b3`  
		Last Modified: Tue, 30 Jun 2026 23:41:52 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:85410247dc10acab254df3997278b10a3b0ce3db8a77710b4775ecb1ad6658a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325689542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f604ceec64b559b96929a4e5cbb0d0f01599fc2f800fd07f735bd8f4de7300e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Tue, 30 Jun 2026 23:34:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:34:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:34:49 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8ec7789c331459e48d19f428fbcbbcb0b3cc1497798c19c3025d746ad6b457af`  
		Last Modified: Wed, 24 Jun 2026 00:27:55 GMT  
		Size: 25.6 MB (25552772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d688f7fde2657890dd7b50e1ac012b1aee318edbe465a5b1062351c794459d09`  
		Last Modified: Tue, 30 Jun 2026 23:35:30 GMT  
		Size: 300.1 MB (300136770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fada9b5917149301e1647482593ad934527c360f8564c2ff1a035795e910f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d118d34d4d25273668537711e2e98ed7c799f2fca0096e22e63cd81192a4265f`

```dockerfile
```

-	Layers:
	-	`sha256:e195e9ba7842d560d2bdd546fc1c9bc6ef6f913c278a5420da893c43ae879794`  
		Last Modified: Tue, 30 Jun 2026 23:35:24 GMT  
		Size: 4.1 MB (4120019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cc26ef00858d9c3d60c3209f7c5a878bd873d2b397370332707bb172274c78`  
		Last Modified: Tue, 30 Jun 2026 23:35:24 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1678a5ec8a5cde36b94420fbccb01f95db59fca7539b4d620396c237f54b5a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264687614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a59da720ac4e574e0fa3ea86896f8dbc0319aa5139c23b31406b655ae4142c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Tue, 30 Jun 2026 23:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:39:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:39:32 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc934a844f5bd88866c27f55e3d6b22dd33ced44051f59285320f9c4bb789872`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 235.9 MB (235940688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b86b22f5b75047b49c05ac4fa3bb5d2cfe35770c436db0086ac234845b5ed823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6252f11ee5ec9e4b21564e24543044b3335093d1333ac53debafd8973f2e45`

```dockerfile
```

-	Layers:
	-	`sha256:8f486fdc210f69297a9ce95e8b052bcd131cc643a17b547ae93434d02e8ea529`  
		Last Modified: Tue, 30 Jun 2026 23:40:02 GMT  
		Size: 4.3 MB (4308415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30e1bedf0e6329cc4cac19e8ffb6520ea51a47e1d08ac6bf488c3e26d80bffde`  
		Last Modified: Tue, 30 Jun 2026 23:40:02 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e77958d2ecf27494389076dd15b31a2f8170dacf01a11c9fa2829d942824b236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333442825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33bde8006564220259c687f8b8f28bf43ba9cc07a18a581013ae96c15788733`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Tue, 30 Jun 2026 23:35:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:35:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:35:08 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:edbad50f4a6e85b8608c496472f5f48b2e108ebbad0ca8f7c81784396f0c79d6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 31.2 MB (31196135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6336bcb9a50b6b8beac71dda008d64cc237515b6ece226be1bab261b960dd27`  
		Last Modified: Tue, 30 Jun 2026 23:35:52 GMT  
		Size: 302.2 MB (302246690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d235abae105d0a04f2ab5aa821efaf6b6d40c0b6ddcbb2ede2a7e18c0ad4d488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9e8e2b63e15036658fc294a15a129cd5152fc0e11217a13dfd2bc3423185e9`

```dockerfile
```

-	Layers:
	-	`sha256:afa0a7bfb63b4168021eee32f615aec57a50d4986b52a615eab29ac1d8e671c2`  
		Last Modified: Tue, 30 Jun 2026 23:35:46 GMT  
		Size: 4.3 MB (4301768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361abc90976ccb84b39926b743b4d2d08197aaa0853f371969581b10bfa643fb`  
		Last Modified: Tue, 30 Jun 2026 23:35:45 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
