## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:6647ee008601b95358d213ff0767a67ccb0895a6f48556490cc76dbe24d415c4
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ec64e0e83535998ddc24f76ee1ff4fbdcc8fce088cbb35f8cbfb3d2e98508495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303748073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a16fff4c6cc8cfadefbf93676f53555d549e04299ae47b77b935eda39fd5bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Mon, 10 Nov 2025 20:11:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:11:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:11:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d66572fffa4ab0324db789080b200116c9ea5100f14e3acb6be204871edd0`  
		Last Modified: Mon, 10 Nov 2025 22:00:28 GMT  
		Size: 273.5 MB (273489477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e4b43b90ed271d141c5e7363fac6b27ecebeb12507ffd9b0373d2c759f0424a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8a2ad181d54e70bf9cc2557bb4b4f7a151f73795319adf50766ab4c16d928c`

```dockerfile
```

-	Layers:
	-	`sha256:13b73ce24631f27d42962f429dea5c7e1d026c4752d6dea4c5748e7c01d4578b`  
		Last Modified: Mon, 10 Nov 2025 21:45:59 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71e64b7615b142083bd36f03b5580dae2ce22ce4e055717afeb1be3ae426f0e`  
		Last Modified: Mon, 10 Nov 2025 21:46:00 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fe0fafbb9b56311c8a507ec5a11852113692dfb733a9ad6c7f832e2f4abe5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325807166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71033a404fa1ff804b8b3e11523af716e90a157323f377b9a4e864e18470fd66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Mon, 10 Nov 2025 20:12:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:12:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:12:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdba5d2c395245baf429e98eddaa17549f0917e7ac7a50cb1efafe3626da3e5`  
		Last Modified: Mon, 10 Nov 2025 23:13:28 GMT  
		Size: 300.3 MB (300260840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:88e6efc0b660fd8da2b4d5188fd0e52371fa750b0974b5531f38193242a6bc33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194b69d9e27c290aaa8f804c0cebcc2bafff804013411ec413d6460022cf6411`

```dockerfile
```

-	Layers:
	-	`sha256:e86e3c52f42f5f7c7ddca68cf185639471c8b8f8ebd6c26712865f59d64037cb`  
		Last Modified: Mon, 10 Nov 2025 21:46:06 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dfdb2267ad59493b4043275a2ee8b241795baff27c4cc7462b6477cffa4ac0`  
		Last Modified: Mon, 10 Nov 2025 21:46:07 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ed49bf4ce1ffa8a010738ad88a19ad26c7ecd9a1fd7af3d618fd3808b6686d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264724206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bd759e7277b152f9ebb6bcfc62e9c6ac57b164498e893d105f20ec4b8da69f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Mon, 10 Nov 2025 20:16:03 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:16:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:16:03 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7192ca09e5a41e082a7e7b496ed640ab6636f5212d593cde10d3586b8ab3d214`  
		Last Modified: Mon, 10 Nov 2025 21:46:53 GMT  
		Size: 236.0 MB (235975654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c48c1b88c6375914f88081a9dfcee1e3f90b260eb63d24bcf75d97e4b249901a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94416036bc96d264bd406c35477268f3c13ca05915d0f162942c4fc5f01fbf2`

```dockerfile
```

-	Layers:
	-	`sha256:115631664fadc3de861d56e6298ea3d61ab09fa9552eb5f002b89268ba7d71dc`  
		Last Modified: Mon, 10 Nov 2025 21:46:12 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b856f4eeee55fba2e98306a2c6e1d3d7888db553a33006f778efd9fffdcc91d0`  
		Last Modified: Mon, 10 Nov 2025 21:46:13 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:fe57bbf3b4b827aae0e4282cacad352b1226be54efcf04e5be02de2c3dd7b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329903881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f696c03739404522ba0f32d0cb6dae41b45b254abb5311ad4f6e004b7a087458`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Mon, 10 Nov 2025 20:12:41 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:12:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:12:41 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:56d9ac38e76a44e89bc08ed485ad52f65d899438b382b7cf8d3c2d3fbbd6ad3f`  
		Last Modified: Tue, 04 Nov 2025 00:14:00 GMT  
		Size: 31.2 MB (31191667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f44620a9ce44addc699890962f84d258b45d9a5c4a9b634fd59cbbd2b58bf`  
		Last Modified: Mon, 10 Nov 2025 23:13:30 GMT  
		Size: 298.7 MB (298712214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1dd0ceebc57099e1718d2f4a3b8be152844e728f3951bc5ba6ea7cbbafeadd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bcacee06ed2c91f251a566b879ccc97ff0c1c78c8822e9e2e8113ea6222fee`

```dockerfile
```

-	Layers:
	-	`sha256:e32fe7db792e99daf16c65939bb3b6ed81af7f1c80dc1816a7bdb4a155104009`  
		Last Modified: Mon, 10 Nov 2025 21:46:17 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a999cc8dbf114584fccea436956bf5c934efae4fd20afc321ea7efbaaead34`  
		Last Modified: Mon, 10 Nov 2025 21:46:18 GMT  
		Size: 12.7 KB (12681 bytes)  
		MIME: application/vnd.in-toto+json
