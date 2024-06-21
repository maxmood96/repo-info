## `erlang:24-alpine`

```console
$ docker pull erlang@sha256:d5ec5079ccceacf65976690876fd39b73a3faf1e1cc551683937fa84bf44ddc3
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

### `erlang:24-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:28829a72742cf308f907b8e8f94b9d6c0b55fea8b866704e616416047507554a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49064420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec91706f624f73368e7374c928575468cb067da5fb8c81fd03f5ff336caae109`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d99d3e877eb5fa0be11d2e5f544cbb06797f0e788d3bc55b073d24c48e814`  
		Last Modified: Thu, 20 Jun 2024 21:01:46 GMT  
		Size: 45.7 MB (45674457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ca850daea1816fa284582da2dbdd08bb47dd4f56e47e25a942919f969582b81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 KB (278262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690661b3b4956a76cec3f9a262595c22fc007a22438d230d2f9af9befd97f8f3`

```dockerfile
```

-	Layers:
	-	`sha256:8b614a8bae181931d66e63e396406aa0e2ccc82c73630fb6336ea0eaf91ddb8c`  
		Last Modified: Thu, 20 Jun 2024 21:01:45 GMT  
		Size: 263.5 KB (263461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8b0141b450900e6fe288a4663e89aab79c54249472d3b9263fd6b610439018`  
		Last Modified: Thu, 20 Jun 2024 21:01:45 GMT  
		Size: 14.8 KB (14801 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:3ee3ed495dd5e39751acd654fbd01bab8531bcf6346d72bbaaf15da2c308b609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48119793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cf7b69b14e2350b663304b6042bfda2b11147d3a7613d9d111a6dfd58510e7`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:07 GMT
ADD file:248255ed09e14a0af5432820adc48fdeff8b679f7965161e9fe1c7102a55a874 in / 
# Sat, 27 Jan 2024 00:15:07 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a35f077ad6eed63841c524f727e359345dc0ddf23f8d8d826405b587110cf4b8`  
		Last Modified: Sat, 27 Jan 2024 00:15:47 GMT  
		Size: 2.9 MB (2869839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc42fb11f98e943b4ae7a78dd80ec49b45e6fd76e80d59bab2a20ee7172cdd6`  
		Last Modified: Thu, 30 May 2024 22:45:28 GMT  
		Size: 45.2 MB (45249954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1cd0adcc40975c6beabb430b4c210487e7346e4097d2f6fa25315ee03f3fcaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 KB (274986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0d3a7355fe72f600b5e6c5e7a38eafbddd9dc420caa8dcbc4406578d29df5`

```dockerfile
```

-	Layers:
	-	`sha256:6cf2b5d135faadb8d285780d0014e8c22a37f9b2d950f99bab076a3ac6624108`  
		Last Modified: Thu, 30 May 2024 22:45:26 GMT  
		Size: 260.2 KB (260164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e1e2979c372c9ea44a519cd45d225192358277a69c4df27ee912de5003c75a`  
		Last Modified: Thu, 30 May 2024 22:45:26 GMT  
		Size: 14.8 KB (14822 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:36526cdce2308c373397a2c13e9a04aa7f2d97b4562c4105e6298dac8e4920b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea2f432362bd00d28bef861c7ffc793d81741b80cabe96a60307c36a0ca5963`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c868702000001199bebf61b8785b93985891a437a2f8240850217e7d8c0e80f`  
		Last Modified: Fri, 31 May 2024 04:19:44 GMT  
		Size: 46.2 MB (46243374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:76abd31111d6e9e19f5393ff8b0eece7ae59b610230f98aee80be8eab0fbf8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 KB (275235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436b8a7a27f5ee3b49a9f6d4e4c8dfba8cb280de85f06d868792d3f1264188a1`

```dockerfile
```

-	Layers:
	-	`sha256:229aafaa6fe238ec03c57fb5155db5b1e84b8c974b5d565dd975626d8a5cf43f`  
		Last Modified: Fri, 31 May 2024 04:19:43 GMT  
		Size: 260.2 KB (260183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f243f77eb64161fd8b2acdb17a417f21dbba56ebedabb310e268737e4eca9e3d`  
		Last Modified: Fri, 31 May 2024 04:19:43 GMT  
		Size: 15.1 KB (15052 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; 386

```console
$ docker pull erlang@sha256:2ae9cbcbd01736cac168319845bab3fe80b6a502f8377f1daa1b88a6cf679af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47947179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986261ae6dcaa67479b28e09d6bf44ef9f2af5b43ef9ac6e126461d8f827f55c`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:d9d35363029b961e059f893ce316b225dff0f0cf0e83239eef5112bac34f489b in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:352e67149c757f9318808910d9c845c3d46a0040885ce37c39e0a1b6e3190acb`  
		Last Modified: Thu, 20 Jun 2024 17:39:24 GMT  
		Size: 3.4 MB (3424306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a305323b44bc4ec235c210f84ece05b39da3c8262874ba95c2feeed27f856a66`  
		Last Modified: Thu, 20 Jun 2024 18:59:59 GMT  
		Size: 44.5 MB (44522873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:6b4f74cc8631378e88479a212b779090c12c48e790a312c65cb6e5763920d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 KB (273934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162b8f34f426ba67b2e0e3ad4369e2fd5aba0b2f481fac11e7eb01f49dff79d0`

```dockerfile
```

-	Layers:
	-	`sha256:0c0318ded9d963cb3d24e371630b2bea50e030585644e389ffcae06f020ff32b`  
		Last Modified: Thu, 20 Jun 2024 18:59:57 GMT  
		Size: 259.2 KB (259162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75c0f3132bcc9beffa53d75048e79529010f0b0161503b97270a37adfc33251`  
		Last Modified: Thu, 20 Jun 2024 18:59:57 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:2b8d3744ee58629d19a5e1c864f3f041c12b950a2bb8f7b940e94dc6b8ecb44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47970035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078d4dc2e771e11a366279543a46f46fd5a31583791277d2784ebddce3a80a5`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ac2165d1efbc6e79a37ea6bc80c5c24bae8dd6955a03fbeae88fa1dfa2080a`  
		Last Modified: Fri, 21 Jun 2024 01:46:43 GMT  
		Size: 44.6 MB (44568226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b3606c1e852d477d35bae9294e1cbdcb4945ef47814fdecbab25a879980996ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 KB (273101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efaf95b68990022b0510a48cc744366d262dbb1ed3823de483604f07ebacfe4`

```dockerfile
```

-	Layers:
	-	`sha256:6f23292bbecb96f842202f4baaeb53ec8fb47baf04f5480b64cf82caab82f8da`  
		Last Modified: Fri, 21 Jun 2024 01:46:41 GMT  
		Size: 258.3 KB (258262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b182bcaf02558c2e97fc11e7d6c534f95b8815a28eb1d7c7fedbb3d191e72aa`  
		Last Modified: Fri, 21 Jun 2024 01:46:41 GMT  
		Size: 14.8 KB (14839 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:f2b24125bb8e4edc2fe1a7110f430b2f5f07c8d369d9ac05ce54e0c1bd827923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48837541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70a4c528677f1a0a27d30b3cd368b2e2cf203ff9c69dc24f94ac06443293581`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 27 Jan 2024 00:40:40 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Sat, 27 Jan 2024 00:40:40 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4af0ceb0d0d4df310458e717c5e6df795fe5e8876f309038ce25b84d80c069e`  
		Last Modified: Thu, 30 May 2024 23:17:20 GMT  
		Size: 45.7 MB (45661011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0f5c128daeb4b3a0dbb86cbfe25cef6e31c6d56dcaf81713ea7c84950c0c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 KB (272925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577fea634e935ba4f8b8cc1df9d4ecd819c3ab93dfacce9b015ed4d4ca402a1c`

```dockerfile
```

-	Layers:
	-	`sha256:c809e2cb85481254ed3d76287286e62e9183993a9d686faf1ee66156a5e5d171`  
		Last Modified: Thu, 30 May 2024 23:17:18 GMT  
		Size: 258.2 KB (258174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d8aea0ff0e1ff772ff4a25d7dc40c593f2c25535be0d5edb7424929e5fa407`  
		Last Modified: Thu, 30 May 2024 23:17:18 GMT  
		Size: 14.8 KB (14751 bytes)  
		MIME: application/vnd.in-toto+json
