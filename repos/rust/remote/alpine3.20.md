## `rust:alpine3.20`

```console
$ docker pull rust@sha256:6b1a8a05a7d4863f87c383ceb645bf038c5dba41e5a43fb7c7cc4a252b313a35
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
$ docker pull rust@sha256:d6ee218d63de073b1df513eaa866e2a6b261f27e5a4aa9378434e9ab7b3f317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329630644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9bf6b1a37f4ae814f235e22283ebe67dbb883c8efbe88f35873a0f18349fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:53:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:53:56 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:53:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:54:14 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d718a61dc80a184fb46d3de65bdcf9207e16c4fe4d0b5720b47c6ea9c007a9a`  
		Last Modified: Thu, 26 Mar 2026 20:54:53 GMT  
		Size: 58.8 MB (58781701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfcc1ca3d4fb1437e05b8d752d5da577749beb1c385b6d1a98871938fb6908e`  
		Last Modified: Thu, 26 Mar 2026 20:54:56 GMT  
		Size: 267.2 MB (267221079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:00b13f01bff22da41284f968d5fed9f9414a612b0acccde92cc231b02d895ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e5cf461796b627b3a3dd68a91fc9a173bda267a4646bbf2b7d9f1d72125fcd`

```dockerfile
```

-	Layers:
	-	`sha256:54a91cef92107598804d652b1356d6a3611b7b001fbd71193277cb189c1e8c06`  
		Last Modified: Thu, 26 Mar 2026 20:54:50 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8698ae63be2d6d4f69e2998ff3e17c8ac0427c3229aa940b9bb7da2fd24e2c6e`  
		Last Modified: Thu, 26 Mar 2026 20:54:50 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43df185bb0f65ea798a9b20e66b978b302f2f342ffe0b0d10f476eee23db80d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332795809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0b3ebc683ed3c613ca87cca002f1032f01d39ed57de225dacd71f05f3ba7bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:53:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:53:35 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:53:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:53:50 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e521734345e0e19be9717fe08cb3dc5abd48bf7402a8a16842e1460b55652e`  
		Last Modified: Thu, 26 Mar 2026 20:54:25 GMT  
		Size: 55.6 MB (55558386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d974fdfe6a5a51209667aa57f3979b96a4f4d430e19c33df464ce23bc5b1af0`  
		Last Modified: Thu, 26 Mar 2026 20:54:29 GMT  
		Size: 273.1 MB (273147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:24173bf8d955dff9b56c0103e1d7108b28bab811ddb62b9cffc19e858da522e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667eb82bb5ed22bee0217f4f747130d27fbc81e4beed7be38bb60c66b865a605`

```dockerfile
```

-	Layers:
	-	`sha256:0b17474db555c9a24f20f9c8b5a9c2cc9c1db4c7cd8c49c8ef479d050f3a26af`  
		Last Modified: Thu, 26 Mar 2026 20:54:23 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69260821c896fd77bb2647ea8e7689ddeed89e05a674705eeebbaddbd5b898d`  
		Last Modified: Thu, 26 Mar 2026 20:54:23 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:c34101142d3f8ecb847b57523997197754923d38ab5ce7dd201a6d4bf127cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352501822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c75866b379394f70a8d3c807a6ba21f9450fee25efc669e1f67751850fd384`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:56:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:56:27 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:56:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:56:51 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a0b3b28d99180bfbb9bd2ab6f2f022fbbb076dd6f928d65d1473be00c72404`  
		Last Modified: Thu, 26 Mar 2026 20:58:02 GMT  
		Size: 56.6 MB (56619559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d30920d2fca958ec6f9528e90f8f229bdcd6a245cb5af0d8f2b7e52309cb2`  
		Last Modified: Thu, 26 Mar 2026 20:58:07 GMT  
		Size: 292.3 MB (292304753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:fa78567c0a9cef1ad133c2a432ad8aebc605a9e5ece49109826d7aeb908228d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6daba87a20474e67029befb0e08e0bb83a03cd65e97f304a3e30652f8b1660`

```dockerfile
```

-	Layers:
	-	`sha256:3a9a67c0e3c984ecbd590106c03af5b0df0431d1016e26338d585501c5e90d84`  
		Last Modified: Thu, 26 Mar 2026 20:58:00 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a156be018177e4ad3914478fcdf611555b948b4f636ffa6f6c6675faa54892`  
		Last Modified: Thu, 26 Mar 2026 20:58:00 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.in-toto+json
