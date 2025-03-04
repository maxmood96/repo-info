## `rust:bullseye`

```console
$ docker pull rust@sha256:6cb2cf341137cabc58d05942ca17e31c2c973ee50e2dac8bef4c0edc4e9e21ac
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

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:4774472306a1c334734103f7bf6231ad1370d4f71c2ae394fe8978afac5b2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514821415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63309be2c0345cac77307aa173b9782aa5a84f553951abd498d16f5c04a4fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451f55144f64f697f2945598b3a000bbac10e699d6068b7d6e63f9aa2b7f3b5`  
		Last Modified: Tue, 25 Feb 2025 04:17:48 GMT  
		Size: 197.1 MB (197074397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c39801b95216b4260c69cafb56f78679aec6c847d1e3d1afc1de560c4cd5e9`  
		Last Modified: Mon, 03 Mar 2025 21:14:42 GMT  
		Size: 193.7 MB (193695108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2ee0d74ac110bd1a17d8332af3912202fbe343a4a38370a9db6bc9fa364b9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd28e732df28539d58b7d7f26dacd50370d93acc3d43ba5ae570174138f6aec`

```dockerfile
```

-	Layers:
	-	`sha256:b0537ca4f5998de091de7aadced2002bc586c005466354e27181079037c37733`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15073413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b971a0322980ccb6d5b56d28083ac175e1bd00757315708f1421f1797d01f`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ac2d9029c9950551413e86bd26d8ad86f61590dd45bb4cd2da0a4b001432ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512134009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5029ae4b22101f3709c37ae1b0f1483b2f9ff3209787eb6e49ad590cad55da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016ff31b139f4cc1ac2b37027c3a5c553771198a19e3563f9ebcc51e15f4999`  
		Last Modified: Mon, 03 Mar 2025 21:23:09 GMT  
		Size: 230.3 MB (230265301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bd6feae8faa96fd3e378eaa561081d1edabb91e202219f3fa32d7468381c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7808076946af42d45e2924dc9a57c449d7f6c9539ed7801a920d87def0c75`

```dockerfile
```

-	Layers:
	-	`sha256:afaa1ab536f6764953fbf3d43692672f51fc56aa085586bfb78431ead85f5d36`  
		Last Modified: Mon, 03 Mar 2025 21:23:04 GMT  
		Size: 14.9 MB (14874204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d11f72eaf746d2a6aa73bdc233abd05555878019f6832b3a21234f539567442`  
		Last Modified: Mon, 03 Mar 2025 21:23:03 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5d6e25360f6d028455c8b643f8f53d7c4efbc0064b23759608b61ad6a3adc223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.4 MB (571431917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371eb80ca3e9f7fe5098765803837081bef8ff5751aecccc695e544f321dec2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bd61bef017e8e3b4e6f403c074fa47f738d2ac56d92eb50f50fff5dc8bd03`  
		Last Modified: Tue, 25 Feb 2025 15:23:19 GMT  
		Size: 190.0 MB (189986146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0073060607bc719b0aa94e147a0b6b03b6aefcd068fff7a78b8f947eecf9d5`  
		Last Modified: Mon, 03 Mar 2025 21:36:29 GMT  
		Size: 258.8 MB (258797560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7c24d055c4c4a49c2b849357293da9e9e2988140bdd4d982de7271f0e3143c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebf36916e6fb93d90caf00958262c0c8b9c86735cb8958a061bbc281f3fd85`

```dockerfile
```

-	Layers:
	-	`sha256:493bc9dc75ddde0e35de2091d2eac442ce52714aa89a6f684f07608dbbcc2dea`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 15.1 MB (15075673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44037f8c5cd51ccebdbaed303063aa1b879764d15ae47c490d35c0fe101c959f`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:d96bbc13b6e3f5741b38e2d39e57c378073d01c5cf0f2e18023d0bf7c730098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.6 MB (537592438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fb3dfd29980bf4e4cf1a785df10f73d2a9093d02a06e3fb1789e2e0670f645`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883849d920b1b05e06838787b545a094134ce0719a6b7b9f208333a79ce9a242`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:16c416c5f5c143b8d3d0444b211b06b0f4ce71c2d44bab44374d6c8e196621f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baa792f584e43afed942f1cb227670cfbb389df99f48d8914c3676ae81592e`

```dockerfile
```

-	Layers:
	-	`sha256:6a66d8cce735ea8c5513f850111cf3a06be5855d644d3836537665c230246349`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15060440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f74ec7a17331b1624aac92a9d8ebad6de4e7c0902f293d6a7495e63d14e456`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json
