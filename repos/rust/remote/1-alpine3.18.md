## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:0fd951162d6e4ec56e3a914d5d85129873b4961f40a122b02a3ed502b1593636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:c5ec773762c368cbaf27531d03242f78feebc3d790387fdbebdaa7a9022d6504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275016268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd89726c597e7f1c057f7146beed68c80aca16c691024ca4f887f007b4f7293d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 15:56:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e3bf2d2d006b60c416b21782bd08d25cd7759ef5fbce14ad74f01c3a6e54e`  
		Last Modified: Fri, 15 Mar 2024 23:55:43 GMT  
		Size: 51.5 MB (51528263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c5c56e1f01a09a5efcb93c03e02ae8521bf955a7f196177cb09cdbbb73e6d8`  
		Last Modified: Fri, 15 Mar 2024 23:55:45 GMT  
		Size: 220.1 MB (220085463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9f62bea469cdccb01530281b2f9401f15c13d36dc820305b8d02356eef342f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.4 KB (707401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57fdee2d418aed846c70e31b75d09faff8c59a1d8b6b1c0f04822e39db31d2e`

```dockerfile
```

-	Layers:
	-	`sha256:243cae8c7a06958273c4382f525fd4ec375d7849c5f48340d55b197fc63f9a55`  
		Last Modified: Fri, 15 Mar 2024 23:55:42 GMT  
		Size: 696.9 KB (696917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d6c5e7505ed63d96ea7e8398eea60b71f2d71c42738baf28df2c4999891e57`  
		Last Modified: Fri, 15 Mar 2024 23:55:42 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e834553e3a9e93ba4e003813d475d1ac1757fb1834c288e180a4d0442d2a6b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279846688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8aca25580b4b0a9580df6250bef7f3a005c40e714f24c9d420df02f978ddb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 15:56:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c73fbb8d9e4fe84ab7fd209062fad97866a9864eaeec7f172ad185e216466d2`  
		Last Modified: Sat, 16 Mar 2024 17:11:42 GMT  
		Size: 230.4 MB (230446968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:0b084fca843fd0d997c288bc37aa18594d74138a6b4d73187b42e17defac3d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.1 KB (747063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94e5cbd908eecf4abdc507b41fafbde0d28f9f860a93e7fc15f530dc759237e`

```dockerfile
```

-	Layers:
	-	`sha256:5a90cf85445118d53f88565fef67b2eeff10013ab144d27b6f7a925325bbbbc6`  
		Last Modified: Sat, 16 Mar 2024 17:11:36 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbb99f7db16e6ca0e5f980e42a818f84603c73b9ba4ec16acfbc90d9351c3e9`  
		Last Modified: Sat, 16 Mar 2024 17:11:36 GMT  
		Size: 10.3 KB (10328 bytes)  
		MIME: application/vnd.in-toto+json
