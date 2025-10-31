## `rust:alpine3.20`

```console
$ docker pull rust@sha256:55905a107df49e2ca919ebceb11bdc35471b3436d9f08c179c3c51ebf931a360
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:189e41d7ea7385159957443109805b96797a3e8068f68f79623862b947b5a2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327094301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7022ae94d55b53b7fba7a78c003afb18fe60a3ce489a0ba0e54d5118b1166b3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 23:54:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 23:54:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 23:54:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 23:54:51 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b1f5e007aacbb4d0e7ad54f3bae9e97074ed97438f50378f6f2b543b7e58a`  
		Last Modified: Thu, 30 Oct 2025 23:55:45 GMT  
		Size: 55.3 MB (55309692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff293524d66eb80274d724c97d29d61800dd3b9f737ce365093f9515ffa8b99d`  
		Last Modified: Fri, 31 Oct 2025 04:08:31 GMT  
		Size: 268.2 MB (268157553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:bbe59008c45b9d3afaa6b26c934278706bcb65ed391e4a7a39c63fdeddc3c08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.0 KB (721967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2938c605af6d88bdda62458b129432c73bdd047b73686fe86ca597782704f2`

```dockerfile
```

-	Layers:
	-	`sha256:77754d9b6707db430f6834f16c6d22d9d5b3528b540eb4981275bee1b9a04975`  
		Last Modified: Fri, 31 Oct 2025 02:44:35 GMT  
		Size: 709.9 KB (709860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74818e977a8861f2a027eb4904eb959cff18cf1380c6df9add198430d99a68f4`  
		Last Modified: Fri, 31 Oct 2025 02:44:36 GMT  
		Size: 12.1 KB (12107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2b1f24765d5621e41b309cbcf190fad00badbcd79cddcfbcc6e9afb4e74859e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332323361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2be9399e5a5e1241a21bc9d4b6a3fb9a91eda423ff9f867729f1c7d4dd1494`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d29124b0199e51ffb3475f695f3b57083f5755bdca3b30b7fb7e41ace7ab`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 52.9 MB (52945684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5474d3d895c6f5799dd4f3bbbdcfa776a9e50f408ba69a4717a2899eb367`  
		Last Modified: Fri, 31 Oct 2025 00:34:55 GMT  
		Size: 275.3 MB (275288300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:2b3d670ab5944d9837c64cdbfd523b88a99f9a56456dd23f8118f9363cc14688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.0 KB (758017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15731caffee3bf6608f446feff1ee659f031fd1cd8f5b09435eb35688932a2`

```dockerfile
```

-	Layers:
	-	`sha256:6912c322cae1e576478d01096232f97779aa51160ce3cfe9cfaec428fcf894a3`  
		Last Modified: Thu, 30 Oct 2025 23:46:04 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e187fd7b741e285cb843267475b89466d15f6b182c4390c712e27e84fcf08123`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:cd7481aa52dab2ec5a74ac72700f64e64d12de25bd25fcb8180d52b6ab48f86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351705694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838ee80df76d45534e7db0519fdf2ad83b46713fced3855fa567b53e5bda74ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 01:01:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 31 Oct 2025 01:01:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 31 Oct 2025 01:01:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Fri, 31 Oct 2025 01:01:56 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05fabcf0d10f721852d4113d672f0230add628d52619a147b8bbdcb561d800e`  
		Last Modified: Fri, 31 Oct 2025 01:03:37 GMT  
		Size: 54.1 MB (54069725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e0f0305b690c8b100c33c21c950d3700f00f2f8d02c2a64b13f84180c085dc`  
		Last Modified: Fri, 31 Oct 2025 12:48:30 GMT  
		Size: 294.1 MB (294060406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:0cc0f207a83537057bb9767593fc074be67f1e1ad1663e592d2405a66af2c3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.9 KB (715881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd87e14d33d475e5b1f4c90597ff65e0c652abc33a7f2d4bc8930892ae75021a`

```dockerfile
```

-	Layers:
	-	`sha256:d38f70fbdcc9f4abb21152b7286a1b10a8d27ebe0d250cb3378e8e87cf39d95b`  
		Last Modified: Fri, 31 Oct 2025 02:44:41 GMT  
		Size: 703.7 KB (703728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6fda7827a0665df5000082f2da98c7834acaac4b36c9bffa845aa0ef6bd950`  
		Last Modified: Fri, 31 Oct 2025 02:44:42 GMT  
		Size: 12.2 KB (12153 bytes)  
		MIME: application/vnd.in-toto+json
