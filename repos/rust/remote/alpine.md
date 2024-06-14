## `rust:alpine`

```console
$ docker pull rust@sha256:df74621c42c7f33352093ad5191930f38cab56cd64c964ef3c36549863bdc316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:93b16b091ec3814d2eb9e262f580743be5d5457f59add401936ad23a5d433e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278133112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8fe2f4da371bf6ab0042aa345db1323ee69902def6cd3077e57414b11386b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67145fb6ab3cb1f73f53ef3d8c224db35c2ee42a5afb0a40df39fdf8ae81c5`  
		Last Modified: Thu, 13 Jun 2024 18:31:29 GMT  
		Size: 55.3 MB (55313798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8d5f52a1dd5d942e3d2537e7a50e981115ca490bea408a05fc9c0547ed815d`  
		Last Modified: Thu, 13 Jun 2024 18:31:32 GMT  
		Size: 219.2 MB (219197220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3a8ce6613dd82f5be6e04ea1ba5bfd0caea563e352955b958752017082e9a295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.9 KB (717938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d4367b470b5f7f5b7d0756a051aa7f54835d5d0b590e1bff55f90fd4b6bb7a`

```dockerfile
```

-	Layers:
	-	`sha256:a40097683d9402e1c942dfc928d9aabb766df2836d3d803c24074b01627dfd83`  
		Last Modified: Thu, 13 Jun 2024 18:31:28 GMT  
		Size: 706.3 KB (706259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc22457e95c0a601ab1007da65d0cd8ebbc4e75d831e70a5727b926c8f89adb9`  
		Last Modified: Thu, 13 Jun 2024 18:31:28 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e20123bdd1453a9074402fb774c82174eccb53edd1b3f1471739b734160625b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284122732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afceff90bc8530e228a040bfaefd23df6a5390761689bac71d7b085326d03b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9723d494dcfa621843d26ad962ff8b243f426a291ceb3483dafaed876c12b06`  
		Last Modified: Fri, 14 Jun 2024 04:28:13 GMT  
		Size: 52.9 MB (52947017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f53e394c9d1d9eb25b5bc70f454a96c55c9d0957c94b65edb18f8d56f97ef7`  
		Last Modified: Fri, 14 Jun 2024 04:28:17 GMT  
		Size: 227.1 MB (227088939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d28d3c92b3d52bf6995a4c7a59c3d71f3fb44f993f48c2e0177fb4a80fa38c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.3 KB (754321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45206cb07675b4f80304917c3eaa09503e538476b6745edb901bc55e19738163`

```dockerfile
```

-	Layers:
	-	`sha256:1477ab405ec6c99815d1d89b74a677ee4e290f0e0f0d792bf5620bd6e6215aa6`  
		Last Modified: Fri, 14 Jun 2024 04:28:12 GMT  
		Size: 742.3 KB (742295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8919d75f01c63c9215dc44c3fb922f3ab07909a241adfac6b91f0b689af9ca41`  
		Last Modified: Fri, 14 Jun 2024 04:28:11 GMT  
		Size: 12.0 KB (12026 bytes)  
		MIME: application/vnd.in-toto+json
