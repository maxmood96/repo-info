## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:72321bb784962314ef72fae59ade734dd32170c6641b877bdf88cb110f5ee0c9
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
$ docker pull elixir@sha256:6c71915dd55db73817e1f2040dfa22c00b0ed36e75b13568c188400d0b9436b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57570858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061542b8d679e3b0bd4a78d9ff87bf1a204d1c3d8cb641b00579f4f9893abbb`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:cf3246aeaa406a2d91d08f5cdaf2b3da64dc55e90233f66b3c2f420fa5e4a83e`  
		Last Modified: Wed, 22 Oct 2025 17:48:33 GMT  
		Size: 7.9 MB (7858985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ab74b7575b1e26018ebce4635f88cae1655365e8837f9f76b2e3b690f9e74072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 KB (289903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf31806a530995e4310e566cd4514113a32bea112d11b7bc752911f370cbb6c3`

```dockerfile
```

-	Layers:
	-	`sha256:731ceb35c17d6fb43819d22057bc6fb0b4cb8bca48f7cacd1365807faa490c51`  
		Last Modified: Wed, 22 Oct 2025 18:45:30 GMT  
		Size: 280.4 KB (280374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb14f0ff2d8bb6b0650887d9df3384c579d101f89aab329ae93ad8f80ecaf12d`  
		Last Modified: Wed, 22 Oct 2025 18:45:31 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:22da4dbb4c6fee7a39471120a51e2c1f9347ea29e57fa23f7c7ab17a7da5e3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54701429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde00af9d6ed7707eeccd001166cefa802aa0ce3a06328d17662e1ca1a78f510`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:132b874f205aba7b6d71b72e606d964cf7149ee77bad5a886421c691aa4f7de7`  
		Last Modified: Wed, 22 Oct 2025 18:30:48 GMT  
		Size: 7.9 MB (7858322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:858b67aaf3dae388e2f3989c61a661d64454847c9687def221b1bd74841d82f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 KB (285687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35377244d9b195de61cb88701567d86ab74fe3285929c4880e4ef526a7f9eba1`

```dockerfile
```

-	Layers:
	-	`sha256:72a35e76853e8981c7d6eac6860a83977bba6052e2d34e89f96aaef67b72088e`  
		Last Modified: Wed, 22 Oct 2025 21:45:15 GMT  
		Size: 276.1 KB (276087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f836cd1c7081a1def1693d8ccaad7ee95e21bf40fa00e1551608d99daeb46fe`  
		Last Modified: Wed, 22 Oct 2025 21:45:16 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:07b2f84a0e8c4f79c285bb5e411dc7787515765c01570bff6eebce5bd7383e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57822141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df719fc81ee38ed0320478305463dece017ae10ca4d4d9a19163bc5c3f8d8078`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:557315ec0fc72ed4031378df6b84b5e613a018fe900776e3b6254f6e08eb55b4`  
		Last Modified: Wed, 22 Oct 2025 17:48:01 GMT  
		Size: 7.9 MB (7858621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:b9cca4a89bc2a72ea6656591ed2a022ae719b369bd32d8f896f6153fce98b475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 KB (290776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce6faf66918d5303ab609b7fa859567dbba9a696ed7968d5453c5b82ddd07be`

```dockerfile
```

-	Layers:
	-	`sha256:138907ff63b309d850b8540627a0a1f43caef9d6156ac7f364f9cc6f818d54f6`  
		Last Modified: Wed, 22 Oct 2025 18:45:37 GMT  
		Size: 281.2 KB (281155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fde381201d0f5db79786da5648ac9036e11549fe05c13aba9b562909355e9d`  
		Last Modified: Wed, 22 Oct 2025 18:45:37 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:9be9667faeb1fb29d5696d85ae5675ee99411ffddf8c1ff882cf1a7cf14f4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56009798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d085ff453724a5a8c80d3bab78273db2a039f6521a54b1d8dd8dc8b7dfc240`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:69b8be8dc0beda31f83eff4ec897ab9678e00c7f3f97e529184c0b9f74367f8c`  
		Last Modified: Wed, 22 Oct 2025 18:03:01 GMT  
		Size: 7.9 MB (7858268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:d4cd26de873db9a9ceda58436f894fcfa1e0af7e910a748da30c09f287497802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 KB (284804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0185332f32efa13d602ed87f8f31e8426e97fc4b4390222f9a5fefd43dec9`

```dockerfile
```

-	Layers:
	-	`sha256:09a96048d968d91180734ef95f804c2b3e78bb1616a60ec5184ab2d51d176375`  
		Last Modified: Wed, 22 Oct 2025 18:45:41 GMT  
		Size: 275.3 KB (275302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04e94fe2e4aaf68ac6e6bc579cd885eb78621a1a649f4975083ca2b3a461ab5`  
		Last Modified: Wed, 22 Oct 2025 18:45:42 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:6c6eb29e087f2ec24c45605aca33ed9dc77c70e7c4d11ef64eda2b79b032d844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56165834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9597fba280188dee5efeec3a9e3432a8731a4adab27cc633da9bf0c62ad1c02d`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:cd8b622348b72731aa8e1489c94aac38273b0866c162dcd767f94cc81fa73ea1`  
		Last Modified: Wed, 22 Oct 2025 18:15:19 GMT  
		Size: 7.9 MB (7858125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:c5e85f31118500b3418cfd738baef2bafd6e2066c05b7e391e9b0998fa4235dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 KB (283703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46657b9afcc0f19f21af021dea28cb40cc26a66c8103d316a30e94f32315b16c`

```dockerfile
```

-	Layers:
	-	`sha256:fc3bf73a9f81e6265b576fb036399012fbd89ac800944dc28fb09bc492046b77`  
		Last Modified: Wed, 22 Oct 2025 21:45:23 GMT  
		Size: 274.1 KB (274136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b01f747faa8eba74dc86fa455fd41c875b951287d87787f20d2e8973f1c043`  
		Last Modified: Wed, 22 Oct 2025 21:45:24 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:046500b6dc6e0c71526eb6e6d721d746c00ff1523536a3d74358838a67d0b106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55710479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5e47286783eb801e53b365fea81a4a723d21188e530dd03758f09c299fa295`
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
# Wed, 22 Oct 2025 11:46:49 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Wed, 22 Oct 2025 11:46:49 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Wed, 22 Oct 2025 11:46:49 GMT
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
	-	`sha256:864c23d018a9d5bb72f3e9f4a116b2d82adb2f8abfc1dd4e198d3391f4e31c6f`  
		Last Modified: Wed, 22 Oct 2025 23:44:31 GMT  
		Size: 7.9 MB (7858343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ede92107947ffc68f64d8633f841c8d9285c9f2a7043558de89a9a7e972f08d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 KB (283637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7a8bf88bf0ddc5428b7d149b7621c72cc3a4505f2f37056520cbdbe68481a`

```dockerfile
```

-	Layers:
	-	`sha256:61a797118002c092fcbbca8688be5a892f53afcf8f866190ecdc2e02cb7a19a7`  
		Last Modified: Thu, 23 Oct 2025 00:46:18 GMT  
		Size: 274.1 KB (274108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da5f913291c8abb9996204e73cd15b1d400bf959111277f80c96d2e02e6c971`  
		Last Modified: Thu, 23 Oct 2025 00:46:19 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json
