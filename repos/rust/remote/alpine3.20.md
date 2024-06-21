## `rust:alpine3.20`

```console
$ docker pull rust@sha256:6e1a6ecaad93ff738b279717c9bae0818d6f0d1b990be239731c17adcacfb433
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:1fd5647240e16a7ca968780a3b9d011c1f868f472e8f1739c0257639f0441ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278134834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b044b3a815a76afb9686c59fda26d1e03d1ffc5ad557a1b6e833c976af5459b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 13 Jun 2024 14:36:52 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb1a0bcffc46374772a9151131b8314b527b4042779a73551e2ce445aae4b82`  
		Last Modified: Thu, 20 Jun 2024 20:57:12 GMT  
		Size: 55.3 MB (55313779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4513f55edff3bda26dd09c867dc66fc0e9dfd6a62ffddc7d1aa3dbd4bad2ac8`  
		Last Modified: Thu, 20 Jun 2024 20:57:14 GMT  
		Size: 219.2 MB (219197211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c78a4aba3cb5ebddb51a402e1c506ceb4ceec0d18cf1548baef2d6cf5eeae348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.9 KB (717939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fc90a3879243665898f7b09110b083b505820641c1b262f9452298467fa125`

```dockerfile
```

-	Layers:
	-	`sha256:d438704cb2ee31b45d94d103cf3e063bfdd65f67e567e7c31540ac3a45129757`  
		Last Modified: Thu, 20 Jun 2024 20:57:11 GMT  
		Size: 706.3 KB (706260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f60bca25ef414d01dd82c995a83ab40154a58ddc1fd794f3a737b42c02df4`  
		Last Modified: Thu, 20 Jun 2024 20:57:11 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

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

### `rust:alpine3.20` - unknown; unknown

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
