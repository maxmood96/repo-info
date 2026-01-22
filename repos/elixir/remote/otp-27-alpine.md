## `elixir:otp-27-alpine`

```console
$ docker pull elixir@sha256:cf3e8ee853337192da915018959011aea892d3019460c0082fcd48fe7dc9b538
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

### `elixir:otp-27-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:55143cc496b9c23e7ed399fb46f1c112263d59ed73fc1284d21a680805a8af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61436137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a657eb50529fa54495bc9c4482e7061af906f2664d3a145f1983a743c7b592ad`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:28:18 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:28:18 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:28:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:28:18 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 21:50:43 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 21:50:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 21:50:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95341a2ff0e99b16d75dc96f2e240d470af6f563a2cb986051c0bb37a6846a1`  
		Last Modified: Fri, 16 Jan 2026 18:28:27 GMT  
		Size: 49.8 MB (49840975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9333e06afe23f9d350a698a987bc05a4c103ad9dbf9f03b167a3df107567b495`  
		Last Modified: Fri, 16 Jan 2026 21:50:57 GMT  
		Size: 7.8 MB (7792710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6a7dbf902039cb6d36b6f9a784458587c2ba3ca2071327ae0a5f639f6aba25c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 KB (295239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c3b2968ec5e2f3eab17c86d0b6034d1fb32dd13a251db89ef8da90e4ae01db`

```dockerfile
```

-	Layers:
	-	`sha256:6e0b361b31a499e87d9be2c23ee0a3bbf2b53489aeebff041c8cfce2620b8245`  
		Last Modified: Fri, 16 Jan 2026 21:50:49 GMT  
		Size: 285.8 KB (285755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0b28b2a1e09f96487d9db3a5c6ef4a40a40efe0ca31a2e09a81c35e43b5883`  
		Last Modified: Fri, 16 Jan 2026 21:50:49 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:5ddb933f752747dfeecf5d80faeea55ff329b8e6572eeefe83b655e898dc6092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58388121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1735386e6fef991fdde97dc067c007837f6b17a81e3f0743d4c75a0cc9ecf677`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:28:30 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:28:30 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:28:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:28:30 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 21:50:19 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 21:50:19 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 21:50:19 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc352f1ce5dbf34997f7beff06df39a9a6bef9defd536110ddc9d3a582e696`  
		Last Modified: Fri, 16 Jan 2026 18:28:39 GMT  
		Size: 47.4 MB (47373373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7143c62072986b21e1ca2867d70113b17916643a9b392d2e4766fdb82fa494`  
		Last Modified: Fri, 16 Jan 2026 21:50:31 GMT  
		Size: 7.8 MB (7793193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:689f4d23868c0fb5b98801630d8c85ffeaae206f9556af60117650b3a6646e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2985c93378afd050061e76ac1e28534d939bfa7af27362f4b1c772a2057ffc2e`

```dockerfile
```

-	Layers:
	-	`sha256:076fa7e802ecf579f0c644a24f9ff8c47ed4328ae9df5ed497f0e3b1f38b474a`  
		Last Modified: Fri, 16 Jan 2026 21:50:25 GMT  
		Size: 281.5 KB (281539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c82eb6cd36ce20c014f1a1de9ea7088f6492225f64a108291718bda9fd49c3d`  
		Last Modified: Fri, 16 Jan 2026 22:53:06 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:6f4f8dd0c2b44a586be38b5749d21fb94cdaf5704515fca06ad1b3fbe91750fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61569615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4700ae3604cc2ab947cae1eb179bd53656edc1e0801e5b51c944176a6a8cf780`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:28:55 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:28:55 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:28:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:28:55 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 21:50:58 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 21:50:58 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 21:50:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184c4d363a4d0db6ad942dd5fd7ab4d961598380a3270f15e2b8ab7550ce2ad2`  
		Last Modified: Fri, 16 Jan 2026 18:29:24 GMT  
		Size: 49.6 MB (49638821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71242c51a72259903cdc2b4da236d5cc1f1bd3af23ef19b36b2cafb1de6946ec`  
		Last Modified: Fri, 16 Jan 2026 21:51:10 GMT  
		Size: 7.8 MB (7792725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:16faaa3d4abeeb15e230ba2e450d03fe87ec0d6b6641936da0de86c1384c9f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 KB (296111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13127cf56eeb993c23c43bf08bcb104dcc697c2e03c3c24f1fbae35d6e1982a4`

```dockerfile
```

-	Layers:
	-	`sha256:a2ed6b85650b059cd7fc1be756bb8fcbda4bae2bd61aa988a3e0b9c8b56c9244`  
		Last Modified: Fri, 16 Jan 2026 21:51:03 GMT  
		Size: 286.5 KB (286535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55605c15625f6a9170bb5124687ceaab2f7270c1b7c6741f2e8f0119cb6adc9`  
		Last Modified: Fri, 16 Jan 2026 22:53:11 GMT  
		Size: 9.6 KB (9576 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; 386

```console
$ docker pull elixir@sha256:3ab8b39c7489413c642a980dc04a3ee3a0eb4ebab1eb92d4e3343f223c6a873a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59707183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea932f9d2e6d54e077d1350bc2a1267383740227fe0c1e692102b8a3a1d2585`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:28:28 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:28:28 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:28:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:28:28 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 21:50:37 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 21:50:37 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 21:50:37 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b78d84b86ddb2c16f9c1a700e7bead9342ac6dd3beaaaf1b7621c5ab50992a`  
		Last Modified: Fri, 16 Jan 2026 18:29:05 GMT  
		Size: 48.3 MB (48295005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a52cc13f98bdcdf50865b5c2ba8ce5191c7a36aed7deeb8a3e321fb1264296`  
		Last Modified: Fri, 16 Jan 2026 21:50:43 GMT  
		Size: 7.8 MB (7793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:99c040eb14f9aadb69c29a89fa2a5c286877f071f05d46081a212dfc1e6bccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 KB (290213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ac3bb64ecce5f56c8330c06134706cfc2eb6d971e647c74cb6fb3d50a1823`

```dockerfile
```

-	Layers:
	-	`sha256:6969307ad939ab0f5ccac75f6f191317a62d197e120d372269c444e41fac040e`  
		Last Modified: Fri, 16 Jan 2026 21:50:42 GMT  
		Size: 280.8 KB (280755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b48ccd03951f5bd09b9fbdb4f3a4317eccdfa95a4afbfd596da459ca84a1429`  
		Last Modified: Fri, 16 Jan 2026 21:50:42 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:b0c187fec003ce199513095044355cbd81649e7fd075ace8c4c9fb65dcd861b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59919611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a25643135116870acfd5c662e0415b3f3f6e16666f0d402ff50164b35013b`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:33:53 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:33:53 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:33:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:33:53 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 22:24:17 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 22:24:17 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 22:24:17 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e7696db3289ad5934c1928d08e8fdf8371a4a539e3bab54272aba6849bf9df`  
		Last Modified: Fri, 16 Jan 2026 18:34:11 GMT  
		Size: 48.4 MB (48394130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3fab634f15bb04dea7e0bcb579366114e74407890790623e7a78db8d7f9f79`  
		Last Modified: Fri, 16 Jan 2026 22:24:46 GMT  
		Size: 7.8 MB (7793240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:bb0a8bb15b4a479af50b960ba77e193854d5ff197fc2d2544dcec2b2e6f1e86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 KB (289111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace61676fae2d725ad3825ac8f25a0d6729ac66fce64d71a4e0ab0f907e5d552`

```dockerfile
```

-	Layers:
	-	`sha256:42c350663f7c3b37bbed798cd5328922f63008a36f67d6159377c5127a658f1d`  
		Last Modified: Sat, 17 Jan 2026 01:46:15 GMT  
		Size: 279.6 KB (279588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1221647e704118b71b10203015fa6056d32149d3b63a69e480cfeb0de5570f77`  
		Last Modified: Sat, 17 Jan 2026 01:46:16 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:e3f79b896191d959b61e03935764cc4c3b4716bc2566c5723e829266943b13a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59500886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70a3726cc9399aa7b733a639c66650cbee92ed7de96a391bc05c19eb1bf324c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 18:27:28 GMT
ENV OTP_VERSION=27.3.4.6 REBAR3_VERSION=3.26.0
# Fri, 16 Jan 2026 18:27:28 GMT
LABEL org.opencontainers.image.version=27.3.4.6
# Fri, 16 Jan 2026 18:27:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="658529f94cc5b8833907aa680a5e979e67c32dd6ebba69ed3b90b95f526ccda2" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 16 Jan 2026 18:27:28 GMT
CMD ["erl"]
# Fri, 16 Jan 2026 21:55:25 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 16 Jan 2026 21:55:25 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Fri, 16 Jan 2026 21:55:25 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e54cf37f98b2e3e05ce36a499a2f31be32107b21e490753b581c6655d34a0`  
		Last Modified: Fri, 16 Jan 2026 18:28:15 GMT  
		Size: 48.1 MB (48058428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc92b60560d9429d8c5ab25403a04efbcd2a725755320bc272a14adc0769e3f`  
		Last Modified: Fri, 16 Jan 2026 21:55:35 GMT  
		Size: 7.8 MB (7793214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:98d0df23f141bfeeda94bbc71e217f8556c9a22f5afe13c3bf3952b9cb8aa905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0740af6105f728447368acfd9a16d55df340d02efe42c062dc7a9cec7f9533`

```dockerfile
```

-	Layers:
	-	`sha256:9f388e6416e49cef83c90adbbbe6a98c0f096b1b4b064bc0839c360d969e09d8`  
		Last Modified: Fri, 16 Jan 2026 22:53:23 GMT  
		Size: 279.6 KB (279560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63bb8ebce51579ec90b0bf117a1b1a38b805261562e2aa44ff255650784ff83`  
		Last Modified: Fri, 16 Jan 2026 22:53:24 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json
