## `elixir:otp-28-alpine`

```console
$ docker pull elixir@sha256:39d02a29b8395e99db30ad596447da0296706dc32853c9b974f1b928145ad901
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
$ docker pull elixir@sha256:df23f8596a0a2a537aed281cff679f9246526aded6493acdfeb0d8de9914c8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63564912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8010cec9e0183a85aa512c8d0166f696048c8fc928c82cbab534ef6a59688a92`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:24:46 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:24:46 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:24:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:24:46 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:36:42 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:36:42 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:36:42 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb3eab1397d0277ee2fb404e2683f070b468c3ec5eae7934ae83b70833d3e4`  
		Last Modified: Thu, 11 Dec 2025 19:25:11 GMT  
		Size: 52.0 MB (51981579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0ba7c5cd6e40e6314bab931c8d55edd001e649e4dc7720c4df8e23cd85371`  
		Last Modified: Thu, 11 Dec 2025 19:36:54 GMT  
		Size: 7.8 MB (7780881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6d226241fd61d1e7c2cc90ed9ac1625dc487dee069b0258f223899e71561dc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d81f5b3de54f2ccbb3527374a8b1863b1a660e08c7b94edeffef179aea1de9`

```dockerfile
```

-	Layers:
	-	`sha256:e33b02b14d3395605e6c13c045d3946349f59a853eee39bda87369e88c0e7098`  
		Last Modified: Thu, 11 Dec 2025 22:46:38 GMT  
		Size: 286.5 KB (286517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9707a4b125702bccac84482cbb42b9dd0148f792fc35fa802dbd26b2dee1de90`  
		Last Modified: Thu, 11 Dec 2025 22:46:39 GMT  
		Size: 10.4 KB (10383 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:aac08abfc6cc03d117b9bd6ada9ce4a7cb18de8cdbbbb0f269006c5c2211be37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b47e602adb7c2653cabbc219b49ec89b6d8860b74b5f3d5d524bb0162c8c5d`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:26:35 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:35 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:26:35 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:32:35 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:32:35 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:32:35 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14717fb57fd4d65552be9928f90056850c33a09c7200a2bf0dabb322ec5fd44d`  
		Last Modified: Thu, 11 Dec 2025 19:26:55 GMT  
		Size: 49.5 MB (49525382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885198f921111713bdf86b14595d52a09ec4992f85e0214147930aa1668dd824`  
		Last Modified: Thu, 11 Dec 2025 19:32:47 GMT  
		Size: 7.8 MB (7780422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:c5155d7503abd08dbbcfb0a6b7a264c707ddf9ecb395c94bf15d91675fe353bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670df769874e65d9e6de7f4398d4bae03ce791ef689e8b52b019a26cb4688abf`

```dockerfile
```

-	Layers:
	-	`sha256:7c447517fe1fb64984c54ce26485cb00bbc2c7228dfb1d7b0ac40e1a8e19cd77`  
		Last Modified: Thu, 11 Dec 2025 22:46:43 GMT  
		Size: 285.3 KB (285311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa462fbb36e7605e9220a8860aea8171d30c322e2d38ee33ebeb667afeb84741`  
		Last Modified: Thu, 11 Dec 2025 22:46:44 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:4021372adc9e11dae315a797999626c2e01518e0e7379bae73bc56af50b41068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63674736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab0419a54ab9e11b482776bfd2ed7dc6a566df114fb833053cacf70573a6f23`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:23:40 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:23:40 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:23:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:23:40 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:37:00 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:37:00 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:37:00 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e844193d843829e3b8c807844d5e834ed1958ccf3cc0df050c38b8462cbdb07`  
		Last Modified: Thu, 11 Dec 2025 19:24:02 GMT  
		Size: 51.8 MB (51755833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c9823d091364636a2b595b58dea24e08ac9e661a1868903dcf743323102cb`  
		Last Modified: Thu, 11 Dec 2025 19:37:14 GMT  
		Size: 7.8 MB (7780834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ad4fc3c8f4c3fad2a3d2fa973c4460b5ebd535aa5c1a07ad5347316570edb477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 KB (297842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeb2d4d2f04238b59546d13e73d7574578aa1ae197c4d5e8351d584f46678cd`

```dockerfile
```

-	Layers:
	-	`sha256:888bfa77ac45082d074cc0925e9551d9e7654fec7f1ecb67e63bf16c695589dd`  
		Last Modified: Thu, 11 Dec 2025 22:46:47 GMT  
		Size: 287.3 KB (287329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ffeee1a62dbaaaf5430e283d9057690ad9c39f7c55bb4755882463a97b0992`  
		Last Modified: Thu, 11 Dec 2025 22:46:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; 386

```console
$ docker pull elixir@sha256:e4b7c80cf19399fd78288429a7a19e9d976de94d9c803ba931e975aeca0e3089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ec2904c5274acb1bd21ada74e26f3992f018013d048885a34b40a812302a2c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:24:44 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:24:44 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:24:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:24:44 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:32:29 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:32:29 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:32:29 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa0c3ca8e6ee1503e0a34083e24b89b2dfe53ad8bb5b5181b20c198ca26ea5c`  
		Last Modified: Thu, 11 Dec 2025 19:25:04 GMT  
		Size: 50.4 MB (50442205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285a260be5e8f28dddf41fe850e659ba330ab5097fe70709e17e3c7c831d386`  
		Last Modified: Thu, 11 Dec 2025 19:32:40 GMT  
		Size: 7.8 MB (7780000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:30d9eecbd5840520b4d3da8d36447181655a80907e9277d340ff1cf461e8cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 KB (291845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fca5a8c4acb840ff1ebdb9e45a8950e3998034b44df621b4cb40975544c17b`

```dockerfile
```

-	Layers:
	-	`sha256:894f3c61312e975771d000c914f0046ecd8f70884c09f7c7520cf46f63903717`  
		Last Modified: Thu, 11 Dec 2025 22:46:52 GMT  
		Size: 281.5 KB (281502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d55a57970edb8bf08498849ac8150bb4384ce695557ccdd29e63372d48d8d2b`  
		Last Modified: Thu, 11 Dec 2025 22:46:53 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:587bc8ca873ae07cf481e92b3269bad86ff80b0125907577235d5413226c6a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62060904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b8fa3db17e31426b17b0a144c5f8f44b1d5936a307a4b8dcf6c6d2c2198964`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:27:14 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:27:14 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:27:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:27:14 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:50:43 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:50:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:50:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790946d8d389721172a60613dd0e60e397f8f54134bc33f0f798e9ba17f91c9`  
		Last Modified: Thu, 11 Dec 2025 19:27:56 GMT  
		Size: 50.5 MB (50548628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5af431e4c9ec44f029d1e7be0f3f351ce82bdbfe4a02c576ab1f094423d279c`  
		Last Modified: Thu, 11 Dec 2025 19:51:01 GMT  
		Size: 7.8 MB (7780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:354147ce5570563d5521c72bb9427d0439a0fad834011fa06425bb49adb39bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 KB (290805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479c627642666adebc51ed004c9071cd911eb68ac7c0dde35efb3d6eb4b5cef`

```dockerfile
```

-	Layers:
	-	`sha256:12c4af617518ca4dcff94307c2e8c80771c4415b829b4b2b409facfeddf28162`  
		Last Modified: Thu, 11 Dec 2025 22:46:57 GMT  
		Size: 280.4 KB (280364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28af3cedcd8777cfa5ff5b8c1b071c44765939bc8bdabc8d9ae7981a613f39a`  
		Last Modified: Thu, 11 Dec 2025 22:46:57 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:77c0f94d3591662df865091a5c47cee03bd695e0ef9bf2c03c82e5d2c6242ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61709389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7e780eb89f1d2c7ee719d782e42a192a140eba772000dd6defea6e3ab63542`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 19:21:53 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:21:53 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:21:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Dec 2025 19:21:53 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:25:40 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:25:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Dec 2025 19:25:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d425e3f34feb2120e82edf5f767b19f213977af53de4363fdf9669c2c3e9a52`  
		Last Modified: Thu, 11 Dec 2025 19:22:48 GMT  
		Size: 50.3 MB (50280122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee3197faededf309e52076cbb94a6db5f04e0dc24da7e6b00cf9f97ea70b4d`  
		Last Modified: Thu, 11 Dec 2025 19:25:54 GMT  
		Size: 7.8 MB (7780023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:12f3f9c855a481b67b5f0564c534becce72589bffde49347a26634ba1cc90bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 KB (290703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afbc443d69c09496ab16b61fe20c0792cf7f36210605259ab5c8a1535cd7130`

```dockerfile
```

-	Layers:
	-	`sha256:32c60e12757de76a241d54c91e9f8db72bc0dc154712f09c66a42fc724b3007e`  
		Last Modified: Thu, 11 Dec 2025 19:45:37 GMT  
		Size: 280.3 KB (280318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ceba5cf5b0ca7cd140058e60ed860fe187b2bc43824fa38289285bf42a65bf`  
		Last Modified: Thu, 11 Dec 2025 19:45:38 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.in-toto+json
