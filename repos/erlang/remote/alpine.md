## `erlang:alpine`

```console
$ docker pull erlang@sha256:c12b2a7532def96e4af41f5443ee2c832dd6f2739a316e198235f209417d7a00
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
$ docker pull erlang@sha256:2896b44eb62d5fbebca865d5c7e525df88d4dc993d1b7a33a482429e476def5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52528193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef480f055ca73e5200b813b1a7f8f1e560be52aff23f0ea1527825e39a2d3a49`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c9f928087f9557b193f7a4b6b037da61268b2dc585daa99056440f0f32328`  
		Last Modified: Tue, 13 Aug 2024 20:10:09 GMT  
		Size: 49.1 MB (49109153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:5c40bb767c33bf76a54db5c1096835933a2cf471210ab1e7fc4b429bfd292c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 KB (286237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e550a9ff225a64902f5b6cef3cd2a7f077aa23e9b16a2009ffd7bc1654a139c`

```dockerfile
```

-	Layers:
	-	`sha256:11a2dd5c3db172a304d285d150ee248c3cb5377274367f74656209575de95d81`  
		Last Modified: Tue, 13 Aug 2024 20:10:08 GMT  
		Size: 271.1 KB (271147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7cdf15c5feb0afae7ec098468e46bd955261e044b8d381d2cbe4d925e617346`  
		Last Modified: Tue, 13 Aug 2024 20:10:08 GMT  
		Size: 15.1 KB (15090 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:09188f237793b164da2b243b4a8af847f3d0e58a9fed7a8da7562ebb5adc7094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49813465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b603e50b48ba6fd0746ff941aab8cee22d286ff00196d03334075c438b1fda04`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc6c58997a7fc64161373d339d092f8cdba403be674556d5bdec4f70c0a0e1`  
		Last Modified: Tue, 23 Jul 2024 12:53:50 GMT  
		Size: 46.9 MB (46886360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:175a9032fb1a750441d04c4fc127a14e481801368f14861142e384d9deec827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdadcaa6d89c74552ca8339ec31b8f29e98d3a0584acaf8315ab9290426c1a6`

```dockerfile
```

-	Layers:
	-	`sha256:d448f6e03b8853880bedbc18a55c5badcf4c0db66291b2a07e7ed13271593ce6`  
		Last Modified: Tue, 23 Jul 2024 12:53:48 GMT  
		Size: 266.5 KB (266459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f7fe14c57944e2c56ded98f29f9150d881b14f80fb4ad73ccc8f638debf4cc`  
		Last Modified: Tue, 23 Jul 2024 12:53:48 GMT  
		Size: 15.2 KB (15166 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:60428ba860b6c0d1722b6595ac7cf6d1955fc43ba939821ed98c67b1e624b211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52253391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3233e5ad4c75b84a7a65eb01419e9d18a056fc8110c5b86a16eb56a401d06`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0021672c73a207d42392e7706a9128748e3b662aa11a17559f20a43f4a961fdc`  
		Last Modified: Tue, 13 Aug 2024 21:04:52 GMT  
		Size: 48.9 MB (48894933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0e16535887737bd8dd4a79876aa6d2c1be92d7c94db94b11790fe65c6eb2bbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 KB (287246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bfb54d3ef47a8493f0d298a175e453a2e5ee3b0e9cab793244f9e81f30ab43`

```dockerfile
```

-	Layers:
	-	`sha256:bbfd0b86858a9836fc990306ea2da8493c6dd27d9a8f895093cd6fdd45e2b0f7`  
		Last Modified: Tue, 13 Aug 2024 21:04:50 GMT  
		Size: 271.8 KB (271844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde7810e2b19e7b34f737cf6744dc02ae6d6af78cf7d64ea731633578bfa31ad`  
		Last Modified: Tue, 13 Aug 2024 21:04:50 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:df2df42d3da72097d9304548dba5ebd63105b3ba822d2a21a5e25d42b3da25fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50958557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b560b4f7f45e9ce458d696f01fe7c4c6b5becc78dcb96149a3968d0bdf3a93e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e71df2af8936b9605ba0967a816231c2377573346c739018e15635df7c9c25`  
		Last Modified: Tue, 13 Aug 2024 20:10:54 GMT  
		Size: 47.7 MB (47705955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8d6b2ed3d7ea9aa106b38e1a7aa0bf9b6f5a9366027b4437e6c96c612badbac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1fe2018b519fabae8dcf29c2aabedffc229ed01098a5b0de450ca2b6ded6eb`

```dockerfile
```

-	Layers:
	-	`sha256:accd43b46099b168ee7df57ce3981d7af719cf33a6510c919c6c073da1625da9`  
		Last Modified: Tue, 13 Aug 2024 20:10:53 GMT  
		Size: 266.4 KB (266414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3006561400044772e11dd80ffc04eb6a36a340c81e7ac5f4d5a07514835611`  
		Last Modified: Tue, 13 Aug 2024 20:10:53 GMT  
		Size: 15.1 KB (15056 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:8d0233c20c466e9d71d689a3e2d6fac4439847ebe4a5a07082d30a15fdd5d874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51083913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b22a7eef015cd7c5b6fe54f52276c4b9a7ce258f4efd70a5dad904a65fcd04`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cac44214da6827bc6aa0330108c8e23234f82121788482192930a79c00c1a1`  
		Last Modified: Tue, 13 Aug 2024 23:28:03 GMT  
		Size: 47.7 MB (47720807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:015d9c29f40dbe19916ea891b84dbbbf2ac231b32254fc5ae959b85893666328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 KB (280293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6235cc5eb55e1f460f15f38eade74b2f0f644b6910620c45f52e8530d832f976`

```dockerfile
```

-	Layers:
	-	`sha256:3c4f0934cd9cd85723f292af8bbc58a25e4407e8b1f1275481ca3b7dc566ecd0`  
		Last Modified: Tue, 13 Aug 2024 23:28:01 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada981911daeb6b143e2f9c488fff65ec7aaa831ee74e3fe91452fb7217f62eb`  
		Last Modified: Tue, 13 Aug 2024 23:28:00 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; s390x

```console
$ docker pull erlang@sha256:f2702b86c8ee85e5fdfb2be1f31cb6402ace07f36b27b7eb541010ef135f63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50672659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20873c7d14cc0b251ada639fcc67b7d5b5ce0bcd41632ccbc2bcb1ee3eb81720`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce824ac25eb0c78af6b9bcc7a1487e236ce9af8f90c90a93ce61404fda1b92b6`  
		Last Modified: Tue, 13 Aug 2024 22:21:30 GMT  
		Size: 47.4 MB (47419583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a120bddee6e35f5a3cc7e178fd4690db57752e9cce72266fe1a19b74aff9fc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928da1af3c101206a91fa3ae9fd1908bce483c3a0344a7b8f2b90bd4ca17fe75`

```dockerfile
```

-	Layers:
	-	`sha256:963f1581fe541ca924178b1a11b565213d3f58f859f95cbb96a826a2b285b0bf`  
		Last Modified: Tue, 13 Aug 2024 22:21:28 GMT  
		Size: 265.1 KB (265119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a92b475a1d9189037158614c9ccbfc19296837df548735f9f82948f317834f`  
		Last Modified: Tue, 13 Aug 2024 22:21:28 GMT  
		Size: 15.1 KB (15090 bytes)  
		MIME: application/vnd.in-toto+json
