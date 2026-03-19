## `erlang:29-alpine`

```console
$ docker pull erlang@sha256:bd9d35947528d69b1fd5af4aa5af411e09c2b64d31c19e3e961e7d9e21527e85
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

### `erlang:29-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:44569f863d94916d947da98d5cad9ba83749d83832f11fe13f78d8d6c52019df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56956389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7763157f57b834ebb32228ac7704e9c2215b3eab51e55d87ea8425a6a4b104`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:29:04 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:29:04 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:29:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:29:04 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af64a5e7513896513ea6aa6636a870613ef7ce3343525bedaaf949dc0fc32d77`  
		Last Modified: Thu, 19 Mar 2026 18:29:13 GMT  
		Size: 53.1 MB (53094568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:c71c0d02543d0b267dfa7911af62e7864d4809ad6bd91bc8fd87de017442cad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 KB (294080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c49a392bbc6d141df166d8ffcc5f1abd38057481b4003d1b98768ef4d794c8a`

```dockerfile
```

-	Layers:
	-	`sha256:6a38bbdd63f7784330d8b5dd5c4c140533afdb575fd30b65d1c2de8f98922b5b`  
		Last Modified: Thu, 19 Mar 2026 18:29:11 GMT  
		Size: 278.4 KB (278450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9caffbb8ca11e436d67ac57c23f4a7eec33b334afe90caf591081fde63e0a3`  
		Last Modified: Thu, 19 Mar 2026 18:29:11 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:aae24d5e80738692fcb61f63e1bd4c1ce0e4b700c0744e434ec21e870f5d743c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53903763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bba5a37597582a9eecccc451c450a3659d54a67cb544b5cd2e987e5b348a224`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:26:10 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:26:10 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:26:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:26:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda15c30eeaa5315a0a689ed9813dd7f3269a99e29f5fc1446676f4ae2f03feb`  
		Last Modified: Thu, 19 Mar 2026 18:26:19 GMT  
		Size: 50.6 MB (50622039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:52fb9cace75dff604576245f9223ea4ebce725c905847378d16e128b555f0a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 KB (292288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5c1e6a563a1d8e6ee790ef3bdac0071655efbae391d5b2c5f52a7d2da196e`

```dockerfile
```

-	Layers:
	-	`sha256:203d69c778c876bbe9a92cc7ddebfc1009797d70fc67a1ebe218f130c53fa3d6`  
		Last Modified: Thu, 19 Mar 2026 18:26:17 GMT  
		Size: 276.6 KB (276578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:141c45b3c64988486184ba3813282793c52664ae91d7d8a292b460923cd48f3f`  
		Last Modified: Thu, 19 Mar 2026 18:26:17 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb1a92e33874965bcc77c1fe5e7c8b8ceaf3c5585482b5b214780304321bce39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57091751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195b8ef83b3103a445fd0b5316bd20057c5a0f4b9075a9b597cdeaa219981d17`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:28:58 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:28:58 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:28:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:28:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64ecc0a717e38f07090ca7251251b5fbb55a73ca81d3b954ca81b8c69122ada`  
		Last Modified: Thu, 19 Mar 2026 18:29:07 GMT  
		Size: 52.9 MB (52894660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:4306109c9de8ed67fd46d50f1d4f9c395b8ee1f47668d3c369932ea8f9544b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 KB (294321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fd426962115f55a5885a7dcb89bafcdc05b0ec2e98072c4d305b93fc95d8e9`

```dockerfile
```

-	Layers:
	-	`sha256:0bc35330c7febe716c555c59d9d6cd26625f93b5d92565ff557c21f4081d58cf`  
		Last Modified: Thu, 19 Mar 2026 18:29:06 GMT  
		Size: 278.6 KB (278588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd597cfb345df490c185ad91a77f74f0ff31585a6650795980f60c4a600fc15c`  
		Last Modified: Thu, 19 Mar 2026 18:29:06 GMT  
		Size: 15.7 KB (15733 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; 386

```console
$ docker pull erlang@sha256:ee9d81bb2ab3b4796b4ca1ec6917d9071525f503b5bab03cdd17c7997adb23eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55163426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344a89f10d8b9000633f7fd199f5795b5fe9e40358330d66666449fb123aabcb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:29:26 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:29:26 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:29:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:29:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b7861b88a74471e540c1636c41838ec9462aa4a90aa571b08baca73999148`  
		Last Modified: Thu, 19 Mar 2026 18:29:35 GMT  
		Size: 51.5 MB (51476428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:bae7eb26a033d3b1f88add598d1ffc724d8484abf301b307aff35b3b374c0a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaeb33dc6b54bf59f9bd8e0f94e7f80316efa92312c35d3fdf4fb2bc3f2d566a`

```dockerfile
```

-	Layers:
	-	`sha256:6920e63518a3c5bbcf86db0a61c0e897a567bdc3ec686969519a549570389eb4`  
		Last Modified: Thu, 19 Mar 2026 18:29:34 GMT  
		Size: 273.4 KB (273445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbd8dc3553db6d9732d36d502e514883c01cf73d8ef718689c335500a9e8eeb`  
		Last Modified: Thu, 19 Mar 2026 18:29:33 GMT  
		Size: 15.6 KB (15598 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:bbe5e509dae1e239e8774fafa0c94856cc6f2f5fd3a1ca14abbe7d4762b95b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55607731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14456a18eb901301f5ffb1bec295c5e019236ee35732b34b04dc93124147db0`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:30:18 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:30:18 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:30:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:30:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8cf8232d5e29fe1de3763f7075b3c469d3b890209b59e56a533cfd7b9f88ee`  
		Last Modified: Thu, 19 Mar 2026 18:30:32 GMT  
		Size: 51.8 MB (51778088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:9c87e1e1ba218b8dfe8c02f590573a57da2e4ebd63dc9750781995dbf42c054a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 KB (289259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ebffd6a025c9051ae354818c6439de4f339020933111674192a5368e4f54c9`

```dockerfile
```

-	Layers:
	-	`sha256:a54ac54e4352f3c3ace060a3b0bede2ca19b566089189f0b85f97fc0dceffbc7`  
		Last Modified: Thu, 19 Mar 2026 18:30:31 GMT  
		Size: 273.6 KB (273585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d7d15416aef1bdda4eb05c61524358714d00dbe82c06b23d4bc335e9d401d0`  
		Last Modified: Thu, 19 Mar 2026 18:30:31 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:f64a5a372d620182126aa71fc5dd15b3c7023bec4efcff04ef392dffddf8648c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55129930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710ac0111a0f7b03a36cfd7085ef7371a34e28c1b10ff8f0b48035eec538b714`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 18:38:43 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Thu, 19 Mar 2026 18:38:43 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Thu, 19 Mar 2026 18:38:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 19 Mar 2026 18:38:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082bbf76cdaea3fd32816e21e1fe1e9153334f6e1d0cfa1e98258a0a981af302`  
		Last Modified: Thu, 19 Mar 2026 18:39:07 GMT  
		Size: 51.4 MB (51404597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e4162299f1c569721d1abf1bac3c9cf79d955632978ee0887193a8e1ded6f497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 KB (289180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b92fcf032309197eb9f1b869315b08726cd28b5c3955a3c8bddb9f84af6296`

```dockerfile
```

-	Layers:
	-	`sha256:3f10031aadcb24ad85bc8415661b1548b8ba46badd3a5731727d9fc6d2d0aaf7`  
		Last Modified: Thu, 19 Mar 2026 18:39:05 GMT  
		Size: 273.6 KB (273551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16af5019fdd0a1298c3cf7f4a642179d2e81942fea9cf153234568329e7ca4c`  
		Last Modified: Thu, 19 Mar 2026 18:39:05 GMT  
		Size: 15.6 KB (15629 bytes)  
		MIME: application/vnd.in-toto+json
