## `erlang:24-alpine`

```console
$ docker pull erlang@sha256:af9b78ead6ee92ccc49829834947e23d400ea2f4d16c1090313273fbdb55ebe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:24-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:850c27870adc2bb8fb9f34bde61a614dc6b39208ce6f327ccb07a05ebfdb0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49062733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3952045ebeccd068644603abfdada5f610fd7d2542e4fae198230559852277cb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Jan 2025 18:50:03 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 18:50:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486c0dce9bf5f8b39e10346d71a2adb407fd9527e32705f3f4ffb5a8ab7778b5`  
		Size: 45.4 MB (45448734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:376805301e64c482de9869c73b6181f5e7cb62f82313f4d3c85d47c3beee684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a496d1e92037d3225ba07f2b4363b9e692a7e2397dac65f55a89c562bce7e20`

```dockerfile
```

-	Layers:
	-	`sha256:daf49b5a538d99d86e7ac078063603ce08f9bd4d4691dedc45b6febd9c266575`  
		Last Modified: Tue, 07 Jan 2025 18:38:07 GMT  
		Size: 267.1 KB (267130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e4b4b3c6c8841148b4c27e76328b60512dcd79bb439475f91ae9f299acc8ba`  
		Last Modified: Tue, 07 Jan 2025 18:38:07 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:849855fefe08c8a7b98d2a373064e938b6dfffdd82213bfa67ca0f00829e282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90260a68865324b2c8d093b9f1af4370258616452bbcb29c3c29c6fa71e6635`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-armv7.tar.gz / # buildkit
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
	-	`sha256:845348bd1dac290491d16e4c9229b11ac46e1df9e4a500110bee98a2f9888a29`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 2.9 MB (2880509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3601b6d4fc9fd59ecf977ded90112c9c27dbaa2292cb811bac64f8ea68bfe`  
		Last Modified: Tue, 12 Nov 2024 17:06:01 GMT  
		Size: 45.3 MB (45252047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cf59b783b4368dab45f4fbb7057df51423ca4ae91833e405bd79e509a6b058a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5662c2d53f168612338ce816b518ada23ca4e75f743198938d3f84b3536a7f86`

```dockerfile
```

-	Layers:
	-	`sha256:401033779000849d3fdb51cfb1b57acccdb679b291a55d2320e0390565266ff4`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e76600c6f614a2705cc1ca60a19a4ab11eac2f45eac10cda519c3f095f94f`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:16b511fbd3e7b250bd7e5901f485b258e81e45885e3690db10ad0f2fe9712dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115b00ecc97b0fac61522d510e0cc50b2708cd0108a97bc43d1211b4f7b62cb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Jan 2025 18:50:03 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 06 Jan 2025 18:50:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116c363fe5b5a6d099aa25eeb6a667c6d772a404b3327b3364009f7ba9ecafe`  
		Last Modified: Tue, 07 Jan 2025 19:54:06 GMT  
		Size: 44.0 MB (44024487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:01625b86a0dd7e085bec3da36473867cad8d78f14192715cc096bd7d095cc6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 KB (278375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625792f573923533540ca49c775604090baaf0a1dfe055956aaffeef162ad98`

```dockerfile
```

-	Layers:
	-	`sha256:16f86c8e7e19f404663bf0dc99396661eb24a2fe94caa304083b5e254ef6a84e`  
		Last Modified: Tue, 07 Jan 2025 19:54:05 GMT  
		Size: 263.2 KB (263225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd545a11dbb7df1a8df60a25618d18da6a2c0fcba9298f3296882d93c297543c`  
		Last Modified: Tue, 07 Jan 2025 19:54:05 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; 386

```console
$ docker pull erlang@sha256:1bf5d93dd976e34cc9036810c9eb473f5cdfd4151eaf176b4815036c6f526299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47614904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b83b8be410b0b4feedad4bbbd5bc3fc70d16ed61ac057640f3b705bd343f83`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Jan 2025 18:50:03 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 06 Jan 2025 18:50:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a734e68060cb0a4b5792b616a8c2387372a6360a21fe3352c58ab5dfb10fc`  
		Last Modified: Tue, 07 Jan 2025 18:38:36 GMT  
		Size: 44.2 MB (44151715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3989f9b43791593595cd2c0521ffcf358f931b76e9cabd342636181e8fb7eeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 KB (277420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186eaaae71c84c0cf06dfb8192177849fc5e0031a145e3fb2728aa76b8f30c6`

```dockerfile
```

-	Layers:
	-	`sha256:368c159bcd2f7197ce496ef6f9ac53f1f1b82f798fb74343ab43ff036afc191d`  
		Size: 262.4 KB (262407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa7cc957c413e401d68e14d8ffa0731900f8d247833fc53a0fc18ea91a0e243`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 15.0 KB (15013 bytes)  
		MIME: application/vnd.in-toto+json
