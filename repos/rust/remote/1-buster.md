## `rust:1-buster`

```console
$ docker pull rust@sha256:3465ee3de385bc9b0d697da7365015fb38bd2811fa753694eaf13626c954531a
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

### `rust:1-buster` - linux; amd64

```console
$ docker pull rust@sha256:201bf72882b259b5aefda3d24a3f2971f2ff093f6f0a392ce8f47f102819a239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.1 MB (490072016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dde130826010179eb37d57d937cfa090f4989eb0f58e05a42449d8764a07b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:28 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 13 Jun 2024 01:21:29 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:43:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:44:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab8bed435ee0e35413bb45d14dae2283dc0841644d881be35089debdc88cc3`  
		Last Modified: Thu, 13 Jun 2024 03:51:25 GMT  
		Size: 17.6 MB (17586423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a567eb2264b60aa779a5bc8f8f4dc7a6d3e1e01d8f5d1bcd039ed444d91a408`  
		Last Modified: Thu, 13 Jun 2024 03:51:40 GMT  
		Size: 51.9 MB (51895667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be81a73cfb7b45f4634965206adaa318a889f15cff6ced0ffd70f7c2d851fe4`  
		Last Modified: Thu, 13 Jun 2024 03:52:10 GMT  
		Size: 192.0 MB (191957999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48778a0ff99eb107bd3f556264ec1a21e8e8ade98c04c18df217a05245f72b92`  
		Last Modified: Thu, 13 Jun 2024 18:31:31 GMT  
		Size: 178.0 MB (177974554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:307ddd4f1df3f54feca7e34cc85059b32ad4cce097c2466785dc6e1f5e9edef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15977901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b4e2786360bd244e3101899ddee674d36a9e13992c7566afc4058d649a4b6c`

```dockerfile
```

-	Layers:
	-	`sha256:ac6207534d62d27721c2cc0f6f0ebb452ad3b9d1b456fcdde1ac3ad9e49dbe5b`  
		Last Modified: Thu, 13 Jun 2024 18:31:27 GMT  
		Size: 16.0 MB (15966857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4075aa5e1c7696e17dfa2bbc0a7d3e008e2295c098e34ab651a7a4c633b85ce3`  
		Last Modified: Thu, 13 Jun 2024 18:31:26 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:08c939ed1c12c799be5dcb6d9b5c3378af3b98f191f2705e8e1341bc68316e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490747250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e225e7d6031cf19d5054ee3cd34014cd899fd00d175abc4dd8547a57e07e12d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66d6e1b7bddcb1c893c2c3e9b1ac8f5fca7c047037ed836079c97c9a917cd989`  
		Last Modified: Tue, 14 May 2024 01:13:47 GMT  
		Size: 46.1 MB (46129793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e36c6c43e23d017283e609c78ad3425681f38a7cec50832f329aebf9f45a45`  
		Last Modified: Tue, 14 May 2024 01:49:06 GMT  
		Size: 16.2 MB (16217024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d070dbdc44447a3c019b1076d14827afec1e3d9f53f0941c341dde2f5b674`  
		Last Modified: Tue, 14 May 2024 01:49:23 GMT  
		Size: 47.4 MB (47410306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeab1a68b064abb317c5afc7a68fdc8b46b5c9f37a1fad3e3d9664777a761c11`  
		Last Modified: Tue, 14 May 2024 01:49:55 GMT  
		Size: 168.2 MB (168170028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f856bba6b981a76ad9e94b02ff1f9dd00b9e9736276cc57695e475463e4fe0`  
		Last Modified: Wed, 15 May 2024 07:43:17 GMT  
		Size: 212.8 MB (212820099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:43d8a16694d8059e2903f311f4c885149b31f9221a7827ae928cc5c5983dc0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7225498dc742a31a154ce9907b180bfb2994ee28e08ee04f44b7d96a5b91b7c`

```dockerfile
```

-	Layers:
	-	`sha256:16f8e88da7537fdeb64820a1f045683a08882a3861225935037cee1e9c62cc04`  
		Last Modified: Wed, 15 May 2024 07:43:12 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b521e68a2be54b6133cfe6a0504c68d8bebcc77375e2d49508b7e810b35bf0bd`  
		Last Modified: Wed, 15 May 2024 07:43:11 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d77c4e102dc72ccd4149cf0deaa878e6857c03fae051a5d64e19e0fc6cf97008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548926316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5da9b6166c1c938d026317bd5ad176748fe6aff0e50087360263df8fe69f25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e540eb6c9fa042a5d3f1166ea6b4d3806d751dcc600baff113c7e2b711719d`  
		Last Modified: Tue, 14 May 2024 01:54:42 GMT  
		Size: 17.5 MB (17456998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334249e7f4554ad45c3998bd6a23aa8d7ecc535422903784fb251e6345d36f9a`  
		Last Modified: Tue, 14 May 2024 01:54:57 GMT  
		Size: 52.2 MB (52230498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b2124bd151541dda5ef935a2883293321b124587270f4c0c28495c25a1ca4`  
		Last Modified: Tue, 14 May 2024 01:55:22 GMT  
		Size: 183.5 MB (183534368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465e757173638fc73483fe11c995402273625b6785f795a0e0353051241bbe59`  
		Last Modified: Wed, 15 May 2024 14:39:45 GMT  
		Size: 246.3 MB (246251358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:99316a0c39c17d4fe415cb67b3cee5a9ea1bb80ac74194429aad44af9722a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15968723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04df67f0b91dd4c1a9cf555db762d960aa1d800863c71c736341e4149c07ae`

```dockerfile
```

-	Layers:
	-	`sha256:a48a2ce1409c02bc40bd40210a256488dd7703bcf2882cfc30d491c400cec5c2`  
		Last Modified: Wed, 15 May 2024 14:39:40 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f727f392438b39c18d7c9371cb9f860b23ecfd6de9fc16a7e4f7d2c17731a4b`  
		Last Modified: Wed, 15 May 2024 14:39:39 GMT  
		Size: 11.0 KB (11005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; 386

```console
$ docker pull rust@sha256:800620a0760169894985b9949ac9ff0375059293af2682d945a1db95398bec1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.2 MB (513240488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835edf15ab336355ad515cce97130910e6668938667a90ae39820d5be446e581`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40f693ac8434364b7489c467dd31e0263396e4e0f3102204854d8530f11116f`  
		Last Modified: Thu, 13 Jun 2024 01:22:28 GMT  
		Size: 198.5 MB (198491652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f45e3c5d864cfdf759d756c09ca047d13010c95ac775b1432803fc5bb717f`  
		Last Modified: Thu, 13 Jun 2024 18:31:58 GMT  
		Size: 191.7 MB (191738925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:c26abe0b2e1a56010b5779945f7593ae0abe2c3a3e100c2ccca4f5aabb731d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15983453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d074df3c393643b23584093951422969a34987c8f0a39eafb57e06b659b13b40`

```dockerfile
```

-	Layers:
	-	`sha256:a97c7da13d9cb654e9b18a14da19e8d713383ba2c0a87fa67bfa05387e12bc25`  
		Last Modified: Thu, 13 Jun 2024 18:31:54 GMT  
		Size: 16.0 MB (15972438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e631c7ca79396bb2212ddca8fefb1a24e3ffc7dbd1b1257a5f975de21fb320`  
		Last Modified: Thu, 13 Jun 2024 18:31:54 GMT  
		Size: 11.0 KB (11015 bytes)  
		MIME: application/vnd.in-toto+json
