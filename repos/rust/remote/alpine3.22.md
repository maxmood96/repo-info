## `rust:alpine3.22`

```console
$ docker pull rust@sha256:4b800f2e72e04be908e5f634c504c741bd943b763d1d8ad7b096cc340e1b5b46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:f9617326395be71547efa3c8b8d58b89ff958afc594596713bceb585aabc067e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326674102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db8072fa10b38ffff96132697449d8aece6dfc91f8a689491279bc56970d39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7660a6bab9aa847e6a2af94673d75f67d2d9a7148d3f3142d7e23034688c65`  
		Last Modified: Fri, 08 Aug 2025 16:56:32 GMT  
		Size: 61.6 MB (61607080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc1dd2a17b09b5edae96526662eca709441d2b0be4073a3d7d8423a37f3c9bf`  
		Last Modified: Fri, 08 Aug 2025 17:48:42 GMT  
		Size: 261.3 MB (261267333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:f7702cc8215bd80d9b2afd8fd7e9d6bd0b8b68a1f198165ea8f96ac4f01f72e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **792.4 KB (792356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd590f3f39f1ba807cd2820decae4b92785010ddb4f6fa65197dfff66570c750`

```dockerfile
```

-	Layers:
	-	`sha256:fe75a08c6beaa30b32296534b555e477673b71f917f78e5a33f0c3eeb81e11c3`  
		Last Modified: Fri, 08 Aug 2025 17:50:14 GMT  
		Size: 780.1 KB (780060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9941a7e8c9d96f152405617dfe96500386099aa6c90b4c846f5d847ad378acb`  
		Last Modified: Fri, 08 Aug 2025 17:50:14 GMT  
		Size: 12.3 KB (12296 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:375c19a34ded78a3541ea2fe20f46cd494ee20f737d259bde4aed8ae340fdc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327146269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc37e5c91f9dcd5c4bcbf0b90b6c728af6ffc58188878fb227c3e5dd4e9d8cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbcc8f8ac7e9fc0443f9f2b925f971b4eef84c8db212fd1518f7f477cf20946`  
		Last Modified: Fri, 08 Aug 2025 17:06:19 GMT  
		Size: 59.1 MB (59141426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4585764f0557f5959d3af4f4a823388c74aa6d376c208a5be8ba39f3a55bfd66`  
		Last Modified: Fri, 08 Aug 2025 17:50:17 GMT  
		Size: 263.9 MB (263874093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:11b9f2b3d7fce7237c8a4c01faf405fe2d245abe16291440b8dc3987ff76b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.1 KB (872110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849391688512655a0bb7a6c61ad2d94e25b582c75b4205e68303f36dc4e03253`

```dockerfile
```

-	Layers:
	-	`sha256:613de896c1f89c7f627297288d27780c53fedbe2d111e3cb76caaf433cafe743`  
		Last Modified: Fri, 08 Aug 2025 17:50:18 GMT  
		Size: 859.6 KB (859646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b47796ce2997cd284227f7b03226b1800692854cefbc34dad4a7bf934a208d`  
		Last Modified: Fri, 08 Aug 2025 17:50:19 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:b5c3e8a178672499521c3ee5750d18765d46f89bc9183e844e8877d98a8cf404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345214932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03c431be7d965add7e1126f2624dfd7f36ffa1f869de3ed0f30becf4d8d879b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 07 Aug 2025 14:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 07 Aug 2025 14:12:07 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 07 Aug 2025 14:12:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.89.0
# Thu, 07 Aug 2025 14:12:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a28b81e3e09705dabf7c395d8214e4711db832e8881ed32918c0cf752cacd4`  
		Last Modified: Fri, 08 Aug 2025 17:14:39 GMT  
		Size: 59.0 MB (59004657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda1c58ada41229b5a342e15510f431b7d672732b324f4bed8bdaaa8b0598f2c`  
		Last Modified: Fri, 08 Aug 2025 21:00:28 GMT  
		Size: 282.5 MB (282483164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:b0e5c75db5a9cf5fb2b993654f579757f89957827b300e2937421479819b1078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.0 KB (804995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86632ab74283ecad572da1100d03c59647017bd6b6b21458a4bed663a5ff538`

```dockerfile
```

-	Layers:
	-	`sha256:49df7ab16156417a8363f94c38582c83c0e12cb134256c6fe441fbf0edbb5bc7`  
		Last Modified: Fri, 08 Aug 2025 20:44:25 GMT  
		Size: 792.6 KB (792628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19bef7d630429e623570fca4ba86d5eb6c68c906ee50bc44618b7da650399cf0`  
		Last Modified: Fri, 08 Aug 2025 20:44:26 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json
