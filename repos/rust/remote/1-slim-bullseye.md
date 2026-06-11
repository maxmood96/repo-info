## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:ab995cf540fc78d921dc4a41afa4dbb5b2824a24d2d18b519708df1287f78ef3
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:8cbe059264774738bbcf635909d4e1d5aeacf696855d02973873dd1fb4a85d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305631328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976df5bae2f2c2878d7c009500697fa1f4a0c9cc59b7226827cf8a0b0453c70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:13:16 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Jun 2026 01:13:16 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 11 Jun 2026 01:13:16 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe8f0955d10d6be0e7883d017d9ed1d06c6f631706616de1fca5aef4695d0d`  
		Last Modified: Thu, 11 Jun 2026 01:13:59 GMT  
		Size: 275.4 MB (275371073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:bbca23426ff2ebec88fe2de48425cc38b8f7e575cbcd5f3945d34eea7fb228a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb74cb529c70d9e32cd523f1616bad8dd8a18208072c747da5f5abf1877975d`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e5292e8d33fe491fceb1cdbe9b49677096dbfb0a084ddf8872d16b09aacd8`  
		Last Modified: Thu, 11 Jun 2026 01:13:53 GMT  
		Size: 4.3 MB (4312026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0854193217d241f150281e0ecc0e1f387a588d5fd2be14106b0cace796efeb5`  
		Last Modified: Thu, 11 Jun 2026 01:13:53 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:86440f012839cd786237d0776b09b6fc8b28013738b8c79c6f49547b8aa87767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325643266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4fd34e7a90f8c9e48dcfc9a6289da4ab377b900db197efc0a724126ebec48c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 02:38:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Jun 2026 02:38:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 11 Jun 2026 02:38:32 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9af1b9418ebfa3b3e1bb5cf3fbe460857fae69723843220eead8ae5afefaba7`  
		Last Modified: Thu, 11 Jun 2026 02:39:15 GMT  
		Size: 300.1 MB (300090424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ad39f3b5335be943efd21f3768519212b8602e57ba24b109ce1e774d87a8cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f582ac53eea2f9c08cce0e83f087ed793fb0153601cf69a0032c6dc74705f63`

```dockerfile
```

-	Layers:
	-	`sha256:e63e9caec34f340ea9895862c62ae477a056295acc9e56d29dc44e3ed9a2e4f3`  
		Last Modified: Thu, 11 Jun 2026 02:39:08 GMT  
		Size: 4.1 MB (4120019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4078e2ade75f3cdf68d119d8159dac8fea8ef0493603541b99141ddb2ad6e92`  
		Last Modified: Thu, 11 Jun 2026 02:39:07 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5373e9b6c1a43ecaa9b660bc38b1a57343a0a34989c6d1ee4f9b39df69bbc5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264674050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b486117abcef445090771f0c561a6e1d6e72e6bf438c7964ee7f8dd053ac0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:17:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Jun 2026 01:17:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 11 Jun 2026 01:17:05 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd046107d0dec608252e2504b8058ea7824bad63bdc3ebaec9130df2d7dfb69`  
		Last Modified: Thu, 11 Jun 2026 01:17:41 GMT  
		Size: 235.9 MB (235927896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:eb29ac8a3df5ad7fe8b5866cea4bdc9f58b3a9a11f77a99d3c5c33a145892279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458b89be76a35680dad91b271c2231956142b0b8d031060b62d74ffdd4457ad2`

```dockerfile
```

-	Layers:
	-	`sha256:a656a900f0a05d2bb43f6a293087425b7a9c2d051118f6bc21afc3d7a21a78cd`  
		Last Modified: Thu, 11 Jun 2026 01:17:36 GMT  
		Size: 4.3 MB (4308415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e9534b638586b0a67d0535765b27c03067f1d8584bcd597e68f7109ba1735e`  
		Last Modified: Thu, 11 Jun 2026 01:17:35 GMT  
		Size: 12.8 KB (12817 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:db52755cfbfbde79158f4e8614ca64adc908f7fa0c3771161243fedc94a59bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333479346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e48ae82d224018b3a4ddc894be1b4ab2634af444059f09ba6360976a95ea2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:15:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Jun 2026 01:15:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 11 Jun 2026 01:15:00 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9727809fc62f601eff99a08952bf87375634b9e59f5cd4a16d4ef724743de127`  
		Last Modified: Wed, 10 Jun 2026 23:40:14 GMT  
		Size: 31.2 MB (31194385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61865dbcf6fbf81e5c08f9dfe18fd88399e8a482eb64ff474e75555d56df3f5f`  
		Last Modified: Thu, 11 Jun 2026 01:15:42 GMT  
		Size: 302.3 MB (302284961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:256658e24a5bcb11f8238a51a8e1575a42cd9286402a1c44a7a21787e32d8fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db51dd809c2fd0e8b1768c0c562bc268b24ac2127bd69b1f2d33da7bf86bb0f`

```dockerfile
```

-	Layers:
	-	`sha256:9dbdbbb97be544043caa4a0987ad03b1fe21d822245a3a1850782fc0c8d27710`  
		Last Modified: Thu, 11 Jun 2026 01:15:36 GMT  
		Size: 4.3 MB (4301768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65f81eb6ad3108e6ef3583551757ac762fcac1ade7e56d377f7ec8d601a20ae`  
		Last Modified: Thu, 11 Jun 2026 01:15:36 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
