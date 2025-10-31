## `rust:alpine`

```console
$ docker pull rust@sha256:29beb3c7b3b1f8c6e2e5b9e7e6c79a38a7e8a8102d92f50f98951feae046a999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:ee9b9f2ebd8741e4ecf1ade08918e492d642c4e625be481bb7b7954b89e9d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffa4185585206d4d98e871b83bebc561866519a6dba20de63e3192e6804528c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b94f1896c7d7197d473e46aa720688e4b64cabd8c559482b9ad62f5d1c54ea`  
		Last Modified: Wed, 08 Oct 2025 23:46:44 GMT  
		Size: 61.6 MB (61604379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe284ea8abe7a0d30bbfc5a349ac250b13a8a3d1760d8ee638d1c27fbf60b9`  
		Last Modified: Wed, 08 Oct 2025 23:48:01 GMT  
		Size: 263.4 MB (263377869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b05da53540ad6b64b76c78df048088711a426b503ce3d7581f4359156aacb4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.0 KB (794968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b251f281fcb5a2b4f9301b279ee799dbd08e11092d95582b55c6da2b21b4b`

```dockerfile
```

-	Layers:
	-	`sha256:703eec4d4cc485186fb35c31aed213134f9ac25b9ea2420f1fed91ec0b037f1d`  
		Last Modified: Wed, 08 Oct 2025 23:44:42 GMT  
		Size: 782.7 KB (782673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40831b0dc30117747a9bf98ef753d0b9c681127cd96f9f85d11abebfa5eb8934`  
		Last Modified: Wed, 08 Oct 2025 23:44:43 GMT  
		Size: 12.3 KB (12295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:9036b3b6866c1835ae0647bf6e39ed634c24250cbe5ce9323476525325207c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c326a8fb61738f78b6e832d76856f610184e585f0bea48eeb0b05acc9a561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56909a4c35c502dd43802ef31d4890df3cd54f15133b9f35dcaab1ec3f3219`  
		Last Modified: Thu, 09 Oct 2025 05:14:10 GMT  
		Size: 59.0 MB (59006725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20f6c21afdba425061e0ba687974793c99c42b22eafef8cce1227eb48c95ad`  
		Last Modified: Thu, 09 Oct 2025 08:45:22 GMT  
		Size: 287.5 MB (287524125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:fd67dce82d8a2b47d722b477a74576185f4a69052847396ccba385aec9c0cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **807.6 KB (807608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c44369fd4d6569b24f091dde0bde6f511b3ece2eeadb14bc5830c655a4e4bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dccf24b40112f8c8bfb29e2beac0c23ea4a599fc28af8dd896d2a067e715e`  
		Last Modified: Thu, 09 Oct 2025 08:44:26 GMT  
		Size: 795.2 KB (795241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fb1d78b372874952b95cf42ae7f491a90983707634ae9103ede8f18d7de58`  
		Last Modified: Thu, 09 Oct 2025 08:44:27 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json
