## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
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
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
