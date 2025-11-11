## `rust:alpine3.21`

```console
$ docker pull rust@sha256:33398e1909eae993d43395f85cb102294222bc4ead52a701f72887cb556ff40a
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
$ docker pull rust@sha256:30407d4812d52567be3e5a32623960c282ef51a399a975f17dd706a2afda8e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333363470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8cac8a240961d07b1a7df5b1c19d743ddeb1bef84b6e99810652f2bdc4fb43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 20:12:23 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:12:23 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 10 Nov 2025 20:12:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:12:42 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4829fd6ec818a18915b79d31d935a06ce6a7650320f374a271e301f61ca4d1`  
		Last Modified: Mon, 10 Nov 2025 20:13:37 GMT  
		Size: 61.6 MB (61563889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f147d817f92eb9643fc931229a64b9099d5538806e64ec592c3138d4b7007264`  
		Last Modified: Mon, 10 Nov 2025 21:59:45 GMT  
		Size: 268.2 MB (268157012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:2e99d2fa5f8308c86ab525da27d51e09380bd45426230f083e2561926e1cf7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **792.8 KB (792797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03efddf236e7211faff2fe3d009a8677d8944a6de1f7a497fd3a7b19285ae6`

```dockerfile
```

-	Layers:
	-	`sha256:f445328d6f61a4dd0063d9d6eceda1dafc67449898ad2e68e78424a566b8b918`  
		Last Modified: Mon, 10 Nov 2025 21:44:54 GMT  
		Size: 780.7 KB (780690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12fe9dbae6e1bc8db73bcec82ceed80ec5b33754530ba34058180346d0a370b`  
		Last Modified: Mon, 10 Nov 2025 21:44:55 GMT  
		Size: 12.1 KB (12107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cd5e398a38f1bf162faf4594199497cfa85ddd933bc0616ee9ed4875c8e55b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338404148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839e49041f23baf0a5c21662268b362b1ec3a9d575cfa13594b446294e7872dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 20:16:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:16:51 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 10 Nov 2025 20:16:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:17:07 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f4bbc4710019f0ac18dcc28fb229da2c68fa1e481e903163391f0722c56fe8`  
		Last Modified: Mon, 10 Nov 2025 20:17:58 GMT  
		Size: 59.1 MB (59098754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44318f2d56bddc1aa2fc261a02e096328fce29293ced76c282f7285e66492d1e`  
		Last Modified: Mon, 10 Nov 2025 21:48:03 GMT  
		Size: 275.3 MB (275313041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:ec3f4dfa0bd3f6e2ab8062510765d251bc1bdce33f45b87643e314a2f2ea892b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d02781fc15785000d877753444e32000f28271aa0b422cf3253ada3de0787f`

```dockerfile
```

-	Layers:
	-	`sha256:a11f3b418ec410aaa7bf863fdbb5486d1cd8398dad1821695af0dbf26c35bb15`  
		Last Modified: Mon, 10 Nov 2025 21:44:58 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e6e503fa2ad5b12320b91af43fa6f193615708b002376dd521b5573a17af1b`  
		Last Modified: Mon, 10 Nov 2025 21:44:59 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:81f043b6df356460f5f67f165b1e3ba12a11698915d2f357d6a9044ff6063308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.6 MB (356590766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4031b471f6ec09121efa28f45ff959ef0a2f7d5628c8de9a981a4383e69a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 23:09:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 23:09:12 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 10 Nov 2025 23:09:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 23:09:39 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2049e525309be6cd063f98b68042c1685f0b1aef990caaeb0a9f3a0a02c800f`  
		Last Modified: Mon, 10 Nov 2025 23:11:14 GMT  
		Size: 59.0 MB (58965848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f23c595bfbbcdd7a55b2a7a9e7d74cdc3ff77dc9b59412e771a5a362961bbc`  
		Last Modified: Tue, 11 Nov 2025 10:39:21 GMT  
		Size: 294.1 MB (294050843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7406e1b8838f132e4cb517441f2a05ebe92b118de20a53aa0e4d8a99ba80035d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.4 KB (805387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912cf4d0e65609b606d0999255b9e8e69aa891c4bf71265e739982044436451f`

```dockerfile
```

-	Layers:
	-	`sha256:3789ae44dd01b9969105b73e9511a1b83135a973593bfb1bcd58bf1963fd029b`  
		Last Modified: Tue, 11 Nov 2025 00:44:39 GMT  
		Size: 793.2 KB (793234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20acb991e37475e516447ff888a016ea82287c62a6632f696a374f97be23eef`  
		Last Modified: Tue, 11 Nov 2025 00:44:41 GMT  
		Size: 12.2 KB (12153 bytes)  
		MIME: application/vnd.in-toto+json
