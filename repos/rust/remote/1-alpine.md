## `rust:1-alpine`

```console
$ docker pull rust@sha256:10c5186ce24e556b47c29253558933618c05141e5f068ed4d147f46a73d64327
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:3e8b0e9d4aad767ceaa31e328c5c3a0f6c5995c6a99a39f8d88c991cec8fc121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296401172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a2321d34732ab3b433221f562777a0d6c23fede534f689b9d5b26c2e1d477a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 22:20:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Dec 2024 22:20:09 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 05 Dec 2024 22:20:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc2fea9d7119845ce1daa03c7e4a48cc033e3cbb3c96820e4795db455788dbf`  
		Last Modified: Fri, 06 Dec 2024 01:28:40 GMT  
		Size: 61.6 MB (61561193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d44bee3385049ce6053d09f0ebfd171096b92dfed8c0b8a746c294680b4eb`  
		Last Modified: Fri, 06 Dec 2024 01:28:42 GMT  
		Size: 231.2 MB (231195536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:069c6111a36e5e5e3dd3f76286fb551a3089cca99059e98b6f425ab95bca1bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d6d7694a95b36a92a0168223ac6bbdd67c49bd7723b3215c1898922f6f3e10`

```dockerfile
```

-	Layers:
	-	`sha256:b519e2f0285f4fa6d5a519a027494f9bdbace9fb0f0f429667cea4fa336c7c33`  
		Last Modified: Fri, 06 Dec 2024 01:28:39 GMT  
		Size: 783.8 KB (783800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3803d179910ce97b74b86e18cfd422e28248f12af5005003ff37185e6f7ffa4f`  
		Last Modified: Fri, 06 Dec 2024 01:28:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

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
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

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
