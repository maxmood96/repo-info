## `elixir:otp-24`

```console
$ docker pull elixir@sha256:dd8d83ea619722e4c0972105259adb10a8ad99987642063dae973af1c36e3dd8
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

### `elixir:otp-24` - linux; amd64

```console
$ docker pull elixir@sha256:305bd4a7c8af6fb2f2763d60f6a654d06631fff77614d1ca447d0f44132b1645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.3 MB (577304231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b767937f6c1e53821cfab7b924d8b0586c491ab54d0985dabb6a3266654552`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0209a266bb24310efc230a2cedc8c753df202b1367d6b917b3a6febaaa225fd`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 197.0 MB (196974754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda86262fdce4609754d9cc436713fe350dfd0627b81276519e0fdc000069c5a`  
		Last Modified: Tue, 13 Feb 2024 04:15:27 GMT  
		Size: 247.1 MB (247134636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca92604c142c550ea3028398d0cbe33c5c71ca70dd1e1becc8dfbd184fd7b94a`  
		Last Modified: Tue, 13 Feb 2024 04:14:59 GMT  
		Size: 196.5 KB (196476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7c1346989fc640c1fa73696d5ded40a0522530ee693e6d5540c98c2738ae9`  
		Last Modified: Tue, 13 Feb 2024 04:14:59 GMT  
		Size: 772.2 KB (772188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfd64cd44e3dfa1de0ebca8c1dc4a1ed61964ce9b0aad01e3fd0b05a637d44a`  
		Last Modified: Tue, 13 Feb 2024 04:56:06 GMT  
		Size: 6.8 MB (6789346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:fcebf098fd3662bc870798cb3ca29da0ffca51399e4a14d12010d49a1ad9c34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19656196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a958e4c58531113a231894cef74f490d9cc799ba47611f71cdce30de53eef54`

```dockerfile
```

-	Layers:
	-	`sha256:639a6fc02e4cbae3263b593debf914ddb3702eea3b16c2a955997e3b5ba73f86`  
		Last Modified: Tue, 13 Feb 2024 04:56:06 GMT  
		Size: 19.6 MB (19644852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c123723ff81dc827247a90a28c5b7bfbbb4b194c48d67e41155a645d2fe8dea`  
		Last Modified: Tue, 13 Feb 2024 04:56:06 GMT  
		Size: 11.3 KB (11344 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24` - linux; arm variant v7

```console
$ docker pull elixir@sha256:d4fbc22eb656c1de7e72907ac80eefbc9333bb70a2c3aa5c4bda53c14b433d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513113596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f615687f0cfa8544c2100221d16ad78f1a1a89fe805d0f3590c1124bb06bfde2`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 04:59:21 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 04:59:21 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 05:05:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:05:58 GMT
CMD ["erl"]
# Thu, 01 Feb 2024 05:05:58 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 01 Feb 2024 05:06:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 01 Feb 2024 05:06:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bfc3e692e8ff6873d25f44400c58bd3aa6d14344de87d8ad43f17573aaa0cf`  
		Last Modified: Thu, 01 Feb 2024 03:00:28 GMT  
		Size: 167.4 MB (167381508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd111e40ffff65960b64881fd5381ccacb8bb7027161312026140cccabd2088`  
		Last Modified: Thu, 01 Feb 2024 05:38:55 GMT  
		Size: 222.5 MB (222516000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ec5300328118524e37682eaad85832724fd0e1a5c77052bec0991288654725`  
		Last Modified: Thu, 01 Feb 2024 05:38:28 GMT  
		Size: 196.5 KB (196472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62956eb8bf3c8a6028cd459c999ebb62bc1f7b20e480efcb44c9529c173dcf9`  
		Last Modified: Thu, 01 Feb 2024 05:38:28 GMT  
		Size: 772.2 KB (772190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082b655a4890ca40004b5977df0ecbe26a0a78f9f23cdedb36d13abcf509c28c`  
		Last Modified: Tue, 06 Feb 2024 22:48:01 GMT  
		Size: 6.8 MB (6789357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:780cb1c888de4a0329255b7887cb3809969d18c16e29d56dcecf7c8a4e481f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19397506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4ff1e3dab18dc2bcdc946c07f2cccc1f4cbe35b1a6f2175c50bdeddebf7843`

```dockerfile
```

-	Layers:
	-	`sha256:69688fef8d0c7093175e455dc33f252a6cf7d6127387736b148e8c8331ba10aa`  
		Last Modified: Tue, 06 Feb 2024 22:48:01 GMT  
		Size: 19.4 MB (19387255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a1c54cbfbe91daac483dec9cbdb3e529542f418a5344af3a5644b150a455f`  
		Last Modified: Tue, 06 Feb 2024 22:48:00 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:9dbbf197d532438c7d899cb309ebf5957c5b01f1b014c9fce245dd87788b9443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.4 MB (557405757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd2559e857cd59a2589c2323eee9444b47fa57020a79a123826a048a2a23b34`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:23:14 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:23:14 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 00:27:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:27:36 GMT
CMD ["erl"]
# Thu, 01 Feb 2024 00:27:36 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 01 Feb 2024 00:27:39 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 01 Feb 2024 00:27:54 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890edf75599fe558c8b1705d12a7ed49aca378c73d11ce7f7d9f59e1fc0e6c90`  
		Last Modified: Wed, 31 Jan 2024 23:53:47 GMT  
		Size: 189.8 MB (189834575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f931f247c8eb9200a8bbe2bf4eb71bbbbdf073651c205fcdef4a87a1ad022`  
		Last Modified: Thu, 01 Feb 2024 01:09:11 GMT  
		Size: 235.7 MB (235654324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f263b0d5a2402a565ce86d889301eb47715fbdcee75f93a48b68fc71c76e0ba`  
		Last Modified: Thu, 01 Feb 2024 01:08:50 GMT  
		Size: 196.5 KB (196478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc987c707c9e659aee0812f1f8c991d5e02159380097729bae717f4cb69fc41`  
		Last Modified: Thu, 01 Feb 2024 01:08:50 GMT  
		Size: 772.2 KB (772189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae6b5e06a1738f9462540f1a514a94a9eb09f340b5e6428b560ba6d297e0a4`  
		Last Modified: Tue, 06 Feb 2024 21:44:00 GMT  
		Size: 6.8 MB (6789368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:3c4e00969b58c61bb1c9b0a2d2eb8c86a50f4464d305b47a1a7f74d868fc83fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19571855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb079fb69748c1290de65a3a9369452d80ff96b5b971388a1a42976945c3e0a`

```dockerfile
```

-	Layers:
	-	`sha256:c8ac29bd676fa59c42a0b59429c4dbaaeb1a64609e108a2ba091e43583a91eb7`  
		Last Modified: Tue, 06 Feb 2024 21:44:01 GMT  
		Size: 19.6 MB (19561658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df1056bfcd1767aa9d5fc9faf43597c2d0f1f95e745171cbb3e5d74bf41ef8b`  
		Last Modified: Tue, 06 Feb 2024 21:44:00 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24` - linux; 386

```console
$ docker pull elixir@sha256:301ec54b9a98708e6ad2bc5d975600781046636a2b264628807b6267f0dfbcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579355518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6bd20d8fc2fe2ed650cb6002a7aa2039fb82141b52307a910680960f20816f`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:36:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:39:37 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:39:37 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 00:51:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:51:31 GMT
CMD ["erl"]
# Thu, 01 Feb 2024 00:51:31 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 01 Feb 2024 00:51:36 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 01 Feb 2024 00:52:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16eaec20d2529e6d6598173a9d9d703f940af73aa52ac269cec733301bc178`  
		Last Modified: Wed, 31 Jan 2024 23:47:23 GMT  
		Size: 199.8 MB (199825679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e7e0048dec17e605111cd45b5ee6057b3ed46dbeb1ffb22f7b830d0009cc`  
		Last Modified: Thu, 01 Feb 2024 02:50:29 GMT  
		Size: 243.5 MB (243516280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708012285c69019602d278837d6981e4501459ee6ad2958187569209c497a4f7`  
		Last Modified: Thu, 01 Feb 2024 02:49:46 GMT  
		Size: 196.4 KB (196441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e06286ac3726c500f21c995c9f4f32de9161aae726706b6fa876cf1e682ea`  
		Last Modified: Thu, 01 Feb 2024 02:49:46 GMT  
		Size: 772.2 KB (772188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e9a60a4ad7ef56dcd16972a4b4fb2523f2e5790937c3f3dd24c17e42d04a1b`  
		Last Modified: Tue, 06 Feb 2024 20:53:13 GMT  
		Size: 6.8 MB (6789358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:3bed2e2f777a99c1c837fb5ac437f78da61bb3401a5f40468aef8004b47b3f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19552502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0903350a20cd0f98d2e7485194e9a27dbbb163464e3a1857e3f9e6bc9906417`

```dockerfile
```

-	Layers:
	-	`sha256:a0d02c15021859df49c2da4f9d2a9204fc231ffffc677ef5aa981b80193fbb52`  
		Last Modified: Tue, 06 Feb 2024 20:53:13 GMT  
		Size: 19.5 MB (19541182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211603a7280806bc051468348b0029adf16482ee73db6a41bb64e8576bbf83b9`  
		Last Modified: Tue, 06 Feb 2024 20:53:12 GMT  
		Size: 11.3 KB (11320 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24` - linux; ppc64le

```console
$ docker pull elixir@sha256:786ac401b4703368b4e9af08340bf78166348fc7bd474086335f2a8b29271077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583912119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621b29062df0f9225a50c28673c330513cf76e92d261d4efa97d2144a69a6bee`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:35:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:24:03 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:24:03 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 00:31:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:31:33 GMT
CMD ["erl"]
# Thu, 01 Feb 2024 00:31:34 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 01 Feb 2024 00:31:40 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 01 Feb 2024 00:32:08 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c8fee1359a50ceab803cfc7fbcbdb50e8cb467db6a3203354529949ebe118e`  
		Last Modified: Wed, 31 Jan 2024 23:49:53 GMT  
		Size: 196.3 MB (196277517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14c9821fdff4abb8550e6aec3fe8228bc2bb5544d39648cd4ab82216d8d2dc`  
		Last Modified: Thu, 01 Feb 2024 00:42:07 GMT  
		Size: 245.3 MB (245304698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11782f2cbcd764ca3e6fb9d889efc9242dfc406d0a84aca748e6ebeec8e686da`  
		Last Modified: Thu, 01 Feb 2024 00:41:34 GMT  
		Size: 196.5 KB (196469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51e208241d51a59c4f0c7a2f9a22e2495497ac50b92d1c9c19ed4942b4b5a45`  
		Last Modified: Thu, 01 Feb 2024 00:41:34 GMT  
		Size: 772.2 KB (772189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1216a27a63ebd36922444ca822ad009dedc50b3258f4d59b99df26510eb5f91b`  
		Last Modified: Tue, 06 Feb 2024 21:26:23 GMT  
		Size: 6.8 MB (6789357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:f4b191059029a22d361d29011f3226cfa287c7beaf7443c5509269a2a3770812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19525549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54e7f6f284e2770fa00baa2fd0b2795deef8f0e8cc902053a9657dce8894ab3`

```dockerfile
```

-	Layers:
	-	`sha256:0f22f22a4f3608fca7e11b85608e39916007659708bb13a6c1bda7c6a89814fd`  
		Last Modified: Tue, 06 Feb 2024 21:26:24 GMT  
		Size: 19.5 MB (19515328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c41b4c64e02a5402e0e06e54404d3e1206a2e947cb78d69ffa2f017b1f2a953`  
		Last Modified: Tue, 06 Feb 2024 21:26:23 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24` - linux; s390x

```console
$ docker pull elixir@sha256:27c5bce32b075ce9e8885cab1019b3d6aeaa1a3aaf483d0ca5613e823a6604cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538628420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33bf896483aad287b89700677b6dfe7361de4ba7551043dd855a7865fa207a8`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 14:24:32 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 14:24:32 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 14:33:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 14:33:48 GMT
CMD ["erl"]
# Thu, 01 Feb 2024 14:33:48 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 01 Feb 2024 14:33:54 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 01 Feb 2024 14:34:17 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ecdcf8ccc5ce5336d916683310b1e013c65a510e5e5800558225199775e30`  
		Last Modified: Thu, 01 Feb 2024 08:19:47 GMT  
		Size: 15.6 MB (15643328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fd27dc397984da98ece9a2d55abf511e61b71edc88c38624d78b7fc0cb773f`  
		Last Modified: Thu, 01 Feb 2024 08:20:18 GMT  
		Size: 54.1 MB (54071240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b0db4f23942f60acef6ba1bd97c9d42b0327cd92d6882b65d1dd04594b47d`  
		Last Modified: Thu, 01 Feb 2024 08:20:44 GMT  
		Size: 172.9 MB (172923157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca94ccd1399a7b7cc71dfad42330c00e5ebba2a090c891c9e4cd7c541f49e93e`  
		Last Modified: Thu, 01 Feb 2024 14:41:16 GMT  
		Size: 234.9 MB (234938037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4021975b990591827f04731eaa1a154e18e3daa31e3dee4810facbaac4b405b3`  
		Last Modified: Thu, 01 Feb 2024 14:40:47 GMT  
		Size: 196.5 KB (196475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc2d6f30191dd52181737db1bb4914fd40a959571644c591852aca08e8baaa`  
		Last Modified: Thu, 01 Feb 2024 14:40:47 GMT  
		Size: 772.2 KB (772188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455041b917508109d829fafa8f9bc2f15ad2c1e92063bf6638f379f281e75294`  
		Last Modified: Thu, 08 Feb 2024 01:25:19 GMT  
		Size: 6.8 MB (6789313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24` - unknown; unknown

```console
$ docker pull elixir@sha256:702fe67e12db7a62174df36d5b6feb376c61c697a8b1c989275ec93778f16d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19377868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ced709afc569b153e1364d86ba5412a5276b9d8e79610a674090aeb488e27c8`

```dockerfile
```

-	Layers:
	-	`sha256:95f9f8625ff0c9dd84eb79925cd4509cc7f738b9c68941b9dbb1922edf34864a`  
		Last Modified: Thu, 08 Feb 2024 01:25:19 GMT  
		Size: 19.4 MB (19367679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dee3bb055dc9c5c62b6ca3d4a605ab734fbceaa587f0d0bd1762357458dd07`  
		Last Modified: Thu, 08 Feb 2024 01:25:18 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
