## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:343d2257f9e18769ce40185935254880c398d32e597fdfd28afd1ca2bdbda044
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:b47c3b7c8f618a7fa83d4920b45fd8f720985e344ff58882e24b2516cd9f2508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279145798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02470ac11fec976aa8d060c6b333ccd4413cd8f32be52105ae3dec3af616b1d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 15:35:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 25 Jul 2024 15:35:56 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 25 Jul 2024 15:35:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.0
# Thu, 25 Jul 2024 15:35:56 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccfef29cef622f26086fdd78b5571a1350ff03bbdd2123f9d962606d72500e0`  
		Last Modified: Thu, 25 Jul 2024 21:01:17 GMT  
		Size: 55.3 MB (55346789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f47a10c6236a505271287cc9c3319d890069107fe8d7d521fbaa6dc61e2acfc`  
		Last Modified: Thu, 25 Jul 2024 21:01:20 GMT  
		Size: 220.4 MB (220379969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:565af3c7d65d45042bc9ccbeb2bdeabf29d874dff286b5b7c74d5d1cba312abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59c0f63dde9fd091c09bca7b3e43c46e1d81bd2bf61c9e2d4054120c3cf5d6a`

```dockerfile
```

-	Layers:
	-	`sha256:b34888632651a3ae5612be8ac3ce1d233d4f5c2b005c13a64f0faf75996f5f36`  
		Last Modified: Thu, 25 Jul 2024 21:01:15 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437f2acb21f42303fd058a5353c5f14915f67184f012e61f9e6e3343b298934f`  
		Last Modified: Thu, 25 Jul 2024 21:01:15 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3c135554160a74563760c8287be46fb731914b02f3af6296e731112ae7620f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c75f34ecaa924e7c3ee558999ad8bfeeac2de4365e4774087d277fa743c17e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 15:35:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 25 Jul 2024 15:35:56 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 25 Jul 2024 15:35:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.0
# Thu, 25 Jul 2024 15:35:56 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064f62499cbb2ec3ae0a63c9a3d88df9b070852ca8b861a5d047a5a917514a3`  
		Last Modified: Fri, 26 Jul 2024 00:29:43 GMT  
		Size: 230.3 MB (230270616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:3f90be85f740638afe9cc5246647b3580e345cc1628b7c95ff4db653cf83f561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec48f662b536c6649ce01b74c5b70eb89fa53da8b678743ef6e269e8fc4d147`

```dockerfile
```

-	Layers:
	-	`sha256:af9eb333e47a8a21973ffe24acd43990cf0fdb38c58c5da80d1244dbccb6414a`  
		Last Modified: Fri, 26 Jul 2024 00:29:35 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd28e93444b41880962a3ac15e6792002bfa15eef232069c69eef608879bbe87`  
		Last Modified: Fri, 26 Jul 2024 00:29:35 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
