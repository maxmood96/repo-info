## `erlang:alpine`

```console
$ docker pull erlang@sha256:5b532ba56229790c8e65be88e53becadfeb19f4ce1db4de6c44097e1843926f5
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

### `erlang:alpine` - linux; amd64

```console
$ docker pull erlang@sha256:0b1534bf63d0883b2c3782ff2a5fbaf96c04bbb6ca032f76a3de36a094dd21e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59151885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314f4a7567b453d76fd28bc51b2a29b6a7c7e1d76f8590a0720ef5ab36e0857`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:17 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:17 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c74954b1e285a5290314cf726a95084c5ff6b44dab26690faf576c8927041`  
		Last Modified: Thu, 11 Jun 2026 19:11:26 GMT  
		Size: 55.3 MB (55287696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0797e365b0f4b66a3aa9172f16a2b46ab453a75ece3a49ce83165c1bcc75e5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 KB (282556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fcf01e67df6e05276758259939e87e32dfeb5ce856cbe5a71c9a5b57f16246`

```dockerfile
```

-	Layers:
	-	`sha256:a040ae5211097fda6c6a86a9158bef6abadbedddc173859aba0c20f6a104221b`  
		Last Modified: Thu, 11 Jun 2026 19:11:25 GMT  
		Size: 267.2 KB (267187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edcdcad993d4c4e47ca71faabec8c925241a85c9098c37418e90b9a4c181441`  
		Last Modified: Thu, 11 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15369 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:9d7f0963f1ef54de980503b25a450ff678f1317ed2c2e33d9e057efa24418f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55600730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fda503c0dfe27e67a1f106d8df5a975e64f35d53150f355263b85d4bc0abfe`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:31 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:31 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2314bd76c1f0050fe25c20bcc515b0956701e80145c2fba1cc17a228fa3ab15f`  
		Last Modified: Thu, 11 Jun 2026 19:11:41 GMT  
		Size: 52.3 MB (52317607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0cdc0b4b3517441e9f0897775b527035ae793ed6eb3a336238adfe0a6f59ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aed59c67afd788fd761481d9dbb92b9dbe9a8b5937a33f6990304569e82c4b`

```dockerfile
```

-	Layers:
	-	`sha256:69f0b810a55088730bb4e7c045a77cf4aa527d9e956fc5261ae3c5d85c4f4f3c`  
		Last Modified: Thu, 11 Jun 2026 19:11:39 GMT  
		Size: 265.3 KB (265325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb7031a51b076e52f123c4807d0c5331521f3fdc22259f0ab5e78ea11f15c56`  
		Last Modified: Thu, 11 Jun 2026 19:11:39 GMT  
		Size: 15.5 KB (15456 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f41d7b8fdc86603470fdbb003bf47513eb401da06bbd23138c42562014038a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59560829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddf06f70e45405415cb434b7d74f7ae514c5d5ad0bdb4703574b0661927da0f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:14 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:14 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d4ab113babe191ec758e19658e48c52dbb1b4010076bf4fe4a55d1f8eae98b`  
		Last Modified: Thu, 11 Jun 2026 19:11:24 GMT  
		Size: 55.4 MB (55360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:bdd4eb91805c39259fc345e91cb2ace5a21b44e07daf6850835b17c2a3f9fc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 KB (282823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f427bc1e967e0cec4ac6608e34d0884daf8fba923be268c15fbfcfe80391fc`

```dockerfile
```

-	Layers:
	-	`sha256:d3503053ef7e014eca7543c0d5d7a52d29ad09386e22778c9c6a6bae9ed7e5a7`  
		Last Modified: Thu, 11 Jun 2026 19:11:22 GMT  
		Size: 267.3 KB (267339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c2f62ab908c8c26bcb2b0f231ba389eed201dbca976beef99cbc993ff6890c`  
		Last Modified: Thu, 11 Jun 2026 19:11:22 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:9b0b64557bdc99765d983886153cc33d4691de468a1c2d21eaaeb9aeec7ace2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57175287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94814c8071b46287c10c72c352d2b3888badd98a5ae8468c1526348f031aaba`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:27 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:27 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3148dfd4688690a6069d215809581a9da9887579b5512fa2958324b4d14215`  
		Last Modified: Thu, 11 Jun 2026 19:11:35 GMT  
		Size: 53.5 MB (53484841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:232a0b4d294170f341c9fc2e55664e1ccdbc1319292966d7c5bf51285a7beffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 KB (277508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27ca8af19edf9154caad2c80720dc6098b2e81edce1b37114fe3359701b4b0b`

```dockerfile
```

-	Layers:
	-	`sha256:a56fd55c67c2e436c38bb007f87c70dcaf3c8df7674cf30fa254dd7fc13762d0`  
		Last Modified: Thu, 11 Jun 2026 19:11:34 GMT  
		Size: 262.2 KB (262177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824533bd4c75d0f8125fd4530a92023e681ddbb366213f6b88b91d61942135da`  
		Last Modified: Thu, 11 Jun 2026 19:11:34 GMT  
		Size: 15.3 KB (15331 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:51ce9753a69b6079191fdfb73b37555f159203e92d68bc3dce6f85832d1232f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57642145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d12240088cce7754fdf435809f8e7439575256917400aeeb9e8feece478023`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 21:02:29 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 21:02:29 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 21:02:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 21:02:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ddfeaf1205d30c9c02cc2422a27ef104981693464a59b76851df278b1695ce`  
		Last Modified: Thu, 11 Jun 2026 21:02:44 GMT  
		Size: 53.8 MB (53811216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3e87dc1d2eab9739cfa4796cdc81b2481ad8798608d831023cab8dab3bed4ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 KB (277749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd47c4bdd74592a9eb6887d204c92978a3e2c2d3f9907328c12e3c33c2b70b2c`

```dockerfile
```

-	Layers:
	-	`sha256:2d939aae33a0eead1d7f35acee2cb2701d5ebcf1595e075c92e00dc0b9627b07`  
		Last Modified: Thu, 11 Jun 2026 21:02:43 GMT  
		Size: 262.3 KB (262330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b8451bb13143cac85240632852f8b435d97a8b17c5131eff7361804ec078c8`  
		Last Modified: Thu, 11 Jun 2026 21:02:43 GMT  
		Size: 15.4 KB (15419 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; s390x

```console
$ docker pull erlang@sha256:bee7b5bd4370d42d02b09f34a7c63842e93b5eac35e7dc289d011e2d3325e647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57067537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d673fbb36b918fb8f8695e71765507395815b68b5a544c7db3f439e606d5c0d6`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:12:37 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:12:37 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:12:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:12:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44807fb13ed4723b55ff85a9d0903719fb63ab261b24cbc0b92405927465597`  
		Last Modified: Thu, 11 Jun 2026 19:12:52 GMT  
		Size: 53.3 MB (53341005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:f553587f7c1f0f5ea342f8beab6b753a8f25aac54f17554f0b88becf66d08cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 KB (277657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6564d452aff788337812715c72f4ca2e9e79e3368e794d6a2e4e7e478a11291a`

```dockerfile
```

-	Layers:
	-	`sha256:04e5c57e534d01b903b4f72e01fef5ccd281b3dac5fc6932db91b1a4035a6216`  
		Last Modified: Thu, 11 Jun 2026 19:12:51 GMT  
		Size: 262.3 KB (262290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89888b9606292df4fb87e6339d0b8e64cff6f39f6ff549e4fa6529cb37103bc`  
		Last Modified: Thu, 11 Jun 2026 19:12:51 GMT  
		Size: 15.4 KB (15367 bytes)  
		MIME: application/vnd.in-toto+json
