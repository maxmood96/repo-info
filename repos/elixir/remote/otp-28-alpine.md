## `elixir:otp-28-alpine`

```console
$ docker pull elixir@sha256:bf2b6f75b6318be06df896ab0acafa78a882291807988e7c16ea1349393a5db3
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

### `elixir:otp-28-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:764e698e4931b7f55d1232408cd337a41bbe0545a7c696d3585938e5b2bcab91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63315219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505dff8533e8b8671ff64c7ede416e1b447406d37e08b29449bd2f903193a1a9`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:05:29 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:05:29 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:05:29 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b21b7e8e6bde7efd736e800ed7cbd88cc7a7a70f86346804702193d851c82d`  
		Last Modified: Wed, 08 Oct 2025 23:05:06 GMT  
		Size: 51.7 MB (51740774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c0e89b1d3da1b8815661cd456734db1bef775e5989647475164e9e5d37c29`  
		Last Modified: Sat, 08 Nov 2025 18:05:42 GMT  
		Size: 7.8 MB (7771993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:dbc64fbb3d29319f48b975fd611d743e8de51bd3cf50473aca83efc2bc57b783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8d7275a4215ed9d9588307470fcb14bcbbe228f61c1d0ceafde0ae2e39743`

```dockerfile
```

-	Layers:
	-	`sha256:22584cc516774a0ff37e515fc40a912ceb1935530653d08e22545059e514e25e`  
		Last Modified: Sat, 08 Nov 2025 19:45:09 GMT  
		Size: 286.5 KB (286539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00548bac3d9f00f6d9b2c2f969a9b87e90f28a687bf00b662a6cb59aa6fe58cb`  
		Last Modified: Sat, 08 Nov 2025 19:45:10 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:d3b5bc6880a7d9c052aef011331754fd7afe1f82d85eb381bf83788e0d29cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60273663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1c97365fec359f91bd4b281e339a06ebd199855e691aa16051819c619db888`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:04:19 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:04:19 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:04:19 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af20cf6e740711faf63c8772bf9ff5cbea4910b84edc3cb6232da24c0d3a9652`  
		Last Modified: Wed, 08 Oct 2025 23:50:52 GMT  
		Size: 49.3 MB (49280868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f1ce982a70e2f93078db3df3551b0c31a500ffab23370e7bb809ce095e4afa`  
		Last Modified: Sat, 08 Nov 2025 18:04:34 GMT  
		Size: 7.8 MB (7771240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:30ddd7a0084f8d63512e835ff579a23118421727adc736290b0310ad38070f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faba6ee994194d30161131ba136a889a177651906ef6f457d9e633e474cf618`

```dockerfile
```

-	Layers:
	-	`sha256:25d9bac5e553707aa8e149c2c8af85a06e8b8058f10da5fa5c8dcdcc2e31ec8a`  
		Last Modified: Sat, 08 Nov 2025 19:45:13 GMT  
		Size: 285.3 KB (285333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaddc75ffc2cd4294c6bb883aff2d7c2335c63621c44e17d171da4693bfd701b`  
		Last Modified: Sat, 08 Nov 2025 19:45:14 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:3e0ec19c988be96d7b4f49c96bc6ea8916a495cbb1137d6ad29420c87c00d0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32fe6cbc8ceb1a6ea3b44fec42d116aa5164949ee256c7696d51d307f709f5`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:04:40 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:04:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:04:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a0bf09d92594b9c0b7efa2a7ddcd2940aacbdd712d0adc25177e9e9226d601`  
		Last Modified: Wed, 08 Oct 2025 21:51:10 GMT  
		Size: 51.5 MB (51499879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549b72fa47030528d163d9ab78fc3da0f239cef45627e39d1baa8cfdecf564ae`  
		Last Modified: Sat, 08 Nov 2025 18:04:57 GMT  
		Size: 7.8 MB (7771937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:37097307c253a1491fb885e4d046f6594a371dad9c57f9a59ffa8d2728b1a903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 KB (297864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5347d40dadaeac6c5ea62c8fa0b98c41e532504a6d9e17912280de14cd0f9279`

```dockerfile
```

-	Layers:
	-	`sha256:10587515fb43126ca2797292c17452fb4d40f71da25e449a123c55593262bd85`  
		Last Modified: Sat, 08 Nov 2025 19:45:17 GMT  
		Size: 287.4 KB (287351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbf9da021a2a40997c5bd15863326781efc4fa6bf6484bfbb4ed97ae9a7bceb`  
		Last Modified: Sat, 08 Nov 2025 19:45:17 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; 386

```console
$ docker pull elixir@sha256:de61654ed57c3f9f558f80b0b219c3e4b85e304ccfd565e49d13317c095001d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61591433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ddb74eeb326df2490d2c7e04fb0255a4916169f4bd7294e0747ca6e69cf2f3`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 17:59:53 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 17:59:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 17:59:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd4d6ac4b4aa194d2a98b8b84d0786525c1faac8dfa1ebf2db84d0d32c9c2a`  
		Last Modified: Wed, 08 Oct 2025 21:42:14 GMT  
		Size: 50.2 MB (50201781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd33e2bf76cc99548eb908f018f340749095b4263a0b8055b1b7c8f28cfb18f`  
		Last Modified: Sat, 08 Nov 2025 18:00:07 GMT  
		Size: 7.8 MB (7770721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:16fc333f2e86ed4c6dc29385cf4df601df9492524fa004e4c72bf64452f766b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 KB (291867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66737137dcaa6bff181ebe4e07de1e0e4c947bbecb84edca5959b1a293b58ef4`

```dockerfile
```

-	Layers:
	-	`sha256:632c68e48977f8315e18acecd630ed0c63f8bdb18aeef2808f0f70d363a82b70`  
		Last Modified: Sat, 08 Nov 2025 19:45:20 GMT  
		Size: 281.5 KB (281524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1355ec54e9a884d972a498b87c9ff7c9f63d65d80dc59cc30202624a7c4d8255`  
		Last Modified: Sat, 08 Nov 2025 19:45:21 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:dbc4a870ca7d176c74de934b069d8f0d356a277c872b06a94b2a709ff69c598e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61884545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a03feee7ac0987a06b65cd52dd4ccb32bada3776ecde79069ec7e89ad77f3cd`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613342ef6ada9be614521afc12925dfedb015ef257c71646af27f57819d7b1d0`  
		Last Modified: Thu, 09 Oct 2025 03:42:12 GMT  
		Size: 50.3 MB (50294300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e48056228a63bc8acb789638789989d430f42f1da6a4118ada0e4a54b6be853`  
		Last Modified: Wed, 22 Oct 2025 18:07:59 GMT  
		Size: 7.9 MB (7858004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:74841ce95cf77cc19cdcc9f2575c80756030af979c4572f133b28d3cfadec116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 KB (290860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2359946397e99c35731c8bfa0d12e3a874ba4acd3159edd2d8b11f0f090da6`

```dockerfile
```

-	Layers:
	-	`sha256:6f2cb9b23049eeb8bd744321fcf83669e03d8c13975d34d15813e8dc9fff54af`  
		Last Modified: Wed, 22 Oct 2025 18:45:23 GMT  
		Size: 280.4 KB (280376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a868f4f8a4113fc023984734974e63cc61f4580dc189a15534f1e187d0215`  
		Last Modified: Wed, 22 Oct 2025 18:45:24 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:51b5542be33401f1d0dac0ee1c053cdd6bf8274485e2bdad17b8ef2caf54b60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61531528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113de22c3cbf61ec3247883bfd7b6462c86f646bfa36e19c524541e81c7b86b`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00ef9c70cf06e0ce864120c57f04de21823092dd69a5800141558566fe50efa`  
		Last Modified: Thu, 09 Oct 2025 02:35:28 GMT  
		Size: 50.0 MB (50024050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ad0fc056642481bd9873ad980f826c43877e922b5072794340fd31f16c89b`  
		Last Modified: Wed, 22 Oct 2025 23:40:56 GMT  
		Size: 7.9 MB (7858234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:03330c4378e6a6cf73563d342b44f574e090b99b901fedc214bdec982fce9402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 KB (290758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd07e8d8f0c52bf037e7536727c4ea60b6e09a95056ce0a6398bcb0940271bec`

```dockerfile
```

-	Layers:
	-	`sha256:29dd1289c0c2327af8ce566292d7fe197555544fdf266c5b20032a836cbaca36`  
		Last Modified: Thu, 23 Oct 2025 00:46:07 GMT  
		Size: 280.3 KB (280330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fdf2510022efffe4050ba0d9d562649a70271a4b9ed5d768deb40fac06bdf1`  
		Last Modified: Thu, 23 Oct 2025 00:46:07 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json
