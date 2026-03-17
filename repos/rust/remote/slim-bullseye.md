## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:2caebcde6774a5b01f6e437e435459f8f3077eb3900de57c2f1444d8888c7afa
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
$ docker pull rust@sha256:24ec58301e750652cdf3b51c0ab2c8d1ee449aaba9f9a74d45d183a6dfd312f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303450289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc04903ed22f3e64dd5baddc95bc7403e595892f3ee23661976d790d7808a036`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:11:10 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 16 Mar 2026 23:11:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Mon, 16 Mar 2026 23:11:10 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10998fb1a4e927ed2de44ce67ee92bdefdb3dc83388c0d93b37c70959bc35f1`  
		Last Modified: Mon, 16 Mar 2026 23:11:51 GMT  
		Size: 273.2 MB (273192463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:49f5fb24bf0f6f60f4dd1d4768a61b743754a9ae267f94be2bd40c66452dac51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cffb220863ed7c4f6d332fddbb7ab602312fd45b5ac39ad6037aa4f1e13a06b`

```dockerfile
```

-	Layers:
	-	`sha256:0c8de6fef8aeb0e1995863ca3929a3791bf26e9733580e175d7f3a2976ec04c5`  
		Last Modified: Mon, 16 Mar 2026 23:11:46 GMT  
		Size: 4.3 MB (4312022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88e2cf2497ebd3b271b257a773d059d2b9f5febe72e2ce165c9840d7d4b6c663`  
		Last Modified: Mon, 16 Mar 2026 23:11:46 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:a53e16296baa331daeb6957a1f0e68ba5d5c3e6d6aa0a64f6191c4927ee3528c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323841855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f45ae5ddeafdd099cd2ece085b64c88fa1d6bf71308b2eb91ca7ef2632eb59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 00:28:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 17 Mar 2026 00:28:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Tue, 17 Mar 2026 00:28:08 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d1061694e5231bd5478948f1b788d67f9231a154595d6f632764ac9509b066`  
		Last Modified: Tue, 17 Mar 2026 00:28:48 GMT  
		Size: 298.3 MB (298290463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:652812017be28efb1e3fcbaac06fd72ed47bb9bc8a094f44a509a534b63632a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bd6d8b4d63a9904568282415a1f7ebfbc5ea9335fadfaeb65aafa6e6e09b6f`

```dockerfile
```

-	Layers:
	-	`sha256:d92bfe8cf0296aa466e73aaaf14182e6c8d41a7f3b12ab4ed9c60d1d4afac745`  
		Last Modified: Tue, 17 Mar 2026 00:28:43 GMT  
		Size: 4.1 MB (4120015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308f01aa6832dd1abd0889b1faf1ad7eed0411960d3d40f270091c40570cb81e`  
		Last Modified: Tue, 17 Mar 2026 00:28:42 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:eb9dbf79385c888668c72d3aeaa8a486956b311f9c72ff9b785a57962a23b73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262908384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342c7886beb727b69505942c3801c94c32da1ffcaac5df54dae28f386d3e3db1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:16:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 16 Mar 2026 23:16:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Mon, 16 Mar 2026 23:16:26 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35d764b8257734d1a28fc09969a0e6e67c48f2a12f02d70d25806292dd4c8ef`  
		Last Modified: Mon, 16 Mar 2026 23:17:01 GMT  
		Size: 234.2 MB (234163858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dcd5caa36f2f1dfe7e62245859f3809e3cbba36cb6eba6a3b9d903dba1f54b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e99deae367e5174a306c43616f4b6a5c53035fbfd17192dcae664f91b1906`

```dockerfile
```

-	Layers:
	-	`sha256:7763eb7dad2f47118d90bb0191acebe6127799f679010692b32ae9d21433e639`  
		Last Modified: Mon, 16 Mar 2026 23:16:56 GMT  
		Size: 4.3 MB (4308411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe52cf58565c3a9954cc00c675697356a79181f5ecd937de1fec590e3f0c8263`  
		Last Modified: Mon, 16 Mar 2026 23:16:56 GMT  
		Size: 12.8 KB (12817 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:da6c06320609b86da74ffd8694873719a7ea79f9e0a85aa2ab46d40350b8c83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329278261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75075f82991e7af1488385aebb4fcb4095bcfb4d18e48282cbb95292a719431`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:11:50 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 16 Mar 2026 23:11:50 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.0
# Mon, 16 Mar 2026 23:11:50 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f9a1ac4759c4f531107bbcb94882648bc1b2c093ca00c3ddc1fe3d72957fb19a`  
		Last Modified: Mon, 16 Mar 2026 21:57:07 GMT  
		Size: 31.2 MB (31191663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8437b5e6a080e7b5b796f5bef34d6b90da6e74050eb27e6851bc9878fb0b1747`  
		Last Modified: Mon, 16 Mar 2026 23:12:29 GMT  
		Size: 298.1 MB (298086598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c5c93c5f4e182598f0ba99af9de056f742449f25c654d0f789a96d65e9226c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ea6148f59d916b77eac58f6a9f9ae617577ea7dbcc0fa5333281c66b65dc5`

```dockerfile
```

-	Layers:
	-	`sha256:cfa4138bad0160f2c93f4672b50a61a5d951f39eba8a6121b0a054c4d737dd3e`  
		Last Modified: Mon, 16 Mar 2026 23:12:24 GMT  
		Size: 4.3 MB (4301764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f1aaded280ff484964a0955ff3e9ce6091bdb3ed484435fc1a5abe20193f6f`  
		Last Modified: Mon, 16 Mar 2026 23:12:24 GMT  
		Size: 12.7 KB (12681 bytes)  
		MIME: application/vnd.in-toto+json
