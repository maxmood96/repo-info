## `rust:1-bullseye`

```console
$ docker pull rust@sha256:21d112adb6ab370d39eef8f861f10b42342419b9569e7a05dac15e19eb65a3b4
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

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:65136b30fc6b10112cbae63a868da085a878679a80d562272e485ecaaad3276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.9 MB (536895700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1180171a45255830dd6c52f737fc6e25d6468de8a20abb315a6280fbd26435`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:40:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:40:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:40:56 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816526a6d4acf81b392ec5a1e6d8d402fbc4bf0460323c5ad45b376b247ca6fc`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 15.8 MB (15790805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3cf50c221acb61e259a7ecd20caf425597eca7d93e329dde2640ca7ec8aaf4`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 54.7 MB (54742897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a160e6d2c8242d5f49a2c1be818ab0f47647e5cc5cf1fcb068e6618846d778`  
		Last Modified: Wed, 24 Jun 2026 03:18:13 GMT  
		Size: 197.3 MB (197335039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143375a08243397d86927c703a00ab22a648e2f813240e1e05719cb7383c77a0`  
		Last Modified: Tue, 30 Jun 2026 23:41:41 GMT  
		Size: 215.3 MB (215253950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ec8ceb17da7bf86bcdcbbbfe3689fcc0d7a15d4021dba8d08751944a0e8a30f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9716a5e3356553c446c08a476c3f841033958cdcd1856fa5845d53a0d93cb619`

```dockerfile
```

-	Layers:
	-	`sha256:5e9c93ccb0be10a5c5b0446ac035ce53cd7fd7d681d35f7778896bece0bfea8a`  
		Last Modified: Tue, 30 Jun 2026 23:41:36 GMT  
		Size: 15.5 MB (15473464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ac5232581b181939c4054932b7451c284e52403ab6b3d3d3311594acb4ec36`  
		Last Modified: Tue, 30 Jun 2026 23:41:35 GMT  
		Size: 12.5 KB (12503 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:95a74f9adefda719bd334b1a528a3a43512bead1809e7bc2c5a7490a2db1cf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540239546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6775eef0b711785686fd04abcef8569671f0d64ca4d61f1d74c7df3de5aaaa4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:34:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:34:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fc5ae1e57bd12fc3393aea9c4c883b87d2ec58e18ce0892f8effba71fbfcd039`  
		Last Modified: Wed, 24 Jun 2026 00:28:02 GMT  
		Size: 49.1 MB (49064073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f5593b138af5d5b60d8e82c822aa52fd74f6a603db24886e0573d60561397`  
		Last Modified: Wed, 24 Jun 2026 02:23:28 GMT  
		Size: 14.9 MB (14905363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4cfcfd51cd63cbc0a86a0ed17f661e5157a3b24f24a750cdb7ac4191f84c2`  
		Last Modified: Wed, 24 Jun 2026 03:55:06 GMT  
		Size: 50.7 MB (50659165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7e6cd4f6193c57c8019ecd8089fc02e4912acb7efee4fe62122766c0d5356`  
		Last Modified: Wed, 24 Jun 2026 04:18:24 GMT  
		Size: 167.8 MB (167779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ccb2c5532e8317abd9d28cc20cee6c76b6945b86842364b5d9db45ffc39d09`  
		Last Modified: Tue, 30 Jun 2026 23:34:59 GMT  
		Size: 257.8 MB (257831625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9c6e754615103c37abf3e54d5a8a7771886a0f4c7ae2595c087222b25ea1bb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15285391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9272eb6c240a0ac0f31145e7d84c3676a2f6290d1a03894af68c11173223d6`

```dockerfile
```

-	Layers:
	-	`sha256:c274dc1c21e1b306c9e99683912f75107adcd16297875963418f997f7178ee29`  
		Last Modified: Tue, 30 Jun 2026 23:34:54 GMT  
		Size: 15.3 MB (15272808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf6c002a70180b99a53a683043b9e0abb745f6cb24d7234e8ef597d4906963c`  
		Last Modified: Tue, 30 Jun 2026 23:34:53 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69e444ec65a82386d041a4a3d15e47a797967b90ae24aa342bd8a3600dd9e244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 MB (493348034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9004b62c7b6149259e3eb6b2c69f4f9f7837a0aa57865d5dd32bcb4a9dac21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:40 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:38:40 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:38:40 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf305d6ad7bad47ee0696c3db8b8fed8e9c2a42c53b57d047f8ab32f5d9b546`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 15.8 MB (15774954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f37219bba62c0b4908476dc3cf7f0f98f1c87e8908c188797b1dc1f610c77`  
		Last Modified: Wed, 24 Jun 2026 02:35:29 GMT  
		Size: 54.9 MB (54879567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e939dc6537087193b54cb28550f30706346c9eb7faf3f1da018845a5675ef09`  
		Last Modified: Wed, 24 Jun 2026 03:17:29 GMT  
		Size: 190.2 MB (190229454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a0e470da3354fabe932b34f5b265cfccfecd385c7de2d3e80cf8af7a4fc0d5`  
		Last Modified: Tue, 30 Jun 2026 23:39:20 GMT  
		Size: 180.2 MB (180206840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3a16b6fa6d7f7326f84132917f56208b2dd93e8d8d72ea4ab8d5b940a50b1c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce822070b5746c7a4e1adb31bd15b7fe20e217746af6afe90da484d1d6cfec`

```dockerfile
```

-	Layers:
	-	`sha256:6fac9f294c13891db25cd8d803dae3da587351f89101ad0af1b4944336c3966d`  
		Last Modified: Tue, 30 Jun 2026 23:39:16 GMT  
		Size: 15.5 MB (15475435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3899c7202655db8c83a23541e4edd239746c728f1433ba296f6e6e3c407f982d`  
		Last Modified: Tue, 30 Jun 2026 23:39:15 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e853e2725695c8048a8b138db56e64d1b0da5843e4b94f24a986c39d1147e875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.8 MB (568772449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad9866b38bd033f3577434311d7d2c79341519729e55b13fdd0ffb0ce8171cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:34:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:34:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:34:09 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:508ffc251196056212d40e318af0b7425af79fd3069a3f9ab15fd6220917ec75`  
		Last Modified: Wed, 24 Jun 2026 00:28:09 GMT  
		Size: 54.7 MB (54712884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f059b391cd2cd82464a697d38282bb9c5437ac5b83e7b92cde4d9a0644a137f5`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 16.3 MB (16295718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18472033acd6c573e081fc2a3814994e7ab4e4ca2f812052bd6f7c4b0286c5cd`  
		Last Modified: Wed, 24 Jun 2026 02:35:09 GMT  
		Size: 56.0 MB (56047273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6beec4254dd6d9d54bec111217bc6634d6c5d7b5ceaa6029ae996278552695`  
		Last Modified: Wed, 24 Jun 2026 03:18:33 GMT  
		Size: 200.2 MB (200244154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e703af94c4533fc68c2687f9c5ff0a94b0c1df2ca33aebc5f9cba7b40d6911`  
		Last Modified: Tue, 30 Jun 2026 23:34:54 GMT  
		Size: 241.5 MB (241472420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bc00ae08e242feb6b1551177815e2bbe26937b6f7549f4316e9bc85d1f07e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357caaa60d17674ced144726abb2b757649ba6bde0bbeda1288045d6856f5971`

```dockerfile
```

-	Layers:
	-	`sha256:27e3fea3fa845f1a2634be032b6332e7f1ece4da6d83470bc9aa8ab40a5a2438`  
		Last Modified: Tue, 30 Jun 2026 23:34:49 GMT  
		Size: 15.5 MB (15460166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb2c2c23ffc6732ec924cddb79e6969a864a88c140fa765530a75f50e37cac25`  
		Last Modified: Tue, 30 Jun 2026 23:34:48 GMT  
		Size: 12.5 KB (12470 bytes)  
		MIME: application/vnd.in-toto+json
