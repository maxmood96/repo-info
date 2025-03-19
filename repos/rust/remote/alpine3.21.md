## `rust:alpine3.21`

```console
$ docker pull rust@sha256:4333721398de61f53ccbe53b0b855bcc4bb49e55828e8f652d7a8ac33dd0c118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:813376c206852d4250641eb86720c04fd20fbc6547d1a030c93a45b22a1303a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304363971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657a0afa845621c92e5fbe5bbcfdd0f38fc8ac517bf12c4bc3e6a440813d7b82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80256bc0c85619d177cdaa3c1034795f0ca162e7cd919f4e0fd9eaebe67b220`  
		Last Modified: Tue, 18 Mar 2025 21:25:12 GMT  
		Size: 61.6 MB (61564890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7e86201c32622cb2b88533e8edd399c97cb04d34183aa120071f151d19cfaa`  
		Last Modified: Tue, 18 Mar 2025 21:25:14 GMT  
		Size: 239.2 MB (239156834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:70b0f573882957fbd4d1b923d99758a218538426691c0d4a91c8f70218bf2052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79614d0da8b095398071388d90203f8de83f345c707a416712219512107e067`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d04c386e92954684b722e0908cbfcfe020c185b4c3e527ab029135f776172`  
		Last Modified: Tue, 18 Mar 2025 21:25:11 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acf88de5f72a8e0d54579925aa108a283409dce5e8a2ecb984b92333ba48656`  
		Last Modified: Tue, 18 Mar 2025 21:25:11 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8eed1d324a486196374b67025fe0a8a724245c42d0c3687fa8d6fc953228b9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307461385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3c705bafc50e801b1c69e6a17a3ac51bec2391ec1201498e963cb929f3ffd0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd1c532d4bfc13624585c1d7d362bd1c5a7fae473cac98c7e93678de08ba318`  
		Last Modified: Wed, 19 Mar 2025 01:06:44 GMT  
		Size: 244.4 MB (244367129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:0d544943f2367ce30379bdb562d69a08f427fce4c4ce56cbbe68bbe1e847e443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957717d341b608878af795fc77326bef5b07ff700afb0662c7446d565c90429c`

```dockerfile
```

-	Layers:
	-	`sha256:ac322500c04c9ac2eb1e898267b664beffb18dd7d72874dceed9a6d516cfb673`  
		Last Modified: Wed, 19 Mar 2025 01:06:38 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa03e1a4a468a2ab163a023775e0effb6f111a27901d3f6533c4e2db1f16f76d`  
		Last Modified: Wed, 19 Mar 2025 01:06:37 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
