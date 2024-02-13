## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:056a9f0d23db1059e49099f4b80177ca633ffda42bd62ba26ffbd158849db853
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:7182695b4df05e6e102201259ab93e5f9eaf11b3735f0355620a98064af825d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279371843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c221e464aaccc6fb9374d2cc10b8742f3a154d7211985813b70424ce40ab7d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Feb 2024 14:18:11 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Thu, 08 Feb 2024 14:18:11 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25691eb7d62a1dba4ac865e10798b95531a11fe88ea735833ce8f5bd2ffcdaaf`  
		Last Modified: Tue, 13 Feb 2024 01:55:31 GMT  
		Size: 250.2 MB (250247752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f399573b602868394e06881e77e4894fcae039f9658e6f00c2d358774ba12ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd36c569f3aa32f8695f38aff18010546e2134f82b63aa5a3fd089cec0d0d35`

```dockerfile
```

-	Layers:
	-	`sha256:2b2f594ebe8b1b09d6bb9f1e71ad99df9ae33f8f00a63755dc2233915be8fd0e`  
		Last Modified: Tue, 13 Feb 2024 01:55:28 GMT  
		Size: 3.4 MB (3412394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06070e00f404e7798ceff6c9c603333d5be858c492bea0b5479d606a03d6a5b3`  
		Last Modified: Tue, 13 Feb 2024 01:55:28 GMT  
		Size: 12.7 KB (12702 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a4b18bcc9da8a61850144e393663136fc451942ac883f78201c6376b95e67e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288208762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b004650ca191f0e6bd22f08cc46dcac5f31d4eee2a8be345b926a92b240825e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94728089f9c14ab4ada9914bf55a1bc19d79b8f6ba989b1d73c73f3e11253c57`  
		Last Modified: Fri, 09 Feb 2024 08:26:56 GMT  
		Size: 263.5 MB (263467197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:334232d79d2e89aa152bf23c71646d6d0d637faa9a66273f047e3142ac738545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3265361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f441d131fc95f0f75e7b0b4a7725df7ac5705d1ffee57b7bb748b43e97b35`

```dockerfile
```

-	Layers:
	-	`sha256:69bde84cb379829f554e62ff22e0801bb3e8265e420a29800ef1df0d6c246072`  
		Last Modified: Fri, 09 Feb 2024 08:26:50 GMT  
		Size: 3.3 MB (3252724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde75d22824ea3a9405eb89d68fa4415952f76a2d45e680802c5a0b0958d1fdc`  
		Last Modified: Fri, 09 Feb 2024 08:26:50 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5b9cfa5c1aef8025da326fb4799fa3cd8f20d4f904e6c64ef7d02f65e8dd0729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343880869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5cb3960cfde7b3455ad5f5e9b47d97f6194a09821dcd99eabdc366172c8683`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4141db1ebf1f056a8ccb1eb01dfe2df81fdbad4d50b865e9da72621b41755e0d`  
		Last Modified: Thu, 08 Feb 2024 19:35:36 GMT  
		Size: 314.7 MB (314700037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8454d9c7fec8ec96fdb7e23886348373148d462d24be6c9299fb6ca207559257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3444524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e42ba5c65ae3fbdb102ddeb5cf93618930912d10911e63a483659c396c799e`

```dockerfile
```

-	Layers:
	-	`sha256:c99581407cc43203ad3ac35e04cc0198a8dc76b02a932c6242adf11909042fd1`  
		Last Modified: Thu, 08 Feb 2024 19:35:28 GMT  
		Size: 3.4 MB (3431972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d6b461081532033c3a2be2f96cb293e70ab7bb0223378eae4f6595251090ea`  
		Last Modified: Thu, 08 Feb 2024 19:35:28 GMT  
		Size: 12.6 KB (12552 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08be9c2409e6841c95896f39f7855d34c59c9de7621941ccaede1abfa3bd4e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290933200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaf3058683ec02f2ebe13612539d546eaff3ff30a44a3d94a6e9cb3eddf27df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Feb 2024 14:18:11 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Thu, 08 Feb 2024 14:18:11 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb63a0fadee5f6ea59c829eb00e6efa7e87a726cb581bd131a497ea977c8c05`  
		Last Modified: Tue, 13 Feb 2024 01:55:46 GMT  
		Size: 260.8 MB (260791391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2e4999074215f5f2cc85564067b7ee1a8cb1172812621a960404d0cb78d9ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3408124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f603ebb5793c1b780d4f1789f9d5b312e5894139a9476db7a905a973e4d1895`

```dockerfile
```

-	Layers:
	-	`sha256:9352a633392395ce0614693ab5d53ec25653c4c592768871528c42ab932f0d15`  
		Last Modified: Tue, 13 Feb 2024 01:55:41 GMT  
		Size: 3.4 MB (3395471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1eb9744323dbe937d33c93370c2017bb946264590d7d9aacc3ceca7b319514`  
		Last Modified: Tue, 13 Feb 2024 01:55:41 GMT  
		Size: 12.7 KB (12653 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:272e80c283cc9caef82f8369314b611ea1a9633dcd366f7eb9c6d88ba7f1ed3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294662076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4251946d203250555c559bdb411e88d0efa3c74f2b778302af5ee425ede4f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:41 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
# Wed, 31 Jan 2024 22:29:43 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954f1193140da2cb3dfc7a19a75cb4a555f46f55bad12303e3cb920ed47756c4`  
		Last Modified: Thu, 08 Feb 2024 19:20:58 GMT  
		Size: 261.5 MB (261519159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:06839e778364ae0fc8f7f08f5d6baa0760de6845281caba8eda540edc712447b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3401517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1224815e3b9dd7e7f2a18386cc5c437f3b476352415d598b3c95b11dc38e1`

```dockerfile
```

-	Layers:
	-	`sha256:682a528fdf00bdd80024a81440ee03e3b3109d5e4110803cf9427527afe0f4ec`  
		Last Modified: Thu, 08 Feb 2024 19:20:51 GMT  
		Size: 3.4 MB (3388920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6a3762478507b660c8f2c2a6156d134b22e1a2a153a49f96cb97e943e334ca`  
		Last Modified: Thu, 08 Feb 2024 19:20:50 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json
