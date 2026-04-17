## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:317acf72837d78c0cb61f5791fc3de2bb016374bb0a92102956aee56a1c914f5
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
$ docker pull elixir@sha256:f040cdc79703bfa2cf57e241d2fc8c2f14bb50e4227bcb28414b30158b745962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57527660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6bc4eb1526b91256b9ac1e9e0b41711c1895b4fda57ce10463d72ca72fb88c`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:35 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:28:35 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 00:28:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:35 GMT
CMD ["erl"]
# Fri, 17 Apr 2026 01:15:15 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 17 Apr 2026 01:15:15 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 17 Apr 2026 01:15:15 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade15963d7e2176de95239635da007fdf1fa4dda57b364f3c2db84eb84e5f743`  
		Last Modified: Fri, 17 Apr 2026 00:28:43 GMT  
		Size: 46.1 MB (46105027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8524166c858a2bdff85b51ba08d96bc0d94e1f81a01521f2c2c543ed5289588b`  
		Last Modified: Fri, 17 Apr 2026 01:15:21 GMT  
		Size: 7.8 MB (7792312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:61752548f2cb88733608ee1519cefcd9ffd2935991104936b929b532824b9b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b106a4b1aed40c67eeaa9aace8744776487b36a32e1a2c816dc0ed7c2132f39`

```dockerfile
```

-	Layers:
	-	`sha256:375fe0f891c4535b79bb62f0fc7211ef88801e165dc6298fd38195f076b37ff8`  
		Last Modified: Fri, 17 Apr 2026 01:15:20 GMT  
		Size: 279.7 KB (279726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723026124facb5cbb39747f830ce5df05de221b07f995782560ab52a62c110b1`  
		Last Modified: Fri, 17 Apr 2026 01:15:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:98ca7b0edc7589f7eb10877b35b6233954838a3ce32cb330cfa3f50ceb106325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54661969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada0efcf5112424c10d2ec67d0e94a952c943d793f9abf2b9858ca7b099f5bd7`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:25 GMT
ADD alpine-minirootfs-3.20.10-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:25 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:25 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:32:25 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 00:32:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:32:25 GMT
CMD ["erl"]
# Fri, 17 Apr 2026 01:17:04 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 17 Apr 2026 01:17:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 17 Apr 2026 01:17:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:70293f0413d2297be1651e9765a7327f173f0d76bf7e1229f6e604faf61552c4`  
		Last Modified: Thu, 16 Apr 2026 23:54:29 GMT  
		Size: 3.1 MB (3100051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180a2f2f311d781af9057e7bdfcbb9e821f214373b4d943e6215424681157bd9`  
		Last Modified: Fri, 17 Apr 2026 00:32:33 GMT  
		Size: 43.8 MB (43770104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083de36dd2a09edf1eb92ac33c4a997a80663c507fcf077d152d761e83a1d84`  
		Last Modified: Fri, 17 Apr 2026 01:17:10 GMT  
		Size: 7.8 MB (7791814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:f85415c736bf9d8396c13ab9361c658eaf0d2fc24cebef3d548e4c32a8984b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 KB (284997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cff039a4be75f0ea712890d2d3881e749df81b83f99c4e1cc5d1dcc0661352`

```dockerfile
```

-	Layers:
	-	`sha256:ad38b35293b42565ac2ec5712026f1e5cd209e6a94506182efd3ca83457c0115`  
		Last Modified: Fri, 17 Apr 2026 01:17:10 GMT  
		Size: 275.4 KB (275439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787504e62632ea0a4e5824b7316a85b1229ecf6086a4584493685ec1c0d42915`  
		Last Modified: Fri, 17 Apr 2026 01:17:10 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:c063c222b6dbd921032e731d3280b8fc60419e429b53f664a9605b9c30434682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57785660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939dbf7136892d065bf327202c45bf1636dd3db7e6b85643abfa3f31afd2063e`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:48 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:29:48 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 00:29:48 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:48 GMT
CMD ["erl"]
# Fri, 17 Apr 2026 01:39:51 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 17 Apr 2026 01:39:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 17 Apr 2026 01:39:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991e65a8013e90a674613cc720249289d4853344ded6e0cb43098a2f720b746d`  
		Last Modified: Fri, 17 Apr 2026 00:29:57 GMT  
		Size: 45.9 MB (45901056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1b0da0342ca5ec224cfeb95ba8bd06d4bc50cdf00076c5b2c0b2a8cb6808dd`  
		Last Modified: Fri, 17 Apr 2026 01:39:57 GMT  
		Size: 7.8 MB (7792285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:1b4256730db17a272a9bb9191f68eb3c7be7a078b938f81f1b099daebbee7756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 KB (290084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318e0b82c60e1f05177f52eb2e1b82c00f4aff7dda4926f18e60db3401c32101`

```dockerfile
```

-	Layers:
	-	`sha256:ad3f26a37fcafe6da05c9b189ec40facd767e3096cee3d180ba64f4c28cb8cbf`  
		Last Modified: Fri, 17 Apr 2026 01:39:57 GMT  
		Size: 280.5 KB (280507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d007051c4bfcb37c99f9ea455a5c1d791b5eec4030921512ea3af1117ea00a`  
		Last Modified: Fri, 17 Apr 2026 01:39:57 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:c753e2b92465c5c509cf908b5b93d0561b0fe176689b83d6a3b7c5912794e85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58505321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c8f4b85aa1982d59280b83291e5e96d59941e60cde7bd3933c3a77e0615379`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:19:04 GMT
ADD alpine-minirootfs-3.20.9-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:19:04 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 21:32:14 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 21:32:14 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Mon, 13 Apr 2026 21:32:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 13 Apr 2026 21:32:14 GMT
CMD ["erl"]
# Mon, 13 Apr 2026 22:18:07 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 13 Apr 2026 22:18:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:18:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:deafad5a9be5989c4df2fba946fa81d5f8f786fc89fbc6a1f294ce7e14e8aea3`  
		Last Modified: Wed, 28 Jan 2026 01:19:10 GMT  
		Size: 3.5 MB (3471744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce1dd9f35db70a4f0649e745237b4945abc052ba57a3fd9031219237b5775e`  
		Last Modified: Mon, 13 Apr 2026 21:32:23 GMT  
		Size: 47.2 MB (47241558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae14e59fe204cf622a1f956ffd2db5ad5ad2dd950f6a558dbe8501f0cd567f94`  
		Last Modified: Mon, 13 Apr 2026 22:18:13 GMT  
		Size: 7.8 MB (7792019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6d523deb26c8481e0b6ced3c2d2ce021f305f0b87b0c60193fcbc0d1a0665ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 KB (285821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef95ef425a7b5b5c7d2238cfeb65554e395070c6905052333712e8313b78efb2`

```dockerfile
```

-	Layers:
	-	`sha256:4931395643dc9f99ddbafcdb4bda9edcb4733d2ee9d64db04063e394b469ac20`  
		Last Modified: Mon, 13 Apr 2026 22:18:13 GMT  
		Size: 276.4 KB (276362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e56659b713f9fdacfed4da00b45c358b31a224a23a3c2a7664b8bc1d26fc6b0`  
		Last Modified: Mon, 13 Apr 2026 22:18:13 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:43495902fd462f0c88dd2449f6085ee04c75903fb543ef594bc94b6e0e8e322e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56129411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf40e083a82797fd1e554fb9ac5ad8031605d4b3073adf132e35ebc58f1d8185`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:56 GMT
ADD alpine-minirootfs-3.20.10-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:20:53 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 01:20:53 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 01:20:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 01:20:53 GMT
CMD ["erl"]
# Fri, 17 Apr 2026 02:19:59 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 17 Apr 2026 02:19:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 17 Apr 2026 02:19:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:20cdb1125d416be08241b781f88b15b42332c2aa8dbfa8619a7c0093274c033e`  
		Last Modified: Fri, 17 Apr 2026 00:01:07 GMT  
		Size: 3.6 MB (3581214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e251eacab4307ae41d2efd27859240640dfe26858b84785570ffd1e5366792d9`  
		Last Modified: Fri, 17 Apr 2026 01:21:10 GMT  
		Size: 44.8 MB (44756439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306c8273363b5492697b4c661544a835798c0c57e44ef14454b9a8ec8929b68`  
		Last Modified: Fri, 17 Apr 2026 02:20:20 GMT  
		Size: 7.8 MB (7791758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:a21318a7764d360b9f39203de2be5a87dfea1ed1965016c82fa9debaed04a2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 KB (283012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9212783c24b4bc4db7e2c40138a51aecd4609cfa7f8dc304e546613a16de241d`

```dockerfile
```

-	Layers:
	-	`sha256:ecb3ba57e26dcaa2ff94b7d60bb10ec0f1ede1cd85cf28ebd05ca00eab81660d`  
		Last Modified: Fri, 17 Apr 2026 02:20:19 GMT  
		Size: 273.5 KB (273488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3862d2c29d4eee8490faa4d0cccfa42b57b702bd8ec013f59b14b005eabc37`  
		Last Modified: Fri, 17 Apr 2026 02:20:19 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:6a4d58161c55600a5a5afa6fc0fb4cf6475eabd65408b53bc53bf76e11a59a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55677131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83b66afe3131124d295893bf810e58b687e16a2b1d74e8ca227c21aaef314d`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:58 GMT
ADD alpine-minirootfs-3.20.10-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:58 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:48:22 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:48:22 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 00:48:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:48:22 GMT
CMD ["erl"]
# Fri, 17 Apr 2026 03:04:48 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 17 Apr 2026 03:04:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 17 Apr 2026 03:04:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d38f020baf1fa2c87122ac85c7c1277244aec5f8a4a3f4c8a78bf2d10851e1e4`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.5 MB (3466630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14d87aaea22d27951d830c5b8ef72e488ea0f712186dea38488e75a6950c2f`  
		Last Modified: Fri, 17 Apr 2026 00:48:36 GMT  
		Size: 44.4 MB (44418957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c37165535ae3dfa81e8a2ba777f5e190f17048adac031da7668635e591546`  
		Last Modified: Fri, 17 Apr 2026 03:04:58 GMT  
		Size: 7.8 MB (7791544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:49e0f37aed85df5e0e0dffdb2f39d5944ab05a3ec8e50ca98995cb49f4af3864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 KB (282946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5647b2250b597364b02287f741bef7db36b079e91e082d16c325fde4c605dbeb`

```dockerfile
```

-	Layers:
	-	`sha256:7b4534a907591192e1a11317974911e1b1a5f1fd65fb9f7609aee96ee5213fe4`  
		Last Modified: Fri, 17 Apr 2026 03:04:58 GMT  
		Size: 273.5 KB (273460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6afe3d95c7926866b4e648b0c16757d57bb1464870deed6953dc7d3da36edf`  
		Last Modified: Fri, 17 Apr 2026 03:04:58 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.in-toto+json
