## `rust:1-alpine`

```console
$ docker pull rust@sha256:50c2dfd3b864a83a8b73a49cf4fa84f26fe89d4ae69ab8373692cfd2d96060c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:7c094ad1afb45a61e28dd007a2add9d8ac171fd3a268e5f8f74b8aebe6c723ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.2 MB (346198921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888e119bbb52426dc17e904e8937f05e319aa5ca98130c7b88b1f355ca1f5408`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 15 Apr 2026 20:55:44 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 15 Apr 2026 20:55:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Wed, 15 Apr 2026 20:56:01 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008dcc7513c19b21f3c474a33e66b906669e58b9a0fc2235f5b041e8374a5c21`  
		Last Modified: Wed, 15 Apr 2026 20:56:39 GMT  
		Size: 75.1 MB (75113649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a47509c392423b14fa55a333881cdc430489c34cc4838c18529bdfb43b8d5d2`  
		Last Modified: Wed, 15 Apr 2026 20:56:46 GMT  
		Size: 267.2 MB (267221083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e6c7b4dc07ce841971c9735828d5c1398acd54da494a4a715d9086a950fb4cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0ce1167b9e46aab282306b932ea06d9d658bf728b53226a519ad90a1560aab`

```dockerfile
```

-	Layers:
	-	`sha256:34ce73698f63069381e650d85e304a1d67ca62103c8c12911d3e03bd06a94955`  
		Last Modified: Wed, 15 Apr 2026 20:56:36 GMT  
		Size: 1.0 MB (1006460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b593eb93b7a91b74e5ef784534e7471dd5969f5f19a7280e9fe6d37de26a942`  
		Last Modified: Wed, 15 Apr 2026 20:56:36 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c1e4313a36ea7f5b21b04675272e50f90fb5f129eae98e5fff3bc3c87f9f4623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343888876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b512f5e21696e50ac3cc0cb5ed5eaf38a79a54930924e19a52e374691339cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:04:38 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 15 Apr 2026 21:04:38 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 15 Apr 2026 21:04:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Wed, 15 Apr 2026 21:04:53 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0b8ad2b591eff0128a9b31cf86c0cd67c383f874fc96f8b11fbfef420c3682`  
		Last Modified: Wed, 15 Apr 2026 21:05:30 GMT  
		Size: 66.5 MB (66541538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783c89fdb5d6031e8c4c26e440cb773320807a92ce42c6dc60f90c91c7c36811`  
		Last Modified: Wed, 15 Apr 2026 21:05:35 GMT  
		Size: 273.1 MB (273147468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b01eb47e83eff2d5acfde9990ead211541540e314b5316c3bebad460b49bfe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd5124c07c532aefeed4a1c556a5e6d03485b14a768e73d7aa9186ae8d06189`

```dockerfile
```

-	Layers:
	-	`sha256:5698cc7fb356ead097da7710275db287fdfc5dfe51461c062baa4ad345eb2ed3`  
		Last Modified: Wed, 15 Apr 2026 21:05:27 GMT  
		Size: 1.1 MB (1065519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7dec035c3c4025c1e5759dc5987cc4f0b79437401a3284787a601186623cbf1`  
		Last Modified: Wed, 15 Apr 2026 21:05:27 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:0aa08058b1b2a5245434f264eac3c145bc5675c77d0eebc7b315b15d77a44119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362560400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3660431d75596396bd07820f9f139095a139787e1fbbb1056f722442556fc7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:59:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:59:04 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:59:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:59:23 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8eeb202db021149303090e1d6eebf2cfd3613ce5bc0e9f4edafa71fffb2dfb`  
		Last Modified: Thu, 26 Mar 2026 21:00:42 GMT  
		Size: 66.4 MB (66425978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376627d76746f609868721929276ee72d958fcca003b9230386fdaa5ae93c873`  
		Last Modified: Thu, 26 Mar 2026 21:00:46 GMT  
		Size: 292.3 MB (292304779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:59ab8fbfb7af3e996c50d1fd4c249426e26c033e907903596aef0f51fadc881a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50437541e00fc5b5d54fff1823a964ae4529a56794d6c913ea0bd91a818bce2`

```dockerfile
```

-	Layers:
	-	`sha256:19e32046f135179853ba80c451f2a6ad99ae8e2647c9189aa4c686a7949999ce`  
		Last Modified: Thu, 26 Mar 2026 21:00:39 GMT  
		Size: 1000.8 KB (1000761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f9813f9ffa6598afdbf5f2938da4c2902a3b95a8f70894da22634c8345f4e4`  
		Last Modified: Thu, 26 Mar 2026 21:00:39 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
