## `rust:slim-stretch`

```console
$ docker pull rust@sha256:299214bbee668fb11e2faa509f68a03ae8b4a86e269fcb35916865e7765d3a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:8f358020857edc0990ff065cde2e6cc413362b3e4cd889c875124547af13c98b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174796488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef81557a2594c7a7395901151e856283d6a91ffd22b31c04716a8f806e92bb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Mon, 03 Aug 2020 22:58:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.45.2
# Mon, 03 Aug 2020 22:58:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='49c96f3f74be82f4752b8bffcf81961dea5e6e94ce1ccba94435f12e871c3bdb' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='5a2be2919319e8778698fa9998002d1ec720efe7cb4f6ee4affb006b5e73f1be' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d93ef6f91dab8299f46eef26a56c2d97c66271cea60bf004f2f088a86a697078' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e3d0ae3cfce5c6941f74fed61ca83e53d4cd2deb431b906cbd0687f246efede4' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.22.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0de42bdcea098982661015d06080d5d8fbfc620efbef3ecbf8e4b13752dba`  
		Last Modified: Mon, 03 Aug 2020 23:01:25 GMT  
		Size: 152.3 MB (152280853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc7363f2b0f01c36ba264d37ceadf65dd73ad6d6eee08820e2363046b0d248bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178926770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b462b1fff841f4e2bd8e15fff7e1520cc56d294736eabc932a7f7419b423e15d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:10:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.45.2
# Tue, 04 Aug 2020 23:11:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='49c96f3f74be82f4752b8bffcf81961dea5e6e94ce1ccba94435f12e871c3bdb' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='5a2be2919319e8778698fa9998002d1ec720efe7cb4f6ee4affb006b5e73f1be' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d93ef6f91dab8299f46eef26a56c2d97c66271cea60bf004f2f088a86a697078' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e3d0ae3cfce5c6941f74fed61ca83e53d4cd2deb431b906cbd0687f246efede4' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.22.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235521a45cb93741b2cefc2ec27a9180dffff0140b79a41a2809806c18c26fee`  
		Last Modified: Tue, 04 Aug 2020 23:15:46 GMT  
		Size: 159.6 MB (159622159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b9973f0c0ba7f7c153aee29bcb2760119c81590403fa2af2176a2e0d217bbe60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179729126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889eefee81afa7a68bc816a18220c711a2c7aabffa55a13fb822d5a491b2d5e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 07:00:02 GMT
ADD file:448eac8822629a9f212483d0e6123c797105b2ec368648e6f259b7d4cb83e0a1 in / 
# Tue, 04 Aug 2020 07:00:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 15:30:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.45.2
# Tue, 04 Aug 2020 15:30:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='49c96f3f74be82f4752b8bffcf81961dea5e6e94ce1ccba94435f12e871c3bdb' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='5a2be2919319e8778698fa9998002d1ec720efe7cb4f6ee4affb006b5e73f1be' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d93ef6f91dab8299f46eef26a56c2d97c66271cea60bf004f2f088a86a697078' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e3d0ae3cfce5c6941f74fed61ca83e53d4cd2deb431b906cbd0687f246efede4' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.22.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:5984ce78d2759fcb147a7641f941b59e71e8c9f82aa5cb0e3d511c74c876a7e3`  
		Last Modified: Tue, 04 Aug 2020 07:06:31 GMT  
		Size: 20.4 MB (20377078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165632ad9235b37e542d8d442e5a2821fe2527da8cb50d2fe4ae8809c3d793e`  
		Last Modified: Tue, 04 Aug 2020 15:34:14 GMT  
		Size: 159.4 MB (159352048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:7238558025fe1bb6d0a5d0588d5205bb5dece8b13df351cb3a6b7e4e9ed5121a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199345801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c494aeefaa178cbd3516203390a1eb3cc5c21b0d4734977728b263ffc60d817b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:40:13 GMT
ADD file:ff2993d54fcdf1a789ee9e5b098096c1283c9949774c2a2a20ff74ddcd2c7534 in / 
# Tue, 04 Aug 2020 03:40:13 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:47:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.45.2
# Tue, 04 Aug 2020 06:47:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='49c96f3f74be82f4752b8bffcf81961dea5e6e94ce1ccba94435f12e871c3bdb' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='5a2be2919319e8778698fa9998002d1ec720efe7cb4f6ee4affb006b5e73f1be' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d93ef6f91dab8299f46eef26a56c2d97c66271cea60bf004f2f088a86a697078' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e3d0ae3cfce5c6941f74fed61ca83e53d4cd2deb431b906cbd0687f246efede4' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.22.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3a48bd72000b026c382f2687d17167c79613e7af6b30df4ac42b015d7ab40315`  
		Last Modified: Tue, 04 Aug 2020 03:45:51 GMT  
		Size: 23.1 MB (23148236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f76ef24e0a4187fc24d5093b408cd1c57ff0988d6207a5969a4e1df705b88b`  
		Last Modified: Tue, 04 Aug 2020 06:49:39 GMT  
		Size: 176.2 MB (176197565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
