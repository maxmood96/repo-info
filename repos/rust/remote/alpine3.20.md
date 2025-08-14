## `rust:alpine3.20`

```console
$ docker pull rust@sha256:8476b180807ca64ba3af8ddaaf4197d2238e0607a18628d797b3d2ed3d8ba527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:0b56d26a70b5754206215faa41231e99ace69c1de552de764d652414b80b8259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320189688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542787b2b548e8a6fed952bae4ea97497672e754903e9fb25647d07b6cab9553`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f351fd7764cd6532f91183d4141cca0602b7b5f3cbe2d779dff96bee9218591`  
		Last Modified: Fri, 08 Aug 2025 16:56:35 GMT  
		Size: 55.3 MB (55301954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab0079e6abb50af677ee7f7f543106623517adf98f699484bc2fc3f3bd0950`  
		Last Modified: Fri, 08 Aug 2025 17:52:23 GMT  
		Size: 261.3 MB (261267257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:531103051ac9b051b1ad23e7a1dcf1822fbb818d68023b617704d521b84c2a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 KB (718339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa1b5bfdd945a6041eb3892d94f815856518f912b6617a96a8075e8f0b3aa8a`

```dockerfile
```

-	Layers:
	-	`sha256:8d36a15bbf7ee70a205b7ec6f1fc87835420b6d40156a8c72d66080184aec01f`  
		Last Modified: Fri, 08 Aug 2025 17:50:18 GMT  
		Size: 707.2 KB (707247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18b6417ed02ade19be4dba134fd9ed595fac3b8e4dd3517247bfeb0d4d2f385`  
		Last Modified: Fri, 08 Aug 2025 17:50:18 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:de4bee175f2e7d8867f610235e65f6316aef9f5a173e13ca5cd95a2f2cd60b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320902587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baebd360a63ad9bcd9b08a62fa13bed52ddceb89d206f65301644f57683e441d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18d865dde2a1af19abfc6b5673b4ed8a206f3778349160a66d43180b3350b5f`  
		Last Modified: Fri, 08 Aug 2025 17:03:46 GMT  
		Size: 52.9 MB (52940461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a699bcac7a4c15eec1ed98e094aaf912875fe48d8cdc07572325a7edd597b0d`  
		Last Modified: Fri, 08 Aug 2025 17:56:29 GMT  
		Size: 263.9 MB (263873758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:06fce2385151755f7acd76b4e211c0f8d1f21a4c92050496fdc95ba38e462cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.4 KB (754390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456b3f80cb9563405ec6ea2a0607cbba442e4f451453092d3f30993265d547b`

```dockerfile
```

-	Layers:
	-	`sha256:c458e4d17852001b9edd884dcc8b1fb89fae08c47db4abb25b3a292148b940e9`  
		Last Modified: Fri, 08 Aug 2025 17:50:22 GMT  
		Size: 743.2 KB (743179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c56015a6b12acf9896d6e8423f1b6132a195c2a5e31b1704e51292a0580812a`  
		Last Modified: Fri, 08 Aug 2025 17:50:23 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:cdd39083f093bec61153e9964e981156b4ac5b90877a4843763988730dbbba08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340114142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca846231a32addfb3edcff6e7bc826dc3d761b127a53bed92817d13655b2d42e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:73bde2df7f2a99c3410af2a896f6a27d75b568382e3402ee391dd7f3a0b19069`  
		Last Modified: Tue, 15 Jul 2025 19:00:47 GMT  
		Size: 3.6 MB (3570555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d394561ac16253d8d7d49dd6cbefe0a1adbf0e3aa39368559280ccff13c6d8e1`  
		Last Modified: Fri, 08 Aug 2025 22:06:51 GMT  
		Size: 54.1 MB (54060291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7a5a6b54cf4096101ec38d8613fdd32765d113a57c5f942538812b4a8eaa2`  
		Last Modified: Fri, 08 Aug 2025 22:07:04 GMT  
		Size: 282.5 MB (282483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1b1cbc80c32acba82b6b670ca6d6decd3e70125ec61c589ebaebcb21ac469f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.3 KB (712254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81437543d0ee6f012f4359a7c870d0b14f8a786288b54351a87351f1e2e826e1`

```dockerfile
```

-	Layers:
	-	`sha256:e6108a47d254b6200787e9dc5fef036a67a928f3e972a341548a86e681b5ad35`  
		Last Modified: Fri, 08 Aug 2025 20:44:29 GMT  
		Size: 701.1 KB (701115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fadf6ded42c2bf1ef32b7f7e93aa61f1f25dddb44d124523621e08bbf16d77a`  
		Last Modified: Fri, 08 Aug 2025 20:44:29 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json
