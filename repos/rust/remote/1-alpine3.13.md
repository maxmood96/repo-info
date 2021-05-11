## `rust:1-alpine3.13`

```console
$ docker pull rust@sha256:619072a6ef5348f19748c6bc10fb5e534abaca3dd6d286f499709ba171817959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.13` - linux; amd64

```console
$ docker pull rust@sha256:594905721611108f35e62cae7b8167e49a3524ae440657ba471a8bc1e18a2e72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236121305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ff7755df549125e1bb5b2ed089b68ea2da298865223342b81501b760188c86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:49:01 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 11 May 2021 00:42:15 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 00:42:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0be8eca5527a01ceab7f038cf1613c804e74597a07cde2e89d3c7bb2bc3d952`  
		Last Modified: Thu, 15 Apr 2021 02:52:05 GMT  
		Size: 42.2 MB (42173846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8915061b65bfdd5509eb7d1e645edae98fa45713d0fb1d07c5d8211badbd5fc`  
		Last Modified: Tue, 11 May 2021 00:48:42 GMT  
		Size: 191.1 MB (191135490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fcf114fef7b0f23d9a2777bb0781229b92f2a4d2bf3b9c86fd6d17d87dc6dc08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230035079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b08ffaa39b29f57e72d3dc4be077626820ae6e126012acf39f6326f99387ff2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:22:15 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 11 May 2021 02:16:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 02:16:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c04c5fad17000f31e76a7eade8ed3ae7ad773e864885771cae105a07c9c65e5`  
		Last Modified: Thu, 15 Apr 2021 07:25:07 GMT  
		Size: 35.9 MB (35928255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66cbdd9afda988c006d78c4257bffd6bbde1412a57ce6d85a74bbb1e0073f1e`  
		Last Modified: Tue, 11 May 2021 02:23:36 GMT  
		Size: 191.4 MB (191394798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
