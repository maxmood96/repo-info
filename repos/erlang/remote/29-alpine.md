## `erlang:29-alpine`

```console
$ docker pull erlang@sha256:a3cb80cfffb64de708e4fe952d05d760afc83a7bba4fc5eeb6201349eaa5fd9b
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

### `erlang:29-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:3d56d22180e72ad4df68b7efe7438b3e0f39169b2f27477ead94174e837e16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56955786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63199499c2c4ecd4f5f67e655e151635e42652c362e40de9c590ded9b194ec`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:36:58 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:36:58 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 20:36:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:36:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3403e1db2c5d44e696870b7b0601de8420083d8c87ce357e0a6faebd016d8758`  
		Last Modified: Wed, 15 Apr 2026 20:37:07 GMT  
		Size: 53.1 MB (53091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:59732f532f9bccfac64ab4976ae67fee504a5e64b1a473c602abf0004d1da5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 KB (292125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f549b68f38a5f5725c336512bf4c938d801b26f78b7ad79872958e7cfbfe8b7`

```dockerfile
```

-	Layers:
	-	`sha256:3af6699f6f0ce97ccc7b0d2d5d0904afec15067e40eef0d4be76193f30fdc47d`  
		Last Modified: Wed, 15 Apr 2026 20:37:05 GMT  
		Size: 276.5 KB (276495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88df7f4c040e5dc18016e5b1a875d4c6c304598a5e0f50c9e25fab77756ca78`  
		Last Modified: Wed, 15 Apr 2026 20:37:05 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d4045a1a24d2844f71276609d5f1ca3113a4e5d115d57a77672492b4c81ecd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53893146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c962071813e4e0cc376137fd65af01d8eb7b7bc103806a39099a932b0676fd2e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:37:32 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:37:32 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 20:37:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:37:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d287e5d798164aa849f0634d1665ef39ce216c48a6259e66bf4d919961bee5c`  
		Last Modified: Wed, 15 Apr 2026 20:37:40 GMT  
		Size: 50.6 MB (50610023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:45892ca56f32be598e3aca5d6c53104e35dd6896fcf1a44d37a1d860251b30da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 KB (290333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f51218978d8c3b0028c5d0328226ed7c0e4f204c1f90519d390074c0baf55`

```dockerfile
```

-	Layers:
	-	`sha256:57a15382a20c437b5d8c70a3497e3cb6c96308236dcc1d83a330ff8c99ab0878`  
		Last Modified: Wed, 15 Apr 2026 20:37:39 GMT  
		Size: 274.6 KB (274623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0e013c70298dc129730f044bc9150dbb4f1af38ae66b850f4424529cc9d9d5`  
		Last Modified: Wed, 15 Apr 2026 20:37:39 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:19186d6d642f0282616bacc7934639426513a76bc08aca799f5b05250eb1a51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57101475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d3134d18086799e79484c08aeaf3972bc68fd79c366b45d6169f64f9e3263`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:37:20 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:37:20 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 20:37:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:37:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd851c955404e9ff4e6d05eff041b4078b388661429091e65387ef2778b8eed`  
		Last Modified: Wed, 15 Apr 2026 20:37:34 GMT  
		Size: 52.9 MB (52901605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:da56d265eb9f99dee0de70f8b68b8e8d28d6abe1622d2c27e1c1c759f2a1323e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 KB (292367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf01d46a1e1a43e14cfefe6f5acd6d72e2129ca05d87aa275b3cffa8d4fcd0a0`

```dockerfile
```

-	Layers:
	-	`sha256:49ad12a6727cbe5b6cd0e200f9e04a55fe3194c393dd2220b5fba65f74f980da`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 276.6 KB (276633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f914a39aa409c03453232786c9c1b66350d3a33a0d7785f353e9b2fed836f9c`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; 386

```console
$ docker pull erlang@sha256:acc5dd933d1da69f3ae4a867c9aa29a21bc9d53975ebdb349e2623a4162dcb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55171627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafbc5d9e89dbbee051b229ed22663f136d071e397054b1679170a3544a368b7`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:42 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 22:27:42 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 22:27:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 22:27:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb86a5f1f0e03d61c2c41df4a0b844b6f30cc3efbfefec184b497951c6a7c0`  
		Last Modified: Wed, 15 Apr 2026 22:27:51 GMT  
		Size: 51.5 MB (51481181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7de301415caefede6a9bd8f6f269d31a01d7215a1670ce1f54c90e7c55138a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb1f7f0db388f54c4373b1037e70819b63427e07d023ed1b0200c0f9cdbbfd7`

```dockerfile
```

-	Layers:
	-	`sha256:7ce2980cea68075f1515bafb258420f2df556b30a5f30d2b8dbc2b4a44f2f1dc`  
		Last Modified: Wed, 15 Apr 2026 22:27:50 GMT  
		Size: 271.5 KB (271490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e39a4d10233da2b2c4811f99ccdfb363f37bc467cad5bbd4174442ca22d173`  
		Last Modified: Wed, 15 Apr 2026 22:27:50 GMT  
		Size: 15.6 KB (15598 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:20e68a649637cdbb837aede31c9f93f65915f3ee31760cf50a127f8d9f280fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55602406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc39641c41c6a48d2bd55bf3fa7050a6a6ce8c5e6fc9d30d6dd88e0651165de`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:34:09 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 21:34:09 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 21:34:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 21:34:09 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b32b8d44090d317c4ba2dbf758c16241944468471b3112ccf35f408f85a32b`  
		Last Modified: Wed, 15 Apr 2026 21:34:29 GMT  
		Size: 51.8 MB (51771477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b5aa9cba5213dae48dcd3411154cae2b08cac346deda076e7ad37ea62cde950b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 KB (287304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c62f464439be680d403128f09d938225708b25c36a6c7d9cb2d2c401421e2e`

```dockerfile
```

-	Layers:
	-	`sha256:e9062f4e617a2c3f860051302b1c0af60c7c7e8a04df6636b16a2916e1258c40`  
		Last Modified: Wed, 15 Apr 2026 21:34:27 GMT  
		Size: 271.6 KB (271630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c219bcaffe31fcb5bdea09a071c88904c38982d9956a8a39d3118f08952d51`  
		Last Modified: Wed, 15 Apr 2026 21:34:27 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:9bb162345c71d3e14acf08bc953cca72d975111ad2df5f9d2f6376b062c6572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55125328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ce90fe7f98066161c9f0ea47bb08c4cf4dcd0eeaebb7798bd1dcc89502da2d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:51:16 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:51:16 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Wed, 15 Apr 2026 20:51:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:51:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ca67adabdc47bd4afa21043c62ffdc8155403039e56d3f937bc0cd852ca87c`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 51.4 MB (51398796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:12dd00f4354837b60695d6cb0512d2fc71755b137f1619d91487f8bcb6e165c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 KB (287226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7eb472339edd7780527eda7c0b52e267a9525bd344b50a534ad0b48a27a24fb`

```dockerfile
```

-	Layers:
	-	`sha256:ef00e6f4c263da7eada14e5304c30684673170eb46810abdee261f6aeaf5829d`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 271.6 KB (271596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edd465825bbc32fdb66dcbd1db40c6ae9677ac53d388a9c488ef08b2bb4fac7`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json
