## `erlang:23-alpine`

```console
$ docker pull erlang@sha256:0f7bf0b5b8faedff36ee124b54a84058e5aada4cfc88794dc3a49bcab91f982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `erlang:23-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:bc3d762e33c0f7f8e84529dae03519b6ec062c9e43f00eccb78cccb7e51416b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45530793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9ec80aec9283e0f4c06df684e24f4311d92b53f118b05dc97d51e8e238f884`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:30:39 GMT
ENV OTP_VERSION=23.3.4.19 REBAR3_VERSION=3.20.0
# Fri, 01 Dec 2023 03:30:39 GMT
LABEL org.opencontainers.image.version=23.3.4.19
# Fri, 01 Dec 2023 03:35:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b3b5ad2942c7f643cdf7e5b7af57f007e404f44caaa0a8ab288f4c3de23552f" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Fri, 01 Dec 2023 03:35:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be7dd9ce30ef32fa18fada5462c7d7d2fa1cc9f36fa25aea7bff924804baa16`  
		Last Modified: Fri, 01 Dec 2023 03:44:00 GMT  
		Size: 42.7 MB (42723011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:cd7b337bbeefa53b3886b7fd06807c557153689acda7215f70380d8ab6d09379
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f25dad7d4cd9bd150b742de068f06f0e58b00711c28547c9a276dc3ec5c15`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:33 GMT
ADD file:911497ffc967e53c16d8356f320bf61fe06b85fc3250b7c01183f7bcfbfef404 in / 
# Mon, 07 Aug 2023 19:57:33 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:32:32 GMT
ENV OTP_VERSION=23.3.4.19 REBAR3_VERSION=3.20.0
# Sat, 21 Oct 2023 00:32:32 GMT
LABEL org.opencontainers.image.version=23.3.4.19
# Sat, 21 Oct 2023 00:36:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b3b5ad2942c7f643cdf7e5b7af57f007e404f44caaa0a8ab288f4c3de23552f" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Sat, 21 Oct 2023 00:36:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d27c9f7e5791cecbf0251c0e7638ad6fbd2b510f038f66cc06c933da98c75979`  
		Last Modified: Mon, 07 Aug 2023 19:58:18 GMT  
		Size: 2.4 MB (2419274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9d413c96658c3e2aad9e1b87a52847ed9ce9a26499903f6b758c728c32b76f`  
		Last Modified: Sat, 21 Oct 2023 00:43:25 GMT  
		Size: 42.8 MB (42841179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:a92658a46ea7ab57986a552faf56687cae19e7f7b27b8bdc8004e0a9f9c18e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45120486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de818e8e05e734b978eeb8fde3fd84703acb41975e279ea5c07a7858168cd91b`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:11:14 GMT
ENV OTP_VERSION=23.3.4.19 REBAR3_VERSION=3.20.0
# Fri, 01 Dec 2023 07:11:14 GMT
LABEL org.opencontainers.image.version=23.3.4.19
# Fri, 01 Dec 2023 07:14:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b3b5ad2942c7f643cdf7e5b7af57f007e404f44caaa0a8ab288f4c3de23552f" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Fri, 01 Dec 2023 07:14:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862fc438153db04eefdb597a844f710e700c673e10d1528867bf10f4e46e5518`  
		Last Modified: Fri, 01 Dec 2023 07:20:16 GMT  
		Size: 42.4 MB (42412193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-alpine` - linux; 386

```console
$ docker pull erlang@sha256:93ac2c2edfbfc9fe9c89927396c55767d864b2a4daa1bc9f74b012412d7bfa06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46975190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c17d7857732731b41938bbabb099aa6177f255396fe4d08c0dae30b60af304`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:34 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 07 Aug 2023 19:38:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:35:08 GMT
ENV OTP_VERSION=23.3.4.19 REBAR3_VERSION=3.20.0
# Sat, 21 Oct 2023 00:35:08 GMT
LABEL org.opencontainers.image.version=23.3.4.19
# Sat, 21 Oct 2023 00:43:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b3b5ad2942c7f643cdf7e5b7af57f007e404f44caaa0a8ab288f4c3de23552f" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps
# Sat, 21 Oct 2023 00:43:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457478f891b06861e76c5ed97f449b95189c42fcf395f9322f1e0ad6af5ce6f`  
		Last Modified: Sat, 21 Oct 2023 00:59:55 GMT  
		Size: 44.2 MB (44164637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
