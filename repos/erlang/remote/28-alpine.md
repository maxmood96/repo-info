## `erlang:28-alpine`

```console
$ docker pull erlang@sha256:d6fc78fcced35ec52a471a44572541fb9a8cd68a2133fa41cff6485cc7f247d1
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

### `erlang:28-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:83ea60d41cb661e12933fbc61f1070fdcde616f235ee73d4721966cf7b96d12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54344951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d94526aded0b3b1f53c5737d186b61315ae5047e49eab250692fbeeeae1938`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90423016e416aa99e2e6dbc2619a5a245409dbdec85c35566e3ab52decad6da`  
		Last Modified: Fri, 09 May 2025 08:13:59 GMT  
		Size: 50.7 MB (50702704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cdde3d22fe8bd1208418e375856d2e1fd39147e0c78f6f098b9dfd9ee2eae56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 KB (291562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63e55251568b39d49febeb9d821a8495d4853be58a3fca44d7c7949d389b5a6`

```dockerfile
```

-	Layers:
	-	`sha256:3eaccaa56ad9a170210b11e1474593ae8c05727371dd9d75dafe3c8b68718128`  
		Last Modified: Wed, 19 Mar 2025 22:58:41 GMT  
		Size: 276.4 KB (276434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f208a24ee8b3af9e460974ec40bc02ef1c580a2eb609af6861d341ec929f26d6`  
		Last Modified: Wed, 19 Mar 2025 22:58:41 GMT  
		Size: 15.1 KB (15128 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:60e9cb7ef6efa4e69b97265d491d24c47ae9d3d289829a6d04e3b37e5330ecfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51375965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7172763edaf0d9d3f0300a37c071c924bf3491236ea9883fb5cd7495f5b38133`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea53373ef8c14e4cd996df1dc41df23a7780331f30632a04c201fda18d82b5c`  
		Last Modified: Wed, 19 Mar 2025 23:10:12 GMT  
		Size: 48.3 MB (48277842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:18410cffbd78afbbacce8a0c1abf89c8f5821cc38f786820b256ce8745881e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 KB (290593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e0dc92e41caf6c775654afa957079fa23b8d74599b3f3dd4d0c076f198443a`

```dockerfile
```

-	Layers:
	-	`sha256:89fd711af76e3d3a6881f7bbcdc8c620f9da380c423261c0f74ba5966afab15a`  
		Last Modified: Wed, 19 Mar 2025 23:10:10 GMT  
		Size: 275.4 KB (275389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54b8e58eee3daf6842abae40da14eeb2867b5ad78357f1736dbe6c574a37043`  
		Last Modified: Wed, 19 Mar 2025 23:10:10 GMT  
		Size: 15.2 KB (15204 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b449c1645bb8064f4e57bc245eff1c072d960e7e0be1d0fb5d69672d24fe8607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54439609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebbbe8a81a5446624bb7672159326e3c99e76e737cf5c7c98210ebd532955e5`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a6ddeaf2ec9e7bc19c53ef202b343e486a112fdb40e3e7e14671c0143c7c11`  
		Last Modified: Wed, 19 Mar 2025 23:04:07 GMT  
		Size: 50.4 MB (50446580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:370515a93222844e2acf77f4ba6bf482d35d0c6a2955d032c3c5c76bfc423cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 KB (292453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574a3554829e51955d514fc9623e70ea2b30f7651cd703697f97157ffd422c5c`

```dockerfile
```

-	Layers:
	-	`sha256:b96d03dfd0140ebffadc328b48bcabe1a1251aed27755b2e9d2bc68d2c4748ca`  
		Last Modified: Wed, 19 Mar 2025 23:04:05 GMT  
		Size: 277.2 KB (277222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420862896029a754ae6ee145de27e5701a6b7bf03ef4737bb35fb9c5ece67529`  
		Last Modified: Wed, 19 Mar 2025 23:04:05 GMT  
		Size: 15.2 KB (15231 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; 386

```console
$ docker pull erlang@sha256:bd1725e45d4158393b54dc485b3175bdf1f1ec3c3faa753679b66209aa41ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52614544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac3edb7053fcdecf5290184369c401a01b5e7374cf23c55c4bb851c100d124`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cc13fcfa9bd7734e76991bd8e6437a6368d4c56e9eb2988885a2a2855cf7ff`  
		Last Modified: Wed, 19 Mar 2025 22:58:32 GMT  
		Size: 49.2 MB (49150921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cb8f1a0fea4712608de76b3703ef0461dfaca4e9ab487da5428f934ed17e52ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 KB (286879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a46a464eb2a8cdf7777f3afe349eb10e406975136cc67797e76b72c524f8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3f4dcd01d438d025d7eda0c2d80ad5b3418ce48393ecab148d6f7a73a783c79b`  
		Last Modified: Wed, 19 Mar 2025 22:58:31 GMT  
		Size: 271.8 KB (271783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404d898b61fb528116c3575b4884908e149a6aa225e2cd6d146c9287801da581`  
		Last Modified: Wed, 19 Mar 2025 22:58:31 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:657aecad0f7015d5829fb23501597ae6994adf0eb866f60f4477adcd12a78953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52856509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a1d8a83a6e6d23bce9a2a8177cc34be8e4c8a6925255f792c53975cec617b`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81cddbb00379e3b3c6a33f12878c20f073c4caaff42c80b3b72657e84da481c`  
		Last Modified: Wed, 19 Mar 2025 23:01:28 GMT  
		Size: 49.3 MB (49282164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cec57686f3aed34e2fc4a49aa3c6b6a2dc13de1bae32ef0abf57715bf1bbb225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 KB (285795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9330e9abc9aad5d356e807245fb5bbfacab98c8812a4de2527b3d75f265965c4`

```dockerfile
```

-	Layers:
	-	`sha256:8016c6cfff1c870cfe7207073be834a31e18cae53fa4e9f90fad41d122dffb79`  
		Last Modified: Wed, 19 Mar 2025 23:01:26 GMT  
		Size: 270.6 KB (270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b162193711f41ed0abc5648a6162d8154e005a5ab9adac7ac1a0fded2b52f581`  
		Last Modified: Wed, 19 Mar 2025 23:01:26 GMT  
		Size: 15.2 KB (15172 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:adb663c1eda2cf4b66e035d5397caf5e22e21a8a845384d11e4bcd3f6220ce0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52414214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669e13e50094a4faec5e53783a1ebb8d279444feea19a95e4df2cdcf2b3332d`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38552e4b94f957bf46453fd956ee4a0c085e0d93e42ddb5048b65a744a7be921`  
		Last Modified: Wed, 19 Mar 2025 23:24:10 GMT  
		Size: 48.9 MB (48946647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:03f4e0bba3987ebf33d64653ac2c52547390edeac71f531ba0a6afc8752f947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 KB (285716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8293396ad7f1c206104a93cd13f1bac898b5be15d1cfa0e4a8c2b2cd5bd1088`

```dockerfile
```

-	Layers:
	-	`sha256:98fef9f99c2d90d793f400c0e14a273482f1419e44585eb14ca68073940db5cb`  
		Last Modified: Wed, 19 Mar 2025 23:24:09 GMT  
		Size: 270.6 KB (270589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b02a02f720b9e2e0e0c46e41cc0751fa9eb845e6bdeaa98670b168d7f4cd89b`  
		Last Modified: Wed, 19 Mar 2025 23:24:09 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
