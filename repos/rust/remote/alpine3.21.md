## `rust:alpine3.21`

```console
$ docker pull rust@sha256:1b3ecdc66183eb821f89f9a085af55b842593d711b95894ec4d90e00dc234198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

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

### `rust:alpine3.21` - unknown; unknown

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

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f07f6ed51215ef1915c88d7f7a4a8a017afb328d4dd7dd0f02a0582c2354b43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f1f73f6bdfe09679d5f292ff46d5d0e2775dc636d961952d0064c8f5567ce2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9ff267c15e19d6d8b8527fa75d5ebf03d276ebda1e240af18e4ef01000b60a`  
		Last Modified: Wed, 08 Oct 2025 22:09:39 GMT  
		Size: 59.1 MB (59098820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad9e348e042b825f53ca997d806d448dae40bceafe71c0785c5b519ec73bae`  
		Last Modified: Wed, 08 Oct 2025 22:27:59 GMT  
		Size: 268.6 MB (268591632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:3001b4a4329235ee12795aeb3344de3c9ae1557837226af60d865cc523cb18e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.4 KB (871440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfdbd40dc5d09cbe3768d7d846e6698e01a066df11997d94419e94c37fe2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:c4bf070188ef51f3ab7bfd048c34b2625b80910eda7bb1ebece6dd20ba6b1055`  
		Last Modified: Wed, 08 Oct 2025 23:44:40 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4bf3e336c0502b92b1d9561cf26b9a8fd28885ba0dd2d7ae1778f0354c231e`  
		Last Modified: Wed, 08 Oct 2025 23:44:41 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:c3e84e4e1239cd198222985f7d5f7641767131394cdec02fbb763000212e54dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350042789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed56c3c03b2a6e6035dbe5dbdbdb8c9b73fcb9d2bbda79cc0d86d0961e6546`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1a6157423a4e0ce2fffce1102b10199945bcd698647adee247e2342ba05513`  
		Last Modified: Thu, 18 Sep 2025 19:27:01 GMT  
		Size: 58.9 MB (58949474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b2b934fad56686d5f9a705ed0ef1af753f08468fce2a3f9c61ba22d0293585`  
		Last Modified: Thu, 18 Sep 2025 21:05:45 GMT  
		Size: 287.5 MB (287524190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e763d3d764f5a9fc036c72d819f094a91d42bca1e5f3b7befc5e6fce999d08f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.8 KB (801760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51407785c1de29a683e56619b026117ad6e859b3ad77f2f88e9c260b49ea71e`

```dockerfile
```

-	Layers:
	-	`sha256:af2b3892d14d91833679b486e0390dbf90e8ffbeaf95761c4cfec21a65b7c290`  
		Last Modified: Thu, 18 Sep 2025 20:45:14 GMT  
		Size: 790.6 KB (790621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0e0dc9b05ce555223e7e4d5f43d713e19ee5e96852e0f314469ffd66817b7b`  
		Last Modified: Thu, 18 Sep 2025 20:45:15 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json
