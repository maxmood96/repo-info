## `rust:1-alpine3.23`

```console
$ docker pull rust@sha256:14b9b5f47dcc6644d0f0c1b35a2c2c5d0124f67159aaee28a348627523459b55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.23` - linux; amd64

```console
$ docker pull rust@sha256:addffc00fc29651ab600b411be00775753252125b017a92513f76ca12c0b9624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349440860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650a3742549ca0501aa1e4156ddb05f620330240a531f8c434c1a3fdb1f4ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:43:38 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:43:38 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:43:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:43:57 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35681aa166ddb968c12a105f82e8f146bc28953236a49f5abff7fe2e950ddb6a`  
		Last Modified: Tue, 30 Jun 2026 23:44:38 GMT  
		Size: 75.1 MB (75066624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47babbed243d5495ea144b6f0cccc187e862ef0a818211ca63b221e31c58711c`  
		Last Modified: Tue, 30 Jun 2026 23:44:42 GMT  
		Size: 270.5 MB (270529815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:459cf7a45621dbb1a5953326eb83449c345f1c19743d11bf5b89341575082208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.5 KB (1000550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e47557dd342a2d05052645627d5fe0a974c998f2bdb3a706996d02e10cb7a17`

```dockerfile
```

-	Layers:
	-	`sha256:2870097f15500aa0c4d0b65e66ba6580b8443400e1f4ada03e3826989475e915`  
		Last Modified: Tue, 30 Jun 2026 23:44:35 GMT  
		Size: 988.4 KB (988364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f92180ac36a238e93f9a80de2a1684a5e59f4e1b841d82e5797f3db0af31c8f`  
		Last Modified: Tue, 30 Jun 2026 23:44:35 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b38e527af9cd485d62885dcf64a7842e8d127e94d8b43fa6dc67347675a94d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345062288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ba2d6cbea49494bebcdf22f30d05042234ca90bec514343268858f57b7c54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:41:11 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:11 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:41:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:41:26 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acab90dd04abbcc6f19c5159e47037a20695133fc287933b431fa81ab12d38c`  
		Last Modified: Tue, 30 Jun 2026 23:42:04 GMT  
		Size: 66.5 MB (66493005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e88dd3f2644e1dc33d0cccd8c425a8ac3eee4104753bdc925bf6cf84b23a33`  
		Last Modified: Tue, 30 Jun 2026 23:42:07 GMT  
		Size: 274.4 MB (274387423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:29f4f40867bb142b3e31bd5fd3b0b85cc53148a083b4a1d5aa768a0023e53735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa25b8c005010d764c45c4f6469a8d51953dfdad144a1daabd65e28fbac9206e`

```dockerfile
```

-	Layers:
	-	`sha256:eb83a37eabd331d370b3962fa5139326d3029ca59306112f6f9331631d571198`  
		Last Modified: Tue, 30 Jun 2026 23:42:01 GMT  
		Size: 1.0 MB (1047375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8cff0c17577d73de4fb62d3f7aca3d949b59c1d585083943cb5092bf840ca1`  
		Last Modified: Tue, 30 Jun 2026 23:42:00 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; ppc64le

```console
$ docker pull rust@sha256:4620fb49410d4d5fbb176f8f33040c76e1c3faf0e1fc2f2b29eb37ce932b4435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363623289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b68ba083548b8e8edb5d6fcc58df9c02a22dc0ce139a5e4e4b98a33d32043`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Tue, 30 Jun 2026 23:48:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:48:34 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 30 Jun 2026 23:48:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:48:52 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488209299366ce8085ef0275c2af8ef458cce94116b41960ddabac9037b4f29e`  
		Last Modified: Tue, 30 Jun 2026 23:50:07 GMT  
		Size: 66.4 MB (66374525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab5ebd5143fbfbdf9a084b9416a27c88ac77255a12144ca894beef0325a094`  
		Last Modified: Tue, 30 Jun 2026 23:50:11 GMT  
		Size: 293.4 MB (293436465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:3b07d5b79c0876dc7b23c4232f53bd5a5592a98a657e62c635b5d83e82696322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.9 KB (992918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74934d28d52cddf55738cf980ed3fc71c0aea07c3433df129856c50bf67ad8df`

```dockerfile
```

-	Layers:
	-	`sha256:31cab00042815a6a7b6e54bc188f20e2fe028e46d39d93088bec9711df8e896e`  
		Last Modified: Tue, 30 Jun 2026 23:50:04 GMT  
		Size: 980.7 KB (980686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1a91e60dc8f3bef3d82ec42e5fd561d6dfa80bafab22a06809052f1a54f298`  
		Last Modified: Tue, 30 Jun 2026 23:50:04 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
