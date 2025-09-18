## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:85ef0dac25e61cf7a81c43b861401c39577257b848769b95b5fba92bf0ece004
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
$ docker pull rust@sha256:f465ee64e31105ae94a873f12c2871ab4a1a575a712963e0c49ae1a0fe4d209b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328570896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047d70579593f501357470fe1cb2a7bcadf3ab063802c1e6aa0691611fe20f54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f272a65ee644d0530a00a5d089333c210c4dcd4ec0dda7534c117af1866e15c9`  
		Last Modified: Thu, 18 Sep 2025 19:08:34 GMT  
		Size: 61.6 MB (61557416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ac32e97308f657738e3c097c39c8fc231b476ccdccc340406e32c85e0558c3`  
		Last Modified: Thu, 18 Sep 2025 21:00:18 GMT  
		Size: 263.4 MB (263375910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e00399449650ab5c7c6ce189a75c5974aa4026c5353840083ff5991b28374a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.2 KB (789170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38f8c55ca20d2527931dfb8a043377297a65a5afe20a0d26de007783bc7a2c8`

```dockerfile
```

-	Layers:
	-	`sha256:44a057ea8ec4156da0374023174b4c75784009300e771318c7f2b2140bec08a9`  
		Last Modified: Thu, 18 Sep 2025 20:45:04 GMT  
		Size: 778.1 KB (778077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ce492f1b7240d3d931ca5ffe876f7399ff35cdb9491bba5354fa58cc76c07b`  
		Last Modified: Thu, 18 Sep 2025 20:45:05 GMT  
		Size: 11.1 KB (11093 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:818129528678a14f6d20cfcafc11c6b445dd18de42e8d231434bd0b5373a3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331666232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c52a7992b63e785e94537250239460f2adee066e92b0264989b300fdc7150e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a1549672c9df172b561f5f160aa767dc77281cb3f185436189511ea80305d3`  
		Last Modified: Thu, 18 Sep 2025 19:07:11 GMT  
		Size: 59.1 MB (59086435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6672a8728db176e2b2560ad6616fec5b9a015d4be44db31cd912928ad454748`  
		Last Modified: Thu, 18 Sep 2025 21:05:23 GMT  
		Size: 268.6 MB (268592860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:429ad7b2392e5101a927024393583915c2c3b8e62810d7dcf3b80abbd4a2450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.8 KB (868827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f460ccc53f25ffdd12ff54498b630240c1564aa62d084f82deb4cf1e791dfff`

```dockerfile
```

-	Layers:
	-	`sha256:a565aaf7f93b3d9154ad88a0a9256126d79b90ff3980b8be13c80330259aabfa`  
		Last Modified: Thu, 18 Sep 2025 20:45:09 GMT  
		Size: 857.6 KB (857615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7642f22e9b3300b081800d7675b85cdd1a8d592d7c2ee8a7d9ea653d674ee1ca`  
		Last Modified: Thu, 18 Sep 2025 20:45:10 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; ppc64le

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

### `rust:1-alpine3.21` - unknown; unknown

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
