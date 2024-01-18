## `elixir:otp-25`

```console
$ docker pull elixir@sha256:0df93640e24d0e826470af0535e929f95392a0f21046664d58146f2d641dbe83
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

### `elixir:otp-25` - linux; amd64

```console
$ docker pull elixir@sha256:14b770d55e5dd7318dbb785ad5d7efbb2ea43aebf501f3cc83abcceb8f62a68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.5 MB (578488879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0405c2029fab374b7bc73f1c4713a2fddb9e9db0dac2231a4a7457fbd91afa37`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24098c8d74fae9a314e70517566e785db7b39341cbc4bd63adf14c330728677c`  
		Last Modified: Wed, 17 Jan 2024 02:01:11 GMT  
		Size: 54.6 MB (54601537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6374b4ceb7a33a2609d9577d1f8cb5133e782949ab21f31086c1de775cb6843`  
		Last Modified: Wed, 17 Jan 2024 02:01:44 GMT  
		Size: 196.9 MB (196898503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9d5d71841bff9bbb1fe6e6005203e221df3c7570d7b72035e504ebb49ea13`  
		Last Modified: Wed, 17 Jan 2024 05:20:31 GMT  
		Size: 248.4 MB (248370358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4874407b4d04ad5015f989f93c814c6a6939436e553899cf7a58307c57170c`  
		Last Modified: Wed, 17 Jan 2024 05:20:02 GMT  
		Size: 198.6 KB (198604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d0043aa51837a025fd493e6d1810bba6197df91efa4c758d0873ce05ae403`  
		Last Modified: Wed, 17 Jan 2024 05:20:03 GMT  
		Size: 781.9 KB (781897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07948e4455a7dc20b86372e7875d1b73ebf12855720d8474f8bbfa7f45ec4b41`  
		Last Modified: Wed, 17 Jan 2024 05:49:06 GMT  
		Size: 6.8 MB (6815144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:1dfbdeb2f0c2d6eb26c6614748cc38a5bc0cb6bf4206533ae96a26e4b3ae5b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19563358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3678432a398f168158c4e4ee4fa8476d00cc06dd3c472ea215005a4b0f04e5f9`

```dockerfile
```

-	Layers:
	-	`sha256:2ecbc2e435f041a78e4bc0958ec06cde7ea94c6593735f8822c91d509ca0de7f`  
		Last Modified: Wed, 17 Jan 2024 05:49:07 GMT  
		Size: 19.6 MB (19552015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029596911f79d0ddaac630f80a4692d81a20804f6c1fd969551ad005ab0b2010`  
		Last Modified: Wed, 17 Jan 2024 05:49:06 GMT  
		Size: 11.3 KB (11343 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7b4462f25026c0765348f4db9a02410f7f3980ae913be1a9ba85b60191dbe561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.7 MB (513714869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63195e8bf4446cbe683d6b9ad629f07a8ec09d4e78ea3d746480989276e6fbb`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc92f863388ea7a660a09ac1581e426ed098ac1fe970d4ad13e7ac5a7d728ee3`  
		Last Modified: Thu, 11 Jan 2024 03:30:20 GMT  
		Size: 14.9 MB (14880496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45ae6e4109fcb63cfd59b29d1bc073059fb189aecab8d10de1468ec026aeae`  
		Last Modified: Wed, 17 Jan 2024 02:20:03 GMT  
		Size: 50.4 MB (50361413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c23fb1c630ad99b41c55ffc45c51811221b308683a461f9615d0788e64f9b9a`  
		Last Modified: Wed, 17 Jan 2024 02:20:44 GMT  
		Size: 167.4 MB (167381995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4a746c37948fd7b81464701b1c7934f5ba1143e885a74d206ad6a28cd287d6`  
		Last Modified: Wed, 17 Jan 2024 08:01:51 GMT  
		Size: 223.1 MB (223079743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb31248b831087fdb476c1b111337789e5c61ae8e2da7fbeaf03a097ece5aa3`  
		Last Modified: Wed, 17 Jan 2024 08:01:11 GMT  
		Size: 198.6 KB (198612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc385f377e1c10cab20ff35cc51cacdfb12db70ed9633b0ed4589867445e76f6`  
		Last Modified: Wed, 17 Jan 2024 08:01:11 GMT  
		Size: 781.9 KB (781931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d21b9e844447d9579811f9b8eb070f653ab06debc1e5ba7417c64e8908acb9`  
		Last Modified: Wed, 17 Jan 2024 13:07:07 GMT  
		Size: 6.8 MB (6815149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:bc2e0fd72bc17495a0e9aa4052c931b1ecf61516a8fc3c429210fd7e8540d3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19397684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b135a97d142a38d7d80eea4282c870e6bb617b865e917f6bfdac591837023f99`

```dockerfile
```

-	Layers:
	-	`sha256:d3b388a3512484ea52cec837fee7c8aa7531ab0f27d00466ebb8d96cc566ae39`  
		Last Modified: Wed, 17 Jan 2024 13:07:07 GMT  
		Size: 19.4 MB (19386280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed27b853214c413465842b39ae8bf623e0e1a2ac0b7e18e146ef0f967725482`  
		Last Modified: Wed, 17 Jan 2024 13:07:06 GMT  
		Size: 11.4 KB (11404 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:8448f6b592067fcf14af429107202cc515910fd4117552ad7eac5682539bfc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564237555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ffc271f1026bfe0b155401a945e02a7e100e4669e62de3de6c56d0a237821b`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd94a910a6d687fc7621b3af4657f78c1208a07fa463f30e2ed002dadb7e021`  
		Last Modified: Wed, 17 Jan 2024 03:00:10 GMT  
		Size: 189.8 MB (189834377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c025b7841bcd1f2cde1645510105f308272b001dc38220431a295550a17e220`  
		Last Modified: Wed, 17 Jan 2024 04:11:00 GMT  
		Size: 242.4 MB (242449063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048b8e398f59efa775e9f5f0e275d4e58fa20a4b4784c41a8a4410ae418da791`  
		Last Modified: Wed, 17 Jan 2024 04:10:39 GMT  
		Size: 198.6 KB (198634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d2b45ba981bfd56d58108261b9fd033875a87844c2a0bfe71127ece51f152e`  
		Last Modified: Wed, 17 Jan 2024 04:10:38 GMT  
		Size: 781.9 KB (781946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8588aca2a4d3a27a0755eee093565f84891c99dfac1bcb3338273ea18a8e29`  
		Last Modified: Wed, 17 Jan 2024 18:27:13 GMT  
		Size: 6.8 MB (6815151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:d3344e803f1b38cd5fa9a29a98f69e424599f34af9e6139533310e354cc3db3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19572034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f407d84f5a6a7a7357042dd79fdb15068269478ff01fa5a1d303fa106a578b4`

```dockerfile
```

-	Layers:
	-	`sha256:183ce4751c850e43bab990ab7ec0c125e19f52ee89ea1b2c2f0a68b6fa024a3e`  
		Last Modified: Wed, 17 Jan 2024 18:27:13 GMT  
		Size: 19.6 MB (19560683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddbccc2741cf42e73e4631c4364f4e24bb4265d53cc8c5a4e27232c146733107`  
		Last Modified: Wed, 17 Jan 2024 18:27:12 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; 386

```console
$ docker pull elixir@sha256:1537a556ddb377f39ad3cc592521346e231e499a6bba6b1ed387a3819a3cbe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579863903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d899fb444e6d39fc67d005994c4186630d6a6f41ac102ba90bd3b04afd1f4c`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:5ec37a8451203256eba8b114f21ff297f9b2e0b420ec7f0c50658a448ffc8f7b in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9b04188f89c4a7eaa549c59c16834ec81012244afac6c52196bafd2cd4486602`  
		Last Modified: Thu, 11 Jan 2024 02:43:42 GMT  
		Size: 56.0 MB (56046385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75db71c7ec6ec0e64a32b92dfa4a3127698f085f1df99e2c6187447f2433d41`  
		Last Modified: Thu, 11 Jan 2024 04:43:06 GMT  
		Size: 16.3 MB (16269099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33bceb83dc9fcc65d74c8e79da8ad46a7b1d7378b402830b29afaf04bd04df1`  
		Last Modified: Wed, 17 Jan 2024 01:51:38 GMT  
		Size: 55.9 MB (55939768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82eb38b7dd14b4951198e5118a540832cdd8e5d77970d1b72b7fa2e5578c545`  
		Last Modified: Wed, 17 Jan 2024 01:52:24 GMT  
		Size: 199.8 MB (199825169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d590a2e8d36f0ed439a87c2f48e6b4f954916b6cb6469aac9dc0d1418002c`  
		Last Modified: Wed, 17 Jan 2024 04:13:00 GMT  
		Size: 244.0 MB (243987784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7200ea79685daacd2a2f2c3b2ff65a6a8a4d0046c04a1135c2833285971b796`  
		Last Modified: Wed, 17 Jan 2024 04:12:15 GMT  
		Size: 198.6 KB (198640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b7284d425f9b7eded3f13239aa53d457d087f7ce1f6ca76723af2d56e21bb`  
		Last Modified: Wed, 17 Jan 2024 04:12:15 GMT  
		Size: 781.9 KB (781897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25c409dae779ea3243660129938bab20006784f81e3fd1085efd1582516993d`  
		Last Modified: Wed, 17 Jan 2024 04:49:56 GMT  
		Size: 6.8 MB (6815161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:16652b2254519264a1a5ae49fbce21502fe7b0cf85019d018079bac4daf743a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19551526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cf5b08d4403d81f701666caab84c9eaa03502d36e3a8764331b4bc99697662`

```dockerfile
```

-	Layers:
	-	`sha256:61e74c94a861b499e46df3a96c30e5b9ebf651f658cf0a5b9cac7f1bf7833780`  
		Last Modified: Wed, 17 Jan 2024 04:49:56 GMT  
		Size: 19.5 MB (19540207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f48865ab2a51fdaaa42f3c7cfc124491593732a72bc91b920b76124c07f494`  
		Last Modified: Wed, 17 Jan 2024 04:49:55 GMT  
		Size: 11.3 KB (11319 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; ppc64le

```console
$ docker pull elixir@sha256:03ad88a309845dd153069d124097d21da1ea900781405bb553611362d8a6a072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584408016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8458eca5028f6f4daaed2c448937559836b4141699984cf4c3101db0a1dca0`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e705cb61758280364899cd162b2510b2a119833c02f501318b83950af12d2`  
		Last Modified: Thu, 11 Jan 2024 07:24:33 GMT  
		Size: 16.8 MB (16767158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145205e451151b6f00222d734b41542a45ff000be2156f6dbce151466b7f0645`  
		Last Modified: Wed, 17 Jan 2024 03:25:51 GMT  
		Size: 58.9 MB (58874243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1556eebd2a6ebc2c0ceb94060d683a42d2497130a1a12ddf85649f866bab40f8`  
		Last Modified: Wed, 17 Jan 2024 03:26:27 GMT  
		Size: 196.3 MB (196277746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d5881bb06acbf5bd465293a972003e02c30507b0778b0931df27f08c6097c6`  
		Last Modified: Wed, 17 Jan 2024 06:57:14 GMT  
		Size: 245.8 MB (245763506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b329b41ae41e9f15f1b7f036b933030f8f7427d011a611f4bfc7964b1c6dc`  
		Last Modified: Wed, 17 Jan 2024 06:56:39 GMT  
		Size: 198.6 KB (198617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa1d9544c72cd9597104e5db5096bb3b80db0dd5367b972bd079e07449ae9ea`  
		Last Modified: Wed, 17 Jan 2024 06:56:39 GMT  
		Size: 781.9 KB (781897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694b302b730ad4f5672631ff01083bcbef9f57c77e3f9c26001eb66745216b5`  
		Last Modified: Wed, 17 Jan 2024 13:52:36 GMT  
		Size: 6.8 MB (6815187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:5f925d2a4a9386f11df5604bc3b8114146bb36f808e51511ef1b4a63db376257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19525728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db0131b5b63cac50ea6bf69fdcaf99297b61d7727dd2d1cb17d887af2339e14`

```dockerfile
```

-	Layers:
	-	`sha256:533a578087011026f833e0f308e205cf5857e685b0388cb401e78a85d497aa3a`  
		Last Modified: Wed, 17 Jan 2024 13:52:36 GMT  
		Size: 19.5 MB (19514353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c6e547029b85c4e2d1f1335187d46fdac1ba7e17423ce2f5406f50ec6f5a20`  
		Last Modified: Wed, 17 Jan 2024 13:52:35 GMT  
		Size: 11.4 KB (11375 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; s390x

```console
$ docker pull elixir@sha256:e38383a451eb9988e10cee05f59e2d8df0095eec5da9d980c773680ba8cd6619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539187298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591f903fcad0d053a840919f2dc91c91e4242ce059be36d2907b722fa83d2f1`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d30f97393df8af87413ca6aa015986e13ab489522ffe9a065961b2ed0f9352`  
		Last Modified: Thu, 11 Jan 2024 02:22:01 GMT  
		Size: 15.6 MB (15642723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59822891147cf801aabc1a3824089c8385793e177e1610b0c14dfb8ccafc4934`  
		Last Modified: Wed, 17 Jan 2024 04:04:21 GMT  
		Size: 54.1 MB (54070709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d393636eb45ce9c7153873b9a523d1c13aae090017d8089b56b8da8e16645`  
		Last Modified: Wed, 17 Jan 2024 04:04:47 GMT  
		Size: 172.9 MB (172919632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c167289739c7d2d9d6cd1bba2e03b2b1c52378cdd5816b27ffa70e191a887481`  
		Last Modified: Wed, 17 Jan 2024 06:13:17 GMT  
		Size: 235.5 MB (235462510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508e408c6f6fbbf4bd1d2492ee1ba5a9f64ffa010ba9d39e93935407692c9dbd`  
		Last Modified: Wed, 17 Jan 2024 06:12:49 GMT  
		Size: 198.6 KB (198633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17de8a264a13b860a2a718acfdab5d20c66f40719376e0382db6e629d770c97`  
		Last Modified: Wed, 17 Jan 2024 06:12:49 GMT  
		Size: 781.9 KB (781897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a26c8c86c5b4cb7e55e1d7e71a594b61952af7aa2889040132a4cca1c862c54`  
		Last Modified: Wed, 17 Jan 2024 23:15:14 GMT  
		Size: 6.8 MB (6815069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:ef68ec54e8529e4e7ab4e3aa93d010c1ee4c6bf5146ec1cd099dbdb67508f527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19378047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783fbf1570afaa2e3d10b63a8c2791a0aec0231c7adb9d215c8387a23b11e933`

```dockerfile
```

-	Layers:
	-	`sha256:292fe52d26f38d8fe52e531737d08ae812a059a62e94e126860b52c5ae2f746d`  
		Last Modified: Wed, 17 Jan 2024 23:15:15 GMT  
		Size: 19.4 MB (19366704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee18c770685ad3ed62a2a4105d48a05a0bc76c8b14837a9e4b22cc391660d21`  
		Last Modified: Wed, 17 Jan 2024 23:15:14 GMT  
		Size: 11.3 KB (11343 bytes)  
		MIME: application/vnd.in-toto+json
