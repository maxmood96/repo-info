## `rust:alpine`

```console
$ docker pull rust@sha256:71571f70b9040894fad9194ab3bc70ca1ccd705e1af979d8d79be74fa7ebcfcd
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
$ docker pull rust@sha256:ed5d156ac0fec2b124529725bb37b2fdd771dd16d7e0031f6cc0c853780da8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347054180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5076ac0882cba426ebd8fce7f87577ecce40d37ab855fab3df6ed3360d79bf4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:29:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Dec 2025 19:29:32 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 11 Dec 2025 19:29:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:29:50 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826fcc9b6aab2531921c95e1f007e9954b5afa6fe5c7d32dbf6be1be9eb2edd7`  
		Last Modified: Thu, 11 Dec 2025 19:30:53 GMT  
		Size: 75.1 MB (75119123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c190384301592e25394950f24863523b1b1cc76e7023d7224a0427ee9b355`  
		Last Modified: Thu, 11 Dec 2025 19:31:12 GMT  
		Size: 268.1 MB (268075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3d675e7415a326c010d03ac8317b88ef5ac2ac1ad2e6409d33b1c92debbd69ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1021805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ceafd563a2506a0ed0e70084455588e13a289a6274d81db058d9328a2ee36e`

```dockerfile
```

-	Layers:
	-	`sha256:c662d44b36e00b726f8460a0f8b3e940b8053f38923af4c9a37f5d0b4a68ee38`  
		Last Modified: Thu, 11 Dec 2025 21:44:45 GMT  
		Size: 1.0 MB (1008415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea5bfbd0413e6bc04935868032354eff5ce3d133b811fb3c9bf089fd133af9e`  
		Last Modified: Thu, 11 Dec 2025 21:44:45 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:72ed726e184c05475d410d22bf059d1dc60133adac7dc7baf9bc18b64287119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345777914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f4173ada48295568102571d0f07c6ad6c2448cbb18e0027510f35d0d49941f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:37:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Dec 2025 19:37:28 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 11 Dec 2025 19:37:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:37:44 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451c20bcbca724f81ad923bf44f720421812561e18b3953fb2a2fc8fa8dcd741`  
		Last Modified: Thu, 11 Dec 2025 19:38:38 GMT  
		Size: 66.5 MB (66542726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55983d95e3784368e2ddcf8abd698fac8b51111154625fead15b520d12ae6e4`  
		Last Modified: Thu, 11 Dec 2025 19:40:57 GMT  
		Size: 275.0 MB (275039988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1b66ca41ccbd4bf3f5cd3a1ead06ae8752cae58c35a1c19b2abcc74f52e286db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1081031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801b4b6346f66a4dfde36d8998384b8a3b407bfc996f5ac19b23c4096553166b`

```dockerfile
```

-	Layers:
	-	`sha256:8a1058f8f5604efe07d5e3a0dae47c7f8e815132fbedf20abfb30a47ec21d31b`  
		Last Modified: Thu, 11 Dec 2025 21:44:49 GMT  
		Size: 1.1 MB (1067474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3578b4db1cbf08c7d7db0201f163395c5b7058eb28241eb02c0a595dbe595a4e`  
		Last Modified: Thu, 11 Dec 2025 21:44:50 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:17c4ca8ccb4dbc5f020830fd7299f7db77df1293f4865a188b3c93d87af6621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364207022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d05322deeba9b63f6365fa97baa74acb64d333fccb797a8fda51a8db1f84d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 18:08:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Dec 2025 18:08:55 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 09 Dec 2025 18:08:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:38:59 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ec2bf96d6d60450c8cd070bacc238ae1a3d76f072311731f95632810b1772`  
		Last Modified: Tue, 09 Dec 2025 18:11:53 GMT  
		Size: 66.4 MB (66425895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d6598a828f2b8c6dd4d7bf728d680d7b3d5ee2d355a7221772009929b78c8`  
		Last Modified: Thu, 11 Dec 2025 19:40:52 GMT  
		Size: 294.0 MB (293954110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e738cda703884504e0734ebe841fa4ffb6ab334c7e19fbdcf587a4cc474e88cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6169c3b348fca0ecb6a58f0585c0ea09daa7d6bd60354beae7383f626ff80758`

```dockerfile
```

-	Layers:
	-	`sha256:d8853890e2fc24ed30bdd87500b27172044d11878f309d1a9d5d33b4216501a3`  
		Last Modified: Thu, 11 Dec 2025 21:44:54 GMT  
		Size: 1000.8 KB (1000761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7a09ee54cff813adf1641e6c0f9756407670e45f3a24a0a926d7884cbaeabc`  
		Last Modified: Thu, 11 Dec 2025 21:44:54 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
