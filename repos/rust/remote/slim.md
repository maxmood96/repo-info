## `rust:slim`

```console
$ docker pull rust@sha256:ca6e0803131b678a41c3c0a54867fee22444942bf28d8776fb73e43855c2bca7
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

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:359983f2bce6874e38367f30f6b116392f812772c464642fe5e52a2fb1e2f59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee254c30526616708c08f9716aa0a9b9f084c8457b9091cffdbe6a25deecb94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3fc82887aef5e54a660e1e881b330eb4ed6e4bb9444cd50be5be4239bc7b45`  
		Last Modified: Mon, 29 Apr 2024 19:49:17 GMT  
		Size: 256.2 MB (256249043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4899230234456d41c256bc481a9f9a9dfcc2e0a408a361823013741a8fd2ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656443dd76eb6d6966a0bae0169dfb9ae52c503115473acfceae0881b5bdf347`

```dockerfile
```

-	Layers:
	-	`sha256:474fcc5c3664599bffb59ee37ae9254ddf837ada46d2014b485f308365258ce4`  
		Last Modified: Mon, 29 Apr 2024 19:49:12 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:553b8396d841d367a4c57bcc6262d8a662bfe04eba94ae9d5dcced614bb9d40a`  
		Last Modified: Mon, 29 Apr 2024 19:49:11 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8991dde5a00d6c74da09fe98612f7383338540e4f3e6b13cb33f9566a73160a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336467807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635ffd565a045404c85e84e8dceca896fd64d8ac5ac76e03016b0dac23ad62c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08cb2d082c2626977e40e88edcba82165dbb86c76f940fd58647d45db5c8e1c`  
		Last Modified: Tue, 30 Apr 2024 06:30:20 GMT  
		Size: 307.3 MB (307287872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:012227c103378058ef2e1c157847bd392b83b0f5f53c161af68567ccabc57173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36773060f706aa28404f51577ff178d601bf110d761e46a55bcb6acf68700ee1`

```dockerfile
```

-	Layers:
	-	`sha256:3f26060cc9210273dbc1da711483a01f3df6c4e8017aef877bb6ba56df4f4de6`  
		Last Modified: Tue, 30 Apr 2024 06:30:14 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48fd1ada47963bce35a7d41daef7a1fe6a77ca0d2431956f8999bbcca9899b6`  
		Last Modified: Tue, 30 Apr 2024 06:30:14 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:16229532b3afe12894fbb196a63c91ea6f848e7c6f896456be4ad2446952504d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332325109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40e5d6a097024a7e9f54d35e687db6b7b9c83f1b727745d6ed3704f2c121ffb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1194547d8e84b94c1f905b01b6d3aa05aee094bf9c04df8fcf13056d9926f2d9`  
		Last Modified: Mon, 29 Apr 2024 19:40:18 GMT  
		Size: 304.8 MB (304812754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3821eb9925a04580eaab98b615e7c42096e092ff3a11eefafcaaca5553980fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac50d94903116ee2a6d19494b8e8d2e41e4c1ae7c6bad29576c583ce8ba203ce`

```dockerfile
```

-	Layers:
	-	`sha256:572cc696a924161de1c76817a33832869018208c510822ef0808863f9ada96a8`  
		Last Modified: Mon, 29 Apr 2024 19:40:14 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffdec964d0f7af10b80d1b5161a9fce73c910501d017018b5b72a409746e5a7`  
		Last Modified: Mon, 29 Apr 2024 19:40:13 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json
