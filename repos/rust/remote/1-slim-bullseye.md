## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:eca54108db942b7003a5753cae5588004d0f06e9df8a9bad9e28af17dbd8a8ea
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
$ docker pull rust@sha256:5ba472a305ad385516fb593be84ff04fa732ffea7bda561db39651b8b078bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304491942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d16f458fc85fb81788fb9d4d09f95a51336d56471c9168c0ee6875e8c2225b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 12 Feb 2026 21:51:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:51:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:51:21 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d016a781057092885ba4da34592dce66e5d366687fc09a6e22673f956bc018`  
		Last Modified: Thu, 12 Feb 2026 21:52:02 GMT  
		Size: 274.2 MB (274233658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:40a99c19b7179f373a4173b6a4faa0910ac5cb4f348e290b27746e3c23fd5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3204ddebb37049686467c1cd49b7682044a58c000452947f8045552248c73506`

```dockerfile
```

-	Layers:
	-	`sha256:b4e09535189a3f73abb096eac0ea3dc02c4f2594a76c850df11d9e16b20f48da`  
		Last Modified: Thu, 12 Feb 2026 21:51:57 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989e8d5a7fca657708c828f758ccc66e529682b95a2a3690aa3a95ad1a755108`  
		Last Modified: Thu, 12 Feb 2026 21:51:57 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:41ce6b03f8063ca12649eb5d436dd945de1dc967110df05c40ccd9382f69c9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324461347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2a297a14f138d85e3b94580ad4ae0ab881e32357abb967b4e311d2760e6394`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Thu, 12 Feb 2026 21:52:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:52:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:52:06 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d4a60816105cda5c5be50efb8112333fc1c654d8187a6b3d11eec8fcf6f89e`  
		Last Modified: Thu, 12 Feb 2026 21:52:46 GMT  
		Size: 298.9 MB (298915238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fcbb2f716a682db28a8bd906b77c052a9474907cd0dec989fd3f1d1065d2874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be7782660b1d32225eed32adc0cfd984ee11b3142e3b2d28e4b4aefb51f30fc`

```dockerfile
```

-	Layers:
	-	`sha256:ff90964b3d9398eca0780c72c209d23cd42af46888f2d533ad0ca3b752087ccb`  
		Last Modified: Thu, 12 Feb 2026 21:52:41 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705154fb9f650d26540f01cfc12ba89b4beeaa5f735aea6f7c3eab71ff49847b`  
		Last Modified: Thu, 12 Feb 2026 21:52:41 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8511345965a6608f16c310207aa99bfb6197419a4f64e09f1b034dace00e4650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264662397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557af046551386c8e937220b9b28c3531f18117c72413f13a089c3847288233`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 12 Feb 2026 21:51:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:51:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:51:28 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2051e430901306ee62022728036a5390a40b266ac083c1dec7080cb3ed0b8c7`  
		Last Modified: Thu, 12 Feb 2026 21:52:03 GMT  
		Size: 235.9 MB (235917958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7ced4502db8351c73361b30fdacecaf1e66fa208cd8b98899d9b016f20443225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0b1736fc4f0d9eff10a57559ed0cf63ebbcf1c87d5777f08d2a9c45866ab82`

```dockerfile
```

-	Layers:
	-	`sha256:0015d4a6d75b39aa209d949a46315eff3b24d959964b6fc31d46b20cb860a3ac`  
		Last Modified: Thu, 12 Feb 2026 21:51:58 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce6141f014adccc66ae7a410653f77a1d36d9bd6607b0623756d81543ed875d`  
		Last Modified: Thu, 12 Feb 2026 21:51:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ec1db230618060aecee1013db933f6cb0ad38ae8e263f1ba68d2ced62baff85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329419436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd1a6a7f758d6c078b020561cca589e2bc58f606e81db407eb60ac504f689e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Thu, 12 Feb 2026 21:51:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Feb 2026 21:51:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.1
# Thu, 12 Feb 2026 21:51:08 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be44e5b8c6651635597dcc56e16b6cbc27fa88aac451d0e6807ab115918f8351`  
		Last Modified: Tue, 03 Feb 2026 01:13:55 GMT  
		Size: 31.2 MB (31191501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceadf1d00b544207f65294aa376c8108b842be5b2750459f40a1eb0e99d90a2`  
		Last Modified: Thu, 12 Feb 2026 21:51:48 GMT  
		Size: 298.2 MB (298227935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e341d8f478d3747fc76fc8a6f1daaae1feaca13ab8535a92eb164913bb656b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceee9575cf59d0edc3a8d72cf6d3756f19673e01f7df3ddc5ba6b96dfc825260`

```dockerfile
```

-	Layers:
	-	`sha256:57acbd2726997adbfaf4c85a2defadf7fff68f3c1c803f9ff8000f53525b330b`  
		Last Modified: Thu, 12 Feb 2026 21:51:43 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e502a2054348a618bbb3dface66c1495ccc5b251991cbfe1fa1aac890500883d`  
		Last Modified: Thu, 12 Feb 2026 21:51:42 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
