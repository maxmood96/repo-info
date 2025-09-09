## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:30673e1fb79a95d8dfb016827f9766ca75f25b93e2cc0b745d1d8b4d425a6d4d
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
$ docker pull rust@sha256:f4f7e3c3c5d5f794b1d9ac249a6c49c0e0f5afca4b3fd7acb9e38bcace1e17dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299832133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2127295da49cac3c9a0b820324a2ee7bdca86c55f93c71cae2bdf0f863429895`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437202c0fbda70687a1fee7ef241eaf8513a16a8669cfe0fe3ccae6ea890515`  
		Last Modified: Mon, 08 Sep 2025 22:37:25 GMT  
		Size: 269.6 MB (269576065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:45ced725ec1eea50230b8133fa9ce651bb043a1a2ae312d6181a91ae232164e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f35d1f99cc8352013ba258c74ec85f4e0e5e0b8f01b9a52ce02bcfd85da4a9`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f5c47c4dc8d456462f1770f711a2f9c76f7094f8dcfab2ec2a8926c52bd2a`  
		Last Modified: Mon, 08 Sep 2025 23:45:04 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:547d5419e769b65d8450de573807ef98c1317bf0f69080b89d68c8625531f804`  
		Last Modified: Mon, 08 Sep 2025 23:45:05 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:056deab4d006dbedde3336b534cc0b99fc2f7edb026ed9a2dc8e6befa901e60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 MB (315791030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266737bd4f410276a4b4736468122d497b4a17aa79f012d5f14f40f6015c9ba2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dceb61d5a0cd40a4fc7b6629327699f80e4e3781a42d496ceb2c4934b0fe8523`  
		Last Modified: Wed, 13 Aug 2025 13:01:30 GMT  
		Size: 290.2 MB (290246913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b09c11c859d53582193bbf2a47760c8987587f173f5609693a535f8a4cb63370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1db04d2161e401bc219bfd4da915b03a2a7e307c361cc884ae3ec6695f8ad6`

```dockerfile
```

-	Layers:
	-	`sha256:d2e755b4273dd05505378bd98ce7157f4da674ae01511926bbd2d9139851ba20`  
		Last Modified: Wed, 13 Aug 2025 05:44:32 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be599b526986fb3a14f4af02bea8dd95dbbeb2397eae1c50d92496d124760230`  
		Last Modified: Wed, 13 Aug 2025 05:44:33 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d12cdcd25cc06e8acfefbb4532b63121a4c4a6f394932f73fb2f4067c23f766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260974260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d29d3c3f8a5294044ed06d85dbded35bd8d0e08db1d7503b4abcb0f39d41ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac61d04e50e2f4702fe5c5d00ec7eabf2b63305ea36fcd3177c64ad69a07a2f`  
		Last Modified: Wed, 13 Aug 2025 14:51:49 GMT  
		Size: 232.2 MB (232223769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:559b77ad8779870e8245e7a1586800e078a851071214c9b7e6f1ca46b0efad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9f8e678473f30172076fcc9244531a8db963d4cb5d4eebfa3488a6fedc580b`

```dockerfile
```

-	Layers:
	-	`sha256:aba284a19945289693242bfdafb401fd6c042281793ee1a52bb090950f6e6ef4`  
		Last Modified: Wed, 13 Aug 2025 14:44:36 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0000cd2ca3501f0499c3f18e2c2e749fa2bb7e71f54c4b2a28572c2b8e0aeed`  
		Last Modified: Wed, 13 Aug 2025 14:44:37 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8605da440d2f17a761873f361363cb4f6a04d0268daf4fe1a34ecec0544667f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322996925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadf29a9a21a5f818a25978c875e522a8cde5a8c5f1f37d2d521950d46dabf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Aug 2025 14:12:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f000710188b00f8cdc72241f34c956ada0679ed3e9fe2689e605404fa0930b8`  
		Last Modified: Mon, 08 Sep 2025 21:24:20 GMT  
		Size: 31.2 MB (31189738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60866aafb7f849823d5d46065cdc81774f3b2a2b34157b6e54d6398a32b606f`  
		Last Modified: Mon, 08 Sep 2025 21:33:12 GMT  
		Size: 291.8 MB (291807187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:42214799e56e805820b29d8a3949d18e63827b2dc6d2ad1099fe924e20cfd142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04442329e1f0eabfd56b6bd1a69140dd6ecc6a22741ae01f2e420e178b10e014`

```dockerfile
```

-	Layers:
	-	`sha256:0a3de8c8aad5ae70e30db8a01286c51d682699dc7d6d60d5102c5370077b7764`  
		Last Modified: Mon, 08 Sep 2025 23:45:18 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661bf1b0a5580a8cb8a6065fd059992f7898ebe3c6852bf499b170321ce48c7`  
		Last Modified: Mon, 08 Sep 2025 23:45:19 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
