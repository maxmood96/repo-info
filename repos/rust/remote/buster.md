## `rust:buster`

```console
$ docker pull rust@sha256:da006b598fcd53322aa78dfcdd4ccb5de7fd96c1514d02e75760de90a1fe8fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:buster` - linux; amd64

```console
$ docker pull rust@sha256:4928ae58a5c2eab27dbae294f3cb7fc0b6e0f04575de58597ca6494b501c693b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487989700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402d011ebda78d48ba33da2dc12282a7779e152f5a08b5ce01a15a04315e023`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:41 GMT
ADD file:c865da7afcf35b5a9538e63633f7e99ae4c40933cb8a0235e9704713042fba66 in / 
# Wed, 21 Dec 2022 01:20:42 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:16:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 11:16:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:17:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:48:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Wed, 21 Dec 2022 12:49:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='48c5ecfd1409da93164af20cf4ac2c6f00688b15eb6ba65047f654060c844d85' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0e0be29c560ad958ba52fcf06b3ea04435cb3cd674fbe11ce7d954093b9504fd' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c7c50787e2da71205402343dd1233b3ca6ebe70c7e790f6ba7d856b81b893200`  
		Last Modified: Wed, 21 Dec 2022 01:24:55 GMT  
		Size: 50.4 MB (50448893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff359114acb7d843de09375f87669fffb0abd1125c16f96431bc3c4173b48f8`  
		Last Modified: Wed, 21 Dec 2022 11:22:32 GMT  
		Size: 7.9 MB (7859309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821dc261e045ba09851c52ed28be3b9ecc9fe8c923fba05854ab0fd2fa38ceca`  
		Last Modified: Wed, 21 Dec 2022 11:22:32 GMT  
		Size: 10.0 MB (10001385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790459d63d5fdf148a092f1857010796dfa217329491b66a015a40de92f3db9`  
		Last Modified: Wed, 21 Dec 2022 11:22:48 GMT  
		Size: 51.9 MB (51869572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09b016fff62bb8002f99d7e639c0a2c0ce5a774796aae1e446e99deeb1ac01d`  
		Last Modified: Wed, 21 Dec 2022 11:23:22 GMT  
		Size: 191.9 MB (191892695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec64f9be817c10f2561df8889ad9b5e2b2f07643d2c2808669064ac5f9feeb5`  
		Last Modified: Wed, 21 Dec 2022 12:51:44 GMT  
		Size: 175.9 MB (175917846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:49d73d228c87660414421ff7731a06341a016242c8dbc7a7d88bed804e70ccd0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.8 MB (472785091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413e3e444e21f1fc11328c8e3187ec552b7ae416f311623298417b533c4e0a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:37 GMT
ADD file:aeeb7c51d456bb161dca543eacf9cf356a7b5ab0505401ec5a04b590a09353eb in / 
# Wed, 21 Dec 2022 01:58:38 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:29:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:30:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 16:47:37 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Wed, 21 Dec 2022 16:47:55 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='48c5ecfd1409da93164af20cf4ac2c6f00688b15eb6ba65047f654060c844d85' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0e0be29c560ad958ba52fcf06b3ea04435cb3cd674fbe11ce7d954093b9504fd' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c6063743b06c86630fb56f8ff5fab94f69ee547fb713805d49d9a99ed6ed8b52`  
		Last Modified: Wed, 21 Dec 2022 02:05:34 GMT  
		Size: 45.9 MB (45915614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759517224594ae5ac12414b070002578f41404acf8f575343f0c567f65000c77`  
		Last Modified: Wed, 21 Dec 2022 02:39:20 GMT  
		Size: 7.1 MB (7147847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5260ca8282e3cc7c3555d566866b390494e7bd2a7d9f221d67bc0e59a796c9`  
		Last Modified: Wed, 21 Dec 2022 02:39:21 GMT  
		Size: 9.3 MB (9348911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10232c2fbb3336070671d9a9a9ba6bde9af810a535d5358d6b00aa5f6acd69e4`  
		Last Modified: Wed, 21 Dec 2022 02:39:40 GMT  
		Size: 47.4 MB (47397355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52bf348a48fb30073b35aa3333ef2eb2ec10c91f6d9ccbb1c4330524bf23fd6`  
		Last Modified: Wed, 21 Dec 2022 02:40:18 GMT  
		Size: 168.1 MB (168090499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d0656e8f5b91c3308eb769cb3cbe5b0459da3edb6f37e49d9c5d15d8163aa`  
		Last Modified: Wed, 21 Dec 2022 16:51:33 GMT  
		Size: 194.9 MB (194884865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:47da7e44830cad1ffb3f7e8da29c38599f6df1228d6a4804fcd9e441bf91ab1a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529217540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304e1154588c39d9548d3e99cedcd5f611da57db62b0b859da2742a53ea68c42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:54 GMT
ADD file:2129940567ffc1f6fc724b59b8ab1f337db54cd9164e50494822bcedd46d85c7 in / 
# Wed, 21 Dec 2022 01:39:55 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:07:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:07:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:08:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:55:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Wed, 21 Dec 2022 12:56:07 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='48c5ecfd1409da93164af20cf4ac2c6f00688b15eb6ba65047f654060c844d85' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0e0be29c560ad958ba52fcf06b3ea04435cb3cd674fbe11ce7d954093b9504fd' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:ebd367421c805cd84d245a61615aeaa29bb9c2fdbdb111a373ee13b9934d9cf9`  
		Last Modified: Wed, 21 Dec 2022 01:43:31 GMT  
		Size: 49.2 MB (49233817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2a650584f22c4b0b1ceb1f2afaa0462e3ae41ecb07c7cb82d338e99fc3a9e5`  
		Last Modified: Wed, 21 Dec 2022 02:13:37 GMT  
		Size: 7.7 MB (7727254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4859d8b8d8b84e5f11d435628f9c17fbbf42bab8f1e960e9142d545c44a21c`  
		Last Modified: Wed, 21 Dec 2022 02:13:37 GMT  
		Size: 10.0 MB (10003411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9601af78fc4fcd830dac782c2beaea046f8ff4f93fe94827fc2b7d4c3f7c07c9`  
		Last Modified: Wed, 21 Dec 2022 02:13:52 GMT  
		Size: 52.2 MB (52191098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776561d3fe9638d512b8baba6ecda33d0a2c17a122aec3004d37c4a3bd2488c`  
		Last Modified: Wed, 21 Dec 2022 02:14:19 GMT  
		Size: 183.5 MB (183456433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c147664f32f660635010d383fdc7e5c86cfd3cc890280af39e1f111cdba880`  
		Last Modified: Wed, 21 Dec 2022 12:58:56 GMT  
		Size: 226.6 MB (226605527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:74ef3a8d7cec04238bc4c845639520ea0f0b059ea75c98fb224864fa3e4128f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.7 MB (510738137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7e575ef152f449b11479c317b8f8a3310d94365f7efa1d20925b2123038017`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:32 GMT
ADD file:761d50db794e5887a7dd528cff032401788413ed374043f8995fb4370f61a175 in / 
# Wed, 21 Dec 2022 01:39:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:54:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 09:54:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:55:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 21:40:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Wed, 21 Dec 2022 21:40:32 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='48c5ecfd1409da93164af20cf4ac2c6f00688b15eb6ba65047f654060c844d85' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0e0be29c560ad958ba52fcf06b3ea04435cb3cd674fbe11ce7d954093b9504fd' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:e8258458fa95364a2e7bf12aba19bd9fab7ebbb3144d9ff63b54fe3bdb605cc5`  
		Last Modified: Wed, 21 Dec 2022 01:45:08 GMT  
		Size: 51.2 MB (51207743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00a8f013f9cd8ac22f5327c59808641022657a0cac2bdb1c3eb73b487c77a33`  
		Last Modified: Wed, 21 Dec 2022 10:01:30 GMT  
		Size: 8.0 MB (8026073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5069b3ddc6d943d5145605f59b1624a8f00ee9deac834aea81d071c2cd6a16e`  
		Last Modified: Wed, 21 Dec 2022 10:01:30 GMT  
		Size: 10.1 MB (10127974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e12615e464affd32d36088dfafa685d0ceeef3ec6a1d077f00765fbf68bf4a`  
		Last Modified: Wed, 21 Dec 2022 10:01:48 GMT  
		Size: 53.5 MB (53472284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93428f4a3ddb4d157e185de9eec6d1d61805335ffc7846c35dad5bc953f5274`  
		Last Modified: Wed, 21 Dec 2022 10:02:20 GMT  
		Size: 198.4 MB (198431621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caecb609507d7d94e9013c8256fe5bc27ebaee68582ff89b973a4efc68f95c37`  
		Last Modified: Wed, 21 Dec 2022 21:42:20 GMT  
		Size: 189.5 MB (189472442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
