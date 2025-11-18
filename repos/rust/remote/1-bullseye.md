## `rust:1-bullseye`

```console
$ docker pull rust@sha256:9a8a7734bfc0251be5b9ae5533a81fe75936ab3d415ea9bcfd94f11c9757f49e
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
$ docker pull rust@sha256:d7ebd65d544a3d237537d49e34f984d7a8016578368f911a972466a097def2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534822478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d4dd0d8c3f72f8c2d2169ab1a20df0fc6d5ff94b19fdef6d7a2e8766778ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:42:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 20:11:50 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:11:50 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:11:50 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba74ac44652a153d2c2058f766703586a059b3775323934bb7195c47e2f7244`  
		Last Modified: Tue, 04 Nov 2025 00:28:27 GMT  
		Size: 15.8 MB (15764072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e217875226b0af2272d40b4ff7389d8caf7d0b8c528152c0daa8b5716a1398`  
		Last Modified: Tue, 04 Nov 2025 04:14:47 GMT  
		Size: 54.8 MB (54755157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4510c73592efcec58fa860cef6afcaaad48b6da2a7a238940d194f2a5b305d99`  
		Last Modified: Tue, 04 Nov 2025 11:00:15 GMT  
		Size: 197.2 MB (197204878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f543eb75955b8e739431d756cf2753e68a6a1ec8909f997fa46cbfe23f6a4f5`  
		Last Modified: Mon, 10 Nov 2025 21:17:24 GMT  
		Size: 213.3 MB (213341677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:64f2750c47ec3f0de1ff0d4f80fe46c8601da1fd8949391abfd58041dc616cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15476554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24f250b985485b1192edd55851185bd6c88b6008410f9c410aaaa03b2c5944f`

```dockerfile
```

-	Layers:
	-	`sha256:9a6ec5d25f3d21643955d446a340f7df86fef54d34aa23694b14814684941a04`  
		Last Modified: Mon, 10 Nov 2025 21:45:26 GMT  
		Size: 15.5 MB (15464051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fcb1945d5860c7f5c17c4466bed5b9470c54c4ad3731bc593814452209d267f`  
		Last Modified: Mon, 10 Nov 2025 21:45:27 GMT  
		Size: 12.5 KB (12503 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f591a2c22291c6749997e3c2bd7b7e6551342dbedc388317411ac39e93e0077c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.5 MB (540528570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a98b06c6a13cbef8c7f9907a46d7ff526f2d94f2a12d173233a0c7b36a9748f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:38:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 08:38:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 08:38:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2280342788a66a44d1f2e4bd1eaf8389d9bef9428e09fa0ae948652bfaeee4b8`  
		Last Modified: Tue, 18 Nov 2025 03:58:13 GMT  
		Size: 14.9 MB (14879454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f566f1ab80bd353b42ed837b52fe4ec496dfff10630b53797d35c9eb72bc27`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 50.6 MB (50629469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae163b8147549b72151eb921eaef5a03a6a925fe675fbadbf871e2bfc1097c32`  
		Last Modified: Tue, 18 Nov 2025 07:35:47 GMT  
		Size: 168.0 MB (167975659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68672e88a9126f706003fb1bca6b562dadbd4fd71185b16fcc2a632b4a9ed3eb`  
		Last Modified: Tue, 18 Nov 2025 11:32:15 GMT  
		Size: 258.0 MB (257997623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:744c96acf68eca61c7c19717665b39a5b1bbf5cafb3ddd9976e9aeed8ed4f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd022d1ffde0ddd646cb6c2bb1055a21f6435a33583cf7ba337842215be019e7`

```dockerfile
```

-	Layers:
	-	`sha256:fc4f373d5b28145bf12e5d69be010005b9143b4ae09505fc0a41ab4898dc814d`  
		Last Modified: Tue, 18 Nov 2025 09:45:46 GMT  
		Size: 15.3 MB (15263395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104c34af2460eae521131b27ced8556535b7b3e9f3c218c36cd749ed1d98fc00`  
		Last Modified: Tue, 18 Nov 2025 09:45:46 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c041cb1390f83e168820820181842e9d1e1023b4b11d88d940999e2e9fc45ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493232819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd31705f566afa9f82b59022ffcaa4baeea7a2d327bfd955c0afd456c406985f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:20:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 20:16:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 10 Nov 2025 20:16:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Mon, 10 Nov 2025 20:16:02 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4de5de87e4df8d0116d41cc30ea033d913f47280433132cdf3c66653327716`  
		Last Modified: Tue, 04 Nov 2025 00:30:31 GMT  
		Size: 15.7 MB (15749511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b5305a450275a04f32f7333d98eb8edca9aa808f9904a4e0eb28b3cf08b52`  
		Last Modified: Tue, 04 Nov 2025 01:29:57 GMT  
		Size: 54.9 MB (54866573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfc142fa91493c8fc5a336bf0d0ff412766ba3d6cbd3ae9c6cd9c9969abc19`  
		Last Modified: Tue, 04 Nov 2025 03:15:38 GMT  
		Size: 190.1 MB (190102698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a14ea804ec52b8bd09e72573e92d1d3159378959c805ebd0b8c5f612d66330`  
		Last Modified: Mon, 10 Nov 2025 22:48:16 GMT  
		Size: 180.3 MB (180256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4dc1ddd6d2265f3f8863f826750cb7fe92d7dcebc81025de51ffa7eaee9df7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40383be996378d85c957d50c26ff9b02ee2b3e1bb2b525fc95e526d1447b7924`

```dockerfile
```

-	Layers:
	-	`sha256:ce36a6a1bcc5c9ee5d486f6ea343562cb326a4754096019ff5654a47572011f4`  
		Last Modified: Mon, 10 Nov 2025 21:45:54 GMT  
		Size: 15.5 MB (15466022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95bf71027297bf930ced83e791b49788f8fe4482b50545caf61efde69ca473a`  
		Last Modified: Mon, 10 Nov 2025 21:45:55 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:cdcd527145b3d3ff25d5de6e08774357b73466eee14d2da63c44d90a7b13d41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565057918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dda4c89fe2f1fd5b34e0f02e6c3dc5e288719164b8614ad3e5d439036a818a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:47:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 06:47:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 06:47:31 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91162d93e41e901767fb0ecc9c7694fbbb7b80a5384451f5ee29e2889d7672be`  
		Last Modified: Tue, 18 Nov 2025 02:56:26 GMT  
		Size: 16.3 MB (16267715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d157624c72b4d56de915d1a1b7dc5753760ddee0f8443f1fea29deb51353623`  
		Last Modified: Tue, 18 Nov 2025 04:10:00 GMT  
		Size: 56.0 MB (56048948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb42e4f564ea211f0c952153987cf04f1026b7ff7de4c09f7bb3a8688b84ef`  
		Last Modified: Tue, 18 Nov 2025 06:21:07 GMT  
		Size: 200.1 MB (200103553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc872224f064d19bcd2982760e95661841c43e2579efa91b96665dd6e6422a5e`  
		Last Modified: Tue, 18 Nov 2025 11:36:44 GMT  
		Size: 237.9 MB (237938103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3508e46685f84c184f2d40fa0e5e1dd432b56fac5ff49c4f89f5da871c9e4aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938fe2e0e0d226cdd5b6240520eeef16000293a86b21aa7e43919551bc2b5ad7`

```dockerfile
```

-	Layers:
	-	`sha256:f0d13a78e4ba5548e8f8b72cb5988887a0b65669987149ff339131e9446f92d7`  
		Last Modified: Tue, 18 Nov 2025 09:46:11 GMT  
		Size: 15.5 MB (15450753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3852ebec77d68f7f765683f3b73e8cc1310ca29c814272786c9acad92dead20`  
		Last Modified: Tue, 18 Nov 2025 09:46:14 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json
