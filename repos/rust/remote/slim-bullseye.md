## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:915a4826b6111266e53e06f47c16cddebf36901623f0631f2cc10ce5c26022e5
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
$ docker pull rust@sha256:955e6b161e189ce9a70a3176d62bc853df1d45a8ff2c877bcc2639c1334e05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72160f9a4acd420abe48f6f6d762750669ca08d8e16c3612f2aa8e48e6886df1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38e595cdc330fbe56f1cc54e1fbb521c5c78b889fda1cb2553ec996eb7494`  
		Last Modified: Thu, 17 Oct 2024 01:28:56 GMT  
		Size: 244.5 MB (244487378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:913457ace1ef4de84bcd5852f75e36f52b6ec6cb0381db81b057670c1f7a64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b212c9018b48677c88ed0905ec79728757d918f45bb4e41c5f9ac0e6c8a10`

```dockerfile
```

-	Layers:
	-	`sha256:8347c9cf5193ed18506b7d4c96a1dd5a0451c1c9d4c0049fd6c1adaaefe4b7cb`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 4.2 MB (4164416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee600185d29aecb0803b6cd08dc6117b7080dbec62c710fa35ae4dffc674e387`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:649f33f2004e7cf32279d259133d1c887680c82371ca61040be0676de14478f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dea15d81a85919b55bae459fdf9865c474d6a3eeded3a426c223d45f15fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dc5030bdc38ffd749a496abefd5f5e3c43706db1ac4fbe6a89b425b6f565`  
		Last Modified: Mon, 07 Oct 2024 20:12:29 GMT  
		Size: 263.8 MB (263784209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fdedd82265ee4abb67e00cb5ed763bb6b00b1e1a9cff139eb943b524eceddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338ea06da0c03a6090e3a6d0cdfbf4558bd2939605e26dcb73de43f3ae2445a`

```dockerfile
```

-	Layers:
	-	`sha256:ba5dd9365cb77053e5b690af6fb2194be4ea48e4cf45c38343e7917bf11ac2d6`  
		Last Modified: Mon, 07 Oct 2024 20:12:23 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bcc530464af98ed85ff675234211982092c53f113700732ff05ba7b7063828`  
		Last Modified: Mon, 07 Oct 2024 20:12:22 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6a01ab245dd0f9c1c5289854e6bfbf41eda63717a403c2ec5715751e29df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53157f2dc99d3da88944463c603f1435f567f3e51e835146526d5ddc3602023e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5b36cf8f1de6f21df811fbf5e9fc34a4a885fdb4d55f5d99d5d38e9e10aa1`  
		Last Modified: Mon, 07 Oct 2024 20:29:36 GMT  
		Size: 304.2 MB (304248835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:117078f67d65fb1fb6692b2e819225b0028efe02b38e50d365a11fb8218ade4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7528c856c92358d9c7cab5571c3f927091bf38d06d14ae6832f0cdb6a0ea1f`

```dockerfile
```

-	Layers:
	-	`sha256:e585026bbab5521b31de85e6d76a91d424b33a11f16dfc4c480cb11110170e68`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eecb4972db015834bb7865e3b2013bcb5784751739299b04ee1938b1efb82`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 11.2 KB (11240 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b869a05737d767ce7fb7056cf77751bb5a8b8b577dfbc911a05c94b2d3754822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290535137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880359cc690264cb0b553f18917849f5c945bc7ff9fea96ceea4696a15d345f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabfbb638063d13147d4f9a1a5694685c92adb5cf15ae94665eae2cd245e5f7a`  
		Last Modified: Thu, 17 Oct 2024 01:29:49 GMT  
		Size: 258.1 MB (258121307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e7bc0dd978b6918b697d54b2322bd89a8fc2364017dc1354c01927066ba886ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222bd0ec93f4d3719cfa3e3ebd12b938ba155acbede32405b0b9551d71c0e27`

```dockerfile
```

-	Layers:
	-	`sha256:58a6810008287c12bb6320144c20f384550200c86b54ba7c87a2e079a24c5263`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 4.2 MB (4156184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b166a715fea1c9ef90fcc577433cc2762aea86d09168615d781dd8d5e38012`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 11.1 KB (11146 bytes)  
		MIME: application/vnd.in-toto+json
