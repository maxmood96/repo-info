## `elixir:otp-25-alpine`

```console
$ docker pull elixir@sha256:4d22ccfd286bec6306d44c35bee059bbb216219c085c45671a0e92eb06c34eb7
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
$ docker pull elixir@sha256:ff8343475b0cc320e6211967d8330cd8855dbe9791a65cbd1738d48650645eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58308535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11085c883618c5ee3e63a7af509e28235b198f4d12ecd1ef50ce4ac447d15c0`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77f07f4cca15ed273caf8b3d8426c02fcab61ccd0723aecb6398eaa208b21a`  
		Last Modified: Mon, 11 Nov 2024 20:04:08 GMT  
		Size: 47.7 MB (47689014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63189594cbb24243567cc5706bbcf54d2a9b8e07bc02050251ccaa2d992b669`  
		Last Modified: Mon, 11 Nov 2024 20:49:40 GMT  
		Size: 7.0 MB (6995714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ff7aeb11a5295bce1223f88990a5fc5f7bea4ae2fbb7b6687ce3ec2b30edab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 KB (288264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7c9646bc7e54e8063baa58105534ec7cd281291adab1d4e99f849a8e1c099b`

```dockerfile
```

-	Layers:
	-	`sha256:a31f4218054edbcadc258eec7bd41eb4cef91fa9052ad82e1a9c6bc5cd5949ae`  
		Last Modified: Mon, 11 Nov 2024 20:49:40 GMT  
		Size: 278.7 KB (278735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9bb432b266ef9b6ae831bfc917ef141b5b4a8fa17790e31b420744fdc52138`  
		Last Modified: Mon, 11 Nov 2024 20:49:40 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:5a71405ed1ff4a61b5aaa22d013b52dffe060e7f2b959b6b2637de96a915c629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55046447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b7dfef8e03845ae122c38b0716db8af1695fec935109da6c9f7ee77302c18`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8733d6e8ef8ecd39368f084f5ec8c08245ff70e8f37cf3a718c8797df03ee`  
		Last Modified: Mon, 11 Nov 2024 20:10:14 GMT  
		Size: 45.0 MB (44955501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d905a79aeee813c197a9ad8d7b52029f90183539af130f11bc61796ad8549b`  
		Last Modified: Mon, 11 Nov 2024 20:59:30 GMT  
		Size: 7.0 MB (6995444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:1735591fde6414e488e0c40833bfa35cdee7ac928cd87e4d3c306ac7c72dfc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 KB (284406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51b035cadccab826fbcfddc6acbceae4b0503d4154a18d60def6b16de14ee4e`

```dockerfile
```

-	Layers:
	-	`sha256:18d1bdf76c93720d70b6cd08b628ae2347d9dea686864b9afcdb79db5dc51560`  
		Last Modified: Mon, 11 Nov 2024 20:59:30 GMT  
		Size: 274.8 KB (274798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e81b534aa266d0f29e42a04d1c7388fb73382948f89f61c426cfb15873a4fe`  
		Last Modified: Mon, 11 Nov 2024 20:59:29 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:8c7ae3ae3e772e865e05b5ac2812e972969f40c74e001ed7a6c1bcad987dcbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59008309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28f9b90c926e88b144801b004d9c137280a26f6cc87e920b1a17a5ff9a15a39`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d984282065fbb1dc33ee218124875cd43c92d4b54040fad420ed50cb2ea827`  
		Last Modified: Mon, 11 Nov 2024 20:08:52 GMT  
		Size: 47.9 MB (47924976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc640458370a4a88e01373d59252b81d8c2811eb941f64ef89ba9b47c42f375`  
		Last Modified: Mon, 11 Nov 2024 21:02:32 GMT  
		Size: 7.0 MB (6995687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:51fd1f113278995eab547ffa296aa33b94b012cad1d6fbc9154fec6668a952bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 KB (289150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c422d4381947665913edbf882ef7500517efeea2baa222e4344580bd1c7ec0e`

```dockerfile
```

-	Layers:
	-	`sha256:c08b5c79d7afd16b8f0533946d3dc8a1ee525f6f53756c09f847b7d7ea86a537`  
		Last Modified: Mon, 11 Nov 2024 21:02:31 GMT  
		Size: 279.5 KB (279517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8297f3bf90c6a93f447ff8a939b3b36c5346cf86a90fe124c519dbce49233986`  
		Last Modified: Mon, 11 Nov 2024 21:02:31 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; 386

```console
$ docker pull elixir@sha256:f007560c8f5b2c44592814067a48623ce50be4ef4323e9d8c786575fa3417057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56663169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694e2963ed9c358bbc60a02b6ce07eaf956e9ffa0bfdf9badddbfbe61e83b59e`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1932aff49ef3199fe608ccac7de1d5a5f566416bb1525c467a1131ee9cce53b1`  
		Last Modified: Mon, 11 Nov 2024 20:05:13 GMT  
		Size: 46.2 MB (46198625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01f3e0beb89440263590f08886eb594b3e07b6dae313a4a88ffb716848fb05`  
		Last Modified: Mon, 11 Nov 2024 20:50:21 GMT  
		Size: 7.0 MB (6995379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:f6717635e097d1302e64ab5f3be721cff254c00f981f6e012a665ec5e8536fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 KB (283514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b3bc0bdd38175c730a5d533f8008522fe86e1a6ccf951e636f2029243e7782`

```dockerfile
```

-	Layers:
	-	`sha256:b5ce411788f4a0f54f6f5021d37ba4e234c41c42fdebd75e4efdd932e64582c0`  
		Last Modified: Mon, 11 Nov 2024 20:50:20 GMT  
		Size: 274.0 KB (274012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe971d2fb933f30149cfdf6ed66a125b4ad0a135088aa355cfaf18265e4d56bc`  
		Last Modified: Mon, 11 Nov 2024 20:50:20 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:d69af84bcb684222eae85ac422aa012e0ec1bb18301037e1a4f5d6dd9edf9571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54090813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5b797b11914c2e31864c547f2cb6276a2e3f051be32b53d7b6f866a72e6c09`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:2b1a723fec64c757d924d7e1e007f92ef7f3d7e7c91198b52ccf7c47d5a4d10a in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:09f69d5d2e4b62e458d29b2e4d2542a265853dd015a23f55217326820e81d7d9`  
		Last Modified: Fri, 06 Sep 2024 22:26:59 GMT  
		Size: 3.4 MB (3358817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf619d1ef8c0c6ffc8e44862331f280a039fee4cd776ea3d6d74d2cd3b958f1`  
		Last Modified: Sat, 07 Sep 2024 06:46:11 GMT  
		Size: 43.7 MB (43736312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f63e9f0ad3f85ebffba1dd0ee7e773f2e1d431132e569031bd0a6defeaaac6`  
		Last Modified: Tue, 01 Oct 2024 20:07:29 GMT  
		Size: 7.0 MB (6995684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:757a9d54a771826a5fedda90a1fe1bbe6443d0089aa65118de9fcf1a4c2ff27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd41a0070cbea7e315b96b908674b6c5f309286d74d4308adf49018ce29958f`

```dockerfile
```

-	Layers:
	-	`sha256:a8580aa3c09790823ee30139c95c605b776bbe776a7f2af092752b423239de2e`  
		Last Modified: Tue, 01 Oct 2024 20:07:29 GMT  
		Size: 272.6 KB (272639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af49c022a8dab64f77cca3beb47843a7c7a16f6e48a3222ec68bc6f76fa34644`  
		Last Modified: Tue, 01 Oct 2024 20:07:28 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:03b81f4b6b4e73d49f6609d52fdc53bc039077bd4b7ab2839645bd3fe629dab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53359244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e390cc009f19ccd3a6760d3f9ba144f908f9f7baa818322e0a0aa50ba78711`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:915212fdde86cc10e2c0038779562c7f4c2d80f238c5807ab3e6bf15c3f207ae in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e1969bec132c5668fa6607cfae829c75ec87bce5e800a6cb6454687412d3c2db`  
		Last Modified: Fri, 06 Sep 2024 22:49:09 GMT  
		Size: 3.2 MB (3230415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7d723af7915223a56d053c90b35cbe3289d0173f329d25b7cc7e8e5630f32`  
		Last Modified: Sat, 07 Sep 2024 02:29:29 GMT  
		Size: 43.1 MB (43133187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75b9407f04de576b2ef7bfe6cfd449f58ac77902930525d4c5614968c6f107`  
		Last Modified: Tue, 01 Oct 2024 20:10:20 GMT  
		Size: 7.0 MB (6995642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:0024e0de76e916fbfb9370c6e6117a1cff07e5dd30fd8cfc9942ce1b6985c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3ed04c4b14a442039944ec45e7917addef55b89bb008739c61d16dee9dc9cb`

```dockerfile
```

-	Layers:
	-	`sha256:efecf8a967d57d8e1413b3feac39d53a0d7d8670c76e850ed9fa0196051ac4da`  
		Last Modified: Tue, 01 Oct 2024 20:10:20 GMT  
		Size: 272.6 KB (272611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e989d527c7dd1120be90427f1e8136b2c82198758bf41a4775b129c62246af`  
		Last Modified: Tue, 01 Oct 2024 20:10:20 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json
