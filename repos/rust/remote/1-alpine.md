## `rust:1-alpine`

```console
$ docker pull rust@sha256:71c9d7afe57ce0c6c53573544e33fbdc88275446fb5c84c78272d6c155b7c847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:4507e352e63be31659483b8b8d76eab2683341bfa00375e5f405098a0d87a9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278129484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e206797bf146aa03fa50885a0ca4d52b5b3d4027d66ec28fe19eb65a849b7289`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c7fbd688f478563cb61c0e573df586d1576845a6c45b57ade3233ee2d19f62`  
		Last Modified: Mon, 22 Jul 2024 23:04:45 GMT  
		Size: 55.3 MB (55309272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba2f8a946d42f568cf4cd29d1b9b4178e6c9ed0729b03b8c30d86173872eca3`  
		Last Modified: Mon, 22 Jul 2024 23:04:47 GMT  
		Size: 219.2 MB (219197320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e67b6221e3004e088edf9cc6053aecf7225612a0689a9d23db92926611845942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf10baa393880fba92972769292746519c3353d3de0d6ce95fbf3cc1ae04bfbd`

```dockerfile
```

-	Layers:
	-	`sha256:84ba051827849b7b74f23fbac4ea816f832caa09818e94b8d17b5f565096b0e4`  
		Last Modified: Mon, 22 Jul 2024 23:04:44 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8362b8ba88bcf7973441ce1f7a7fdcdf11ae3f3e91bab8d981ce124705b93344`  
		Last Modified: Mon, 22 Jul 2024 23:04:44 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b3624ba0133b7a8aa8cb0eb5e55613d1dc0f34e986f5c89556a680a1598787a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284124847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc89c857e9b145490765a7a57ee50cc9082193b18286f2cbbd42aaa3276ea5b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa6cd997e70a1eb384610a94ec222277ae81bba84df0e86ec74bf2936ce928`  
		Last Modified: Fri, 21 Jun 2024 07:00:40 GMT  
		Size: 52.9 MB (52947060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514be7ecd8382f4e79822cf619638f646f54ca988978a8224c4bafa1bf2ef978`  
		Last Modified: Fri, 21 Jun 2024 07:00:43 GMT  
		Size: 227.1 MB (227088987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:2532f90a86ceea43ea86a765bd61e33c927da3cf1322d711b926d0b03e5a8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.3 KB (754323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675d133793cfb10dc5421697174d35bdb83ef322a9897d8332f00e2804234856`

```dockerfile
```

-	Layers:
	-	`sha256:fbca26287c7d51838e55f0a78b1787ef120db18b9849189253356cf31719f80c`  
		Last Modified: Fri, 21 Jun 2024 07:00:39 GMT  
		Size: 742.3 KB (742296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2d482f301203805e3450d6b58b0d6392a904cf3b5150d608c20be1c25459c6`  
		Last Modified: Fri, 21 Jun 2024 07:00:38 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json
