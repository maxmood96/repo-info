## `elixir:otp-27-alpine`

```console
$ docker pull elixir@sha256:b8b76874005955191f3b8edfb01709858768c98adeeeb742d3d757b9e8aa1184
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
$ docker pull elixir@sha256:f6ed0bd9e4bb13e9cfcbe46cdbb872cebe81e4c3d64c43cdca58a42ae2d5e1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e30bb25d0b6c32930e5043bc3baa532c2103fac0ad92801a52b2d5ba993a74b`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845e47744390803c6c9bbadcc3e772a8e0b72df4633f2453700258703486252`  
		Last Modified: Wed, 08 Jan 2025 18:22:44 GMT  
		Size: 49.4 MB (49422345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f3bd720b59f82235a9f5bf3fa6409799f37f7c1f81d8d3c9d1d76b9e8595c6`  
		Last Modified: Wed, 08 Jan 2025 19:17:59 GMT  
		Size: 7.4 MB (7449950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ca13392655131758b2d0c56763a8b438725a58ac2ef1a605aa7c17fb58b570c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 KB (289979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4dcb74751630d1ca82a3a2836dd3a63f565eb2b98aacde50a9c4574c59175b`

```dockerfile
```

-	Layers:
	-	`sha256:5598b00c8df436b3d3c4596a7d93f9d7ab764e3347e2404638051cc909426e28`  
		Last Modified: Wed, 08 Jan 2025 19:17:58 GMT  
		Size: 279.6 KB (279551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce63d5b27a3dc2fd97608c0feaddfdf346465e6d522a84b6107e6e188202c229`  
		Last Modified: Wed, 08 Jan 2025 19:17:58 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:c9e294872a567245be810115c32a31555a45bc1361838c507aa51bc022a89c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59331587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c363764200378ba0fe002c3f508f7067e6b2c31f5478de25e76d6e6235980b`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
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
	-	`sha256:be67333f68a966789093e163bb78f0452b6d79a358247d0709c032e31867fb83`  
		Last Modified: Tue, 12 Nov 2024 16:24:56 GMT  
		Size: 48.8 MB (48786925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6abb058a59bab20e847529079d08fa263f0e9c69032f73c90a03633a535916`  
		Last Modified: Thu, 02 Jan 2025 19:54:34 GMT  
		Size: 7.4 MB (7449175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:8e5e089fe435204a7b7c0691066b6ace5f811b23d9f800dd8002c76f59a6c711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 KB (284927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8ff4e9b7a9a0fe6f400698a531ad7958e4cc0d54605ccc58db38794dd53c2`

```dockerfile
```

-	Layers:
	-	`sha256:72ab4dcf1761299315ff20a949443b301c31eeee1134d3593932b29739645d39`  
		Last Modified: Thu, 02 Jan 2025 19:54:34 GMT  
		Size: 274.4 KB (274405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f442414466f4b6ea1ff23b48d59a62be76e2de175d452a2ad4ae697444d3a7a8`  
		Last Modified: Thu, 02 Jan 2025 19:54:34 GMT  
		Size: 10.5 KB (10522 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:0d69539675311143d59b22e252c872ec22712780125a4915db4827cd05681c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60747312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025120302ef9bb9799a6a85c9783bf250d6873cbdbf6410348cd9b6c97dfc116`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285649b7ec4ad6688b61b2d88de12f731ac0d93b23f115477bdf73e8a507fd79`  
		Last Modified: Wed, 08 Jan 2025 22:28:45 GMT  
		Size: 49.2 MB (49206681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55762c0745fcdd9e53d193948349b302f727547822d81722603d9a9ae768a5`  
		Last Modified: Thu, 09 Jan 2025 08:07:46 GMT  
		Size: 7.4 MB (7449862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:4823f0056fe04f37adc73894ace9c33be6354149492ff544eb4cf8d584b6bfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 KB (290919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e1c5da0f7af0b0b48eaade4177a6df8e82bca4deaf44533d7fbad02c584cd`

```dockerfile
```

-	Layers:
	-	`sha256:b9d35f2224063ae078bf2148cea01ac8a86a0ff9a9cd47ea5665a72382336ba0`  
		Last Modified: Thu, 09 Jan 2025 08:07:45 GMT  
		Size: 280.4 KB (280363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c89d674d9994d3a06b941c662f077a3e07751b697e93df6654218a180a3e55`  
		Last Modified: Thu, 09 Jan 2025 08:07:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; 386

```console
$ docker pull elixir@sha256:ddfa73e0f5b9a97fe93ea8a63464a398bf661ee9055084b277f6e2e49d9f9b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58896206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84239350c5c3bc89f04900902904420d815d3d4a3f4ed3890fb92a84b629aafe`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bb38458eb135af68e363fdf191d7ada36282b8cb7b9900830680198d84a9e`  
		Last Modified: Wed, 08 Jan 2025 18:16:40 GMT  
		Size: 48.0 MB (47976032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036311ad71e00f4b8ce74ecde0324aaef72ea6ef7bc3a3535e89ac43fd124e5e`  
		Last Modified: Wed, 08 Jan 2025 19:17:58 GMT  
		Size: 7.4 MB (7449205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:1d7142689c2acd44de6f6428a69058f447c09682c50247483df21f0800cde929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 KB (285204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36debbeb98988d430c3c5ebcbf0050fbd573049e8f3d7c3a250b79c4f87ed657`

```dockerfile
```

-	Layers:
	-	`sha256:e7f4bcbd116a9bcc3f2e4ce4ec03ee8971eb016e359393308249f6a68870101f`  
		Last Modified: Wed, 08 Jan 2025 19:17:58 GMT  
		Size: 274.8 KB (274818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2706dbf62907ee66d1168bd43296443528dfd6ee286be2fd4fd7b2ef9851b0ba`  
		Last Modified: Wed, 08 Jan 2025 19:17:58 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:20af896cd253ddd32af132a3140ed1bce82f706d076806d8964046d07619469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59045101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf4b8f78cba3d644abcdefda564478cd9b0a99623308b835e74b4827500f6a`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33daa9956e417e81adb800819ceb8166e7e64fc7d7bef544bf9cbfbe52bc8113`  
		Last Modified: Wed, 08 Jan 2025 21:42:06 GMT  
		Size: 48.0 MB (48021493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b633b9fa125837ef81977e5280c0914b0507f813b0e6730ba20a7aced64526`  
		Last Modified: Thu, 09 Jan 2025 03:32:36 GMT  
		Size: 7.4 MB (7449202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:98c5eeafcae656c63bbb55b6d76fd2d94a2e6c783433c3d446c4db3032109f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 KB (284164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1d7a82eaef76a53aab4ff38335d28420f872e16c4086066e42e62583b2c454`

```dockerfile
```

-	Layers:
	-	`sha256:e201717158afd96425d4eaa1cea6644400fd7e9dd9c86afd3ba6a29aa3de06a1`  
		Last Modified: Thu, 09 Jan 2025 03:32:35 GMT  
		Size: 273.7 KB (273680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380790e5bc945fcfdae7f7b191ee13bacab491eedb41f44970a9575e1ad08c3c`  
		Last Modified: Thu, 09 Jan 2025 03:32:35 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:f390ceed517e290852b8bfb9b5878dd915980644159d903b8440aa1e5e9c13ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58600931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ed62d36d4b8945e8c20b79d65227a3c86b337fbf80dd2733f53a8fb71f2c71`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d99c0459ca41e10138550cdc8e86de2012210d9764ddaee4ebc1449e30530c`  
		Last Modified: Wed, 08 Jan 2025 22:19:13 GMT  
		Size: 47.7 MB (47688697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a6f06b6807f15a1d84284b9718d59516d2186077071b4e9f6e542a80ff8fd4`  
		Last Modified: Thu, 09 Jan 2025 08:58:45 GMT  
		Size: 7.4 MB (7448912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:90a623b82e06728a50a494643273f59634c1846aa7c3f8980ea2ca0ad1040e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901add9a21b4b8bc5b9b103183c1908613437ce145f7436cc815f09222f21818`

```dockerfile
```

-	Layers:
	-	`sha256:5422d49cf77b4832f941c0998f4aaa1a428a2df83ed3d4d40ed9a171459ec8ca`  
		Last Modified: Thu, 09 Jan 2025 08:58:45 GMT  
		Size: 273.6 KB (273634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d5ce76e80a7285d043da3971d4f6db8b8ec24dc8eba50c74fc84c48f234259`  
		Last Modified: Thu, 09 Jan 2025 08:58:45 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json
