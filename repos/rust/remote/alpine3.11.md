## `rust:alpine3.11`

```console
$ docker pull rust@sha256:780ea29c540931995ce5c9a59f97eb6447ed1a0c1cb94904f25b75bbe7c1d0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.11` - linux; amd64

```console
$ docker pull rust@sha256:6589eea0919dca605297441d3d92c27f3bbdd4949700bcc7c11a86f5402d3096
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210490359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f259530316d087eb66ce1af09080e9003c1b04c1b8eb193a81fe1ee407c9952`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 15:04:47 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 31 Dec 2020 20:28:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Thu, 31 Dec 2020 20:29:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='05c5c05ec76671d73645aac3afbccf2187352fce7e46fc85be859f52a42797f6' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a8a480d8d9e7f8c6979d7f8b12bc59da13db67970f7b13161ff409f0a771213' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca0b100b8171be66aabb5066642a3c3aad4b20c054e978df59cdcca17cee34`  
		Last Modified: Thu, 17 Dec 2020 15:06:53 GMT  
		Size: 36.5 MB (36465795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e740614dd6af37bc18312f949af79f4a482188c7c3a280a6e3d7108c077b5dac`  
		Last Modified: Thu, 31 Dec 2020 20:32:07 GMT  
		Size: 171.2 MB (171209700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.11` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:67ebe883096eb1798ca1c018397cef406d826e08e95bf01a24605d37bfe95e0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193008245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853f9312992b924d5ef05e43dec0dc5f024da94f11df4fe086ff00e8ab8da86a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 31 Dec 2020 19:46:21 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 31 Dec 2020 19:46:22 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Thu, 31 Dec 2020 19:46:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='05c5c05ec76671d73645aac3afbccf2187352fce7e46fc85be859f52a42797f6' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a8a480d8d9e7f8c6979d7f8b12bc59da13db67970f7b13161ff409f0a771213' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a758853755134c357fefc7956f55987e0b3dc58c5962dec33b5e5f8fddc68dc1`  
		Last Modified: Thu, 31 Dec 2020 19:49:43 GMT  
		Size: 29.2 MB (29178177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d154d847f7d898e842d93bb0b6e8dea0d115ce3465f7985fb8ecfa7a947bc06`  
		Last Modified: Thu, 31 Dec 2020 19:50:15 GMT  
		Size: 161.1 MB (161104852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
