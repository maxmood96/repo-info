## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:405e5b0fe9f74098d19f3a7b65368c9cd4323758dd6b2d6305a35df8d2cc0a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f8c0bb10d0e408141ae1ce9db3906933d04044014b81315956bb8babefdb4538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ed3fc33b113775a941d354adccbf40b6a225401b883ee5966de1c83f41b2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88fad72c2506246ffe6396d482cf40fced3dbdcef8f4356795a7cac8ff6b2ef`  
		Last Modified: Tue, 08 Apr 2025 01:35:00 GMT  
		Size: 259.0 MB (258988010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4741338f8e175f2156ac1827a7e205ed3ea2f97dab9e129c70963ec485678779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0edf37b8243573464db9fa035308a4066da5453afcc99b305823cb05f7a7437`

```dockerfile
```

-	Layers:
	-	`sha256:9eb94d3eacd1815973a9e0b2b8d9ea7e1aba5c23b593f6bc9dcc7afb1bdd484c`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 4.2 MB (4175124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3cecfcf1347fea0549f31ad4367cab149129294dc8dfc57ccf6d6f0813fff`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:64862b5819093237df39378fbaa1b43498424fab0bec03cae5733be1b24142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309037855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6173382e6c055035ab42b01f20d2e1159bc44baf086271255b1ca3daf44909`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabdae83abb8c4e7989a8005a7a92a8535e6ab6c0bd633442c316443e6f2bab`  
		Last Modified: Tue, 08 Apr 2025 16:53:16 GMT  
		Size: 283.5 MB (283498720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a1e648062c749afa43013786ee2772e71053aae03cb4782bbc4537e21bc45a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80946ceab5e2263d6a3d2080648d12b9fa299c11ee188d9f752f9d87cf949f4e`

```dockerfile
```

-	Layers:
	-	`sha256:82474d826cb3957f1fe6d11964dabb805591e256095862418b74e61335f2d2bb`  
		Last Modified: Tue, 08 Apr 2025 16:53:10 GMT  
		Size: 4.0 MB (3984274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1e96c51cd14f17a15a43d875ce615aeb964e08b5edb459ce6c20c3722eb049`  
		Last Modified: Tue, 08 Apr 2025 16:53:09 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:663387b95b7c33a5430b967b31ff194fcdda0a1ce99f5b57701067a097d7790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252089618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f3327734efe4ca704111ca38e47742d41d1d6dbf7fd5f688890f0d51b0358`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae574b04e648f49bc601b389c9fe05b55820b884d921b0be2237f6bcbe8a3f94`  
		Last Modified: Tue, 08 Apr 2025 10:47:57 GMT  
		Size: 223.3 MB (223340120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:82d09db72e41c93ab2119868ef3741a813878f94117b474e06283adb390fbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4183262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544589af526ae2c336c2f08de66d4d92a1e44abc4a3bc1dc03656c481d5d7819`

```dockerfile
```

-	Layers:
	-	`sha256:b88826ea138c560bd03b90c875666115d0b79433cb4be2921f0d1aa605f9dc33`  
		Last Modified: Tue, 08 Apr 2025 10:47:52 GMT  
		Size: 4.2 MB (4171802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef1d405fbb2d4f000818000750480dae3e874eb9e5dd56ae60396665119ffe`  
		Last Modified: Tue, 08 Apr 2025 10:47:51 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:43df35999046bea8233d1a5fdfcd2356fba15a793fbeb9fa5224d1262adf2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34f303281cbb2b93f669a37283d0e2d6c0068957020ef6fa5232b882c63638`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b380f9c572c29705a08754c4980a85f7915a4d9cd340d7f3c36e3926cba3001`  
		Last Modified: Tue, 08 Apr 2025 01:29:00 GMT  
		Size: 282.9 MB (282912918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d00c62057a0ddf1ba7ff04c110803c0702d91dcdad6a4eed7e9ff8f85cc8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ca8b84c676afa150db9ce38fd1bfaca44431b98cdac4af32efe184523a8ca`

```dockerfile
```

-	Layers:
	-	`sha256:80703f1c4e5c8b72cdde3f31569d00b27ba521369410893b3e2dbc529daa0b19`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 4.2 MB (4165381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fd41d56f3f22ed5780318a7bc49397260241142ba692570d227a36598e668b`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
