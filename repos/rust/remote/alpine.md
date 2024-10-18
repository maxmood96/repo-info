## `rust:alpine`

```console
$ docker pull rust@sha256:b8a600dde33a0acee8d555a760b76c12eef15b5f3c471de4fecdc48525630bb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:49abeacc841e604b61cda0afadfcf380230b0a8adddbb3c30fcdea755d8e4caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a56099178a47aa31db1f30d598081e7a531fb025ae36798c54aa211f188025`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c434bbc0f398dd4b8e7f73aed18588fd16d2df2beefbc11e360b889d14f244a`  
		Last Modified: Thu, 17 Oct 2024 21:57:44 GMT  
		Size: 55.3 MB (55309294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5607933a863bc2411145de2d0f367f57915fd65e1e7e3beee3dce10bc3a6c49d`  
		Last Modified: Thu, 17 Oct 2024 21:57:47 GMT  
		Size: 233.2 MB (233159992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:5087462084153aa0523415167191d5bb333b6944627f8709aae8d1e3e8681076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.7 KB (722665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7af3525c868ccdd1d1d4ba920799232ca3ef614289e611e30dc83872993792`

```dockerfile
```

-	Layers:
	-	`sha256:294a701c3235d9c87b3187e2e76315ceae69bb1f2152ef7ffee769b89e5e3160`  
		Last Modified: Thu, 17 Oct 2024 21:57:43 GMT  
		Size: 710.9 KB (710948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722095366e8446ac84efd170e6c6a3e6d3b6eeccacc6c7facd41632c7b799517`  
		Last Modified: Thu, 17 Oct 2024 21:57:43 GMT  
		Size: 11.7 KB (11717 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json
