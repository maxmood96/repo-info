## `erlang:26-alpine`

```console
$ docker pull erlang@sha256:9a665499728e67f8bd5c322bc957f34621af684c6b3eb8cb334e8fda78f8735b
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
$ docker pull erlang@sha256:c8ba2b595eda4ec5851a4532cdefb3d4de3d579cdec26a909557aae6f83895b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49272051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31979248e25c35d781df7fb5d072e7ec06c676c9339973fd6fe1fc9ade035d4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db2bb61fc4d09afaf3f7a6bd5ca70e67a8417c6e66e627a9b8e3c23a3085de`  
		Last Modified: Fri, 06 Sep 2024 23:26:06 GMT  
		Size: 45.9 MB (45852345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:af91ddeb76ea473a24f529e9ab4b28f7a5ce959e4440ba463cb6a0c16d0e446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 KB (286856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2b353b4b5bba71190f9e3d1e63046c61c6c39d51fa7c85a7d1361eeed5f5c9`

```dockerfile
```

-	Layers:
	-	`sha256:357ef7675ad70765a360048cd323b7b06ac2d58dcc7e61d1c1e80857d05354e5`  
		Last Modified: Fri, 06 Sep 2024 23:26:06 GMT  
		Size: 272.1 KB (272058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ceb3f3df68e783d8d93438c4928c610f15045b87367775f9e11d7a5ef73a2d`  
		Last Modified: Fri, 06 Sep 2024 23:26:06 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:10981098f0fb2d44f128ae8f665991dad6833bedeea0a0808c8316804866532f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46488445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6349a9c450e08f95296549ea834ad08b8401160172f3b14ad337f0400daae`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de9b2e33b197cc41d963ae1e0aed045c4c1cfc44f8a402e53fa81a4f51079ef`  
		Last Modified: Sat, 07 Sep 2024 02:32:34 GMT  
		Size: 43.6 MB (43560781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:6d5add4e1c4c8fefd047dc5cefe4283b3e9d26d02d66921515455e11b015cd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 KB (282888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba77586852d927dad312905d83ecb1551fffa6420e112e9cf7d61a2ac3daf12`

```dockerfile
```

-	Layers:
	-	`sha256:10e17c08360859d317d264af63c0c9526e7bbd4a3b153eadd7edf8c09d45673e`  
		Last Modified: Sat, 07 Sep 2024 02:32:33 GMT  
		Size: 268.0 KB (268022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e8a49bd1753d8064a7301f75cc38894b76b3c5db5b8d6458824075a90669d1`  
		Last Modified: Sat, 07 Sep 2024 02:32:33 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4d13a08b8424943b50158eb6037c60346cc04ad2037f6f970e1dc78e1d53bf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f830bb301f83012a08786eb0f9388dc988a3bb27b2b67ee163b1b144f23a8815`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c65f7c488c0dd14acc4f73a67e53adb5056811a55dd6983d73f028db97fa76`  
		Last Modified: Sat, 07 Sep 2024 05:07:53 GMT  
		Size: 45.6 MB (45646357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:926d84021c00af7e44d625af69d0a9fe87e46c584820a60bb577958e59db8942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 KB (287843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c251e88e6bb3e92bb9e2a49afff5dddc7e5f8b8aeb4d0c785ed263d41ebe36fe`

```dockerfile
```

-	Layers:
	-	`sha256:d5e9b6b6b406e07aeeb6a60731c6abe8be8cbd2ab3a2b1dd49d1cbcc937b2981`  
		Last Modified: Sat, 07 Sep 2024 05:07:51 GMT  
		Size: 272.7 KB (272745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d892436cf926b0f4a8b17c7707b1e88643c486f6b8d5df782f03ff56ed1193b`  
		Last Modified: Sat, 07 Sep 2024 05:07:51 GMT  
		Size: 15.1 KB (15098 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; 386

```console
$ docker pull erlang@sha256:edeb26f40c2eff22d8b8efebe3d12e7f42a83a423de6db58ab82269f3d9874f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47741711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d85c193a856f44d678b49c2a21fcb80f9e74f2de6fce2e5fc09ae78ad5a522`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720ec63191a7a9af02d97d7fec87250278b0a9f12f4ea2c2d920589ce3945f47`  
		Last Modified: Fri, 06 Sep 2024 23:27:17 GMT  
		Size: 44.5 MB (44488106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0ec16a2686baab6d460781e56592bca4039f50624313af0f98f0d4c906769796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a195ce6539a9d6d57451bf8b877e1a81c3a8f82405ff7e0b5857fa5e8fd07a`

```dockerfile
```

-	Layers:
	-	`sha256:fed91171e75d70c90b026625063dd6453429af2aeff8b103e8a65ca5abc78740`  
		Last Modified: Fri, 06 Sep 2024 23:27:16 GMT  
		Size: 267.3 KB (267330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9b0cb559f40f3c4e5ec042ac6bbedcb6cb8b7cfa479997038888d04ade71fb`  
		Last Modified: Fri, 06 Sep 2024 23:27:16 GMT  
		Size: 14.8 KB (14769 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:5dd34719a5752e68ab901224e444781d6eadc2a75dd79b5cd903ac64b9a34fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47866169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1c94a482fe00b29bb8974050b9138f8d4a7b599a755f16edf0d7b7fac31c8`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8c3ec3d03a6bb017273401203cf75c78f39536eff1ab08771d2c66ea673cf`  
		Last Modified: Sat, 07 Sep 2024 06:41:01 GMT  
		Size: 44.5 MB (44501702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d7f2fa1224c4f2fb279f256e9fccecc9ee8014d2f524bb9282b6a29849137dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a550a978dd571362479db8fd38d0d3041d162b73f702504ab6ca99d86acd50d8`

```dockerfile
```

-	Layers:
	-	`sha256:fb089ca9583b6e9f24ed1effbc9c13c34804122fca689fca401730f63223e742`  
		Last Modified: Sat, 07 Sep 2024 06:40:59 GMT  
		Size: 266.1 KB (266066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a224defe8703d73a90d21a12fcde7704787a20ece5bf2c107c1b1478264348`  
		Last Modified: Sat, 07 Sep 2024 06:40:59 GMT  
		Size: 14.8 KB (14836 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:b2f65c1b084f23b486a02eff77999cc2fd2775bae1cf0dfb1856766e11720932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47453390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75696540545f7b5ef8fbfac3ed2fb241c3148d17db29ff1abb890ff878bdf9b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef458bae4f566ea087150ba9664fd270b6ab2410ad9927d43983f949e3cfbbe`  
		Last Modified: Sat, 07 Sep 2024 02:24:32 GMT  
		Size: 44.2 MB (44200033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:701476fa5fc94b0bc0067090d8cf9b34816e7a6a782b12b35e9f4b51896be832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e90c744ed761094f8fbd70bf17e8639f609c950d81c96ff370c95028a2463d`

```dockerfile
```

-	Layers:
	-	`sha256:d208e5e22ca4093f01766a5aaa400c6dbc632027afc18e45493ddc9995246149`  
		Last Modified: Sat, 07 Sep 2024 02:24:32 GMT  
		Size: 266.0 KB (266032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7624dd482fef1c0a5d3d8c64621cf1a66dac2e87f818717d0d7536c2bec08418`  
		Last Modified: Sat, 07 Sep 2024 02:24:31 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json
