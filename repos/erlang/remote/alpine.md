## `erlang:alpine`

```console
$ docker pull erlang@sha256:c7e2c739f2ab0bd53d55000a3bc56cbf0358ce6bb48704df7d52211e3081c3a4
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
$ docker pull erlang@sha256:a739c58a1ed8ab8a65d5bb334a0c677ef273f2ddbfe26b9ea9ff7d6dbfa80cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56608459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db394667af267a4873cbbc5a945f068c2e26ac6bab8a4743f1b706c305a295`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:59:55 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Mon, 22 Jun 2026 19:59:55 GMT
LABEL org.opencontainers.image.version=29.0.2
# Mon, 22 Jun 2026 19:59:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 19:59:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789ba3a7340d5d166913d6e044ba2bfe0b0abb115ed8305b6f6b86549a930ac`  
		Last Modified: Mon, 22 Jun 2026 20:00:05 GMT  
		Size: 52.8 MB (52764038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:eb94b3d3131cc89185c126e4bf3738ba8b5063502f0e83d68cfe3d904299bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 KB (265664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361e3aa20e3b1f8ccbba532f19411dad92bfe3b4ed8aed09cdb05e6c580f8d96`

```dockerfile
```

-	Layers:
	-	`sha256:ff7c845836d75cc43d21ce0db5bf4fcd7b65197f0f5c27872694c634bacb6a33`  
		Last Modified: Mon, 22 Jun 2026 20:00:03 GMT  
		Size: 250.3 KB (250295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91eb9c1889560dcaa42bf63ab2a182f9a45873642eb6ab0cc5b2483160112e98`  
		Last Modified: Mon, 22 Jun 2026 20:00:03 GMT  
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
$ docker pull erlang@sha256:38ecbb213ca45561d1d9f6ef65c58a348f28e13f43ee11b43aece8e0d7705b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56735289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd6ce0579a75f6d9ec96c9091a83c8b08f7008a960f3ee256534faeaceb6819`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:00:38 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Mon, 22 Jun 2026 20:00:38 GMT
LABEL org.opencontainers.image.version=29.0.2
# Mon, 22 Jun 2026 20:00:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:00:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7097b7ef987e778a8f8a73ac7d3c3157380bb9fa673b7868ebb582fe8c9b2670`  
		Last Modified: Mon, 22 Jun 2026 20:00:48 GMT  
		Size: 52.6 MB (52553429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3a353635aa025e49280c4ccebcaaf66acb6310889998a80d02d31019bcc43993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 KB (265931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c184ba9ada255aafa5ef4f1da9f1d539c85e208cbd753bdb32114540ec97702`

```dockerfile
```

-	Layers:
	-	`sha256:fa582166f5eb217e51b8b8e8fe04cfa170b04bce531b69fc02261270b4c5be1d`  
		Last Modified: Mon, 22 Jun 2026 20:00:47 GMT  
		Size: 250.4 KB (250447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:516c6e4c5a49aa7320f9619e2fe0330b7d2645729930d0c9d69a7c55a077fad8`  
		Last Modified: Mon, 22 Jun 2026 20:00:47 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:72bfb7ffdbc00f958645205b25ad0a3322e946428b34dd8e6391a4b0f5869e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54816141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba49799caa7f4341eadeb04b24f1e9046e53245890c4cc997e3f9c9ec10e634`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:00 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Mon, 22 Jun 2026 19:55:00 GMT
LABEL org.opencontainers.image.version=29.0.2
# Mon, 22 Jun 2026 19:55:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 19:55:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7116cc9cc80632505d929a52e1a7c8ec3ea64ee5d9d4d6509eda4efa33bf3cf0`  
		Last Modified: Mon, 22 Jun 2026 19:55:09 GMT  
		Size: 51.1 MB (51148151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7fbb28a26db1b7cfe1d08a2ff55db39317d8a3bf42f32656b22b50cecbf20b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 KB (260617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132ba1f648fa5c1e76ef0175b60d179a0e88f54e5cfba22392230631008f99d5`

```dockerfile
```

-	Layers:
	-	`sha256:8a6741ecb11f55f49f530cf0bb60f957da82acb5c846cf74dfd6055e7e8bf324`  
		Last Modified: Mon, 22 Jun 2026 19:55:07 GMT  
		Size: 245.3 KB (245285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583c4708340e9973029d85ecf5d9f97474d16707fcf449e726ea3aebb17ca6f2`  
		Last Modified: Mon, 22 Jun 2026 19:55:07 GMT  
		Size: 15.3 KB (15332 bytes)  
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
