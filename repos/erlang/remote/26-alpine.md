## `erlang:26-alpine`

```console
$ docker pull erlang@sha256:9fee309a2e6bf2b8d2d07b31892070b7a52e2842ec25146a80f7924e9a327b8f
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
$ docker pull erlang@sha256:1d3e7ee49ee92b7b60101503d0a26110ed67791480f3f7877bfd81fbd13ae1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51911439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5733ff1379ea1ea299462e0a097e9b0da2372ad41a94267353103137cf7ceb`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7f6093e8f19c41e3b91fa09219941e30bb0ab528f83d9d1182f4e9980f9d97`  
		Last Modified: Tue, 12 Nov 2024 02:46:29 GMT  
		Size: 48.3 MB (48287535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b1bda6099260911a264ccc2ab411bb3c30da70fb128f4949716d0dab8d21d442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 KB (286697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed65ae19e7a40885ece69171d4c645a09143ff3b1777a0e6731c30df08fd49cb`

```dockerfile
```

-	Layers:
	-	`sha256:184ce10279191a344190e00b8e7b2df862bcc38547bbbeca1f485e8e00821730`  
		Last Modified: Tue, 12 Nov 2024 02:46:28 GMT  
		Size: 271.7 KB (271655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef04a77aa2fd013d585bb5cf1fdbfb138b576683a69964d409c3886e20d16ce`  
		Last Modified: Tue, 12 Nov 2024 02:46:28 GMT  
		Size: 15.0 KB (15042 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4ecf73733b6921d7baaf259893c2262d12925d93795ac567740dd1c1e71d5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48567509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df52a3e0e590af0464f3276ad4eab80e54e496d110e7ea48bfff878933405d2`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a307f88bbc258d8a5480fa0d0a7f9ff76bdd10401472b74fb07450e1a7f972`  
		Last Modified: Mon, 11 Nov 2024 20:06:11 GMT  
		Size: 45.5 MB (45472007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3ce5a3a65c5bcf2eeb11664b2bdc49536430ae8e66654a5a26e73ee6bf33f771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 KB (282627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e32dc5215a73c7cebe0e957fc4bc4400a07b5990d22748ae4f730b2c6a79a`

```dockerfile
```

-	Layers:
	-	`sha256:53fafde6458c7eb1df755893eb983df4c25af8c10acffba7dc7c83de0434a66c`  
		Last Modified: Mon, 11 Nov 2024 20:06:10 GMT  
		Size: 267.7 KB (267725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f74458a1e2a7ebd783fa89e5e327607bf03060c5d4a80ea2c084ac329960675`  
		Last Modified: Mon, 11 Nov 2024 20:06:09 GMT  
		Size: 14.9 KB (14902 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:e4063b6d062cf32f0fc070d567ca13356dba5f4577a24bdc7234802ecefa130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52578130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f884f099e32bf2dba0b29de967c7b8e071516f21b84b8634803c740450e571c1`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8d3892825bd313a51ccc633ac65a6033912b93b38e232313dc2c61d7cadc8d`  
		Last Modified: Tue, 12 Nov 2024 11:44:53 GMT  
		Size: 48.5 MB (48490404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:bf1769f11722d8a32084a425f6f517a5fee3aa6537e7e2685fe1000bb3e492e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 KB (287595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f082beb39088dfe262e60102546f06f9f10786e4f6bd7f982c1a4e1c5a2d559e`

```dockerfile
```

-	Layers:
	-	`sha256:c753e3ecefd3fc7993fafef745a9f8f8100866cfe69f9ca4427cd839ff0c300b`  
		Last Modified: Tue, 12 Nov 2024 11:44:52 GMT  
		Size: 272.4 KB (272448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6532f6678c6dd31abbbfb316e83b56394894f6b668de2cf4072f24aa88c6facd`  
		Last Modified: Tue, 12 Nov 2024 11:44:52 GMT  
		Size: 15.1 KB (15147 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; 386

```console
$ docker pull erlang@sha256:bd7e00ef03e4ba42ed70d67e77300a7a8c9ce3d5e924cada633a6fe93d9fb972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50189611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a946dab2531fc7106b99d36bd384959cae9e4ef250d454911973e44744ec6929`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84059e6d65821613b15631478b48a43f6a9af3d6c3e3cc9b8bb4b92e4854f2e6`  
		Last Modified: Tue, 12 Nov 2024 02:47:52 GMT  
		Size: 46.7 MB (46720392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8d372d9f76ea448bd8ded620305420be21f9b429e0113401120e6806a062b454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 KB (281937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbedbb9ac07def7d7aa3b00e4161bb526dcde3486cfdf63504b8938901cef6e`

```dockerfile
```

-	Layers:
	-	`sha256:00a284c77c6ff6ca38233790126db9024abd6857ff322c273905ba5dfe5da71d`  
		Last Modified: Tue, 12 Nov 2024 02:47:51 GMT  
		Size: 266.9 KB (266927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dff0bbe61e3cf3e14342775dfdc6b3a3f1633e3656d700402e7fa728400e224`  
		Last Modified: Tue, 12 Nov 2024 02:47:51 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:70ae2058c25a9580c9e982ea59ef130d8571cb727b2216000c0d4a711e2d698e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50379943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fd9fbcb470fa75c2dd7a694a69e25bc7494b1d4a30617816bddff1259fe75`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363b577ff6eca4f9ccfcf84512e9091169eb59ef70ab084dac27c858572b735f`  
		Last Modified: Tue, 12 Nov 2024 08:57:51 GMT  
		Size: 46.8 MB (46807484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:14a96f9a771fa148dd0e3009e91d33be83a284e6e9f104194196c2733001129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515dd3b4a7c8ccf39bbfb75ae7782700ea01c5c57eb81da807a90863a30026b7`

```dockerfile
```

-	Layers:
	-	`sha256:75d789afcdd18b40bb4f3c558248f509960985b812e148cff1315cf935518349`  
		Last Modified: Tue, 12 Nov 2024 08:57:50 GMT  
		Size: 265.8 KB (265769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03854043da884469bfed8c648aecd96c84bfb7adf499e51240954d93f7d62b17`  
		Last Modified: Tue, 12 Nov 2024 08:57:49 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:24f5053dcbfd36bccd945c160030a1b8d76966a100cbaed481e736722cb4e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49810072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8f8345c29412dab2df479e75d5e3e931fe556024838711c53e3f23e46cdb96`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb23d1d8fb8f245a67327704c349e7273b15f84b7e123d8c9cd2aee089f727`  
		Last Modified: Tue, 12 Nov 2024 09:34:10 GMT  
		Size: 46.3 MB (46348464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:31b2effe067bd6e110c0f71b77fb970b37f7073ab4d53225371bd8f5f99bda3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45773e2025722d10b9334900d6fce6b3580d36d959517b7e91ac0d717b79f729`

```dockerfile
```

-	Layers:
	-	`sha256:87339f213f5073622c358cc4390cca23dbc4f56dd4826ae58efe6f6f86607095`  
		Last Modified: Tue, 12 Nov 2024 09:34:08 GMT  
		Size: 265.7 KB (265735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced134adda93e9da21d6499c5b85c58b0d41edac39a082477f51476a42f51226`  
		Last Modified: Tue, 12 Nov 2024 09:34:08 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json
