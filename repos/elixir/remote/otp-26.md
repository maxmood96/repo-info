## `elixir:otp-26`

```console
$ docker pull elixir@sha256:35e0665eb4c77ff7b0fdff317f23a91e192e4724d6ad3130e7be000cd8af9298
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
$ docker pull elixir@sha256:3499372cc61b43f3a12d76b237c58199816102ae04272aa814a967fb97b2916c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.6 MB (580631454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d9c046c715cdabd8ceeeded306cd9d452102374955c693917a1f24917842e7`
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
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:785a922c8cb57010af1e1190f82e5877abe9bf80e83f0357d2660322458dd246`  
		Last Modified: Tue, 13 Feb 2024 04:13:21 GMT  
		Size: 250.5 MB (250505454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c0c869d6a39fd0b524399901fc2cae8a2c597d00b2d3c218a81fbda7df1c39`  
		Last Modified: Tue, 13 Feb 2024 04:12:52 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241c840e40f50d08ec82355fb8d8ce9319e89130e2949fb0811e9f09c806a92`  
		Last Modified: Tue, 13 Feb 2024 04:12:52 GMT  
		Size: 781.8 KB (781811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6910baac424eaf278ddeaa3edb90148d266034625215dfc11a80b97fb2a197f`  
		Last Modified: Tue, 13 Feb 2024 04:56:04 GMT  
		Size: 6.7 MB (6737618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:4bb091dfcbb5da288bf0ac3a150f1c60785b5765525186324f377a2d44073a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19655148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac218b1993896b7526e120b3c3e6ce6d5645bb129daf5a7c0aad01928681f9f7`

```dockerfile
```

-	Layers:
	-	`sha256:52dca6da3744265928a014b5222ac943d477c4410f62b9e70013e189bcd78d95`  
		Last Modified: Tue, 13 Feb 2024 04:56:05 GMT  
		Size: 19.6 MB (19643849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6e7f60ac830645358f1aded9bb4fb570ca88d0ff3b943cf1ca5f43f5076c09`  
		Last Modified: Tue, 13 Feb 2024 04:56:04 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm variant v7

```console
$ docker pull elixir@sha256:8b4a8168ccd65b41b885985f76de44df4c7167d9ecee91a1a764023a8c7879d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.5 MB (514529445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a59ccf8a8eb83ba8905a0bd16bd37d1baa5f4c9d9e9945b367f5558532212ed`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbdd712885977c538429b59aa851dd5be6499412cb7b2ba0cb37a20b9186252`  
		Last Modified: Tue, 13 Feb 2024 04:29:25 GMT  
		Size: 167.4 MB (167437433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28c0f8d38ba6390acc5eddc34faa7f401aca676046e76c6a0a6753d05bc1b3f`  
		Last Modified: Tue, 13 Feb 2024 18:44:23 GMT  
		Size: 223.9 MB (223899026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08521bdc3e5afc6fc4d2ff1be8c1f5016c7963042d4c18a12264e11c0a75967`  
		Last Modified: Tue, 13 Feb 2024 18:43:38 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a96053e50c1cf538568906892d9a27c6d26632ecf83583d9fbaa80b643aefaa`  
		Last Modified: Tue, 13 Feb 2024 18:43:38 GMT  
		Size: 781.8 KB (781811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8761a3a2e794780e0eadb9dc12ae586ec157c0316c608820a5adbf49ceefc899`  
		Last Modified: Wed, 14 Feb 2024 03:20:05 GMT  
		Size: 6.7 MB (6737553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:0ea4eee560df28ed6220bbafe497804deda7f8453bb3d444cde7652aa5e1a172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19489475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b2f85673c77d0180456323955d5d7782b481f874ae44ec0d7ab9f56905c293`

```dockerfile
```

-	Layers:
	-	`sha256:bf2bdc6928976f4a5c495e44862bb7fd47928f223f43e2ad14f41e1ce8c7dced`  
		Last Modified: Wed, 14 Feb 2024 03:20:02 GMT  
		Size: 19.5 MB (19478114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ebc854bbc6b96a97c264142ccd0a93b9047d697cd5cb81762222e311744f5d5`  
		Last Modified: Wed, 14 Feb 2024 03:20:00 GMT  
		Size: 11.4 KB (11361 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:56da5bfcaffca246dd20fb171f4b464fd66871547afea6cfaec23b4cb66ca842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.8 MB (565808975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e801105f196c3355c4ed9bb38eb754007bdc3e0b6b5970878278a6f0da46318`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abc8b7accd0e9bdc9cc49eb9156409ec3f7da3e3f756461cedc2eba2531331`  
		Last Modified: Tue, 13 Feb 2024 01:48:18 GMT  
		Size: 189.9 MB (189883632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea207c3b9e88bbd182bada64c2cc407f4fa3cc018c79b6c5681e5ae43dfa6e0`  
		Last Modified: Tue, 13 Feb 2024 03:57:08 GMT  
		Size: 244.0 MB (244046650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff23b2ebfd0d90b792b000573b920d75b4b75dfcc23b1b02941696b2bdccb2bd`  
		Last Modified: Tue, 13 Feb 2024 03:56:46 GMT  
		Size: 195.0 KB (194965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25a2a3df511be591ead5dd59490b11b8ee1939b2c40215a5d14baaa7e99693f`  
		Last Modified: Tue, 13 Feb 2024 03:56:46 GMT  
		Size: 781.8 KB (781825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a65ba1e4867d65ac6b5e33b405e2cdf1c3a43e14669ff4edd1d674b7a302f3c`  
		Last Modified: Tue, 13 Feb 2024 16:54:41 GMT  
		Size: 6.7 MB (6737597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:96607ff49310e6bb2d24f47e6b12217bb894711b153e37245f86f35fc2ed6920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19663824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860a45add8d30759c6801f01e252c208c34e5125da5aa72f4b1aebf24047718f`

```dockerfile
```

-	Layers:
	-	`sha256:77e36ac4b088946254bbf16592f969d8189f23a1873620893bb268083308083b`  
		Last Modified: Tue, 13 Feb 2024 16:54:38 GMT  
		Size: 19.7 MB (19652517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0163d598caa5cc959e4408441eef6cdabf775989ba219937a9aed223c604cd6`  
		Last Modified: Tue, 13 Feb 2024 16:54:37 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; 386

```console
$ docker pull elixir@sha256:d9f70b3e21753d766658fb86f6a4a1a25ee82cd668b386b8394b21e727b247df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.7 MB (580654689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32aed6f2d4f6b169f2c5881512ab6ab61a5cafc116c6a9e10285af9bc03587dd`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830822b5fe9fcce0a36786775e56d3ebba121abaf50d97e715d9bb63fb9b2291`  
		Last Modified: Tue, 13 Feb 2024 01:31:14 GMT  
		Size: 55.9 MB (55927728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebf2d43c0cb851da7dfab2d9ae6a682f338a112bb35e5720e1105ddc4e26dda`  
		Last Modified: Tue, 13 Feb 2024 01:32:00 GMT  
		Size: 199.9 MB (199872460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6aa3b7529ddc97bed1f050e14b486abb33420e7c36ff4a9a8b5743f6a8c6ed2`  
		Last Modified: Tue, 13 Feb 2024 04:34:54 GMT  
		Size: 244.8 MB (244814640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ed603bdd1f49ae3ff2dd5cdbbd75f9913a634e635ce600dd50224c51f003d`  
		Last Modified: Tue, 13 Feb 2024 04:34:11 GMT  
		Size: 194.9 KB (194908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93f046de51bb97892b85553461de2004ebae2b4531920357e87a1dc261dd744`  
		Last Modified: Tue, 13 Feb 2024 04:34:11 GMT  
		Size: 781.8 KB (781811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2211ca26c57342d38401c66ca775dc8d55b90b0740f0ae43ba64428735e7fb8`  
		Last Modified: Tue, 13 Feb 2024 04:56:27 GMT  
		Size: 6.7 MB (6737592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:b4ecf4b7abaf4def7742281ef3f7ee4d1f22364967af746d494814e917077907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19643316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900f6997c2c6b4aa13d233aeddd3632af1887afee7a92804f47eaf9ee8c88a8a`

```dockerfile
```

-	Layers:
	-	`sha256:93c19cdbde0383b1fdf6c533e5bbf92353e5cf6eb806aa5fd8f116d895628d96`  
		Last Modified: Tue, 13 Feb 2024 04:56:28 GMT  
		Size: 19.6 MB (19632041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88077ceceb301d664ae8db926f3e4b755bdb2500a77395e5fb51d5b06624b969`  
		Last Modified: Tue, 13 Feb 2024 04:56:27 GMT  
		Size: 11.3 KB (11275 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; ppc64le

```console
$ docker pull elixir@sha256:464e053f25ec7b0f63ebb9372087a3524adffa117346f81257fba725d7a8ff26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585250516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26adc7991a014b820a3aa313fb675d92af5088cde71c910fba19db3b76cf9c3`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfa650184f634b15bc0f1ddd50aeaa4b660e83cbc9fd51d576c3910ebaaad53`  
		Last Modified: Tue, 13 Feb 2024 07:37:27 GMT  
		Size: 16.8 MB (16765559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c4f70ca0212997eb1b2c82b5f1feb6920ff2654089e68975cba4b400a4451`  
		Last Modified: Tue, 13 Feb 2024 07:37:46 GMT  
		Size: 58.9 MB (58872935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b71a4e8c3360ab2f0fc44790fa318623d9b5bf860bb3aff76bf5e481709053`  
		Last Modified: Tue, 13 Feb 2024 07:38:23 GMT  
		Size: 196.3 MB (196324754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc2e0a2bd351c947ea830b0130279f88f723b56ab7249458b930a8addcfe05a`  
		Last Modified: Tue, 13 Feb 2024 11:23:45 GMT  
		Size: 246.6 MB (246618358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fade03ba40398851dbf11a44c5652aa90e07e1ab8bdad58a72496d4239aedb`  
		Last Modified: Tue, 13 Feb 2024 11:23:10 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ddc7436593497774f1f96f12c9a40459f80ea1a09bdaaafb6381fc895860f1`  
		Last Modified: Tue, 13 Feb 2024 11:23:11 GMT  
		Size: 781.8 KB (781811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5257572be314efbd86869324e11f6de4b9d8071e18e34e17eda6a1b3d60a8aa`  
		Last Modified: Tue, 13 Feb 2024 15:16:52 GMT  
		Size: 6.7 MB (6737613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:b1fce62914c2410415074053f210ffe9f910ffd6e050616d25fca6ec7f18a900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19617518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b37462826bd737d307672c647e230badaee537c3c1a98e7ec3889e3407f3cb`

```dockerfile
```

-	Layers:
	-	`sha256:b22d49f410061ca5b4d192e5940a2ed745021b30a3b79dded7b6778ce1250532`  
		Last Modified: Tue, 13 Feb 2024 15:16:47 GMT  
		Size: 19.6 MB (19606187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de347d4ba10887cd7c55db7bf68669d7d144905960d23053c2a9750da3a1aad0`  
		Last Modified: Tue, 13 Feb 2024 15:16:46 GMT  
		Size: 11.3 KB (11331 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; s390x

```console
$ docker pull elixir@sha256:b75f99cabb317769714bfc2ff378aa9a95b7aad5405f828b399d0e4f59623307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540032654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeeed1021ff8ca2736aab7ace76cc083b68f7a90333c20a92403f5d65c874fb`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb188cda5ee038922dabb4ba5c3c81be9096f05e1d4d4cdeab23a983e578d77`  
		Last Modified: Tue, 13 Feb 2024 02:59:09 GMT  
		Size: 54.1 MB (54076017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3290768c093f8e148cae12eaffa30fa6cd78ef3fa1c9639c07459aa92948e70`  
		Last Modified: Tue, 13 Feb 2024 02:59:33 GMT  
		Size: 173.0 MB (172970685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036ab26c43915afcd09d7d734d87ad6e6a38f12e92835fd9012337c35b5aefae`  
		Last Modified: Tue, 13 Feb 2024 03:54:25 GMT  
		Size: 236.3 MB (236310987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227109fba8218f553c5b33890afda3a2a25c63f58ff29cfc33b8fa76beb91077`  
		Last Modified: Tue, 13 Feb 2024 03:53:57 GMT  
		Size: 195.0 KB (194965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41127243b8ebbda7e026f188d00714a31cc7edd70aca70e77f3a2f32a7f351c4`  
		Last Modified: Tue, 13 Feb 2024 03:53:57 GMT  
		Size: 781.8 KB (781811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a9c54cbeba74f7516eecb6d6f312d77f5e3f572225be4e42c37dc42163a9f9`  
		Last Modified: Wed, 14 Feb 2024 08:27:57 GMT  
		Size: 6.7 MB (6737591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:6402f57dfded67139d6a995a3b095ac6b8f8f2d6f92a36e2a10e1d9996eb7ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19469837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130cc7d647e14ff1b8d2e3533d5e6ee552b30b100bb67858838defba2054b63`

```dockerfile
```

-	Layers:
	-	`sha256:ca144e3d85a57abf27cbdea6dfac68215e2cc2a20005e75ca9dd78eb45e89119`  
		Last Modified: Wed, 14 Feb 2024 08:27:54 GMT  
		Size: 19.5 MB (19458538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa186423e2196ee551e69f8132cd47a3c16b4126e60d925afe9ced6a7d63d132`  
		Last Modified: Wed, 14 Feb 2024 08:27:53 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json
