## `erlang:29-alpine`

```console
$ docker pull erlang@sha256:65713bb2f1785163a9dba8301200abff1587bad53a3577fe2c745a1984d5c3cc
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
$ docker pull erlang@sha256:244146dc5d7d945ae72c905b3053201be34d644fb1a416262883b43280e54a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56613971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38198f1b05479e0d3b7b09967c5414ed9a094dc05af1ae9394f8d0a6c665ccef`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:52:40 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:52:40 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:52:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:52:40 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf76b7538f0470c4bbc5811456491a1faeda696d405f998542200eda6117201`  
		Last Modified: Mon, 20 Apr 2026 21:52:48 GMT  
		Size: 52.7 MB (52749782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:dc5456a436e3b6eb9dfd9173a162f49435929039e59da6f22643f25786cca7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 KB (282461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c3700dee12d2ea58d3e4ec70e19292595186f0bd1b1a0cdfc7f2581cae9ed7`

```dockerfile
```

-	Layers:
	-	`sha256:db2ef406bfc4dd7082ffd52604939f1e9a088f182a7cb5299dad5adff1553faf`  
		Last Modified: Mon, 20 Apr 2026 21:52:46 GMT  
		Size: 266.8 KB (266833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe56a07234705fb7678802dc9d0b93b26459dcf9b45a0af121e908368c608a91`  
		Last Modified: Mon, 20 Apr 2026 21:52:46 GMT  
		Size: 15.6 KB (15628 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b3b92460242cd796559962ee6dae4d8ffe97e70f33433b2d0ace6cf9d0d575d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53587953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e73dfed48da84b698d568189cb04514642a853953d5a78a507812917d7d33`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:51:30 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:51:30 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:51:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:51:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e02683645ab35b1ea94db2926275d30f9d65507f23c9080cd0fbc27b69590`  
		Last Modified: Mon, 20 Apr 2026 21:51:40 GMT  
		Size: 50.3 MB (50304830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:90f9a333777af0dfa9c03649bb072346ec444207318e9a6188eb2232e0059c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 KB (280670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bde8e950113c1edf04210bdac2f3c0aac349eaeb441274e1d8e0761cde7a92f`

```dockerfile
```

-	Layers:
	-	`sha256:6106fb2dd1ea2a4e7baef85fb870a2f8cab53865e14f9aab371ec16dbf5fc4a5`  
		Last Modified: Mon, 20 Apr 2026 21:51:38 GMT  
		Size: 265.0 KB (264961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbae4df4552d9704b1b0347da65eee1c5629ca836272ee31557ef93c96d7c341`  
		Last Modified: Mon, 20 Apr 2026 21:51:38 GMT  
		Size: 15.7 KB (15709 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:38e9dda5a4756d37f9fcd04de36b1b57033a4cab5db0d5f8cbbab2f5d12c36b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56728168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fc855112107ec5a302b95a587a996946f49445f52f04c4976e38ced99cb54f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:53:17 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:53:17 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:53:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:53:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9427066c4025797f15ac493f76390edbe105cad8d790e7584272a038157af5`  
		Last Modified: Mon, 20 Apr 2026 21:53:27 GMT  
		Size: 52.5 MB (52528298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a24cd3067239516b86e8c4bf626538a3b0f70bbb0ec1485e98e16eb926515a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 KB (282705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b57c7655be3cc98067df873ca60cd43f4f5a20014f56b0b6b9fe559e329c04e`

```dockerfile
```

-	Layers:
	-	`sha256:28d08e76d315ae474978fffa6a10c6749df45561e9fefc3a962096442fbb2307`  
		Last Modified: Mon, 20 Apr 2026 21:53:25 GMT  
		Size: 267.0 KB (266971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564d870deadd40a8e650b3f9ce680a5085b54e4a2997aac9148e22f518fa67f4`  
		Last Modified: Mon, 20 Apr 2026 21:53:25 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; 386

```console
$ docker pull erlang@sha256:c2156891f3dad4667b64953be8fe9bf2fb1fc50183aa193b47c1b3046e8a335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54837009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f58f6481c3499a9d301d075e613655693761ba94139bd54f90fbea31906f41a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:53:27 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:53:27 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:53:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:53:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe18d63010adda489ce87d80e8c178982de64699b6468bde33da15d5e5329e`  
		Last Modified: Mon, 20 Apr 2026 21:53:36 GMT  
		Size: 51.1 MB (51146563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1550acac7ddf9a40c2e911c7e47def68d54ec2bdcca2ea781159043980571588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 KB (277426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eab8f34e44952963d2f3b1093b089e4128b3a55b6ddc6487c9ae6d5f6bda4b`

```dockerfile
```

-	Layers:
	-	`sha256:103c6f535255e4e57f72d9a9944a06b44a4ef09369aa0f963ad0c7c61dd734f4`  
		Last Modified: Mon, 20 Apr 2026 21:53:34 GMT  
		Size: 261.8 KB (261828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d315da247935e9d1680c35754cb02cc43903bf96de7822caa32e4747f51d09`  
		Last Modified: Mon, 20 Apr 2026 21:53:34 GMT  
		Size: 15.6 KB (15598 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:f94e4b6ad9d76ff6e9f7893b274f366318793a5bdbb823b053f2f39e371623f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55230306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9e00a6b1649533ff7dd6f144c44d4ef9535c9efe93f9f26b7bc53f089420ce`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:54:54 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:54:54 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:54:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:54:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e41c91a95d72d7e339766f1d15ffc5909c5135f8b24d7c209bce3995c2901cc`  
		Last Modified: Mon, 20 Apr 2026 21:55:12 GMT  
		Size: 51.4 MB (51399377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:58506dab267d70f0000ee2d0006ce04c08b2ddec1c577a430feb2c1100e450d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 KB (277642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9719de7e2e130325e394919e17bdc023b57318e666f559bbf7c72d37fb917cae`

```dockerfile
```

-	Layers:
	-	`sha256:c858bde84a00d3d84839196085971042a2e8b079293187412514ebb558068d86`  
		Last Modified: Mon, 20 Apr 2026 21:55:10 GMT  
		Size: 262.0 KB (261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed8e496e895c128e769150f8b3494930e6b8432bee7cb0cb999d9462a8e3ed`  
		Last Modified: Mon, 20 Apr 2026 21:55:10 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:0796a216ecf9fc8c25c73cdf06707310d0ba202014f1826cebf9f075631d3589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54757945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2f3f00191e6646e7e96a6890d3f269c70a3a1299a4e8908bba593415f204ea`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 21:54:57 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Mon, 20 Apr 2026 21:54:57 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Mon, 20 Apr 2026 21:54:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 20 Apr 2026 21:54:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c3345ef45718304265e20b149dbecb9abfb5ebca6237ce5bf5a40d21bdabe`  
		Last Modified: Mon, 20 Apr 2026 21:56:37 GMT  
		Size: 51.0 MB (51031413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:5f53cb009558c36ab330e67d657e01d6c136eef761843c31be7b4beb5d953541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 KB (277564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c084b5bfdb03a69f1999e0d7b0a01d1bfe76dc72a02bdbad5999f57b5503e39`

```dockerfile
```

-	Layers:
	-	`sha256:81dbfa2324367a582bde1519311a66c670f1e914ced014bd84cfeb95c42d5ade`  
		Last Modified: Mon, 20 Apr 2026 21:56:26 GMT  
		Size: 261.9 KB (261934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddd3068f507019089bffbc9098784eaed8e69664768f914f711c37ff1d15c00`  
		Last Modified: Mon, 20 Apr 2026 21:56:26 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json
