## `rust:1-alpine3.12`

```console
$ docker pull rust@sha256:bba61cf2d94f72860e4cab8adfc1bc3bb76b0bb02c5a3e4221713997ba21ff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1-alpine3.12` - linux; amd64

```console
$ docker pull rust@sha256:9597c2fca816d330ff387ea93d6c4b2b50264533a61cfab3134da89459045301
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (183992258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d0e19ed16e2ba08216ecfbb796802fec0c6d97b61c0d15fdb938c684dd4c9a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2020 19:22:19 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 16 Jul 2020 22:55:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.45.0
# Thu, 16 Jul 2020 22:55:25 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.22.1/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "cee31c6f72b953c6293fd5d40142c7d61aa85db2a5ea81b3519fe1b492148dc9 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e80d17ab1e216ced34af8e4c92cbdcb53881599ae0a364b0de54ceafa10317`  
		Last Modified: Thu, 18 Jun 2020 19:25:47 GMT  
		Size: 47.6 MB (47612931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739e99f6bb87d92b1dc412b8dc1b0c09541feeb92b8ed7e5de3d4a6e80dc2350`  
		Last Modified: Thu, 16 Jul 2020 22:58:23 GMT  
		Size: 133.6 MB (133581786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
