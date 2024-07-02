## `rust:slim`

```console
$ docker pull rust@sha256:5670d317e54f21f0297bc8620ce118a9ba2132ef3c75c339f4c777b5813b18bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:59d7d804da75699221be088325eb22f4282ecf9826dfb2a81a9966154e4cea38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277882169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4419e7e6fcb336faa61ffce030ad772a0338b8296a78cde4c100a56fa3071b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09fd2d6d843f7b7cf0749fc92ae9bee2f0622b0ba10fe778687e3a2d3f456d8`  
		Last Modified: Tue, 02 Jul 2024 03:31:17 GMT  
		Size: 248.8 MB (248755891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:684a252b0cd04a8e0df91044c00b0b809ff8b500c40df9e553b89b1fc4833a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa5786c886b68a6bae673e2e69b4fb8d1e6c0c8f600b72c821f2ae309a5506a`

```dockerfile
```

-	Layers:
	-	`sha256:5d74eba7bd04ce85def2c03a6fc867d7dced8537042467a29ea32eae4d027e24`  
		Last Modified: Tue, 02 Jul 2024 03:31:13 GMT  
		Size: 3.9 MB (3919206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7551160ea45ac8f3ca2b27357b6015b6fc399ffff81a6a9ff4414803b33e5625`  
		Last Modified: Tue, 02 Jul 2024 03:31:13 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:147b596df4301f18be2c8662fdafc03208791070e5cdc35e2c7da972eb06e9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285503450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f369852c10fb1ae62db85734f73f582c7c56224f8db536fd49e73a57517564`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590830b2cb8490fdca5de1105573d6e280e38f74a835ac73a004302bf196f118`  
		Last Modified: Fri, 14 Jun 2024 06:01:47 GMT  
		Size: 260.8 MB (260763235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:8936a9484f7200797556482abff4e06fa00838de34670d61a17a3820ece36560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a1aa1a58d4c73cb5630f52b6eb78243d3e656e07afcec3e95ce723573456b2`

```dockerfile
```

-	Layers:
	-	`sha256:1a67764d6ceba7d0088ec2878aadde2f1d85bcab23e4551e8a822f36ca6bbfe3`  
		Last Modified: Fri, 14 Jun 2024 06:01:42 GMT  
		Size: 3.7 MB (3736349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b77a2c438b547046aa23d973303d67023d55c449e8fc435acd05d9f9a9a5278`  
		Last Modified: Fri, 14 Jun 2024 06:01:41 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c428882ff081342a9661fb13a1d059ecdc0b6e979ffec64b80371cf20a2088b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341579296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde07befc9d7f81191fcc84a7ff43b33370dcd95125fe4f958cea4f5dcdb538`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d7657e22931084f9df2df204bdf942fba5d5331b21866129cd2b6f74ec1674`  
		Last Modified: Fri, 14 Jun 2024 04:25:07 GMT  
		Size: 312.4 MB (312399630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:14f1a3f948f310d9caf331a9f1373711345fe858b13cc4043f0ad611cf28fc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb28847f292ea3267c9d212e94a92926e88ac63932cfb2b30511194fbb6184`

```dockerfile
```

-	Layers:
	-	`sha256:2632ba0696a665df32f5d820dce5f6b0840ef858f058383b58b9e8d17687a567`  
		Last Modified: Fri, 14 Jun 2024 04:25:01 GMT  
		Size: 3.9 MB (3941546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322f207a7cfe2bab29a2b6b4f5581ea00e1d5a8b33c5fb60fb5a6125eae7b4f0`  
		Last Modified: Fri, 14 Jun 2024 04:25:00 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:e4f52f2bb47947ce3ac722cbb6bcbcd525ddd3dee710cdd79409340e5df3df61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289462559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f2f36b8d8476951c75500b6fddeb97bace3ed125f490c8efe0fc645ba148fb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c3914b577d8a932eff6503c038f675f7877703067cbb7a736be9b37ebe6e1`  
		Last Modified: Tue, 02 Jul 2024 03:31:56 GMT  
		Size: 259.3 MB (259318284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5aa6770395a49bf2e6b108e82733166e5720622753fcb85500f442b72c38a185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424cf67d07ab6afd1b94822e444a912afe0378003e54b00f763c7bb518405685`

```dockerfile
```

-	Layers:
	-	`sha256:1f291314409db28215f4aabf3db8c9f244ddb1b44ec817ae55796626cb0b95c6`  
		Last Modified: Tue, 02 Jul 2024 03:31:51 GMT  
		Size: 3.9 MB (3900905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91123db1676acce93ed324aa1878449b167a36aa902043b88262278684858e78`  
		Last Modified: Tue, 02 Jul 2024 03:31:51 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e2829ada56ddd9095c1922f7bd79b55ad2890f121c8cd27b5e880a1438bc6527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289254875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2246462d560d2f3bceba4c85da6bb2afb75caa29e24187c1edfafa35671a1aa2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:04 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 13 Jun 2024 01:17:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05de6d6cf4f84b24b1fe1877b9630bd4f3d3522be0244356de26db260e53abb4`  
		Last Modified: Fri, 14 Jun 2024 06:27:20 GMT  
		Size: 256.1 MB (256113680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:be4332f04bc1282738f71789acd8ae326b69822c14b51abb8c611d57e2d0095c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e1b1acef39033804dafd7ac9b58a15f120801e923f19ca80cbed8d204edd22`

```dockerfile
```

-	Layers:
	-	`sha256:f26143ff64ee7c05c35a9d88a0b97ad96cc7933c3aa2fedb79c0efd3fde576e5`  
		Last Modified: Fri, 14 Jun 2024 06:27:14 GMT  
		Size: 3.9 MB (3891625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff7ac7f28879640ee94261ff0ee133b46b3cf3abb4e714f25fa50f121267f36`  
		Last Modified: Fri, 14 Jun 2024 06:27:14 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:e72c41e16a47967abbb92d88cee32eceb157b9e092706fbf93d0bebe82970923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336901940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda2cb596865c956c4af43a1827a700929a64b291902f6ddc113b96ae28066c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:38 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Thu, 13 Jun 2024 00:42:40 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746a3bcd511aa006f67e48c1fe028e54aa9c4cf5e6262eff47603e6eaee16fb`  
		Last Modified: Fri, 14 Jun 2024 07:14:47 GMT  
		Size: 309.4 MB (309389481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:587902e6e3b437ef50c22bbe656d3980535fed0e41f13bde1ea0c92f86a81581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf284eca0299db1afd18e1ae6d43a590e01ac17aa8453a9f4f105a33d2b36bba`

```dockerfile
```

-	Layers:
	-	`sha256:28d667727e4419218143a92766c2b04f30bbff43af517f95cab3eaaad2a7b145`  
		Last Modified: Fri, 14 Jun 2024 07:14:41 GMT  
		Size: 3.8 MB (3762074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef1fb224c598a7550e2bb7f6fbec40885aa6806a6108de0e816df76eaa64d11`  
		Last Modified: Fri, 14 Jun 2024 07:14:41 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json
