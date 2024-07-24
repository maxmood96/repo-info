## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:823d2a308cab1114d499da9c01daae4c8d68a723bc65958989c403dd746a5359
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
$ docker pull rust@sha256:56a3c93cdbd8dbfad1f15fe1dbbe361db3127c23524d2c61aa877a812a94415d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283442917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54693e391a057dd4b4300e1b3a6573483239c072ba686f0b16511ae8d0610f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2110242a6d9443b5f50e3d0c0c4436de04f5ef6178e0a795b644c3f4378a0fd1`  
		Last Modified: Wed, 24 Jul 2024 08:21:26 GMT  
		Size: 53.0 MB (52995447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c79376a7932a4ad0f50c39cab77124ead259093636f7c7e0ce4de8df6baab`  
		Last Modified: Wed, 24 Jul 2024 08:21:29 GMT  
		Size: 227.1 MB (227089012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7205c428bee7aed3add7c2d56b1f11878dd3a8626b91129a65a529e5f636c2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4e3add6789979425caab2f9fb39ad5f4369f96191a25f593bf982388f9eba`

```dockerfile
```

-	Layers:
	-	`sha256:43d4fa0cde75ee3322a03b230736b326d4a6a421a937b5713c6c24d0c5d5635a`  
		Last Modified: Wed, 24 Jul 2024 08:21:25 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce63da0f36725756eeb11b7259f45651dc9393a068c589acd5d3a863550f45fd`  
		Last Modified: Wed, 24 Jul 2024 08:21:24 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
