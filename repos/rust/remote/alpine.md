## `rust:alpine`

```console
$ docker pull rust@sha256:66f48b19d6e88519e2e58bebe0d945779a6a4ca41c2db17db78c9569655b50ac
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
$ docker pull rust@sha256:df39ccf0119a41ecf2a944964db3a20c0e419b3d410ebd7a5a9a3f7bea949361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349458367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a233b536603f517d5c5e8963e94a8e2be6db710206ddffe7425f998abb1ec75d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 28 May 2026 21:49:38 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:49:38 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 28 May 2026 21:49:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:49:57 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb3d2d0646a71bd1fce6ccaa3d582364014b76eee4f12edf7db794300e24e4`  
		Last Modified: Thu, 28 May 2026 21:50:38 GMT  
		Size: 75.1 MB (75113720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bcc9f35a550647e6649481f36f676efec59284eb5b0089ab4296ae88219f7b`  
		Last Modified: Thu, 28 May 2026 21:50:42 GMT  
		Size: 270.5 MB (270480458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:c4096c37227355041d7835e4554c14fcae34b365f11e94b44a4d1a2d14003756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdc55fee5a9fe932073a1f4671ca3bac75b9ce23625ae893910c03968a7361a`

```dockerfile
```

-	Layers:
	-	`sha256:aadf4a5082ae81b00611c2742fdb31a6f8d386c7fc53239a0aa5a8a32e07054e`  
		Last Modified: Thu, 28 May 2026 21:50:35 GMT  
		Size: 1.0 MB (1006460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad9bd50846f9bb15b4e12a142631a4deda66a582c0d7ed7845305a187bbbf98`  
		Last Modified: Thu, 28 May 2026 21:50:35 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:6771f6cea908fe195e7471b5712d25c7b1460340b49370f7ed450a913a43c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345166039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c131c87ad7030871f216c5516bcdd816a749bacf981e800c94dcdf353e5cdacb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 28 May 2026 21:47:47 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:47:47 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 28 May 2026 21:47:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:48:02 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6771a4dbcd6091c4e568d931effd0dd634a9b1d482550c42aac0bac4782a5a`  
		Last Modified: Thu, 28 May 2026 21:48:39 GMT  
		Size: 66.5 MB (66541651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5263f3579fa195df0f0a7fdcfc0813947d4806260f4a852ddcdd1fa7d23773c`  
		Last Modified: Thu, 28 May 2026 21:48:43 GMT  
		Size: 274.4 MB (274424518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:847eb579bcd6ab8c6f1901649dc83c76abe79f0583f58d56504be0d28b54032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e219163423432fa96b3bfeb45749dd0bf62ea7d7f93562b8b185b7fef6539`

```dockerfile
```

-	Layers:
	-	`sha256:e90081458ec8888a0cf11c1a4ced8b95b8999fff1b3cd15c3510012e7fc2f2fb`  
		Last Modified: Thu, 28 May 2026 21:48:36 GMT  
		Size: 1.1 MB (1065519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c94992985bfb1815f1442a01e550ae82e39934d2a3e04465c38c588adf917f9`  
		Last Modified: Thu, 28 May 2026 21:48:35 GMT  
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
