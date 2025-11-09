## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:65c868055d38c312672c4bcea8371e54943436b56383d56b097968829b1e5193
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
$ docker pull elixir@sha256:ee07761a7c244cb1b27b54d9dbd7a6354a50ccb498928abee7f24060b47db1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57491715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b2aff16bf95b37a0c047df20a5dea7476c583244492d207923a6fed7b3d16`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:05:35 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:05:35 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:05:35 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61376e7a1277e186ac82f4aaaffba72d7584b6f0f0e2fc79dbae95ab374a963e`  
		Last Modified: Wed, 08 Oct 2025 23:07:11 GMT  
		Size: 46.1 MB (46084817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f02e01afc5f2cb292511a5937202e2831d565b4fb23417ab330c9e2cf4a749`  
		Last Modified: Sat, 08 Nov 2025 18:05:49 GMT  
		Size: 7.8 MB (7779842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:2c0c976410d1b2f05f993db43a2ade2a8c609fe9e8d3866f046a465d2df06505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 KB (289870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb69c3ea41bbbdee843441af5b7e5b2450e35f4f398eb5578c4ecac08686e0b`

```dockerfile
```

-	Layers:
	-	`sha256:402a8bdc63e91842c52ffab430489cf09d1e66053bb93a70c0a9367acb2f5758`  
		Last Modified: Sat, 08 Nov 2025 19:45:36 GMT  
		Size: 280.4 KB (280384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1353f8064022f873175b93a98927f45ff51f37385ef7988afdc6c99130cee9eb`  
		Last Modified: Sat, 08 Nov 2025 19:45:36 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:40e122638ae9ecc906e9e12ec7d285c9aa3c4452b4861638ec6b14b83f0ccd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54622609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab82d2720174896200f23e9b99e322000aac31c09133ab956645ca3369f89448`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-armv7.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:04:52 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:04:52 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:04:52 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d9d7b8e1c6b20394731c1f62afa10545ea3d2388aca5051c7bae7732dbced5c9`  
		Last Modified: Wed, 08 Oct 2025 12:03:11 GMT  
		Size: 3.1 MB (3095971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5a44104cf4bf360a898a9ca0fa265151465e642e5e4c48b63fc922982f935`  
		Last Modified: Wed, 08 Oct 2025 22:15:14 GMT  
		Size: 43.7 MB (43747136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5d4ed4affe7d7f9566caaabe76fcc41567015cbd9db01fe841ec85fded7b6`  
		Last Modified: Sat, 08 Nov 2025 18:05:03 GMT  
		Size: 7.8 MB (7779502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:1266473e0a602d6c4d27cb0ed0827eee4af8f26862ab499b71d14c421bb92925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 KB (285654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fe898b088930af945a6a58dd9d934ea755180bef0906fcd800300bff0d2ce7`

```dockerfile
```

-	Layers:
	-	`sha256:970d914ea5ce8e70ac8d5cf0e15df3f18115d364f5e8d2b1d942efca08ecc18d`  
		Last Modified: Sat, 08 Nov 2025 19:45:39 GMT  
		Size: 276.1 KB (276097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da8b350c20a4ee5022ab22c436fb4f11377617e099b210a065b745fde957585`  
		Last Modified: Sat, 08 Nov 2025 19:45:40 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:f656b28d846ab5d3dfeeec1713a5302c8979678179edf922922d510a9b1be518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57743358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f394950672c04827a90d7741cd5a58f1cd29ae6d2f41e04f00c7b09ff69e5`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:04:50 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:04:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:04:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b0b6a506d1c642e03e090637397493acf73f07ef024550834ee143d26d22bc`  
		Last Modified: Wed, 08 Oct 2025 21:52:33 GMT  
		Size: 45.9 MB (45874143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566ac0c7e73ab328ccc5a560f2d4ad3ca354dabb7e1a92ad100801f27d2bfca`  
		Last Modified: Sat, 08 Nov 2025 18:05:08 GMT  
		Size: 7.8 MB (7779838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:81af9ad4364d4193973cfb75aa438657add29f1df45a341fac76416ea1bdacda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 KB (290743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427fffa433678f872368679ec3c136263db2c5aa9735a8037d343c92194402d6`

```dockerfile
```

-	Layers:
	-	`sha256:a09cfe932bda4212612472f444e7f505a6649eda94c96253980a1a788c5e78fd`  
		Last Modified: Sat, 08 Nov 2025 19:45:43 GMT  
		Size: 281.2 KB (281165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4a5a2d605bb8ce3c60e336d7cff543ae09cccf1c29d50dbcd21bba06aa8458`  
		Last Modified: Sat, 08 Nov 2025 19:45:44 GMT  
		Size: 9.6 KB (9578 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:b62406dff8b464db038bc233ebf0e6633bc2c11a11dec779b7925e69b47f2d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55931086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e4983ed5e2e63a42cf20b466a4263b9fb7e265dbe1f30d55acbbc3e993e3dc`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-x86.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:00:53 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:00:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 18:00:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e856d2de40a4729121561fa833570a5178c9f2def6f5ec8c0ef1681f84149f96`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.5 MB (3471033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec55c6f27b35ad9db0d56ebffe4850a73632cab80d2bb40ca4773161aabd144`  
		Last Modified: Wed, 08 Oct 2025 21:45:16 GMT  
		Size: 44.7 MB (44680497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1a35255ff4c9e4dc8b457b9e7e9cb61b0f7dd955be2f83368ae637aea1015`  
		Last Modified: Sat, 08 Nov 2025 18:01:07 GMT  
		Size: 7.8 MB (7779556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:2263ffa952f3f1da29c25aa30aeb7787e656accd04ac31929ab6de55782ce823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 KB (284771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e089662e3a496f29613f34efce66c4f827cedb22542d55e6f3267bafc56ef6`

```dockerfile
```

-	Layers:
	-	`sha256:8f10505aae3c7f4a713403a498d8a76e115cb9dc7dba357957e417774fa891f4`  
		Last Modified: Sat, 08 Nov 2025 19:45:47 GMT  
		Size: 275.3 KB (275312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bfafe648a91e41bf850547deacd1750c962cce70d7b6c6209176f3735becee`  
		Last Modified: Sat, 08 Nov 2025 19:45:47 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:c27dc56ee8033b11e6290c3f48f752c7141c5533cf37fed5ec092bfaeb5e0499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56087283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11864f7f7611e3e47d5eb0aceb6fa484b0a13814b8d072cc78099a9b75a7af39`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 19:54:02 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 19:54:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 19:54:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eec4056a60573777b74e7d5ff662a6aa1f8091cf9c8aea3c924a32a0eca88a`  
		Last Modified: Thu, 09 Oct 2025 03:52:07 GMT  
		Size: 44.7 MB (44732146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caafaeec7f4ff8b4edf624169d7d50f8383e52f1de9636b8ac24ebc6b97acfb`  
		Last Modified: Sat, 08 Nov 2025 19:54:22 GMT  
		Size: 7.8 MB (7779574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:de49e0047f9a08adda3b8b6e6b85865432fdaaee5508c92a54ccb84010af6601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 KB (283670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b209d993467d165a752f2504ab0119e4dd4974458bc7675ee9ee8dc8416930`

```dockerfile
```

-	Layers:
	-	`sha256:3a79e221a276917fead6c43619ccf42d67068db124db705a55d0ef5cb0784ec3`  
		Last Modified: Sat, 08 Nov 2025 22:45:24 GMT  
		Size: 274.1 KB (274146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52760b656bef8dd8a7888b36178505bf9461daa94712f717ace4ad10324a6f7b`  
		Last Modified: Sat, 08 Nov 2025 22:45:25 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:1796f6a02092ea50e945383d0eb1869aba2f78b4fcaaa4a115b7a455f42daee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55631539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4933e271e3a879560bd33c1360016e6b56b727b4d6034daee67e774a8c6520`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.20.8-s390x.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 19:57:58 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 19:57:58 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sat, 08 Nov 2025 19:57:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f904de3749cc276a12799ef0473a83bc2c72312c8555897e435b03275a44b66a`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.5 MB (3462801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076016bb9f1c2a0ce4e7669307253f9eeff99566dd997f565e303eebb9af5cb9`  
		Last Modified: Thu, 09 Oct 2025 09:19:42 GMT  
		Size: 44.4 MB (44389335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72425066480e588c7bd3278984aea2250e096b73745b20963fc9ef29ed9a1d5d`  
		Last Modified: Sat, 08 Nov 2025 19:58:11 GMT  
		Size: 7.8 MB (7779403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b96210db1ae2d0eb5cd7b38f15c63449203dc997a3e93a56134dd1903b52ef8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 KB (283603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afd154f72a218deba83aa19cf2f542536153347fa9fe52c9686fedd8f9f96c`

```dockerfile
```

-	Layers:
	-	`sha256:9b767cd9264384c0c761659cf868f9002a9ffb15e565150bd315c696becedb40`  
		Last Modified: Sat, 08 Nov 2025 22:45:28 GMT  
		Size: 274.1 KB (274118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b505d2108a821cdc23a5cd873b0b32c18d8f4ef0934dce53602bb6faecc8c6`  
		Last Modified: Sat, 08 Nov 2025 22:45:29 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json
