## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json
