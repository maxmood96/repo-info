## `elixir:otp-28`

```console
$ docker pull elixir@sha256:d3c050c253b4bd06f30e5eec22b29d368e22766a1937ea622f9c0fd15538c18d
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

### `elixir:otp-28` - linux; amd64

```console
$ docker pull elixir@sha256:99633245348c13114f023701712182f6ab6d6d127cb379714b0bb8d15c3aa2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.8 MB (679773007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b2a77273beb79cf5da91f6e2f194dfb21b83c5972da6abfb42cbff41ecb0ac`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:35:33 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:33 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:33 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:33 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:35:33 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:35:36 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:35:48 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:46:09 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:46:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:46:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d823e3848f3d74363d9b5b44f39f2d2f81a99a37d8c7fb54831a489a32e999`  
		Last Modified: Tue, 13 Jan 2026 05:12:51 GMT  
		Size: 236.0 MB (236001828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ddbe20790f74e75fe43be8f9666dc99e7182cb141bef8e92d93269a30cf1c`  
		Last Modified: Thu, 15 Jan 2026 19:37:49 GMT  
		Size: 292.3 MB (292309557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48524c6830772e3f844be7aa96eb3809b698bdc00e681dbc7789f632fc39ecfe`  
		Last Modified: Thu, 15 Jan 2026 19:36:53 GMT  
		Size: 191.5 KB (191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c3e3b3718c67d08794cad1444e6a17df66c70fb7661a594d3ae1531560d83`  
		Last Modified: Thu, 15 Jan 2026 19:36:54 GMT  
		Size: 819.8 KB (819810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3612b2e41dd9195dfb16ab86fd269ca13c285290e4f921d773f14cfd34ebbe84`  
		Last Modified: Thu, 15 Jan 2026 21:46:49 GMT  
		Size: 7.8 MB (7764511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:343ce182f8111bb684574e7ce63561d440affaa134780dde72dde17854d47edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22067066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4afdb4dd475102e1eb3f20a047c9c4e10796a28ff19d2b5809d413886cee535`

```dockerfile
```

-	Layers:
	-	`sha256:c37c54234bc806dd469b09974fd9946c88ca81ba2b19808df7f087a102c9b15a`  
		Last Modified: Thu, 15 Jan 2026 22:47:22 GMT  
		Size: 22.1 MB (22055815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c934663a7c6a14987bf14418824037b1e58cdebcd686c3cde35480cc83fb7ce`  
		Last Modified: Thu, 15 Jan 2026 22:47:23 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm variant v7

```console
$ docker pull elixir@sha256:b23f147e488d2b470aa28b9f03da4396c986f0156d4db57a6b9ac919b365f0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592702539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52633bc8d905fac43bfe625423f0a67981f5f1e885be8add81032ce4920e26cb`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:35:53 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:53 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:53 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:53 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:35:53 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:35:57 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:36:17 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:49:41 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2c3dfa2d6df259da14558beefb7cee69246c0da0fdc440a04d5af7c8fb7dd`  
		Last Modified: Tue, 13 Jan 2026 06:15:55 GMT  
		Size: 193.3 MB (193306851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5d300aae4586cc437bad24323b3ffac9cbdc295d8175511f9f8ef1d07174fd`  
		Last Modified: Thu, 15 Jan 2026 19:38:35 GMT  
		Size: 258.6 MB (258562071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899d178f8fe9d824a2f81674f1fc23945fb05b1f86cb9ad980510fa74ec8acd`  
		Last Modified: Thu, 15 Jan 2026 19:37:18 GMT  
		Size: 191.5 KB (191483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb43a7712df6a952286bf09e6d96f156d20ba449c2241619cccc382747df5a2`  
		Last Modified: Thu, 15 Jan 2026 19:37:19 GMT  
		Size: 819.8 KB (819809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d77189edc4da7d7561fb0dd789439eea24239b3346f0b426386c628c2aeb53`  
		Last Modified: Thu, 15 Jan 2026 21:50:19 GMT  
		Size: 7.8 MB (7764456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:17e3098d1064ad97e53d93adb5ce4602796874487f6831fc38a82737e2f3b763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21813162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f14103f9b2ce4787e5788b1df806bd960b593cd3403e7cb056d942c5b491c6`

```dockerfile
```

-	Layers:
	-	`sha256:1f74aae76576dd16fedd43cd57a23fcb9e9526c41cc7d714a93c7e3f2ca95156`  
		Last Modified: Thu, 15 Jan 2026 22:47:48 GMT  
		Size: 21.8 MB (21801815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de6e14b579f44d259c625da2bc5d6ce682335690484971fdaf030e427a1d8945`  
		Last Modified: Thu, 15 Jan 2026 22:47:49 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:5c163ba62525d24a7787ec42e034cf82769abc0a2c5f640d63dc10b3cfe4419b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.7 MB (661719171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be229f7497077d4b47f987efedaa027b737dec5ed01398f044edeed76d582bae`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:52:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:35:59 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:59 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:59 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:59 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:35:59 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:36:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:36:12 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:45:41 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:45:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:45:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffeb567ed4215b503f814aeaab9fa5a2e701d3efa35d4c285b3cf111e9cb4a`  
		Last Modified: Tue, 13 Jan 2026 05:16:01 GMT  
		Size: 226.1 MB (226143857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b14010ef5a8674cafa23f6d0917a8acc9adb4d0b9817930956a779fb15f5799`  
		Last Modified: Thu, 15 Jan 2026 19:39:10 GMT  
		Size: 284.5 MB (284537291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3e8cd9e3f6b4646e1139aadfb87c9c9afef85063f1ca952bdd447a7f369979`  
		Last Modified: Thu, 15 Jan 2026 19:37:17 GMT  
		Size: 191.5 KB (191492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a19f95f387ade96545e7b400d2abb995aa26d85c8e2d329264058cb9c42bcc`  
		Last Modified: Thu, 15 Jan 2026 19:37:17 GMT  
		Size: 819.8 KB (819809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f671503a54c6d8c050dfea7d4b25d1f159933f6f1acaefb1a68fb546d40d7133`  
		Last Modified: Thu, 15 Jan 2026 21:46:18 GMT  
		Size: 7.8 MB (7764490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:cb6d970eba82bb138bed1b7e634cf83019266dc93acd0c9a42fbf89ced5c1934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22138538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e760212eeb67bb46bc84e778ecd1e376343b146d62c01e09e823ff21c75199`

```dockerfile
```

-	Layers:
	-	`sha256:f7b14b591c4d63ee6dcbd223d828e937174e2fa3e6543f2469630eeb195c4ff2`  
		Last Modified: Thu, 15 Jan 2026 22:48:13 GMT  
		Size: 22.1 MB (22127161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8e8950f6c8bfe3c7a84b587bf1733b4ccfe978176e7a7b0ca7397554ecd23e`  
		Last Modified: Thu, 15 Jan 2026 22:48:15 GMT  
		Size: 11.4 KB (11377 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; 386

```console
$ docker pull elixir@sha256:6a8a4e8643bec6d743d809b3fd665e83e0c29b406ea061da8042b85f3a7370a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681719773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b8f13c5ac396a3f2fff72971bf276ed6a5f0c23c181f3dc7987078407c8d3c`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:56:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:35:50 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:50 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:50 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:50 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:35:50 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:35:53 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:36:11 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:46:38 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:46:38 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:46:38 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c438693622c619054710e61f4e49c9f44709996e7ac1c8577527c38f87d008f`  
		Last Modified: Tue, 13 Jan 2026 04:02:03 GMT  
		Size: 240.1 MB (240108789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02b34c34ba3036edbea6fd2eea34c98d8b56a7197e31b29fa4408759d158b14`  
		Last Modified: Thu, 15 Jan 2026 19:38:29 GMT  
		Size: 285.5 MB (285454849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d9f4d1c9342713053c34fbb3b41b74cd4f39c0aa1134d44c2c63065699e2f`  
		Last Modified: Thu, 15 Jan 2026 19:37:13 GMT  
		Size: 191.5 KB (191482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6603fad54cabda488cef4ca2d3a92031f9d44a9e609a3ebe125161f5d20b666c`  
		Last Modified: Thu, 15 Jan 2026 19:37:14 GMT  
		Size: 819.8 KB (819808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94cfb1caeee6d4e9ed8bb1e905b0350279d087d907009538d2cfcb75450db1`  
		Last Modified: Thu, 15 Jan 2026 21:47:16 GMT  
		Size: 7.8 MB (7764487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:dbd5474d693d6a573c0dde57e9a769267b08b10a066d06b06eaa7dffd3a2bc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22034988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f117c475da4748e301240bf3a878031acd1db75e3b05ba2fcd95ae1ce9618f`

```dockerfile
```

-	Layers:
	-	`sha256:eac25f079127432352ea4b2d6683c05ee2e56911536da64da7932e5f8f21f2fe`  
		Last Modified: Thu, 15 Jan 2026 22:48:41 GMT  
		Size: 22.0 MB (22023779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cf22233bf7fee725af8831ed6e1ed8f739630134678dc889a0a378a7e9b05`  
		Last Modified: Thu, 15 Jan 2026 22:48:42 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; ppc64le

```console
$ docker pull elixir@sha256:298c9f98a91dac49718bd13f3a0bbfb6337d55aeb1c10b6ffeedb1cad60804d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.4 MB (676418593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ae0808a21f73f25dfa43e03596dc2a3be34d1411c150576214d3057030cedc`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 16:13:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:41:57 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:41:57 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:41:57 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:41:57 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:41:57 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:42:05 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:42:58 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:55:34 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:55:34 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:55:34 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:09 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:20:19 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e13e772271d599b914654801e760b6e090a2d2a51765f2bd85981f821d1eb0`  
		Last Modified: Tue, 13 Jan 2026 16:14:51 GMT  
		Size: 231.1 MB (231145655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ae9a21e5701631d843af1631aaadb57708edc83395e5273ca39b0bfa196ed`  
		Last Modified: Thu, 15 Jan 2026 19:47:30 GMT  
		Size: 283.4 MB (283354502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d412cd106ab47d29786cb831091089cf706ba0e16d369552aa4a49bca1016f6`  
		Last Modified: Thu, 15 Jan 2026 19:45:30 GMT  
		Size: 191.5 KB (191491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d770392f1529c17ff67d7d0acf44815274838c1f2c8b188b3818e3c8f85b892`  
		Last Modified: Thu, 15 Jan 2026 19:45:30 GMT  
		Size: 819.8 KB (819809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2d25c5622fa6d680e373d8646130729be14e6e9c02b8d9254ca5adba83494c`  
		Last Modified: Thu, 15 Jan 2026 21:56:37 GMT  
		Size: 7.8 MB (7764514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:8a194be3faca2d8a5430ec7583071084af101aa3d853fce8af543b2b3b782519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22026946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eeb3a98e8a4ad7573415005106a03503c27bd29c60e0986375716b75e79622`

```dockerfile
```

-	Layers:
	-	`sha256:fb618c0217727e67e755941fb80167e6e9d738b51207fb58bc2d54677e82282c`  
		Last Modified: Thu, 15 Jan 2026 22:49:09 GMT  
		Size: 22.0 MB (22015639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9baaeb2cd37ff335f8b4c4c91dcb9bd8a69f7869bd1c13401622e1bb4794e6`  
		Last Modified: Thu, 15 Jan 2026 22:49:10 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; s390x

```console
$ docker pull elixir@sha256:5696c275c124d0c1b36582cc4c260d3b80c8aa9ee6262b9c85b5bc97318e79c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648160570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21df303ab111d436adaf2334650337ae64ac09cc37ce854abeb44b8246dea774`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:37:12 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:37:12 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:37:12 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:37:12 GMT
CMD ["erl"]
# Thu, 15 Jan 2026 19:37:12 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 15 Jan 2026 19:37:15 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 15 Jan 2026 19:37:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 15 Jan 2026 21:49:28 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 15 Jan 2026 21:49:28 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 15 Jan 2026 21:49:28 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc8348b5ddb8c2acabb8e9ca2d1b4b97457b5a1f89dd3ca04047f15644b88c`  
		Last Modified: Tue, 13 Jan 2026 05:17:23 GMT  
		Size: 206.5 MB (206530469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8c33cd6e71ff1e912894c96a61a4647a4183b59f162fcb7af2010fe3e1b7f`  
		Last Modified: Thu, 15 Jan 2026 19:41:35 GMT  
		Size: 288.1 MB (288080068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d91811ce44e0078dc0c340fc168705947518b6fef938d8373e9b3256293c9e`  
		Last Modified: Thu, 15 Jan 2026 19:39:15 GMT  
		Size: 191.5 KB (191484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5131ed13843bbba0cb7aec13d4744d0b60fe57047d7f6db35c2f45d83426202e`  
		Last Modified: Thu, 15 Jan 2026 19:39:16 GMT  
		Size: 819.8 KB (819809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60229a66d25aa4b78f0f63d34eca62952d44c0dff1aa2c09ee0b42b6ae24a629`  
		Last Modified: Thu, 15 Jan 2026 21:50:19 GMT  
		Size: 7.8 MB (7764466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:f359b109b8bbc83f8751fa50f3f5c599e66358dfce1c3a98cde2d0c261145c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21716824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabac955c7ab01f108500ac19211950a1872cafa3c472b12369bc258d1f0b4eb`

```dockerfile
```

-	Layers:
	-	`sha256:8f66f8cdbb755301d7ea1d6c41e1c1956fd9bf454e4a4ccda7d8db4c45e3d8ed`  
		Last Modified: Thu, 15 Jan 2026 22:49:36 GMT  
		Size: 21.7 MB (21705573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce759f91531a5316faa6216fadd96cc045c29ee0459c255485db62f19d0a255c`  
		Last Modified: Thu, 15 Jan 2026 22:49:37 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json
