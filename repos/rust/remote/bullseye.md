## `rust:bullseye`

```console
$ docker pull rust@sha256:9410911c6006cf53ce6669c464570097eeadf1a2f2243a702d0fdbdb56baad5c
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

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:e6d6b30cc542e783d7c99f59c4981a1dfc16854065004dd2031731c1f39bde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500031479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcad364931eede82edf28ce9a8b0d641d449dfc7c66a5409117906b6b6b8b4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e29bc91fb60d9860548fd0c66a11e7a14b5e9417059fd06a35fb120d542ee0`  
		Last Modified: Wed, 24 Apr 2024 04:22:47 GMT  
		Size: 197.0 MB (196986464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534d57e3d7c23ea864729859cd9639d95758dc80d3fae7c2f1a781369374f72c`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 177.6 MB (177591486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:394674afd531ba7ba75772c582acf4520d9dfde25713860cf929548250230b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd227c9c6937e47e8c7124353322fb9c95d173d5e40454385bc62a5de0a4d204`

```dockerfile
```

-	Layers:
	-	`sha256:5175f4542d292457f1a4530967191286a12c21391a2bb9a183579ff56267c300`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da52b512eddefa1c1ecbaaa573257018e0b1790c5832c459900ce53606e1b2a`  
		Last Modified: Thu, 02 May 2024 17:53:16 GMT  
		Size: 12.4 KB (12418 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:09772a5759e8f44e647e203bba36dada6bae0ec51b4137b86c102104140d9604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.6 MB (491551070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837642bb5169d29595bf617d0d66300a58fd4acfdf2e25d0304cbc15066c5c3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f8222c355674e8dcbc3894b4612a6d53d2a526eb1ca3123325ac52c24eb3c`  
		Last Modified: Mon, 29 Apr 2024 19:42:54 GMT  
		Size: 208.6 MB (208612599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:eabc7d8d1aa11e2a798f0a513678d02fbde1208f53cf865542636297d3321eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14788669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c613f0f4f6239721d2511e05b7dea7e3e7627e6a5aaf9e535af255be2ae73843`

```dockerfile
```

-	Layers:
	-	`sha256:df8358c0982127fcda7d4ecdf92fda27992cf53c85830d6189d61a49c138427f`  
		Last Modified: Mon, 29 Apr 2024 19:42:50 GMT  
		Size: 14.8 MB (14776844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e955a20148c0101ba190f991bf71c5655176cbdafd4fe1babb24e73782d2c290`  
		Last Modified: Mon, 29 Apr 2024 19:42:49 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bae789c4c5a3f2c67c842d178fe93985ededc36dfa596680f2c3258eaa99eeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555715472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5b3b472b343bb28cded3b51bbc3695508b34e33438a76d46a200655dfa37e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea323986e6ac9a4ca87d66042184aa1ca12118a8786a96c9a26b4c6aef5397`  
		Last Modified: Tue, 30 Apr 2024 06:25:13 GMT  
		Size: 241.6 MB (241616563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23a8d2798abd1b9debf004fe2b2450e719db220af81d0eb4e05f35b303c82e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983787e80bcf8ed33c05d8cd89524aa6d5ea43d76c70a5a775efdf5011beac7d`

```dockerfile
```

-	Layers:
	-	`sha256:e9c9a0b626dd92761d2e9e7cad25bd5e6e166081a119ba3e0b033d59c1bb0a05`  
		Last Modified: Tue, 30 Apr 2024 06:25:08 GMT  
		Size: 15.0 MB (14977411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce844fc091a0b6afb17ec3c83a667071efcba9b449436cc6b4dd405f277fead`  
		Last Modified: Tue, 30 Apr 2024 06:25:07 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:232c18232dd7076711f3603df35b9bfe483c49663e03b9259edbd30810dfc02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518766287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858075fb8a3b54656c0ee7518ef0b22601a2d1b7d4d1f2fd037699198b2bef9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:32:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df053a23eab4180eece3d17162346216b301343de9fb6226cd226f21702be82f`  
		Last Modified: Thu, 02 May 2024 17:53:36 GMT  
		Size: 190.6 MB (190599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cf1fa86ecf03dd1fbb4dcce34d4a6d575a64d018570476a025626d21108bf3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056775c2d4a3ef6fbace0e34ff6db97f0f12ad062f8875c69193a8f497145ad`

```dockerfile
```

-	Layers:
	-	`sha256:189cacbc159513dae1c96778228fcacb8fa5341832b01271f051b1124b140d81`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86ac21aeb5f940ce0d749c02477c27d23e1023a107afeb492eedaa85b35f6e8`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 12.4 KB (12389 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:74f6d27411b0fe1655b74893221edde39cc79b5c54f779b8f924d0f94e5b6ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518096210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655131ce8b88722fe88822b0323c0f901ee374ed6e1eb86f90e53c8a0f1031de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f315af7fc149bdbb645add44aaef365e14662b9bf33a24ebcdeda2ed49bcef6f`  
		Last Modified: Thu, 02 May 2024 18:07:04 GMT  
		Size: 187.1 MB (187143092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02041686275df55e6c1cde2ab50a36777b23e5f0bfa0620bcea85ce288d8403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14954340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14dc83c058acbfa6bd18b2ba83506e0f719407a324008942f86a2d4dcc87af`

```dockerfile
```

-	Layers:
	-	`sha256:ce1abb7d3006b3e51d88e3b055b4055bbc25212003172c9a9aa9532a8425ad91`  
		Last Modified: Thu, 02 May 2024 18:06:59 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c168268955e9148deab9bdffcc4c0a75e9a8cea798c2286a9aab8cdf5599398f`  
		Last Modified: Thu, 02 May 2024 18:06:58 GMT  
		Size: 11.8 KB (11793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; s390x

```console
$ docker pull rust@sha256:378cf7ec7c2910088689170050d91dbc9836c6dec6041e5eb31549e2dda6f08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.9 MB (550928317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e271b8777d05d94ac2885ecad0cb3087f3c180f1309a816a866af33f6f7bce1d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b03fc91e909bfbc0df98ad158a10a95a51a16ac44385dfb4b926241ed3e0a10`  
		Last Modified: Mon, 29 Apr 2024 19:34:21 GMT  
		Size: 254.9 MB (254877310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2c2bf74ad6d990d6dc4a61e43e7e47e917a01a3a127b8a9f72def137f726d5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14808368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67fb63953c1a48170eda2497ba62d7f12a01688e476ea7bb56bf9ea5be2b813`

```dockerfile
```

-	Layers:
	-	`sha256:fc42addd4f13febee274d98c3caa451b68e9715d7791521c706a2a1484387e11`  
		Last Modified: Mon, 29 Apr 2024 19:34:14 GMT  
		Size: 14.8 MB (14796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc62098780cf85cc61bedca6a7dec2a8c7fc104ec55e9c4ddd2ce6ebba62c13`  
		Last Modified: Mon, 29 Apr 2024 19:34:13 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json
