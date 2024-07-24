## `elixir:otp-25-alpine`

```console
$ docker pull elixir@sha256:29c41ec134c1ff7dcb69eb70bbf815530c5df85d858a4fa68e4350e9584280c1
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

### `elixir:otp-25-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:7ef8e5deee5f1676b2c8c0a65594e6a22832b6e1b5d9b310b4e788c1eaf1dda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55248285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61cf9e8f4070fc8320373de64d4fbcb8d19bd4e7e2d26dc31e9d81ee90fe143`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d593aaf8ff4b2324d2497ee03ec3c5b25b86bdd130590bc85467e0cfcc302059`  
		Last Modified: Mon, 22 Jul 2024 23:10:08 GMT  
		Size: 44.8 MB (44842497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c2587d5b6520d57014de4f35c74e1e3697f04312e714896330e81e3679892b`  
		Last Modified: Tue, 23 Jul 2024 00:09:05 GMT  
		Size: 7.0 MB (6990148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d2532fcd20f774420f4d4c4624f381badad363eb060b215e96f6895ef8249b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 KB (287001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e98463b472de60d6f9a5f4366cb23b0e427b212af6e61313246deffcead2b4`

```dockerfile
```

-	Layers:
	-	`sha256:b6630ca70434de96769b1967df70d3ba9463ef585cf7b947818338651ee31c38`  
		Last Modified: Tue, 23 Jul 2024 00:09:04 GMT  
		Size: 277.5 KB (277507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f30017f07e188338b198edaf2d84f7feb6414efb22b3cbe042e5d953f40e57`  
		Last Modified: Tue, 23 Jul 2024 00:09:04 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:2952b31a0cda6fa45eb1c09888db0033d4dab88ff239d9e4a86b7cddf6db3a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52686676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27bb17f7390092ff476b5d77db2c5bf733300738c46925fd751ed1f1b5d946`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05dbc7272b483760bfe851e9f3c8fb7ff8b8206dae802995a0483ddb44ce76c`  
		Last Modified: Tue, 23 Jul 2024 13:34:01 GMT  
		Size: 42.8 MB (42786247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28972c8d1fc033d4090b5ca42b13c1108d625abe09babbcab3a16044d73ed9e6`  
		Last Modified: Wed, 24 Jul 2024 17:45:11 GMT  
		Size: 7.0 MB (6989865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:a30edccf4059557bed0dbcf34b0e0ab4772e6d1eb1532f851ee01e5aca6e80a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 KB (283538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a4a642c113d059f0d0589085717dfc38dc04e4ae0a13be7e1757a6de062405`

```dockerfile
```

-	Layers:
	-	`sha256:23bc3eee6a6c7b2d1ae42cec34c51e3d9d0465863e038960561bf113780deaa8`  
		Last Modified: Wed, 24 Jul 2024 17:45:11 GMT  
		Size: 274.0 KB (273963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c15d85cdeaee1fd865bc05b7acf52abc3bab1ff24750b41032ee59f3995eb39`  
		Last Modified: Wed, 24 Jul 2024 17:45:11 GMT  
		Size: 9.6 KB (9575 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:f8ce4d795f06510759be14429f83de3f1bdf8efaa38852bbff26cbe5139e76a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54973909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e53f785bd17d0cc80eb6448cce9da478554eb385eb98fd352328a50a944bb5`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e65e2cf800f2336d725128324b4fc004bbf27a1d7c883cb503bcbae737bf08`  
		Last Modified: Tue, 23 Jul 2024 14:49:28 GMT  
		Size: 44.6 MB (44644282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd91051c433d97477d065fd1b42042be88b6bbcbd5c15e1524bb33fceb63b9aa`  
		Last Modified: Wed, 24 Jul 2024 14:31:03 GMT  
		Size: 7.0 MB (6990133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:7ac16e698a29284f37261edbc6e622c8285690492d0c010b3be74f2b76663e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 KB (288568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c72e3e9bb50096334c2a8b3ff521a7c479e83a04e4b986b7ee8304c96e8db`

```dockerfile
```

-	Layers:
	-	`sha256:4b8c71cc31d3b3da73c4d2d566bc820fbcc9c74e8d5de2c408f8796971a4f09c`  
		Last Modified: Wed, 24 Jul 2024 14:31:03 GMT  
		Size: 278.7 KB (278688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:526bbc72142021d19b50ce0ed265530ec3d9aa3b9354d7a505c69a3e51180b28`  
		Last Modified: Wed, 24 Jul 2024 14:31:03 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; 386

```console
$ docker pull elixir@sha256:8d9e9d5bcb604463f2b3757052f5136c7cee3ba889557500611160bcec60f728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94c0dc684733f29e5c10b53ce6150f8cda1ef042bcf436de0d725c1b7f09ac7`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4b89ccdb53a74f4511b9bfda30b9e20adaf34e51ec2676bff8c7d2c801603c41 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d44793d00d423eb1fe30b1af6f1e058aa74668822ff05f0f574c0e83d5379359`  
		Last Modified: Mon, 22 Jul 2024 21:39:15 GMT  
		Size: 3.2 MB (3249679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f0b5b11c6cdfee41bbd428484aabd96fcfff80b89fd26858090003ec94025a`  
		Last Modified: Mon, 22 Jul 2024 22:16:22 GMT  
		Size: 43.6 MB (43631903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b6c2aef786f8977ac94c190697e07965e41dc605805f0af0836eed45774fc`  
		Last Modified: Mon, 22 Jul 2024 23:07:32 GMT  
		Size: 7.0 MB (6989848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e8b023882b30e2f369c468fc8ad1223a8c65bb109fbde40ccc432d544146021f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c14bfc3f20ad95b051c9069bba754fe232e232e704aa1ce8fa187e670cfaee`

```dockerfile
```

-	Layers:
	-	`sha256:d4c8e6e62722c4705c66e6f463d87321b5b4ea5d29e70998e319cabb2471bf89`  
		Last Modified: Mon, 22 Jul 2024 23:07:32 GMT  
		Size: 272.8 KB (272778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af916e5dbcb827d78b8dbb9940aced7a3fa5016de0fd40c4c394a6a919726ae7`  
		Last Modified: Mon, 22 Jul 2024 23:07:32 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:1b15aaecb3d744936825f78d0c23089eff1ceb1f58010d971750bcc86e1f468f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54082729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc005999610192a2cf0ad5598c0d8220779c3defd046b1a681650dd1e8a380`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c1ce81388a283e32b3a88f1c5d595810be4e0278afaaf170561f56660e742`  
		Last Modified: Fri, 21 Jun 2024 01:41:38 GMT  
		Size: 43.7 MB (43735931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1e64bb22885d21aedcab53aa3743b17e655d6567e30434712a8cc823e6c18d`  
		Last Modified: Tue, 16 Jul 2024 20:10:35 GMT  
		Size: 7.0 MB (6989765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:3a2c3968eed7be9742ce34f43c17b594c20f679a8a4920002b79430f93f736ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c1534b36542faabcfc10ac4bdf295cb9a1e7038899f2dae09d5a9c66a2cbb6`

```dockerfile
```

-	Layers:
	-	`sha256:ff9508b5bdb65fb24933874a54436395eec47478e9436f21fe48ed239d0d3822`  
		Last Modified: Tue, 16 Jul 2024 20:10:34 GMT  
		Size: 272.0 KB (272009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61eb298b9f6834ab651faafff0e57b2ec44ad2dd1768ab4f6ab1c6cd81633f43`  
		Last Modified: Tue, 16 Jul 2024 20:10:34 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:f8d2b589ea20c126b67602738124761375f37a67d0552e4ef16e88b6e011045a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53352702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582af59287f09176be4a4a6a68c7189496957df39062c3b55721fb12b1e9af4b`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["/bin/sh"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e2daffa82a33f2d874afcb99e4f8d5a99140dde6a39957475f0316c15994f`  
		Last Modified: Tue, 23 Jul 2024 10:07:38 GMT  
		Size: 43.1 MB (43133060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e73a93a82637eb6e99c60b58e5690769297aeb7e172fe689ab2686ef774091`  
		Last Modified: Wed, 24 Jul 2024 14:56:46 GMT  
		Size: 7.0 MB (6989750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d2017fd7e809fcfefabe50bb4dcd23406fbfe5f74b92511d31cbefc96f879908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825f98a2a93b54e28409256c734e4eb7731b3827a754dd2b45fd504527110659`

```dockerfile
```

-	Layers:
	-	`sha256:3359d5e2989d8ada3b8cd708945bfa44d55ebd44198db387a88ca60a049c63b4`  
		Last Modified: Wed, 24 Jul 2024 14:56:46 GMT  
		Size: 272.0 KB (271981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6962a8aaf0dc1594d6277ecf29db1d9d3f5eefeb3f1efe6dbcd99bc58c876361`  
		Last Modified: Wed, 24 Jul 2024 14:56:46 GMT  
		Size: 9.5 KB (9506 bytes)  
		MIME: application/vnd.in-toto+json
