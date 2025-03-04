## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:f0cef6c65992995b1c7816cb667de95799852e3fbed9d06f95855cbc512a0fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:6d824fef86a8532aecead5889d49d432d19e0dd58b958266c994cca9eb7a3357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298102813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38e59fb99c1014ea6d250d396bb9bf55981f1d69fe17ed05047b90cd119ca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0430b4a2b30329b0c06034d1df61c2f3533c436834a54b76def8756d804d888`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 55.3 MB (55315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7dd06f6e434e3727cd86155430a51568846533e3824548334e20f1078e28`  
		Last Modified: Mon, 03 Mar 2025 21:17:31 GMT  
		Size: 239.2 MB (239160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ab2a41c3a86b0e8de97e1cff7ca3624a6e69e478c7c29615df5979d5655d03c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e987a7ec625942a721de02dcd92bf4ea3f7481ee651c6aef639e3a2f3f16ba`

```dockerfile
```

-	Layers:
	-	`sha256:4100e90a822ec6152c54ec22e8ce0b4cfb24694b82b0d9252e191958ce4d59cf`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca3c1b9b1144fd4038e19dea5e9afef77e4732804442cc1813ffcbd1c7289e4`  
		Last Modified: Mon, 03 Mar 2025 21:17:27 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f91c5c68a69111314bb721b7bb75aaa4b310b9ef676f2591e88769bbbb3bd933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301363171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61566cb96efc54b3ee29f6409c0e76059ca7b3c261b99a2940c188c54c3a66c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bee9c91c68545cb9604a6baaf13f4c921f1a8a851437cc7ce63f942e113d`  
		Last Modified: Mon, 03 Mar 2025 21:26:24 GMT  
		Size: 53.0 MB (52950488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e7300919f154807a1ce8bdaa868228719c39a95b4c276a758f1bf480b361`  
		Last Modified: Mon, 03 Mar 2025 21:26:28 GMT  
		Size: 244.3 MB (244321518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1e4651facc4a66b01c40f8bec063469f936cbf603daf477c1003e794040d3e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb6c0426bb32cbdd133d31ad5ed10820561b72d66e1d95f332bfb42d012779`

```dockerfile
```

-	Layers:
	-	`sha256:183ceb0143fb3784d416af0d9e6e49059191e33606b5db6d715b5666f0fd139b`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe75a1adc68e5615e04f2ea23b7e198a996bb1378319d115d5ca7b6fbef7602`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
