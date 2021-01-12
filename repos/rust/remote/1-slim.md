## `rust:1-slim`

```console
$ docker pull rust@sha256:228ddd14221ea441133e03105adb279bba1b25059e4c8631bd193e450cf7a676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:7a496a40f86bdbe8c6e0013ec48892ab74fb6443e7ca43a6d5729c13a34b2a25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213895248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59407856b415d63c5b559cc9fe84802f7d82c388705110d8def96f6b1f6ceb2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Thu, 31 Dec 2020 20:28:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Thu, 31 Dec 2020 20:28:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06291b7251383aaa2c26791323fe00ec996aa4912f9daa2ac08be07088774db`  
		Last Modified: Thu, 31 Dec 2020 20:31:23 GMT  
		Size: 186.8 MB (186795953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:58cb29151843a8ba8e0e78e3f80096ed2f9514cf81d4f85ef43727140631e67b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206569511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ad083135a978be91ba6fc632894746345f0fe9987a044035627a1580e09c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:01:09 GMT
ADD file:1db27e410cc7caf4a97a7313c57260fd01aa134b84306914ef0948dcca27372d in / 
# Tue, 12 Jan 2021 00:01:12 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 17:00:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Tue, 12 Jan 2021 17:01:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:be493c6a598447fe5f46a390f3bee10f2d2ba2215d39829fe84eb40a7add18fc`  
		Last Modified: Tue, 12 Jan 2021 00:11:14 GMT  
		Size: 22.7 MB (22715905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ecc7dc7ad421b9a1666d6547fca14549055db658eef606b8f2ae23ea9c49d`  
		Last Modified: Tue, 12 Jan 2021 17:03:46 GMT  
		Size: 183.9 MB (183853606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2a44876432ba0cfbe7f7fcddd9b16f316ee13abecdee43b25f0645529966bc40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213527123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae6556c4805e09e56e96830d6766c3c98e489ac25c83872e0eea71711fe6c4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 15:38:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Tue, 12 Jan 2021 15:38:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c6556a88cfbc71622acf881baad2b6313935f968f330b68df7d2683b9c93e`  
		Last Modified: Tue, 12 Jan 2021 15:41:26 GMT  
		Size: 187.7 MB (187662631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:4db22b065e46759eaaf77b188e33cdfcea47d868b69b3e0417b288599385bd07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238719663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3805264c2812884369a35d2db08aca46b8c18cf603954fb4fe4e4c3d5b5530e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 15:54:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.49.0
# Tue, 12 Jan 2021 15:54:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dbd0491b35bb304ef53ee3107407181ed28323d0397b7ea1f8384868763b4b`  
		Last Modified: Tue, 12 Jan 2021 15:57:15 GMT  
		Size: 211.0 MB (210951672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
