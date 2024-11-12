## `rust:1-alpine`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ef7372f8426acb07a8384ecc19acd753766a128fda95f3755b40cb7dea8ba288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292093012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3dfa5cbe4293fac5e9de9e995618d7703c98c1b5179e855591a58aa0cf1bab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8ec533df57e2eec7e7ea5f79f74992d8739c0ebd7894e95d52697b388dab3`  
		Last Modified: Tue, 12 Nov 2024 02:21:38 GMT  
		Size: 55.3 MB (55309260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf987c9d46c6f8d7c49241f03693a6871f8e3129ae8ca4e02561b64c857d2a6`  
		Last Modified: Tue, 12 Nov 2024 02:21:42 GMT  
		Size: 233.2 MB (233159848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:348e407376cdd07e3899e36bcc401eaecf42cd72ea3b3b8501a2aac7b77b840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 KB (723170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2358d2dd7e75ce43ec9c3bd49bd9757cc4ba95a642247cf701b19ae069fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e70e9632e04dacdd9c17469d4022009fc7724452a123931f37845d30ea68de06`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 711.3 KB (711253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60ba53240156bc0235ef9304159f6fca61b87de219ec2073c609fb58ef8b153`  
		Last Modified: Tue, 12 Nov 2024 02:21:36 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json
