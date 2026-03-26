## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:f800c06daae24db26d34e43cc3a5c72e5aa863b0ef7f95569a0d13b1ad8891af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f0476f1db83ea1bb46ed18b6ee443d208653c25600b45f87dd7ddfebbcdbf059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335896787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8127d598c996590279061f17b129969970865e95f38a4a86fb053dd2216004`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:54:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:54:01 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:54:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:54:19 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407844f61af8fa8a9f80e0c898df794cac8a611a2aa9ed0b19a089556772836a`  
		Last Modified: Thu, 26 Mar 2026 20:54:57 GMT  
		Size: 65.0 MB (65032040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c42812ee92122f6e114d3a45cb305a91bcb0cbc5161d8d444c3f94748bb756b`  
		Last Modified: Thu, 26 Mar 2026 20:55:01 GMT  
		Size: 267.2 MB (267221005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:9ac07b63ea12b6486281b48cb6d4a1d6bcc60329784ef17d949f361ca15541ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.7 KB (973716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68be6526c7b7c9c8114ffc6bb72a7ba5ba4725936a39a132e581787bc0683ec`

```dockerfile
```

-	Layers:
	-	`sha256:130ff11093afb1b4ddb2abdb46649753bdecd1c7c3136c3fc66d0ec468f98209`  
		Last Modified: Thu, 26 Mar 2026 20:54:55 GMT  
		Size: 961.5 KB (961530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52557c0e412b82ce5da5e577301495bd5cdd98426c2fa1d7ee0fceb4bb504ef`  
		Last Modified: Thu, 26 Mar 2026 20:54:55 GMT  
		Size: 12.2 KB (12186 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9f6610c2b00376d3a0a9dabf0daf194c57602a306141599b6b8ecf0305c2e9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338843902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055642eb16f5b4c7cdf237deb1c368d6190c799b7c6fb7f217f2cb7c5eecec3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:54:11 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:54:11 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:54:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:54:25 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b00e434a3cdda16de45946214890a78ef309182aa508659f1ed8359196e53`  
		Last Modified: Thu, 26 Mar 2026 20:55:02 GMT  
		Size: 61.7 MB (61703578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b76f664a3b777525303c599b8bd0c3b5b73e8f1930181eb8895af28ceef84e`  
		Last Modified: Thu, 26 Mar 2026 20:55:06 GMT  
		Size: 273.1 MB (273147444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:c443fbf4c6de4511e7cf10a5c8390da1384398bcc136c23d4fc47d5e44d8da76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1053159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa4935278435b78d11c99a27beaa1d0d24d6c76377cb498b6e43378c1402676`

```dockerfile
```

-	Layers:
	-	`sha256:2b0eb2072123f60ccc028a025578e70e3ec3f24ea5341a12cacf1fcaff9351c2`  
		Last Modified: Thu, 26 Mar 2026 20:55:00 GMT  
		Size: 1.0 MB (1040856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdd071b830f0ab51ad869ac8875c3294e1a32cf5c40b76c6ccd6ac153059637`  
		Last Modified: Thu, 26 Mar 2026 20:54:59 GMT  
		Size: 12.3 KB (12303 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:b3baa7bea80c724d316915583758a75e0fc1a37556878c70e927958440ed7f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357395541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9813a5455cadd1eb248c20ae92d8bb8436e01a74aa6684f70d6f7640231c2cca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 20:57:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Mar 2026 20:57:08 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Thu, 26 Mar 2026 20:57:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Thu, 26 Mar 2026 20:57:25 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='9cd3fda5fd293890e36ab271af6a786ee22084b5f6c2b83fd8323cec6f0992c1';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='88761caacddb92cd79b0b1f939f3990ba1997d701a38b3e8dd6746a562f2a759';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='e15d033af90b7a55d170aac2d82cc28ddd96dbfcdda7c6d4eb8cb064a99c4646';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fee82cc96e90241b4bfe2fe85551ce2f74cf2697c140ec8471aae8ac190eaa`  
		Last Modified: Thu, 26 Mar 2026 20:58:37 GMT  
		Size: 61.5 MB (61515210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992ba84145f6742a186612deb104407d15f96a01c2356edd69d06121cb2557f`  
		Last Modified: Thu, 26 Mar 2026 20:58:40 GMT  
		Size: 292.3 MB (292304896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:8c8feaad7cdc10c9c3e3a062e5400e31887423910bf71c2936348c0777ce10ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.3 KB (986306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e174ed29e4f0b4258bc388ed248530e52d1a1057fe470c21cc6094de06eaef`

```dockerfile
```

-	Layers:
	-	`sha256:56c996ecdc86ad50cd7c7bbd731b588894d3d5fce0ee1c5928c6c1dffc7da834`  
		Last Modified: Thu, 26 Mar 2026 20:58:34 GMT  
		Size: 974.1 KB (974074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673753ef8b0b41fa85f79197ac4c61c38a407adfa5089a3fa6e69fb1d1db2c0e`  
		Last Modified: Thu, 26 Mar 2026 20:58:33 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
