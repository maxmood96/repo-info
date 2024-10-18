## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:466dc9924d265455aa73e72fd9cdac9db69ce6a988e6f0e6baf852db3485d97d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

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

### `rust:1-alpine3.20` - unknown; unknown

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

### `rust:1-alpine3.20` - linux; arm64 variant v8

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

### `rust:1-alpine3.20` - unknown; unknown

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
