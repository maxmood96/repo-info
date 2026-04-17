## `erlang:26-alpine`

```console
$ docker pull erlang@sha256:0a898a08bab9111bab8cfee7dbbb4fb3861466ac1d7b2e6b524955b574b280d5
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

### `erlang:26-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:0445c74088d4e42071bb77c1998e46a1eb14c1eb64f6f62940000fbb70a3f766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49735348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a0d226b690076393fb9e6aafac004101637263d6b45f4deb5056331ca2444e`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:95c9a6580d556c3452eeef1ca7efc572c25b922f4a120ca2c1ad0219fb333d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 KB (287704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cff2e9b21ccea4b7a39e9a31e0ca37d18c90e4332a85d822390f5b2da86ab`

```dockerfile
```

-	Layers:
	-	`sha256:b2e5bc51b88b649fe66047d26cecfad446025aaf6b824aa58c0ffef3926e2a60`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 272.7 KB (272702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583f8796780a1054e0d67ae5ca48d921ff199ffb06d825d982f116594cb4455f`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 15.0 KB (15002 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:085546b9ca1a223318c50b2c9b26cfeac2bf340a3940da3ba7e12b3852f7d401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46870155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d036c1e4b227502d6869939eac6427962be168dd7fa6f4f774f06030e6f0ecc`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1342d9cab0213c705415be0abcb887c7b198f7ab8c2336332ea7dca70d55167f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 KB (283506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e4988aa73576e6037c5def4b518021e2343a2083d8abb1df9304db1d38c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:4fc0b97c67e820f80d381a8aa50921fa579f48eca0d54772285a1aa09a4d3be8`  
		Last Modified: Fri, 17 Apr 2026 00:32:32 GMT  
		Size: 268.4 KB (268423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4071eacd95cfb904b36893e1341748dbad82a963e8f4a32ebf9cd8de8e117f`  
		Last Modified: Fri, 17 Apr 2026 00:32:32 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:149267b59af385c05ff208d82b606b4fcf84945f99a63e2d118da56b15b44d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49993375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569064c22215d8c91603d93804f982ff3f924586fc22d28fe7b9b6e71e3f66b3`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1c49e0721a732446d11bd6dd9e8db061765d79b4e074455d63526d669f7691f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 KB (288602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0602bfcb6bb9f67459167635b36bb32403bd7e7fc08c6582343570eef026ba4`

```dockerfile
```

-	Layers:
	-	`sha256:d2b074522286a36822afc86abbf5eb5f5b0fcd6152bc5a6e352bd61f3adce5e8`  
		Last Modified: Fri, 17 Apr 2026 00:29:56 GMT  
		Size: 273.5 KB (273495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25aa455feed39304cc6a06ccb20466d24a4f69d27ad2cf219def9f1a3db2eaa`  
		Last Modified: Fri, 17 Apr 2026 00:29:55 GMT  
		Size: 15.1 KB (15107 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; 386

```console
$ docker pull erlang@sha256:07f374246e843c70656af850384be194807cdd56432deefbcb79d880a872579c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48180385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b5dbfdc0d7066cd87ff1f02519561a4bfbdcc7587bcbfac5f890eef3f496c8`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:41 GMT
ADD alpine-minirootfs-3.20.10-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:41 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:59:43 GMT
ENV OTP_VERSION=26.2.5.19 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 05:59:43 GMT
LABEL org.opencontainers.image.version=26.2.5.19
# Fri, 17 Apr 2026 05:59:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7fda9da782f34a9e3a7223dfc1c7b76702f40f91561efbefc4391b6b529dcf3a" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 05:59:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c3891655fe7f935c0edb9d8699a7880f85be6681344aea8dbae92ace3f127c30`  
		Last Modified: Fri, 17 Apr 2026 02:42:45 GMT  
		Size: 3.5 MB (3474644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f729d10e0421d7701c9facd8a0e5515222ef9a5cab916e79d6b18f9d96f047c`  
		Last Modified: Fri, 17 Apr 2026 05:59:51 GMT  
		Size: 44.7 MB (44705741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:6e9e6a0ff2dc3eed0d10bf45c55e1d077e648708559b3fc035d7c5ed47e3404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 KB (282596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca2d639997e790f40440291096c3df4e7658a70ad21933a0a7c1ca34f7f345b`

```dockerfile
```

-	Layers:
	-	`sha256:1993f972d7e62ea094eb9526da01a634c5e13de61058a4b0c8231ca8e9ff84cc`  
		Last Modified: Fri, 17 Apr 2026 05:59:50 GMT  
		Size: 267.6 KB (267625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccedc39d051d6ca8034ac1c039ad52e133ef3f81c5e52f9d67aad644094a9222`  
		Last Modified: Fri, 17 Apr 2026 05:59:50 GMT  
		Size: 15.0 KB (14971 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:acfa9c9660ec8d77e30577d34f90b9a486b444108088436417d186002b3f927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e4a8a988c1aa0f23d105c1b8f8209aa623bf099998dd51032a8d0115a3edf`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1f2abd5407eca75ba0a0525d8104e09cab028f8867631e3479b194637cee986f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9151568012124094523aa5f63e2d4982db6f4e92b4933a575dd92c251aa5d1`

```dockerfile
```

-	Layers:
	-	`sha256:ddfd4ec3a4a4e69eb644e6eef90aa1e474c5ba49b7b99b31df411d3ee3921a95`  
		Last Modified: Fri, 17 Apr 2026 01:21:09 GMT  
		Size: 266.5 KB (266470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5105facd834ef1aa0b14c0f3fe771c5f40579849a805c1e54fb61c9e47fb73b`  
		Last Modified: Fri, 17 Apr 2026 01:21:08 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:64c11db65a8bc55afcb7f5ed56feb1ef56ba9a58633ee2a180d18c06a06822a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47885587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae467f7b01d30e0cc00cc5f5d74d19f393e054a158f23f313d5091e0b68a6aea`
-	Default Command: `["erl"]`

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

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a5d8c947cf289de8666e58df4ced21a51efde265755ce26d4129655fda8af7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc259b5f404a31b914f00e2ca47fa855cb55af1d41a1338f0bfb400db07b273`

```dockerfile
```

-	Layers:
	-	`sha256:67c5fa2487a41b92cc206f16126263d894f72552b13e3c4579b5e4b509357d6c`  
		Last Modified: Fri, 17 Apr 2026 00:48:35 GMT  
		Size: 266.4 KB (266436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583d52b1fcdfe54c96c56e2f550acb4359013c2a52435335cb49f90c9f3def57`  
		Last Modified: Fri, 17 Apr 2026 00:48:35 GMT  
		Size: 15.0 KB (15002 bytes)  
		MIME: application/vnd.in-toto+json
