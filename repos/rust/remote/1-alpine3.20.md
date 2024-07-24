## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:cc9b42c44d37caccb8f7c366f19f5a41ca0f20f826fb043be073167308b6073d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

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

### `rust:1-alpine3.20` - unknown; unknown

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

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:223875d41972c63ce2a7d191452337272aa3328414ecd5da95f14ee7d7142921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284122246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516f61bb3e7aea62cdbf92addbef0d965932d6179863a85468591bdfb0f507a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d4cd3c962917973194e382e7484ba9e85a37d9b55b692315a7a195f87ccdd`  
		Last Modified: Wed, 24 Jul 2024 08:22:31 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76f719aea09b6212d7c98ae7199f686e5465781e2290ca3e33e725c33bd512`  
		Last Modified: Wed, 24 Jul 2024 08:22:34 GMT  
		Size: 227.1 MB (227089059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:7a85fbe4ca35ed4713cbf9807f9e6fd18b47c8a6450e325de20c8cdd0529121a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b6cc71150f06e98e0247a89ba3d4920b967a7da6c672631d11170671873e5f`

```dockerfile
```

-	Layers:
	-	`sha256:52c50b4fa98c98b63496cce27f8a451833920fef391708dcaa209a03a8cf7774`  
		Last Modified: Wed, 24 Jul 2024 08:22:29 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71175fd76100781eba782151b652a8cab89bbc3ce57abd2b348ed99becaa1a28`  
		Last Modified: Wed, 24 Jul 2024 08:22:29 GMT  
		Size: 12.0 KB (12026 bytes)  
		MIME: application/vnd.in-toto+json
