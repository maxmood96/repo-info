## `elixir:otp-28-alpine`

```console
$ docker pull elixir@sha256:c4aa6b3f33ad1ee637d2a95f0fb2b322df67ed78534d321b6a92664ffed94a62
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

### `elixir:otp-28-alpine` - linux; amd64

```console
$ docker pull elixir@sha256:5d568e00e3f7bd0a9911ab46188d46137a238107936d317149e9bd963a595a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66932754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2531a4fa0441d56ed75903737e8df133a1177184a9644b41f4810737ef964a70`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:10 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:10 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:10 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:31 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:31 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 20:12:31 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada6b9a4c56e2c69fd1be7c44e0529940c510e740f4d595021c2ab96fe8c35e2`  
		Last Modified: Thu, 11 Jun 2026 19:11:19 GMT  
		Size: 54.9 MB (54928230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbd683f984f1859820f091ac4b12971c7736904b6bff5e8a8eadf6d8f894ff1`  
		Last Modified: Thu, 11 Jun 2026 20:12:38 GMT  
		Size: 8.1 MB (8140335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:6eafabdcc5027b585c33592831c15b14a3b062637a4e1bf707c66bfdd25896f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 KB (293247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2f61b1671072f9b4c056d209980cb291cd5954bc61f4bcee8d3da683870ee9`

```dockerfile
```

-	Layers:
	-	`sha256:0c929a6ea4bc0ca7c94b0e57647f523866ae0002ad629197b44a459871133e77`  
		Last Modified: Thu, 11 Jun 2026 20:12:37 GMT  
		Size: 283.8 KB (283763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1454c009d491c13006fb358bab6ce49e94f3390e3cf605a791a2ea1d538c8e07`  
		Last Modified: Thu, 11 Jun 2026 20:12:37 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm variant v7

```console
$ docker pull elixir@sha256:ce4699d451f19b390873363042090d361d6c58ee7cdf2750f35b343f193e0bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63327218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f781e84cbcf2c9950490d9978e795d760b039d466a02d1a70161df8c3d43fa`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:15:22 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:15:22 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:15:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:15:22 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:13:20 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:13:20 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 20:13:20 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d861e3c381ac06ec4e96f2c499f09233e609ad90bc07faec0f2828a965255fbc`  
		Last Modified: Thu, 11 Jun 2026 19:15:32 GMT  
		Size: 51.9 MB (51904150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6591117f9af44ca720bebee5f7e31488fcd93cbdfce6ad588f22ee7558be7f`  
		Last Modified: Thu, 11 Jun 2026 20:13:27 GMT  
		Size: 8.1 MB (8139945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:e8fc6789387e80c9a39e07fd31e4c5c4a9055cd12c2378f5b2146f7656f1e7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 KB (291444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e0c8222518c05f19a66a19de6424afb541f4d3604527101283f08e9c4b6c57`

```dockerfile
```

-	Layers:
	-	`sha256:4bc461b1412aa339061f3a26a0a1a5bf186330cbfe163ebbfea08c90e81b74cf`  
		Last Modified: Thu, 11 Jun 2026 20:13:26 GMT  
		Size: 281.9 KB (281887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e451481ce4da6adf8941faf7578de00bc6092708ab5174232339dc9ed284d`  
		Last Modified: Thu, 11 Jun 2026 20:13:26 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:6b9e95a15244260b5833463f0e3e994419a528dddc0f38516d74d01adb495434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67364716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a6be4a36915083c5b7ac5dfcdcbf4281654e0b2d326dc4aa558ffbb9677a06`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:29 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:29 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:29 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:13:02 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:13:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 20:13:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03748567d51bcd0021b967f2bec05489cc396c50a2625b148f5b6a6ead07fb89`  
		Last Modified: Thu, 11 Jun 2026 19:11:39 GMT  
		Size: 55.0 MB (55024483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d3ae55cd6a59268c345c539c84317bf9cfd0538646f483d3ce790650d0e55d`  
		Last Modified: Thu, 11 Jun 2026 20:13:08 GMT  
		Size: 8.1 MB (8140363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:9de60fefec825e2af9b7c237f24cf014a7b123257095581fa7221fe45c301d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36848af64704837fdd503fc26a3b61eac232ede84a50c6068d824f34fc40b7d3`

```dockerfile
```

-	Layers:
	-	`sha256:d30d4ceb58968f20a80254e0a1356ce65a1b044f4281bd03ce098ccd68eb9e39`  
		Last Modified: Thu, 11 Jun 2026 20:13:08 GMT  
		Size: 283.9 KB (283893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ab104e864605a1ba05972758508f58439de0b914e26c4ffd6d6b61aa05e85e`  
		Last Modified: Thu, 11 Jun 2026 20:13:08 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; 386

```console
$ docker pull elixir@sha256:dc64b22bf8e47ef8b2e86d2ce26fc91951ad46f61e2e4b97cdc99d93e33c3821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64926225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06bd1bce673d5db054f88469118d8532eb87db128b31f8123fcacc22bc12e57`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:11:32 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:32 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:11:32 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:13:13 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:13:13 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 20:13:13 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31bde4e5c11589a4a73a0ea21b17c4d5af54483e6c10e1985e7830e3b9cef04`  
		Last Modified: Thu, 11 Jun 2026 19:11:41 GMT  
		Size: 53.1 MB (53095948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d6adc0da9d3d7d7c7be70dd527d136954cd9bfccf608091ecf5ef03155d5b3`  
		Last Modified: Thu, 11 Jun 2026 20:13:19 GMT  
		Size: 8.1 MB (8139831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:9c40b8caf31b425c945f6d58222c16928dbfdc4e16b17a8197609c51b912da51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 KB (288221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d538522f67d49b15ff27ce706535a143b530093258ed793fefeefe5054e50607`

```dockerfile
```

-	Layers:
	-	`sha256:ef3cbfb8ac51f1f49e567e0c50e85bfccbbbf5b2b1257f25424130a76a0b2462`  
		Last Modified: Thu, 11 Jun 2026 20:13:19 GMT  
		Size: 278.8 KB (278763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388d413fd55526432763a0cbb10e570830da0f5f49279175d0b30ea3824ac76f`  
		Last Modified: Thu, 11 Jun 2026 20:13:19 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; ppc64le

```console
$ docker pull elixir@sha256:597add7e2700af7fd677b5e4e3f97d952eee03ee1095632717ee1946024b0264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65422084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c94c43e46c2a1f5c62b98c08c893da406b9760ea8474b6eb1ed96c3d33bd0b`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 21:10:10 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 21:10:10 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 21:10:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 21:10:10 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 22:18:10 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 22:18:10 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 22:18:10 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81bb4d8310e0c978a63a8147ffcd0e280b8690000b2c66c17f6058093486e44`  
		Last Modified: Thu, 11 Jun 2026 21:10:28 GMT  
		Size: 53.5 MB (53451308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2771dc5864a99163d2170b1d2207ce10e7aa512f4020fa5b486c007e2a233a86`  
		Last Modified: Thu, 11 Jun 2026 22:18:26 GMT  
		Size: 8.1 MB (8139847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:16823c477df80933975eecffe39b704fd82cf3c4be64c90f2ed08d06dee89830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b5de54e996dd886a429194930dbba682bbc83fa7329aa53689ffdbf7ac6c8f`

```dockerfile
```

-	Layers:
	-	`sha256:ca22fb76eb414d99b127d3a6c195e60cbb054620cb420cf48d5f93f3b639bb62`  
		Last Modified: Thu, 11 Jun 2026 22:18:26 GMT  
		Size: 278.9 KB (278896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e8e9f3a17306e4a52176e4bf767e9044484e23ffe9d9c4aa978162d70d0b70`  
		Last Modified: Thu, 11 Jun 2026 22:18:26 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-alpine` - linux; s390x

```console
$ docker pull elixir@sha256:cc93b819d5133d28e3eeaab2fb6af268e2a81734bc3d9d6aeb7167cd75826ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64849287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70aefc12fd15b74ca0f79e9f53beda9b864149634b326ada1aafc8b432bb2976`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 19:16:06 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:16:06 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:16:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Jun 2026 19:16:06 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:14:15 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:14:15 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apk add --no-cache --virtual .build-deps $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apk del .build-deps # buildkit
# Thu, 11 Jun 2026 20:14:15 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d357352d8ededcf8f27c1aafd7d1a92beb54f3a5850db2c675568e3b004185e`  
		Last Modified: Thu, 11 Jun 2026 19:16:20 GMT  
		Size: 53.0 MB (52982964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a47163f00d8ec28d623f702cc192ba893d7c8fc1640610c298f254f394d330`  
		Last Modified: Thu, 11 Jun 2026 20:14:25 GMT  
		Size: 8.1 MB (8139791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-alpine` - unknown; unknown

```console
$ docker pull elixir@sha256:68c972785c24304545ed68dd24dfd2f00a683e31c4695356139da9de3be0727b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15aae869fe2efe47a47398d4899b407e7242be0331091cde7d6b2599aae677b`

```dockerfile
```

-	Layers:
	-	`sha256:ac62fa6c45586d45096a9084f9dacf8319cf91cb9f2429f14eab4e94608b5a36`  
		Last Modified: Thu, 11 Jun 2026 20:14:25 GMT  
		Size: 278.9 KB (278868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2779d6065c716cce1ef92f4d06404c500ed57f3387e32d4b2827f20a357f6ef0`  
		Last Modified: Thu, 11 Jun 2026 20:14:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.in-toto+json
