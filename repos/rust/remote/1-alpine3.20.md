## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:5df30b4ca1a37bcd778b8a1031cfa84e697d98c2473b1dd38db8bae3b7040dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:93b16b091ec3814d2eb9e262f580743be5d5457f59add401936ad23a5d433e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278133112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8fe2f4da371bf6ab0042aa345db1323ee69902def6cd3077e57414b11386b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67145fb6ab3cb1f73f53ef3d8c224db35c2ee42a5afb0a40df39fdf8ae81c5`  
		Last Modified: Thu, 13 Jun 2024 18:31:29 GMT  
		Size: 55.3 MB (55313798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8d5f52a1dd5d942e3d2537e7a50e981115ca490bea408a05fc9c0547ed815d`  
		Last Modified: Thu, 13 Jun 2024 18:31:32 GMT  
		Size: 219.2 MB (219197220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:3a8ce6613dd82f5be6e04ea1ba5bfd0caea563e352955b958752017082e9a295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.9 KB (717938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d4367b470b5f7f5b7d0756a051aa7f54835d5d0b590e1bff55f90fd4b6bb7a`

```dockerfile
```

-	Layers:
	-	`sha256:a40097683d9402e1c942dfc928d9aabb766df2836d3d803c24074b01627dfd83`  
		Last Modified: Thu, 13 Jun 2024 18:31:28 GMT  
		Size: 706.3 KB (706259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc22457e95c0a601ab1007da65d0cd8ebbc4e75d831e70a5727b926c8f89adb9`  
		Last Modified: Thu, 13 Jun 2024 18:31:28 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:585cc661d6e6d5927dfc2bf4fa90e94b26a8bac20e68813235642792dddc982e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283590130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755cd0b4235c5a9528f231df7473df7ec03eed02d71fb0eabba06742a9da909d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 16:10:14 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 16:10:14 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 16:10:14 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 22 May 2024 16:10:14 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 22 May 2024 16:10:14 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Wed, 22 May 2024 16:10:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebaa8cc5c942399e2af730f1fa1261664f9e7ce06d68dd3cd8707795b1a72c5`  
		Last Modified: Fri, 24 May 2024 02:55:31 GMT  
		Size: 52.9 MB (52946908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881478cf640933e3ef85d240d048f7bf3b6b8824a7ae134bb4f21d3c7b7bbbee`  
		Last Modified: Fri, 24 May 2024 02:55:35 GMT  
		Size: 226.6 MB (226556446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c8e49426aa4dded33ce04f5d8ad3d3cbd75413d6c33ada244abc39ac25897409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.9 KB (753859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10510d2404a77b7a17ac7bf9ac2c0afbbf353128ffa49583dffcc09bb84bdf2b`

```dockerfile
```

-	Layers:
	-	`sha256:5f9693a4d276225762bde9ff73650868202acb239bcc860e8ddd86dff777c9d8`  
		Last Modified: Fri, 24 May 2024 02:55:29 GMT  
		Size: 742.2 KB (742211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3af407e3e525ed2e248760791190f0e98973bc0c7dfe99bfb763886f8b356a`  
		Last Modified: Fri, 24 May 2024 02:55:29 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json
