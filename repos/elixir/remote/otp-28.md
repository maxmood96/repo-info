## `elixir:otp-28`

```console
$ docker pull elixir@sha256:ddecde1fce775f5cc7d63643bf303e062b2bab977c572df433e3bdb1e53a9502
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
$ docker pull elixir@sha256:22ff373a621b2999510e8a525b1ec5aada2e09c27e42bb35c8c104c09ea73e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679605897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7715205220b826603aaa965ca0a6f6a83b2766c22bfaa66f54bd5ca1041a22`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:15:10 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 06:15:10 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 06:15:10 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:15:10 GMT
CMD ["erl"]
# Wed, 22 Apr 2026 06:15:10 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 Apr 2026 06:15:12 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 Apr 2026 06:15:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 22 Apr 2026 07:34:02 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 22 Apr 2026 07:34:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 22 Apr 2026 07:34:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1bb20756a85e159dfb7908a2a5c860ac2f2254254a915d8c047e02cb2b0259`  
		Last Modified: Wed, 22 Apr 2026 05:14:09 GMT  
		Size: 236.1 MB (236074811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e472cdb5ffdee838dddd458782cd9fb4b4b6f5c3bec1064d83edd9d955f87f9`  
		Last Modified: Wed, 22 Apr 2026 06:16:27 GMT  
		Size: 292.0 MB (292038171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ac2d8c408f2ec49326c04f2e31f6bab3997ef3e792b52b650a9d3986c94c0`  
		Last Modified: Wed, 22 Apr 2026 06:16:20 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c688b0ad7c45733607cdeba333a3f27c51e51d81e13f37ac2897aad6f8cb4`  
		Last Modified: Wed, 22 Apr 2026 06:16:20 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf4dfec45caccb283128d8c53dbceb383ebc4fd7e3acdb4a018a99f1ebe284d`  
		Last Modified: Wed, 22 Apr 2026 07:34:33 GMT  
		Size: 7.8 MB (7766946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:5d29a10e0a62d8090dfc4b847112d29d00585ad285d8f0539fcdf29aeb1309d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22066816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7b69c62072c45036691b3e8a1d85ebe7506921071621cbef73ec906385a4b7`

```dockerfile
```

-	Layers:
	-	`sha256:b9cce14d91c03d5e2d0c82c08a2212839194cd9bc01297d4eb6c03d49a43e2a9`  
		Last Modified: Wed, 22 Apr 2026 07:34:33 GMT  
		Size: 22.1 MB (22055565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e53cbd973d1aefe93f771a8c8f8411d28f7e7ed82f7c9d02a4f788146f3db4`  
		Last Modified: Wed, 22 Apr 2026 07:34:32 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm variant v7

```console
$ docker pull elixir@sha256:47f31755998ae26137e2e901629df477888f965b9e3940f0d2d546c53228d5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592906478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2cdfb0f94165a9f25473e5182eca0944504198c0a1c950444a8da9764772b3`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:16:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:16:44 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 05:16:44 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 05:16:44 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:44 GMT
CMD ["erl"]
# Wed, 22 Apr 2026 05:16:44 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 Apr 2026 05:16:48 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 Apr 2026 05:17:08 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 22 Apr 2026 07:11:28 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 22 Apr 2026 07:11:28 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 22 Apr 2026 07:11:28 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab603b07acf826bbac9a62308beed40392f03d30c6911af4cf6fde3264b31d`  
		Last Modified: Wed, 22 Apr 2026 04:16:39 GMT  
		Size: 193.4 MB (193387724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a879c26b7ebc5bf1d50bbb8b5178e7f4379971982a31feee6ec451494115302`  
		Last Modified: Wed, 22 Apr 2026 05:18:03 GMT  
		Size: 258.6 MB (258644311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eaad96d7261e91d5edd42674f826ebca79c80a88a6eace3ed1dd459954c20b`  
		Last Modified: Wed, 22 Apr 2026 05:17:55 GMT  
		Size: 191.5 KB (191495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16174fb62504de9e2713f2f4046c1128124611aa438e1f62c08219e5a68d262`  
		Last Modified: Wed, 22 Apr 2026 05:17:55 GMT  
		Size: 819.8 KB (819846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341438d0608990d43da201bca25053c6282c07b769fea34a623006e93b93f1f2`  
		Last Modified: Wed, 22 Apr 2026 07:11:55 GMT  
		Size: 7.8 MB (7766838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:93b21ba9731ef285f9fd079a85caec764b5999f270b9af5329a46cc601efaa80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21812912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c444e5fd2485f93197fc6b236cc149d33a18babf8930bcce844c8d041b6f48d9`

```dockerfile
```

-	Layers:
	-	`sha256:f492ea4090d374d3bf5d81f0fa90552eb3a9f1fa539b214b79b73ad37f1ad870`  
		Last Modified: Wed, 22 Apr 2026 07:11:56 GMT  
		Size: 21.8 MB (21801565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb4cbec990f4794f15cc9f6e8dd37af38159d54d841735bd67d0adb487dd6384`  
		Last Modified: Wed, 22 Apr 2026 07:11:55 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:8c0eacdb435178c0f6cffe39c82ced6389a4f4b19a661126529abdde22cfaa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 MB (662030338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0849f5690ce0c2142d0dcf1f4134e70278373c2bc8cc0d2c63983756dc3287`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:16:23 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 04:16:23 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 04:16:23 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:16:23 GMT
CMD ["erl"]
# Wed, 22 Apr 2026 04:16:23 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 Apr 2026 04:16:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 Apr 2026 04:16:36 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 22 Apr 2026 05:13:53 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 22 Apr 2026 05:13:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 22 Apr 2026 05:13:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5461f2dc96dbc8b34faf5c31d5312e44d27b85e81fffef565438663f34f538`  
		Last Modified: Wed, 22 Apr 2026 03:18:16 GMT  
		Size: 226.2 MB (226209559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dcf5e632d4880b5c6b78fdc64dc28365c31b9529d0d7a56fcbdf40c95e524e`  
		Last Modified: Wed, 22 Apr 2026 04:17:35 GMT  
		Size: 284.8 MB (284765147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c714d5182d7b45f43dd93efbd04b5cfc1e839049231e0d3f134af20fbabebb67`  
		Last Modified: Wed, 22 Apr 2026 04:17:29 GMT  
		Size: 191.5 KB (191472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56831276e47ea91097c3069a395b83ee0448add1a441c55942c48eeed72f6ab7`  
		Last Modified: Wed, 22 Apr 2026 04:17:29 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86fe18fe43ecc4f07079e6f44aa78d505784f8461fd3193b57083dcd65cb3c7`  
		Last Modified: Wed, 22 Apr 2026 05:14:22 GMT  
		Size: 7.8 MB (7766924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:e82a8e902ed3529287afda8f1e6483c656748d9469d1780ccc4abe0affd58a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22138290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fdc66a9384a0198e0c6165dbc5ed1205ce5f03dfde625bf30a5d2438352885`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f8d14aebd02776fae471e71a64ed6761d7cff7f2a6d44aa8356ed2ecbf087`  
		Last Modified: Wed, 22 Apr 2026 05:14:22 GMT  
		Size: 22.1 MB (22126911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30aab570d0c030399c0346f732375722e8d3c81b3b15245a92004c9adec4f519`  
		Last Modified: Wed, 22 Apr 2026 05:14:21 GMT  
		Size: 11.4 KB (11379 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; 386

```console
$ docker pull elixir@sha256:69547766429dd3cbafa0b528d6d184d0506e91ffd4aba935d1b19ae660d8de53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.9 MB (681936355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124acfd9dbaf1e9bb4ace1d116c708490b4f341cf7a3019fca6ba073f8dab3f7`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:20:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:23:47 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Fri, 10 Apr 2026 00:23:47 GMT
LABEL org.opencontainers.image.version=28.4.2
# Fri, 10 Apr 2026 00:23:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 00:23:47 GMT
CMD ["erl"]
# Fri, 10 Apr 2026 00:23:47 GMT
ENV REBAR_VERSION=2.6.4
# Fri, 10 Apr 2026 00:23:50 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Fri, 10 Apr 2026 00:24:11 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Fri, 10 Apr 2026 03:33:11 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 10 Apr 2026 03:33:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Fri, 10 Apr 2026 03:33:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6419d63858855afa34d3a14b889b2d9e157f74b4901b779052fba5d24c1f0a5e`  
		Last Modified: Tue, 07 Apr 2026 03:20:54 GMT  
		Size: 240.2 MB (240182156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcfc922cf2e34215fbf83d3ac3e882a8af934aa281298ba3ba8df989bd02728`  
		Last Modified: Fri, 10 Apr 2026 00:25:13 GMT  
		Size: 285.6 MB (285578259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f5742e1a15ff74a609962fe47c4074f010d9ebfe7d8e7a6d14e484a32beddf`  
		Last Modified: Fri, 10 Apr 2026 00:25:06 GMT  
		Size: 191.4 KB (191447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aaaac039b89a2894557ef7ef7bcab7fcd195f258f7888653c1b6b9876f0fa7`  
		Last Modified: Fri, 10 Apr 2026 00:25:06 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a843e531d6b0a8fdc7d3049beed2f9dd8f7b6f4c00b829c4b3fd61000c2c1a0`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 7.8 MB (7766871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:5c6bc7639ae35d5831f71e8daafe8f909c6a1561ae8996ebc38b0d3ab814c8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22034559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2403c516d6b66add35b52bd361ec42b98b05c1a117099abe6ea2f9c9c0c99c`

```dockerfile
```

-	Layers:
	-	`sha256:29e8a865ffaead7e464c9e168b10286d75ccacab785a5c25ad27da074183f617`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 22.0 MB (22023350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a8e5e1aaf754886b4edaa5a86c269a1296a28efef1de1ef6415966bb55e789`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; ppc64le

```console
$ docker pull elixir@sha256:9127a34ee06c881fb5f3eb27d4ca786f5a9d02ddf90446fd804e061f47144ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.6 MB (676612944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf296316241163ae1d2c603b87ad5ebf20e41a8a2d5daaf95c06a8e793aa7cd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:12:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:27:45 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 23:27:45 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 23:27:45 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:27:45 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 23:27:45 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 23:27:52 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 23:28:35 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Fri, 10 Apr 2026 01:02:05 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 10 Apr 2026 01:02:05 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Fri, 10 Apr 2026 01:02:05 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169353b9ab6307e2b065964fc878588895f32907dd884c905868bc86f58edd0`  
		Last Modified: Tue, 07 Apr 2026 09:55:34 GMT  
		Size: 73.0 MB (73033989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5f682bd4776a2aa089944df5527ca4a87b57f256c6c979b8dea44633e85334`  
		Last Modified: Tue, 07 Apr 2026 18:14:03 GMT  
		Size: 231.2 MB (231208883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d347741419bdd1e8f04906a44603476487fba752c64806e29644b95bfde88`  
		Last Modified: Thu, 09 Apr 2026 23:30:22 GMT  
		Size: 283.5 MB (283459327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41362d7807bce2a9d4c8bfcdfa0bcbba5608b6f7775fd0ffbf89f88c2d6b5080`  
		Last Modified: Thu, 09 Apr 2026 23:30:15 GMT  
		Size: 191.5 KB (191461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb334d667d2885268edbfd740129f339c3a4393a263f0d6353dcc04ffb5fb5`  
		Last Modified: Thu, 09 Apr 2026 23:30:15 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96404ed91b2cb0f8beab23a4f80770cb89af1da6b6b5caabab54a76d442a1148`  
		Last Modified: Fri, 10 Apr 2026 01:03:15 GMT  
		Size: 7.8 MB (7766914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:c5e1d24f6fc6809cb5b27e9ede576ddbc38a625f66891fc2ab6c4d1c387e5bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22026514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bf809e60e738e2aab10b0e3ae5d6257bdac5d5d9698df32123d30a56634c2e`

```dockerfile
```

-	Layers:
	-	`sha256:8d9df8976eef26bcd514c2cc1562746e25d69e17f932ed564df8ce2d39958d2f`  
		Last Modified: Fri, 10 Apr 2026 01:03:15 GMT  
		Size: 22.0 MB (22015207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf589bf03ddd2845f942d28a0ac8794f8337674cdf8f3846a8a92e87ac206d3e`  
		Last Modified: Fri, 10 Apr 2026 01:03:14 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; s390x

```console
$ docker pull elixir@sha256:46c3cf0ec48c1bb419d00200b401747d2870d15664214c506c8883ec36fba55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 MB (648338076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2750d8a351d2f1c7e658fb45807fc586a66c711e97b107a261ec62776b60d743`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:13:35 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 06:13:35 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 06:13:35 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:13:35 GMT
CMD ["erl"]
# Wed, 22 Apr 2026 06:13:35 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 Apr 2026 06:13:39 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 Apr 2026 06:14:03 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 22 Apr 2026 09:52:23 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 22 Apr 2026 09:52:23 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 22 Apr 2026 09:52:23 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797d445faaa1f9219c6d6ae09f17025e8f5995b4cec1bfc6cac2d3adf9581a2`  
		Last Modified: Wed, 22 Apr 2026 05:14:44 GMT  
		Size: 206.6 MB (206602552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19f41833026a71ce682d8e175f6a4effc3158fbbb132f4f6b3b294d9d396d71`  
		Last Modified: Wed, 22 Apr 2026 06:15:32 GMT  
		Size: 288.1 MB (288145922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa4d256b3667a39159dc1a1a96aea004cb76177e7948b08df39f2336a4d4c96`  
		Last Modified: Wed, 22 Apr 2026 06:15:27 GMT  
		Size: 191.5 KB (191461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798fa6013c2d38c26a7c7266e7ea5c765d7fcdf1eee3ba7c75b9fc1a26ba9229`  
		Last Modified: Wed, 22 Apr 2026 06:15:27 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a29ab63676ced9ac4d54058c779d6bba56ec8c61fbe3ed6bd1c9a4fc39af7b0`  
		Last Modified: Wed, 22 Apr 2026 09:53:14 GMT  
		Size: 7.8 MB (7766863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:1cce6c50c914f6feefd91cb6dd07c38fd113ca405ee74c4420be3e97755a6328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21716574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3557bb76319af5777de01689e9c3dfd07581a6bb31c13f4a960dd6b2bccde347`

```dockerfile
```

-	Layers:
	-	`sha256:b4e3f1aa350d1ab6e3b32fc25bf978d824558b95b9f621bc11f2510640b539a0`  
		Last Modified: Wed, 22 Apr 2026 09:53:14 GMT  
		Size: 21.7 MB (21705323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc37f102081ce31849c958ebd7e4fc70e73e51233447e8bc5a4d46214ec41d0`  
		Last Modified: Wed, 22 Apr 2026 09:53:13 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json
