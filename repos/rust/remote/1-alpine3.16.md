## `rust:1-alpine3.16`

```console
$ docker pull rust@sha256:e2a5da4dddbe0b32a97dd89c082740a916a1f38baeef7259c11fbdb34a3d21e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.16` - linux; amd64

```console
$ docker pull rust@sha256:55921a2104ca06df50cee94c631e06696976fdbb493581d24c832cf216c82ae4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263683744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618eedc2cf68112f4c6b16bbae51a5bbb02a86dc24d71079b6a795cd0b4fd14e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:11:34 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 30 Mar 2023 02:11:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Thu, 30 Mar 2023 02:11:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='241a99ff02accd2e8e0ef3a46aaa59f8d6934b1bb6e4fba158e1806ae028eb25' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a2691ced61ef616ca196bab4b6ba7b0fc5a092923955106a0c8e0afa31dbce4' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded8ef5f8bcce3a528ff9355e26495b21eb63ba63d2e37a1e9958d0022e8b13`  
		Last Modified: Thu, 30 Mar 2023 02:13:08 GMT  
		Size: 41.4 MB (41443514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058d2c75740b791943f038d63e878833a4acad7ffa62e6ed4fb597e3878f422b`  
		Last Modified: Thu, 30 Mar 2023 02:13:31 GMT  
		Size: 219.4 MB (219432427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bdecf19938afab341af97dad1609aeec198a44e7d8bf0f19ba25e32d0fa5a00e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265388679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a378a1214b79889e34081e7ec672b1e280a8129cb268138aab376b8d00197763`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:44:18 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 30 Mar 2023 05:44:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Thu, 30 Mar 2023 05:44:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='241a99ff02accd2e8e0ef3a46aaa59f8d6934b1bb6e4fba158e1806ae028eb25' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a2691ced61ef616ca196bab4b6ba7b0fc5a092923955106a0c8e0afa31dbce4' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b36d9b7eaedd15a55b398329b3c688a6505413914e01f6351f043cb4c2ed43`  
		Last Modified: Thu, 30 Mar 2023 05:45:38 GMT  
		Size: 37.2 MB (37190761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541891d89c6fc8d92c9088db7c5ee19a5d0622726800168342544d3ca156cfb1`  
		Last Modified: Thu, 30 Mar 2023 05:45:57 GMT  
		Size: 225.5 MB (225488574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
