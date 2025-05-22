## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:32dcc2fe5087d439348bd1b63c97232830682009c49bccfe80cf768d8cd40bd7
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
$ docker pull rust@sha256:97b80590a20d5c2eb07da85188192a7adef3f4f312522cbfd475c7de7bd82c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295463417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d550ef0b540bad33bf2ec9fb03f2c8e364e5380cd6213c65d4878abf01f3cf67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3b96d50315a23a39f84e3081e1253eab321a691d742d8baa3fc48a80f9ad0`  
		Last Modified: Wed, 21 May 2025 23:30:17 GMT  
		Size: 265.2 MB (265207477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7654398afe6d9c2ada6a00ed784165dda7ea2364aeee0713ceae8da91147f90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2e800891f1055bb4074ed0d02441fe6240edc04c0a2722808deb75b744d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb46c3c2dba7b7825cb14a2f20554b65d85f1b7982e36530088fe6645b473f`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 4.2 MB (4201683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43919c7995c8288c67859032aefa9df80e945eb0051bf122fab252d5ab8603e8`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d7fe35b437a43f5c8b105ef8043454ee8af3135db2b5641fb09c5d055d5daf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316098566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2914d4cdc596581164ceca361033ef369e680fabbcbbe605a68a193cb4db928`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Wed, 21 May 2025 22:28:43 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a7a23f881e3ac735eb288c13345342b8148239a8d2688d5702420649b1d2b2`  
		Last Modified: Thu, 22 May 2025 11:39:08 GMT  
		Size: 290.6 MB (290554664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b258f7c165e9de5f3214e367c222487df3bbb1e05d59df870590eb9c31af017b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ff2f1feab73aee1f330155ab074919959d284d68c3ba5aee7c97c403578ca`

```dockerfile
```

-	Layers:
	-	`sha256:310296341e34a8cc96a786571e3cd18539cb5de46555776710867f540db119fb`  
		Last Modified: Thu, 22 May 2025 11:39:01 GMT  
		Size: 4.0 MB (4009673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25b6fea9bf814c65e49dc13a29327f38f112e959fb6ad202f14c2e5d2196eee`  
		Last Modified: Thu, 22 May 2025 11:39:01 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2907732cdf47a54d11bb9f215f66c880cf6cca6ec0e8a3b93a4fba907ce9bc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258528076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afb3cb7d67a48a06f1caace546ad2ee2a1df2d1af4210b512807ed48c9832d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590353f6ae903422fefc4fa09a0f1bb9dd75ff6b6755395242d7b54c4785b1f2`  
		Last Modified: Thu, 22 May 2025 07:36:05 GMT  
		Size: 229.8 MB (229781819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:00526e50d2c74c3be02296e29306d40260a837b04db15a09e82fd4c4c5fb4267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc445eac70a8b1428bdb51ee46a427aefe0249cc05745a1bda1b00e6459a208c`

```dockerfile
```

-	Layers:
	-	`sha256:791ba0d879ea705a2e12ea2b0fa552e59d0427fe470b816f23c36d0ba8598ad9`  
		Last Modified: Thu, 22 May 2025 07:35:59 GMT  
		Size: 4.2 MB (4198071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a7a2b9b0d6187854cd4153b622fb05e4ccdff7691ecb6a02668ae54ecedd6f`  
		Last Modified: Thu, 22 May 2025 07:35:59 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6c6e66e31919c82fe7ea1b63e8d37f1b3b89a184a6c95c9c4a1433e39d84c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8dae71aa0ae8520f4e956746adc671bfb485dca203c82aa62b3d1a6a45d00c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452460d1c227bf7acc8aeb01051d54bfe06fb359bfc4c6ae3535ea37ea6e2d12`  
		Last Modified: Wed, 21 May 2025 23:24:38 GMT  
		Size: 289.3 MB (289323688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d135ffd369ba51d29a1c421aeea4320644446c924c37fb843458a4188caca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbdf2ab316bec0455185f0aa859a9e62785b877b4f0e81754f1f65734dc86a6`

```dockerfile
```

-	Layers:
	-	`sha256:46da1a092528e79eb79c8dfaac9bdc3cc88154152aa2ad577f97f5eedcea6360`  
		Last Modified: Wed, 21 May 2025 23:24:32 GMT  
		Size: 4.2 MB (4191427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270cf5ab3f0a6904e359a5f16f1ab8ffc19021fe328a31afce493aae98aa5bdd`  
		Last Modified: Wed, 21 May 2025 23:24:31 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
