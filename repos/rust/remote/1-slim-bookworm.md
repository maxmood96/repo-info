## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:a0ec8004db470ca2e5475621234dfe53c6d1be79b50d1de1de8c4d27aa092331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:6eaf97af4566844305641159183461e2acb624e7dccce49bcdbf1e1850f6c1a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279442476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce8a0e8a984dfaf00dc8f7e8a3b20b372a10f0fa844b05834870fd7180ecb50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:46 GMT
ADD file:382dcc0dd39da90030a2de09d6847df082978a1a8ba5f3b2c7f678a1a5e917f3 in / 
# Wed, 12 Apr 2023 00:19:46 GMT
CMD ["bash"]
# Thu, 20 Apr 2023 20:48:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Thu, 20 Apr 2023 20:48:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:143db7d084219658b1d5dc81071b28069505f56c5edd84ce9783d7d1b0689f38`  
		Last Modified: Wed, 12 Apr 2023 00:23:05 GMT  
		Size: 29.1 MB (29082376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff02d453fcb0d138b15bf0d5edf56e17ebcf4bb4e66534ac86d2b116275e2f8`  
		Last Modified: Thu, 20 Apr 2023 20:53:56 GMT  
		Size: 250.4 MB (250360100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:5be2500e44ad3aaa9c0ddbdbb527ef0bcc1377fe1113cf662102d1372d7f1a7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279779201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7b599142af0a461648a1ff7997db46ec0b2bc2d94104fec69a4fef58a6e116`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:36 GMT
ADD file:e771d6b2e2850268fcc9dff0019be11ba90fe85b488e205a9d33057159a17211 in / 
# Tue, 02 May 2023 23:47:36 GMT
CMD ["bash"]
# Wed, 03 May 2023 15:40:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Wed, 03 May 2023 15:41:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:8a2e9321dbdef2d3e23adde50603a12199d5f152a46c8f95b1be6f81d94c5125`  
		Last Modified: Tue, 02 May 2023 23:50:52 GMT  
		Size: 24.8 MB (24785091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7774af0e81a49cef4565e9031e82489860727fd5723727413074f1011badfe8`  
		Last Modified: Wed, 03 May 2023 15:46:00 GMT  
		Size: 255.0 MB (254994110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b3a015a4752bcb6864c26a3f1d9655686ad58b56441d11b3d24c2b76ab996a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340156692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad4fd9f6a7317399ac9bce8fe643535e9f59d621d12b1bd8bee2522b9503d82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:36 GMT
ADD file:f9329dbe55130ad6519986bd39af4c990be00854398667ae7e57b1e77112fa2c in / 
# Wed, 12 Apr 2023 00:39:36 GMT
CMD ["bash"]
# Thu, 20 Apr 2023 22:09:37 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Thu, 20 Apr 2023 22:10:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:2a4e4be009fb4bf3377ee02176cde1465e9aa86b2ca16b6f906d04d62b5e600d`  
		Last Modified: Wed, 12 Apr 2023 00:42:01 GMT  
		Size: 29.1 MB (29121294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7c3baab32af2cae55b1037804fc418cdb8e4ee9062a8809a5c6290703d9ef`  
		Last Modified: Thu, 20 Apr 2023 22:15:40 GMT  
		Size: 311.0 MB (311035398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:e939eed51a3f3223b1e14d06a2c0116e92407af43374f5343a6894ac1bae6f27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292063068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a9eba58590470495760f0494d50fd32a0f5c09b9bd9926fc036acc19f71c62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:41 GMT
ADD file:95913b5ae0f08fceb261e02adcee66071562c6366fbf309f33e6b54479abe59a in / 
# Wed, 12 Apr 2023 00:38:41 GMT
CMD ["bash"]
# Thu, 20 Apr 2023 21:00:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Thu, 20 Apr 2023 21:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:75d8cbfc608962b83bb059f2130cdb4d8502e95801d291dce6ae1695dd1608bd`  
		Last Modified: Wed, 12 Apr 2023 00:42:02 GMT  
		Size: 30.1 MB (30102772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296a0c683b460bfa9511f4d3ebf8b15c239a2b8e47b1b394b3bb2d934582f6b0`  
		Last Modified: Thu, 20 Apr 2023 21:07:27 GMT  
		Size: 262.0 MB (261960296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
