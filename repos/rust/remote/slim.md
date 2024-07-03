## `rust:slim`

```console
$ docker pull rust@sha256:8147f469458ff9dd26ac25c7dac505749db934088776a624869c01cd60581314
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
$ docker pull rust@sha256:553e4c4b54ca2ed4db594da10f7186f39e5e4fea6d987086ab79c7735e7d2ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285675838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9afe0ba4d5fdbacfef74d83fb106262407332978277f41911bbb32fe6ab8d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c93274777e52b7cc87f751088639fb414566ecd03a18a7b7cb7763bc080edaf`  
		Last Modified: Wed, 03 Jul 2024 01:25:13 GMT  
		Size: 261.0 MB (260957668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f08a756579bf98b2b856220a41975d1bfdbbc50f2eb9c9cdff40b6ea8610c2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67e3e0f05f7a8430b87ea8b17b968d7ffb3bb5d86cd41c191104e41950e2058`

```dockerfile
```

-	Layers:
	-	`sha256:881902005e746374c4a4b697a28fa1a562a031218a23324a79192e6cbf8005c2`  
		Last Modified: Wed, 03 Jul 2024 01:25:05 GMT  
		Size: 3.7 MB (3736378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82674fcd5b769ec70bfbcff455f539500360232e0d4559517730c72e20af0075`  
		Last Modified: Wed, 03 Jul 2024 01:25:04 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3d869e4574d6bea4ce728cf1fd8071805e272c9a35da5fe3996e264c28dd88fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341752241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a961b1007476fe9ae346834ec48d4aa22241e39349952a8dc5aeb4dc4bbe361`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aea7c0d5a859f64ea62eb45787e4b8b861b44b9e2af4a5e9f2559d8de92aa8`  
		Last Modified: Tue, 02 Jul 2024 23:53:19 GMT  
		Size: 312.6 MB (312595678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:ec6c9951a2d38a42812224963bc493c84f95e237123ae248a1c922c07e63ea8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cde28d325791438588e028d9568706b320864eabf9da7f9d474106e0583f34a`

```dockerfile
```

-	Layers:
	-	`sha256:2d669c29d79221684691281bd82ff672d685bfc596135eea4792a24cddaefd70`  
		Last Modified: Tue, 02 Jul 2024 23:53:13 GMT  
		Size: 3.9 MB (3941575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a58e0eca717a17c06d139365316e69ad9c8161c25a4c6c9ca30e514fa9f4878`  
		Last Modified: Tue, 02 Jul 2024 23:53:13 GMT  
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
$ docker pull rust@sha256:6d8cdb4f6e3a3d5aabaf0784011a29c7fecc159e81f12169a8129af49cda1257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289436665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190724bdfe1f439326b80758bdf4c9f192c116ca8a405c6704b6a6e60fa89465`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cc3fcb1a35b159b05875fe5690a84c8211f4dd27d5add206785ebbd0ba1fe5`  
		Last Modified: Tue, 02 Jul 2024 21:17:08 GMT  
		Size: 256.3 MB (256314388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:82bb5b86608cbaa1f38f91631739bd9b6a5d0142a9db7eb7be829d77ddf3e087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b41b2b6d735960bceed83530d6de523501ff6aa35768806d9941bfe729c11d9`

```dockerfile
```

-	Layers:
	-	`sha256:a8bee735e357890ad382e1526ad90ed1cee58d819f2a82759dbae20c74ca584d`  
		Last Modified: Tue, 02 Jul 2024 21:17:02 GMT  
		Size: 3.9 MB (3891654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1700e1f1148d236db318fcbcb0119c10c432144080b5427c619b204320f577`  
		Last Modified: Tue, 02 Jul 2024 21:17:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:fc60ed45c43f3e43c0542f5cd8d48eba88d0255ae8721348abe3bbd07b7c992f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337059356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003a1092f017599d6bd9b926a6665d9f421a170164e7640b50d35ab18d34bcf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7d5c957120c4b4799601378655c32b0c96fb41e0e37f282613c951519312c`  
		Last Modified: Tue, 02 Jul 2024 10:56:43 GMT  
		Size: 309.6 MB (309569266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:6416d3c198f9ee28d25dddff8a5d42696c8d96acf02b4e4afebca90022d7bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a840125a7e3d0b2f8a43cd83a2e71b0cf3e068dce1b6c0699ae028ba1ac2a7`

```dockerfile
```

-	Layers:
	-	`sha256:50301fa722c37ce09ede1135550e9a1b864844b9cd57d22716bf3d6ef11fa84a`  
		Last Modified: Tue, 02 Jul 2024 10:56:40 GMT  
		Size: 3.8 MB (3762103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eecacaf8eae18a9ffbfb006039b2a701162815130d3fbea3acfdc25933551b92`  
		Last Modified: Tue, 02 Jul 2024 10:56:39 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json
