## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:af0364d9255d89de01bcae210db895244cd503be9ae415717d94fb569dcea787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:512157f29bdb9a2fce55fa344e697f7c588aa3bad9420e6b02a16f4be6271212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277963082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f813d88aac5742a46de612f5b1647b161b6062e99be8a575f1698fc3dd130491`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f3491a86ccef92f6223fd43358c591c79972733b0a1df79a27c9cd555fa3f`  
		Last Modified: Mon, 22 Jul 2024 23:05:09 GMT  
		Size: 55.3 MB (55346788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c27524ffef2b9218255cf2c7a5d802abd48135f335e53bb475b0e01f727637`  
		Last Modified: Mon, 22 Jul 2024 23:05:13 GMT  
		Size: 219.2 MB (219197254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d12711d5f6352956e8f567990ef3da494fabbded745e01cacbc297f58af78206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a952ae6a6c3f1a661aa264ffbfc294d1bf75bc57d47b45e6add9d475d096ec`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d2a5ea0d62b9813c01e28109e13ee24fd6126e6b508f15e74bd696c517773`  
		Last Modified: Mon, 22 Jul 2024 23:05:08 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9d4bd37a44adbeacbcb181e128ec72e057b0ca86790472316d6aa5965c19b1`  
		Last Modified: Mon, 22 Jul 2024 23:05:07 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be707a7bc73e1697f45768df8542297bd3a1b47acd115cb6605917021ae08e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283441619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e674368cffc67e425499e23a91f905615a808cfe52a008d93f56f285bb2fac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c95e7093f4e1936360dc1a1d64a143d7919144308498f80da4778474e6242a`  
		Last Modified: Fri, 21 Jun 2024 06:59:34 GMT  
		Size: 53.0 MB (52995379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ca1f34b5fc187dd384d7a2e06f8f3a7d929ac00a6ddb5555dabd0f4e309af`  
		Last Modified: Fri, 21 Jun 2024 06:59:37 GMT  
		Size: 227.1 MB (227089038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:25af8517631b2b9556ab2ea26f3826acd576d900bf36dd75bf9edee8fadd68d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.2 KB (755238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1470c5e93a1bae378bfd3d25a27f3654d1eda9c8c7b874245b1616297580e8`

```dockerfile
```

-	Layers:
	-	`sha256:526b6cee0089438fa58619687a2d373ce5efb301cb1a95aded17642b4c01151f`  
		Last Modified: Fri, 21 Jun 2024 06:59:32 GMT  
		Size: 744.5 KB (744463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b23299b161743c6bac19d945716ff9fb30ec6e476542c8247c33980532d3055`  
		Last Modified: Fri, 21 Jun 2024 06:59:32 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
