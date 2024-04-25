## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:c559a40cb4afe827a248707c493a290fdac72894807f26a454f2823854c680d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:43ea72d42d2c038ea843c9b41316622f86f5374dc6dfb82a037587761a04b849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e28bbeb4bfd6d136fe79aa0822e42176d77fd24f75c05e8458b105546c898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c309d2cedf4817a559551782149cdca9318d0a6c23018b97523a0fe91857f`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 232.8 MB (232831469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8b95d9eb6aa93d0dc9fb69ff759960ed6ca6dffc91099527b5f001a00f624d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053dac136f29cad1cf8460c926ae37b678819959d2a4d6f351e2d57c76b04680`

```dockerfile
```

-	Layers:
	-	`sha256:3bf84e83a418f557d6b1f21933fed9e3f861d44845045ea89e0dbcb27c9bc330`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf51e74c2bf86d87b3bd5677d94c687071178480fd648aa0c64a816c4ed6e0a`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 11.6 KB (11630 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d87bd027a2ec897941ff0f691413f27f6ab798f47ffd1c6954fd687bf58928f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859469ac3ba60ce123589a9d56e54f17c194a61ee18931acfd7e3133b2aec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54685378a8d57ac36e4ff6a2c342ac52809f585a7d4c8fb662229230e65ce`  
		Last Modified: Thu, 25 Apr 2024 00:15:07 GMT  
		Size: 250.7 MB (250681610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3ceebf9c5462589e2d813246b8a8b6852d230b823549fe33fbab50984fca842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8625ff2e32464e91cc3d770313871c50321ca890b2a17a4e0a2092840860cd`

```dockerfile
```

-	Layers:
	-	`sha256:f5d89aa7dc719b61e8b5071c3b29c385557d01a1d8ded536e3e3559ebf05078e`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9151d79ca50c92149bee7df68a8e9b97ed397aedf889f6cbd71f43a42f9f1d6`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 11.5 KB (11533 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5e93b701f3f0ab84b99cc927ae34c580ef3ee3de75bd19fad5da6d51efb87b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327241674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50378ce9e74de9ce3b5dcb5dd9594a2c86c6945f2492dffdcc18a50ce8c577f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d911f3f952c405465816aca5420841e93889b38f2ca31db6fd0c5bf9a937d6c1`  
		Last Modified: Thu, 25 Apr 2024 19:33:11 GMT  
		Size: 297.2 MB (297154338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:03eb33f2de7d934a9ef4709a8d0fe60b02c7c2e485f70ae9e1fa846b64e502ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a80db7b87d85ab4420a9e10e771fc01f031d2b9d575b67eeb92a067d9fcff8f`

```dockerfile
```

-	Layers:
	-	`sha256:16dfae4cd89402181697e395c2a82124d1775686189eb286cf54379bfd8d94b6`  
		Last Modified: Thu, 25 Apr 2024 19:33:06 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba8f2e5d2812d8820176b411a10c50587a4427981713371964758f5d702a934`  
		Last Modified: Thu, 25 Apr 2024 19:33:05 GMT  
		Size: 11.5 KB (11473 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9d5d2ddfdd6a58b18bb7f0b8e5f8f37047f9ea8f1e2aa50dbcd4977bab58cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280018615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbfbb115c7bc121e9f0e8a7827e251c41349a8bd1984a1e769d5c0374d67939`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37221a01bece8cf821897f51b65bd44350746155d325214a918695731a66d3f`  
		Last Modified: Wed, 24 Apr 2024 05:12:24 GMT  
		Size: 247.6 MB (247593842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:790c11b457e330245a08ee08368b80c4f9ba2376cd04a83d8c1281b66b8c95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aebfaf8b74b4087da8d50d05aab6f15d452168841659b66338f8cdefa27db2`

```dockerfile
```

-	Layers:
	-	`sha256:7ded81c8554c4a76e11a1920802c6a674e41a6c19c84a7a708cb38fde0d159c8`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86498619bcaaa39fefc2150c322446a6fcf7367d267078da6811a589fe3d3977`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:d1fbaf1eb7c480f19373691dee46b7333091e312a0067cfff60e4f88125b1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278620161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0eb2329b60e7b7a4c321b3eb186e7e8291157920a4c927c5b1239dcd290362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effd22b3d858125536254bd2d670cd1a720ea963a5f5b9a6295f1cf04c849f2`  
		Last Modified: Thu, 25 Apr 2024 09:35:52 GMT  
		Size: 243.3 MB (243308436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6c908c45ab479e9a650293593a45d8210151cc0acedb0d2b98bd1874afc7b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca374cdff5e57bddc8583419f72f992120d629a52de5d00744829a915b1da9`

```dockerfile
```

-	Layers:
	-	`sha256:409c6f41b6182bd1869c433f7aab4744d5fc0538822f779fc042144d994129ad`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f597651f5972b28de5ed540ee23e227c15cab9910914b31894c8c48ed893f`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.in-toto+json
