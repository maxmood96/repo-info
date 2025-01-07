## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:3d73aa2e05e77e190587a17a07daa930712ee82375e78f8b3fd54ca608d2b81e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:981ab8e75de6bc6d7a309b4a3866ebf9715e4b1a9030e8cca4b4383f00bfad1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290108198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b60f51e73b89f4211a038f78af83195a4ceea568d20d6e7335398a379c57551`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Nov 2024 14:36:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5387e8e6b02dc43704c3be00b46ce1501373ba28ca469cbc52c69ac94bc5f784`  
		Last Modified: Tue, 07 Jan 2025 03:17:53 GMT  
		Size: 55.3 MB (55298396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41a4630e582eb2b5049fe3b869b784de443c30df72d50cbd8fbb0e76a979ee`  
		Last Modified: Tue, 07 Jan 2025 03:17:58 GMT  
		Size: 231.2 MB (231195803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:eb7dfe1af3151e00eb0f09c8490d55212aca396578378fcff5eccb1b17e35a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.3 KB (714324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b851bfb69d97305bfe57d6dc5dca1260f6447aa89e35077ac1a9d0c1d0e4b4a`

```dockerfile
```

-	Layers:
	-	`sha256:5f24b042877685de690c69e7040f7cffe9afea15fc4f3ce5603b794fa95b3f9d`  
		Size: 703.6 KB (703610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089595f53cfd991dd29775187be7adf0b57a2b755e2fb71f1969421c9fa19c4d`  
		Last Modified: Tue, 07 Jan 2025 03:17:51 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
