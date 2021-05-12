## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:f054cb72705819f81ffc666006a1b6cd24a01728f8ddf01d4c86e949420ced10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:02fdcb2e91c79191c483263142b5172451b35d7f713fced9d2698b2ff77be45c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226896694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3927f7fee9041f1a305d0461ad5c8888aa52054da443508e1bbe5fbe15243da`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:19:58 GMT
ADD file:355194a9b58fc933fe444d7866cc4a39713a870a65402d65440a2dc357735259 in / 
# Sat, 10 Apr 2021 01:19:58 GMT
CMD ["bash"]
# Tue, 11 May 2021 00:41:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 00:41:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:59d01ccdd87174a9ae0eb936ee6947e974e2b30eaa69a472f92ce378f07176ef`  
		Last Modified: Sat, 10 Apr 2021 01:24:28 GMT  
		Size: 31.3 MB (31347743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d21b5c637b3c23f66134147143a7d339e7a664f771d7c940d90678d204ca47`  
		Last Modified: Tue, 11 May 2021 00:46:51 GMT  
		Size: 195.5 MB (195548951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d8aa8a2c5334a5b26121f740e5553b50366d9dead8e8f4d04618941133f221f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247696318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a509c014195d49058c51c062134c9c568044b0ff0dddc98822a85fcb2dc628f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:58:54 GMT
ADD file:49314be3b948dd917c99b41c532d83ae6749173379fe4a80d8e4ad55b2d89c6e in / 
# Sat, 10 Apr 2021 00:58:56 GMT
CMD ["bash"]
# Tue, 11 May 2021 00:45:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 00:46:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:535f9c9bd2387fe5771446f92b5683c8f2986c9ad78ddfd34210e0dbc8457937`  
		Last Modified: Sat, 10 Apr 2021 01:07:01 GMT  
		Size: 26.6 MB (26552221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b805b387321f0a1166ccb678a6b9eed2e2ceeb09eee1483d9df4fe949d4230`  
		Last Modified: Tue, 11 May 2021 00:51:39 GMT  
		Size: 221.1 MB (221144097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:84f68491712a816ed289888c1f1efc20fb4c8b096d8910109cdba1fc2976066e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278367332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba98431a669f492717c302fc4d8bd254bc4679e299f77cbd273b4e90cda2e6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:50:23 GMT
ADD file:69a37bb5501b4a81091151db1ed36e1cbab011b856c3d80130117c13cd24dba3 in / 
# Wed, 12 May 2021 00:50:27 GMT
CMD ["bash"]
# Wed, 12 May 2021 04:44:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Wed, 12 May 2021 04:45:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:33c353e2500432835925df0c924200953f7cab59e47bdbb7549d04d71f8c7449`  
		Last Modified: Wed, 12 May 2021 01:01:21 GMT  
		Size: 30.0 MB (30038783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d39ded5b948b39e9f3a977cabf2aabbd43bb632becebffaedc3cfec2454ad0`  
		Last Modified: Wed, 12 May 2021 04:51:00 GMT  
		Size: 248.3 MB (248328549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a0fd55759d0327a4ee521434462771a89915dbacdcbe3139da8eff9a57c1a903
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267902258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e42d879039d59df0dcf26a8dff654b8740c9bad2c4bf26f8428a4b252edafb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:39:18 GMT
ADD file:4c6fe51c6847dd9c3ef6d97cc7980550c01edf974c1d34e5999b08da304726fb in / 
# Wed, 12 May 2021 00:39:19 GMT
CMD ["bash"]
# Wed, 12 May 2021 12:50:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Wed, 12 May 2021 12:51:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:97f8c393f679514daae013b4e04e6b0fdd6cf4ba4c91c6450cba666631b901c8`  
		Last Modified: Wed, 12 May 2021 00:45:42 GMT  
		Size: 32.4 MB (32364315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb9f8f91dca78888dd088c08764c76173d5d9b9041e43295e882b6ddf3bf2de`  
		Last Modified: Wed, 12 May 2021 12:58:09 GMT  
		Size: 235.5 MB (235537943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
