## `rust:1-alpine3.23`

```console
$ docker pull rust@sha256:5dc2af9dd547c33f64d5fc1d299ab93b51f39eaa16c426c476b990ce6caf5b3e
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
$ docker pull rust@sha256:4ee08e7c49df686ca3fd0f83a9728b8addd6979f3239253a6f12eab191eae8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349391303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c718a841b4aabd6f43e56d606217d923668082e32b6048d469f1190bc8b51aaa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 22 Jun 2026 20:07:28 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Mon, 22 Jun 2026 20:07:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Mon, 22 Jun 2026 20:07:46 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd38f7377619a7b7bb781e01da0efab73bf5a980f640ff9793e35a867a1627f`  
		Last Modified: Mon, 22 Jun 2026 20:08:24 GMT  
		Size: 75.1 MB (75066307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608f0cc1b61cfb7270e10b308a29d1357c83e5e38a28acfc5565e3f3ed42a491`  
		Last Modified: Mon, 22 Jun 2026 20:08:29 GMT  
		Size: 270.5 MB (270480575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:569fac0ff4f81e778e256bc6c6aa83542aa7ad5dc2c413baafbaaee8f1b84b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.5 KB (1000548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b88727a0297232042d727d1eefc949f5cef509ac7ff5c275820242d828dbf8b`

```dockerfile
```

-	Layers:
	-	`sha256:9f5d2faf0713e59a2d37ae1c3b4496e0cd40e25d52296fb65584cbb0bae36b52`  
		Last Modified: Mon, 22 Jun 2026 20:08:21 GMT  
		Size: 988.4 KB (988364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:395a18b7c9e5676650d66bec1721bf15143e533ea3c7b4f9bc0d2f1ace4643a7`  
		Last Modified: Mon, 22 Jun 2026 20:08:21 GMT  
		Size: 12.2 KB (12184 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8e0b6ff01d99929145d578cf92f04b7093f67d45527045290c6b760b6b574d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345099326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ea64861c7680e25d88f8948cc1313ca622a070848b966a9d9190c4d4200b24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:10:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 22 Jun 2026 20:10:44 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Mon, 22 Jun 2026 20:10:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Mon, 22 Jun 2026 20:10:59 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6137bd93700c4a4819998f6661cd39b88cb1d6eca339057816335ba8038d8`  
		Last Modified: Mon, 22 Jun 2026 20:11:37 GMT  
		Size: 66.5 MB (66493004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f20661a1223c64cfab57e20da7d444c82aa826c644000559d7c1e17062d5f6`  
		Last Modified: Mon, 22 Jun 2026 20:11:41 GMT  
		Size: 274.4 MB (274424462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:11c384dd3e432c93e608b7397c4ce46f86e2c00a6c18111c9c37f90cdf6748cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c8b573662a9839f5b204b0e4ffd1ed58be27d0b3625554379f51b6ad628ae`

```dockerfile
```

-	Layers:
	-	`sha256:c01aa32bbab921de7af73c80f232bf649e43a79c4de6ed51ee3107070ea43c52`  
		Last Modified: Mon, 22 Jun 2026 20:11:33 GMT  
		Size: 1.0 MB (1047375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e5447a84cfc44f1b0f1737edbdda4c51ed9e57bd6c010edecfc1007a32925d`  
		Last Modified: Mon, 22 Jun 2026 20:11:32 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; ppc64le

```console
$ docker pull rust@sha256:37e090e6db07a0617f8c0b82d48fdcc9882ec5b0d88d5c55b62940be7c2d35fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363636277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d978dd6372559964a6fa0956601f99af771232d04b0b33ae500a8086f722adcb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:33:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 22 Jun 2026 21:33:26 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Mon, 22 Jun 2026 21:33:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Mon, 22 Jun 2026 21:33:43 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7004b836c0f2206cccd9150acf7aad2b1e1354358afab7e623a46d49d199c325`  
		Last Modified: Mon, 22 Jun 2026 21:34:59 GMT  
		Size: 66.4 MB (66374502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfdfa72db882162150ee2c69fb87d4b1e822fb93a1976716081a3ecd4a6787`  
		Last Modified: Mon, 22 Jun 2026 21:35:03 GMT  
		Size: 293.4 MB (293449476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:3b623ba71d39a41cd54017ab35ed816ef6a7cccd5f129725b8a961748d948f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.9 KB (992918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb2bf6d0d0439afd373caedfb8c62e21dbd326400a7ed53865459cf9229b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:1e06b2e3fa7c7c2876a9609a2ff661f9da43aae161a8f562cd5c57426c10be70`  
		Last Modified: Mon, 22 Jun 2026 21:34:56 GMT  
		Size: 980.7 KB (980686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a47bb6f513d67b5eb3f599be7f3b07ec9f4e4f72a8c22cd7bd6d3bd3bb94ff`  
		Last Modified: Mon, 22 Jun 2026 21:34:55 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
