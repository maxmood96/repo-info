## `rust:alpine3.20`

```console
$ docker pull rust@sha256:fbf6b3f1b3b497b5e1f61919af0f63bc31216232704f0f954952b91272cbafc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:9bf1ad7a18aa44ff85ed5a885c3b27c27008bb8247d4d3095d19b1d27997c195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298099598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a43ceeba7a70b0b691a78b50230c29396c4533e7587114db5b93bc8d39e39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275c3cffbf0d435f6af6345d11230eb8dad38943f32432c5b8cb5952a29b622`  
		Last Modified: Tue, 18 Mar 2025 21:25:10 GMT  
		Size: 55.3 MB (55315660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6526bb500db123460bf7dfd4c2d0c27d7887076cea4866449f6afdf1a24d03c`  
		Last Modified: Tue, 18 Mar 2025 21:25:13 GMT  
		Size: 239.2 MB (239157041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:9f8ce01b968720871f5a3b6b4084ed641cb6f1dc3f859dbf07ab33ffe7e99a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925967397ff46d570772cb260a9e85c4e860d1a7ac092239808f66464419ad60`

```dockerfile
```

-	Layers:
	-	`sha256:740f26fb4052f94da689e1dde8ada62d4a144bc82527b8691fa3ed26dadc27ba`  
		Last Modified: Tue, 18 Mar 2025 21:25:09 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5417d8139f31a32a78f95acdb7439bcc61de75acd329352e4f35c1c9a6be6a6`  
		Last Modified: Tue, 18 Mar 2025 21:25:09 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f2a117b2a64f376bd42636bd8702cd8e3e9d0e42bcf0de8676bb98b08e3bcdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301385668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f08f54342a2606e6163f2e3dbc95cc7b82de13ad76717bb59045d5e7425970b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:dae341a5a5f18f2a2eadd5230f0aa7b532a6135767080a759e3e478787149a0f`  
		Last Modified: Wed, 05 Mar 2025 20:23:05 GMT  
		Size: 244.3 MB (244344015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:29cbcf815de9b2e1178cd879f1ba3ff46c18df56b81d124fe5b5704dbf1893d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad28d19852867e367c997a445e116bfdc25c1c0d54a412edd0ab1d48865e6ae3`

```dockerfile
```

-	Layers:
	-	`sha256:fbe9a1a5af96333d7d6c126a126eaa681c2d6033b92b2885654038303591c8e5`  
		Last Modified: Wed, 05 Mar 2025 20:22:59 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8066031b20d3ec4ffa4a65fc7dc69a22ffcbe6aa98128af5165fdbf3d3077d9a`  
		Last Modified: Wed, 05 Mar 2025 20:22:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
