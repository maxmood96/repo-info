## `rust:1-bullseye`

```console
$ docker pull rust@sha256:946097c1915b456095e54ea1c68ec87d45503ebc1a11da6ed3bc66c772736c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:a2208140d9a7a5f38c3652a965e48a66fedfddd818390e3773d90d4cd0d97ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (460984949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf8404d24739e4d6c05d585a3797b2ef79b50c687dc89a90c71884bc8a5c20c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:48:53 GMT
ADD file:32519b03930d9f5db9010ae49e0987322ce19eab681ad5c841fe1cd6268ad2ee in / 
# Tue, 30 Mar 2021 21:48:53 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:00:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:01:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:02:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Apr 2021 19:07:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Thu, 01 Apr 2021 19:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:6abc78d8e2422868f293b265b6c0ec3ba250fc4987f862ba05e86d7eb277f297`  
		Last Modified: Tue, 30 Mar 2021 21:52:53 GMT  
		Size: 54.9 MB (54868089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1424cff1d2b47e24acbeb3381319a9bbefd1f8dcae5c521f0198833d9b2911ec`  
		Last Modified: Tue, 30 Mar 2021 23:12:47 GMT  
		Size: 5.2 MB (5151423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859f37c645b9a1a4967007d3e310ace7f83d9924b7fd77385ff9e2de20a55a5a`  
		Last Modified: Tue, 30 Mar 2021 23:12:48 GMT  
		Size: 10.9 MB (10867143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f1dad4b787cfa0293818e7bb90048de585a8c37b12fab90dc184d527078652`  
		Last Modified: Tue, 30 Mar 2021 23:13:10 GMT  
		Size: 54.6 MB (54565465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36c31cee26847b9913a77e1631113701b54672f1892eb370c5ec4db2b9da2a`  
		Last Modified: Tue, 30 Mar 2021 23:13:50 GMT  
		Size: 196.4 MB (196360959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c0ad408e7a047f76a469f366e091fe75821ea50cc22f25b8d713a09ab541e`  
		Last Modified: Thu, 01 Apr 2021 19:09:19 GMT  
		Size: 139.2 MB (139171870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ed818f2ac1ddd545e3b1d71715824ccef89db39b50e04b9b69b4b4d6f40576a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 MB (459232429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9c175b88b09e767aeaf1250f0e227dd94fc9b5afe207e927739020483654b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:58:24 GMT
ADD file:5e17f4d5cdf1ff091554ccfa33e22ab2be0c278b0cec1c11b45333deda2cfc79 in / 
# Sat, 10 Apr 2021 00:58:24 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:01:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:01:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 06:02:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:04:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 17:23:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Sat, 10 Apr 2021 17:24:25 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:df95183d3a18fe92c278757657c6fef8fcc11f2a9a578df2f2b00dbccf0a8ea6`  
		Last Modified: Sat, 10 Apr 2021 01:06:36 GMT  
		Size: 50.1 MB (50070347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d156c39bdbf88c4fe691e2b8db9d8884ace98a295e72db7f8f2c7a7b09d88301`  
		Last Modified: Sat, 10 Apr 2021 06:18:29 GMT  
		Size: 4.9 MB (4920554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5c1a00fb4cd0a81f72ea5458a8eb52ee825d2ec64b5b3d6324e8fe844eed2a`  
		Last Modified: Sat, 10 Apr 2021 06:18:30 GMT  
		Size: 10.2 MB (10218022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f63a9b9b58ff5c896075723b17ad5cc2bd3e1daada4e1379a89a0b57120ce9`  
		Last Modified: Sat, 10 Apr 2021 06:18:54 GMT  
		Size: 50.3 MB (50328298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1bce068d2d60caec9dd5bb24665ccd9551dac38a7bb9816b617ad204c7c847`  
		Last Modified: Sat, 10 Apr 2021 06:19:45 GMT  
		Size: 166.8 MB (166833103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5eb15e1cf6364587642cccd6273d59f3e549e07045c489f4add5c5ec204a28f`  
		Last Modified: Sat, 10 Apr 2021 17:29:13 GMT  
		Size: 176.9 MB (176862105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cd59e54d284ce249a7e0eea0df73b51f5a55c5b1ecf80f59876ca907af62ac2e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.5 MB (500527202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ef28ba95ce82e5eceebd3481fd306b18ed51917b07d767fea04874e8671135`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:14 GMT
ADD file:e1b7ed0c35932136d6c29369c3eb387896a482b3b227f18462715ed1690af4d4 in / 
# Sat, 10 Apr 2021 00:40:17 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:45:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:53:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Sat, 10 Apr 2021 16:54:09 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:a5ad85c1142d6ba07dd2031cb0c6c7513422a29a4e0446b232121280077ee9eb`  
		Last Modified: Sat, 10 Apr 2021 00:46:54 GMT  
		Size: 53.6 MB (53555409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cf7b2e11a6c2d24640e32bab162f44730583fd12321a0b43f568de4528c6a0`  
		Last Modified: Sat, 10 Apr 2021 01:59:38 GMT  
		Size: 5.1 MB (5140721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da257970ac9fb41c862a9ea5857f77aa158778d568d6766498b801a239be01e`  
		Last Modified: Sat, 10 Apr 2021 01:59:39 GMT  
		Size: 10.9 MB (10867421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607f59eaee90bc16e7091c941cb4640481bec283086c165c038bc666c6072d4c`  
		Last Modified: Sat, 10 Apr 2021 02:00:00 GMT  
		Size: 54.7 MB (54666062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae24588640368910d2900b49106d27554747510bc30c3ae59f30d00d21dc7a6`  
		Last Modified: Sat, 10 Apr 2021 02:00:51 GMT  
		Size: 189.3 MB (189251974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f16edd7590ce7a5571bca5f963af88e69de13d470fec1976734e48fe230eef0`  
		Last Modified: Sat, 10 Apr 2021 16:59:36 GMT  
		Size: 187.0 MB (187045615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:2217c8d46a995b0fbaf27cc688a95396ff3c6a1ccdc98372578b276a356f595e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.1 MB (502054109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f71b9cd875b7880c32e778d1697dc69508f07976655f33c9dac265e1cb2dbe6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:38:57 GMT
ADD file:72806e483423c962f867acf22783e8b91aa9d8486d1d35505eaa5442df41be57 in / 
# Sat, 10 Apr 2021 00:38:58 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 03:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 03:15:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 03:16:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 03:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:35:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Sat, 10 Apr 2021 15:35:55 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ed7773edaf1d289656bdec2aacad12413b38ad0193fff54b2231f5140a4b07c5' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7a7b9d246ad63358705d8d4a7d5c2ef1adfec24525d1d5c44a7739e1b867e84d' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='f80a0a792b3ab905ab4919474daf4d3f60e574fc6987e69bfba2fd877241a8de' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='4473c18286aa1831683a772706d9a5c98b87a61cc014d38063e00a63a480afef' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c73c775bc05dae13d9e00c5c3e6660d213997be492a06abcfe494e5fbfe97f21`  
		Last Modified: Sat, 10 Apr 2021 00:44:36 GMT  
		Size: 55.9 MB (55881380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e0bd737226fabb79b27a428df2d8a89fad1d3d4380eef8f36ab1540f975ac`  
		Last Modified: Sat, 10 Apr 2021 03:27:53 GMT  
		Size: 5.3 MB (5280440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93fbf8ae86f8ca0c477fd1e852305a2a6b5b121a2a0d8a6c785ab27d113805`  
		Last Modified: Sat, 10 Apr 2021 03:27:55 GMT  
		Size: 11.2 MB (11248838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e044730d7057c92a5b5235d54b58ae32454dfaf5781ca5e0f7dd728dae5dfe2`  
		Last Modified: Sat, 10 Apr 2021 03:28:28 GMT  
		Size: 55.9 MB (55908848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b2bbe7701e35f9555e2edf50f6ad1859731da7bac0e4e679b1d4b15c24aa0b`  
		Last Modified: Sat, 10 Apr 2021 03:29:39 GMT  
		Size: 199.3 MB (199314675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592605fdb7519ab842ebd55f3c094e53b704eb8dd9ca78dba87c161740a37451`  
		Last Modified: Sat, 10 Apr 2021 15:41:17 GMT  
		Size: 174.4 MB (174419928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
