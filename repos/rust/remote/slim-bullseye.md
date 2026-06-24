## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:290a6e49a53e54df34abc66be10c77af6e446b88f23dd62ea5b1793ab04e040c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:1a88b350852c8f51d9f804d7d63426926ffd413230883e35682c6c2d5e301924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305630655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f904130913a7794f462de872a226f4471d5ba2a52e66c64b6978462a5216f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:12:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 24 Jun 2026 02:12:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 24 Jun 2026 02:12:00 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeca8b38ad869caed395dc9a8a44d720e630a3534b2a01e7a3dbff5394d694c`  
		Last Modified: Wed, 24 Jun 2026 02:12:42 GMT  
		Size: 275.4 MB (275371208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a47a489dccafffe3de5fcf0dd1eac399a11e638d96dd0ea285cbdb4fc65325b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb47a448fce594fedf9c2453c73693771de3098eb964ba931bffeaf537b476a`

```dockerfile
```

-	Layers:
	-	`sha256:ee24a328969dc7f9b59983ca3af0a024eadc28cb1ee3aae22d5ab25574c2fbd1`  
		Last Modified: Wed, 24 Jun 2026 02:12:36 GMT  
		Size: 4.3 MB (4312026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f201b6f2b94a336a3b6e76627f87d2c0b0d3360bdd94b5f1167f931000e5c6ac`  
		Last Modified: Wed, 24 Jun 2026 02:12:37 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b74f052ddd1d9530a74df880ea9210d48cd0e5b623bdd7b5b2a5d7d5b6495c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325642355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53beb44bd1eb8a2f4cb483e59b85cad66a7254079d029a329037811e92c23a9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 03:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 24 Jun 2026 03:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 24 Jun 2026 03:35:32 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8ec7789c331459e48d19f428fbcbbcb0b3cc1497798c19c3025d746ad6b457af`  
		Last Modified: Wed, 24 Jun 2026 00:27:55 GMT  
		Size: 25.6 MB (25552772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cd79b199ecb86d55907f29b2dc707f8db8448d8e38b76679691fa98cc059db`  
		Last Modified: Wed, 24 Jun 2026 03:36:12 GMT  
		Size: 300.1 MB (300089583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7e1b042c1c2ba296a3b6fe366898b70847cca5daf397c768a1077ead5afb038c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249722d535977bb6a0c67f4e072e71e500a2bd77a619a0e97baf3b3d99d65c`

```dockerfile
```

-	Layers:
	-	`sha256:bf217f17f4ae42989573d72d6f933d5c0121f46ff203cc8831fb92a17bc03822`  
		Last Modified: Wed, 24 Jun 2026 03:36:07 GMT  
		Size: 4.1 MB (4120019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec83bd741debaae5370f716ef44650f3f8eb67ec92e936672d888e520658b65`  
		Last Modified: Wed, 24 Jun 2026 03:36:07 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:598527d906c40c7d69ff5b896f18903a67b3ad5c2508780d2897408f545cb460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264674961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277343ac637429e293b320cd849adc8f37283998bd4efffb22a1973ddbd3392e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:18:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 24 Jun 2026 02:18:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 24 Jun 2026 02:18:07 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf76275ac570989e033be61f4e2339d12266adca5fa9dcb127be9c82cff9a23`  
		Last Modified: Wed, 24 Jun 2026 02:18:44 GMT  
		Size: 235.9 MB (235928035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:879a7513706517d478dfb2eab1b125923559de38600490bb2068c3b801646d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941010cbd463cb173776fff431b18f6ac2efbd1ece4ecbb1cd607e85031b353d`

```dockerfile
```

-	Layers:
	-	`sha256:8319d6dbdde24c2aa5d9d02f72757f08c18a12c732be2f73288d0909b5c8d035`  
		Last Modified: Wed, 24 Jun 2026 02:18:37 GMT  
		Size: 4.3 MB (4308415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb2e5e6de1ff522662ac3b3584fa150f7c6a8690a449eddce58b0b50833bec0`  
		Last Modified: Wed, 24 Jun 2026 02:18:37 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6098a430c4c95ee04111d48c4d78f9bd83451fad4db896dee4298a13b94e1eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333481417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f28961186ffe0c3b1cadb6c02313c723f474c5c26af885fd757a3fdda98c59a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:14:57 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 24 Jun 2026 02:14:57 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Wed, 24 Jun 2026 02:14:57 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:edbad50f4a6e85b8608c496472f5f48b2e108ebbad0ca8f7c81784396f0c79d6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 31.2 MB (31196135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934647cabf51ce76a8299024215deb177c0e86cf7fe88365af2b7ae15933c672`  
		Last Modified: Wed, 24 Jun 2026 02:15:39 GMT  
		Size: 302.3 MB (302285282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ca1f18bb42fa5d4e18b2bc6356f2994233d8c68df1d9f4024d2d975841f8b53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6d0b21e1a4084cf6a4e0323adc11ce21547946fac3216a1e077c9fadb8f3b`

```dockerfile
```

-	Layers:
	-	`sha256:aa876f88ddfb74995621e0202b02e7e42a03fb7274a77d960865a9a25d801feb`  
		Last Modified: Wed, 24 Jun 2026 02:15:33 GMT  
		Size: 4.3 MB (4301768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b46e8712a941df1461bdf6cdaa43429157332731d0193901e2ca1b1343b21cd`  
		Last Modified: Wed, 24 Jun 2026 02:15:32 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
