## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:a9bd605cd31827c6c20d145d7ba0c0c5ec66827ad26894a8f07d5575f3110c1d
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
$ docker pull rust@sha256:73683c9b1073e326871420038bda0caa79018735e1596ac92997f93b786a641f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305635052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c4c0d7eefe9ab7349159c62ca61f2d6665b17459f165b91d2f5640395e9c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:53:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 19 May 2026 23:53:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Tue, 19 May 2026 23:53:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f008a95827993e77a96388afd01cc2ed69e5743536608f6c5f3d0bef7a38bede`  
		Last Modified: Tue, 19 May 2026 23:54:01 GMT  
		Size: 275.4 MB (275377454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:88ae1f2c5267a23921b5a436a2f4fc12ec883440b538d634a613192e55f17946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36b24e248c185dce67db6ce23b41f38eb2b3efa435bff7d75a7d30c8d83b348`

```dockerfile
```

-	Layers:
	-	`sha256:68f4fdccfbdd3c8ff89f608799ba041514514250059cee1aea5bf68f63f509b9`  
		Last Modified: Tue, 19 May 2026 23:53:55 GMT  
		Size: 4.3 MB (4312022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9114765632834f05f8aa0671a5e05ef70362c4c8855deb234783ab8519e4f8`  
		Last Modified: Tue, 19 May 2026 23:53:55 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f497315c426a472e6ebbd0cc728057b11d06fa99d13cf8b3db4785bded85c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324738005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb4dcaf2ee0e3dbabf98068aa01b697a76f4dddcbaabdd2b5eb3d0e02980d64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 01:11:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 20 May 2026 01:11:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Wed, 20 May 2026 01:11:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e995741dd34535ca4c7e788f07a2e7c5679f9f18d5daa5786aefc6c96e0cc6`  
		Last Modified: Wed, 20 May 2026 01:12:20 GMT  
		Size: 299.2 MB (299187067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:073c8502980d7b84aa7df5b6eec024284dd791de91e7fbea1975c1383422b579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657a40c0710e41868ce51148c8fb91669cd7bfcca04b3001eaa578db14e70934`

```dockerfile
```

-	Layers:
	-	`sha256:8ea5defa1463e4fb8e1fb5591c324ea67c3c8e9f9a1dc8a5ca9ec00e127230cf`  
		Last Modified: Wed, 20 May 2026 01:12:14 GMT  
		Size: 4.1 MB (4120015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d58d594719b4164fb9bf0b1631fd85d6d5f96d8ccc546be3346837c1253e448`  
		Last Modified: Wed, 20 May 2026 01:12:14 GMT  
		Size: 12.8 KB (12793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:67ab4696009632b36088394197ee4bb40f554784b68d00a20106e53809295252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263998233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e74e4864bae0ff87c4690818aa0242cbe1977ae3cd403a1a798222af55b1f22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:00:10 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 20 May 2026 00:00:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Wed, 20 May 2026 00:00:10 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d17220681939a831d60330081f73f93ca1a607710d97719bd3484bd8e83148e`  
		Last Modified: Wed, 20 May 2026 00:00:50 GMT  
		Size: 235.3 MB (235255261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:028abfcf8cec7d41e6284eb05da17e7c53e7dd9f7a7d2556a7931de18a1c00ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4321229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b93bd87bd257f5f5d1356bd047ce102a11a03a76f7ea65c7351ef8bcf6ff0`

```dockerfile
```

-	Layers:
	-	`sha256:2f78a3a9a9b6feb665b93531c0fffc592b8a026772e4f415327a6700ac071504`  
		Last Modified: Wed, 20 May 2026 00:00:44 GMT  
		Size: 4.3 MB (4308411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d38ce99530542f842decb7cc2a293256b67c0da721a6d5ba1c3f2388ff4827`  
		Last Modified: Wed, 20 May 2026 00:00:40 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:bef9da5d2811c52a9b6aff6b4367eb8b65e80ef71f4b67f8435300c9f77a5f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.7 MB (332722373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346d6858f536f847be727bf64f93a7f5b549cb1ded3461d7532cd77299f6cf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:54:53 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 19 May 2026 23:54:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.95.0
# Tue, 19 May 2026 23:54:53 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2f6471dabb4ec95bed651099aaba5ff48a4c6332742cc6af6c957b880b8a6aff`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 31.2 MB (31192759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a1e32c8f1d2d3b08641483df5427e0046de1918e14529874c2414e87d6fe19`  
		Last Modified: Tue, 19 May 2026 23:55:35 GMT  
		Size: 301.5 MB (301529614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6312be685ae3a64ea4fb42a5376277ffd129d679d740b9547ef37ca84abcfc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64af89fbbb1a7af51485d255a81da75fb3e926386bc2c483f6d964f5a4d5823a`

```dockerfile
```

-	Layers:
	-	`sha256:308d7b8baf11f4bda2174abecd1eb0aedbed988fafc43a7704bd7bde958ad7fc`  
		Last Modified: Tue, 19 May 2026 23:55:29 GMT  
		Size: 4.3 MB (4301764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247d6fbe9fe4890b22f633aa48a450f98a48e6924cbffae2ba12d52584396ef8`  
		Last Modified: Tue, 19 May 2026 23:55:29 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json
