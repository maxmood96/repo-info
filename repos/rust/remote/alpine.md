## `rust:alpine`

```console
$ docker pull rust@sha256:a454f49f2e15e233f829a0fd9a7cbdac64b6f38ec08aeac227595d4fc6eb6d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:1fd5647240e16a7ca968780a3b9d011c1f868f472e8f1739c0257639f0441ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278134834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b044b3a815a76afb9686c59fda26d1e03d1ffc5ad557a1b6e833c976af5459b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb1a0bcffc46374772a9151131b8314b527b4042779a73551e2ce445aae4b82`  
		Last Modified: Thu, 20 Jun 2024 20:57:12 GMT  
		Size: 55.3 MB (55313779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4513f55edff3bda26dd09c867dc66fc0e9dfd6a62ffddc7d1aa3dbd4bad2ac8`  
		Last Modified: Thu, 20 Jun 2024 20:57:14 GMT  
		Size: 219.2 MB (219197211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:c78a4aba3cb5ebddb51a402e1c506ceb4ceec0d18cf1548baef2d6cf5eeae348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.9 KB (717939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fc90a3879243665898f7b09110b083b505820641c1b262f9452298467fa125`

```dockerfile
```

-	Layers:
	-	`sha256:d438704cb2ee31b45d94d103cf3e063bfdd65f67e567e7c31540ac3a45129757`  
		Last Modified: Thu, 20 Jun 2024 20:57:11 GMT  
		Size: 706.3 KB (706260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f60bca25ef414d01dd82c995a83ab40154a58ddc1fd794f3a737b42c02df4`  
		Last Modified: Thu, 20 Jun 2024 20:57:11 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

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

### `rust:alpine` - unknown; unknown

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
