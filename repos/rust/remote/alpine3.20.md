## `rust:alpine3.20`

```console
$ docker pull rust@sha256:776eaf8bfde5edc823572cf49668ed6534592fbbbdd0f6f334bc5ade55758bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:d49e6de6c44d772d7b755d65c9ffb9734e7c993797e42df6196617ff0239fe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329612750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426308d8230cabf5916caddcc33eda48910fec2e1e655c83e27acf91f1ba65c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 19:08:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Mar 2026 19:08:32 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Mar 2026 19:08:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:08:49 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbe123026ad8e30639b66ca7928650b4d79c9336613574196ff32cf85f65de8`  
		Last Modified: Thu, 12 Mar 2026 19:09:24 GMT  
		Size: 58.8 MB (58781698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5349c2f3d37d93ea438a76147b54b0345a8c5a1d643c5c1263958657005e0f`  
		Last Modified: Thu, 12 Mar 2026 19:09:28 GMT  
		Size: 267.2 MB (267203188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:aa260bcb2ee9a4f2aa67dcd49a821be8df0b99193874cd4048d57bc09b7f847f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d33ccaec1947daee5c7ea43d0f3252cf514d1159f5d492c3f4e300b23ef15a`

```dockerfile
```

-	Layers:
	-	`sha256:b4a218b6841ad3c8c88579c047f3e49a3645ef314aa7f2e624282303eba2b3a3`  
		Last Modified: Thu, 12 Mar 2026 19:09:22 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4457e7057c808fb573b16a965f0a7c5e1ccb16394e982938206cd02e0e293c68`  
		Last Modified: Thu, 12 Mar 2026 19:09:22 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7f815805df035477d242b0ff221d8bd1d39218f7aafd6b8a5117d3ddd93a891d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332821887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24425822be393e4fa99afdb89720702b6febc325dfa650e16666811a3f08c2c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 19:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Mar 2026 19:08:38 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Mar 2026 19:08:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:08:52 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c67eb1d047b062b021d1f5642b23f640be895e1da466bb48c02adb490e8fc2d`  
		Last Modified: Thu, 12 Mar 2026 19:09:29 GMT  
		Size: 55.6 MB (55558411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30057af9c8df4d9c120127d00381c8bdaaccba3e3bb285d4c8548d64932e1444`  
		Last Modified: Thu, 12 Mar 2026 19:09:33 GMT  
		Size: 273.2 MB (273173518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:392a3f2a5e8237400c2d4204f63c8af54c643cf473d77e815be6a4918dcb9e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6970dc43bef12b6fc5ed94c16430ee96a69461a039b4e439fdf9f7ee87ec15`

```dockerfile
```

-	Layers:
	-	`sha256:c27cd393d29c9fe381bde877eac30a5c940eebe6593ad8738e1d55915ef21237`  
		Last Modified: Thu, 12 Mar 2026 19:09:26 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc33a274ac5df8786c4c47a7963d25133ae42a23612b2292b23bc9d6e88050d0`  
		Last Modified: Thu, 12 Mar 2026 19:09:26 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:3eea4a38fc41e76dab40df6154d9f81d7c2505178411e3c58793dd1400536a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352504326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0743fae3a236b1186929b3e4f4d3f23548fb55d561f59b074e6397d0a67b5e41`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:56:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:56:26 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:56:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:11:02 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33f18efd80ab9e3f3226192e424a82888219c8b6ae0d2a2e71437b45ef8dd6`  
		Last Modified: Thu, 05 Mar 2026 19:58:22 GMT  
		Size: 56.6 MB (56619708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcd9fc5aa14f5d7612f9eac9de8e88a057044203a47122a3e93b30ae14977c5`  
		Last Modified: Thu, 12 Mar 2026 19:12:16 GMT  
		Size: 292.3 MB (292307108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:f5843c86004675991cd791261446fff69f829b2d3457457bc6f738cfa4546039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661a99623ad22815c7b78d3cb13044a62343c0d37ddc3239794ed8acf74bb133`

```dockerfile
```

-	Layers:
	-	`sha256:9fb026523918ee5cb47b41a35318a625441c45ec16561b2fdb1e2694786b0bf3`  
		Last Modified: Thu, 12 Mar 2026 19:12:10 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2fd5efa2fc4367e6063da2f06dde02df1d1804ed228960cda64e16e0a18e0c`  
		Last Modified: Thu, 12 Mar 2026 19:12:10 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
