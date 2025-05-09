## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:3cd2942a051699ddb419ad5ed00313872bf15b6ff665a4c678c0893efd9e7f8a
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
$ docker pull rust@sha256:c6da0916620f085517fc956370627a516b02a7232b253f81499e55e314666b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294771407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27972dc7782aff598d1dfb771643744e7d5d71aaf76a1fe3cf9372009473055`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 05 May 2025 15:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 05 May 2025 15:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Mon, 05 May 2025 15:33:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14cdfcc43a29efe782f07dab439c915550a4c83c9e9fee85f0d5a81e4269066`  
		Last Modified: Mon, 05 May 2025 17:26:15 GMT  
		Size: 264.5 MB (264516803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:92a93d801caed1cc95724eca8c73d1bd1c85346f6722e59908352e256099e54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae435bf0452c7944e6c76481c1afa37f58feabcc7917f5c33e2e28f37268468`

```dockerfile
```

-	Layers:
	-	`sha256:e823c422721b1b8c0b37c1926a059ef53aa4ff078b4479e77b56d8011b86298c`  
		Last Modified: Mon, 05 May 2025 17:26:08 GMT  
		Size: 4.2 MB (4176419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4a32743557ca60733880bf1d187f61e225b77130ebe1fcbf1b28b5bfeedf40`  
		Last Modified: Mon, 05 May 2025 17:26:08 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b109a4f220aa1944328085308cfac2ddba5513c81f3d77c52bdedda9e0aa25f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313378217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcf09d705bbbc3e859b096fc8ec99c21ff5e1b3d4b159452ddd9e54bddff734`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Mon, 05 May 2025 15:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 05 May 2025 15:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Mon, 05 May 2025 15:33:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42a700fc43973efe6476d03cf60d35df1a160a4ec03723c1a8b794eb15982a7`  
		Last Modified: Mon, 05 May 2025 18:15:40 GMT  
		Size: 287.8 MB (287835790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:612ef7e4dad2ac0c6ce701b3b0d15dcd1b1ad66124abc04010612a039592b112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ba4c0c0083bd264fe161f724b465605ec8bd3c18e4a5cb9a1b3f84684fdcd8`

```dockerfile
```

-	Layers:
	-	`sha256:f0ff865de39862b72a173debf3c5343c1e0df7abe208344261b2e94d6f7a8f1a`  
		Last Modified: Mon, 05 May 2025 18:15:34 GMT  
		Size: 4.0 MB (3985569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf942c36af0364451ca815f37f9d388ab89e29ea8945757dcfb58bf75fe8963f`  
		Last Modified: Mon, 05 May 2025 18:15:33 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b952cd8c7cb5bc685fafc0453675c157b0e7ab60ab4d5cb19f5654e83b0814f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256826543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c148d249c561a66fd63b97f149c5c936c92b00522f66db83b291c9f44d8ef0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 05 May 2025 15:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 05 May 2025 15:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Mon, 05 May 2025 15:33:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64fc11e40a28f7221b1d17b06a175882a71dd647ec387405b4d5a3e3b51c22`  
		Last Modified: Mon, 05 May 2025 22:55:10 GMT  
		Size: 228.1 MB (228081898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:47d1014c495a6a6ee2bde898372e598ac58849f1f86688d70090da92ce6a384a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7741eba43e412b2ab465ba4498aad969b07078c8e86487d3f63fcb3fc49d0398`

```dockerfile
```

-	Layers:
	-	`sha256:6f50d7e6189c3c4dd127c226f9c1d9f50a49f95eecc7d5a0bc1e688cb81a9477`  
		Last Modified: Mon, 05 May 2025 22:55:05 GMT  
		Size: 4.2 MB (4173097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6782b620ca0cc5aa21ed4c3f814075d57dc7f21f7472d30637027661eeec8e`  
		Last Modified: Mon, 05 May 2025 22:55:04 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:5613dcb09ba9335955247d11b1543340cdf887295dc1967c7b1b88fa37554cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319138342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711369e34544e54701f7723455258f5b3e32f3f5192dbf6fd42f18a6c041486`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Mon, 05 May 2025 15:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 05 May 2025 15:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Mon, 05 May 2025 15:33:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7deaf5b431f97c6a834fd5871b0ef3a962b42a29b8720fe94fda84e827206b`  
		Last Modified: Mon, 05 May 2025 17:26:07 GMT  
		Size: 288.0 MB (287950449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:68a7a3ad45589db586b7957257d9d6b81843803a135838d44ea91f12f9218c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f3eb57d7790ad203d01901b7bb7ff0859114b20705c19393d680b11bcde6dc`

```dockerfile
```

-	Layers:
	-	`sha256:523b6b4bd52dd8ecae13fb2f050dc91463542de725b1b1431fe61af3e461dd4c`  
		Last Modified: Mon, 05 May 2025 17:26:00 GMT  
		Size: 4.2 MB (4166676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918b2b62103dce1319a0fcf3ff3746a36b2073b0d52a4bc793ba7b85868cd9c8`  
		Last Modified: Mon, 05 May 2025 17:26:00 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
