## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:2fe55129f54ca2eff36278ff3afaea300720ad7e645cdb7567039daca9c3cbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:37ffda431022698abc8316207592fb9f2d388a129ee1bb8a169fad3f549ce0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269552605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7986cce88d4af57a0fea7746af7993d99b720ba743e3033c87b2ab7ef9466ea9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987164d58d99713a86899ae634f06f38b55cd4e5e4522666e2543e12dfb54db0`  
		Last Modified: Tue, 23 Jul 2024 07:27:01 GMT  
		Size: 238.1 MB (238124275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fd673804da5b9cc4769e358238cd365e15ae348c65c4e0d7382bcaed28d29dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d9095b60772e891e74c7ca1a09a1394563a97fb412f6506c416e2cd245ac6d`

```dockerfile
```

-	Layers:
	-	`sha256:c9c5307f4b60a39f8eaec1e75fddda81f71679fc4a2d2e2a8ed7edfe99c8f773`  
		Last Modified: Tue, 23 Jul 2024 07:26:55 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd952bc8d79e92d0cf17e5853a8a1c5a242a11bbee63903a2ca43e3ff2a15578`  
		Last Modified: Tue, 23 Jul 2024 07:26:55 GMT  
		Size: 11.9 KB (11863 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f475f2120cebe9a45e6aa66cb9a03367831d551aaa14ad239338321d621a607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285544832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac05971e524fdf3233e1bc1ec8ab31ecec14b0f1c2fd17486f80663c5728a1a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 15:35:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 25 Jul 2024 15:35:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.0
# Thu, 25 Jul 2024 15:35:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5206e7b140ced3750e22afad0b0e144a35d26c5f18f9429513300d4d5ce775`  
		Last Modified: Thu, 25 Jul 2024 21:05:03 GMT  
		Size: 259.0 MB (258955702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6a5c0b31adaff21ed061ca80f98019ab06b61369259ee22dfb0356301d171229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e51a0baec4d836e209ed5efd18e50338d8dfbd7a28b1a529c7b64b001ecb74`

```dockerfile
```

-	Layers:
	-	`sha256:37cbf4bb77965b30a0c0ece4c7719623bfa9550273adc058a85bda6f0bc84f13`  
		Last Modified: Thu, 25 Jul 2024 21:04:58 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0e9586baead85c74d991b8eeaf615790d124d9e7917ba952bc93ed42a487fd`  
		Last Modified: Thu, 25 Jul 2024 21:04:57 GMT  
		Size: 11.9 KB (11936 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66022b5fd653ebd82fbe98610963654f22f5eee8e13148a375a2ee72cf9f0a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332526610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0090d7c2cda85a5b509f5ca71871d7b3c5e9a34573a3bc0916f772833251930`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748563ef3a74e77a78d753b959024546a23902216042a065e459705d497e94de`  
		Last Modified: Wed, 24 Jul 2024 08:17:30 GMT  
		Size: 302.5 MB (302450527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f458f5aeadf8a5790b2408bdb145903daadc070f647d8c6533fbe4013c18d8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0d9db7190d9673cc3c9ec743c7b2787e6df18190b99d4cfa24347351340b66`

```dockerfile
```

-	Layers:
	-	`sha256:0064383bbe68f5bef07d120f5150714ff39367d171ef690a6ce407ed04d7f6df`  
		Last Modified: Wed, 24 Jul 2024 08:17:23 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0957f90fb5752c2132d992f1de44f141874191e79855f6331185fca2ef3a4431`  
		Last Modified: Wed, 24 Jul 2024 08:17:23 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:53c2c50e8cffb326d57cf006a480aaee7a3239ad12689b96430be32f70539444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286334009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a26f8f6d5fe1926a59fed01bbc9abf20962ed54fdee3cdf488e347b8f03d00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:35 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Tue, 23 Jul 2024 03:54:36 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 15:35:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 25 Jul 2024 15:35:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.0
# Thu, 25 Jul 2024 15:35:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736db6ea864c62884eaae6de292a353e60d7fb09ad20c8713ed990f1154db563`  
		Last Modified: Thu, 25 Jul 2024 21:01:23 GMT  
		Size: 253.9 MB (253920201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d11140cf74730b9379aa21efa6c8ce6c6c983680b679e15e750419e04b38fdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ef05708bebaf0301e4485368467cd363054ca12653ae82cec8a1269226974b`

```dockerfile
```

-	Layers:
	-	`sha256:74506efeb6a57e2eda1452cdc6cac0819582f8141adc813033a0be0e3dc0850a`  
		Last Modified: Thu, 25 Jul 2024 21:01:18 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dd5681e615b12728573dbc27b44c4f2e108c3f9401e8f26b6c3a893221a0fd`  
		Last Modified: Thu, 25 Jul 2024 21:01:18 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:ae0c7c21811d6c5e569555e3b14a0c818272b9dbff91dd797d03bb24648712ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277857013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28da409b076f40c742ace6833c056943a1e887c5e9cf9004862c551e6cd21f25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72735da2b75e508aa6d2000b49b9a64b6040b211a083a92159e3b627de2773f2`  
		Last Modified: Wed, 24 Jul 2024 11:50:54 GMT  
		Size: 242.6 MB (242551810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:03db106e5ccdac6ad532d10f37c1f50202d42e1ea9687a9606e33b0218a03372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6badde6f7f8b33a6a39a3bb398090040e50b4009ce14ffdeb23210f73e77819e`

```dockerfile
```

-	Layers:
	-	`sha256:1823df0d6c1b12807be5ab6011b67b9784aa39901282f2eabcb57d1cc5a1498f`  
		Last Modified: Wed, 24 Jul 2024 11:50:48 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7398af0409e399ecb1ce0640a39c80708a50300890302f5b6f57b4dd3ee62c8`  
		Last Modified: Wed, 24 Jul 2024 11:50:47 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:fe4e798815dd8c4608832bcb41462339871584a130fe4e95e79ef35aa81ec1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335198187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443cd06aced83a4af1b3360ef8c4133c12db4c0e1dd3cdc5e15ee30b38177542`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:25 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Tue, 23 Jul 2024 02:28:26 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 15:35:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 25 Jul 2024 15:35:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.0
# Thu, 25 Jul 2024 15:35:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cf98e8335a39aa3d5feb8de22e9b504ff41c7e2deeac6a7784d1648b6c3034`  
		Last Modified: Thu, 25 Jul 2024 21:04:13 GMT  
		Size: 305.5 MB (305529169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:846df9f41fadbdc51ff6f2df842d436c84b9e6c8a25f1b9fff515a142096f860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce2d201cbdf5acac480313e58758e5f4e63eb66ce633ba34a043d80df79214`

```dockerfile
```

-	Layers:
	-	`sha256:260302e92c2e3c6622a370b02eefc7e20ad055a0dc32d5f3ef887829ee9e3a28`  
		Last Modified: Thu, 25 Jul 2024 21:04:08 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d7184abdce8b406e6d603a65e077c4d7d75a620034d3bf8d3299e2967d733ad`  
		Last Modified: Thu, 25 Jul 2024 21:04:08 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
