## `rust:1-bullseye`

```console
$ docker pull rust@sha256:ae411a6ed4812ea54668cf819566e950b162d59a94fde0fa298cf7bb400f6b3f
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
$ docker pull rust@sha256:68ad6598e881466006ae5f65e50411b5dff8910426cdb069dfa79b6713293d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.8 MB (536813083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a04e57076cb9108518cf5ccdcbcd0628388de7d31b5165f6653c1b6cac1290`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:46:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:46:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:46:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5942943df443b1bc1e709676d52a57b0a7ddee0c58a1602ecf5e2e8b271916d`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 54.7 MB (54743262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc88763ad50d1ab5c41218bf6aa5893d2c739925d42b6eb8f2c52823019e44`  
		Last Modified: Wed, 20 May 2026 01:16:23 GMT  
		Size: 197.3 MB (197307874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37a6001065504a669ded7e466887a139e6025ae92e6d6e1ff638fb7ced9115`  
		Last Modified: Thu, 28 May 2026 21:47:35 GMT  
		Size: 215.2 MB (215202237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02c68eef07aa9dbeb268db69a95fb9c57de117c4b1d9d39ddea116ea9fe11e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffca951ca0e485e4199e07390ddab559d0f52f40663d4dc69b5a4a2faa4eef5`

```dockerfile
```

-	Layers:
	-	`sha256:1ca0d1b9d4bc2ed52c2563c3515af8678e098f2ccf345e6b22bb6dc25675e22a`  
		Last Modified: Thu, 28 May 2026 21:47:30 GMT  
		Size: 15.5 MB (15473456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6b7841a91f542507d419fdc73364aedfd3556a32df19ce4ae78d9f304f4860`  
		Last Modified: Thu, 28 May 2026 21:47:29 GMT  
		Size: 12.5 KB (12503 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ee067a2375548bd5c2ae1a531dd17e4bd5984abc30c2f91b5ee3cd142cfb484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540133200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e9ffd5e802b7642e212a411a7a1fbd33fd511af66b5a1788e4c196db86386a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:14:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:39:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:39:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:39:31 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c303da1bd3f277cef3c251ecb02fe6ceb28404700c2776e5e52078361e0d5a63`  
		Last Modified: Tue, 19 May 2026 22:36:43 GMT  
		Size: 49.1 MB (49059808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6159604253fa0b585197db46cb3703cf956f0b1a4d8cb67a661c9f449e5220b`  
		Last Modified: Wed, 20 May 2026 00:03:11 GMT  
		Size: 14.9 MB (14905378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb581721ec88241b5b5ab6b082d3be5546d7889197d205126a49442b917bbba1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 50.7 MB (50659222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9412242c111ef7d371b4d7f9d3c50953090d140db79f045fca66bbc462846c8`  
		Last Modified: Wed, 20 May 2026 02:15:30 GMT  
		Size: 167.7 MB (167715549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f1c9ee670bac3df344ccc162c1c62460f03ec206c42b507fc228536fdf92d`  
		Last Modified: Thu, 28 May 2026 21:40:18 GMT  
		Size: 257.8 MB (257793243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ce698254b1649348873893dc7358aa1f3fcf5860d762a954e6a5c770c645bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15285382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddafe86aaaa41136405a6a36cd464748ab05d86cb7f213cae0f065eca8ad727c`

```dockerfile
```

-	Layers:
	-	`sha256:275d7ce20a20cd7c643ba0e19319846d8a689c4aa17fecfd5cb71aee26e8aab0`  
		Last Modified: Thu, 28 May 2026 21:40:13 GMT  
		Size: 15.3 MB (15272800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c212ec0d56c8d589ee29a3df0280c1e749708362196263a971b4da251818bb`  
		Last Modified: Thu, 28 May 2026 21:40:12 GMT  
		Size: 12.6 KB (12582 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:069f49365b1207eea9979d1c8f2683b1bf88a7aed292d03f41e0d69064d52e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 MB (493341991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf5f78af299e1fc81aae556031ca2ea556bd9aceb53ce58cdf87b2e88b79400`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:45:10 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:45:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:45:10 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a0e24f23d039a1a5ae21822bccb045bfdedf83da569dc13fb1992e903bbcb`  
		Last Modified: Wed, 20 May 2026 00:27:11 GMT  
		Size: 54.9 MB (54879862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5578d03844480631fb598cecf497312529f7e21642b612b605246de4df178882`  
		Last Modified: Wed, 20 May 2026 01:16:01 GMT  
		Size: 190.2 MB (190209386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b726e08abea616b4d6455f2a75364442bca15ff6ccad12f753fecba588cbe0`  
		Last Modified: Thu, 28 May 2026 21:45:50 GMT  
		Size: 180.2 MB (180221285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:78cd6477398f10bd7e25ad932f9eef060f8b0571e8cf4a7d74a728f8e3555fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1c9d198bc74b7ce63f1753f8cb31fc75799e624d3494902571c92175b2c0`

```dockerfile
```

-	Layers:
	-	`sha256:c9bf1b0847012e134643548528435bbddd55ab7b6383915c59e95f91c13a20fd`  
		Last Modified: Thu, 28 May 2026 21:45:46 GMT  
		Size: 15.5 MB (15475427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99f7f89ad4c85f9f7b3930eee298af0dedc55fc7347f36c02d6033921110f58`  
		Last Modified: Thu, 28 May 2026 21:45:46 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:00c7490a4c90395f534cb8cbf0ae91501d46f5fe5ee0921d1b0e9179009c3343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.7 MB (568712536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce89cb053c315c416e24b1389c6ad9ae97b78ecb13386dc55376f1ea0f3d79c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:02:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:39:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 May 2026 21:39:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.0
# Thu, 28 May 2026 21:39:39 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a100a514adffbab3ef3834e4740a809fc60c49ad1b434f56a2d8254524b75`  
		Last Modified: Tue, 19 May 2026 23:25:19 GMT  
		Size: 16.3 MB (16295788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f642862236d0c357dc4ae576bafd5ea8cfb669f7a55b517fc7627c3283f4b`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 56.0 MB (56046808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db8f3fbeb17a8bd13e4eb6de659e76a8e6c76fd6b0fd0a16a26b1613dafc13d`  
		Last Modified: Wed, 20 May 2026 06:02:56 GMT  
		Size: 200.2 MB (200154801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d94451a1456691ddcb6b8a09e790b95366bfd962f46996217daaee321d26b1d`  
		Last Modified: Thu, 28 May 2026 21:40:25 GMT  
		Size: 241.5 MB (241506089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:68369135ff03b9ef383d2a7fcbe4819776fb24b223a67757b3bca4eb67d835c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1af3893e44a99b8049895ecb8e4fd7db6ab9db606e160542280c64553b26716`

```dockerfile
```

-	Layers:
	-	`sha256:5114393069e486d25df527247d2cbfbe313473336ecbfb77223b6a43d42f3d8e`  
		Last Modified: Thu, 28 May 2026 21:40:21 GMT  
		Size: 15.5 MB (15460158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bf7db73bcc5128710776f4939d73f94342722e195dfe589bb2ede270e48dba`  
		Last Modified: Thu, 28 May 2026 21:40:20 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json
