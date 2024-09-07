## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:d57abe50ab0037f861817a85b4a26c8211d91075b5cca94a133ed02f803cd7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8262442a86a9b570c7bedc81c277028b530ef2ae4ef10c22848cfb06f71378e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664bdc7bc1cc39559e322f3677d7de4a00f2b45ac0c0a71d159a842b4311f188`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd515919089f9642c11b714ac224cff96a19d4c9efb5257a5858bad5ea1684c`  
		Last Modified: Thu, 05 Sep 2024 23:30:27 GMT  
		Size: 52.9 MB (52946299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce7917b4794db9f021843d5b3813f49ff17a7e599668e6ab6f843c370c9b98`  
		Last Modified: Thu, 05 Sep 2024 23:30:31 GMT  
		Size: 234.4 MB (234420835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:a76775262ea1ecbe49f6bd1bcd6a457d70939f11c1c839e26e9651e829885c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5be0943946cb3d5881ba9db6f6b8c4c3ae71f6395f0fe676eb2316209e9e2`

```dockerfile
```

-	Layers:
	-	`sha256:b8e84c1ce52bc24dcb63da4271a86922cda5cb3cb52488d2dbb25223bb559996`  
		Last Modified: Thu, 05 Sep 2024 23:30:26 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc0ffa252a55ae42ccb1e53df41022c2031cc782c2456902f82a717bb8df3e6`  
		Last Modified: Thu, 05 Sep 2024 23:30:26 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json
