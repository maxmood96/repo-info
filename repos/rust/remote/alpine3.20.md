## `rust:alpine3.20`

```console
$ docker pull rust@sha256:d207993ef2aaba3ee4833731a56afd444bbaffa84cf5e5cfe7aaf210c4512b89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:5dc085c8e197abdada64bf5821850a395e8aa13847b152c5501f84490a4d3699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298317597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68b7b51dba9640aa1eddfa4850fc6b5b8ea12784a325ddfc6e9685ae56caa96`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d10a7c414ed4c3f437d8c638a1c3f82f7b47a764d1a15f1da8284a8b952df6`  
		Last Modified: Fri, 14 Feb 2025 22:03:24 GMT  
		Size: 55.3 MB (55315382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6441553d33e2490ee6d6b61340b5ea2e5765ca4a900027c10aece36e049529`  
		Last Modified: Fri, 14 Feb 2025 22:03:32 GMT  
		Size: 239.4 MB (239375318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:9b4dbb5eba42e82030f6f8e6a4efcb5d3251d46a6f64e88304de188cc26308bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007373e21a49d1da437f484e8f6d5a49f8de324c054850496577bed1ee55a92a`

```dockerfile
```

-	Layers:
	-	`sha256:2b119cdee18ea304507638882be838e1330fe6691e31682f66584568caee0534`  
		Last Modified: Fri, 14 Feb 2025 21:44:26 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465dafc1700c4dfd42b4b274691dffc615bded2a5ea0865755c5d103a5ea6826`  
		Last Modified: Fri, 14 Feb 2025 21:44:26 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f8ccadd20b0bd22fb05f920dd0858e3f279cfc0139493a830116e7cd511260e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299889006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2565bf45c52d6f2b2e8ace0b51267dee758c91ac5f1879927d48f2bea63b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 23:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Feb 2025 23:42:01 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 19 Feb 2025 23:42:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 19 Feb 2025 23:42:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccabb602b869c8da4cf2b12e95603b1f8726b7eeb72b3c5d393e2421de449a8a`  
		Last Modified: Sat, 15 Feb 2025 12:44:58 GMT  
		Size: 53.0 MB (52950978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee72b63df0954b814d63f423c10f02ce212a49a6916c92f77be22c413ecf7c27`  
		Last Modified: Thu, 20 Feb 2025 23:37:17 GMT  
		Size: 242.8 MB (242846863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:671c5f453a22b27582e351182a410793fce829b7b6a4696f9e9edcdf95b9e0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcebaba6bf175aef5a1b9b76e3f5650f3626e1286a564e0594198d6619bac12`

```dockerfile
```

-	Layers:
	-	`sha256:17ea0f4ab547a5a7dbd8627efd6edf899f1616b7ecd1d864b903a3e1053834a4`  
		Last Modified: Fri, 21 Feb 2025 00:44:40 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd354314ffafd56d3bb06b410ba3a7efd6057e753e7816ae818af733b2c8108a`  
		Last Modified: Fri, 21 Feb 2025 00:44:41 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
