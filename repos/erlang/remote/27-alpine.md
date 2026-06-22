## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:b18934496370cfb5afc40f8cb4d2a1cc61b59891870cb07b4d3727e97d57d8e8
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
$ docker pull erlang@sha256:950ed44d9a4c1226fdfe639c2eaf2b77913040e6adf8d1f17bef27b20d4f6153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53608912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c88695221325d51a0df3291d0f4efe0d22b52ab465db512002e8f038f0e993`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:59:44 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 19:59:44 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Mon, 22 Jun 2026 19:59:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 19:59:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af406eb2139a1a50f7ba3b532a92c75eaffa3df127144588a6355822ab442050`  
		Last Modified: Mon, 22 Jun 2026 19:59:53 GMT  
		Size: 49.8 MB (49821317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:fe0df01e5cdaa234889d12bdbfdfa4c124dd71db1f60cf7e8cfa437abe2a8fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 KB (276287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87399f4fd67d388ba79d5d67ee4ad8914c6378c9dc2ad484b8cc94668122fe68`

```dockerfile
```

-	Layers:
	-	`sha256:85bf8de1f381654b749d481ac263f529490d1469ad167f7ce064a26fccb84548`  
		Last Modified: Mon, 22 Jun 2026 19:59:52 GMT  
		Size: 261.2 KB (261207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39541f669f02e571020bd1d1fd24265b9ed37de0416e2cc20eaa9751941be725`  
		Last Modified: Mon, 22 Jun 2026 19:59:52 GMT  
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
$ docker pull erlang@sha256:46c9b23d522ebbd04cba7f27729bd99e57050408e2e8423368e7bbd6f175dce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53749398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17dc2076cebc5abdb9bc4cc80e9db615108a378ce204dbb2ca10ec17a5f17e91`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:00:32 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:00:32 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Mon, 22 Jun 2026 20:00:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:00:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2954ad2ab8d1204773bc4bc0d21d83b5fc8842395313aeb05cc75cd7354b0e06`  
		Last Modified: Mon, 22 Jun 2026 20:00:44 GMT  
		Size: 49.6 MB (49628912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:94d264aa85aed8eef728719a541ce443fc09a720557e3efb595f1b87c45ffa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 KB (277183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead03b5b763041affc39650bdde64246c45382a183e6a8984475697b48637252`

```dockerfile
```

-	Layers:
	-	`sha256:85b9a679b5610ad1090c51d599e55b26274a4c32ad1181d8361a171f7bbd26ac`  
		Last Modified: Mon, 22 Jun 2026 20:00:40 GMT  
		Size: 262.0 KB (261999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9819b5410c2792fe2095fb5ac14000e2bbe9b5a4400d832530ad523bb0ad6027`  
		Last Modified: Mon, 22 Jun 2026 20:00:40 GMT  
		Size: 15.2 KB (15184 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:a70ea67a958cf2b043e6e745d7f08bdb37bf175767100c2208016347962a61fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51885155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63aab23be95fe80a124c8c29a0c454444e771a85d2c23c5c769ee9e73114b76`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:03 GMT
ENV OTP_VERSION=27.3.4.13 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 19:55:03 GMT
LABEL org.opencontainers.image.version=27.3.4.13
# Mon, 22 Jun 2026 19:55:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="38308102d1f7e44339911ddc5e3a94a6b4bbb0ef8a5fc392e2e4b280daf0fc9e" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 19:55:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a4b74ab0c43260cc6600b37d5a1ed742d904bba03625caa74b18e45744cde3d1`  
		Last Modified: Mon, 22 Jun 2026 12:03:14 GMT  
		Size: 3.6 MB (3605660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17caafd705d1ebed573535e7d48378d988b103279c58af763e94976319ed0246`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 48.3 MB (48279495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:96386eebf01475f197e91761152496f8686970cb8be4eb58dc45ee9d153e7936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 KB (271250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a80df47a32d5cbc8a6b3112104ba28f1795af3a40eb07140fa9d2eeb6f043`

```dockerfile
```

-	Layers:
	-	`sha256:22ecbefcb8f4d08fde03d788194b255a67b7dba0d58571122ba5ce7973ebcd81`  
		Last Modified: Mon, 22 Jun 2026 19:55:10 GMT  
		Size: 256.2 KB (256202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e02163426e9a37df5765ee964916b9ce52506d31f745e4469cf0cb02a7aaee`  
		Last Modified: Mon, 22 Jun 2026 19:55:10 GMT  
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
