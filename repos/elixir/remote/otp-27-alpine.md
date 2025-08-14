## `elixir:otp-27-alpine`

```console
$ docker pull elixir@sha256:76db0705d8e3e331bd6724cc2a90774bb4170569660fc3a1c196359faca5164d
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

### `elixir:otp-27-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:54d7054f2983c82d474285ac64877f84c1973ffc568659c9d8af2f2484c4ae8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61112087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1b50c6026d449e53f9837097710549b381fc2e68d018938a15ff917dcb43a1`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff37a7e46020860acd1133f865e4e3f42335cb8cd00c33869928ccda98072995`  
		Last Modified: Mon, 21 Jul 2025 16:57:03 GMT  
		Size: 49.8 MB (49831913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d53125ae094841272c6fd103a9ef3dd3069bb41bc4fccd438f5924b17bb31d`  
		Last Modified: Mon, 21 Jul 2025 17:06:37 GMT  
		Size: 7.5 MB (7480485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:c869e50ff359d902bd9b77c4c71030a8c4b4064cd84572d2af3853f87ebbcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 KB (292640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb40c11d13a0a683063d84c4f168821d3f947dcd396fd058d59b79982d7a899`

```dockerfile
```

-	Layers:
	-	`sha256:08934e4d2ff78540b01712fc688f76d2a48e86d238ed432d1816bcd1f01de702`  
		Last Modified: Mon, 21 Jul 2025 18:46:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a85e3478c05513daad28a03fd32f16a20c3b7877545dd067512033fddd4506`  
		Last Modified: Mon, 21 Jul 2025 18:46:47 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:a3fce1b3018fade7170ca7056f0d2ad853a2076b10609a936c3c8495aded2c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (58045386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8914f7f52065c9618d736c9763c11cc66af07723aed71264ad1b5d12f3220b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadef7d87f7567a6a7477d9aeb69206ab3441721ad8d108b450afae10ea288ae`  
		Last Modified: Mon, 21 Jul 2025 17:14:41 GMT  
		Size: 47.3 MB (47346087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95d12066654f6285ab0fe6f9b0aa67e0b44a3e14b8eccc1be50578f68d070b`  
		Last Modified: Mon, 21 Jul 2025 18:32:05 GMT  
		Size: 7.5 MB (7480261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:8a2fcac7c69bf7805ce685a3a220bb4352928e8d04c62a2ca07457961fc6b262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049cd553d7928d2503e6d8d62052da02228faeb85d78b84158b90e04cd81c1c7`

```dockerfile
```

-	Layers:
	-	`sha256:2527f77c085fe852ffd5d06e5a62f0365960360ff1008ad0363aa24678177172`  
		Last Modified: Mon, 21 Jul 2025 21:46:28 GMT  
		Size: 278.9 KB (278896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cce7411a7479b31877353b855a5ad1243ec1b7a3182c36da6abe00d18565912`  
		Last Modified: Mon, 21 Jul 2025 21:46:29 GMT  
		Size: 9.6 KB (9596 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:63c8fd56de9f3c80d63946ade01d861f1a78174dd56e0d7d4591fffb20571761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61223833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84433e3f81b8280df8890c33affec57787218eb427ac5fd28852c29b41305e6e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b607f55c5d3bb75ec4de29891ab695539ef6af0570021dbbfc02d88916dafcb`  
		Last Modified: Mon, 21 Jul 2025 17:11:07 GMT  
		Size: 49.6 MB (49612772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f156b6b08d1770740853bf803435dcd1299772586b0fc898f23205307b5ad4f`  
		Last Modified: Mon, 21 Jul 2025 19:25:50 GMT  
		Size: 7.5 MB (7480311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:5f931874c9ee26340d2c0f39e7f3829ad1d69caba11de3b55e4070b63793a015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50842b8e5c719c0cd1a36a981d89e6eeefe6dddbc33461868826cf120dded285`

```dockerfile
```

-	Layers:
	-	`sha256:b50826dac64e99f94b549a42731c688410200b1b18c7d40c7a810cc2b2dca83b`  
		Last Modified: Mon, 21 Jul 2025 21:46:34 GMT  
		Size: 283.9 KB (283892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aa644e8654687fee4a49d4b1d3f316d85f95f6da7489a6229d61f72c410de9`  
		Last Modified: Mon, 21 Jul 2025 21:46:35 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; 386

```console
$ docker pull elixir@sha256:b4bc6cb1f4afc7742ba652069bd0c752f7da51d3038e21350184c59d5686db5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59361106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede2fa82f496e1b9fb31c0ae97893c13702ef3e49e6fc2fd698e93d75e3596e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfb7f12152bde59dd8bdb40ea933365046a6158ed7c65729d2aa5b5505f0494`  
		Last Modified: Mon, 21 Jul 2025 16:57:08 GMT  
		Size: 48.3 MB (48265806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbc28766df7cf935e247100bf9f79497ff94b972c0daed4a5d377eaf687f1de`  
		Last Modified: Mon, 21 Jul 2025 17:07:29 GMT  
		Size: 7.5 MB (7480294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:72268f318e38101eaaa22356e421244e7f343bb970d7528651e5021cb606bd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 KB (287611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847354627ed4c55ec97f13e9065ff4fa9e7bd228feab1e653498c1728ef9a202`

```dockerfile
```

-	Layers:
	-	`sha256:57f14b85ac704eb3199ae2b01d4c305bbdf32653544147284026fe5c51921c46`  
		Last Modified: Mon, 21 Jul 2025 18:47:01 GMT  
		Size: 278.1 KB (278112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe4c8cfbc463bfd2478af4ecd2fa79b800c664121f564631ef867057c113b95`  
		Last Modified: Mon, 21 Jul 2025 18:47:01 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:fe2edc1eba3c5ab2b53997b62f08b5b786b4fdbb11034c302161917345788d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59566288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3068cfda626544584f68a649ec13a4eb4f14992372e29807b5f4a18dd499f98`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fc229700f92c09495dcdd080fa302d98145d6be2842f2940269c423b04e26`  
		Last Modified: Mon, 21 Jul 2025 17:21:53 GMT  
		Size: 48.4 MB (48358908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f078b56478748cccfff40d24304d1709d01b801c92864971e8059b24e993f`  
		Last Modified: Mon, 21 Jul 2025 17:58:36 GMT  
		Size: 7.5 MB (7480269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:394ebcdddafdfc722ca52a889615cf1c53d36811e215b3f10ddd2b6f6359c6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d108f6ad3a65183c2401aa92d16dfa28d4a549aa818032b7eac7aacce6608d`

```dockerfile
```

-	Layers:
	-	`sha256:cf735a6fa9aa07cef2567bc903069e3dd0d69e0ad6fd746eda8110e5dd9a87b2`  
		Last Modified: Mon, 21 Jul 2025 18:47:05 GMT  
		Size: 276.9 KB (276945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bf561916bbf68664da445027403d376ac9d8136fa5e0e11420db1777d9c0ff`  
		Last Modified: Mon, 21 Jul 2025 18:47:06 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:f317bbfccff88e73253219519b60784c4fb0fcde46c331f1bda8e1cb3554258c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59175142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c58a2966384d25ca48d96da9eafa09e0134c424f209503e17d439941916c16`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58704fe6596f77d1f086dbee501e9951145579b79d0b8d1200094368f55bd32d`  
		Last Modified: Mon, 21 Jul 2025 17:16:24 GMT  
		Size: 48.0 MB (48049882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec1a964fc4f0ba859513df6443e6bfb3c26372bdbd8c7e44e7a085ef155295`  
		Last Modified: Mon, 21 Jul 2025 17:44:48 GMT  
		Size: 7.5 MB (7480289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:90917458912592ff5c0836932122b1085a7be3836c9d3613230cc52168ba2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 KB (286445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a8d774e7018e38d35552e29939887412184dff77d6176435aaa0ef9f659e2f`

```dockerfile
```

-	Layers:
	-	`sha256:1438ae5e1c206d042f41af06e417977fd445f5eb76a4d9257b0403cccaa18a04`  
		Last Modified: Mon, 21 Jul 2025 18:47:10 GMT  
		Size: 276.9 KB (276917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461d235f387078d170616540a624c9ecbec0a34ca2929e5d52b6d28044992445`  
		Last Modified: Mon, 21 Jul 2025 18:47:10 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.in-toto+json
