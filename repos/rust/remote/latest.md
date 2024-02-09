## `rust:latest`

```console
$ docker pull rust@sha256:8e876026c9dbf43a12c2a15476a5d8f81cc41a56acbb975f04f859170fd0a105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:9bf8062398ef8c2cad01b29624dce55c90cfaba824682b093b88e2128aba7916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528369240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ca6875abb0d32622c96de43aa2c5d3b55c4a235256e716bb2dbcee0cfa95e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069ab9fbbda8d665751dae3953a8a28248db49aca5d8085ab60b35823b9e344`  
		Last Modified: Thu, 08 Feb 2024 18:51:10 GMT  
		Size: 179.5 MB (179481557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:13902db55ecd44406c011a1b954d2520a27d3dfba0f2d4fd2b6539e1ad732278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01522eb58ad17d9daf6f9fd87fbd81b70ee14a51ce69f8b2b2ab8982d71773e`

```dockerfile
```

-	Layers:
	-	`sha256:65bb084adbd3007e4725df4bf8c05da694badd50f81715d0a1e1bde00b30c6c8`  
		Last Modified: Thu, 08 Feb 2024 18:51:07 GMT  
		Size: 13.4 MB (13403323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa570dd56201024b2b85ddc56d1b7a9fc8ac4df17889a94db8e8734b4a23ed6`  
		Last Modified: Thu, 08 Feb 2024 18:51:07 GMT  
		Size: 13.1 KB (13110 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:d659e800007290f7e82b974cccafa6e19b946b2752d86d725eeaa5727e6e4848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.3 MB (517252981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287b3d2c55a5bef9237f92705ae1e9dd50b718b89229b4958fa1013ccc0527c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab65e8beb4237d6928b484e6d4fc9f0ebe2a13456ee82124924c2fd5021f6297`  
		Last Modified: Fri, 09 Feb 2024 07:22:33 GMT  
		Size: 215.8 MB (215822728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:93a95d74e1c514010c036f583bba089f41fb7fcd0c8a357210c1c88c0791e174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13246559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d0f2835beae4d8c4203278d4603ff5f3c7b32b292ad386ee36ec91db566019`

```dockerfile
```

-	Layers:
	-	`sha256:a209a5beb4c392985a8c79201fce5aefec07d7b78fa44aac0e30262c37137be0`  
		Last Modified: Fri, 09 Feb 2024 07:22:28 GMT  
		Size: 13.2 MB (13234010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb292f6a854406afc4143777e8e964ceb53be19531c60f3e4c3a2b42a3bb832`  
		Last Modified: Fri, 09 Feb 2024 07:22:27 GMT  
		Size: 12.5 KB (12549 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bcafcbe03b0bbe8b47558822b890e3d4824b80296e1de481b084315f477ae0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588749808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9e904947ce177670fa8d62afc3d0fb3c1674def200ab447b73875ecf8e4a89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbc7b993a7f777998eebd88e80609633c1378c64a47987dd228e797b62a8df3`  
		Last Modified: Thu, 08 Feb 2024 19:33:59 GMT  
		Size: 249.0 MB (249047307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:8474fd01400ab936188fe195637bb1441f623ed4a71fbfdaf82ca50271d1896f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13441024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1858330a27f742c87a5ce75a4aa5d89da6719d15865a8c1ef5c1dd602183c`

```dockerfile
```

-	Layers:
	-	`sha256:e35b9f1328304b399bfae725602730735a6a053213822b9660963dfe39c19829`  
		Last Modified: Thu, 08 Feb 2024 19:33:52 GMT  
		Size: 13.4 MB (13428559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930affed5108b491c8bbc470f1edda42062303d14943b96eac2fe9b106b674c6`  
		Last Modified: Thu, 08 Feb 2024 19:33:51 GMT  
		Size: 12.5 KB (12465 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:09bd823e4a93dd8f25a8b826fe1cb58eeb866184c2504df72dfcc94bb1f289d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.7 MB (544732773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4c8794c2f09c650bbcc484df2c226fc1a93ca5ae66670c83ae1501814d10b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5d662d773fea816c984a59d6fe934f5dcb9f01d11c39e790439b20ef367af`  
		Last Modified: Wed, 31 Jan 2024 23:46:03 GMT  
		Size: 210.0 MB (210044410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617affd707da68b40df0ade0e68526a82f896d6626e9e2fa5d274a4b71be494c`  
		Last Modified: Thu, 08 Feb 2024 18:51:16 GMT  
		Size: 193.2 MB (193207127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:30a84685999b1f9587b4d7984a3b32e044e6f27e18153cf058e3d93b37822c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13396792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557b14454139d1a73686b0dd1323515fb1a3f7c60b93b61ebde8679d54d7ece6`

```dockerfile
```

-	Layers:
	-	`sha256:0e17fa10469fd48e493dfa6b52d602b39ed846fb786b05a55931b316ddab3895`  
		Last Modified: Thu, 08 Feb 2024 18:51:10 GMT  
		Size: 13.4 MB (13383731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7da99d0f3ab4d76682f6a8e9af178d0d366dd21f6855978bef7d257bd0e776`  
		Last Modified: Thu, 08 Feb 2024 18:51:09 GMT  
		Size: 13.1 KB (13061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:be0d3d84f4e5e139f2a695d35feb8c3a1f1fed771ce21c4c982fd0e5846e0064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555962514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4be6c43b0eb0bb85da1cd2cca586fe8911f67a3fc6c49bf26a78f060967aa4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42b30e0f68312c85379c7a00171fe29113b00bf5bf04d13d4a0551cc284bcf1`  
		Last Modified: Thu, 08 Feb 2024 19:18:34 GMT  
		Size: 193.0 MB (192956777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:d4938db0218486f9cac9763e835ab9b132445d5f0b7945389ca5b61e1ff7482e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13395515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc4fb5a2cc97eda45cf1d3848536c90f93c91f8fe225ce9d8ba3ae9bfa7c5a2`

```dockerfile
```

-	Layers:
	-	`sha256:036a5d5f28b161db8df6d8d096d18ef7b5ccef689913365443f7c0c4ba8383e4`  
		Last Modified: Thu, 08 Feb 2024 19:18:30 GMT  
		Size: 13.4 MB (13383007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696c3ef4d83b60aa91531409b3ad1c901e0afc6b8081dbd9661051aa7007ca3d`  
		Last Modified: Thu, 08 Feb 2024 19:18:29 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json
