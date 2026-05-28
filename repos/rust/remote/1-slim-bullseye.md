## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:2f7050b70a1abf82adc75002c754b5508ffc5494b981424547e6473d9fca6ebf
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
$ docker pull rust@sha256:ad7564b6124a6dfda0b3ecf573eb35bb496ff1f0aef3b9bb014ad8a946153161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305629130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c80c52a0ca1a2a06466c3429a874b3cf45debd3b15782d2050a84f86a8ee5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 28 May 2026 21:46:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:46:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:46:49 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612825230b261fa1a5631b760c1a4cb326a79188f0a73d630e8da44002015d2`  
		Last Modified: Thu, 28 May 2026 21:47:27 GMT  
		Size: 275.4 MB (275371532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bf4dd00c4fcfcbdcb3ecb5f4aa18d7fedd380d47ee641e88ead7fbac71a71d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259abb3c09585a278c8922141523ae132e8551ef5fa5cfc234ab93ed2a35ffd0`

```dockerfile
```

-	Layers:
	-	`sha256:e91347514d2651621e2586ad5ebd825b8ea6de6468c3531815529eeffd9ff1e8`  
		Last Modified: Thu, 28 May 2026 21:47:21 GMT  
		Size: 4.3 MB (4312022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362a4658034e34d2bdedb724f6ab0f8783218dadb40a90dde2bcd570f03da6c5`  
		Last Modified: Thu, 28 May 2026 21:47:20 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:c761748512094aa8f3169b39ec2afeceacfdc9ae54cc80b3f564317780ccb9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325641572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a882985e2269f6a66d6c0ca9b1eaa714ac1beb4c335de709de6fbc38d480ac34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Thu, 28 May 2026 21:39:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:39:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:39:51 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133d25c7e610181e78a1fd6137f6459bbf16b3c936c039dcaaffe2f1d5f9c56`  
		Last Modified: Thu, 28 May 2026 21:40:35 GMT  
		Size: 300.1 MB (300090634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:aaa2498385983d62f72ee0210325579b8521cfe927cd99ed856cb2074b71235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fe2dd9359a728594716f215fb19a6892fb1190db820bcef493287accf0574`

```dockerfile
```

-	Layers:
	-	`sha256:607a5546c737749e4c3fd6dce7fc8852217a7a141c196206887e6a9c07e7e5d0`  
		Last Modified: Thu, 28 May 2026 21:40:28 GMT  
		Size: 4.1 MB (4120015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34d77a18835d2e339b618d7f6fb00f2f3f5396a40a5f0b561b957c9427fe522`  
		Last Modified: Thu, 28 May 2026 21:40:28 GMT  
		Size: 12.8 KB (12792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9d8e85c4fd091ad239252b5f7f42db1da517eaeb238f0f49973af45057e78dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264670067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba9571941e864b1baada54f3606bd1e6ae15b3ea41aefd0b98f412c49eb77e2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 28 May 2026 21:45:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:45:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:45:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cd63c87586aaa9de93d6608b86a212f30715e367a3cf3ccaa5d55cbf23edf`  
		Last Modified: Thu, 28 May 2026 21:45:48 GMT  
		Size: 235.9 MB (235927095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f4801c5ad33fb62496bd738c349f688d8cb28a41da9b2c23e1615ac82b90f705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ab2851ee243b95faabb26d2625c203fb9cad5b24dc8c244dec63cddb4b3adf`

```dockerfile
```

-	Layers:
	-	`sha256:346df1bcd00e1d85a0d6479736eec6f83512c871b0c6fc03cd16e421a0e41b2b`  
		Last Modified: Thu, 28 May 2026 21:45:43 GMT  
		Size: 4.3 MB (4308411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd7894732c4324ef8bd32e5b0c6ba089d749368c7270d22fa02237a454c56c7`  
		Last Modified: Thu, 28 May 2026 21:45:43 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:739b5466d19ae14f772d7857c4673d61c6374ea1516fb8280853f69472aef203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333478044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028be6b345b205262d0d00aa6d6b3c6e043f6aec5f638dfe40895f1045a7319f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Thu, 28 May 2026 21:39:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:39:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:39:49 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2f6471dabb4ec95bed651099aaba5ff48a4c6332742cc6af6c957b880b8a6aff`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 31.2 MB (31192759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1157db362fffd99582336a6c1378ce01d2ef7e6b487e2e533ee47278c18a8b`  
		Last Modified: Thu, 28 May 2026 21:40:35 GMT  
		Size: 302.3 MB (302285285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6d81d1e4cc1001a2082bd14bd5635713a86cc75f545b927981e0e6369752e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7512ac4ee78f2eab5fa9c2274320cd39abc38dcf39e6453b6b9869118f59e616`

```dockerfile
```

-	Layers:
	-	`sha256:108c16882f75dba1fd940b228cc6509c402f0511324ffe2340031b3274ee316f`  
		Last Modified: Thu, 28 May 2026 21:40:29 GMT  
		Size: 4.3 MB (4301764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8021c2713faa9a00e842d513456b0dd60f71d5db92eb963250b7417906735381`  
		Last Modified: Thu, 28 May 2026 21:40:29 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
