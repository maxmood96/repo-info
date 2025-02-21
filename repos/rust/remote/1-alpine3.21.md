## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:b11ea81ffd224a7acf2546d6deace59232a5c6e3e2e6dca61daa6369687fb567
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:74f39e6bfe58a1b610fdc5e6fa67468bc73140469f2090411d2f242d2c9ff407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304582444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458995c03409bbcd98aad3f8d98905aad5e3ed17a8af75404444bf1c40a44b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08914ee27aac92b9d51d0c254e4096fa3710954855f469d9c033328b88aa4`  
		Last Modified: Fri, 14 Feb 2025 21:46:04 GMT  
		Size: 61.6 MB (61564943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577f91cc0333a6bf9ba25ba636393eac92318cad2029d3f7ea1956977483e153`  
		Last Modified: Fri, 14 Feb 2025 21:46:13 GMT  
		Size: 239.4 MB (239375254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e2b417ba07db56ecfd570ba4ba06415b6bcb9c6223bdc248c256292641022c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936b868032fad12549752a349a5ead0978114cd00a432ccc00b3096a11c03d3f`

```dockerfile
```

-	Layers:
	-	`sha256:f6c7849321e26ea20adf4e93b140974a1c9bc65a302ddba1829fde840c5a1cf1`  
		Last Modified: Fri, 14 Feb 2025 21:44:20 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab9bfd3f0d1a3397928e694479a8d3acb066f8cb0d7bf72a8f60f07277b9b10`  
		Last Modified: Fri, 14 Feb 2025 21:44:20 GMT  
		Size: 11.9 KB (11917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5631d8fd90ce08adbc6939db50f221a9edc1080c0591c43fa8c3fa439d758b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305941098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826bb85268a2281ebb44bb2f2e5f85ad85cb32c22cfd88d8c933aac2104c840e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7995ad51d7f8137de2d089a046c47c22b794e249fc189513b6f32c0d853c292`  
		Last Modified: Sat, 15 Feb 2025 09:53:25 GMT  
		Size: 59.1 MB (59101131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcd21a8163258c12f60c947eeb15d7eb972064d5e75a110de8aa82a5e1d45db`  
		Last Modified: Fri, 21 Feb 2025 00:48:10 GMT  
		Size: 242.8 MB (242846938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:d25cf1376d797f662bef4a74d7ac5c48d35cce452bcc13e89b2be288f14ffe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dbbbdd67a3329c38885039388aee2dd2c2e3586ad5852f713988b5c3178877`

```dockerfile
```

-	Layers:
	-	`sha256:c12569e4a08b7e42f85430c95dcc29d53db17ca0b43ecf3a2469197c5a75d16a`  
		Last Modified: Fri, 21 Feb 2025 00:44:32 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5b6a38a5d703183b4feda7beaee9635425c68584d6846ac819d9bf59c65873`  
		Last Modified: Fri, 21 Feb 2025 00:44:32 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
