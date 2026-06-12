## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:7e159af11e6dd2830724a1d3cb7069083cbaf951c14f60683c2885fef15e03e1
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
$ docker pull erlang@sha256:55d9dbe6c2a8057d3ec2a438801115e70b502744dee08162eee0bb70661740ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56154339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d056bcab6027b5e8ee82dce9e3b42ecf23af60ce0e2b9b4599a4ceb1cbff8f`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:12:57 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:12:57 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 19:12:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:12:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da45bf5c57b9a622dbd389b0d835b8e60f348486df81effe799b0482ae2663f`  
		Last Modified: Thu, 11 Jun 2026 19:13:06 GMT  
		Size: 52.3 MB (52346150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:c793b88ff0b03fcbf5125b2ba544469e1f3468191c93dc0ae9febf694cc9d8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 KB (293174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fbb1ff555b571445f804378e804bc311d8e22bd04414c48c55f7571bcf54c9`

```dockerfile
```

-	Layers:
	-	`sha256:d7a1593a30e4843d3d7e7479f457af4152c4c86a9f78d2f819eddcf945168cd6`  
		Last Modified: Thu, 11 Jun 2026 19:13:04 GMT  
		Size: 278.1 KB (278094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7ef862b349e2f391360a1e35bb33d76d6453f9b21b014844e6f1d339556f88`  
		Last Modified: Thu, 11 Jun 2026 19:13:04 GMT  
		Size: 15.1 KB (15080 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1a1086faed1190eba1b96d9a3aed59f72efc8ead0bc8d03f6d6c81542f70705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5519e9bca345fd56d894d73341b23200bc7db789e08e9ef59ad35fcd2728818`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:17:31 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:17:31 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 19:17:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:17:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823167b7e16abdb78ba823bb03606f8ebb3e6f4bc27d4f2e713ee0323ac9aeed`  
		Last Modified: Thu, 11 Jun 2026 19:17:40 GMT  
		Size: 49.3 MB (49335491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:53422fbeb8f0bb3fe59353568bac5d35e858c25e94f4a13be997b220567eec83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0d65d1b45fe671b9d891193e88bf8b971a3061bc49da0998e0d644dd21c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:aeb387422796ed6104bb716422aa8caef5663bb24d957cca212f7b920cd6b3cf`  
		Last Modified: Thu, 11 Jun 2026 19:17:39 GMT  
		Size: 273.9 KB (273886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f129a011231bcd3bbbde677607a1a6d48c1f13f04be9ab0c68cc4732c7286a`  
		Last Modified: Thu, 11 Jun 2026 19:17:38 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:50bdf6a5c641e9e36e50b193f082418493e44d083574ac073bac05724312399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56581678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee25fb6158a9d6e6dece4aec138e66f748b4ace7f4e355e812bcb592cc40b4f8`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:13:27 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:13:27 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 19:13:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:13:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4415dcd538b7a8f2f97413385c32ba578fcb0ae3e541801b9d658bfb2bba64`  
		Last Modified: Thu, 11 Jun 2026 19:13:37 GMT  
		Size: 52.4 MB (52439784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:dae2938fae4f4d458a8637293def9b2dc0e2805fe6926d8f5c4f743a7c188480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 KB (294070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d8c1866d354fd1f350087a87b8a79ae4d5d839db15229d166ceb61ff9f57b`

```dockerfile
```

-	Layers:
	-	`sha256:f54cd4ba80c8489e633e6244f93caf1e91a75fcb383b5fc12c630dfa2cc64687`  
		Last Modified: Thu, 11 Jun 2026 19:13:35 GMT  
		Size: 278.9 KB (278886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8659d2d31cd166fa857460cd8897f22d1976c90cf9356a4666315cdf444e6943`  
		Last Modified: Thu, 11 Jun 2026 19:13:35 GMT  
		Size: 15.2 KB (15184 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:0c7b310ecb91f22a3e349d2d9148af1ba3cb8dae35c8305e64274de6e8215cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54235996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb30c81ad0ff012a4634f2a9410012d3279e17d3fdafad132111bfbc1e38c84`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:13:35 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:13:35 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 19:13:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:13:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb40ad0828836800beb341b142c9ee4c3ab4f5cfee49b46472e5d8d91efa85`  
		Last Modified: Thu, 11 Jun 2026 19:13:44 GMT  
		Size: 50.6 MB (50611275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7042b8b4ee9711f2724360992dbbd07c3b34e128f3c708e6bc441ae57c749317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7bb3d5a57b2e2ba586277247de0a727db5d86b21bfbd53a38e91af6c88eac8`

```dockerfile
```

-	Layers:
	-	`sha256:27b4d09c1229c7d3134c133b3e4a80299647e8d8bfb9f29ad4becb8d2f415462`  
		Last Modified: Thu, 11 Jun 2026 19:13:42 GMT  
		Size: 273.1 KB (273089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06657bf1921c314b4e4d7b28fce0f761ea509ae70a0c80307fbe7c7c132cb344`  
		Last Modified: Thu, 11 Jun 2026 19:13:42 GMT  
		Size: 15.0 KB (15048 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:22e79b7fea529a3b91a0cc23b4284db1dd1e585c771569557bd425fcaedcaca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54495440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decc7ab86e800f3eac94420f957ca4e5263163ad9ed8e8d4b11478bb6942ca76`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 21:16:38 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 21:16:38 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 21:16:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 21:16:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b10e73d1baaba21401b2287535cb5c656dc6aac61703f44eb86be9548d27d7e`  
		Last Modified: Thu, 11 Jun 2026 21:16:57 GMT  
		Size: 50.8 MB (50758784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3b8a703347512fa615b5c44db41352a1ab55cdf54923c79dfb30993e3fcd9fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a952aa4d70390179f47352a3875b3f651a33bdf1417038176e45531ac5dee4a0`

```dockerfile
```

-	Layers:
	-	`sha256:89e641122e234f297c8018892c455b4a6cad5d03c52db4fc286cd073c25af169`  
		Last Modified: Thu, 11 Jun 2026 21:16:55 GMT  
		Size: 271.9 KB (271933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:766e347e49e9559e1afc084baf05275532af81a690e1fc7fd1143116147661b5`  
		Last Modified: Thu, 11 Jun 2026 21:16:55 GMT  
		Size: 15.1 KB (15124 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:a59c9c8299fda708a5aa02e90b545bf2779c1e8f9c53022875d2999182686f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54002435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec9b4b41649b05d8461e78fd5a014b717c9240c1f81eb2d56346df7ec72c044`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:18:58 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:18:58 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Thu, 11 Jun 2026 19:18:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:18:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc43a21ba1c0df33d7796440921875cb8f2ef0543544b32f418e40362e1385d4`  
		Last Modified: Thu, 11 Jun 2026 19:19:12 GMT  
		Size: 50.3 MB (50348562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d4c8af08c9e1635383fdb11a67b2f39a19d5959a5f7b3348b21271841209bbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 KB (286979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb9adb33a6d37c8ea320f83d784e1b6fc8a84b1c0017c56d3406de2f1f6b018`

```dockerfile
```

-	Layers:
	-	`sha256:b1530e3f252e4b7b023fd15553e50d182a050c4993753d8ac6271ebb602f8628`  
		Last Modified: Thu, 11 Jun 2026 19:19:11 GMT  
		Size: 271.9 KB (271899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f74b343f23a24cc281e41c7b3661a25e1707abfef9fea1e23c564cfe46c844d`  
		Last Modified: Thu, 11 Jun 2026 19:19:11 GMT  
		Size: 15.1 KB (15080 bytes)  
		MIME: application/vnd.in-toto+json
