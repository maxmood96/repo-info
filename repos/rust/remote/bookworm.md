## `rust:bookworm`

```console
$ docker pull rust@sha256:6ae102bdbf528294bc79ad6e1fae682f6f7c2a6e6621506ba959f9685b308a55
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

### `rust:bookworm` - linux; amd64

```console
$ docker pull rust@sha256:4ec71e955e6c08aeb238885083222ddff79d82eb87654a96c76e38e94da1a53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.5 MB (561483563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3316753323aa5edd4c2be762323794f4aa9f4335635dc4c7964ee99cb986d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:23:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:02:47 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 07 Apr 2026 05:02:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Tue, 07 Apr 2026 05:02:47 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b267853a2602be02c651d45a79ece242837985d07267fe166ad1109a4b3baa39`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 211.5 MB (211533439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2cfb71264fc5d467d6d3245474095c6366c6bd3b43f32bd29503dcd9540a72`  
		Last Modified: Tue, 07 Apr 2026 05:03:25 GMT  
		Size: 213.0 MB (213027020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:721d332242b6bba86f9462baafc98a90655e9014862c3ce921975ff117b9c330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15883320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b52f513ebb4bca95509baf28ea1a86ffc281d41161acd944e00e8f434304300`

```dockerfile
```

-	Layers:
	-	`sha256:01a655010d8718eb3d6b98331ef582c465e51011c9d55d05a6fca8833f3e3292`  
		Last Modified: Tue, 07 Apr 2026 05:03:21 GMT  
		Size: 15.9 MB (15869647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2491e245e482ec77b752cccadf65574f0c0a713b384643c1d261041ce154e128`  
		Last Modified: Tue, 07 Apr 2026 05:03:20 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:bde4ffc1d56369810c9c459c994ee5e4fc22c2e1ed79ce6501571e18acfbe93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557219212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc20a228a5f3f7fe497e2195bec8936186ba07b0ab336512be2342cc638b3f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:28:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 06:13:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 07 Apr 2026 06:13:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Tue, 07 Apr 2026 06:13:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626437a99246a6d3dc330350016eb9ecbf357123cec9028fd988893fdf863224`  
		Last Modified: Tue, 07 Apr 2026 03:49:22 GMT  
		Size: 59.7 MB (59651814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd84e150a9982ceb8ba7fc1ad7c67a055705b7ab812ff60037b40d4224d90ff`  
		Last Modified: Tue, 07 Apr 2026 04:28:43 GMT  
		Size: 175.4 MB (175432191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222e7f14e894416887fd3348471adfe46902b74d39f8686252c1d84a58a4ba64`  
		Last Modified: Tue, 07 Apr 2026 06:14:37 GMT  
		Size: 256.0 MB (255985307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d32887cbe10d9ea3dea8b09c693d19727530e5dcd89d0d8638381f5d92b05868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c018325dea4b0b47abe35f7870976b0fb1f914e285fb209a2b31e7706d6cae`

```dockerfile
```

-	Layers:
	-	`sha256:51f2e2a88b432450fb781667cebbd6fbfafd0841baaf968da02b6fae0b651afd`  
		Last Modified: Tue, 07 Apr 2026 06:14:32 GMT  
		Size: 15.7 MB (15672133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ef5c1fbc5fb0b42dba253bca8bcdcf1a6c5ab9b48169555b95ede0b67e977d`  
		Last Modified: Tue, 07 Apr 2026 06:14:32 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:55912ad77b52c411af5ecb4cf8901199b3688dbc96bf979570bbd8834dac69aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.0 MB (517988801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2955218ca3a4f3aee5c71026cd1ea3c315a1ed005d64e22792c2ce3c868f33e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:35:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:09:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 07 Apr 2026 05:09:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Tue, 07 Apr 2026 05:09:08 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad0741a80b84ae8126670b69ac8e761fcd50aa252da9d66b5636eca91971dbd`  
		Last Modified: Tue, 07 Apr 2026 03:35:50 GMT  
		Size: 203.1 MB (203067162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f7ebece3dde350b1684a771657782d82a0323bbf7386d59b511ffc310033d`  
		Last Modified: Tue, 07 Apr 2026 05:09:45 GMT  
		Size: 178.5 MB (178464164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f9ef4da1761aa433dc177da9f166f1779f0ed351f669c5f7316177fa2e2909e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755edea4714ea05f0bd816904858517f8fb584d2123f385d1196acb27485e01`

```dockerfile
```

-	Layers:
	-	`sha256:eee35f6c5e18b4a187de3dfddecfdd92fbfbecd96e5d0d29f7bb8a9110b85908`  
		Last Modified: Tue, 07 Apr 2026 05:09:41 GMT  
		Size: 15.9 MB (15898175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b485153e002cd2784dbf37a9790445ec71ade63b5acbefc038168ad31c490f0`  
		Last Modified: Tue, 07 Apr 2026 05:09:40 GMT  
		Size: 13.8 KB (13777 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:f4ac1ca4870e4006cd09b6469c5d1d25e5ddf742500cc0c1cfe6a8d4deb4ca86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.3 MB (588325140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7690f67ed500061f0a714091c26cdc0d86878323b6541e4844895747398bc31`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:48:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 07 Apr 2026 04:48:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Tue, 07 Apr 2026 04:48:31 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fefd2d4d18c0e4a1f706c31af7edb1bb87765de90f366b612fc4f713dbbfa`  
		Last Modified: Tue, 07 Apr 2026 02:40:53 GMT  
		Size: 66.2 MB (66234451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541046ceb46b7e73b05d2819e0dd8de9dc89e5270e5df42429a133712018c52`  
		Last Modified: Tue, 07 Apr 2026 03:19:47 GMT  
		Size: 210.5 MB (210473566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca89c07415f5e2c6038bf5a112770dff96fd4111a41af5c490173036d6e94c05`  
		Last Modified: Tue, 07 Apr 2026 04:49:13 GMT  
		Size: 237.3 MB (237267235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:43a772acc27f629b6a158fbbf62d63ca612be8d46153a08b876e4d0542ffae77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15860201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6835535839bb7fe6c38706ad06dda66a758568e2fd1629145208f30d29ee055b`

```dockerfile
```

-	Layers:
	-	`sha256:9242089bd9e36cd0b7affffd6a3238a1f90bab24d9e9013c504d62be20d7f533`  
		Last Modified: Tue, 07 Apr 2026 04:49:09 GMT  
		Size: 15.8 MB (15846560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9653bd714827a8b0eaa58d2bd346fc6d04157b2caf0fca589ea84bb41bd116`  
		Last Modified: Tue, 07 Apr 2026 04:49:08 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0b8da9e1dde384ee826aea76d77d47f5a77d6aa232e349dd84c43725d5de2e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 MB (655603161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc34492d592a3ba28e12e93e458505ef8c8b3691e23c6877f5cb18df8852704a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:06:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 01:58:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 08 Apr 2026 01:58:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Wed, 08 Apr 2026 01:58:55 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dc56fac65223b1a7667756725ea07ddf7bf4cb03642cc9106da638edca86e`  
		Last Modified: Tue, 07 Apr 2026 18:09:19 GMT  
		Size: 214.6 MB (214586971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2251270d16a68350f24ddb1da554867fcb4d62304ca51b0ea4fb4ae7807c42b7`  
		Last Modified: Wed, 08 Apr 2026 02:00:30 GMT  
		Size: 293.2 MB (293161553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5c1bae5e4f603d787f5d710b92a486d191e796ea875ad661e9de501a9870dc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15859893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd45cb37656b2945e314373924ff0e96cefdfef73c933765b14d01becaf311c`

```dockerfile
```

-	Layers:
	-	`sha256:fc14b55b8ee87da38bd81b234fc0b72465a2a651d01a1a16636a5f42f340ac77`  
		Last Modified: Wed, 08 Apr 2026 02:00:25 GMT  
		Size: 15.8 MB (15846176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93334b4d3fc7acd3afd949aa698659a7a0a3e3d3c15327dac60f11fc29018573`  
		Last Modified: Wed, 08 Apr 2026 02:00:23 GMT  
		Size: 13.7 KB (13717 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:597c8c2f00280dc06671c28b77dca40f4ef92defc274e26ab41d5bc853e5ec96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612375474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63afff0194462f81bacf023502b021fec10f03cb465744e8324c7fa0dfc3ba23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:59:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:40:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 07 Apr 2026 09:40:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.94.1
# Tue, 07 Apr 2026 09:40:27 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47976b1872c5d8fc1ceda4d073087f195be5506b083608f5c0a6767f6b55978a`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 24.0 MB (24033635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3377e46a7f95ad649f4e145572c4253ed3ebf1b9fa463b58c96cf8b20d651ac`  
		Last Modified: Tue, 07 Apr 2026 04:55:04 GMT  
		Size: 63.5 MB (63501358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c31f7e179e46a8a43c58fdf87877cede1441cea2cb5cf12d4262787cd7f3ca`  
		Last Modified: Tue, 07 Apr 2026 06:00:35 GMT  
		Size: 183.6 MB (183569969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83041c7c37a2a8d58316e8dd56b4ace6dd8ba376117362f64c2e647ea5dd00ad`  
		Last Modified: Tue, 07 Apr 2026 09:41:50 GMT  
		Size: 294.1 MB (294122428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:16b229b600158f0b3b929cd8cf6afd19fcc7b7e12cf0e4fef0f58003768c0ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5c240a6eb159d75260026153362feab4d30b18fb14f5110825ca9512f44f9`

```dockerfile
```

-	Layers:
	-	`sha256:f1516499dd9b19ccafaf19e6f08c86a3b0a2dbb12b7e85a824a9ce9314c53bd3`  
		Last Modified: Tue, 07 Apr 2026 09:41:45 GMT  
		Size: 15.7 MB (15677243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d67e1dd247822d41cacdfb8c7a7ccd99353a072bca1baaea0b9efc250cec7a8`  
		Last Modified: Tue, 07 Apr 2026 09:41:45 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json
