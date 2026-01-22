## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:e0b90aa99c59ee60d86795dda9b039b44c1ee48dfd2b6ae1cb763a23dae2e7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:b9d6e2644630f9d438d3c311cbc89522e94841e586125d772593f6015fa04149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329780099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83bd5211ebad2b5f61aaa49631ab8b8af72742ae7a82ce84d25e600eeaeedcd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:01:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:01:56 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:01:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:02:13 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177d0dfc2016e7c20041f6c38dbb8b153dccf37354b81fb03afbed95e02d3159`  
		Last Modified: Thu, 22 Jan 2026 19:02:48 GMT  
		Size: 58.8 MB (58781634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223890baec903b7178ad2c44810ed2f0a7221835bae86a69fe608ffe34010b6`  
		Last Modified: Thu, 22 Jan 2026 19:02:52 GMT  
		Size: 267.4 MB (267371409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:8583d4db91aa1d582df3c6e841d99b59dbe3f0c286cd93b0e76e40116f746e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f284e978f02e4eb8abfa26a1bfcc26b586614eb57e99101bf5862c3367e30b67`

```dockerfile
```

-	Layers:
	-	`sha256:f576b35464627e0e2a202497e2d523fecda7e63d195b60e2ce2df1411fc14e27`  
		Last Modified: Thu, 22 Jan 2026 19:02:46 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2408facd25b8c604df8bfd90b950ca5283ac85570eff0b66201237c7712e5b71`  
		Last Modified: Thu, 22 Jan 2026 19:02:46 GMT  
		Size: 12.2 KB (12185 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ed029ed19899a80d6ff5a509a042e9340a694b64b654e829f36aff06fbec0071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333443876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2ee8056f4de80a2cc3d92009088155df9acf5c696f68b1413975ec3f1c1a3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:06:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:06:12 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:06:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:06:27 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afe805d6304fd6ad30ff95c9ebe269ece6932443ee5332795474423d8c1d17d`  
		Last Modified: Thu, 22 Jan 2026 19:07:05 GMT  
		Size: 55.6 MB (55558367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993cb96b7ca960d9aa243caef5038dbac43ef509f7692332785510bfce0f78ae`  
		Last Modified: Thu, 22 Jan 2026 19:07:09 GMT  
		Size: 273.8 MB (273796132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:108b389d56be115d246e030a7ff2c8c4accb4e09a8f644b2d93dd6132cc98a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0dddb369c38def524aa84dad2cdd76abc45f2b76b7a6317ea3a82f69d4f81e`

```dockerfile
```

-	Layers:
	-	`sha256:1a0220f90c793935201aeaf7806da54a649b3ed3445f20a156a87715df563477`  
		Last Modified: Thu, 22 Jan 2026 19:07:02 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660eb6a030f3d14b7b5e5e049a872d5e72cfaea0399ca6f91ed29425c4fdf7e0`  
		Last Modified: Thu, 22 Jan 2026 19:07:02 GMT  
		Size: 12.3 KB (12304 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:949fbe47dcf81a3fed6d9f75c0434ed8c61a1b1634be43a84fffd2b8979d0c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352562537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650f8a4dc0297e8548c83ecf401d0fbf8c439495fb4d833f42abc528ef1bfdb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 19:39:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 22 Jan 2026 19:39:00 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 22 Jan 2026 19:39:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Thu, 22 Jan 2026 19:39:30 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baee8becb92795c9702954f412fa4b347e40e427c90401ea92ae176a13fe26e`  
		Last Modified: Thu, 22 Jan 2026 19:40:50 GMT  
		Size: 56.6 MB (56619643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d6b385055a0a0c66ccfa0816d1bafe9bc8a45e398f43134bc6b4528165c524`  
		Last Modified: Thu, 22 Jan 2026 19:40:54 GMT  
		Size: 292.4 MB (292367331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:81f9a1f4702b97f61c3bb50cfa10e72182289a3d2b4251e2e69e0c0d566fb1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e880582af86ba88151a9bef89cd2047fd6965637a435992f0cdec9ad0b9640`

```dockerfile
```

-	Layers:
	-	`sha256:0dfa0a48175bac4058023a7d31dcd707648ef56e05269ede09c7f9a8a0859ae5`  
		Last Modified: Thu, 22 Jan 2026 19:40:47 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36e4d85238f17e791b7df2800334bca0e4c33301ab77edcf12bf26b7b47a839`  
		Last Modified: Thu, 22 Jan 2026 19:40:47 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
