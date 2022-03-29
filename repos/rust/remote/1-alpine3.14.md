## `rust:1-alpine3.14`

```console
$ docker pull rust@sha256:dd84941f03f58df790f14f789c5f7464a4d4d32195cec3397db26280ba93abb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.14` - linux; amd64

```console
$ docker pull rust@sha256:f0e391f6d0128d9bd5116332f065399552da2f1345b3dae5a0d6454015b55548
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244898342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a66e083e588427e68d4914757b71da6d8b8f59963ed09bb80d2e353412bce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 16:43:05 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 29 Mar 2022 16:43:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.59.0
# Tue, 29 Mar 2022 16:43:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc4677d930fe6cd528ef025c624dfafd9f875b1a6ab7f775999a5a13c3eebcb`  
		Last Modified: Tue, 29 Mar 2022 16:46:18 GMT  
		Size: 42.3 MB (42340439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9874348178cc5aff0ff80a0f95fdb5d3aa012f91c0d3fabd161337eaa92a6f`  
		Last Modified: Tue, 29 Mar 2022 16:46:40 GMT  
		Size: 199.7 MB (199739549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:57423d7e589e9f6651f8ba05cfdbe5dea60022c4165153f3afa550092cdc831e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a20c8b2bef8bbf4658affe7a7c6d5b53ccaf343c24cc48f4fdd3fa3dfd05ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:09:39 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 29 Mar 2022 19:09:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.59.0
# Tue, 29 Mar 2022 19:09:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b5dae82c6eaefeb109f8baef15acfe8fb5f3f7c6b33a0ee89e16d0e6062135`  
		Last Modified: Tue, 29 Mar 2022 19:13:44 GMT  
		Size: 35.9 MB (35921130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72782eeb17b09ebe69cbea49b779be532d633517f69ef83c2f4b46602936fa86`  
		Last Modified: Tue, 29 Mar 2022 19:14:06 GMT  
		Size: 195.4 MB (195377576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
