## `rust:1-alpine`

```console
$ docker pull rust@sha256:f87aa870663e2b57ec8c69de82c7eedf7383bee987eef7612c0359635eaadb41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:42cc159f02dd5f56e62f5131c54fb3c321050ba5660b04e54d348f3e21ac1dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349406087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd115f1f400d12bdadcf69b38d10f2090111340181e43e782dbd01ac0cf59cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:22:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 16 Jun 2026 00:22:45 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 16 Jun 2026 00:22:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Tue, 16 Jun 2026 00:23:03 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068934010d36c2ce3dd73017597a992975cd28634afebac503803c819d1a9c69`  
		Last Modified: Tue, 16 Jun 2026 00:23:42 GMT  
		Size: 75.1 MB (75079127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31b1578fda69008374c3b88071a85be7d945a915b17867e9fa7c8ba3c45b47`  
		Last Modified: Tue, 16 Jun 2026 00:23:45 GMT  
		Size: 270.5 MB (270480569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:0066402d0e95c8bd68e0e88a7f7fa67a7265dd25c847f109b00930ba480d9d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4920b3803864b52ac63cd4f2ee8579b0d1ae8bdd1275a7701861d2ffe0b27e`

```dockerfile
```

-	Layers:
	-	`sha256:559d573bd38e4d3d48e83c69e0778ab7d2a91748f7e621f257a14767f7e9214e`  
		Last Modified: Tue, 16 Jun 2026 00:23:38 GMT  
		Size: 990.5 KB (990501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52dad70389abb8a0eab4f8dc96574adf32b6a239d60e4edadc9ec4ba5cb25583`  
		Last Modified: Tue, 16 Jun 2026 00:23:38 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:970845a4bf4084d42a9919da8f2fb79c867eca79a92e5c944fe22d76b0630e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345114693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fc9ee159f2ec4825dd9482f14ffef99af715d4ad9eaf3ab47524267a3619e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:24:15 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 16 Jun 2026 00:24:15 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 16 Jun 2026 00:24:15 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Tue, 16 Jun 2026 00:24:29 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49a5675d77a85d9b50aa16c96baff0c2613d5766fb78b290c6ff7244ee02310`  
		Last Modified: Tue, 16 Jun 2026 00:25:06 GMT  
		Size: 66.5 MB (66507128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0770aadcb1d4fe074d33b27c27999ce9473485bd048c12d84071d60edf56220f`  
		Last Modified: Tue, 16 Jun 2026 00:25:11 GMT  
		Size: 274.4 MB (274424528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:a01097fcfc5286408dbb4b851e213070fab9f6ada4adc9a125d98659514d49ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93a87290b7cf03b9d5087d1f711f33863dd33722dd8993cac15fd62fcaa8ea2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f1aae7ff8f005dd827556600611368a2e478436bd8f9cde8940932d40a84d5`  
		Last Modified: Tue, 16 Jun 2026 00:25:04 GMT  
		Size: 1.0 MB (1049454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e7fd72556be2ba21ce2f56efe28aeb2ed8e7abd990fdd04e601d606fdd0c2a`  
		Last Modified: Tue, 16 Jun 2026 00:25:03 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:974085d15d7a3ff230ad736f2eb648de7d309c2e7acbcf95dd23684b217030a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363657478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ddff6b6212e51e6e0ffb0d829e0216ee0b650994a2d5397745a795b53c3a97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:14:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 16 Jun 2026 01:14:13 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Tue, 16 Jun 2026 01:14:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Tue, 16 Jun 2026 01:14:32 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68c11fe0113a6fe85e9624b7058cb9d673f3dd80ece03287e67794373be36f2`  
		Last Modified: Tue, 16 Jun 2026 01:15:41 GMT  
		Size: 66.4 MB (66394520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e13e9546936f4a716461f328ca8b1f9fa40fe4a4142690128db7615191b9bea`  
		Last Modified: Tue, 16 Jun 2026 01:15:46 GMT  
		Size: 293.4 MB (293449558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:fc51f5e9780c2ebd77dcb5a9dfe37aa78f06e8cc3c2a0fd72e19d8f63602f237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.2 KB (996201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b86da2ccc99d225f47f034055924de2b016b6dbbc8648c25e509393c5bec5c`

```dockerfile
```

-	Layers:
	-	`sha256:e39e3b0cbd7b817bff619e5299ed845907f2fedb12866baaadc0b9c9faeccc45`  
		Last Modified: Tue, 16 Jun 2026 01:15:39 GMT  
		Size: 982.7 KB (982741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5d6be2dba0d425d07e71e83a6a74e974917cc8969207f428a177c28ee61711`  
		Last Modified: Tue, 16 Jun 2026 01:15:38 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
