## `elixir:alpine`

```console
$ docker pull elixir@sha256:06336162f203c05daaf60296e38af081380a44991ba9377ca62faec347677aac
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

### `elixir:alpine` - linux; amd64

```console
$ docker pull elixir@sha256:7ec17669bb8420fa6fc782264ff2ff0ee0912b1186155f3a0de8e415edb5fb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64075555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd1fd87a09da403c9a3268160446e166a570fab8b48da8733beb57c333d0035`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:46:54 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 17:46:54 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 17:46:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 17:46:54 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 18:12:39 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 18:12:39 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 18:12:39 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61897aee849ed558e84609bad35595906a3d0469dd1998feeb3e73ac6996907`  
		Last Modified: Thu, 05 Mar 2026 17:47:03 GMT  
		Size: 52.4 MB (52427804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe75536ad26f547a91862a617a895573d61062e4eda379166cadd155f136def`  
		Last Modified: Thu, 05 Mar 2026 18:12:45 GMT  
		Size: 7.8 MB (7785930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:a6453198490cd35424664c1538eaff9faf2fcfb9f5811f498b06a0dde4be4463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d85cace0e62650e3148600804f01a5081052358da5ade5a71aa1cbbaf64da1`

```dockerfile
```

-	Layers:
	-	`sha256:03308e860a33969ca90909ff593a3a9a52ede76f02f98894b283e245bdeef129`  
		Last Modified: Thu, 05 Mar 2026 18:12:45 GMT  
		Size: 286.5 KB (286528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9eb094c4deab258b716d106b61cc8d605fdc394d76ff39a3a0e7491f121a22c`  
		Last Modified: Thu, 05 Mar 2026 18:12:45 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:5fde5d698cf2a34547e4b43000533e440aa4b48191f9a2b1506967b8acd0ccc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61004609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386215004f3d00251d44f170cc91e5ed44f21ae96fe57c1205746100d2f01358`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:44:37 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 17:44:37 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 17:44:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 17:44:37 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 17:48:50 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 17:48:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 17:48:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4786c1c78c7877aa60f704c11ba3991b1f53977b879e7b06a09b0e33f524b748`  
		Last Modified: Thu, 05 Mar 2026 17:44:45 GMT  
		Size: 49.9 MB (49936959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c95c5792860cd7cd98176fc8eb5386eef9d69c58e97a4e15dfdbde2cb274cb`  
		Last Modified: Thu, 05 Mar 2026 17:48:57 GMT  
		Size: 7.8 MB (7785926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:ec581e43ed826b544d8de02f5f6676c80b8387fd78a8b9bce47ef58d91b99ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 KB (295153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492cebe8c2595d0d0cecdd7950353e7d19639b4a112640fafce69d415a041727`

```dockerfile
```

-	Layers:
	-	`sha256:6ad80ccfe4cc23803666e6e911f605e4bea867326d80d086c3484c48482f4151`  
		Last Modified: Thu, 05 Mar 2026 17:48:56 GMT  
		Size: 284.7 KB (284672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e866ebfd204e24d2111f790f658f704b67b7a57e7243d0f73c1c43d718635ea7`  
		Last Modified: Thu, 05 Mar 2026 17:48:56 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:aaed3d456eecefab7ba86b915095e787a5a61d7a51bc1afa8f7e4909472db35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64220276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73000067a1a6cf3b880cf695310790625f098ffe04b71d9c1be3c49b2cab7b80`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:45:58 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 17:45:58 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 17:45:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 17:45:58 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 18:12:24 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 18:12:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 18:12:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899aaae824450d9e41b092a3c956c0557123e2f41b454722419722e46a160d40`  
		Last Modified: Thu, 05 Mar 2026 17:46:07 GMT  
		Size: 52.2 MB (52237242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f41b9435938a0b543b87bdcea92276e6ce09d4c17acde9b3f6c95f1ee9e39d`  
		Last Modified: Thu, 05 Mar 2026 18:12:32 GMT  
		Size: 7.8 MB (7785943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e169a8b65b92c671881740c8b780b04bd829288edbbca038e21ed3b9b3c9d832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2c9212c12ae2d5ee413a5f00f9aefdc83f7ae36503f36d3830715fd45a8692`

```dockerfile
```

-	Layers:
	-	`sha256:b7982d672fa101a3a1587be4f41e339ada1c3dae2a26cecf816de044021021be`  
		Last Modified: Thu, 05 Mar 2026 18:12:30 GMT  
		Size: 286.7 KB (286690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce61762f207762075ed57bd0c10d0189007791e13875223384fd96f3cdad4700`  
		Last Modified: Thu, 05 Mar 2026 18:12:30 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; 386

```console
$ docker pull elixir@sha256:c85c102ebdc0ef8bbe726a910870e02ed2f5edd8ef5fc6dd6c07336a85127811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62259765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9a5581806d6c9f00b3fa7ca51b5962695ca04f4cda6ff1042a9a3c87826a66`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:45:16 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 17:45:16 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 17:45:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 17:45:16 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 17:49:01 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 17:49:01 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 17:49:01 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d0b48fa62bef1ed052dfe03fce8cb09043c5dab1960801b8e7bc2100a90220`  
		Last Modified: Thu, 05 Mar 2026 17:45:24 GMT  
		Size: 50.8 MB (50786981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5d60cf20329138a3459589cdbeb11470e54530f54e0bb1d1c5008d3b99e94e`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 7.8 MB (7785786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:02e7d8b8d61e04d46e4c9da158cca411baf5e2d2e85f1a55d6556c852d0a38aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 KB (291856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5234faed16253616013e6b2655f047c40ddd004279a9629836c76ce7979828`

```dockerfile
```

-	Layers:
	-	`sha256:e6b907913a08d003c16cc819f88df58abccaa20ba356e3ae232a5dbacb8b2430`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 281.5 KB (281513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb994e09cd1abfeb564a51f55b75640daa27f8c62be3c8a7d0d67fbc2189080e`  
		Last Modified: Thu, 05 Mar 2026 17:49:07 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:fea3de1645b1a8af127d702d2d5af8edff9afb42c88eb320a0d72ce85dac33e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62697612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6e7236c92e6d7a16ffc10fa8d0803aeb10a3eb406a44dfebd5874bcb564541`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:00:56 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 18:00:56 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 18:00:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 18:00:56 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 18:14:27 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 18:14:27 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 18:14:27 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09ae64d93048a90259216726ff8b5491ea4510194105b1e2f9d45b1efc1cbf`  
		Last Modified: Thu, 05 Mar 2026 18:01:15 GMT  
		Size: 51.1 MB (51082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d500b7090821e68386f8b8372ed7c5926f3cf2a755eff99df67caa224024fd`  
		Last Modified: Thu, 05 Mar 2026 18:14:41 GMT  
		Size: 7.8 MB (7785894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:90827fea883fdb4e1aab71ce13f2aab08eef16299537a2bb7a2d957a9cf36b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 KB (292116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669950c61fb6151908837d6fd003147c1b8dff81bca8c5e973e3352171e74016`

```dockerfile
```

-	Layers:
	-	`sha256:0414184b18283f882394e64d28ab4dede2991c98dde515efd0fff96842cd1e45`  
		Last Modified: Thu, 05 Mar 2026 18:14:40 GMT  
		Size: 281.7 KB (281675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5882d64467f8dd7406ee94ebf72a0f977a2ac12c832ec540b1d683f336270c31`  
		Last Modified: Thu, 05 Mar 2026 18:14:40 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:alpine` - linux; s390x

```console
$ docker pull elixir@sha256:eec160143b1837b8f0cb7c868308765b960a03c7b965c02189809c1c6f5c94d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62218479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67962155d7334c749da6298eef7c9290d80b84fe3e617015ae2ece1236049fc`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 17:51:38 GMT
ENV OTP_VERSION=28.4 REBAR3_VERSION=3.26.0
# Thu, 05 Mar 2026 17:51:38 GMT
LABEL org.opencontainers.image.version=28.4
# Thu, 05 Mar 2026 17:51:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5b39ceb3e36de8901dde61e88869e47be1b81bd56928da3986c196d696e1311d" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 05 Mar 2026 17:51:38 GMT
CMD ["erl"]
# Thu, 05 Mar 2026 18:10:48 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 05 Mar 2026 18:10:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 05 Mar 2026 18:10:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb8511c00f3cdf28dd4713d6f29c846d483e9dda3c4c47e0c19b0456f2e2f72`  
		Last Modified: Thu, 05 Mar 2026 17:51:52 GMT  
		Size: 50.7 MB (50707356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cc4e2adbb6b2e93d36ebbb65caa04ab128c18f7a99d852f0ea922084a070f3`  
		Last Modified: Thu, 05 Mar 2026 18:10:58 GMT  
		Size: 7.8 MB (7785790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:982e9b396c873b97622b86240ad43cca776d5da5b07bf0c82f52cd1e69805ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 KB (292014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb375e4ece6324fffe9209e5aa7f0cb757212bdde576c3709f25593817fb99`

```dockerfile
```

-	Layers:
	-	`sha256:3ea83222c7e1a765c482643c38898550d71db2f1bb93b29874109d30d4b9942c`  
		Last Modified: Thu, 05 Mar 2026 18:10:58 GMT  
		Size: 281.6 KB (281629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1072d3ca86332d0655bdd631d893c95d7790c587308ff89374a09589b54da85`  
		Last Modified: Thu, 05 Mar 2026 18:10:58 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.in-toto+json
