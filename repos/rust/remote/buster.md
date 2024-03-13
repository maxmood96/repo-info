## `rust:buster`

```console
$ docker pull rust@sha256:8148f5150a2a39f7bb5a02a36e138bea7bf31f804de38db643cd8c6fdb21a0e9
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

### `rust:buster` - linux; amd64

```console
$ docker pull rust@sha256:9ed662412fb95345dccbe9c3bb257daf7b205837dfcea0a409626cf0266435cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.9 MB (491880879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081eef35f101eb0646f6ed6edb43993977006d1db5948f0edaa31d14f656fed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a275b8bae6bef10ec9dd71151b41617e72eac0780ecbfe93ee1dc86db2f5e9`  
		Last Modified: Tue, 12 Mar 2024 06:05:14 GMT  
		Size: 191.9 MB (191942628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c5faa10482ed6e72dcbf5a65d783af406ae3e40f344c59d124547d532e1cd0`  
		Last Modified: Tue, 12 Mar 2024 06:59:01 GMT  
		Size: 180.0 MB (179975287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:7e84328870cdfdb9bf42a455fe3218edba59525e45e6608ab9f787b679cbf505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15621470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a131b152f1cdc70484f706276d60890aa134418b5bdede3c6b4b023d9370d8`

```dockerfile
```

-	Layers:
	-	`sha256:09bc40bc3e9fd823d6f1e63f8a0d57384287b197f934be4b52cc5c7e74a35470`  
		Last Modified: Tue, 12 Mar 2024 06:58:57 GMT  
		Size: 15.6 MB (15609924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a649f7ae12d8f2544a0a3f36486e48bebbe5df6764ba9be2867dec101abca8c`  
		Last Modified: Tue, 12 Mar 2024 06:58:57 GMT  
		Size: 11.5 KB (11546 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f89e4a76491a6783119b3d09ddfce5d876ce8b5527486427ad8eca56eea9d24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.3 MB (494303140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1944b009c7fe3afb6e993de8efb3ae41a9a654df45139d032fe1f870a4d1e0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:19:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508c05504c73b82e0130fe371cfb5de03fef9bf8a98195962243261db202e8fb`  
		Last Modified: Tue, 13 Feb 2024 04:30:34 GMT  
		Size: 168.1 MB (168133783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc725116d31f6bc846467d8af0adcdc300f7c564160a832535688d0f66ff5d3e`  
		Last Modified: Mon, 11 Mar 2024 19:52:00 GMT  
		Size: 216.6 MB (216575293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:356dfec9a944b1d5ad851fd04e62d70d877cd7d6dc830e51447aa9895964d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5784649d1bc35e4d131a851e38e72771a15022b0cb6acc5f6698a61e11229c6`

```dockerfile
```

-	Layers:
	-	`sha256:1e28a72cd205aa783acde63ae7bba26755355fa7a9ccccba20a4a14dc2f1c649`  
		Last Modified: Mon, 11 Mar 2024 19:51:55 GMT  
		Size: 15.4 MB (15412073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52bc08ce1fb0421c0ec4e0baa5ef6811fd50827789e5d463b33cdb50981f79c`  
		Last Modified: Mon, 11 Mar 2024 19:51:54 GMT  
		Size: 11.6 KB (11616 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a70a8fd02f03423cb776fab07ae934567875acda58ab87fe38da89483082b2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.1 MB (552116234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36353ea825709da76e8ae2a2659ae6b3c791f81c0f211979d685693e1d6b8ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2dcd7c406630e333330f43f6e4ccd1e91b2f4df9cac14fab6eeb4d74e67b6`  
		Last Modified: Wed, 13 Mar 2024 05:18:36 GMT  
		Size: 249.6 MB (249628100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:0156e42efe0c126d7146f085a123c801e73538579905d0a7c54242d030db0de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27bd58b4e2041a633b880a5c0fb0c616749598ce7017df663c48f4a0fe59f52`

```dockerfile
```

-	Layers:
	-	`sha256:f30dcf761e829635fbb98012eea9ee8d28e9e1d5ad3b145ebc1184dd613e4417`  
		Last Modified: Wed, 13 Mar 2024 05:18:08 GMT  
		Size: 15.6 MB (15600784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844d73fb6ff28cce74a94bff0a4bd36b4453efaa5b9526308318729a384ed674`  
		Last Modified: Wed, 13 Mar 2024 05:18:07 GMT  
		Size: 10.9 KB (10893 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:2117c1b1c73f38913086f5e679dafa15aab3ed12307766074239f3d6537127e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514813761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc90cd11a8acce7f0e989376bf3d85099da7bbc19f08a245fc46e0fb366450`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611538514415c639eba0b1521fa6f33ff37569ea8882616480d31e1051e4242e`  
		Last Modified: Tue, 12 Mar 2024 07:57:06 GMT  
		Size: 198.5 MB (198491053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb4dcca6d2b982bd9e7a82cd81c8e3740830082e1c322600c74959d2ddfd668`  
		Last Modified: Tue, 12 Mar 2024 08:57:19 GMT  
		Size: 193.5 MB (193475998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:ad8e4aaf6996f112563c517cad99283b0e2388f82a47d590abf024d307a8964f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15627021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b54749c9a904d26b1d2cf65e3a32f4d6606265a8a7c3673e11301b33b25012`

```dockerfile
```

-	Layers:
	-	`sha256:7eb96ea85a10c588d9191c3a3b1990f36a7269c067ad2e77588fc5c880f57d78`  
		Last Modified: Tue, 12 Mar 2024 08:57:15 GMT  
		Size: 15.6 MB (15615505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1f2f7aaa708f0090368ff26aa000ec8c8aa6550313a1a635429bddc4e984de`  
		Last Modified: Tue, 12 Mar 2024 08:57:14 GMT  
		Size: 11.5 KB (11516 bytes)  
		MIME: application/vnd.in-toto+json
