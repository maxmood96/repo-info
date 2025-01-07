## `elixir:otp-25-alpine`

```console
$ docker pull elixir@sha256:259b198b3cd84f411cf81107ef75438d144b6440b810fb4a402508368762b7a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `elixir:otp-25-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:f018165a34be290cb53b0470307bc85378bf84427eb1d6972e1a1afa8e4f32fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56544394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be2e5d451af8605f103720c7a07f0229cbfd78129e517654a8917f553d957d0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4bfe9d39936fdffcca98a58cc959e7aceb4a0ca840cb946df9c454b453435`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 45.4 MB (45400927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43185d795ac377d93ee90aec168a41708f9ab3a5102ebc99467527884864bb8b`  
		Last Modified: Tue, 07 Jan 2025 04:23:52 GMT  
		Size: 7.5 MB (7529468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:03c6c8cc2e568b1d56d26df6e236b086d4e5d6a8f8f6ae7cc8eda2e92b8d429b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 KB (283698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0264d4e5a81e7acc20aee04f6186678977d439e2825c4487cd18ba9dcd1ebda`

```dockerfile
```

-	Layers:
	-	`sha256:2c348660f53a8659fb446948aa5fc1e0d273545109e5d0f2989d828266aa5b75`  
		Last Modified: Tue, 07 Jan 2025 04:23:51 GMT  
		Size: 274.2 KB (274169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2549751531dbc029adadb8b7ad56ae53877fe5643fa63ad5c999c280489dccc9`  
		Last Modified: Tue, 07 Jan 2025 04:23:52 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:853ccebf742e1c1752a623ecd8035179f7afb780f495b670b3b40dce5c887f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55580358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324be7c7189a30e6626393275d2b6327a145ac121956939fa2eaaa5a9c8ae4c`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032252876ed94b98f59290a62438307b857fc27734d127194a38520451486e7f`  
		Last Modified: Tue, 12 Nov 2024 16:50:20 GMT  
		Size: 45.0 MB (44955653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b7a0fd3d096e5eb4fe883d2fa7649efad5e0cfdcdffec66e930b9d8da1bc2`  
		Last Modified: Thu, 02 Jan 2025 23:06:17 GMT  
		Size: 7.5 MB (7529218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:91708f22d74ecb24f0250a6968438b576c25c1b7acbf4aad46d22e2c23d70a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60998f2520c4adae5e932c3561c685eda89aa31512660056af4e14d154ef7bda`

```dockerfile
```

-	Layers:
	-	`sha256:ce4710500a82a481f7480a1ccd4ea0f9cd32ff0572c2b1d7aba0cf8310897fdd`  
		Last Modified: Thu, 02 Jan 2025 23:06:17 GMT  
		Size: 274.9 KB (274862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d485d8df58093fcae6a74946507bae302bfbb31920e1bc3d172f08c7b186a7`  
		Last Modified: Thu, 02 Jan 2025 23:06:17 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:59b335c22e47d80723d34ef508f89b02b6956704561de8486c991c395166c0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59542445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc58de78ed127a8d3ab1904fbc10f803aa0b351d1d1a1d3c532f55a1789b463`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf43345b637ddddc852bcfe60fac8645869df85ad3b9023d78f6eee34379d80`  
		Last Modified: Tue, 12 Nov 2024 11:52:13 GMT  
		Size: 47.9 MB (47925011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb17cb20ed6907cb17fa2f43e01f93b1a1d3dfc0d4154d18e530b768b35303d`  
		Size: 7.5 MB (7529708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:fd852bdd19dfd8800be574e303c1a8a9de9956140e3888bea2c988903967acf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ed271a97722121ec669d677dd5ecce5e692af799d70c26fbcfacdacdfa6be`

```dockerfile
```

-	Layers:
	-	`sha256:d845acdca8bcfc3bbe01b2e2bd7155b4a58ccda86792b71d5dab2229dd577508`  
		Last Modified: Thu, 02 Jan 2025 20:06:15 GMT  
		Size: 279.6 KB (279576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee64df32ccfe1387ec322ed9d8557cf88482e26011e4dcfc205ee92710e61ef`  
		Last Modified: Thu, 02 Jan 2025 20:06:15 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-alpine` - linux; 386

```console
$ docker pull elixir@sha256:01b84bb54b33367934d797c613f6c288294711967cddb4700fca318e695a1cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55068355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e742b4def26f5cfbc6a464d5a5f18460241c3e4bb84e6fdea90e016c3bbd0a07`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dad321e104162329e85cce8b34b65774c49baf98fe0403ca974c65c447b76d`  
		Last Modified: Tue, 07 Jan 2025 03:23:22 GMT  
		Size: 44.1 MB (44076100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f804e7cf1426de2f026ca5df4aed85c9e54c5b57d6755835fe9f2f2fb3f18fe`  
		Last Modified: Tue, 07 Jan 2025 04:22:40 GMT  
		Size: 7.5 MB (7529066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b45778c1a42ab8b648ca3c60037c96d4243b04ed79810c178a743b9fb6725e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 KB (278953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec58fbd94a7c9d82b7f65e2e119d4bef71bcec42ece8102bbe002c5ce3a19e6d`

```dockerfile
```

-	Layers:
	-	`sha256:6ee83cf32116c2a8d6ddb9576e3d8c208402a51ff6fb7df9cc17d38eff3b515f`  
		Last Modified: Tue, 07 Jan 2025 04:22:40 GMT  
		Size: 269.5 KB (269451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73c253c1c1949d9e30e92811ac615828422296c0bcea9884312ef87f4b3f0eb`  
		Last Modified: Tue, 07 Jan 2025 04:22:40 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
