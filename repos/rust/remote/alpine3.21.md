## `rust:alpine3.21`

```console
$ docker pull rust@sha256:77d036177a4caf204bf23c6c68e1aa013a0d919fd40058eb27943295080fe869
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
$ docker pull rust@sha256:3ccb4699768d7097f0b3e2c0b3f31cb403983873d69f5865a1e66ec154eb1786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338293997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40242b1187da13ce02cab149d4cfd0e71a4336892f406a3c9ff3a64cfbb9cb6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:33:23 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 00:33:23 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Fri, 17 Apr 2026 00:33:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 00:33:40 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aa3ac6f2c97191a297fe8438562edadf8bd18a2ada2214232f44e5d0642431`  
		Last Modified: Fri, 17 Apr 2026 00:34:17 GMT  
		Size: 65.0 MB (65028728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5b86ca4980a00e6e82e3b3b8fdc653cd241c09f3028e3bf9dcd22ce66c5bc4`  
		Last Modified: Fri, 17 Apr 2026 00:34:22 GMT  
		Size: 269.6 MB (269618394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:cb44c26fca1b9ddfcc6319ee36ddc2937ec6d40cdca3585ac3f60e7af713c5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.0 KB (973033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f2f2b2455030bf73e7b4c1a6fdcfac3516e1fb88dce9904210e289972eb161`

```dockerfile
```

-	Layers:
	-	`sha256:2c8037b16066aabedced605f19bb16a7071781098f6469f4649a301641412dce`  
		Last Modified: Fri, 17 Apr 2026 00:34:14 GMT  
		Size: 960.8 KB (960849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0c1d676d622fb8fab27cea8a4fb6cbf76e5c668005701633116c0c19e532b1`  
		Last Modified: Fri, 17 Apr 2026 00:34:14 GMT  
		Size: 12.2 KB (12184 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:617723c3b28108d9de0b51158f8a09bbcf9fa7bab30877ce80a0101e62222641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339218618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86de754169f13e8457ee3eeb188dcb9523cfa2b84ea1913e41d1e50fee7c37b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:37:54 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 00:37:54 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Fri, 17 Apr 2026 00:37:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 00:38:08 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4918a223675eca058f31a408ecb63fe3685e00574363c545b95260818a76c6`  
		Last Modified: Fri, 17 Apr 2026 00:38:47 GMT  
		Size: 61.7 MB (61700216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af28f4c07808ede0330aaaafed6386cdec2d3b91c02324b0fcd557e037b8517a`  
		Last Modified: Fri, 17 Apr 2026 00:38:52 GMT  
		Size: 273.5 MB (273523937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:925bd76c043138e73ab4f0319f6c308059e49df752320b0edc0bbfd188f1a352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1052479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4422ba1322cfc7b1b74adecbe3d42d3d38437bd5e2fbb67c6ffc3a54940976`

```dockerfile
```

-	Layers:
	-	`sha256:440bdd2a47c5f73a158b03d5f1d2c5b81b295c76187d09fa3756b0e4c0179e8c`  
		Last Modified: Fri, 17 Apr 2026 00:38:43 GMT  
		Size: 1.0 MB (1040175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640a1f229811063e22ab0c72bf4fe30d82de2c9bc4487a3e152a6fb55e5b7d71`  
		Last Modified: Fri, 17 Apr 2026 00:38:42 GMT  
		Size: 12.3 KB (12304 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:f7542dca228f9db7702008ad2a14efb6e6f23be5af99ddcd111f9a58706fa418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357703914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af3b93392c575a000eb35352ef71ca50fef8e68ff4ac056afc66e4f38096d39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:31 GMT
ADD alpine-minirootfs-3.21.7-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:31 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 02:06:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 02:06:01 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Fri, 17 Apr 2026 02:06:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 02:06:20 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe51ead1f71865857c2c015e74518a0be9e72c6a70a845d843f7dd0cd2ee6e2e`  
		Last Modified: Fri, 17 Apr 2026 00:00:41 GMT  
		Size: 3.6 MB (3578920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37116ea4d99ef43d851dec9099b3b3fcaf650ade517cdcc6e0790d840196fafb`  
		Last Modified: Fri, 17 Apr 2026 02:07:31 GMT  
		Size: 61.5 MB (61512202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac19eb035ee707bda424037602c6a55a91ad1aaca282d4e26d0369657dce403b`  
		Last Modified: Fri, 17 Apr 2026 02:07:36 GMT  
		Size: 292.6 MB (292612792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:39c07104a9622f69b5f86322aee57f9f723583cfd9cfcf844afa5fbdd21b8681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.6 KB (985625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e642b7ee5eda4136012f9d6fdbf13b7eadb8b1ae19d3ab6968134de9f40a089c`

```dockerfile
```

-	Layers:
	-	`sha256:c95eb32fa3df4a7542dfefc60254aa663c5cf39719e303c166a3a2ad3208c47d`  
		Last Modified: Fri, 17 Apr 2026 02:07:28 GMT  
		Size: 973.4 KB (973393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d143fd84a1d45ef26ea013e0a9086233d4f0d378f29d1279e6d8df962785c458`  
		Last Modified: Fri, 17 Apr 2026 02:07:28 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
