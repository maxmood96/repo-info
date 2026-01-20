## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:361bd4bdc7028acc35dabe70b482765758bb6e3ece6a5c7b979b22fa58e14cbb
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
$ docker pull rust@sha256:bcf597ceebef019ccb385f0c7f80831a5b26e9671d52a43fa58adbc81f037837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330484754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b64065fe2757ccbd222542f837379ca7e11990ddcbce37d7d373cb01d091d58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:28:24 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Dec 2025 19:28:24 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 11 Dec 2025 19:28:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:28:43 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb128a231f9815a7cb89012ee1dbe45d1d145dd0fa9a6ce486a28a56167de0e4`  
		Last Modified: Thu, 11 Dec 2025 19:29:19 GMT  
		Size: 58.8 MB (58781610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459ded0301fc361f8accbec03b43f9eaab15dab9de54d5e2b0c9b2d3df01cc0`  
		Last Modified: Thu, 11 Dec 2025 19:29:23 GMT  
		Size: 268.1 MB (268076088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:93ed8e5050ec85d730151e07c9c8771e273f26facdee9992c47c54891caea1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9764c9254c37467c99bba4c7e1045974e0e5cc273fe76c55b3a803100472d836`

```dockerfile
```

-	Layers:
	-	`sha256:a1e2ee26674a73700fb08110a2829dfbda4b33b0542deeb24af847127855ac8b`  
		Last Modified: Thu, 11 Dec 2025 19:29:16 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056fe47dcdce858a12fe0a1a34e2f0aa08837ebe3a314cc5fe8871f7d168b06a`  
		Last Modified: Thu, 11 Dec 2025 19:29:16 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f169bc6135653a470c142f5f4897b23a49eacadff366a4799261ba58ed87df16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334687927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad514d64d01ab9d90e2372d72c0333db5811538ff591c550edb52aca76b126f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:37:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Dec 2025 19:37:21 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 11 Dec 2025 19:37:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:37:36 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2411b2c155f5436391c30abc6408ddb180b3ce9891fce85b5a2ddefbe5f635`  
		Last Modified: Thu, 11 Dec 2025 19:38:32 GMT  
		Size: 55.6 MB (55558382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a9bae9c10c3a768023afc3e6757de669b6471554da3a61ad6798468a374579`  
		Last Modified: Thu, 11 Dec 2025 19:38:32 GMT  
		Size: 275.0 MB (275040168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:cda243187e2b29f66844d5744a4dc4111f47770122f9f99fa250605390e52ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01aabc0c23745134e7c10aa077b07e46405a2e3b2777d3c02cf9859fee5e901a`

```dockerfile
```

-	Layers:
	-	`sha256:71f260e3e9683188e39312b8720827017240979d4fd287fa0d36e606dcac2d2f`  
		Last Modified: Thu, 11 Dec 2025 21:44:58 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b7d6cce9506de542cdabcfb6b60b9308a48456c1cc85b822176428b83c22d2`  
		Last Modified: Thu, 11 Dec 2025 21:44:59 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:1f9bbc4f8923f8b0481a08d7d67d698bb7c3f5d3e6bc66822193fbfcba4c6b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354149732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a6936a98fdeb1e2732a32c46ebe7cc4b8f9ef660d9d3d68d27d805a28e9231`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:35:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 11 Dec 2025 19:35:27 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 11 Dec 2025 19:35:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.92.0
# Thu, 11 Dec 2025 19:36:09 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e62b140ef53522bdf86813794afc358675f5906710b21c1b648488cc7385e`  
		Last Modified: Thu, 11 Dec 2025 19:37:50 GMT  
		Size: 56.6 MB (56619645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a515ef2dae02dce3ed6331b0824c02f317b21d5139fc162b19ad5b4925ee41`  
		Last Modified: Thu, 11 Dec 2025 19:39:08 GMT  
		Size: 294.0 MB (293954524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:e76c1524bc7ac47e4456beb1b241ef451b464c426b0ecfb672319b3a88c79cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4592e9a4edb1a94f13dde6286b6971c174f3c9d956bd2b76d26bb69a34df5c`

```dockerfile
```

-	Layers:
	-	`sha256:00d8be77e17ebe751aeff95897428911f06a858b2bf44a2c01f2835ca2d8df7c`  
		Last Modified: Thu, 11 Dec 2025 21:45:03 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8d25a4120f9f5bbbaddaa27848c8178c8e79c9999861765f8b61d41b4644c7`  
		Last Modified: Thu, 11 Dec 2025 19:37:32 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
