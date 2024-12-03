## `elixir:otp-26`

```console
$ docker pull elixir@sha256:699a27ce90800cfbbae80850b5596f91ca864506f43bf1958b75d032b83b4e76
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

### `elixir:otp-26` - linux; amd64

```console
$ docker pull elixir@sha256:bd4ca151e6be55d31d0c4f542e5ebb3f7e76976108e671cd2e396503c243c063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.2 MB (608206138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84913bccaa4b552e6aca39995a10e830d36392f844502f63a0c21bb5cf4b3a60`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be8df58eeddc25d2712f0b9fee580daa0d8d719d5fe7593caf73a5213c001d3`  
		Last Modified: Tue, 03 Dec 2024 05:26:52 GMT  
		Size: 252.2 MB (252237034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2901c6cacee0983400a4e932f1d14fa9c292ad9e713b8685b1b46157087fdf5b`  
		Last Modified: Tue, 03 Dec 2024 05:26:21 GMT  
		Size: 194.9 KB (194921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85a43a543b85805e46643218b1d02cff6266eb6c7f4c5573362efdc437a9a0b`  
		Last Modified: Tue, 03 Dec 2024 05:26:22 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d913d024758e972b1f78a1d0d6ba81bf538fd2cb57c47c83bb0a18f7aeb6ad`  
		Last Modified: Tue, 03 Dec 2024 06:14:13 GMT  
		Size: 6.9 MB (6895089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:93b135825664ef436f4266766e6ca6a426b7d927cc95e09fef8a9f31c21b81f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22736790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29506e4a391f06d4b5f7988322c2e2ba32c89d7418852a1b335a387530d3e1ae`

```dockerfile
```

-	Layers:
	-	`sha256:459a5c3136f625b7cc8ae08e9ee1f135fa326a2db15f06b35d57d0a95626fa34`  
		Last Modified: Tue, 03 Dec 2024 06:14:13 GMT  
		Size: 22.7 MB (22726370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2eb9ec039a05772b8c612ce782e5788e465ab6ba9d0d10454545ce6216bac9`  
		Last Modified: Tue, 03 Dec 2024 06:14:12 GMT  
		Size: 10.4 KB (10420 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm variant v7

```console
$ docker pull elixir@sha256:c123abb56b67dfe281ebc656fb88135d9aa9b182e5a02b69cbcdbb973cc967d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.5 MB (533491061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffac3615e2e223267bc946cb7751da086b2f77fb6bba9c57fad57b765a395385`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838a997cc57e9ca2f3a1f74f662e2ddf435f1d1e6fd867b25ccb80712804b73`  
		Last Modified: Wed, 13 Nov 2024 15:25:00 GMT  
		Size: 175.2 MB (175243336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d66abd06cc410c8ec9ac243e44fd4fdfd38ab325a4074687f4be6d27352ce`  
		Last Modified: Wed, 13 Nov 2024 16:36:02 GMT  
		Size: 223.6 MB (223587215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca33cc77bb9609310be6e2cbdce79f6b4a3702b15f990908ea4737e943b0e86`  
		Last Modified: Wed, 13 Nov 2024 16:35:56 GMT  
		Size: 194.9 KB (194923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329e07935c52f387a4f185a25f61fb9c66718979e9d49bf6ff0d358a54c9c4f`  
		Last Modified: Wed, 13 Nov 2024 16:35:57 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a5d11370e385525918ce4fe6be2969284d309977a3365aab1ffa1543f372ba`  
		Last Modified: Thu, 14 Nov 2024 01:21:41 GMT  
		Size: 6.9 MB (6895137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:b49da3ec5fcc8b4437139f52831c1e5ca922052dc532fc78c10e50bbc0b85a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22553278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc86b24a5edbd89b0f29fcf166bd88e9eb97b403ca38d3bf211ed58f1028c0df`

```dockerfile
```

-	Layers:
	-	`sha256:8c7e8caa442e22e53652104d8f5d989e6e715c2c47942a5950cc389cc38c4f56`  
		Last Modified: Thu, 14 Nov 2024 01:21:42 GMT  
		Size: 22.5 MB (22542790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7783f10dd19700c66f276c7a15cb70713e232f52ba541f4ce77d6a3a58503f70`  
		Last Modified: Thu, 14 Nov 2024 01:21:40 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:530226b66ca10cffe03e275266fe0d8572ddb74dc190af35eaf2aaf1b3204258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.3 MB (593275703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf10b9d5188620fd41a1b0af8b03283961db28ae97fbc2253f82361aeefdac29`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e541ed4b2e560762a3be2c85dc6f45ef1d7a89bc9fd90d07bbc75ce5e725ebb`  
		Last Modified: Wed, 13 Nov 2024 09:51:53 GMT  
		Size: 245.2 MB (245154822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7499ca69bb660be383d1d2cf622bf125c4b4015b6adeb0d8fd44f25c0902ea`  
		Last Modified: Wed, 13 Nov 2024 09:51:47 GMT  
		Size: 194.9 KB (194855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866f7b315d4a9eb2cc92d2cf57be9e8a9ffb755b924564578af51b1d800aa9df`  
		Last Modified: Wed, 13 Nov 2024 09:51:47 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc51b2cfb711ca2142ec48bf580deccbbbbdbb401782b63a0aedce66338932`  
		Last Modified: Wed, 13 Nov 2024 17:01:51 GMT  
		Size: 6.9 MB (6895088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:94bfc16fc6186b44bebd76f80b0c80e211084a4e1512559c2c3491f01c6d7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22778186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a11c65050a7a16fd64118eac8d63bdced2ac3f6a2f27ad2dbb3a596f94b52d`

```dockerfile
```

-	Layers:
	-	`sha256:7d3182345fcd196f574a4d3ffa91755c2fb36a2dfaf11cc86504194efd42c727`  
		Last Modified: Wed, 13 Nov 2024 17:01:51 GMT  
		Size: 22.8 MB (22767674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e39b618f26e7bf00f1d154b71f6fa00b728b8f4d1e5c4f7e6c830ca6e52442f`  
		Last Modified: Wed, 13 Nov 2024 17:01:50 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; 386

```console
$ docker pull elixir@sha256:c90cf340740ee2b9863363589fd0684a3b8c20829c3426c673165bb97717973e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.8 MB (604779152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187edab99ea5d329325000d7295622442a3e525dac243594d4a39f1393edb9cf`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c488b1655c3a6e36bcb81d097a8b488a7501c766ac7dbbd08a4a4ad5fbf9ffa`  
		Last Modified: Tue, 03 Dec 2024 06:25:30 GMT  
		Size: 246.3 MB (246253960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c2ebee02c6ba103bcb3e317ce9163083c3b571d9a0ca9984cb3cdc702d912`  
		Last Modified: Tue, 03 Dec 2024 06:25:25 GMT  
		Size: 194.9 KB (194919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d55773eeb2200284373ade9d0436c1598ae29aade7ee3e457eaafaa699898`  
		Last Modified: Tue, 03 Dec 2024 06:25:25 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7afdfa239ab4b9ca9844a03c7796099b3be9d0751da5edfa01f76d596bbf05f`  
		Last Modified: Tue, 03 Dec 2024 07:13:19 GMT  
		Size: 6.9 MB (6895108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:6cb44a2bc79c3a5af567a55b58b0fea53f3be937899e9a71dc6de4d316963afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22704960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd71255dd6bbec6ab0830d8e3e1718c1572ba95f82a4649d8c21850107a9bb4`

```dockerfile
```

-	Layers:
	-	`sha256:5671239aab92a4188824c9d94d884b41d55d4568af532c861a6de2fa0a63723c`  
		Last Modified: Tue, 03 Dec 2024 07:13:19 GMT  
		Size: 22.7 MB (22694567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e789137b561592e821a531fac75e3d4694cbfe31ee955dbba965ef8aa28a4a9c`  
		Last Modified: Tue, 03 Dec 2024 07:13:19 GMT  
		Size: 10.4 KB (10393 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; ppc64le

```console
$ docker pull elixir@sha256:4d510e923bbf9a54e67ab267d11b06a2205da6a425aaa6ddf28b0aa255fad140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.7 MB (620678696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63faf89e29c15c6f66b73716e75ece2e14684617f9f8979812b18a57b94a88fc`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cfa53de442ed3d22e9313027d1cb611c8221c646e767a0de246cf74640b94`  
		Last Modified: Wed, 13 Nov 2024 00:12:57 GMT  
		Size: 214.3 MB (214330438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47341b2d40d7a7c7c83c7ba9562ca3a86597e65b15429dee6588437a630109f7`  
		Last Modified: Wed, 13 Nov 2024 01:10:03 GMT  
		Size: 249.4 MB (249354777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da8cd4b572e8dcf979a71ae7730958c040f5dafc50981ff4806feaac07b334e`  
		Last Modified: Wed, 13 Nov 2024 01:09:53 GMT  
		Size: 194.9 KB (194924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9ee48837afa3d28bd3db261d809575682adaccfbac452cd8ce0943b749684`  
		Last Modified: Wed, 13 Nov 2024 01:09:53 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd297e337079dceb8019cacd79331934e24fd3c54c005a474940108fb838bf52`  
		Last Modified: Wed, 13 Nov 2024 06:51:10 GMT  
		Size: 6.9 MB (6895082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:d542640c4b3175c5d8cf6ed03d641992cee226c49bb1c9af1b3d5091359104c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac225327c6cb3a9a7b7cd10ac66ace1c48834f1f3b08ae695337ac58225116`

```dockerfile
```

-	Layers:
	-	`sha256:5f0006d91920edd61a845721211ece39a0e8cb853cdb8a8cd80b98307935756f`  
		Last Modified: Wed, 13 Nov 2024 06:51:12 GMT  
		Size: 22.7 MB (22683165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5b5445e5e656a1a7a4043ebec3da1f212aeb9ac03e40062fce009e2bf7ceca`  
		Last Modified: Wed, 13 Nov 2024 06:51:09 GMT  
		Size: 10.5 KB (10458 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; s390x

```console
$ docker pull elixir@sha256:1fed8d9b6ae1f06482566f22c4769d4b4e7a50cef09be929f70b3ad03245b6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.2 MB (561237260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecbeafa47e8186c7cb0fd7f080c1e86ad5cb9d13e63241364cdc8e547c690cb`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f35195f0f87febce22a47bccb66189a905378e44f198db7683ce2820121d4e`  
		Last Modified: Wed, 13 Nov 2024 03:24:35 GMT  
		Size: 183.3 MB (183326311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e768acaaf79b87bc54d4d8b4b497e77b3f4e16b78fc02add8737b62b2010980c`  
		Last Modified: Wed, 13 Nov 2024 04:33:32 GMT  
		Size: 234.5 MB (234532076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5a9a0d0d9dd358c00626ce13f70e53be2d0b85f05c72f477497f33ea6be91d`  
		Last Modified: Wed, 13 Nov 2024 04:33:29 GMT  
		Size: 194.9 KB (194915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e36b4ca7a99cb796a8149f88f3e29c84fdc883881042dc8c35c57fc492349`  
		Last Modified: Wed, 13 Nov 2024 04:33:28 GMT  
		Size: 818.4 KB (818380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6443e87f249d9ea5977871d880af0fabfd3731c8f0798871ade683e8e4f2ce3`  
		Last Modified: Wed, 13 Nov 2024 12:14:01 GMT  
		Size: 6.9 MB (6895046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:d0d3d13ea6910bcd5437baf824556a0b1d9e5a679dea56c37b997c5f6938603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22511530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff5f75b28a555682eacbf2c6aedd44e5043f3feb0fe330486e2493823048839`

```dockerfile
```

-	Layers:
	-	`sha256:1cc15a515ae183d32293c8c73549bb0bdfe7371bf36e22647dd1a572e55ec718`  
		Last Modified: Wed, 13 Nov 2024 12:14:01 GMT  
		Size: 22.5 MB (22501110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3600d460991928f69157cad485e9e77a6d95f9d11df04d21234dd5d24953042a`  
		Last Modified: Wed, 13 Nov 2024 12:14:00 GMT  
		Size: 10.4 KB (10420 bytes)  
		MIME: application/vnd.in-toto+json
