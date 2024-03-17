## `elixir:otp-24-alpine`

```console
$ docker pull elixir@sha256:84010f66b77a4ad40072f0de4860d0200672def4b3765ae16985762d83703163
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

### `elixir:otp-24-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:ee4c42cd50ea7dc71f19d00bc89e1137217650cafad63ee2f372aba66c213fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55839972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36002725a342a42b0e2cc28785ee1add811da69e24e6c13be6e340c75082a092`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861c13792f86bf8d1d6e372bfccf94e712aa0f45d2f7372b37c9879c2f5fedc1`  
		Last Modified: Sat, 16 Mar 2024 08:39:43 GMT  
		Size: 45.6 MB (45644055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404a8282e7ea892c4d96a69e33d2e80930297b88ed86fd328a008fbc13d691d`  
		Last Modified: Sat, 16 Mar 2024 09:52:58 GMT  
		Size: 6.8 MB (6816513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ba8ba298f3ac14d5d4ddb8f5de1da511d0be747040d192bf3ef9c81b9a606623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 KB (274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188c42760f918b6744e3d4f4e83c0f5d715371b2e55467e5f6646b228dabb17e`

```dockerfile
```

-	Layers:
	-	`sha256:860fc676808c64a38247ee9deea6cb44a852fd7a121e8289a8bd0a5f81505081`  
		Last Modified: Sat, 16 Mar 2024 09:52:58 GMT  
		Size: 264.9 KB (264905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc8ac76e33cf3cf0c392f492227496d10f6d4d9103e3df3eda0b1653bea27a6`  
		Last Modified: Sat, 16 Mar 2024 09:52:58 GMT  
		Size: 9.6 KB (9589 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6d5064b416bca871cf3178d837c1148cbe53c0c0bd74dd4b8b8830caa304b74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b759fb9432a4a0a3d55c87cf93e273655ac9a955f54c0d8ceab3c055bc3fe6`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:07 GMT
ADD file:248255ed09e14a0af5432820adc48fdeff8b679f7965161e9fe1c7102a55a874 in / 
# Sat, 27 Jan 2024 00:15:07 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a35f077ad6eed63841c524f727e359345dc0ddf23f8d8d826405b587110cf4b8`  
		Last Modified: Sat, 27 Jan 2024 00:15:47 GMT  
		Size: 2.9 MB (2869839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb1721b8a2b4e2c598bc6378f65ae5166bee5b9ebb1811905e11eea7292de89`  
		Last Modified: Sat, 16 Mar 2024 00:48:00 GMT  
		Size: 43.6 MB (43618771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee5c996f6220affb5e3a9fff80d7d6b2c34c9ee2f18c598ff6cdc543703fbfb`  
		Last Modified: Sat, 16 Mar 2024 20:01:32 GMT  
		Size: 6.8 MB (6816184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:bfdc8ac9496298fe24bdff9a1d4e68601d363e280842996207493d0d2d32b22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 KB (270314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7674b9bb0d32236c63735ccc51a2d9b61bee744ac82b0c59cb7d7ad5368c2413`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4821cc473f9f72b4df51ae52379833c84eb1694a7b61c4d95178656fd3e0d`  
		Last Modified: Sat, 16 Mar 2024 20:01:32 GMT  
		Size: 260.7 KB (260663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e0247422c981f3acd7b918bd89a9b8f0334dd4fcd8db994a3e53ce6931328`  
		Last Modified: Sat, 16 Mar 2024 20:01:32 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:25217718ac83b0faf5c9f718e10e100016d177b9c04fb88b4e99a4d8a56a5c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54392161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fa0d8715e24e98552621cfab1103a5236eebfdf18cde9fa06bb64dd65a396f`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dc938599f88b82dfd73d80168568dee632750afdfcf5d6bbdd92a2d8c8263a`  
		Last Modified: Sat, 16 Mar 2024 03:36:04 GMT  
		Size: 44.3 MB (44317609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64439516811614d19a03d4b847f94729c8165ecb5d5b9fd94a1e91fd26be338`  
		Last Modified: Sat, 16 Mar 2024 18:35:19 GMT  
		Size: 6.8 MB (6816269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e96bef1ddee327d707b24472414b46cc2924422baaa544cde56a8836f98b16fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de73bd99a195e8649f3da8c481a76654f037c0c8a687f47f2d6b82f5d14c155f`

```dockerfile
```

-	Layers:
	-	`sha256:ee7ba90f8be3614b5a6dc6bcf8c522e417089163db60d08bda93a3b1e494b9ec`  
		Last Modified: Sat, 16 Mar 2024 18:35:19 GMT  
		Size: 260.6 KB (260644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a32dd216cfa1cd8c9f83694c7b3dfd5b3f315b774986cdce9fdedad66c2e7a`  
		Last Modified: Sat, 16 Mar 2024 18:35:19 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; 386

```console
$ docker pull elixir@sha256:9b248932782cc917e9b237a38e7d1ba2e8f4cddd4bb24ea6a7ad04c0b8eda63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54726435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c458020dd8720943366d68bad4d0286b268ea07ea1f4b68d686c3fc2e147e8a8`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:27 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
# Sat, 27 Jan 2024 00:38:27 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d7c666f85c32ca0147fa55f4e9dc646c39ca6ff29b43daf4a3612522fac5f`  
		Last Modified: Sat, 16 Mar 2024 01:07:44 GMT  
		Size: 44.5 MB (44495033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887fd272cd51dd8278b5353c6f8ce12ba2e43c4c5d7686db697537b5f5fab42`  
		Last Modified: Sat, 16 Mar 2024 01:51:37 GMT  
		Size: 6.8 MB (6816224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:bdf4bf1bf8dbe401e0d43d25e9e666f1c85086623bd673ba02563b08212c6092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b4f384786e45a4d5dfb399b4e785754e365d1b9c6e9034973245ec3ed79ff6`

```dockerfile
```

-	Layers:
	-	`sha256:7c8485669fe6611601e6d7483c7e2ebb87617893a84e0daa101a700eac588761`  
		Last Modified: Sat, 16 Mar 2024 01:51:36 GMT  
		Size: 260.6 KB (260615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc5819ed0bb577d95863369baf40250aeb3db459cb806406f0787c1ec0f5a98`  
		Last Modified: Sat, 16 Mar 2024 01:51:36 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:da23b0d55c94bf07b50ff76f65ebc085ee514841a2be49e5ccf04212f3db0b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98516a63450606c74043625b0c55b77f961c6daea871817a99006c4c2054f454`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4cdb8a5b418fb0aed4fcc8290593bf957e14291acad6cff10d2828a9ef499`  
		Last Modified: Sat, 16 Mar 2024 00:28:44 GMT  
		Size: 44.5 MB (44538694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c33b37248ff0bc2b98ebd5a8655969f35c89fc4eae4df0ad0358a14d3af6`  
		Last Modified: Sat, 16 Mar 2024 13:44:49 GMT  
		Size: 6.8 MB (6816279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6d0f02998d5e3cc9f2a93fdaba4fc61c60c3a3076c832b3f7d3a8adab5d886f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 KB (268330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4064621e0cecda670ad4dd21b6b7ce11a25ae9018b143c3904272bb2235169`

```dockerfile
```

-	Layers:
	-	`sha256:9c89b60622606961996ea1b999a64149eec9f7078e4e7a8f92a0209bfc23bf09`  
		Last Modified: Sat, 16 Mar 2024 13:44:48 GMT  
		Size: 258.7 KB (258709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:491861764f095cae9397641a1f007c289c21479827729763bf802c57f83e4f1d`  
		Last Modified: Sat, 16 Mar 2024 13:44:48 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:30383066c33a7de21435cde5a9385069623ea308ca0fb6e8da0f436e6b89261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53832050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906f5229828dcbc6a3b3c8cb2131f95f2bf5df7dc2da72585287e954238cbad`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:40:40 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Sat, 27 Jan 2024 00:40:40 GMT
CMD ["/bin/sh"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb735d39ce15ab25e8a2c4be530ab351ad1b0f4a0f57f145758a7e713e365084`  
		Last Modified: Sat, 16 Mar 2024 16:40:01 GMT  
		Size: 43.8 MB (43839404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d12f35fa0f16fa0fd6f70b9f62725348e31e13a10989616a5e13248071a86ba`  
		Last Modified: Sun, 17 Mar 2024 14:03:07 GMT  
		Size: 6.8 MB (6816116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:10aef959421888ae5f9c7c53362a5eafdf0b937d4906face957753b0cd4b4628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 KB (268270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23575904dd1795e6e9aa6cd489b5dd1eb7661d974666ab25287f6eef93289fc`

```dockerfile
```

-	Layers:
	-	`sha256:46e9dfc512524c20401ffc7449bc8585b168f540824e3de3be678359f6b591d3`  
		Last Modified: Sun, 17 Mar 2024 14:03:06 GMT  
		Size: 258.7 KB (258681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f018e68b07fb46e05a58490922f1138a94ee0ade84e95c56d434822ad0238f4c`  
		Last Modified: Sun, 17 Mar 2024 14:03:06 GMT  
		Size: 9.6 KB (9589 bytes)  
		MIME: application/vnd.in-toto+json
