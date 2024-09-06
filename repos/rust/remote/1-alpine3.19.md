## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:e859571b28fc717aef598f33bd8bdb01bc85f4d4f1e061b49af0954e66089571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:30d1ab580950a760d4b3f2f5c89dd18af51f8a4819c7427f72cbaa421aacbb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283076219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73eb6d513488d60b54a57cd010b23bef28f7300bbee331466d55ff02d7163d5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279aeb4fb07eb191aa7015c51d90be6e61f1b1b99b3fe80018d6418e1dec7da`  
		Last Modified: Thu, 05 Sep 2024 23:04:54 GMT  
		Size: 55.3 MB (55346815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ec10859200fd3add1d2f2473beb5d21c145584a39288a28fd17f35a9c176e`  
		Last Modified: Thu, 05 Sep 2024 23:04:57 GMT  
		Size: 224.3 MB (224310364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:87cb6e2fb8401a58ddd2e1fa3a015191134df2ea4a4fa58fc09d8b05620b698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b2688db111169af7237e0ae96bc22dcaa8eaa4a0803a79e9afdcf8fd53f946`

```dockerfile
```

-	Layers:
	-	`sha256:6f26a9b1197c06a0991dc9dd20e11f9dff03f4644c3bc144803f1896f81f30b0`  
		Last Modified: Thu, 05 Sep 2024 23:04:53 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ef72ae7461493cbaace0719176b6296451041f138bba01ce72a261d6ecf56f`  
		Last Modified: Thu, 05 Sep 2024 23:04:52 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:259c916e1f514be8b17e6d7bb2c98dccad63eada48f6a87c93bc57fc3a12210b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290774748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bbd8a310b6f9f497514131c8fc0dfc5f3d7a0675349e8cbe753cd49004ffa6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2d6e750364f7ebf63b8f2e3bb73079180f1c9b4ab508be1bd2d6f966c53d15`  
		Last Modified: Thu, 05 Sep 2024 23:29:25 GMT  
		Size: 53.0 MB (52995476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a9e839bbed9174aac42ee39450e880ff85334346d494ef65f19dda1eb7e9a`  
		Last Modified: Thu, 05 Sep 2024 23:29:28 GMT  
		Size: 234.4 MB (234420814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:a36d56d6fc9814b65402be108fa535718952177e30bd1ac07782edef2247b6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd701806ea1e1dd21fcb91579dd16459f8699ccbe85b86301142a934ef8252e0`

```dockerfile
```

-	Layers:
	-	`sha256:fd81c57afde7c3557a77376d954f685a921240ed7c1502a414a1a0f101226839`  
		Last Modified: Thu, 05 Sep 2024 23:29:23 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3efd8076289e788fc48fef1af400762918c4c7d677ad513f3f31b3288ff487c8`  
		Last Modified: Thu, 05 Sep 2024 23:29:23 GMT  
		Size: 10.8 KB (10774 bytes)  
		MIME: application/vnd.in-toto+json
