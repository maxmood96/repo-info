## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:68b0409b41f925b0f7a122bbc2eccabaf7c6cfe34ee7b702ab69fdaeb84695bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:af4ee15728e632a91749340e19be7d93ec7c218a56478f1ecc8d764c33433056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231899876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e49e08c20baddf0f3acf94c44d99e9e8b2e7f565c03ba1e4ef680d5a61e2049`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:13 GMT
ADD file:2cd11339ae2bb967d59029b7608479e79b83bf117627766da2350baf6bcefc57 in / 
# Wed, 23 Jun 2021 00:20:13 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 17:47:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Wed, 23 Jun 2021 17:48:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='3dc5ef50861ee18657f9db2eeb7392f9c2a6c95c90ab41e45ab4ca71476b4338' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='67777ac3bc17277102f2ed73fd5f14c51f4ca5963adadf7f174adf4ebc38747b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='32a1532f7cef072a667bac53f1a5542c99666c4071af0c9549795bbdb2069ec1' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e50d1deb99048bc5782a0200aa33e4eea70747d49dffdc9d06812fd22a372515' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:31d64ed241e5742db627adab91980d09188228a29cdeba6d73f80fc250fa5e0f`  
		Last Modified: Wed, 23 Jun 2021 00:24:48 GMT  
		Size: 31.4 MB (31353970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d9befb7a60df20ae22d90f0f9d28969f46dfe41c0b467697c2b83d19daf07f`  
		Last Modified: Wed, 23 Jun 2021 17:52:05 GMT  
		Size: 200.5 MB (200545906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:afb8ea00075673518b1bfbad8dcc752af15992c7b1959882ca9155879a97fc15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251387876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c58b37546335fac48744790c4ce00e1d2b9b73edd3195ed028071eebc160392`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:01:34 GMT
ADD file:8c6e89731956c50d88f6fecbec5759d20881020f65da45d8ce70a04bcede6732 in / 
# Wed, 12 May 2021 01:01:37 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:25:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Thu, 17 Jun 2021 23:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='3dc5ef50861ee18657f9db2eeb7392f9c2a6c95c90ab41e45ab4ca71476b4338' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='67777ac3bc17277102f2ed73fd5f14c51f4ca5963adadf7f174adf4ebc38747b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='32a1532f7cef072a667bac53f1a5542c99666c4071af0c9549795bbdb2069ec1' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e50d1deb99048bc5782a0200aa33e4eea70747d49dffdc9d06812fd22a372515' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:df2b6748c241c44658a2bf32c779e91ff9ce09999beff9d91020d274c7cf112f`  
		Last Modified: Wed, 12 May 2021 01:18:29 GMT  
		Size: 26.6 MB (26553224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90677ea4b295d9f5f3e1650ab748bb4534f6ca2433aa87bbb14fbd5c710ac309`  
		Last Modified: Thu, 17 Jun 2021 23:31:14 GMT  
		Size: 224.8 MB (224834652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0cd9f641b776f96ad6702a0f8c32c1a80fdb0dee10fc450dbd29e73282f7052f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278345832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b44404ef17b9351bff4212b506bc1dcc3ac7d76980c3e7e9f17416a5e7ae79`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:15 GMT
ADD file:6874d465214a9ce35b9e8f82f16b9cc99d4080629ba6eaa630db86dc56861e9f in / 
# Tue, 22 Jun 2021 23:49:15 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:47:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Wed, 23 Jun 2021 04:47:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='3dc5ef50861ee18657f9db2eeb7392f9c2a6c95c90ab41e45ab4ca71476b4338' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='67777ac3bc17277102f2ed73fd5f14c51f4ca5963adadf7f174adf4ebc38747b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='32a1532f7cef072a667bac53f1a5542c99666c4071af0c9549795bbdb2069ec1' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e50d1deb99048bc5782a0200aa33e4eea70747d49dffdc9d06812fd22a372515' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:8159bacf4e4d80ebd092a33a4792eed7e4fb9f274e97b31d2090c317545477f6`  
		Last Modified: Tue, 22 Jun 2021 23:54:32 GMT  
		Size: 30.0 MB (30041114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aed79f6695de9226374000c9b0f308921260921ea93ce3025d496476bf6782f`  
		Last Modified: Wed, 23 Jun 2021 04:53:21 GMT  
		Size: 248.3 MB (248304718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b8b2ca4678e40ea3d9cc65c0493a94cf6d147e90ec0cc567a8abfec49d91e7b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272931167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcd350e73335a8c0e57d85bc13b77f2f4ba3d025d6d2464fc6cb76b4021ad0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:39:05 GMT
ADD file:bff33171228f4449adf88c454588c4700fad9ff9a9a5b7f616a9f9e0d9c6c8d0 in / 
# Tue, 22 Jun 2021 23:39:05 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 16:59:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Wed, 23 Jun 2021 16:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='3dc5ef50861ee18657f9db2eeb7392f9c2a6c95c90ab41e45ab4ca71476b4338' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='67777ac3bc17277102f2ed73fd5f14c51f4ca5963adadf7f174adf4ebc38747b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='32a1532f7cef072a667bac53f1a5542c99666c4071af0c9549795bbdb2069ec1' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e50d1deb99048bc5782a0200aa33e4eea70747d49dffdc9d06812fd22a372515' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d9f5c4e147c0ae408b8d2f3e29b6f9dd5c9efbc940234591cc565570b748924a`  
		Last Modified: Tue, 22 Jun 2021 23:45:24 GMT  
		Size: 32.4 MB (32367527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cd6099ad0d85548a57398f5aa7b95298dc1374fa62e04837cbca698d428866`  
		Last Modified: Wed, 23 Jun 2021 17:05:33 GMT  
		Size: 240.6 MB (240563640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
