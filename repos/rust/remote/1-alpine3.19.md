## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:21ca4b5af20dc0cb48532a53b1747541a6a46dbc5c28f1a42aca46ba00f898cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:711370e09b33243b2c3fcd9e41f01801004819987f2250353b62d17a2fabb260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0043ac5ee88bb86989b67b97316cc070636e247c95323bf7e48406377de71b8c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad749439427ff35b1979483f8d31257c93ddce5c7fc51609c16ff9f4e3bfb962`  
		Last Modified: Thu, 17 Oct 2024 21:57:43 GMT  
		Size: 55.3 MB (55346814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729f094bcfc7ac1edcc51780d88e5e20a5e40b49f72d9ae91287a7fd1a1b255a`  
		Last Modified: Thu, 17 Oct 2024 21:57:45 GMT  
		Size: 233.2 MB (233160025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:597af52605d1fa1c4f635ed3539708427a720cc94f0dd6297fa96d78fa11aa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3285883ed95c542aaaa07899433cd26b090675bf48fe01a8ea29e921b57e45`

```dockerfile
```

-	Layers:
	-	`sha256:aad025c2bd8e51fdf72aee0a200636038fec394948c78e803258e724fc789cf7`  
		Last Modified: Thu, 17 Oct 2024 21:57:42 GMT  
		Size: 713.4 KB (713436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c7a14005c5ce98af5823c8096ee36a1dffaf46c5eaa0b71b4f08ccffde4fdd`  
		Last Modified: Thu, 17 Oct 2024 21:57:42 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2ad5d810439717463a3ad522bfe9c626490ca35176488b753a9e57d23f35d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290775337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e25ee6035525a540920de98ffd4b96c964d2195252fb1dc32743828b84b0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74da714a92090eec171b9fdcc6c89c6591ba432fdeeaa10d5c10538ede56c8a`  
		Last Modified: Sat, 07 Sep 2024 11:55:42 GMT  
		Size: 53.0 MB (52995429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56e9f588d67bf61a8465ec612c0b1095ef03b2d5afe03498b7ad4fed2fd38f`  
		Last Modified: Sat, 07 Sep 2024 11:55:47 GMT  
		Size: 234.4 MB (234420805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f9446358434100ac647f0d3dd9a0e1b2005a6f8910ede685cdc2e9e9c2ec5eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644500100d93dbb3715254eb9f6a6028976c644a3ea440840fa3de87e015593a`

```dockerfile
```

-	Layers:
	-	`sha256:5318473dfb1acaa5a3766971ec81932624e4e3e24520ff1226b8de3a4d1eabbc`  
		Last Modified: Sat, 07 Sep 2024 11:55:41 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f4a984e365a0132171af9a5448f3da92750593f5660cb7358ca62cbe7b3b30`  
		Last Modified: Sat, 07 Sep 2024 11:55:40 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
