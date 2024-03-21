## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:cf4a5a2ddc9102657b862e73ac5a611acc670cd36ee21f7d79172e5c4dd0f1a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:b2683667dc8001b7abbae5ef302ecb2e433a8c9da8090841192e8a12f297e90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268689261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feac781ca19ebd4977cf3429c51a2f846ee2c9bc5870a46ed5bb9d8355493f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 14:04:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e90e0f01f49b067e5fb5fc03c85c1882fde60836ecf154acbb15988b2614f0`  
		Last Modified: Thu, 21 Mar 2024 18:49:49 GMT  
		Size: 51.5 MB (51534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7649e1f404ad1325b9f8506eb1c05e0f42ca9831769819f1a4b336212397a3`  
		Last Modified: Thu, 21 Mar 2024 18:49:51 GMT  
		Size: 213.8 MB (213752708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:7ec3935664d5fe7e8edb03f82badbf3af323792ccd882a82991e2b0881f2897d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.4 KB (712370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d585d0ae7f4d783b744b8acea15e02960d397c3e428d073fcdee8495f1169487`

```dockerfile
```

-	Layers:
	-	`sha256:12ffec392ba978af0b05360a5b9a97aa273915edce3d1434de40c6a03274d9fb`  
		Last Modified: Thu, 21 Mar 2024 18:49:47 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a360e58d6efb0fbbc8e638ecc676c4a64fa788352e4e11e23f7de4c4fc287307`  
		Last Modified: Thu, 21 Mar 2024 18:49:47 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ac669fe0a96eb75078d46a2e70c99c19c04ef6c805e4f7581de2b5d283a3ae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271916069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4137708dae1ce12b866d9b4b0c9ea4e5b07ee9ed07ab20ef6e4166bbe6923f5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 14:04:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3024da5cabb8d9350a8f1f0716c452e917e5c5e89d708c5c133f9bd1ffcefd7a`  
		Last Modified: Thu, 21 Mar 2024 19:01:25 GMT  
		Size: 222.5 MB (222516349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:7478a5d76866e86e0b3483ae16cf0d0f274ad203ca7039f6013a4b670943edab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.1 KB (747063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac3632b0957d472c826a04dc7fdb0c6d6c5cc15ea7b69a6f48f7d1492882b84`

```dockerfile
```

-	Layers:
	-	`sha256:296329fdf26375a39fd021d2ccec76803881056deb2e97b54d6f01617d6db666`  
		Last Modified: Thu, 21 Mar 2024 19:01:20 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642aca0dddaee0a173a7113d8c325d74ed86409b8bc8f5f202b3457afa470ef3`  
		Last Modified: Thu, 21 Mar 2024 19:01:20 GMT  
		Size: 10.3 KB (10328 bytes)  
		MIME: application/vnd.in-toto+json
