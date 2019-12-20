<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1.40`](#rust140)
-	[`rust:1.40.0`](#rust1400)
-	[`rust:1.40.0-alpine`](#rust1400-alpine)
-	[`rust:1.40.0-alpine3.10`](#rust1400-alpine310)
-	[`rust:1.40.0-buster`](#rust1400-buster)
-	[`rust:1.40.0-slim`](#rust1400-slim)
-	[`rust:1.40.0-slim-buster`](#rust1400-slim-buster)
-	[`rust:1.40.0-slim-stretch`](#rust1400-slim-stretch)
-	[`rust:1.40.0-stretch`](#rust1400-stretch)
-	[`rust:1.40-alpine`](#rust140-alpine)
-	[`rust:1.40-alpine3.10`](#rust140-alpine310)
-	[`rust:1.40-buster`](#rust140-buster)
-	[`rust:1.40-slim`](#rust140-slim)
-	[`rust:1.40-slim-buster`](#rust140-slim-buster)
-	[`rust:1.40-slim-stretch`](#rust140-slim-stretch)
-	[`rust:1.40-stretch`](#rust140-stretch)
-	[`rust:1-alpine`](#rust1-alpine)
-	[`rust:1-alpine3.10`](#rust1-alpine310)
-	[`rust:1-buster`](#rust1-buster)
-	[`rust:1-slim`](#rust1-slim)
-	[`rust:1-slim-buster`](#rust1-slim-buster)
-	[`rust:1-slim-stretch`](#rust1-slim-stretch)
-	[`rust:1-stretch`](#rust1-stretch)
-	[`rust:alpine`](#rustalpine)
-	[`rust:alpine3.10`](#rustalpine310)
-	[`rust:buster`](#rustbuster)
-	[`rust:latest`](#rustlatest)
-	[`rust:slim`](#rustslim)
-	[`rust:slim-buster`](#rustslim-buster)
-	[`rust:slim-stretch`](#rustslim-stretch)
-	[`rust:stretch`](#ruststretch)

## `rust:1`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-alpine`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1.40.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-alpine3.10`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1.40.0-alpine3.10` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-buster`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0-buster` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-buster` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-slim`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-slim-buster`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-slim-stretch`

```console
$ docker pull rust@sha256:18efb75eb413d196bbd64a8b4e49225653157e0652d5b824de25a6182f6a61c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0-slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:57c6607fec3c2bfebc517cb9c13321aee87cfd84bace6f53bddbb23c15452b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189328904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94d78b219741c33f7ca91069f2f418bd15960e08c8ac3f31be062ac60551fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:59:24 GMT
ADD file:2c1f5e08834f13ccb9c2326204eb2556e03239d00171e75755c7195289374c61 in / 
# Fri, 22 Nov 2019 14:59:25 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d599a449871ee73b960e80d176b989365dfecb4c8f337bf21e8853862403ee9b`  
		Last Modified: Fri, 22 Nov 2019 15:06:36 GMT  
		Size: 22.5 MB (22524572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a808f9be53ad3051a0da3ba8c2600cba69684fd510f3fc12d59be3902e4e890`  
		Last Modified: Thu, 19 Dec 2019 23:40:16 GMT  
		Size: 166.8 MB (166804332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:17cdc3b13dca4448f6ca6630e2fa70554f5333e468909f30ba12fb1ce44f6188
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fdab16188070657a517c3549752bd5d1f5f42f8fc52f6f03bda11a6438ec5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:28:28 GMT
ADD file:9fcbe16260f606fbea9a4811e693312434fbc4b300e974d33dcac84808f2323c in / 
# Fri, 22 Nov 2019 13:28:29 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:19:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:20:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d721220e5446968b6d6c8c3cd477d7deaadfd7f3ea7070342828f151408cbc93`  
		Last Modified: Fri, 22 Nov 2019 13:36:57 GMT  
		Size: 19.3 MB (19311578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077fd0c83889eaea5dd90c7a392ea4ecd5436249984f4c55814dfc60c741f0e4`  
		Last Modified: Fri, 20 Dec 2019 00:25:18 GMT  
		Size: 143.6 MB (143623330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a1ef6c8c6d5504d56fd9f67c866ace7ad1b26f02a11a3678ad971e163f9360ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164549005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048c98f570a1ff655c5340bd5b5c6c1c90783447553197e411d6ed34e205782e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:50 GMT
ADD file:8e4d0a1e6805c641fc9d18ebad82e4b01d85c6cb9f87d1ef47d75d150212a392 in / 
# Fri, 22 Nov 2019 13:45:53 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:34:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:98a64bf4db7d2219b4fdd8182188d9422810dee890e997095bfb564a0482eed6`  
		Last Modified: Fri, 22 Nov 2019 13:52:17 GMT  
		Size: 20.4 MB (20385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b832e63d71815acfddc8f292e3348c05ee1643280093ea87850ed9cf21a03df`  
		Last Modified: Fri, 20 Dec 2019 00:39:34 GMT  
		Size: 144.2 MB (144163246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:e1b852bfef4bc48288a30548993b4c1a3cceb5a53fb885a8bd2dc1ac23d43abf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210290510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705fa69680fec731459f5e53634dfd7d408fe33fad0538c7577bbd3a76983d64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:44 GMT
ADD file:19d04f738434c76e2dbd14b48de2f0f03afa883b15f638c6ecbbf382df03567c in / 
# Fri, 22 Nov 2019 16:54:44 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:30:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:f26c9a85c76e393c9f2313b30e82d09f933d2dd4883620de242c7d21f8812e91`  
		Last Modified: Fri, 22 Nov 2019 17:03:03 GMT  
		Size: 23.2 MB (23152070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c37abc3a3e7a71d7e95e5889909b34c1611442441497e3702ffd17271460961`  
		Last Modified: Fri, 20 Dec 2019 00:34:01 GMT  
		Size: 187.1 MB (187138440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40.0-stretch`

```console
$ docker pull rust@sha256:ed8271d153db3e91f34e59fd57602836d9f6fed919713d0b50b40cd8a96e6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40.0-stretch` - linux; amd64

```console
$ docker pull rust@sha256:8799cee901791082ca011eae1eb30fd62166fee80f38284e46c28dc764f5cdf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.3 MB (454337046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5302f1b5dabd05a5ad5f9331511d3c230d2d4963c6e168f72857636e7beabf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:58:56 GMT
ADD file:152359c10cf61d80091bfd19e7e1968a538bebebfa048dca0386e35e1e999730 in / 
# Fri, 22 Nov 2019 14:58:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:12:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:13:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:36:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:07 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:844c33c7e6ea19e3f6847e0667befdfb3ef02d6fc735b22c2d070261b6263b97`  
		Last Modified: Fri, 22 Nov 2019 15:06:19 GMT  
		Size: 45.4 MB (45380759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada5d61ae65dc038b4ba788ae5124c2587d0ebe83d3534733677216547b65cbd`  
		Last Modified: Sat, 23 Nov 2019 00:20:40 GMT  
		Size: 10.8 MB (10796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8427fdf429235414d0ea4757fd45fd81f09fd2ba3106e13796a8250f0a04a23`  
		Last Modified: Sat, 23 Nov 2019 00:20:39 GMT  
		Size: 4.3 MB (4340186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bafc4ab87c34cee7bfc43340fa7904dfe6d29a266537f2026cee3a76adfd`  
		Last Modified: Sat, 23 Nov 2019 00:20:56 GMT  
		Size: 50.1 MB (50065503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9577c0793430759082b98068eb2884638a34fa46ca481099e93cfc38d4ebfe`  
		Last Modified: Sat, 23 Nov 2019 00:21:35 GMT  
		Size: 214.8 MB (214841433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1501da54344da67a16aa924db62c0d8f2adda671b60360c046fa04bc9f6e6ba`  
		Last Modified: Thu, 19 Dec 2019 23:39:41 GMT  
		Size: 128.9 MB (128912240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:d96b561912fca37e28cba1a1cc054a03c9a922f070dd1cc0a24f6b56d8ef5820
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 MB (412996360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0928b78b0924d8c0beab12651c97f29861162804784dc2ce4974da728dff33`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:27:54 GMT
ADD file:3893b8a7336301b4a2a741f62c99805c3c7b2bee21e4f026b6885060becfc03d in / 
# Fri, 22 Nov 2019 13:27:57 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:24:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:28:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:18:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:19:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:fb827ed75ba2d760675c1e0dfd2cef27b5120725860abe8870ee3842dfce2a08`  
		Last Modified: Fri, 22 Nov 2019 13:36:40 GMT  
		Size: 42.1 MB (42108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fdca0c72a7ddca7b66d2c47a5de442518d8631adef3269a541a8ee1a1faec5`  
		Last Modified: Fri, 22 Nov 2019 23:34:21 GMT  
		Size: 9.5 MB (9497771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6508d4d51e15108ee995e92f1f1e2bbcec6c4c61ec1997ed246abe0b6504f316`  
		Last Modified: Fri, 22 Nov 2019 23:34:20 GMT  
		Size: 3.9 MB (3918760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8056142a63015026b87069d963bff11cd0de2fc98ce2e0d265c1eae3aaede`  
		Last Modified: Fri, 22 Nov 2019 23:34:44 GMT  
		Size: 46.4 MB (46390335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65472c61ccc368200b23f3c177b57530a446931fbdf7628ee668d699314e2a9`  
		Last Modified: Fri, 22 Nov 2019 23:35:40 GMT  
		Size: 195.5 MB (195522890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca2bec49b499e28e120e9d29d72bfc6b03dd5e9388fe93c299a328f6c51239d`  
		Last Modified: Fri, 20 Dec 2019 00:24:29 GMT  
		Size: 115.6 MB (115558535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:48c2253ccb471cb9ffdbb91bceffae245cceee86e04d23443a0cd0e86a23a4d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420789320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd1db3750013cde4e94a47ddc5130f2a253e21c99891e4e873e61d4c745f80a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:17 GMT
ADD file:ad8ecaf59c4f4c76dd6d93f5efff4420e3b55b36937eb36df317c7cd9ba19aeb in / 
# Fri, 22 Nov 2019 13:45:20 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:22:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:22:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:25:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:34:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:34:43 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c0d6add7f35c078f38df34ebc5a91afab0ba514167d17ad24fd4582eb0880bf4`  
		Last Modified: Fri, 22 Nov 2019 13:51:57 GMT  
		Size: 43.2 MB (43166306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616dd61dc37eac19d38cdbdf732659429ae37ba0d1578100f874fe236e25125`  
		Last Modified: Fri, 22 Nov 2019 20:30:41 GMT  
		Size: 9.7 MB (9747762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36da42882c170ff4b949c027b410428b5c0942632ed441a2f9a168a859ec0c`  
		Last Modified: Fri, 22 Nov 2019 20:30:39 GMT  
		Size: 4.1 MB (4094358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81386fcdc923e324fecbdb336d477691cc0be39e7e4e23ec733257ee50eddd57`  
		Last Modified: Fri, 22 Nov 2019 20:31:04 GMT  
		Size: 48.0 MB (48016405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6156b4a56fd4867da733a232b3da5a4312ee906bd7a09d869b3e3e026b36a5`  
		Last Modified: Fri, 22 Nov 2019 20:32:03 GMT  
		Size: 202.2 MB (202233068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd1ee4c6ce5c5845eb3bc8694b36c235eb904590d829c29e03a0beaaf54f461`  
		Last Modified: Fri, 20 Dec 2019 00:38:42 GMT  
		Size: 113.5 MB (113531421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40.0-stretch` - linux; 386

```console
$ docker pull rust@sha256:87e02add0b10a4927341ab7f15abdc4f45531e5eb81a76080f471c786bc30d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478226201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee49388f75139020a8336510e62aa24d7e873bfcf01230bcdd133edc3088e88a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:23 GMT
ADD file:5c01b74109a8b04410a939b8bd31367bdef970268befe81e02e43ddc646d79bc in / 
# Fri, 22 Nov 2019 16:54:23 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:57:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:57:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:59:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:29:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:10 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0f5940e26a4f3cd4f9002a93c11a8590498495bd0f4ce3fe102e4ddaf7c06d3a`  
		Last Modified: Fri, 22 Nov 2019 17:02:42 GMT  
		Size: 46.1 MB (46100192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536d6fcd65812215df48791595c7d5c60bbe22edb13d48f7c0357e62f65eeeba`  
		Last Modified: Sat, 23 Nov 2019 01:05:45 GMT  
		Size: 10.8 MB (10817095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc23bc091e68a62e274b04a4e8727ea5643f92492bd364f636e8bc810b330a`  
		Last Modified: Sat, 23 Nov 2019 01:05:43 GMT  
		Size: 4.6 MB (4561440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11260fd9d9f5ae8394485c75e8f285a441c5e66ef4fd756ebf2e595ca413cc6c`  
		Last Modified: Sat, 23 Nov 2019 01:06:05 GMT  
		Size: 51.6 MB (51586618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f02a75bb65f92aecb93cf402eaba19d0c711254da0845b5fc8d45679781c295`  
		Last Modified: Sat, 23 Nov 2019 01:07:04 GMT  
		Size: 219.9 MB (219925171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a31917e077d895d65f5e1c0a9ce0bb2d4e2ef1ff52af3308156bc48e4e7d2ee`  
		Last Modified: Fri, 20 Dec 2019 00:33:06 GMT  
		Size: 145.2 MB (145235685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-alpine`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1.40-alpine` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-alpine3.10`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1.40-alpine3.10` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-buster`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40-buster` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-buster` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-slim`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40-slim` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-slim-buster`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-slim-stretch`

```console
$ docker pull rust@sha256:18efb75eb413d196bbd64a8b4e49225653157e0652d5b824de25a6182f6a61c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40-slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:57c6607fec3c2bfebc517cb9c13321aee87cfd84bace6f53bddbb23c15452b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189328904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94d78b219741c33f7ca91069f2f418bd15960e08c8ac3f31be062ac60551fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:59:24 GMT
ADD file:2c1f5e08834f13ccb9c2326204eb2556e03239d00171e75755c7195289374c61 in / 
# Fri, 22 Nov 2019 14:59:25 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d599a449871ee73b960e80d176b989365dfecb4c8f337bf21e8853862403ee9b`  
		Last Modified: Fri, 22 Nov 2019 15:06:36 GMT  
		Size: 22.5 MB (22524572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a808f9be53ad3051a0da3ba8c2600cba69684fd510f3fc12d59be3902e4e890`  
		Last Modified: Thu, 19 Dec 2019 23:40:16 GMT  
		Size: 166.8 MB (166804332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:17cdc3b13dca4448f6ca6630e2fa70554f5333e468909f30ba12fb1ce44f6188
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fdab16188070657a517c3549752bd5d1f5f42f8fc52f6f03bda11a6438ec5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:28:28 GMT
ADD file:9fcbe16260f606fbea9a4811e693312434fbc4b300e974d33dcac84808f2323c in / 
# Fri, 22 Nov 2019 13:28:29 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:19:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:20:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d721220e5446968b6d6c8c3cd477d7deaadfd7f3ea7070342828f151408cbc93`  
		Last Modified: Fri, 22 Nov 2019 13:36:57 GMT  
		Size: 19.3 MB (19311578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077fd0c83889eaea5dd90c7a392ea4ecd5436249984f4c55814dfc60c741f0e4`  
		Last Modified: Fri, 20 Dec 2019 00:25:18 GMT  
		Size: 143.6 MB (143623330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a1ef6c8c6d5504d56fd9f67c866ace7ad1b26f02a11a3678ad971e163f9360ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164549005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048c98f570a1ff655c5340bd5b5c6c1c90783447553197e411d6ed34e205782e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:50 GMT
ADD file:8e4d0a1e6805c641fc9d18ebad82e4b01d85c6cb9f87d1ef47d75d150212a392 in / 
# Fri, 22 Nov 2019 13:45:53 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:34:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:98a64bf4db7d2219b4fdd8182188d9422810dee890e997095bfb564a0482eed6`  
		Last Modified: Fri, 22 Nov 2019 13:52:17 GMT  
		Size: 20.4 MB (20385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b832e63d71815acfddc8f292e3348c05ee1643280093ea87850ed9cf21a03df`  
		Last Modified: Fri, 20 Dec 2019 00:39:34 GMT  
		Size: 144.2 MB (144163246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:e1b852bfef4bc48288a30548993b4c1a3cceb5a53fb885a8bd2dc1ac23d43abf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210290510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705fa69680fec731459f5e53634dfd7d408fe33fad0538c7577bbd3a76983d64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:44 GMT
ADD file:19d04f738434c76e2dbd14b48de2f0f03afa883b15f638c6ecbbf382df03567c in / 
# Fri, 22 Nov 2019 16:54:44 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:30:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:f26c9a85c76e393c9f2313b30e82d09f933d2dd4883620de242c7d21f8812e91`  
		Last Modified: Fri, 22 Nov 2019 17:03:03 GMT  
		Size: 23.2 MB (23152070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c37abc3a3e7a71d7e95e5889909b34c1611442441497e3702ffd17271460961`  
		Last Modified: Fri, 20 Dec 2019 00:34:01 GMT  
		Size: 187.1 MB (187138440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1.40-stretch`

```console
$ docker pull rust@sha256:ed8271d153db3e91f34e59fd57602836d9f6fed919713d0b50b40cd8a96e6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1.40-stretch` - linux; amd64

```console
$ docker pull rust@sha256:8799cee901791082ca011eae1eb30fd62166fee80f38284e46c28dc764f5cdf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.3 MB (454337046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5302f1b5dabd05a5ad5f9331511d3c230d2d4963c6e168f72857636e7beabf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:58:56 GMT
ADD file:152359c10cf61d80091bfd19e7e1968a538bebebfa048dca0386e35e1e999730 in / 
# Fri, 22 Nov 2019 14:58:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:12:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:13:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:36:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:07 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:844c33c7e6ea19e3f6847e0667befdfb3ef02d6fc735b22c2d070261b6263b97`  
		Last Modified: Fri, 22 Nov 2019 15:06:19 GMT  
		Size: 45.4 MB (45380759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada5d61ae65dc038b4ba788ae5124c2587d0ebe83d3534733677216547b65cbd`  
		Last Modified: Sat, 23 Nov 2019 00:20:40 GMT  
		Size: 10.8 MB (10796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8427fdf429235414d0ea4757fd45fd81f09fd2ba3106e13796a8250f0a04a23`  
		Last Modified: Sat, 23 Nov 2019 00:20:39 GMT  
		Size: 4.3 MB (4340186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bafc4ab87c34cee7bfc43340fa7904dfe6d29a266537f2026cee3a76adfd`  
		Last Modified: Sat, 23 Nov 2019 00:20:56 GMT  
		Size: 50.1 MB (50065503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9577c0793430759082b98068eb2884638a34fa46ca481099e93cfc38d4ebfe`  
		Last Modified: Sat, 23 Nov 2019 00:21:35 GMT  
		Size: 214.8 MB (214841433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1501da54344da67a16aa924db62c0d8f2adda671b60360c046fa04bc9f6e6ba`  
		Last Modified: Thu, 19 Dec 2019 23:39:41 GMT  
		Size: 128.9 MB (128912240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:d96b561912fca37e28cba1a1cc054a03c9a922f070dd1cc0a24f6b56d8ef5820
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 MB (412996360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0928b78b0924d8c0beab12651c97f29861162804784dc2ce4974da728dff33`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:27:54 GMT
ADD file:3893b8a7336301b4a2a741f62c99805c3c7b2bee21e4f026b6885060becfc03d in / 
# Fri, 22 Nov 2019 13:27:57 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:24:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:28:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:18:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:19:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:fb827ed75ba2d760675c1e0dfd2cef27b5120725860abe8870ee3842dfce2a08`  
		Last Modified: Fri, 22 Nov 2019 13:36:40 GMT  
		Size: 42.1 MB (42108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fdca0c72a7ddca7b66d2c47a5de442518d8631adef3269a541a8ee1a1faec5`  
		Last Modified: Fri, 22 Nov 2019 23:34:21 GMT  
		Size: 9.5 MB (9497771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6508d4d51e15108ee995e92f1f1e2bbcec6c4c61ec1997ed246abe0b6504f316`  
		Last Modified: Fri, 22 Nov 2019 23:34:20 GMT  
		Size: 3.9 MB (3918760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8056142a63015026b87069d963bff11cd0de2fc98ce2e0d265c1eae3aaede`  
		Last Modified: Fri, 22 Nov 2019 23:34:44 GMT  
		Size: 46.4 MB (46390335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65472c61ccc368200b23f3c177b57530a446931fbdf7628ee668d699314e2a9`  
		Last Modified: Fri, 22 Nov 2019 23:35:40 GMT  
		Size: 195.5 MB (195522890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca2bec49b499e28e120e9d29d72bfc6b03dd5e9388fe93c299a328f6c51239d`  
		Last Modified: Fri, 20 Dec 2019 00:24:29 GMT  
		Size: 115.6 MB (115558535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:48c2253ccb471cb9ffdbb91bceffae245cceee86e04d23443a0cd0e86a23a4d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420789320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd1db3750013cde4e94a47ddc5130f2a253e21c99891e4e873e61d4c745f80a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:17 GMT
ADD file:ad8ecaf59c4f4c76dd6d93f5efff4420e3b55b36937eb36df317c7cd9ba19aeb in / 
# Fri, 22 Nov 2019 13:45:20 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:22:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:22:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:25:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:34:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:34:43 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c0d6add7f35c078f38df34ebc5a91afab0ba514167d17ad24fd4582eb0880bf4`  
		Last Modified: Fri, 22 Nov 2019 13:51:57 GMT  
		Size: 43.2 MB (43166306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616dd61dc37eac19d38cdbdf732659429ae37ba0d1578100f874fe236e25125`  
		Last Modified: Fri, 22 Nov 2019 20:30:41 GMT  
		Size: 9.7 MB (9747762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36da42882c170ff4b949c027b410428b5c0942632ed441a2f9a168a859ec0c`  
		Last Modified: Fri, 22 Nov 2019 20:30:39 GMT  
		Size: 4.1 MB (4094358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81386fcdc923e324fecbdb336d477691cc0be39e7e4e23ec733257ee50eddd57`  
		Last Modified: Fri, 22 Nov 2019 20:31:04 GMT  
		Size: 48.0 MB (48016405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6156b4a56fd4867da733a232b3da5a4312ee906bd7a09d869b3e3e026b36a5`  
		Last Modified: Fri, 22 Nov 2019 20:32:03 GMT  
		Size: 202.2 MB (202233068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd1ee4c6ce5c5845eb3bc8694b36c235eb904590d829c29e03a0beaaf54f461`  
		Last Modified: Fri, 20 Dec 2019 00:38:42 GMT  
		Size: 113.5 MB (113531421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1.40-stretch` - linux; 386

```console
$ docker pull rust@sha256:87e02add0b10a4927341ab7f15abdc4f45531e5eb81a76080f471c786bc30d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478226201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee49388f75139020a8336510e62aa24d7e873bfcf01230bcdd133edc3088e88a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:23 GMT
ADD file:5c01b74109a8b04410a939b8bd31367bdef970268befe81e02e43ddc646d79bc in / 
# Fri, 22 Nov 2019 16:54:23 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:57:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:57:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:59:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:29:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:10 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0f5940e26a4f3cd4f9002a93c11a8590498495bd0f4ce3fe102e4ddaf7c06d3a`  
		Last Modified: Fri, 22 Nov 2019 17:02:42 GMT  
		Size: 46.1 MB (46100192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536d6fcd65812215df48791595c7d5c60bbe22edb13d48f7c0357e62f65eeeba`  
		Last Modified: Sat, 23 Nov 2019 01:05:45 GMT  
		Size: 10.8 MB (10817095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc23bc091e68a62e274b04a4e8727ea5643f92492bd364f636e8bc810b330a`  
		Last Modified: Sat, 23 Nov 2019 01:05:43 GMT  
		Size: 4.6 MB (4561440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11260fd9d9f5ae8394485c75e8f285a441c5e66ef4fd756ebf2e595ca413cc6c`  
		Last Modified: Sat, 23 Nov 2019 01:06:05 GMT  
		Size: 51.6 MB (51586618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f02a75bb65f92aecb93cf402eaba19d0c711254da0845b5fc8d45679781c295`  
		Last Modified: Sat, 23 Nov 2019 01:07:04 GMT  
		Size: 219.9 MB (219925171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a31917e077d895d65f5e1c0a9ce0bb2d4e2ef1ff52af3308156bc48e4e7d2ee`  
		Last Modified: Fri, 20 Dec 2019 00:33:06 GMT  
		Size: 145.2 MB (145235685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-alpine`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-alpine3.10`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:1-alpine3.10` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-buster`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-buster` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-buster` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-slim`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-slim-stretch`

```console
$ docker pull rust@sha256:18efb75eb413d196bbd64a8b4e49225653157e0652d5b824de25a6182f6a61c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:57c6607fec3c2bfebc517cb9c13321aee87cfd84bace6f53bddbb23c15452b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189328904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94d78b219741c33f7ca91069f2f418bd15960e08c8ac3f31be062ac60551fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:59:24 GMT
ADD file:2c1f5e08834f13ccb9c2326204eb2556e03239d00171e75755c7195289374c61 in / 
# Fri, 22 Nov 2019 14:59:25 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d599a449871ee73b960e80d176b989365dfecb4c8f337bf21e8853862403ee9b`  
		Last Modified: Fri, 22 Nov 2019 15:06:36 GMT  
		Size: 22.5 MB (22524572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a808f9be53ad3051a0da3ba8c2600cba69684fd510f3fc12d59be3902e4e890`  
		Last Modified: Thu, 19 Dec 2019 23:40:16 GMT  
		Size: 166.8 MB (166804332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:17cdc3b13dca4448f6ca6630e2fa70554f5333e468909f30ba12fb1ce44f6188
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fdab16188070657a517c3549752bd5d1f5f42f8fc52f6f03bda11a6438ec5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:28:28 GMT
ADD file:9fcbe16260f606fbea9a4811e693312434fbc4b300e974d33dcac84808f2323c in / 
# Fri, 22 Nov 2019 13:28:29 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:19:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:20:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d721220e5446968b6d6c8c3cd477d7deaadfd7f3ea7070342828f151408cbc93`  
		Last Modified: Fri, 22 Nov 2019 13:36:57 GMT  
		Size: 19.3 MB (19311578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077fd0c83889eaea5dd90c7a392ea4ecd5436249984f4c55814dfc60c741f0e4`  
		Last Modified: Fri, 20 Dec 2019 00:25:18 GMT  
		Size: 143.6 MB (143623330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a1ef6c8c6d5504d56fd9f67c866ace7ad1b26f02a11a3678ad971e163f9360ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164549005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048c98f570a1ff655c5340bd5b5c6c1c90783447553197e411d6ed34e205782e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:50 GMT
ADD file:8e4d0a1e6805c641fc9d18ebad82e4b01d85c6cb9f87d1ef47d75d150212a392 in / 
# Fri, 22 Nov 2019 13:45:53 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:34:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:98a64bf4db7d2219b4fdd8182188d9422810dee890e997095bfb564a0482eed6`  
		Last Modified: Fri, 22 Nov 2019 13:52:17 GMT  
		Size: 20.4 MB (20385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b832e63d71815acfddc8f292e3348c05ee1643280093ea87850ed9cf21a03df`  
		Last Modified: Fri, 20 Dec 2019 00:39:34 GMT  
		Size: 144.2 MB (144163246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:e1b852bfef4bc48288a30548993b4c1a3cceb5a53fb885a8bd2dc1ac23d43abf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210290510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705fa69680fec731459f5e53634dfd7d408fe33fad0538c7577bbd3a76983d64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:44 GMT
ADD file:19d04f738434c76e2dbd14b48de2f0f03afa883b15f638c6ecbbf382df03567c in / 
# Fri, 22 Nov 2019 16:54:44 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:30:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:f26c9a85c76e393c9f2313b30e82d09f933d2dd4883620de242c7d21f8812e91`  
		Last Modified: Fri, 22 Nov 2019 17:03:03 GMT  
		Size: 23.2 MB (23152070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c37abc3a3e7a71d7e95e5889909b34c1611442441497e3702ffd17271460961`  
		Last Modified: Fri, 20 Dec 2019 00:34:01 GMT  
		Size: 187.1 MB (187138440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:1-stretch`

```console
$ docker pull rust@sha256:ed8271d153db3e91f34e59fd57602836d9f6fed919713d0b50b40cd8a96e6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-stretch` - linux; amd64

```console
$ docker pull rust@sha256:8799cee901791082ca011eae1eb30fd62166fee80f38284e46c28dc764f5cdf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.3 MB (454337046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5302f1b5dabd05a5ad5f9331511d3c230d2d4963c6e168f72857636e7beabf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:58:56 GMT
ADD file:152359c10cf61d80091bfd19e7e1968a538bebebfa048dca0386e35e1e999730 in / 
# Fri, 22 Nov 2019 14:58:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:12:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:13:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:36:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:07 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:844c33c7e6ea19e3f6847e0667befdfb3ef02d6fc735b22c2d070261b6263b97`  
		Last Modified: Fri, 22 Nov 2019 15:06:19 GMT  
		Size: 45.4 MB (45380759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada5d61ae65dc038b4ba788ae5124c2587d0ebe83d3534733677216547b65cbd`  
		Last Modified: Sat, 23 Nov 2019 00:20:40 GMT  
		Size: 10.8 MB (10796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8427fdf429235414d0ea4757fd45fd81f09fd2ba3106e13796a8250f0a04a23`  
		Last Modified: Sat, 23 Nov 2019 00:20:39 GMT  
		Size: 4.3 MB (4340186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bafc4ab87c34cee7bfc43340fa7904dfe6d29a266537f2026cee3a76adfd`  
		Last Modified: Sat, 23 Nov 2019 00:20:56 GMT  
		Size: 50.1 MB (50065503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9577c0793430759082b98068eb2884638a34fa46ca481099e93cfc38d4ebfe`  
		Last Modified: Sat, 23 Nov 2019 00:21:35 GMT  
		Size: 214.8 MB (214841433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1501da54344da67a16aa924db62c0d8f2adda671b60360c046fa04bc9f6e6ba`  
		Last Modified: Thu, 19 Dec 2019 23:39:41 GMT  
		Size: 128.9 MB (128912240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:d96b561912fca37e28cba1a1cc054a03c9a922f070dd1cc0a24f6b56d8ef5820
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 MB (412996360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0928b78b0924d8c0beab12651c97f29861162804784dc2ce4974da728dff33`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:27:54 GMT
ADD file:3893b8a7336301b4a2a741f62c99805c3c7b2bee21e4f026b6885060becfc03d in / 
# Fri, 22 Nov 2019 13:27:57 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:24:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:28:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:18:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:19:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:fb827ed75ba2d760675c1e0dfd2cef27b5120725860abe8870ee3842dfce2a08`  
		Last Modified: Fri, 22 Nov 2019 13:36:40 GMT  
		Size: 42.1 MB (42108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fdca0c72a7ddca7b66d2c47a5de442518d8631adef3269a541a8ee1a1faec5`  
		Last Modified: Fri, 22 Nov 2019 23:34:21 GMT  
		Size: 9.5 MB (9497771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6508d4d51e15108ee995e92f1f1e2bbcec6c4c61ec1997ed246abe0b6504f316`  
		Last Modified: Fri, 22 Nov 2019 23:34:20 GMT  
		Size: 3.9 MB (3918760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8056142a63015026b87069d963bff11cd0de2fc98ce2e0d265c1eae3aaede`  
		Last Modified: Fri, 22 Nov 2019 23:34:44 GMT  
		Size: 46.4 MB (46390335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65472c61ccc368200b23f3c177b57530a446931fbdf7628ee668d699314e2a9`  
		Last Modified: Fri, 22 Nov 2019 23:35:40 GMT  
		Size: 195.5 MB (195522890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca2bec49b499e28e120e9d29d72bfc6b03dd5e9388fe93c299a328f6c51239d`  
		Last Modified: Fri, 20 Dec 2019 00:24:29 GMT  
		Size: 115.6 MB (115558535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:48c2253ccb471cb9ffdbb91bceffae245cceee86e04d23443a0cd0e86a23a4d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420789320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd1db3750013cde4e94a47ddc5130f2a253e21c99891e4e873e61d4c745f80a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:17 GMT
ADD file:ad8ecaf59c4f4c76dd6d93f5efff4420e3b55b36937eb36df317c7cd9ba19aeb in / 
# Fri, 22 Nov 2019 13:45:20 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:22:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:22:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:25:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:34:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:34:43 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c0d6add7f35c078f38df34ebc5a91afab0ba514167d17ad24fd4582eb0880bf4`  
		Last Modified: Fri, 22 Nov 2019 13:51:57 GMT  
		Size: 43.2 MB (43166306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616dd61dc37eac19d38cdbdf732659429ae37ba0d1578100f874fe236e25125`  
		Last Modified: Fri, 22 Nov 2019 20:30:41 GMT  
		Size: 9.7 MB (9747762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36da42882c170ff4b949c027b410428b5c0942632ed441a2f9a168a859ec0c`  
		Last Modified: Fri, 22 Nov 2019 20:30:39 GMT  
		Size: 4.1 MB (4094358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81386fcdc923e324fecbdb336d477691cc0be39e7e4e23ec733257ee50eddd57`  
		Last Modified: Fri, 22 Nov 2019 20:31:04 GMT  
		Size: 48.0 MB (48016405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6156b4a56fd4867da733a232b3da5a4312ee906bd7a09d869b3e3e026b36a5`  
		Last Modified: Fri, 22 Nov 2019 20:32:03 GMT  
		Size: 202.2 MB (202233068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd1ee4c6ce5c5845eb3bc8694b36c235eb904590d829c29e03a0beaaf54f461`  
		Last Modified: Fri, 20 Dec 2019 00:38:42 GMT  
		Size: 113.5 MB (113531421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-stretch` - linux; 386

```console
$ docker pull rust@sha256:87e02add0b10a4927341ab7f15abdc4f45531e5eb81a76080f471c786bc30d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478226201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee49388f75139020a8336510e62aa24d7e873bfcf01230bcdd133edc3088e88a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:23 GMT
ADD file:5c01b74109a8b04410a939b8bd31367bdef970268befe81e02e43ddc646d79bc in / 
# Fri, 22 Nov 2019 16:54:23 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:57:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:57:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:59:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:29:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:10 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0f5940e26a4f3cd4f9002a93c11a8590498495bd0f4ce3fe102e4ddaf7c06d3a`  
		Last Modified: Fri, 22 Nov 2019 17:02:42 GMT  
		Size: 46.1 MB (46100192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536d6fcd65812215df48791595c7d5c60bbe22edb13d48f7c0357e62f65eeeba`  
		Last Modified: Sat, 23 Nov 2019 01:05:45 GMT  
		Size: 10.8 MB (10817095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc23bc091e68a62e274b04a4e8727ea5643f92492bd364f636e8bc810b330a`  
		Last Modified: Sat, 23 Nov 2019 01:05:43 GMT  
		Size: 4.6 MB (4561440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11260fd9d9f5ae8394485c75e8f285a441c5e66ef4fd756ebf2e595ca413cc6c`  
		Last Modified: Sat, 23 Nov 2019 01:06:05 GMT  
		Size: 51.6 MB (51586618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f02a75bb65f92aecb93cf402eaba19d0c711254da0845b5fc8d45679781c295`  
		Last Modified: Sat, 23 Nov 2019 01:07:04 GMT  
		Size: 219.9 MB (219925171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a31917e077d895d65f5e1c0a9ce0bb2d4e2ef1ff52af3308156bc48e4e7d2ee`  
		Last Modified: Fri, 20 Dec 2019 00:33:06 GMT  
		Size: 145.2 MB (145235685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:alpine`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:alpine3.10`

```console
$ docker pull rust@sha256:727ee417d7d59903c960fc3e33a24eff276fed201c03b4c20004ba17a8aa50b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:alpine3.10` - linux; amd64

```console
$ docker pull rust@sha256:548700dc20e801346feb16a19ab24dbdcba7f35a8b2135b8b739b1c46cb0b7f7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bbb166a3a05a41ada837eda4bbfa1273b3646f70d7f7c17bd9fbf65b656b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:01:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 19 Dec 2019 23:38:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:58 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bac046ab5c04d79d04b250c2e8a820c5109feb3adb8f29ce4aafedbe33628f`  
		Last Modified: Mon, 21 Oct 2019 22:02:43 GMT  
		Size: 34.0 MB (33983607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93ba9981241b8feb11aed98dc30689fcaee3cd2c3a03dddae4bb7ec8646965`  
		Last Modified: Thu, 19 Dec 2019 23:41:45 GMT  
		Size: 94.3 MB (94316888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:buster`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:buster` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:latest`

```console
$ docker pull rust@sha256:cc741b8685dbd7fb69b9722d6ce3086230357f65ae2413cb37610cc89d7fcfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:5552e3511864b93c1ab9479dfa26cd2953aea9151dc51faad11d6e90b149c06c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440931067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9510a0988d8eca7ce1de5be9ee2ea7e089e61baf8cb2aec1401b0a5a12e245`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:02 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4fb388fdfef16e8278fba2b06d46e48d152e1b40f4347c8828a04c8e2a87e`  
		Last Modified: Sat, 23 Nov 2019 00:18:22 GMT  
		Size: 192.0 MB (192044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b40cedefe7ccaa5f34bb9b164194e396cd366f56e9acfd4da7b9460335414`  
		Last Modified: Thu, 19 Dec 2019 23:40:45 GMT  
		Size: 128.9 MB (128911998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:9a2b764e7be271bbacbe0023f4d919c680135b4c064de72e5d63b0a85dbed675
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393401526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbde976dd227f24d3e159b7bda41c7a4840cd2bbb84b0a7cd744aacf272c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:21:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667e3c5fb3e6d562e5a25da025d7da9ec55d3acb9bd1da2d3d1e44d3f3c277`  
		Last Modified: Fri, 20 Dec 2019 00:26:02 GMT  
		Size: 115.6 MB (115558477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be1ee9d75e3cfc99fc096b92547f4dff383fa433953ef7b69d49e7bd5829c6e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416014283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f909636b59ed805d9048fa023cef42000026dce6f92159b948b251dd44eda15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:36:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682a08a83bc70508aee1decdfa525fde8102c9343179e1f3f7b1026849103a0`  
		Last Modified: Fri, 20 Dec 2019 00:40:15 GMT  
		Size: 113.5 MB (113530854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:55f83569d063d9d39842c9f743768b15744fdde6b116d0b356f3892263885688
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466648416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a653b9fddfa62365127bc0c4f1173f104a224d95c8257783e16e753173c45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:31:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:31:22 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f744e53ceea71bfe587a3cb7b27b0858f635c97019916b807a1064e81be120`  
		Last Modified: Fri, 20 Dec 2019 00:35:08 GMT  
		Size: 145.2 MB (145235228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:slim`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:slim-buster`

```console
$ docker pull rust@sha256:086cc72d824f3d61c6127e487370c76443e2d30eb345587ec42f20b76cf60836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:6afe324910ab55800745c84b0c307cf29fdb2426c0e01dffd9b539d53c558a30
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9bf3b5eb0052e075ce684b967a094eecddaaaf0421d42cda31609aa7f4e145`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:38:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:38:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdf0b7af867c9a9c9bb7e0daba56a44f5a4d4a5d6ee84c4053f52c862a6a62`  
		Last Modified: Thu, 19 Dec 2019 23:41:21 GMT  
		Size: 174.3 MB (174297702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:4509825341db94951d73f8f00e1ce9236bddc339ba5d6134b0fa234a5a990cb5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46c91c0e1e83437cf39acafcce0f9335e50cd1f7b6a1962856bfbfb6f4dad6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:21:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:23:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c1d1fb972c66a69dfdc8677cd71368aa0aaeaea626f61f3106a93796d4a84`  
		Last Modified: Fri, 20 Dec 2019 00:27:03 GMT  
		Size: 148.5 MB (148455431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2e2813c81f5254736b43b00a3fcdd6c5b773b34f825acafb67e89ed00aceab74
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179581890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c2752125026f0eaadf48463c82a069d40da3f204f2e7f630a5fffd569882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:36:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc3d3c6c299a7a4510235ba2cfdac2d0bb86d4599ef50c3a5c0f4dd4b2e9d`  
		Last Modified: Fri, 20 Dec 2019 00:41:13 GMT  
		Size: 153.7 MB (153731088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-buster` - linux; 386

```console
$ docker pull rust@sha256:7aea3b528eb618c14da085b239ba24aeb67597bb50d68403123b3e2afa7eb63c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222959508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba03ecb8d7f3a5303857a5238148100c12a11ed6dd38c905786bd8583e96495`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:31:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:32:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1dbbae2efa8ac8d4e1f4cc129484409feb2680f0ece672f541b1f280953f8`  
		Last Modified: Fri, 20 Dec 2019 00:36:21 GMT  
		Size: 195.2 MB (195212748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:slim-stretch`

```console
$ docker pull rust@sha256:18efb75eb413d196bbd64a8b4e49225653157e0652d5b824de25a6182f6a61c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:57c6607fec3c2bfebc517cb9c13321aee87cfd84bace6f53bddbb23c15452b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189328904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94d78b219741c33f7ca91069f2f418bd15960e08c8ac3f31be062ac60551fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:59:24 GMT
ADD file:2c1f5e08834f13ccb9c2326204eb2556e03239d00171e75755c7195289374c61 in / 
# Fri, 22 Nov 2019 14:59:25 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 23:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d599a449871ee73b960e80d176b989365dfecb4c8f337bf21e8853862403ee9b`  
		Last Modified: Fri, 22 Nov 2019 15:06:36 GMT  
		Size: 22.5 MB (22524572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a808f9be53ad3051a0da3ba8c2600cba69684fd510f3fc12d59be3902e4e890`  
		Last Modified: Thu, 19 Dec 2019 23:40:16 GMT  
		Size: 166.8 MB (166804332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:17cdc3b13dca4448f6ca6630e2fa70554f5333e468909f30ba12fb1ce44f6188
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fdab16188070657a517c3549752bd5d1f5f42f8fc52f6f03bda11a6438ec5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:28:28 GMT
ADD file:9fcbe16260f606fbea9a4811e693312434fbc4b300e974d33dcac84808f2323c in / 
# Fri, 22 Nov 2019 13:28:29 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:19:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:20:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d721220e5446968b6d6c8c3cd477d7deaadfd7f3ea7070342828f151408cbc93`  
		Last Modified: Fri, 22 Nov 2019 13:36:57 GMT  
		Size: 19.3 MB (19311578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077fd0c83889eaea5dd90c7a392ea4ecd5436249984f4c55814dfc60c741f0e4`  
		Last Modified: Fri, 20 Dec 2019 00:25:18 GMT  
		Size: 143.6 MB (143623330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a1ef6c8c6d5504d56fd9f67c866ace7ad1b26f02a11a3678ad971e163f9360ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164549005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048c98f570a1ff655c5340bd5b5c6c1c90783447553197e411d6ed34e205782e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:50 GMT
ADD file:8e4d0a1e6805c641fc9d18ebad82e4b01d85c6cb9f87d1ef47d75d150212a392 in / 
# Fri, 22 Nov 2019 13:45:53 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:34:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:36:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:98a64bf4db7d2219b4fdd8182188d9422810dee890e997095bfb564a0482eed6`  
		Last Modified: Fri, 22 Nov 2019 13:52:17 GMT  
		Size: 20.4 MB (20385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b832e63d71815acfddc8f292e3348c05ee1643280093ea87850ed9cf21a03df`  
		Last Modified: Fri, 20 Dec 2019 00:39:34 GMT  
		Size: 144.2 MB (144163246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:e1b852bfef4bc48288a30548993b4c1a3cceb5a53fb885a8bd2dc1ac23d43abf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210290510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705fa69680fec731459f5e53634dfd7d408fe33fad0538c7577bbd3a76983d64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:44 GMT
ADD file:19d04f738434c76e2dbd14b48de2f0f03afa883b15f638c6ecbbf382df03567c in / 
# Fri, 22 Nov 2019 16:54:44 GMT
CMD ["bash"]
# Fri, 20 Dec 2019 00:30:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:f26c9a85c76e393c9f2313b30e82d09f933d2dd4883620de242c7d21f8812e91`  
		Last Modified: Fri, 22 Nov 2019 17:03:03 GMT  
		Size: 23.2 MB (23152070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c37abc3a3e7a71d7e95e5889909b34c1611442441497e3702ffd17271460961`  
		Last Modified: Fri, 20 Dec 2019 00:34:01 GMT  
		Size: 187.1 MB (187138440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rust:stretch`

```console
$ docker pull rust@sha256:ed8271d153db3e91f34e59fd57602836d9f6fed919713d0b50b40cd8a96e6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:stretch` - linux; amd64

```console
$ docker pull rust@sha256:8799cee901791082ca011eae1eb30fd62166fee80f38284e46c28dc764f5cdf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.3 MB (454337046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5302f1b5dabd05a5ad5f9331511d3c230d2d4963c6e168f72857636e7beabf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:58:56 GMT
ADD file:152359c10cf61d80091bfd19e7e1968a538bebebfa048dca0386e35e1e999730 in / 
# Fri, 22 Nov 2019 14:58:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:12:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:13:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 23:36:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Thu, 19 Dec 2019 23:37:07 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:844c33c7e6ea19e3f6847e0667befdfb3ef02d6fc735b22c2d070261b6263b97`  
		Last Modified: Fri, 22 Nov 2019 15:06:19 GMT  
		Size: 45.4 MB (45380759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada5d61ae65dc038b4ba788ae5124c2587d0ebe83d3534733677216547b65cbd`  
		Last Modified: Sat, 23 Nov 2019 00:20:40 GMT  
		Size: 10.8 MB (10796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8427fdf429235414d0ea4757fd45fd81f09fd2ba3106e13796a8250f0a04a23`  
		Last Modified: Sat, 23 Nov 2019 00:20:39 GMT  
		Size: 4.3 MB (4340186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bafc4ab87c34cee7bfc43340fa7904dfe6d29a266537f2026cee3a76adfd`  
		Last Modified: Sat, 23 Nov 2019 00:20:56 GMT  
		Size: 50.1 MB (50065503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9577c0793430759082b98068eb2884638a34fa46ca481099e93cfc38d4ebfe`  
		Last Modified: Sat, 23 Nov 2019 00:21:35 GMT  
		Size: 214.8 MB (214841433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1501da54344da67a16aa924db62c0d8f2adda671b60360c046fa04bc9f6e6ba`  
		Last Modified: Thu, 19 Dec 2019 23:39:41 GMT  
		Size: 128.9 MB (128912240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:d96b561912fca37e28cba1a1cc054a03c9a922f070dd1cc0a24f6b56d8ef5820
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 MB (412996360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0928b78b0924d8c0beab12651c97f29861162804784dc2ce4974da728dff33`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:27:54 GMT
ADD file:3893b8a7336301b4a2a741f62c99805c3c7b2bee21e4f026b6885060becfc03d in / 
# Fri, 22 Nov 2019 13:27:57 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:24:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:28:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:18:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:19:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:fb827ed75ba2d760675c1e0dfd2cef27b5120725860abe8870ee3842dfce2a08`  
		Last Modified: Fri, 22 Nov 2019 13:36:40 GMT  
		Size: 42.1 MB (42108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fdca0c72a7ddca7b66d2c47a5de442518d8631adef3269a541a8ee1a1faec5`  
		Last Modified: Fri, 22 Nov 2019 23:34:21 GMT  
		Size: 9.5 MB (9497771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6508d4d51e15108ee995e92f1f1e2bbcec6c4c61ec1997ed246abe0b6504f316`  
		Last Modified: Fri, 22 Nov 2019 23:34:20 GMT  
		Size: 3.9 MB (3918760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8056142a63015026b87069d963bff11cd0de2fc98ce2e0d265c1eae3aaede`  
		Last Modified: Fri, 22 Nov 2019 23:34:44 GMT  
		Size: 46.4 MB (46390335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65472c61ccc368200b23f3c177b57530a446931fbdf7628ee668d699314e2a9`  
		Last Modified: Fri, 22 Nov 2019 23:35:40 GMT  
		Size: 195.5 MB (195522890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca2bec49b499e28e120e9d29d72bfc6b03dd5e9388fe93c299a328f6c51239d`  
		Last Modified: Fri, 20 Dec 2019 00:24:29 GMT  
		Size: 115.6 MB (115558535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:48c2253ccb471cb9ffdbb91bceffae245cceee86e04d23443a0cd0e86a23a4d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420789320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd1db3750013cde4e94a47ddc5130f2a253e21c99891e4e873e61d4c745f80a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:17 GMT
ADD file:ad8ecaf59c4f4c76dd6d93f5efff4420e3b55b36937eb36df317c7cd9ba19aeb in / 
# Fri, 22 Nov 2019 13:45:20 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:22:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:22:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:25:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:34:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:34:43 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c0d6add7f35c078f38df34ebc5a91afab0ba514167d17ad24fd4582eb0880bf4`  
		Last Modified: Fri, 22 Nov 2019 13:51:57 GMT  
		Size: 43.2 MB (43166306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616dd61dc37eac19d38cdbdf732659429ae37ba0d1578100f874fe236e25125`  
		Last Modified: Fri, 22 Nov 2019 20:30:41 GMT  
		Size: 9.7 MB (9747762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36da42882c170ff4b949c027b410428b5c0942632ed441a2f9a168a859ec0c`  
		Last Modified: Fri, 22 Nov 2019 20:30:39 GMT  
		Size: 4.1 MB (4094358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81386fcdc923e324fecbdb336d477691cc0be39e7e4e23ec733257ee50eddd57`  
		Last Modified: Fri, 22 Nov 2019 20:31:04 GMT  
		Size: 48.0 MB (48016405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6156b4a56fd4867da733a232b3da5a4312ee906bd7a09d869b3e3e026b36a5`  
		Last Modified: Fri, 22 Nov 2019 20:32:03 GMT  
		Size: 202.2 MB (202233068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd1ee4c6ce5c5845eb3bc8694b36c235eb904590d829c29e03a0beaaf54f461`  
		Last Modified: Fri, 20 Dec 2019 00:38:42 GMT  
		Size: 113.5 MB (113531421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:stretch` - linux; 386

```console
$ docker pull rust@sha256:87e02add0b10a4927341ab7f15abdc4f45531e5eb81a76080f471c786bc30d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478226201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee49388f75139020a8336510e62aa24d7e873bfcf01230bcdd133edc3088e88a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:23 GMT
ADD file:5c01b74109a8b04410a939b8bd31367bdef970268befe81e02e43ddc646d79bc in / 
# Fri, 22 Nov 2019 16:54:23 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:57:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:57:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:59:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Dec 2019 00:29:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 20 Dec 2019 00:30:10 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0f5940e26a4f3cd4f9002a93c11a8590498495bd0f4ce3fe102e4ddaf7c06d3a`  
		Last Modified: Fri, 22 Nov 2019 17:02:42 GMT  
		Size: 46.1 MB (46100192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536d6fcd65812215df48791595c7d5c60bbe22edb13d48f7c0357e62f65eeeba`  
		Last Modified: Sat, 23 Nov 2019 01:05:45 GMT  
		Size: 10.8 MB (10817095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc23bc091e68a62e274b04a4e8727ea5643f92492bd364f636e8bc810b330a`  
		Last Modified: Sat, 23 Nov 2019 01:05:43 GMT  
		Size: 4.6 MB (4561440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11260fd9d9f5ae8394485c75e8f285a441c5e66ef4fd756ebf2e595ca413cc6c`  
		Last Modified: Sat, 23 Nov 2019 01:06:05 GMT  
		Size: 51.6 MB (51586618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f02a75bb65f92aecb93cf402eaba19d0c711254da0845b5fc8d45679781c295`  
		Last Modified: Sat, 23 Nov 2019 01:07:04 GMT  
		Size: 219.9 MB (219925171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a31917e077d895d65f5e1c0a9ce0bb2d4e2ef1ff52af3308156bc48e4e7d2ee`  
		Last Modified: Fri, 20 Dec 2019 00:33:06 GMT  
		Size: 145.2 MB (145235685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
