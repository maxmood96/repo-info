## `rust:1-alpine`

```console
$ docker pull rust@sha256:6847f25f5479981b7c79d3029b248012d818dd72d549a8419de9a4104de30a66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json
