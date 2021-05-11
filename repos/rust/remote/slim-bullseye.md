## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:c7c4a891df7f823449c3e2bfcda6e314c68fd44032227550911b7939086ff02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-bullseye` - linux; amd64

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

### `rust:slim-bullseye` - linux; arm variant v7

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

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40a9d825771ba85b3bdca57050a5f0e58aa0cb6403f0da3efc6644c9cb9e174e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278455474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca560afe5e2c07ec7b24c0e183ecb2602661fcfc3fcf54acbeb708cf74b8cff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:42 GMT
ADD file:52386542816793aa41ac6565bc866fb10b7784d3bab5dfbc3bb55624d9de634f in / 
# Sat, 10 Apr 2021 00:40:44 GMT
CMD ["bash"]
# Tue, 11 May 2021 02:13:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 02:15:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f78f5edc1a83a6ef24abc7ff6722c452292a1f4ea954365aecbab9c7fc1861`  
		Last Modified: Sat, 10 Apr 2021 00:47:11 GMT  
		Size: 30.0 MB (30037067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514c46a35aaa07de0ab8b4f1eca990984acd1edeb405dbae37b28532d38cb9be`  
		Last Modified: Tue, 11 May 2021 02:21:41 GMT  
		Size: 248.4 MB (248418407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3742259bec144bb780c29b0c4c724e9c443fbeee95251471931b1ae931c71a2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268028393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7bb4d52d40fbb00c85eb4692f7dd0f75cd2ac7ad006f840d461997c9bb6147`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:13 GMT
ADD file:d201ac3b33d7c359a0ba889539c9fbce9647142726109af896aa8b053cec35e5 in / 
# Sat, 10 Apr 2021 00:39:14 GMT
CMD ["bash"]
# Tue, 11 May 2021 00:57:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 00:58:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='fb3a7425e3f10d51f0480ac3cdb3e725977955b2ba21c9bdac35309563b115e8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f263e170da938888601a8e0bc822f8b40664ab067b390cf6c4fdb1d7c2d844e7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='de1dddd8213644cba48803118c7c16387838b4d53b901059e01729387679dd2a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='66c03055119cecdfc20828c95429212ae5051372513f148342758bb5d0130997' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:baff5217fbd64e583e92ee39435c69cc22ba0b3b14dffcb0f60f4e9b82bf6c36`  
		Last Modified: Sat, 10 Apr 2021 00:45:04 GMT  
		Size: 32.4 MB (32365969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77aa0da9737f77b29aafd75deda350508abba44787b28009d3b94fe515331c88`  
		Last Modified: Tue, 11 May 2021 01:03:54 GMT  
		Size: 235.7 MB (235662424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
