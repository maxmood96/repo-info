## `elixir:otp-26-alpine`

```console
$ docker pull elixir@sha256:1217d00abf83c9e5385b8c85a2c75f0a2d21c6d2737976fb40bfabcd329ca804
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

### `elixir:otp-26-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:133c7c73dd7511339346069cc14b743db03bbfad550c32fff4dc8689bcc9700a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57162262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7d05749bf55104c76582ac6bd9a6378ba4a0202d5b8254070a7896d583dbc3`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d444a214832f824cd8f7be26fe8447327137d14e1bc168a892d90ad579ae74`  
		Last Modified: Tue, 15 Jul 2025 19:34:27 GMT  
		Size: 46.1 MB (46062906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019d1c195a5bc2fcf230e969f5621eaea646e507c6638e523a9d1d1c6803e399`  
		Last Modified: Tue, 15 Jul 2025 20:20:28 GMT  
		Size: 7.5 MB (7478879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:088865435fd24b40e0bb25176ea55a6f04a4f8515a12201446ba2a5f06537f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 KB (287287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386fd1e42f96733ba90c4d3e9de525bf8f039d45e55c8af1bc3763d30a787fc2`

```dockerfile
```

-	Layers:
	-	`sha256:82869058fe6ce7f46762f976fa7d177ab0b73f3b81e5f8708b3ffd67fa089025`  
		Last Modified: Tue, 15 Jul 2025 21:47:17 GMT  
		Size: 277.8 KB (277758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba95dda8f9d8fbda4016e807a645126d939cb810c14b098bb8898e36c1484458`  
		Last Modified: Tue, 15 Jul 2025 21:47:17 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:fa1dbf20d37c76626ffa60608109169ecd3d0094ffaa465d6f58283fcdaaa40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54303167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993c5fe6738aaafb7bda904aced704b1c5177f27df05cd19a402b679e2d788df`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-armv7.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7a2922d87ff4a12ac3b3f3b411977d790a892fd943e7c888ef70811df372c242`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.1 MB (3093180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33179174607b89a15f4b8970fdb7510d37151bfb674c1d09ebf92e716678a581`  
		Last Modified: Tue, 15 Jul 2025 22:51:25 GMT  
		Size: 43.7 MB (43731613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09296f5044341f2af9bb75569525d30e3fc9a5d2e2a23bfe8995c96f03533a`  
		Last Modified: Wed, 16 Jul 2025 07:01:05 GMT  
		Size: 7.5 MB (7478374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:096da76196df22274b4ccb7d712c6ee42d3d4ab9262b816269fe84f6dd5837ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 KB (283068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323fb91246884e1b1693852f8cf7374bf4e65cd2dd98c057e173dba37a985f59`

```dockerfile
```

-	Layers:
	-	`sha256:7b79b6296df0c8cb86a1ff5f6930bdb6b64eaabc558b00539f4d5e76c906b9f2`  
		Last Modified: Wed, 16 Jul 2025 09:47:13 GMT  
		Size: 273.5 KB (273471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a74d82d394697edee74bb250f5bc4b3cfdd883f4e5425918e64557878f98e5`  
		Last Modified: Wed, 16 Jul 2025 09:47:14 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:eb6afd7a10a994312f3ea635edd258abb004aebaa4c80d28de93f49cb35f588e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57424876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89881e2c916b28e84d647a8ca5ef07aadcdaac63eec2eec471f4b50e062bb3e7`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6189f804273163f168211d1ab025838fd14d45b2564109fb3535c043de37cbf`  
		Last Modified: Tue, 15 Jul 2025 23:38:44 GMT  
		Size: 45.9 MB (45857615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26625a581aafd892d9024a89c8c594c077c80ab00df321496544f8819678f61a`  
		Last Modified: Wed, 16 Jul 2025 09:03:00 GMT  
		Size: 7.5 MB (7478893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:1695d92b9cfd3b5f0a088ec6e7550e0568ca66377d976037a6a04b75dd2228e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 KB (288159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bca628917e8165100ef28c71100b4dfbbbd03575903c4c75853e6142b26655b`

```dockerfile
```

-	Layers:
	-	`sha256:b58e62163a77f56cafa6f32e40fba42bf806ba54de99b10b291eedf46ebe36f4`  
		Last Modified: Wed, 16 Jul 2025 09:47:18 GMT  
		Size: 278.5 KB (278539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e38ee3caf637023da6bcfe06765597f1bd7f8e30d37a0e9d60532b78bcd86b`  
		Last Modified: Wed, 16 Jul 2025 09:47:18 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; 386

```console
$ docker pull elixir@sha256:4dfcce3c91521f05043a4f2eaf8a57d21b4d8ac7b08a49a8abab24b533aff8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55606820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8f24d8133474090e75d42d583fd17fb1ed9232fd95a75ae3fedc40374c82e`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-x86.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f2c5554b635c7708a3eca8bca65c800841524b67ab470f877eda5a88d78217d5`  
		Last Modified: Tue, 15 Jul 2025 19:04:09 GMT  
		Size: 3.5 MB (3465007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50079052f94a1a2dfc6e62d123c9f20fc7d39776e5d2d0591c644df2a749dba`  
		Last Modified: Tue, 15 Jul 2025 19:29:13 GMT  
		Size: 44.7 MB (44663408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514aa96ce644b0adfc7e53b0cc23581242afef4d7b51ec66ffc0e049c90237bc`  
		Last Modified: Tue, 15 Jul 2025 20:18:29 GMT  
		Size: 7.5 MB (7478405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e0ee4ffea6d1d04e958cc545f3b3588f50b6b570d530d89d18d924088c8a9eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb29d2b77951c6798f7d0f880499e9950750d26176e7059ee80b209da84d5895`

```dockerfile
```

-	Layers:
	-	`sha256:bd86da990fb068f4406238e70efaa25e1d0469c54cf13ac38c855fe80484a7da`  
		Last Modified: Tue, 15 Jul 2025 21:47:29 GMT  
		Size: 272.7 KB (272686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e5107d51dec5056a6fd6685788c0bc0aedded89bafd1ba494516ab928da22d`  
		Last Modified: Tue, 15 Jul 2025 21:47:29 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:800e2a6906580211c52aaa67534f1f710f0b058a96f642f5089018f4675abdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55759712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d5d88e7fdd341073520d2093d3a6517d86b96cfbc6ae7712a89d8981d1e6e2`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-ppc64le.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:73bde2df7f2a99c3410af2a896f6a27d75b568382e3402ee391dd7f3a0b19069`  
		Last Modified: Tue, 15 Jul 2025 19:00:47 GMT  
		Size: 3.6 MB (3570555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb57c0d43033ade837b6ab295e4b593940f440cb8797139160516f69f1b573`  
		Last Modified: Tue, 15 Jul 2025 22:59:01 GMT  
		Size: 44.7 MB (44710753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa28936c36977573a1a9e9837433ea7bdde666b4d7cb764ecdcb83eee8ad0072`  
		Last Modified: Wed, 16 Jul 2025 04:39:03 GMT  
		Size: 7.5 MB (7478404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:48c2ae1e501e8734a0b5649a85981fe168545f07371a569b7988213bbbb51f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b0567cb12839ca41c25024fa19135764140f1963c848b92c07a80b4e6ccf68`

```dockerfile
```

-	Layers:
	-	`sha256:475514f97f416531e43edcbfd1df67e9f4edb0b085d1889891dab30a46ccd6b9`  
		Last Modified: Wed, 16 Jul 2025 06:46:02 GMT  
		Size: 271.5 KB (271520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d60c5e94029124fe50b9da1c13002a6e2767b8ea9353726d2b06ed11f1591d6`  
		Last Modified: Wed, 16 Jul 2025 06:46:03 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:3cc8489df59e0a60994583c71b0cd717c716c3413aeb8ab2b78365edd94810b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55315683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850d163fa98168a064758a54e0beb55cbbd023fa9177f4c71287aec80bcdb79e`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
ADD alpine-minirootfs-3.20.7-s390x.tar.gz / # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c9d2a262dbe25830d0bf758bbcbf9d2d6289a2b41a504cae662e4865af545768`  
		Last Modified: Tue, 15 Jul 2025 19:00:41 GMT  
		Size: 3.5 MB (3461304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b0c9387c8746fe0c11d5012f72a77763541f6267920797dadedb7f13ebe088`  
		Last Modified: Tue, 15 Jul 2025 23:04:32 GMT  
		Size: 44.4 MB (44376091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c683cae1d442a220bba3b4484764643b87e5f129dd37b0bd949c933da7fcea4`  
		Last Modified: Wed, 16 Jul 2025 08:12:05 GMT  
		Size: 7.5 MB (7478288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e43ebdaaeb51bc2643f9115ad0ad93782204340ec9cba297ef7a85a8fbcf9804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (281021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90d652e1cba68be77cc1cf6a38ae28e4d1989f4d0dd8495a7e6d0bf9346c806`

```dockerfile
```

-	Layers:
	-	`sha256:babb627a71b3d502a71f4a27cce27ce1479b9d43636a57e024689e064790a7ba`  
		Last Modified: Wed, 16 Jul 2025 09:47:25 GMT  
		Size: 271.5 KB (271492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aecaacbdaf894327d23fbd76559a64390998615273b6514735b1e84d0f8cc686`  
		Last Modified: Wed, 16 Jul 2025 09:47:26 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.in-toto+json
