## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:0b8421caa1cdf5084146dc1be28ddc8aae54d17e50bf69ce64ec38b648a5b3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:38784ea86e87f1efd67850a7a8a2711b9127b115e976c84f2fbfcc90d6023c45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277172541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f211ae749dae8cb66c10dfd8f653ea412d69628fbae0d8ce852d714a952a76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:46 GMT
ADD file:382dcc0dd39da90030a2de09d6847df082978a1a8ba5f3b2c7f678a1a5e917f3 in / 
# Wed, 12 Apr 2023 00:19:46 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:35:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Wed, 12 Apr 2023 10:35:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:143db7d084219658b1d5dc81071b28069505f56c5edd84ce9783d7d1b0689f38`  
		Last Modified: Wed, 12 Apr 2023 00:23:05 GMT  
		Size: 29.1 MB (29082376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151fbc0ccd0f2937224610aa64fd8b003a8811d4b75f3396b6e91f0e13a8e6c8`  
		Last Modified: Wed, 12 Apr 2023 10:40:03 GMT  
		Size: 248.1 MB (248090165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:7b96d19cc9cb34e0c26be5dd833f9fdf11028803303564502104c27e2258c47c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284324854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaee4fd870455b6ebdec369267f096f426e5cc43ef269f5c7f92d6dec08c926`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:23 GMT
ADD file:36d02b31daca0f075647db22cc533cb3cc40954d9f5dbb85dca7694dd2112216 in / 
# Tue, 11 Apr 2023 23:59:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:20:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Wed, 12 Apr 2023 08:20:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:7e02fe4f8cb8b942d6a16a9477520427d663c18b1385de1e0c62edf5c17037a2`  
		Last Modified: Wed, 12 Apr 2023 00:02:43 GMT  
		Size: 25.7 MB (25672981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333313722a940dcf7f83874817ced8a9eeed27266016cc8fc2d52da12541e4ed`  
		Last Modified: Wed, 12 Apr 2023 08:23:52 GMT  
		Size: 258.7 MB (258651873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:dac14dfb1b91e6632a9178520d8323deb4bc049f3850a3679bff804d3a251949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338137496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebea9490fa13ddb57140edc8b34ee97ef461bc4eef396d9873848be0bbe1129`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:36 GMT
ADD file:f9329dbe55130ad6519986bd39af4c990be00854398667ae7e57b1e77112fa2c in / 
# Wed, 12 Apr 2023 00:39:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 12:53:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Wed, 12 Apr 2023 12:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:2a4e4be009fb4bf3377ee02176cde1465e9aa86b2ca16b6f906d04d62b5e600d`  
		Last Modified: Wed, 12 Apr 2023 00:42:01 GMT  
		Size: 29.1 MB (29121294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec92e9159f5512feaa0d2ac514a45afccc82a73a7c77930d8200df20be21848`  
		Last Modified: Wed, 12 Apr 2023 12:58:34 GMT  
		Size: 309.0 MB (309016202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:53865b83af7356ba48aceafeccd6e1635e148281a6a1809d0ae345d89beaae97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290115419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bb2203df95ee9a584db90dfe5f2fd2c4f6bf43d485bbf5601d0ac20056355a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:41 GMT
ADD file:95913b5ae0f08fceb261e02adcee66071562c6366fbf309f33e6b54479abe59a in / 
# Wed, 12 Apr 2023 00:38:41 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 15:45:59 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.2
# Wed, 12 Apr 2023 15:46:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:75d8cbfc608962b83bb059f2130cdb4d8502e95801d291dce6ae1695dd1608bd`  
		Last Modified: Wed, 12 Apr 2023 00:42:02 GMT  
		Size: 30.1 MB (30102772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f74d64f50ce0b94d856e10a49e78bfc9fcf71390938d076649898fbac8d1a2e`  
		Last Modified: Wed, 12 Apr 2023 15:52:50 GMT  
		Size: 260.0 MB (260012647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
