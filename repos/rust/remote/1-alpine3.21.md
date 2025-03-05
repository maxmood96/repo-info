## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:bea885d2711087e67a9f7a7cd1a164976f4c35389478512af170730014d2452a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:715f7a1b6b3a538f7b55c0be7db7e5bb0461fe9ea1d0004a481ab0c5d59542ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304381120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2895937b918bdfd662cc0e35d9dff14e4de6d8c901308600bd7833b857895fcd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3511c78a623c9ea42e9b94b0afd9f0736b72ca4be0f25fc9894b5f966b75576`  
		Last Modified: Wed, 05 Mar 2025 19:52:18 GMT  
		Size: 61.6 MB (61564928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeed41a40fb6224cc3b9790c19187837d74d2746902ca63b0a62cd8432a7cba`  
		Last Modified: Wed, 05 Mar 2025 19:52:20 GMT  
		Size: 239.2 MB (239173945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:81d360d9b302191cfacf287b5e84eceefa15af14fbcf47348ff50ca83adeeb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fc777227757621fe24ac4f25d9997627e1d5bf4282e208eaf8e3ce358fc26d`

```dockerfile
```

-	Layers:
	-	`sha256:ec6fa9f6dc4db95de7b8272093f4c0bbcb0ca3d0224cd50287821511dacb531c`  
		Last Modified: Wed, 05 Mar 2025 19:52:17 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02d39641134b134da7017cbbedf5e6e8dc6938d73f55922222302e49d1c3c3ac`  
		Last Modified: Wed, 05 Mar 2025 19:52:17 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ed74da152cd6c96bba19870d941764ae58ed7050a621ffa24930963b2369d81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307439319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e14b10f63ca96222cb3d52bbbde0764c1897e1f0a057e36be4111f0240d1ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f540ae446b73693583ac61b04efb5893f50d01a77484ee5ba6ff8ceb191c46a`  
		Last Modified: Wed, 05 Mar 2025 20:20:26 GMT  
		Size: 244.3 MB (244345158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:976e3c3748ea761ffedd81ec31eacc1f96e5f78d049ce36b8e683a87c43d10f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f32123134add5d6fe09ae8796fcf69f3be5b125144eaa3f030a841498dc4e76`

```dockerfile
```

-	Layers:
	-	`sha256:2a21f520aaeb816f63d00311513a4919ee67942d77b805d1c3c0812e403c9a51`  
		Last Modified: Wed, 05 Mar 2025 20:20:21 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c633081069a6e228ee8fc035698cc79ec7a01b8d04bee004bd7c5213834dc1ca`  
		Last Modified: Wed, 05 Mar 2025 20:20:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
