## `rust:alpine3.21`

```console
$ docker pull rust@sha256:6706207940151d3a18ab3c8d1b639e45d66fac26e76d05b3cb40310619dbf0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:8ebce1297b1911947a95ee34b08aa29433c8939f64f7f8f1044a109a1db9825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304602889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d45d67fc8b6ae558345c2bf4f8aaae836aa824a64b884f15e50e5223cb7c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Jan 2025 15:52:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 09 Jan 2025 15:52:19 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 09 Jan 2025 15:52:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.0
# Thu, 09 Jan 2025 15:52:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a4f4cf3bca91ccf71f670f52402ac1f82181cce738d99416dcefa0b076dfc`  
		Last Modified: Thu, 09 Jan 2025 22:29:50 GMT  
		Size: 61.6 MB (61564880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafc66453de6f9bf524f7022580edfc36a04771dd9a6002597ef241553816e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:53 GMT  
		Size: 239.4 MB (239396294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:b4eddd49287b5b30b46cc3f23978b15a1046008487f989c155c71a2efc594ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a4473f4064c6251f1cae031db53e17475091f543d7db61b5b9712eeb7614aa`

```dockerfile
```

-	Layers:
	-	`sha256:12fd4cc01dd03545ee8ed48dc884e3188f19bb3468e0e6e3a0e674ec055a161a`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58baa09720560053236ac71a3ef7df8d178bb946638c2621be08a22a73b4b4`  
		Last Modified: Thu, 09 Jan 2025 22:29:48 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:98972d919614aba25efd5e0a7cfc8d7c11b11b9959f0ca5df7fc292c490ad0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300682117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbae6a85a9de9503d62e73bf2438d4ff018461ed4d1b242bf305aba272533b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 22:20:09 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f7aeefeb91468e7b008d707b6cce663e04ec66f9af3eb2d728992c8be930ac`  
		Last Modified: Thu, 09 Jan 2025 05:57:20 GMT  
		Size: 59.1 MB (59101141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42ed64d061287384316cff4f9afa9b474fcaff3573dde065f5a94678620ee4`  
		Last Modified: Thu, 09 Jan 2025 05:57:24 GMT  
		Size: 237.6 MB (237588617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:092bcccd446f84cf000d464af94ff686a068666975e45d14ce5aad724ca29f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b38f2e12612a20b9d412496a19e2b6dd4cea03eb99e3f8249b5f86f8c2b94c`

```dockerfile
```

-	Layers:
	-	`sha256:4d72b9955abaaff69ed44cecf5aa380d14ad5cc152f15126d6af8287c1151009`  
		Last Modified: Thu, 09 Jan 2025 05:57:18 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e1be3328161242fe6d6308b461636cf10ea662e8361e472c14337138beff96`  
		Last Modified: Thu, 09 Jan 2025 05:57:18 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json
