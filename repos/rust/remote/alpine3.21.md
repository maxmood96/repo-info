## `rust:alpine3.21`

```console
$ docker pull rust@sha256:d1c67dbc9f2cbad810ca8f1f74ab10664fd7baab051d7761e9bafca1261b5040
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:4bebaa3d13e2933c751eaf4a2e38d0530807572ea101d9c61f20f51eb7174ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296402288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0b90672607f014ece71b1095a4a076f3e6484c5e0638a8cd62a28564c64184`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 22:20:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 22:20:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Dec 2024 22:20:09 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 05 Dec 2024 22:20:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9b93f4025eb5d535dbdccab0ff9847d54232808aac65b016eda89cade7e2f7`  
		Last Modified: Wed, 08 Jan 2025 18:15:05 GMT  
		Size: 61.6 MB (61564905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d54a824d2b794987a5be227b83904aeaa4e3710e251d08a4541f3b9caf23f`  
		Last Modified: Wed, 08 Jan 2025 18:15:08 GMT  
		Size: 231.2 MB (231195668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:cd237348a06461a6a1ac46d6670723e81c1f522161de5a24683fd9e8ca9a2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c1a6f8e0d057fd75368b7f4d79161eb49960fa5069ac845772b1ee62362d31`

```dockerfile
```

-	Layers:
	-	`sha256:088ae8da940cd1a07f414972e438b17daf80d67a4883e4e628d3007df4fed587`  
		Last Modified: Wed, 08 Jan 2025 18:15:03 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5eec4997052f9cfc866117028433c2ab9cd645656b53684368738e67582c3f7`  
		Last Modified: Wed, 08 Jan 2025 18:15:03 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2f450e8765966b93081dccbb84ecf585d87278f46adfdad80436e7f55e5f66c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300654223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb2c5f658171427274508b69ca851cd0d00e2a9afce98229a9ef4d613de6df3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 22:20:09 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 22:20:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Dec 2024 22:20:09 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 05 Dec 2024 22:20:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4f214695e951cda891986d6902db28e31207b6f07d5406302ef3199b91207a`  
		Last Modified: Tue, 07 Jan 2025 15:28:50 GMT  
		Size: 59.1 MB (59082547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d3ad6619b8063bf7f7d89ef3557d87f5c7c081409992007c5be3b69301fe9f`  
		Last Modified: Tue, 07 Jan 2025 15:28:55 GMT  
		Size: 237.6 MB (237588669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:1495b2ec932b8186707a008148dfb4a6530b30e1e319b31da98cb2ddb016bdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0501d9d203e92789042e14cfe2415b538babcf09bdef46f40b94f5c4d7f68f3f`

```dockerfile
```

-	Layers:
	-	`sha256:fe5d46942d78d2b9745b4c4c35ca5e85d2212c78ec7115e6498eacb6cd9f4a93`  
		Last Modified: Tue, 07 Jan 2025 15:28:48 GMT  
		Size: 855.0 KB (855047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abee95e87bd83f2b8ad98c862e61deb695db709db36c1267fdaf4241299c7ba4`  
		Last Modified: Tue, 07 Jan 2025 15:28:48 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
