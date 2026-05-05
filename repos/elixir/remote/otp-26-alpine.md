## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:e202dc4066bfd34990016a562696c1fed21d0dfdc911ae3c44d4704590e8d3d2
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

### `elixir:otp-26-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:28cc7a2ad7f42ab675ed6bb7b8450d2cf0749def8462e2d3261af7f79c183871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57527813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ff1e86e84e5340a25f80b7f4b94b92826e5fb7bcacb01373f3fab871ffb307`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 20:51:09 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:51:09 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 20:51:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 20:51:09 GMT
CMD ["erl"]
# Mon, 04 May 2026 20:58:11 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 04 May 2026 20:58:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 04 May 2026 20:58:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960f5dc58aede4e5d9f41649b6ea110904ce32a4bf95f1850e07b6d5c35c3b23`  
		Last Modified: Mon, 04 May 2026 20:51:18 GMT  
		Size: 46.1 MB (46105228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e6b5c414fc1eb90b72af607b402200215a392b725167adb68216c358bfcbd2`  
		Last Modified: Mon, 04 May 2026 20:58:18 GMT  
		Size: 7.8 MB (7792264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d681ee94b11e4fe0343d1cc932ebfc30c0cc53ee9bb5dde7503100917105bfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59ae25072bb28b6fb07812c8821e7a0ef9f6f52134a2c8ef1f5f1d08aa0d0bb`

```dockerfile
```

-	Layers:
	-	`sha256:23907a943c6d7fdea90bab6826a458ba5f286c5ae61ada125c15a1758ab8bb6c`  
		Last Modified: Mon, 04 May 2026 20:58:18 GMT  
		Size: 279.7 KB (279726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecdd01ddb269d3ac76d199558eb17b31b500e700796ddb4858a52b9d5e4402a`  
		Last Modified: Mon, 04 May 2026 20:58:18 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:a3485ec6c52e657ff1d1e54fd111028e793aac787ed97a25b3b6d9fbb6b43874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54663062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a003c653913b6b88d1883a34a6fa7422a1e05960b980081e496e30996c9424d3`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:25 GMT
ADD alpine-minirootfs-3.20.10-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 20:54:58 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:54:58 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 20:54:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 20:54:58 GMT
CMD ["erl"]
# Mon, 04 May 2026 20:59:18 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 04 May 2026 20:59:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 04 May 2026 20:59:18 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:70293f0413d2297be1651e9765a7327f173f0d76bf7e1229f6e604faf61552c4`  
		Last Modified: Thu, 16 Apr 2026 23:54:29 GMT  
		Size: 3.1 MB (3100051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3247343b8c05cf556e9f2b322e7687293928435cdf79441a29ce7ca2f43713e3`  
		Last Modified: Mon, 04 May 2026 20:55:06 GMT  
		Size: 43.8 MB (43771233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb55c1248eebd41b9a5851a2e039efdeb9a328dff39e7755dc37b72af5058ef`  
		Last Modified: Mon, 04 May 2026 20:59:24 GMT  
		Size: 7.8 MB (7791778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:3b3bdc792075cece08c70121b6082eaa471abc878edb7dacaa30ca3961d4258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 KB (284994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8911a6d36769b9d157e33bc41b015b9749c95c68806b4765f6405a3f181d64a0`

```dockerfile
```

-	Layers:
	-	`sha256:c7778bd48742c54cf5cdf6c90bfb41e8cfb8f1c4100ad915de1ce6ce16780519`  
		Last Modified: Mon, 04 May 2026 20:59:24 GMT  
		Size: 275.4 KB (275439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194fa85fd3e74540d078076ece6fbd6193f3174686997030e8597be95fbfea0b`  
		Last Modified: Mon, 04 May 2026 20:59:24 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:73ed5c6f134ab847d65201e68637ec65be4f798a317dab2359d8174a7785b377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57786254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fafbc91253f09bceababb95783e22a8568258f94abfc6953e06d54568e57330`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 20:50:49 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:50:49 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 20:50:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 20:50:49 GMT
CMD ["erl"]
# Mon, 04 May 2026 20:54:52 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 04 May 2026 20:54:52 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 04 May 2026 20:54:52 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20cc7d90abc9a933fc14b2c3de4b7e52c4ca8f3fe8875be637c6c77d0792d9b`  
		Last Modified: Mon, 04 May 2026 20:50:58 GMT  
		Size: 45.9 MB (45901643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4961c18a3a7d40c617987f864a1532425b7238ca71e19105727eea48e4f8295c`  
		Last Modified: Mon, 04 May 2026 20:54:58 GMT  
		Size: 7.8 MB (7792292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:479cb1e21699f1eccc1ecc33c0372d64f49d06a5e454c5ed4d3d8c781e8e9712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 KB (290085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56ad85af6ba1c08a6dfdeb6dbe446b520a7a7309c2f85afa7402528b4a812dd`

```dockerfile
```

-	Layers:
	-	`sha256:db3727416ce6f031e9d9dcde747f0ae3cbc7280feff1e8fcf50fc3b3fd0565a3`  
		Last Modified: Mon, 04 May 2026 20:54:57 GMT  
		Size: 280.5 KB (280507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf53dba8f68e8f2d9ba3b2175671e2ea8f1b6d2fd4822d0aa46516c437a7da2`  
		Last Modified: Mon, 04 May 2026 20:54:57 GMT  
		Size: 9.6 KB (9578 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:042fd2c7e340ac28ec4d64a4caf2c9ed1706c6f694dc3221eec0adb792825090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55971742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec06c182177ba69eed4aad7b0bd4edc8deadc00e986304896bcb599b795abe7`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:41 GMT
ADD alpine-minirootfs-3.20.10-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:41 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 23:50:49 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 23:50:49 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 23:50:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 23:50:49 GMT
CMD ["erl"]
# Tue, 05 May 2026 00:12:26 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Tue, 05 May 2026 00:12:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 05 May 2026 00:12:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c3891655fe7f935c0edb9d8699a7880f85be6681344aea8dbae92ace3f127c30`  
		Last Modified: Fri, 17 Apr 2026 02:42:45 GMT  
		Size: 3.5 MB (3474644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9542a73ab5c26e257224589d3cdf3a5b35d885a34d5aeeb57bea1cdd49b8bffb`  
		Last Modified: Mon, 04 May 2026 23:50:57 GMT  
		Size: 44.7 MB (44705266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4afa1f4317c42a5380087bf6f9905e06c52c79ce7f702ea106a83f0fafcaf`  
		Last Modified: Tue, 05 May 2026 00:12:32 GMT  
		Size: 7.8 MB (7791832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:62ffd74acd2b4272a9b94ac967fdeac6d1f726c483bc5cc6d234cf2ea6ba2060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e14416fd2088f3e4fdac7a44d7c1bd0048d08db0a8909515aef77bc9503bb9`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbd4424d4377830b40ced6b20669c12cdce3fe2015a3a30e22d27975830247`  
		Last Modified: Tue, 05 May 2026 00:12:31 GMT  
		Size: 274.7 KB (274654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ee13113811274704c2983266841c881abd761af9df0c7aa5f89b313482cbac`  
		Last Modified: Tue, 05 May 2026 00:12:31 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:921721a538c5d62b541a213b59fd15887017718b46e9430aa941dd9c0cc4925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56130981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05ae15827042545fccd95e961c7d2801a2f75e5718c15f7d17ef470afec3801`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:56 GMT
ADD alpine-minirootfs-3.20.10-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:56 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 21:15:50 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 21:15:50 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 21:15:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 21:15:50 GMT
CMD ["erl"]
# Mon, 04 May 2026 22:11:12 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 04 May 2026 22:11:12 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 04 May 2026 22:11:12 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:20cdb1125d416be08241b781f88b15b42332c2aa8dbfa8619a7c0093274c033e`  
		Last Modified: Fri, 17 Apr 2026 00:01:07 GMT  
		Size: 3.6 MB (3581214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4230b535dcf1ae261cc7ab0065decb546ba43b0f70e06bc8b5fa4a7eee3816`  
		Last Modified: Mon, 04 May 2026 21:16:06 GMT  
		Size: 44.8 MB (44758021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05901488ac9368a980df72e313e6b7ac748870252e3869f8ab6f164a5de5588a`  
		Last Modified: Mon, 04 May 2026 22:11:21 GMT  
		Size: 7.8 MB (7791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b189841ba646ad067177e93e86560fcc85c2f7dfeac642bd5a2c8a02bc71c6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 KB (283012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c8591d4da4a77de231fd9f4ed4dcdf13b381078faadaa4e8966d52136312bc`

```dockerfile
```

-	Layers:
	-	`sha256:737f0ec51571415c1d45d8329846e2ceefbdee8eb2e876f7303a9ecaf5eea530`  
		Last Modified: Mon, 04 May 2026 22:11:21 GMT  
		Size: 273.5 KB (273488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00914fb861e0a4274e32183ba79847deedb0a901e3264fa1ef784d43a600162`  
		Last Modified: Mon, 04 May 2026 22:11:21 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:391ec8702f8a334a1aeb8c5d1feea58f0ce5e861bea2738841cd3678a7b378b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55677836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91fe5dfb32acb15963200c68a485e988adacf0839806012af52fc9fde33c114`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:58 GMT
ADD alpine-minirootfs-3.20.10-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:58 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 20:59:12 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:59:12 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Mon, 04 May 2026 20:59:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 04 May 2026 20:59:12 GMT
CMD ["erl"]
# Mon, 04 May 2026 21:17:08 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 04 May 2026 21:17:08 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 04 May 2026 21:17:08 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d38f020baf1fa2c87122ac85c7c1277244aec5f8a4a3f4c8a78bf2d10851e1e4`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.5 MB (3466630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6268f2cea2dd8ab474e15279d74cfd7adf5de7ea25a781cfacbb5f3a5a125`  
		Last Modified: Mon, 04 May 2026 20:59:25 GMT  
		Size: 44.4 MB (44419598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabbb641e2ae08f8e2f96546020556fa8b4f665e3ef5ad598ad3fcea5e9476b`  
		Last Modified: Mon, 04 May 2026 21:17:22 GMT  
		Size: 7.8 MB (7791608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:98c709f441f239df42b616071a3f7862155c1fc411e9e4878a76440f3f1afd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 KB (282946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5bfbcaf38939f10421b5dce4c8eb9629a49e5c033f8473cc028f06f94c216e`

```dockerfile
```

-	Layers:
	-	`sha256:14f15beb3b1d29a2eff13a50cf578af1b630193f296314a11d91fe75afb6c647`  
		Last Modified: Mon, 04 May 2026 21:17:22 GMT  
		Size: 273.5 KB (273460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:545ed606f3f50e7dd09f01b6264899552e1ccc24ec0d48d6c5e27c098f6f84cc`  
		Last Modified: Mon, 04 May 2026 21:17:22 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.in-toto+json
