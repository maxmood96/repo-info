## `elixir:otp-24-alpine`

```console
$ docker pull elixir@sha256:268de95c3b3236282d1720acd8af52b2820298e062c42229422206c327a6a2f5
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
$ docker pull elixir@sha256:f7961a04828eeee78094dfaf6bb5107c65354c3ef28684242cce18f24aee09c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55829043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc519205fef0b1804ba6a5a26b4c4ddc0249fe81a4a909bc37bf437bb61f23e`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8fab31179660a342f2f232e841d27722709c930e6bc009cd5acf7ed1aa3a7f`  
		Last Modified: Wed, 21 Feb 2024 03:27:11 GMT  
		Size: 45.6 MB (45643970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709b91faeaec6c1b75977d507fa0a0f11365e43fd98222c7442b9923a351a7b2`  
		Last Modified: Wed, 21 Feb 2024 03:51:23 GMT  
		Size: 6.8 MB (6805669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e39064dc40dc964f1179d827ed861105d07e8101e774cec6aa1ca8ea0869d39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 KB (274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8965ffce27d3cbf61c4461869e57e063cc156e12bbd53e95f3655fac966c9f`

```dockerfile
```

-	Layers:
	-	`sha256:0c41f20e3e81cec25405db713375d50a72ccce5e2efb0a4a64178bae13c91a65`  
		Last Modified: Wed, 21 Feb 2024 03:51:22 GMT  
		Size: 264.9 KB (264905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c4a19269d7955b4ccd013425f579a3062af5f006b23cca274cb96e8b8fa5edf`  
		Last Modified: Wed, 21 Feb 2024 03:51:22 GMT  
		Size: 9.6 KB (9589 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7ffb8aae9ef3f496593fe15fff44544be98c864940354b87d45d6c832baddfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c18f822c0623af37f7c7b15a06999bb937853d93d8a8ef9a9725af1c4e53f83`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:07 GMT
ADD file:248255ed09e14a0af5432820adc48fdeff8b679f7965161e9fe1c7102a55a874 in / 
# Sat, 27 Jan 2024 00:15:07 GMT
CMD ["/bin/sh"]
# Wed, 21 Feb 2024 03:06:16 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 03:06:17 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Wed, 21 Feb 2024 03:14:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Wed, 21 Feb 2024 03:14:02 GMT
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
	-	`sha256:688fe3d0045e1ae434d6681d327e0dc971bc00d17f92c0e42fdfc982e68b8c3d`  
		Last Modified: Wed, 21 Feb 2024 03:22:30 GMT  
		Size: 43.6 MB (43618975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f225dc1eefc11b150cbc4f32e7e8fc5dd287cc8e338ad4dc9b3865cc9f642fa4`  
		Last Modified: Mon, 11 Mar 2024 23:20:28 GMT  
		Size: 6.8 MB (6816137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:12a1fd9edab4e5b824d7a69141c4c7509f92f60726f5f9eca3493f390bab9007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 KB (270314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71c801974ce053a1dbcf37bd8e8145a270083176cc5e885eb8386a9d352dbe`

```dockerfile
```

-	Layers:
	-	`sha256:5d8d940d04a17a858ef969dc00ed1a597c5c848cb783639319dc66250cb74c1d`  
		Last Modified: Mon, 11 Mar 2024 23:20:28 GMT  
		Size: 260.7 KB (260663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8df97e4bb67940e0ea7319173af6aa7bf69b7c7a5484b05526dc52c996cdeb`  
		Last Modified: Mon, 11 Mar 2024 23:20:28 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:35711259f4c908715dc623f5c9309111b0eb3ad14b80562b9eb5ea73a4e7508b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54391226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db586ca7db41a1bd8dff6740408146c3f364e5f35966a3400b87fdba87feef`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Wed, 21 Feb 2024 01:53:45 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:53:45 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Wed, 21 Feb 2024 01:56:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Wed, 21 Feb 2024 01:56:46 GMT
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
	-	`sha256:924d28ff09e6c029a4a69d94e99debeb709705686b09f125f37578a0fce53d38`  
		Last Modified: Wed, 21 Feb 2024 02:03:14 GMT  
		Size: 44.3 MB (44316712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d266f7e12becca9d6169c762d1f33ca71a2bec3f086c5099154c59a1bc8bb0`  
		Last Modified: Tue, 12 Mar 2024 01:21:13 GMT  
		Size: 6.8 MB (6816231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:af76b5c708b9f0968cf0c680cc9298d6b35596e034e0443ff278d3a6450f1187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84ceb2af84726f468fdced820bb5ec01197cc8c95408f88c7c436e2e0585ac9`

```dockerfile
```

-	Layers:
	-	`sha256:b3f01f6fec841b02aee08a376b9c32e058421048dc09fcc6fb82dcfc6311ae73`  
		Last Modified: Tue, 12 Mar 2024 01:21:13 GMT  
		Size: 260.6 KB (260644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90175cbb77d7abccc9cbdb6136dc196f134c7d04179d6f1d987e1c5172f1d6ba`  
		Last Modified: Tue, 12 Mar 2024 01:21:13 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; 386

```console
$ docker pull elixir@sha256:41883dc46dc46c0ce9adde71450c58d0b74e76dbe379e5afc62c465be603f139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54715351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75842e8830af051984485cf798f78d1a30405e51d8c4f17621fc8ce62f843605`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:27 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
# Sat, 27 Jan 2024 00:38:27 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676fa2c45d7c8267a2f0d2f321173aacfa661b5b39c1db749d11da2fa31232c`  
		Last Modified: Wed, 21 Feb 2024 04:11:15 GMT  
		Size: 44.5 MB (44494979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e6aa75b008822bb0d8b5484b43c875f14a9098f660c69a039301eda6d68360`  
		Last Modified: Wed, 21 Feb 2024 04:52:39 GMT  
		Size: 6.8 MB (6805194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:f2eb1fd30b9f0cca00909f2f9a7c74a656677b668c851868b7435dbc070da38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8133500134c1b1fa989795184c39132752962de0aa3a161626a47eebc25c82f0`

```dockerfile
```

-	Layers:
	-	`sha256:f53e04d1a6e63e9d9dc30c4fd889e4cbdbac5a2629807eb7a91ebd2ddbcfccd8`  
		Last Modified: Wed, 21 Feb 2024 04:52:39 GMT  
		Size: 260.6 KB (260615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3954bb8dbec76ab925c5d711381977d469befd03bfc9018099b617e4146c65`  
		Last Modified: Wed, 21 Feb 2024 04:52:40 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:d8aebc402d619e75dd658aab24bf65495db06095561628d7d97a2000ab04a20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edefb0632e729abba8919420fa82fc8bac23982939d9d317a54eabdaeca588`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Wed, 21 Feb 2024 02:33:06 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:33:06 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Wed, 21 Feb 2024 02:37:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Wed, 21 Feb 2024 02:37:50 GMT
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
	-	`sha256:b995f0af88a9b81f8326c5a61bb9ff4ea8beb3d3776d41757da43e882d953eb8`  
		Last Modified: Wed, 21 Feb 2024 02:44:45 GMT  
		Size: 44.5 MB (44539343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ac550b6d1c07f4d8a8724a8043bf5d12e9a1de87c640cff948343f9f8bbfa`  
		Last Modified: Mon, 11 Mar 2024 23:27:55 GMT  
		Size: 6.8 MB (6816187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ad080e09206617e8d7f8a90e76365175977d7f17a903b9eb11a4f50518e88834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 KB (268330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4187d5a53e485512ebc32153e14a864a4e90ddfb12071b8231fa3ec0b070f287`

```dockerfile
```

-	Layers:
	-	`sha256:52a891a03cf9f70c78948d6c2de5987d99614d6cbd75c0297792a5b3285f9112`  
		Last Modified: Mon, 11 Mar 2024 23:27:54 GMT  
		Size: 258.7 KB (258709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3cd52c95f43561ed62e52c260b65388ee4e14768fa3fd16405c564c93cb12f`  
		Last Modified: Mon, 11 Mar 2024 23:27:54 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:0ff5734ba526653ab8cbe33757a3c92233a0080dbffd368dc18637695814412a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53820990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f75b63a33518089472567a0ab02ed910c76eca964e8f12dd74dfc2e25f1bc0f`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 27 Jan 2024 00:40:40 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Sat, 27 Jan 2024 00:40:40 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc15908a414653eeb5a8b8f1e90600d0268dda7e295fa6bb1e3e4c8736b8ad8c`  
		Last Modified: Wed, 21 Feb 2024 03:25:43 GMT  
		Size: 43.8 MB (43839320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5059ad4cd1bb723e449c14674ccc9cd797aa3edec0505fdd5904e7085cce44`  
		Last Modified: Wed, 21 Feb 2024 08:52:55 GMT  
		Size: 6.8 MB (6805140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d853d4d825a97820e77e69d3ae7fc766dcf0b6d5327ef745a93680c7d7f9388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 KB (268270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a96d1c2321a8562e028d8674461d58c1627968b18a6c4b15f770d9eabaddf2`

```dockerfile
```

-	Layers:
	-	`sha256:bf5057c575269a030906dbd5c1ec1c9dec533c0c147185cf5e525551738b1307`  
		Last Modified: Wed, 21 Feb 2024 08:52:55 GMT  
		Size: 258.7 KB (258681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1892fa14877ff5f2b4844ec2c037979c6d01a80f3f94f229560dd941979a57`  
		Last Modified: Wed, 21 Feb 2024 08:52:55 GMT  
		Size: 9.6 KB (9589 bytes)  
		MIME: application/vnd.in-toto+json
