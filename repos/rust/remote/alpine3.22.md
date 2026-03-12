## `rust:alpine3.22`

```console
$ docker pull rust@sha256:211edb10470c7b07116d23438d8e38448fbc09179da8c780c5d72b0b44909686
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
$ docker pull rust@sha256:df47a6adf941782a68df09a38e43fc3b5d80206f6d83036c32b2b76caea39e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336092224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838dcb4eeb7d8fa341ec2dfe9e49aca8776029dd4c0ac5acfd69c35e13758f27`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 19:09:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Mar 2026 19:09:09 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Mar 2026 19:09:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:09:26 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcc704f3300f35a2fa649d6cc70943e357d33d868a3dfd53bf42f038f301ea9`  
		Last Modified: Thu, 12 Mar 2026 19:10:02 GMT  
		Size: 65.1 MB (65084114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b444c18a627c9ade20b4de86dc4d25d83349981bec1405236ac0c2689c44234`  
		Last Modified: Thu, 12 Mar 2026 19:10:06 GMT  
		Size: 267.2 MB (267203235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:93f25ed8ca4e530198b19afc4f3227a585c5ce1db109fea6dcbe8e792769f4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.5 KB (974497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4744aeef55cf5a8b02fe6bdc9a0a73ee44e9404a66728f32cea3327c165e577`

```dockerfile
```

-	Layers:
	-	`sha256:1a4f30ad8160ec4353d0cffd037bf2c403eb5049e18a20acbcfe2aeeca3e1e9e`  
		Last Modified: Thu, 12 Mar 2026 19:09:59 GMT  
		Size: 962.3 KB (962311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dc7da19caba262894ccb94d73c7273acf57d92dd9c84d1c79b53df53ea092fd`  
		Last Modified: Thu, 12 Mar 2026 19:09:59 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:93a3a2099e3b9f1da5b6111725ea047dff708ff422a71b4ab7cff2f6427de0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339071664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c05263b91681021e52189a8c8758efb5f1262ae7d9a3bbb9c8528480b03690`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 19:08:25 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 12 Mar 2026 19:08:25 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 12 Mar 2026 19:08:25 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:08:39 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceca0385029630fcad40185f1590b734df0ff1eca02538837f1221a8f5e8762`  
		Last Modified: Thu, 12 Mar 2026 19:09:16 GMT  
		Size: 61.8 MB (61758625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eab4bf57b8a2affc35cadd76ea077490fc1d0dcd72d3ec7dec68653f23a5ec`  
		Last Modified: Thu, 12 Mar 2026 19:09:20 GMT  
		Size: 273.2 MB (273173520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:215f8795d4a7bbefcd9bd75f62b8092c18751e758a464fff390461b5dbf13c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1053942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed6071799718aed953d9921927b3f256b2debc6b80033a70d19c535d1be999f`

```dockerfile
```

-	Layers:
	-	`sha256:ac67934cde55ba6221b2a9d98132dd91ed4f4b584f5cf29b6a214189b45d928b`  
		Last Modified: Thu, 12 Mar 2026 19:09:14 GMT  
		Size: 1.0 MB (1041637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7782ffd3b0ce7f64c79865e907138384f65ad447b1ee590cc3950b3d496bdb2`  
		Last Modified: Thu, 12 Mar 2026 19:09:14 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:b74e221eedc1afe15cdee89972e50c7dbd8ebdbba31c3d6ebe588a67c2145660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357614099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ab01b3ee0b6d866fe5615d58b23f8e59cffdf7a295a7f997375362c8eeacce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 19:58:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Mar 2026 19:58:46 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 05 Mar 2026 19:58:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Thu, 12 Mar 2026 19:12:51 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19b58d4c49a4c9435a41a6bea841bae678e0a4dc4b978bcdc48b95ebc72737`  
		Last Modified: Thu, 05 Mar 2026 20:00:25 GMT  
		Size: 61.6 MB (61572689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482f0e6efdb4ff8b3207ff6964ac88144473745f3cef2919e65f0d26f984932`  
		Last Modified: Thu, 12 Mar 2026 19:14:05 GMT  
		Size: 292.3 MB (292307113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:d08b589c016275149669be9607febdff4ef8b0db6f30cb05181cada8c826989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.1 KB (987086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25571c919d737a59d552e7ea49deb7e2bffbf707d2b040f35eb27bc004f040e`

```dockerfile
```

-	Layers:
	-	`sha256:51f766e1d30f3b166a1d6280443f291769cb81698f11e26c218430d2378329f6`  
		Last Modified: Thu, 12 Mar 2026 19:13:58 GMT  
		Size: 974.9 KB (974855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177b31c9f2fc24a49fc5936e9c2664023d6956338f8d3f8ac62166033066bebc`  
		Last Modified: Thu, 12 Mar 2026 19:13:58 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.in-toto+json
