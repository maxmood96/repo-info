## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:ccc2eb384453e6da67e63f60b02d04063bf09db50eb1a44eed0fa986a0dff1b2
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

### `erlang:27-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:2413d1583996f3a0bf00cb13cac8f6f502d7adc310097ea6035dded154dd36b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53645076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a493a26387f2e8977e483df1a724c9b5b4b6426f22201f2c1cc194cdddd1b2e`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711f3af668dd6e98c75c75a61210dd77183715af6f0621b74c0c7066a0714ad`  
		Last Modified: Wed, 08 Oct 2025 23:48:09 GMT  
		Size: 49.8 MB (49842624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d772808ee4b1646807f16255d39ffee58110d031f64dcfb80018a3ec57c2bd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 KB (293843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fdd2296af4c30926f94f1cba9118c8b84ded1d2b4ac8f1ab06b3f030ce9ff6`

```dockerfile
```

-	Layers:
	-	`sha256:252f33a7355373d33ee0cecf6785c2774f62de46d8765f9554f5b989f34f61ae`  
		Last Modified: Thu, 09 Oct 2025 00:48:19 GMT  
		Size: 278.7 KB (278723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6848e410d9fb489c09ae97265369a8f070247feb65068269c4e94a983fed320d`  
		Last Modified: Thu, 09 Oct 2025 00:48:20 GMT  
		Size: 15.1 KB (15120 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:196e90ca397c6a6a05b8a4404d2a3fd945a57e090c2ac180122d571a90c299a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50583190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43708dd655f4c74e9f21ef455efab4024acedd35df8bd5847b57bfb99964b93c`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02ed727d3e774c74e47d32db7ecc6827eb1cea9c13d4cb3c0049d3d2600e7df`  
		Last Modified: Wed, 08 Oct 2025 23:51:56 GMT  
		Size: 47.4 MB (47361635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:90ef69b5fbae611ae8b634f6c2131cb47e0351b5cace38f54ffc67eded1f6ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 KB (289714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374040e8851e67206b872014d587b48a5dc3e008302cf6256abeb32e0d7323c2`

```dockerfile
```

-	Layers:
	-	`sha256:8b5b70713f8f8da26d3a578c89c0e4b1620bf21ed84581b45346ae36ed8937a2`  
		Last Modified: Thu, 09 Oct 2025 00:48:20 GMT  
		Size: 274.5 KB (274515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3eb51cecec14ea2d927dda76fd4c1b9f366e0c692a65108ced1348f9926f9d`  
		Last Modified: Thu, 09 Oct 2025 00:48:21 GMT  
		Size: 15.2 KB (15199 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f373353cbfccc9c4f4cc18083bb3f0a7bb89eccf932b346d7cbfe54ac6e790bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53763154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdc3a8be04d4c847fdaf731ba85f2063e854eace78eb99d22f7047c54fdf0e`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152b807d215b26fc91ce507a78f155ebb4efc37b3ee988bdd3300d856b65b05`  
		Last Modified: Wed, 08 Oct 2025 21:51:08 GMT  
		Size: 49.6 MB (49625085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ec4a1fc4e714332acbb6cbfdcdf0e33f0881868d426cba2ac9ba36bb24fe776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 KB (294739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3da5fff486ac268385916f44f615afa8d3de9aae9381ba714e55d431805696a`

```dockerfile
```

-	Layers:
	-	`sha256:28bfd2bbdeee136798461766048f654e9b8285dafde8e55b41c646b0340249a8`  
		Last Modified: Wed, 08 Oct 2025 22:47:38 GMT  
		Size: 279.5 KB (279515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d1fc827b45868a873a8b9e4cc802d0d2c867333908b02f32f1f3fcd69adeb5`  
		Last Modified: Wed, 08 Oct 2025 22:47:39 GMT  
		Size: 15.2 KB (15224 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:ba1bd7056efba7190b58800dd2b8a13be9872aadef6e0e1c57033547e9789992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51900863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584b113849e95e83323b32d9e79ddad74352f8370fc7f93989a63822db07ca0d`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78120f72c30b86eb18fd1742a765fd26f5a5f05202e313e92f26033ac376dfc6`  
		Last Modified: Wed, 08 Oct 2025 21:42:13 GMT  
		Size: 48.3 MB (48281932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:542ef758d93a37d7b803c7d5ba1070b9df7cdb7f9cafa88b554d9f222b580919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 KB (288805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5702bee2965a4a277e60071841d41f111875a5d08f5f325d265759ce09d91a7`

```dockerfile
```

-	Layers:
	-	`sha256:35ce3b6a353cb302ad7b8ff451f4af07d80c99a612af47badb8796fa8a5fd437`  
		Last Modified: Wed, 08 Oct 2025 22:47:42 GMT  
		Size: 273.7 KB (273718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86057364b8893447e9c9c8bc1325088dc3293e4aecfa9851f0ec1a194379fea`  
		Last Modified: Wed, 08 Oct 2025 22:47:43 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:3d388766f14e8ff0f8dec3eca37716ed6b97098674455add11a962d0e5baccbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54434462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62366451343d0c1230a21698122ee69fcbdfd7ef6ba2bbf2773e0b17114a26b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167522b9fe139b0194fa5a9d18b06b58fdd3fbcd376b15f87a87c6eea20d359`  
		Last Modified: Mon, 15 Sep 2025 17:22:57 GMT  
		Size: 50.7 MB (50707351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:580dd1b9a2987a00a834932160e4a68016f91a780625457acd2c6d4edd0099cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 KB (285113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de1d1a22019e42d8b2f6c432e7633b83a8492b066df44ee641227afe4b22d56`

```dockerfile
```

-	Layers:
	-	`sha256:d3aa4fb738a9a5252922476386eb3d2d73f60b27c8a6aea681b63d973bd17267`  
		Last Modified: Mon, 15 Sep 2025 19:49:07 GMT  
		Size: 269.9 KB (269949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707710e2bbebe2fd4aec810fa8f927c1705226f63d0d0f8f98053911bbb6529b`  
		Last Modified: Mon, 15 Sep 2025 19:49:08 GMT  
		Size: 15.2 KB (15164 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:63dbe80a57aeb0cecca8431a96e7b464447e42ccb1a96bb160019a28558f27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53933801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcee383638b7576d6eb573c3d5c6e96dd2968291a85ba70ae2d5da4f60b7afb`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a6c193b04e81644dff34cad9299a6e863d77f2f7a7eaaf1f7b309d0422d1d1`  
		Last Modified: Mon, 15 Sep 2025 17:17:47 GMT  
		Size: 50.3 MB (50288830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:85efc67b12831454fbc7a41c2296da2c4bb8639626f0ccda8c4ca9f93666dc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 KB (285035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0d6ffd3d4e3e64a38ef52e096f7ca545b4efa0ae3b31a233ca6134f911a77`

```dockerfile
```

-	Layers:
	-	`sha256:17f0b32058c4f91e2fe7f8edeb3e5808da5588d7f49c5fef799fad68eb9f0c98`  
		Last Modified: Mon, 15 Sep 2025 19:49:12 GMT  
		Size: 269.9 KB (269915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9c1e31bbb03f102d7897332803a0d5cfbe73a12ad8c2561569ad0dfdae86ed`  
		Last Modified: Mon, 15 Sep 2025 19:49:13 GMT  
		Size: 15.1 KB (15120 bytes)  
		MIME: application/vnd.in-toto+json
