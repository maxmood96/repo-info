## `erlang:alpine`

```console
$ docker pull erlang@sha256:07960b3e2d5980a4429cc8a6b12e5ca3af819c5575ebe76e927ac315b4f7845b
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
$ docker pull erlang@sha256:dc5a08b9bb17291f68d4f3a5c71f6994a248fe3d9e781b0cb77ef1dc8a376ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56313415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac07b93894f5ca35d0ead754668584db3d4eb30e8bb3476843a5402e8d79986`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:37:06 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:37:06 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 15 Apr 2026 20:37:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:37:06 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199086653d42efab7ec7b38a29d8ad095651e1b3f87e971609b459c01fc4cbd`  
		Last Modified: Wed, 15 Apr 2026 20:37:16 GMT  
		Size: 52.4 MB (52449226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:5673653b7e34c90964d971d2d1ddbc1a1a0d64ab0a8fc9294ae9ae429cda800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 KB (292319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad370a910a1c2cabe2c2c7364b2e7547e2b23d224275158517f11e98cac81336`

```dockerfile
```

-	Layers:
	-	`sha256:a3b5e49eab5a581f1be44b5b43c1b6ede38f85a5562e647a429749399a803801`  
		Last Modified: Wed, 15 Apr 2026 20:37:14 GMT  
		Size: 277.0 KB (276951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3d6ed2931fa48359b524279a42ee575b56154b427893c1b606483b01926deb`  
		Last Modified: Wed, 15 Apr 2026 20:37:14 GMT  
		Size: 15.4 KB (15368 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:933b571d92acc56e4a245125f442cedeedf02c85cec03851c7360f3e6229d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53225661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e289a507468a5e6815c1987389f1a016a2d0a3a43aac5624dc4f9c2539951434`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:39:50 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 15 Apr 2026 20:39:50 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 15 Apr 2026 20:39:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 15 Apr 2026 20:39:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55b4ac6ed7123031305a46b0a0caa5343888402707db9b72937c03bcf9f5354`  
		Last Modified: Wed, 15 Apr 2026 20:39:58 GMT  
		Size: 49.9 MB (49942538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:97b40c42e89cdc56beccc8a4a7dc8bbede7fa97ec26c48003b87efe2adfbec18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 KB (290546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a98c829749ba7cfdec8cfbbc9912877eb16b01ffe692164bd498a41a3331e4`

```dockerfile
```

-	Layers:
	-	`sha256:936b122ebbe71246b0ef9757cf0e26696ac64ba41d7877b8565ff8b4cb95997f`  
		Last Modified: Wed, 15 Apr 2026 20:39:57 GMT  
		Size: 275.1 KB (275089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0921747434347410c338d19fbec07226dc436132b48a98c6e828b02e9b192e`  
		Last Modified: Wed, 15 Apr 2026 20:39:57 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:083e6aec28df765ac9e9f55d0f53b7cc471eaca3e9befef2c0396ce27293e408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56876342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669c05a29286bc2812c0bb47679a5e5bb0457b1c0828936dbdce3ec04aeee460`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:25:02 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:25:02 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:25:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 09 Apr 2026 22:25:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b12ed99d8818c8e579869ce89d0a0b9e90c2c7af6759b92e254e98a4ba3bddc`  
		Last Modified: Thu, 09 Apr 2026 22:25:11 GMT  
		Size: 52.7 MB (52679251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d513b5de0a4fa12df674b7aa61a73e2538024ddaf66d6045db6eb575a9fda2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 KB (295566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a149f3bdbcfaa38b100f23b6984c93834cf8a873c94e958618005500501105`

```dockerfile
```

-	Layers:
	-	`sha256:5243085a96fa4c4732d5c0ed6578d005c4c07230723647aa17b11ac939d9ff29`  
		Last Modified: Thu, 09 Apr 2026 22:25:10 GMT  
		Size: 280.1 KB (280081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a741402db1d9c5cbb143cf88c61f941a5de5997bc09b800e1f4d81aee737e78`  
		Last Modified: Thu, 09 Apr 2026 22:25:10 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:7b729ff8d1e05acb42929ccd0a959f198171a62b19c2eac1815771926e5e9d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57204769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e830956f387f07e13e914f4feab9adb9eef880f6590425a335f04cf01d62f4da`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:25:04 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Fri, 10 Apr 2026 00:25:04 GMT
LABEL org.opencontainers.image.version=28.4.2
# Fri, 10 Apr 2026 00:25:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 10 Apr 2026 00:25:04 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ae4f8a55e01cbae92780db36771e9b2977d61909ae6a18657cfb522d25916`  
		Last Modified: Fri, 10 Apr 2026 00:25:13 GMT  
		Size: 53.5 MB (53517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7e2f59880be4db23257cf3ed957b37a83f8b7b8d71dd5e8bf3c28c1d8e42ce9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 KB (290250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bad00bab901eeddc1b446cdc56c3de40dc3d9f02eaee446854cc173a2603fb6`

```dockerfile
```

-	Layers:
	-	`sha256:795cad3653039b2c0e8e7a1b38566a0f2368008eebb11ca7f40abe9d5333d4da`  
		Last Modified: Fri, 10 Apr 2026 00:25:11 GMT  
		Size: 274.9 KB (274919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a355961b71d7948fff6ce2a26e56bc92f6f04b7f346abcd4c7b4049e75c28e2`  
		Last Modified: Fri, 10 Apr 2026 00:25:11 GMT  
		Size: 15.3 KB (15331 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:60cda9543bb5b8b49d6ca0048219943c16523a05a0be7b4403b6bbfbae7f121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57717602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9f92e1e390fb4fed84f6ca62bb00d30e4dc3cbaf2d21db54c8e4d9f37b6dae`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 23:33:29 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 23:33:29 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 23:33:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 09 Apr 2026 23:33:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453306494e0de4f3f07c8001fdb905c058853ac7fd9d5d2f8a5a9ab62da9539`  
		Last Modified: Thu, 09 Apr 2026 23:33:45 GMT  
		Size: 53.9 MB (53887959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:857210f73877bb5805edd0fdcc8b73dd173a07474d5db52c85eae446ca906769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 KB (290491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee360e7a784518873bd3e96d263e19965bca59bd29089d4563f64ce7f77b6e`

```dockerfile
```

-	Layers:
	-	`sha256:12ce5cd5c1a763b531ad5cad3840f7a8ccef27d2225ff7702536610eb673f78f`  
		Last Modified: Thu, 09 Apr 2026 23:33:44 GMT  
		Size: 275.1 KB (275072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c39469e206da3a828bd2b42f3e57320c008865243c22ab0a888560d5adb5079`  
		Last Modified: Thu, 09 Apr 2026 23:33:44 GMT  
		Size: 15.4 KB (15419 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; s390x

```console
$ docker pull erlang@sha256:a23de7c7873b60bf56fe910c041ebda53959542aed95d6d122a75d69d09593d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57142158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaf4da6fdb9460798671d8238f2c653dfb1599342533689bbb8927a6fcac01f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:52:55 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:52:55 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:52:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 09 Apr 2026 22:52:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693f9d07b0b3198dba436496e3b50b5265bcb5350e26b93d1a2b140049c0f605`  
		Last Modified: Thu, 09 Apr 2026 22:53:09 GMT  
		Size: 53.4 MB (53416825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:2e4270d5503e6992c4e6fc2325e4fb89eaeba6dcb0111460ed77749a6912c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 KB (290400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82fb53f3aa18069b7b32fb81e65f2bfedcaad017c0217766433da119f12b497`

```dockerfile
```

-	Layers:
	-	`sha256:7a2e5b4c67af0a9428b54a78576fa0bc5854d7f48839457bd558c56480beb6c1`  
		Last Modified: Thu, 09 Apr 2026 22:53:08 GMT  
		Size: 275.0 KB (275032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddb5684b1b0b5a221d70baa00e89ebc15171b4537627f52de52b6c981f94f58`  
		Last Modified: Thu, 09 Apr 2026 22:53:08 GMT  
		Size: 15.4 KB (15368 bytes)  
		MIME: application/vnd.in-toto+json
