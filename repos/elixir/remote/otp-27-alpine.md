## `elixir:otp-27-alpine`

```console
$ docker pull elixir@sha256:5ef5ca922f8d2e5fd5bb9e0729b463a84b953cf93a284ba132ee4000170a819e
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
$ docker pull elixir@sha256:30be1f54616ff476edcbf957ccf1acc4afeb821012e0ca1e900b1a274645d87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60776583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2511a3dc33db0614529c31bf6a7bab60b3a41ecedcab2ee9937bc6b2cac71e4`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612bac6e6999542fb247cea8095ef1021e4905688966a59f967e33acd6235f3e`  
		Last Modified: Mon, 24 Feb 2025 20:31:32 GMT  
		Size: 49.7 MB (49668770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b2eacd6490ec395ea7d26c53d6523d8e327be478c6e3b3f8c03f5784811fb`  
		Last Modified: Mon, 24 Feb 2025 21:28:13 GMT  
		Size: 7.5 MB (7465566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:cc9098d0bdca5f15b552f430ae8add6de1ee22f426ce3ac36fe6e80b276eeb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 KB (247073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c56e096a618c108f32e6050aabb31f99ac19629e1206fc2e13f1ea83a1b875`

```dockerfile
```

-	Layers:
	-	`sha256:995056053e0536b5c5dbcf62648efccc557815c761a73cf7ee95e406ac3d3cc3`  
		Last Modified: Mon, 24 Feb 2025 21:28:13 GMT  
		Size: 236.6 KB (236643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cba1c32bc119b0eed6a74b1e84e9427805f16b88622d93e08346cc48e7cf45`  
		Last Modified: Mon, 24 Feb 2025 21:28:13 GMT  
		Size: 10.4 KB (10430 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:acd93bdbd6ac0d578749082e112fba0a1460d1706702bedae361f368812f62d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57766734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb107c5efd5abf34f4d1fc94d67859f1681bd600c92066ab4d9d17eb26770d75`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc0d280a97880b4d716cca9e3f9bb219f4f386819fad44292de42a2eaba290`  
		Last Modified: Mon, 24 Feb 2025 20:55:12 GMT  
		Size: 47.2 MB (47203537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201866812aa3534ff850ffd4a8cc1f5db37e74819839bcb81e0cd8749596930b`  
		Last Modified: Mon, 24 Feb 2025 21:32:19 GMT  
		Size: 7.5 MB (7465074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:9ec744646993721f9afd61c1bd9e93922446ec4b5f9b358a523838217ec535dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1382a989702cd139b7456a02c6dc93976bff49f0d56fe4f4db9dafcec1ef38e`

```dockerfile
```

-	Layers:
	-	`sha256:1603b4219d5a4238f9825e8783b2259863b57d0cd66e7dd9d7d6ca9fa0666b9b`  
		Last Modified: Mon, 24 Feb 2025 21:32:19 GMT  
		Size: 280.6 KB (280627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bef190f6a225d1e1f6ab105117e57ee3649e0f59208699cf4be3886bb04338`  
		Last Modified: Mon, 24 Feb 2025 21:32:19 GMT  
		Size: 10.5 KB (10521 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:efc78bd1e12059a6af1eeca180973dd707c66fe6c7e01d9fd0d6531ea9024da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988f682283235f1ada1bc27175cec101afa12bbf849968fe0ef84903815df8af`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a73839834392f9b9d4f7c4fd66b9ecc51e77f2d5942b5ba5e6f1e2c8545b42`  
		Last Modified: Mon, 24 Feb 2025 20:56:49 GMT  
		Size: 49.5 MB (49459834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d88771d0bde24acf5d1d84126201d938dacbbbe60d637b66a5fc189442db81c`  
		Last Modified: Mon, 24 Feb 2025 21:32:14 GMT  
		Size: 7.5 MB (7465711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:06db417dda3167641cf13bdf786fe2ddbc5a51b1801fc22441d5659a3eae4b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af6365ae866a6c537157f8b62a113cca79d97cd5101fa386219803274d53495`

```dockerfile
```

-	Layers:
	-	`sha256:527f6b00992e1c922b0b8ad8507ec21ce1661aa84c30680cd779acfebdf4b88a`  
		Last Modified: Mon, 24 Feb 2025 21:32:14 GMT  
		Size: 285.3 KB (285281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e833ce203a670b7476559dd4a50e3964646b80bec44b47136e4ee960f73988`  
		Last Modified: Mon, 24 Feb 2025 21:32:14 GMT  
		Size: 10.6 KB (10558 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; 386

```console
$ docker pull elixir@sha256:5b7b8cfc8631443fbf6416caaa4bbe876d3b9aabfe382bd75d47247b54413a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59050094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb452c20f8d308831c0104467be60f64203636e7b6612021d24202bd57254f2`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717f99586060d8a1fbad61954e34be74aee9c0d3edc8971b4eeb4d29e21bc08`  
		Last Modified: Mon, 24 Feb 2025 20:31:34 GMT  
		Size: 48.1 MB (48121609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce81eeae5b37f5ca790e9d994204eb4b098e3ec9a4726022adf712da1c4eee84`  
		Last Modified: Mon, 24 Feb 2025 21:29:02 GMT  
		Size: 7.5 MB (7464862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:17278956140c28f22be2e19e83db10cc5baaac64f989deff43621baf36fdb516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 KB (242369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fee9db9b5fe0cc067cae2593b24de58b0daa8ab64c5dc3f92348dca2affe1e`

```dockerfile
```

-	Layers:
	-	`sha256:576033717ca77dcd57b9fb0bd9fa529dca3372b72e0f49781710ee0ed230fdd6`  
		Last Modified: Mon, 24 Feb 2025 21:29:02 GMT  
		Size: 232.0 KB (231982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c125b24ee9ad20150aee67501b64a5ce58f8d778f2a8ec38db152226a782d657`  
		Last Modified: Mon, 24 Feb 2025 21:29:02 GMT  
		Size: 10.4 KB (10387 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:5810bc63cb013ff63db1fb316e27b13ff32230c1b28a5cbae6cf97ec2826d62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59260769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6859fd6e9535cf7baa1226f8296da48c2d41c6c97c92f1f07e9f0be809f99296`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7bdceac40e028a42c4f3a2266811a2cf462c6d99bf9f85d76dac45a17c2aa4`  
		Last Modified: Mon, 24 Feb 2025 20:57:29 GMT  
		Size: 48.2 MB (48221643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859c664235289287616082b43521736380a2b4ab8705e82791670358d7ce6b5`  
		Last Modified: Mon, 24 Feb 2025 21:32:31 GMT  
		Size: 7.5 MB (7464781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e6ae50bac0072e097fff8a12974a613b904f753098fb5a4d33e9c44828348c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0e656a3a77bfa1131a55a661dd5a704e6a6ea90be37890ee627966dea2e7a8`

```dockerfile
```

-	Layers:
	-	`sha256:f445456540284ef07ff069b1458f6dd2eebd353a2c0546d85b013b86faa92902`  
		Last Modified: Mon, 24 Feb 2025 21:32:31 GMT  
		Size: 278.7 KB (278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656dd5c2bf3691ed45568e6fc16048b4351da8f00624d8003c4d0aa2432806bb`  
		Last Modified: Mon, 24 Feb 2025 21:32:30 GMT  
		Size: 10.5 KB (10486 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:b36ab70ec6f9831c38bd84e908be19bc9805f375d158455ccf741569afeade3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58780259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e99af2900f054fd9040d75b4ea7832a035c8a29fa8599900f63747a95a4332`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 09 Feb 2025 02:28:09 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["/bin/sh"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dacda7c41ab101c2d831da6e6abec358f84f776a42c7baaafe10150e53c53b`  
		Last Modified: Mon, 24 Feb 2025 20:53:59 GMT  
		Size: 47.8 MB (47847829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451cd5d66ac7271d7efcb1c26aae2d5f2faca2f5c71a404164f24a28163bd999`  
		Last Modified: Mon, 24 Feb 2025 21:32:16 GMT  
		Size: 7.5 MB (7464863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:80757bdd5acfce74e1f103b5b4b2a2aa5c9a7d0e6921e2630c3392807efd6a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 KB (289053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e3caf7c48f59408039495277009fccec186ac6cd0a35dba10a08a3e01d5c9f`

```dockerfile
```

-	Layers:
	-	`sha256:e1dd36ba491e6c34017bf91c3a4a61717a18d7a832487033b88b6b57db7335ad`  
		Last Modified: Mon, 24 Feb 2025 21:32:16 GMT  
		Size: 278.6 KB (278624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6583b6cf4fb758a6249090888440309f12cc6fa07392c19c84816fc9bd2dfda1`  
		Last Modified: Mon, 24 Feb 2025 21:32:16 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json
