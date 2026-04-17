## `rust:1-alpine3.23`

```console
$ docker pull rust@sha256:606fd313a0f49743ee2a7bd49a0914bab7deedb12791f3a846a34a4711db7ed2
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
$ docker pull rust@sha256:e98196986adced5602f6e21c54babdbf2a8700400c7a78868324a3630e0c5d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348596215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd3df49495e5c8999a8c75bf6c6bd4ec974eabd17208fd106a9a23633b233da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:00:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 17 Apr 2026 00:00:02 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Fri, 17 Apr 2026 00:00:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 00:00:30 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac10538ca7eeb02d99c9c6f59cd99c72d1202ee1b2e118fe7064ebbb119ec66`  
		Last Modified: Fri, 17 Apr 2026 00:01:16 GMT  
		Size: 75.1 MB (75113584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754f130b6a51072d1a487f177dd493210462b30c556d345382a6eb6325506a8`  
		Last Modified: Fri, 17 Apr 2026 00:01:19 GMT  
		Size: 269.6 MB (269618442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:8113975a53a5d640ba5eb88cc2c8b58174c971a8464921d5bc76c943c96fa61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0abf8f214a4d1ae68ece8676dd40108040fcb868c3a1d08ae51fd9b35edf78`

```dockerfile
```

-	Layers:
	-	`sha256:f1891df239d20a448613855f8dd26883685568ea35c5fb86583332bd90782f01`  
		Last Modified: Fri, 17 Apr 2026 00:01:14 GMT  
		Size: 1.0 MB (1006460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df6ab8f24666f22a8b1ed547f80667f7d735001e5adaed7b77654cec10c83f8`  
		Last Modified: Fri, 17 Apr 2026 00:01:12 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594694ee6b07747b63b5c265be2616b62e814180b66227e2c18c6ee85e4136be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.3 MB (344265292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ac578eba65e812ec8760973123c006da32010f8d441d8c86af62e2b9c5ed7d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 23:59:41 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 16 Apr 2026 23:59:41 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 16 Apr 2026 23:59:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Thu, 16 Apr 2026 23:59:56 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a057f0cb11e27de3615d97d054c8929122e7cdbe93631c1ecf772ab2779a7d`  
		Last Modified: Fri, 17 Apr 2026 00:00:34 GMT  
		Size: 66.5 MB (66541568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342214a195e24bb37c6d54e9ab845a776ec5d2e91c6ba52045d7795dc1b43aa`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 273.5 MB (273523854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:8e355a776dc27e6279374f478ef849e8ad89cbb072be9e5fb8f96e24eaf083ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb997898cd28398b12a09d7a2af06df40520e38e2d7ef15477e44118ba11600e`

```dockerfile
```

-	Layers:
	-	`sha256:957d14987ea9f1ea09284fbb657ff248b23168061c0065ce6e54c574e5e40e88`  
		Last Modified: Fri, 17 Apr 2026 00:00:31 GMT  
		Size: 1.1 MB (1065519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37123a632b3756a359b55ed8f3b95f0addc783a0c97ce4dfc8bb3f29d4f7c18`  
		Last Modified: Fri, 17 Apr 2026 00:00:31 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.23` - linux; ppc64le

```console
$ docker pull rust@sha256:737814f584ff4e75de74a43280e4fdc95175376441f2594ea571f3bcf6a74423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362864952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bff09abb78c2c203f67c89e1b1983b82b047a254e72a8df60e7cfda3762c08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:16:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 15 Apr 2026 23:16:36 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Fri, 17 Apr 2026 00:06:57 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36df2a5fe55fba0246e2043135f7b44d22a83d12d569835953ce94848a4d3ea`  
		Last Modified: Wed, 15 Apr 2026 23:18:06 GMT  
		Size: 66.4 MB (66421216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81754761a7a5961e19b3fa3b7a648abd01c86a3469f93f0c24f842cf7b17e1f0`  
		Last Modified: Fri, 17 Apr 2026 00:08:14 GMT  
		Size: 292.6 MB (292612807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.23` - unknown; unknown

```console
$ docker pull rust@sha256:c4dbc7eb72f3c61e5573bd4290a0eb5e63bcf7c39f70c3cd093f6222677b590a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33c6c2510e012caefc44703ae18c01e584ee9fad27e9a1a2758a49b6e582775`

```dockerfile
```

-	Layers:
	-	`sha256:3e00a5bc33e1f50f2986f7a339868db3d684fbb28316c2e5612c4b3aae6f5b27`  
		Last Modified: Fri, 17 Apr 2026 00:08:08 GMT  
		Size: 998.8 KB (998806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fb5169266350be946a13baa5fa00e930cb1e0a958ddde32db2fb6a8141171c`  
		Last Modified: Fri, 17 Apr 2026 00:08:08 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
