## `rust:alpine3.18`

```console
$ docker pull rust@sha256:580e63c185054908135077702963a87d88d6914002775d88c03033df292bdce7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:f5762f07bc2d9d6699afb162b7f35dfa48e5945cf4395b4f9b9d6826cb1d3c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5e3a7dd699641a0c6368e65fad736d7c583359096663c1e4bf5e98b85d5a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914773acc6db8be08970614a0ed0f5fce71828723bfcb6e6cf1d97a26c284eb`  
		Last Modified: Tue, 09 Apr 2024 23:50:41 GMT  
		Size: 51.5 MB (51534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0af00c163854d8ec5ea9d8a150960293bfd4aa34804a7a160ef80f44ce71d`  
		Last Modified: Tue, 09 Apr 2024 23:50:44 GMT  
		Size: 213.7 MB (213736629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9bfd12461323300ebd4c975ebc91a40d5949fa914272a2abe34315cac6c58c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a20d1e055b2d8dcd9f1dc20fe467a5b977e5e797847f63adebc0d7732c718`

```dockerfile
```

-	Layers:
	-	`sha256:d549196acdb3131a3a009a32ec149198450da016167ecb17316ed5105a440284`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff0d60c39141b47c8ebf94551e1235d461f65e03b68df4a8ae19688754cc60b`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 10.6 KB (10588 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:655629bd56eb9b41b0f5889f9503e262f17f9f22fede7094f675640984d9c6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271903101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6a49fd843fb0e4c9e379f856ca989187c011cbef2af5e85cbf718654869a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 29 Mar 2024 15:09:47 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
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
	-	`sha256:cf79526e3247d6828219e06b9f875445389e071eb60d5af14461a4ba78907a07`  
		Last Modified: Mon, 01 Apr 2024 22:02:40 GMT  
		Size: 222.5 MB (222503381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:bbcd67f23f2f071f41c3bbdb3f95212da99608c673dadd23cd90a9e0ffff49f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.1 KB (747063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261290853e702b1a2136b94d8847257070b672dd56c35854ad4dea2138366e8`

```dockerfile
```

-	Layers:
	-	`sha256:f319a14cf3f557d43043a2224c4fe2de2916dbe8006113c9b7aba2f2fbafc6fe`  
		Last Modified: Mon, 01 Apr 2024 22:02:35 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093dd89f92087bf6d200d26c5c827b9eb1755205f8256aaa4741bc497c9fce2b`  
		Last Modified: Mon, 01 Apr 2024 22:02:35 GMT  
		Size: 10.3 KB (10328 bytes)  
		MIME: application/vnd.in-toto+json
