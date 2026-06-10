## `rust:alpine`

```console
$ docker pull rust@sha256:2c1b8729dff863b6e83354b8cf409d8e9613be7482da8617934b2c82c0d08dd5
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
$ docker pull rust@sha256:170984932c07ff397c5ef4c9eb8cf382e04017857873acda3efd8244daecee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349473821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544d15a2f2694d3db28e5e6e6fd6f36d78bcbce12c71057f73780f0d6ddbd165`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:36:43 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 10 Jun 2026 20:36:43 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 10 Jun 2026 20:36:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 10 Jun 2026 20:37:00 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0157f0b4ade24a571ac923c2d3c43af404465bfe28a8885d6c575dd6a4e67b7`  
		Last Modified: Wed, 10 Jun 2026 20:37:36 GMT  
		Size: 75.1 MB (75126800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e4ca55fb7a7181f4303e49e5b0acad5e667c7bed0b75ce5aca155de70238d1`  
		Last Modified: Wed, 10 Jun 2026 20:37:39 GMT  
		Size: 270.5 MB (270480266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d30a2ec3ab46cb391be368dc684dc18180e8ede482658aec5cce0b7bb442ba17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1020783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4588cdd835fb4a48717628a637366a0c3ef15841302067672bbcd5e29b8eb131`

```dockerfile
```

-	Layers:
	-	`sha256:c63c4f101059601973429ee2917cd89b6c850ef39c14094b5218907e3af9298b`  
		Last Modified: Wed, 10 Jun 2026 20:37:33 GMT  
		Size: 1.0 MB (1007393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1963b099ace2df25ac5054d83bb5aceab3564af1b5d55658f6a92cadc4f6b91c`  
		Last Modified: Wed, 10 Jun 2026 20:37:33 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ef56b3b6b77291441cbdd3d347cfab273f99a912de4e7a307a76e4e408308625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345176018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4717ae0fb3dc83efe744a74b8c757e5746310e4d201464cef7181affca240a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:33:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 10 Jun 2026 20:33:44 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 10 Jun 2026 20:33:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 10 Jun 2026 20:33:59 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a830b232fe7f425ca4d63a6c94558090d9d4223b410775451a8ca67113f412`  
		Last Modified: Wed, 10 Jun 2026 20:34:39 GMT  
		Size: 66.5 MB (66549274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a7ee5074b28f66c0810eec4691ac6bb1b376facf14fe990417d4c22cebf8a`  
		Last Modified: Wed, 10 Jun 2026 20:34:46 GMT  
		Size: 274.4 MB (274424414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:79a6af9d07677198e0eb30497b10428b49bca00589d5055966e4a7b53f8be128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d318d6e8f35e405ce4d4cf821989bbc4d9d6a51185d0a86da240f9d8a6ec3`

```dockerfile
```

-	Layers:
	-	`sha256:a0f3f26c13e7bfb5f092e6622eab715ea95cc8438f06c4a9e1a9c126527fe662`  
		Last Modified: Wed, 10 Jun 2026 20:34:35 GMT  
		Size: 1.1 MB (1066346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91ded1bc9182542759eb5ecf2d7c12f6974b084d856294b100a644a00d4c5f8`  
		Last Modified: Wed, 10 Jun 2026 20:34:35 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:e7246f1a226b34fa2d92336285b67c26c884fa2df69c092d2c4a00063a447f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363701744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb32145ac058f86750b7c88b2061dd3ef55b45709d5cc6b7a9a57ab48f200d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 28 May 2026 21:44:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:44:19 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 28 May 2026 21:44:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:44:37 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575e2863ebb65ff255bb8ee0f755133ba7fc8b97f8dad502fb48c74fd341627`  
		Last Modified: Thu, 28 May 2026 21:45:48 GMT  
		Size: 66.4 MB (66421193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b7c0f2be4a7a091f4713845e9c36bea33f0b4b8c00fa140eb274d3c213c5af`  
		Last Modified: Thu, 28 May 2026 21:45:53 GMT  
		Size: 293.4 MB (293449622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f3261c6e41eea15ae7fd356aba14d2cb0a9f6c774c7b9af1ce5eb12342ab4feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e378653d8a54f80c226f6c380162fc23c4a9348cbc9c5168d143bae31d4057`

```dockerfile
```

-	Layers:
	-	`sha256:6a118101eaa58f44eead7bbbdeb5409ebe10d39002e70dc10687103589cea620`  
		Last Modified: Thu, 28 May 2026 21:45:45 GMT  
		Size: 998.8 KB (998806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34c9291a40b73e90c0e2827f712b408a8bf2de6fd011e9a420c4e8b077b3e71`  
		Last Modified: Thu, 28 May 2026 21:45:44 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
