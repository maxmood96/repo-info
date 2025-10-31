## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:fa5f395f8f6fd74863960299c24fa0e1eecf7587acbd8abf308a120f505f410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ae572f2a6f7d6790ad87264078d4268b6b8618fe1741e61351938474b3981b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328583689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b473418392e0e4e8bec14410ddb1c78d704e4dda726ae28c63d72ae8d39d461f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129b51f390fdd40aaf39ff5cb8eae55f7068b85b99e151bd9be23bcc2a776817`  
		Last Modified: Wed, 08 Oct 2025 23:20:40 GMT  
		Size: 61.6 MB (61563786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a12271e539b62a08b9044001f072cbc32a6fba77e5f9c606417557d0a1da8`  
		Last Modified: Wed, 08 Oct 2025 23:45:17 GMT  
		Size: 263.4 MB (263377334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7cf01932cc651a307073160fdf88a0afd7e41ff56bebf14c0f4636a8a3390341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.8 KB (791783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1513a03317b2d74a7ef63f021d267865d8903e96ac1bd5f732609a72d165690c`

```dockerfile
```

-	Layers:
	-	`sha256:4d06a9911725da4e0a3dca9033e9b573ffd8ec46f3405912a4c481eb4d4060da`  
		Last Modified: Wed, 08 Oct 2025 23:44:36 GMT  
		Size: 780.7 KB (780690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b6dce726eed8669c3b712d102c9c2206f16dc85add3d7e8aa6d8f8bc9ef41d`  
		Last Modified: Wed, 08 Oct 2025 23:44:37 GMT  
		Size: 11.1 KB (11093 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a8d313620e805ad10815a56881e538d77f2691f105866bf1c3d06a763c821ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917e8113aca6a443a4a106b586c655c769fa81ffae061acf9520322b8ca153f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:33 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:33 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0b7e1f75a2459f5f726e6189c5c2d3641caf14b00d2ca791da1bf9326c47`  
		Last Modified: Thu, 30 Oct 2025 21:36:41 GMT  
		Size: 59.1 MB (59098892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f393f0b81dc80a22d0dedab45fc6b4fda056ff253f63643f56d81e2db340d`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275289698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0d8e262a56e25c2157fb337c3d8b20dc1db76f484d732577849cca7c8888fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3ad2c369a7b6bd488f24704a97ec90f0a3318cb7bb60340efe6720f17797e`

```dockerfile
```

-	Layers:
	-	`sha256:4d344bf8bbc4d9656f3eefb11ac3675e925a0a32b5c22728bd7ebc3473c5dc83`  
		Last Modified: Thu, 30 Oct 2025 23:44:48 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b732c240fc68ebdbe4f1cdb77483fdc405ee55243fdc8dac13b63d314636a3`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 12.2 KB (12226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:f4dd90421dec60a7fb1accd10539fa73f7ee02a5f7a2626ee7a1e0d7358ade8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350063686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628dcf3397d10c30cfe3a2da197cbc7802d9013f083afaf5724ba0f884fcff00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602f64aa625bdbad2f881a453963786cb9d664579705975b5c2752ce620d76f2`  
		Last Modified: Thu, 09 Oct 2025 05:12:09 GMT  
		Size: 59.0 MB (58965844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d12187cc736d95350ac1b48c8022932d8f49cc52cbb21f4f21301a7f609105c`  
		Last Modified: Thu, 09 Oct 2025 06:12:28 GMT  
		Size: 287.5 MB (287523767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:75a3a8807264a9e00056be7f21a4d445e55d62566993b3f1a421d2e96e22e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.4 KB (804373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5d3ae9c51942ce90d391458c8f1986586930cf8ce915f3c4cb0946360a6359`

```dockerfile
```

-	Layers:
	-	`sha256:1249f653cab516099082a6ed253d0534f56a8f1e528d0baa470435062437e22f`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 793.2 KB (793234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb6899ed56649363cee6901aacd976f0b84c33f626067370cf29f452a487ff5`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json
