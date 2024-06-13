## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:ae43cf9419400b2b5e21dac22c8b4eb66b4d6b5f908a3ea089944830e615ebc3
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

### `rust:1-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:7b3f73793dc53185eb6e98d08d2aac92ffb933c7b657edd619346bd92449b00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250726811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3acc8a0b7f978cbdd440d6dd8d3abdbeafc07ea53a3e8607f33e00433f4c12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:37 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Thu, 13 Jun 2024 01:21:38 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad808676363ec41289ff19b83f12fab4369020384e821d201a7b40db06124f`  
		Last Modified: Thu, 13 Jun 2024 18:31:21 GMT  
		Size: 223.4 MB (223389108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:27b696ecf6c2c4c104a62b0c111c0f89a71eced18d34e26357df8fb07c5cada9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236ad93016a38cb1ac010968356a04c04d0c7892fe69d4f02886dff78df3f784`

```dockerfile
```

-	Layers:
	-	`sha256:7106d624bf4330a8f964549d9c6b87f7b792605d5cffaa68699b33a0a564fddc`  
		Last Modified: Thu, 13 Jun 2024 18:31:19 GMT  
		Size: 3.9 MB (3941692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66c7b36de1c1ad940085dae9b6bee1f59a2dc43babe0377744033b83145ed23`  
		Last Modified: Thu, 13 Jun 2024 18:31:18 GMT  
		Size: 11.1 KB (11106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:dabb28b2fe488a2d96aa1b391abd246aee270ca3408a5e3385c425f0c930d35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268702415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b60de3d6979c94712a29a20c74ed49ac0ba8febe024543cc4f40d60669ebf2a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:30a8958fe0d5b6c3e6d6c11772c14c4b85029786ca86968f09e078645df26b2c`  
		Last Modified: Tue, 14 May 2024 01:14:02 GMT  
		Size: 22.9 MB (22944934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c772c5837b4e05be9b62c948137fc69b215abf25a4a23d3c77cc3a80c68c52`  
		Last Modified: Tue, 14 May 2024 20:23:31 GMT  
		Size: 245.8 MB (245757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:418d00ea41133e76ad56706b0287ace3992082c70bf8722c70edd20ce8813bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aade7c9e7f4729594f77f695ca8f2702b7c9bb066feb222faf5a6af43f4d13`

```dockerfile
```

-	Layers:
	-	`sha256:004e3080c92ab1fcd559bac44a3fd7791669b7326e23fc4ad70a2be51898b8ae`  
		Last Modified: Tue, 14 May 2024 20:23:15 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c736168393cd678674690cea8ddd02caeecc124da79e5eb9fbcf01bb9d32cf`  
		Last Modified: Tue, 14 May 2024 20:23:15 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec9113111024feeab51f52d2e365feabaf120c52aa72b11ebf4e91c730e3ac4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312575219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aa3003d52be115788a3dc5b765040bd97bacfe3881a87097ea09da885830f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fdebbfc3fa654bdad9931a57e4437c42fe9f231e971b5693122f9bee0a787d`  
		Last Modified: Tue, 14 May 2024 23:41:12 GMT  
		Size: 286.5 MB (286466113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:989c434463efbc46af0d0aac872826413897ccd2814f9fc2b0ee7903977007d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6308fafd775e4ef52e5e4b904823a5d6deb715c86fa3cd698a785763f04072e0`

```dockerfile
```

-	Layers:
	-	`sha256:04e6d7f2f8e500fa766de9daae779a92cc3279b6697beb5d15fd2c239b96486a`  
		Last Modified: Tue, 14 May 2024 23:41:04 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567799f7d052a7bb519176a373c5fd95d794ed9db481c6c35fb29e467c0d72f0`  
		Last Modified: Tue, 14 May 2024 23:41:03 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:ab63458d36b7417fe772108b2f8f7bd76df28143c9896799c3ce5811b801e31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269746131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46edf89a0f4dfe0c00e9e34f94c0c0b5966e853564129ff7c6a5d79a58f4e67f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:36 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Thu, 13 Jun 2024 00:39:37 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2218f37b985cd028f80e5731cdbba0e7a189cbb5f229e6de1b6531896118f9e3`  
		Last Modified: Thu, 13 Jun 2024 18:34:40 GMT  
		Size: 241.8 MB (241751491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:5743c99c6bbfc9500911c8a653fd7656869df4cd7753b5e8348abe806432754d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb7a646a784f589b23891c32e435773593063a42ffcc67d9717dfadf15f461f`

```dockerfile
```

-	Layers:
	-	`sha256:02a3289a063961ba4068170c770d753d695e034b197d6370383b9b2e55efbdfb`  
		Last Modified: Thu, 13 Jun 2024 18:34:34 GMT  
		Size: 3.9 MB (3948317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b7d1812827d0a7e7f9538a873848fef44b5049a8845b4e5f094497e864f2c96`  
		Last Modified: Thu, 13 Jun 2024 18:34:35 GMT  
		Size: 11.1 KB (11077 bytes)  
		MIME: application/vnd.in-toto+json
