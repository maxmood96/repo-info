## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:aac7caa6be67bc543a8c2c781d0c292a29b0e32f1b76063a35524f72219ffbaf
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

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8d311b86ed3db7efe841635a903c3765a83fb25aac886094b734fa79e3436401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372521ceb50eb497542b57d5d137deb3f4d8c1cd7ed97e2886e7ba78d698e61c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a95fe359d00e495189668dbe141be195ddf6d9a78a3082d0ab208fdc048646`  
		Last Modified: Thu, 26 Jun 2025 21:04:38 GMT  
		Size: 293.6 MB (293626479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:29425eb8a1d68f1bbd8e12f72d8e8412227101a7ea2bbfcbb08ffdecc16dd6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f8553b1a62a234f1e2de1872ad54fb81046a5e5d3488912c7f03d53fac8b9`

```dockerfile
```

-	Layers:
	-	`sha256:3c4570be354a09a65f6322bcd4900c854c27ff3ba1fd7580c1985424064ce0e9`  
		Last Modified: Thu, 26 Jun 2025 20:45:28 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829de61e486f36994eea1fe7fef9b96d35abfccaf411ce97d9c8646e7d72ecd2`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:849df862c37c0b0b2dc2d6716ea8519a1f522670921b7b956bf23b823a73f299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a9643ca0f165c66b54e20b4605c0a5c112e93404d3b0ba30efcfe1ab6ad31f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e645d97c2d6a467464c4a80d44a3ac857fa9cca6f0fac0cd777bb89ee1508f7c`  
		Last Modified: Thu, 26 Jun 2025 20:53:31 GMT  
		Size: 240.1 MB (240101856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a85e402c326f3c03e9708ff16120d2c42f7dbcb2e933f19fbb76f11370a6576b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518b6db85de72bbdbe24639ab5a3c4f190131615ff61534fad749f42c8623a49`

```dockerfile
```

-	Layers:
	-	`sha256:2f55a9249efdf67ba656e9474ca10403d8848d6260d0be2c66c50181e3668161`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9caee02c300ab03eee5347edfcfa4c22f0603340af720028236005d0e2cc86`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 02:32:39 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:a6ee3270db18b47a5e87713537b2552b107475ebcb84af1cbcb893af8e2664d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bdc1aa016a9d46b2d995a804b4d8bab75cb01253cae429665ef1d6c723f782`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca28e97a4786e8eb37b8a7c36854e36243402fed50c3e5fe3ea277b12db1832`  
		Last Modified: Thu, 26 Jun 2025 21:07:05 GMT  
		Size: 342.5 MB (342488943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bd6ccbc96e8bfbc97a901d2e33f7c99ae90c565d46501b2165dc621a8e77afc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b93f13d591905af63ad162128ecd1011d38b18ee1e7296c5ed57f44cba8eaae`

```dockerfile
```

-	Layers:
	-	`sha256:9b1eb705233ea430fd4485b9666c14cddb09a587e5580d476f0b9e1c583bf01c`  
		Last Modified: Thu, 26 Jun 2025 20:45:44 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e38d3ec1890649c6050eec5b78c8680784cc2c13f1171dcbb6913de23df840`  
		Last Modified: Thu, 26 Jun 2025 20:45:45 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:ab7f8b1541ae8eb7195601482c8731e87de2e71efdb90912e0e8f3f658480d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a376c365ae3c3044ed47080fdda8ad87aa7e9c0dfdc3b6295a0814cc609f2f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48104e7273eea950b755061c537f29f84178d333006c1c9740d1a17e2335a7f8`  
		Last Modified: Thu, 26 Jun 2025 21:07:10 GMT  
		Size: 333.5 MB (333504316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6be14fe5ba2c09b82ceb30bf7b75fba23c09cd4f9a5981ba850e8394ae31ba20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0666d55d422e137ff91a2199c79ce1381de129fcf1dda669d564a10d1cfce489`

```dockerfile
```

-	Layers:
	-	`sha256:ed6de95ff52034d4c3cd2306eb1d0ea09a8688d01097eb4b676bd054b19a46d3`  
		Last Modified: Thu, 26 Jun 2025 20:45:49 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c918139e98dba5b16dd10dad8428ba99ec7bec44446be184a29df8170e1a8b02`  
		Last Modified: Thu, 26 Jun 2025 20:45:50 GMT  
		Size: 13.3 KB (13270 bytes)  
		MIME: application/vnd.in-toto+json
