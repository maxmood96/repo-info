## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:d447f1580140cc1557b50b2b723c23c7c85bac3193476af2990c33f1cc7d015f
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
$ docker pull rust@sha256:562d6f211888cbd784790e7fb47d3cea4b20480634543579297832b7fd1c25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6261cf21c8a87571e9f4b502375b16f30e624d67d46e199388cdf0bc36235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906e6ed35d183754f56330a654a033329ee5826a5608612dde75a12c80dfbda`  
		Last Modified: Thu, 02 May 2024 17:53:08 GMT  
		Size: 223.0 MB (222997945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e7b9c6cdb9dc891a721e37b31279d12f59a2aeaa33d3a50cd04c15ed9fdac0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a326d7714ebb85020a2b5bc3eb2f017a246b9349e259e29adf9cf787cd097`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cefbfd3006121cdf982e776f479a01d0119707b7d9103dd24cdb58f580975`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca2968425f2c6d21765305834771a5c51369246bdfafc5ca52300a944a9f50d`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:06c1a08af5dabc4454b1cc105c607d4d06c9b0814db93873ff926a1ee1ef7b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264467965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b9e3843b862fb3d9313d353d263101bf53a6b5d8b5e5fc90bf323760a9189`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904fd6bf6b41f2fa9b506f896ebdbe821cd028a693fdf7968eacbc7b23da79f`  
		Last Modified: Thu, 25 Apr 2024 00:13:15 GMT  
		Size: 241.5 MB (241522901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e89bf36198f7184854a7500fc86b2d9017d6dec89f9311e71ecc44493f5ea944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e0ecf007f0e2320b0b6564175d11a3d1f73d3402844e54236f518ce9eee78`

```dockerfile
```

-	Layers:
	-	`sha256:34f4a9c71e486a6edc1e06711c9c2d0e0a73aac8cc3987e71e5a681711ebaada`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa92b499139c82ddeb20b2d912bdeb136fcb250880b3abb0507ed48c61ef2b`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:56bb83c52ae48868648623c66047407de6700aa7067c73f17a1123ab93c64100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 MB (307968254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971b5786e21fc5bd76bb8a35c517b61ed1cd14e896275e14501c9be6c13c62ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8624caead6a91dc57f0ea5505a950601ca0c74bc2f7c1f71a63297c07cfbac77`  
		Last Modified: Thu, 25 Apr 2024 19:29:33 GMT  
		Size: 281.9 MB (281858424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:0d1fd1aad2268db32c64ff9e1a5b6db6797f268b35cf4c63dcecbba8454b1957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0fc0da4870351e89e5daa7dbcf6b5df57e7f0d5b2e19a55c22865f839adb57`

```dockerfile
```

-	Layers:
	-	`sha256:ace377fd1095994294fc743217a0772f26e399c599c8b6f8ce5a278246d27684`  
		Last Modified: Thu, 25 Apr 2024 19:29:27 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d1039b595eebee44a6e4e1aa73e549d348edad0425f7d0376ebfe76f53e125`  
		Last Modified: Thu, 25 Apr 2024 19:29:26 GMT  
		Size: 11.1 KB (11066 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:862f761b55bdfb9b687ccd73c39ea5db75ab570112ac0d7d9da5f5c5196dc67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268610066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12d3e0efa5e20f2dffb6cca638c9d030e51183e0ed6dea06200bb6fa61abb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:39 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Wed, 24 Apr 2024 03:39:40 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3981a552b28468ee69108184598097965a5265b74ad064e8e657f3897f599f3`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 240.6 MB (240615388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:4a7ce102abb3a846743437756ea063f781583ab5bea6f40c2612550634e10222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6026b631db1e909e1f420b7086445db95e1f00ef7bc7c365ad507c9a54fdb`

```dockerfile
```

-	Layers:
	-	`sha256:2e03fc3bfe125dba62e18faebb42c04d798624900a87a5dc953c3be75072510d`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e394e2a792e8d275adc332b5b935d4c9db65a83fe54fda94e7437645d5b02114`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json
