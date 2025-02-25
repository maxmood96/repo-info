## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:a7aedef4b037568ac7050b33518f1ae432e3c4c04df8386fbb700b70b414feb6
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
$ docker pull rust@sha256:7663fabd907a525b6d32ba13eedc297fddffa97909091673a28ae2f179b5e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282418225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888e5a425c1bdeaab6adab7f2946f6e6d3f8d6bd29e5d01ea9931a47b0013dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Feb 2025 23:42:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 23:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Feb 2025 23:42:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 19 Feb 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edabe4fa0576778821602b6c7b3d1bb43cbea035bafa079013083181e76789f`  
		Last Modified: Tue, 25 Feb 2025 02:14:23 GMT  
		Size: 252.2 MB (252164295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e71ea89d10717e348fc9850d743cbd3371afed20edf72204248f3227d6ae64a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da3625c3ca9003d7e50ce8b4cc492258bdd80f735262ff72152de9a3df247e6`

```dockerfile
```

-	Layers:
	-	`sha256:04295c8e38230ac26ff6acf711117d9d0a95c6a767c3e29bf757b137f5d058ad`  
		Last Modified: Tue, 25 Feb 2025 02:14:20 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c80a8e84d69543b38c3e25b3560f132258ce1cdf375261ff19ac2a93280b565`  
		Last Modified: Tue, 25 Feb 2025 02:14:20 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a033cc43ee88fd7f60e525ff894c0f930b391a08610d0cf01f98a9fb8b8506f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297538465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b067b9a8a034929561a5907c74999b4179a340ff64518d28f622e5bbbd8b0ca4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 23:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Feb 2025 23:42:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 19 Feb 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46c0a06f283026539bfa5a7b5d89e1609a237590b73f7b572483e326c6b759`  
		Last Modified: Thu, 20 Feb 2025 23:33:07 GMT  
		Size: 272.0 MB (272004582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a722afbe24d8de3a0c5843336804d877e30aaabadde3bed277aa2d5e8c0808fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479cd6445f606f25bf85127f82b2177fec095de4c4d8b93f63eccae34fb943b0`

```dockerfile
```

-	Layers:
	-	`sha256:d1d93ccdbad056e93b16e00c386af0d0e0a2999ea79e7df6e907166414d37c70`  
		Last Modified: Thu, 20 Feb 2025 23:33:01 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c284d9fbc37f3519b69c046cff9a3f9f566ee46d0f547cfcfc3dd56907ede88`  
		Last Modified: Thu, 20 Feb 2025 23:33:00 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:47bca76cf69f9568f7542554b3c6fe99ac902966552c0ebce4eb590e4923d6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341424639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d9202fb7ea97bca277f5e180812e4334a6c33da45fa36374b3b053c042f128`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Feb 2025 23:42:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 23:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Feb 2025 23:42:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 19 Feb 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45551ee93cf48f818077bb7bd4941e1e0d28c759f8b9673aca5ea25848235af4`  
		Last Modified: Tue, 25 Feb 2025 10:28:45 GMT  
		Size: 312.7 MB (312678652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c74bdd32bda619937e0e974d930393c5ae543f5a22cf745be74d25f7a0a3cc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae3797abcb90aafd7932c84db95bb0bc892cf4434e3bfa6b46da4298c47768c`

```dockerfile
```

-	Layers:
	-	`sha256:6e5809e0ffb766af62cf05489a7fbbba83d70ad5b4d7f1dab624f1e444658df7`  
		Last Modified: Tue, 25 Feb 2025 10:28:34 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2406783a2c77508739c73dde065d821bab1c541294f733a524a6ccb346e4e69`  
		Last Modified: Tue, 25 Feb 2025 10:28:34 GMT  
		Size: 11.5 KB (11459 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c4d4881e03ca7bb46ee57e4f6ac3f539e84573af57eec6bf56f0bf519393ddfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301491364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4357a6c7285a4700fda2a6709cff48c9d7d2f1778530033e683eaa7761e049bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Feb 2025 23:42:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 23:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Feb 2025 23:42:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 19 Feb 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6d8ed1ab678686fa244a7346a1e24ff94c9d55f075fbe497bc9772a9d9c850`  
		Last Modified: Tue, 25 Feb 2025 02:29:16 GMT  
		Size: 270.3 MB (270310937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b4c9ca33c7ffcdcc849e4bf345eb8fecf3eaaa0a299c63f353f9975912c0b043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15636fb1a079077ce56d9d36f37e3d0444768d6f6f6ac9ac34dc48978cf37395`

```dockerfile
```

-	Layers:
	-	`sha256:c19cef3067bfba90665647a461c52c653e2930294fe4ac236846b71a353fadb2`  
		Last Modified: Tue, 25 Feb 2025 02:29:10 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d56793d8ba2373426435ba4de1f1c40de6b3b02196f3f978c672148033beb2`  
		Last Modified: Tue, 25 Feb 2025 02:29:10 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json
