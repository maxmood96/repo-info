## `erlang:25-alpine`

```console
$ docker pull erlang@sha256:dfd5beb2c648b0fd2cf7e759de29a96a01a77ff802febfe608a1213f56c75dba
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

### `erlang:25-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:afed89197799f378abedf34bdd5e4644904ed59003dfd9f7508757818f661ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48258898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814ead232fe6f1ef426dc2245d2eb4a985ec4435358a436c6c8d615f7cbecfdc`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d98d30af08d5f78266d65c681b4a9c5349de4eb0cdcfbbc900567eb85834c`  
		Last Modified: Fri, 06 Sep 2024 23:25:28 GMT  
		Size: 44.8 MB (44842585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1fd4fcec8605b5fd1213f58d20fa9d3664e34d4d290e82e40360cedfc7787d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10ecd55528e4aa79ebc270ecd8af466ba8814de00346ebc4ba1754d0bfc405e`

```dockerfile
```

-	Layers:
	-	`sha256:e909ec42fd01ce0b2e2ecfe5b1fd331dc1f795755524fb51760abcffccb22e50`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 272.3 KB (272295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c097f3e8965d20af7a25653c52c6547a918a325b5eb8e9a4b81b7439c637dce5`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 14.8 KB (14801 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:99b6d93816a3ebc2584fd8e2b97b1cf90a07dee5320feed4736307a63d5976e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45696384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b811ddd9cfc7bd44fde350f5283c6c0d38d9b836bd45cd5ca9b4e3e6f3005dfe`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:57 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Mon, 22 Jul 2024 21:59:57 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fff237ddd898080ffcb8d2b4f9054b343080c7aa870236d000dbdf21889225c`  
		Last Modified: Wed, 14 Aug 2024 01:58:33 GMT  
		Size: 42.8 MB (42785820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:30966cd4ff8ad86781a0ca5c9cba76c66568df43d1dddd4070f2bc5e3f6dfd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 KB (283125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4626c974df1f39764f3a0be3ac0abe53bd995984cf04f8b3a69d40a553dd633`

```dockerfile
```

-	Layers:
	-	`sha256:69614103246ba8651391e5ce39312b6efa438b4f2d68c79ce3876e9b251c6108`  
		Last Modified: Wed, 14 Aug 2024 01:58:32 GMT  
		Size: 268.3 KB (268254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87229217556df28d52ae6d695ec4dc035cb3459e4bc53b9431a80941ed72c9a`  
		Last Modified: Wed, 14 Aug 2024 01:58:32 GMT  
		Size: 14.9 KB (14871 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:01d6eafe522cd810b185e00c4406a8afa1f128d92f6483e958cf97f22e0ec699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47984316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79103c400ad354614a23f1fc4ba7dcf5b52354c894582962edc0dbd50f4e3b60`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:21 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 22 Jul 2024 21:44:22 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d86820fb7aa5b1255e9b61d70fda80ee47ce72369849acc20ceba6e0358fbef`  
		Last Modified: Tue, 13 Aug 2024 21:35:20 GMT  
		Size: 44.6 MB (44644822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ba7684c883de64f2e110fc57714694ea56ebbea71af2e8ed03c83c6e55c7cd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7af83b8a9102997c382b4ab3f35efda9214dd9fa91b8455398f7142999c90b`

```dockerfile
```

-	Layers:
	-	`sha256:3ed2d5d9811f977bb4045651b5b50bf13396919e87d03a6db7140d32289aa432`  
		Last Modified: Tue, 13 Aug 2024 21:35:18 GMT  
		Size: 273.0 KB (272983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d9f7e748733cbd360d4cea2b8863f614fbc794ca75a98884f2231a0897c266`  
		Last Modified: Tue, 13 Aug 2024 21:35:18 GMT  
		Size: 15.1 KB (15101 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; 386

```console
$ docker pull erlang@sha256:96f6a63aebfbc5e19d49e246f2ca926e93b43c5bb86ead8f66003fd55f13aa7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46880860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545f405f9672b53af4d6b6df33164bf34af3e034ef98fecca573a921aa648d0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
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
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2e2ffd89d8060090a0af13f0155658c06db6c47971dda29bad7136b57dd41f`  
		Last Modified: Fri, 06 Sep 2024 23:26:01 GMT  
		Size: 43.6 MB (43630391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:890d426c7ba251fd99a9d149de5456a58ae4b5b1d9dbd2ce364e60cc7d759bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 KB (282333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceccdbe81f49f11258d9a03069cea7806d17c4daee8bc929d2eaeca4dc09e84`

```dockerfile
```

-	Layers:
	-	`sha256:9c98b2d1707db36e48db82cfc0f9937ea28c9925e1fb6ad5df491341ca27e679`  
		Last Modified: Fri, 06 Sep 2024 23:26:00 GMT  
		Size: 267.6 KB (267561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0726045f156dfcec87d0d4bd39d732dd269e58b7e34fec7decb0c135f19a7ba3`  
		Last Modified: Fri, 06 Sep 2024 23:26:00 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:1a860cc578caa68b713ce75a5c9a0896d4211ffeb6dd5475e255d6892114e2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47094681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37803a6fc92b6cdef75e5b3d145f9669ed5679b676fbaafd8b378a6b7f025ee`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:33 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 22 Jul 2024 21:26:34 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43218383f03cebfdf53110d98be412e74e4e77c3d3b74cb0014f67d70abfa3a4`  
		Last Modified: Wed, 14 Aug 2024 00:11:51 GMT  
		Size: 43.7 MB (43736049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:886aed9455614171a87b6815005d9724fea1f6dcb94726b2a3593648dbfbe985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fad6d47ff0a1974b46c8ca220f2a29f7b67ea5a4974b1e65244d0b63f59eb2`

```dockerfile
```

-	Layers:
	-	`sha256:1db5f8796717fd586a17b27fe98aea5547b4e5386f7814b2044ac1d694c33915`  
		Last Modified: Wed, 14 Aug 2024 00:11:49 GMT  
		Size: 266.3 KB (266298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3dd8f799fa48b1f1ece5ab77117e7039092f5c2ad39e9f47b2342195d96d72c`  
		Last Modified: Wed, 14 Aug 2024 00:11:48 GMT  
		Size: 14.8 KB (14839 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:936fc763ea81a2bc01ea393f4977c156eedf449017bc24bb76d6cca0e27027b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46362760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bdf5c2d859113b6c80f10b34b9f7e31c39466ce71e9fa6f6950d8b5b1a88ed`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:29 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
# Mon, 22 Jul 2024 21:50:30 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7891cce8e16730247c0441f9265ee104ff93b119f31de12950db8b6f017a71df`  
		Last Modified: Tue, 13 Aug 2024 23:05:55 GMT  
		Size: 43.1 MB (43132868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d864624b94a629de2feb00923d84d1b5882515d7402e1a3f373915b4656f68b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862381d9ccdb7547f6a606db9e27b21e81fbeae6dfb33ccccae74d80717b1bf`

```dockerfile
```

-	Layers:
	-	`sha256:1405d761b816b04a7379a22df72acc70140ee9bfe1d452e88777f674783f6598`  
		Last Modified: Tue, 13 Aug 2024 23:05:54 GMT  
		Size: 266.3 KB (266264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922d70f89e8476f3e2e049a81dbfc41de3f19631911233f30984926846d66b5e`  
		Last Modified: Tue, 13 Aug 2024 23:05:54 GMT  
		Size: 14.8 KB (14801 bytes)  
		MIME: application/vnd.in-toto+json
