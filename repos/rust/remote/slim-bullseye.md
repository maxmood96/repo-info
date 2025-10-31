## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:511c91223741697cf68aa071b1d676f1545ad354760bb2a6f9ec65b4efa2450d
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
$ docker pull rust@sha256:532c9bafb504801211101abb4e38741bf310e674b45ba05fe837a0c48b18093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301490013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375eb8ec7a7a87934ba8adca1300d377595f58bbbf6720a63077f2c567e43e17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95330b7f3a0a801883f9715ffac7f513641a9c3c181e15460a2979b4e7981877`  
		Last Modified: Tue, 21 Oct 2025 08:48:23 GMT  
		Size: 271.2 MB (271231648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:67072e1caa1ac00c1f7896e4cd9c0020bfbf87f34547d25c8406e77ad587f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df21e2a5b857681a8e521b60d9687f161de4cebccf166ef2b31fa12fa8b3bae4`

```dockerfile
```

-	Layers:
	-	`sha256:36dcd507b25119bcc46133aaf8f95f2f4b063ba744c8da723dc4c733200e14dd`  
		Last Modified: Tue, 21 Oct 2025 08:45:21 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5d4b466b9bdcddd1284d82d1b6e4cd805119fb7d12373a0324ad1da312749c`  
		Last Modified: Tue, 21 Oct 2025 08:45:22 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:13fc3a2170515d49a864808c172e6ef2cdb6ceb7d516c49d43f25dc6d7220aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325804399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041264a283725f3e8d0e27bf0c41b94d5c1f7a4f0ad080f4bab768ec221cd17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f470db143d0044ed53ee3c62d37c264ce9347606e374e60113030bb748254e`  
		Last Modified: Thu, 30 Oct 2025 21:36:25 GMT  
		Size: 300.3 MB (300258212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80c8d376c747cb7f8555437910e6c9a1add734f8d43488803a7fbb48d5300c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb2dd69accf11a0b247c6ebd6851c11ca87d48376f5b4c43e55069d8779493`

```dockerfile
```

-	Layers:
	-	`sha256:3886373e00abc1e6f64ba5c91f674e54b4699c88fafb62b650aaaf8da12bec8e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67c0e765b1816115cb1b8753a4b992d18c1f0dbe17cbdafddb31a15734a966`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7ff887fd3eb13d26eecb0f40398028fdc12a3298ef48c8528331016decfb0ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264715851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae94dab2b12284d1f2e92e3e2ac7b56eff6bb02864e3639caa14c43b4390fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db337e821e80e597fa142716f1cb02566d2cf4168196f5f08a415cfb4a249b7`  
		Last Modified: Thu, 30 Oct 2025 21:35:15 GMT  
		Size: 236.0 MB (235967450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f46b8601c7c669072e496b7807335af3362860103487ba6340ac14700e4d2e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3c48bda2928a06b24f54d0c55cb10592408f842b75a6984f01eb69ebb7f065`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b83830f27e4a54af4a4ff3428fe72f6898a17d7e3c21d3a7b6165de49140c`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ce6087359d14714e6bcbfbfdc372aa884d3abeff3000503021a2c3381d0f`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a8c4281836aee33f681efe73b74c2fe608821ab8a79e1e4f53c408cbee6a616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d16d04c4e9d940226b9321174f5ada41cc3046700d8f53b9f75357436b02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8bca4c0d96694e3d489bc0df62c181f63f68bd29966b3d385296b7f25514f0`  
		Last Modified: Thu, 30 Oct 2025 21:35:46 GMT  
		Size: 298.7 MB (298729134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8220d5bc4c59b662f331a750b1c3e053eb553fcf58d971daa7ceda6433fac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee75a2e521250b772ff737b27beb9860a1292184f784af6f4e157e5a734559`

```dockerfile
```

-	Layers:
	-	`sha256:5ee000ac8ab06e33a71014e51eeb45b60c7820fd0d03e45c9fd2b1573f530073`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb44d48fb78f0b88ebc033734c23af5eb6f66040ca67ec8536dcd1a1755ed6f`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
