## `erlang:24-alpine`

```console
$ docker pull erlang@sha256:5644f915aeb98d1178316ff8873a1af19465e70d5f93e5aa00f09d2de770af2e
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
$ docker pull erlang@sha256:9b69e93d13a5dc54a4e69e0235e7f99f22a292ef1b6f33006f25b95b906d5caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46527033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875db11d1ef2057ccae9e3f79780ee7754781385ad1a1ebb65102b8745c95a2`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:e1af9600d47671f6988c75963ea4e527da5f33f7a6a3a414655eb00c0a1e80b1 in / 
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
	-	`sha256:f243ab88c906a988e795cded32817ff327830c2fa9e2a819e8e436928b399bd0`  
		Last Modified: Thu, 20 Jun 2024 18:01:24 GMT  
		Size: 2.9 MB (2878836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9b3d188f987162a2193f5c3677c75b96e0bd46ee026c032769e43d4d502800`  
		Last Modified: Fri, 21 Jun 2024 03:28:45 GMT  
		Size: 43.6 MB (43648197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3a0d1ce06c666d5f2f932a792b717cd57a91794fc14c72fb424fabba290b4b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 KB (275089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e56270c2b115519d00759962b3e0d9c9cabacf4d4e72f271a6c426ab7dcb4f`

```dockerfile
```

-	Layers:
	-	`sha256:baf146440530e84c3f8c5da72f0556a82d40d4f6dadc1972655e159cdcdf81d9`  
		Last Modified: Fri, 21 Jun 2024 03:28:44 GMT  
		Size: 260.2 KB (260218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc88cb8ac34126c266212836ca7f10bb1ad0941419dcb6927e245cc7c5779b5`  
		Last Modified: Fri, 21 Jun 2024 03:28:44 GMT  
		Size: 14.9 KB (14871 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:2b8c8b8d87c3967dd24d04dff8dd3e69e67f0b183a918b8cbc9c8b3fd83c15eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47610648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab411d35f9d367169da6c288133941df803dec8c496d42068cbf309ffcc2b76`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f92ccda31ee7bbd4730b43204f9a2260fefaeb652f731f1fe6c0fd61f506221`  
		Last Modified: Fri, 21 Jun 2024 05:03:06 GMT  
		Size: 44.3 MB (44338062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:c23b235633df8cb90d18f8d8b2cb1d59e83b3cadf0897cde9f0a5290045cbef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 KB (275339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e02ea321a1b06082bbe7d606f7d4fc8ddb672d030fc611d66cf116a4676765`

```dockerfile
```

-	Layers:
	-	`sha256:e678a582654bf30eb104c9b693986b95dac3f066f67de386ce1fb7cc7b97d0c9`  
		Last Modified: Fri, 21 Jun 2024 05:03:05 GMT  
		Size: 260.2 KB (260238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b182ff10301de7ef4d9f0ce7add0d556d21dac69dafd3cf9fa5b942f9cfc02`  
		Last Modified: Fri, 21 Jun 2024 05:03:04 GMT  
		Size: 15.1 KB (15101 bytes)  
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
$ docker pull erlang@sha256:d62565f23f3c5f5606e8f309c0c55308181c05bf75b2e40610af0356e7ec91ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47051161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac3921ee7ff66dd4c913627bcc95c0b309118052d410d154d266686ff25b23`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:a9c4d6f5823b30643d4636be2b440b50deb92a2d19765e0428420a1309bfb0d1 in / 
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
	-	`sha256:bc4c034c86cf8d5ea77b49537505f7600ac0422e88fc3d77b3ba3b3f0c9dc564`  
		Last Modified: Thu, 20 Jun 2024 17:43:33 GMT  
		Size: 3.2 MB (3183597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198aceaf3d49ed3be18ffad86310cc21a51f341616491197d8090db449d4d18d`  
		Last Modified: Fri, 21 Jun 2024 04:03:53 GMT  
		Size: 43.9 MB (43867564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0a05a7621fdef73f544da15088b6701fcbf06e8abf9635b51b33f538f7ff1822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.0 KB (273029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0710adeea8cb90f1e8cf1a578be15dc1818eab773bf5f82253a0cebc4788ddfa`

```dockerfile
```

-	Layers:
	-	`sha256:2b48a05408aff9582ed8fe55ab4e9717682baba3bbd8faa2892c25554d9e5d91`  
		Last Modified: Fri, 21 Jun 2024 04:03:52 GMT  
		Size: 258.2 KB (258228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270703502c6c4c85184c160ace065feb06fabf59237063bcd16759e988cf623a`  
		Last Modified: Fri, 21 Jun 2024 04:03:52 GMT  
		Size: 14.8 KB (14801 bytes)  
		MIME: application/vnd.in-toto+json
