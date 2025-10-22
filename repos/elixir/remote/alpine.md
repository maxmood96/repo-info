## `elixir:alpine`

```console
$ docker pull elixir@sha256:cce05c075c6dd2d12237ef4a4b317c9bbba92279b8b9830d026d37e6174330c6
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

### `elixir:alpine` - linux; amd64

```console
$ docker pull elixir@sha256:892f0e183b560960c4e95a2cbf4fb9866831f7f353b27e101cecb17b6b0dd6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63401762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783f9075dce0f3e061f6e582358d5c2b04a4959e7c65a419cc8d3c7c139e6fed`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:f90a0293187fd13b2a8b928f04a245dfef42e9f7147604872ea7758f36e8b1e6`  
		Last Modified: Wed, 22 Oct 2025 17:48:29 GMT  
		Size: 7.9 MB (7858536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:a379d4876500dea16fffa0e20b7b74a1d420ebbd7b7400865186916d00acfc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 KB (296957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743d6140bb30a775825698ef58e38ec1067f2d9f5af07e6f2362def60977941`

```dockerfile
```

-	Layers:
	-	`sha256:c4487e4cd548b6b5ed253b290750eedd5a24787e71d5c5ac73697bd0f8238f2c`  
		Last Modified: Wed, 22 Oct 2025 18:45:09 GMT  
		Size: 286.5 KB (286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01e7ac0c95e10ff31bb4f73a111f1161ec64a815cb3b3b22643aa57741c7b1c`  
		Last Modified: Wed, 22 Oct 2025 18:45:10 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:855e001088d959d2076147fa317ef9a853178bbf8fbfcac4772fad7c0bfe8d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60360714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24ff400e8b6cfdb6a6a47df0c8dd3999c4ad13c21276a45f4b7fc4de57b055`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:efaed3dcb69d677ba7d4ba75b9474492e0c393d408b056f388bf9b74ad0dc0a2`  
		Last Modified: Wed, 22 Oct 2025 18:30:33 GMT  
		Size: 7.9 MB (7858291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:457c9991132a42cfa9ddf4d232dfabcf54b4df69420b1c56d8eb97da13a7c055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617d1097df2429d95fccc68ab3a09dd2a15adc6c1fb55af24542bfabab366ec`

```dockerfile
```

-	Layers:
	-	`sha256:fd568e0ef399d25c33a701612e41174f1fdb142eaf8d4c40431cd5e38b20f605`  
		Last Modified: Wed, 22 Oct 2025 21:44:56 GMT  
		Size: 285.3 KB (285323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f72b375f714adbe3f380739517f35c820f56afbb64f37bdd52a59babf92177`  
		Last Modified: Wed, 22 Oct 2025 21:44:57 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:c31280f6fd53982a02dea3b57948321384a51a0f182617a84d63a2f8342ebb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63496340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fe154e0ba5f237cd092f86d9d76518e07d914284276212f6a1870f400f62f9`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:33618cf7b69a70e0bbb8b17411234e219c90f0d68e753069dcd74dce4bb7dd97`  
		Last Modified: Wed, 22 Oct 2025 17:47:50 GMT  
		Size: 7.9 MB (7858392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b26a8c2e942180b738a07f4cf3a90a3c089db629954114e338791b0e4fe2763c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 KB (297897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968a263750fbe6cbb3fa8a078454b22cea98ee4367459e6e7f24d84d6133905b`

```dockerfile
```

-	Layers:
	-	`sha256:89c0b4b2455fe1cbd46dab022597072d044e93eb6b005766a3038f85cbc3b4b2`  
		Last Modified: Wed, 22 Oct 2025 18:45:15 GMT  
		Size: 287.3 KB (287341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329193d51cb6f33d2fc73f8cad99c414eb2542bf03a4ef565a0c90d5a99edaf7`  
		Last Modified: Wed, 22 Oct 2025 18:45:16 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; 386

```console
$ docker pull elixir@sha256:686e54708c3ca07c1db26a3da007221f01545438985da5578009817e0853a0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61678582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7afa1de30fb89ff5e449b1e2e10ca0203e5e88d3f616e6d7be657a8748d2621`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:af089bd85c58fcf58c70815677741f7c3b676a5f961061362a2813baa986b152`  
		Last Modified: Wed, 22 Oct 2025 18:01:43 GMT  
		Size: 7.9 MB (7857870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d7b38a6b7a7867b2c44dd23d5ac6fb76d7ec080d252c93d3349bfc3b24887be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 KB (291900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8b348aba9426fcd9c33e41d37ccf91789d7aabdbf600b3875f5508ae6d22a4`

```dockerfile
```

-	Layers:
	-	`sha256:3cb5f87d14390a40769febd3ab35df76a5bd3d57fc5c9307316139465eb03c70`  
		Last Modified: Wed, 22 Oct 2025 18:45:19 GMT  
		Size: 281.5 KB (281514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8220b03f7f7e6f050209cbe8733d0216927b77d7caa26d13bc9b76cacb797a68`  
		Last Modified: Wed, 22 Oct 2025 18:45:20 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; ppc64le

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

### `elixir:alpine` - unknown; unknown

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

### `elixir:alpine` - linux; s390x

```console
$ docker pull elixir@sha256:4935f57eb5b0795e1df7c7590edb34c21b12aefd12a80d59716487584b7212f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61529663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6401c2599817f9e716b37eafab64b8d5583ab4278342caf346a7cdfc3cf861d`
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
# Sat, 18 Oct 2025 16:12:49 GMT
ENV ELIXIR_VERSION=v1.19.0 LANG=C.UTF-8
# Sat, 18 Oct 2025 16:12:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="99a684045b49f9c5005a1aa8278e1bac8c3769e0a5a13c05ef80b69113029234" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 18 Oct 2025 16:12:49 GMT
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
	-	`sha256:45f2f43b33b70f5ca804080f19e697bf7d4f33186c746e2efc34b7dd7ba32364`  
		Last Modified: Wed, 22 Oct 2025 04:06:50 GMT  
		Size: 7.9 MB (7856369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:cda21f87ef91de42dff7d58a062a62cb74009fead3cd684d39e7cdc5e5673d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 KB (290758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa86e87d0ec61ee98d7ed365ad34f643079786f374917504132236544bf2cada`

```dockerfile
```

-	Layers:
	-	`sha256:5ccb911234bc518f0c38a1f8b0ee97bacd36ffbdfad12dac04c90bfd81543df7`  
		Last Modified: Wed, 22 Oct 2025 06:46:03 GMT  
		Size: 280.3 KB (280330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330103b944a05534aead72a9198c7f8e3f812c009d438565aa22762d8e8c7509`  
		Last Modified: Wed, 22 Oct 2025 06:46:04 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json
