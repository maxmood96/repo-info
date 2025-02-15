## `erlang:alpine`

```console
$ docker pull erlang@sha256:1cdf4b95b273aac99e234ee664c87ae35a61910ae6457e3050606ea4a202fb5a
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

### `erlang:alpine` - linux; amd64

```console
$ docker pull erlang@sha256:6200e8337a1769589124e5b7634c46cc5c73958831a83524f9b57ec253c53c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322d6b0d57b7efa971b84b90c9abdce9fb5eb68753802d576f4531730dad8b`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bb7ac995b9a4bc6ab2d55c68dde6a83facc4e61797deec31644a00e2d64471`  
		Last Modified: Fri, 14 Feb 2025 20:39:13 GMT  
		Size: 49.7 MB (49662452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1338fe749b93f2150550241f7ce4e08d0168f01a1a82ffa1c29c03bd0a08d099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 KB (251714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ae799f329aa96bef5df313c91dbc0a0e38d868c07272f597f1eff10f8e73d`

```dockerfile
```

-	Layers:
	-	`sha256:95bd72639fb1c0bed66fe4395dfbaafcd1e07422081b6d497f693379b72ea972`  
		Last Modified: Fri, 14 Feb 2025 22:46:22 GMT  
		Size: 236.3 KB (236303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f597c132ec9cc2f311b21bedb2ea4cac179ca18ea52797ae2a14edeb974022`  
		Last Modified: Fri, 14 Feb 2025 22:46:22 GMT  
		Size: 15.4 KB (15411 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d563f3d53a12cffcf9680270ac4e71be7f39abaf40b83573a356157e466cda23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50293654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60176301e10f49487afd280cc30dd74453c8a8c8be88081aecf5afbc984e0238`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27b7224c125e3eea25276e7074ed7906947b127ef6d8b0b720c946e8818e5a1`  
		Last Modified: Fri, 14 Feb 2025 21:55:17 GMT  
		Size: 47.2 MB (47195531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8506dfd9e2eda261829e5a2dab40162e10f294a0993fe5349eac2e3969e8fb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2b67b96fa68425698567e4f8189feaca3048fda9a44e73a7bafb76be7220`

```dockerfile
```

-	Layers:
	-	`sha256:53c007a8f63988dbdad3fa642d68c76c762e8e6019413a2cd69f3be929e3795e`  
		Last Modified: Fri, 14 Feb 2025 23:47:31 GMT  
		Size: 273.0 KB (272961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f92a3e4ef6669ed0fce633bb0479a2db1f5bfa492baa340616012b4ea66e2c`  
		Last Modified: Fri, 14 Feb 2025 23:47:31 GMT  
		Size: 15.5 KB (15496 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0fb6909f8bebbf62b23c901ca96dd9d237c671c041ff8b51a1388ea42b6faeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53441939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643475ad80ef78848e37611210e8c1e51117ea85e74ff94bd8e33da3032e767`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4684af61dd275887ba3a28320139a698f94446ff2caf959a96e28744fa96c8`  
		Last Modified: Sat, 15 Feb 2025 00:18:03 GMT  
		Size: 49.4 MB (49448910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8eb40a82570cc558db3eafcefe88730e7b7ddd2e233c3c6373d16c8ff3f99180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 KB (293139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe4ee094c6ae2336eb7476b509cc89eb3a784ac1123cfc997298cfbb412d80c`

```dockerfile
```

-	Layers:
	-	`sha256:1cfd6966a36eb2113ccf8f55cc3db6fb15123422aece15945540d11d0a0663b1`  
		Last Modified: Fri, 14 Feb 2025 23:47:32 GMT  
		Size: 277.6 KB (277611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65985c099384142c2b31d88f37ad92a1cceb467d68bc2d1694262f4322ec49c4`  
		Last Modified: Fri, 14 Feb 2025 23:47:32 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:02c964d4e5aff4ac1bb7130e16557b8cd20e146a55a55931e9ff35fd63fb77d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51578357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef0292b8bab02d1b9027a7accff92bae8f721f810332d01a4ccba56bc831e00`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cc214752fae5a76a78da11247fc7fd4e18886070057e36fbb330b1eed94867`  
		Last Modified: Fri, 14 Feb 2025 20:36:58 GMT  
		Size: 48.1 MB (48114734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:4950165b81210508df49394f866d3b6b6f37e932c91f03c7d39f2b6e114942a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1710b5d6cc6ab07e4829ab922e8595002e9829062f11df757f87ccf65cae6dc1`

```dockerfile
```

-	Layers:
	-	`sha256:fb43da4be3a200f51e03502adb0c1351752554317126fb2ab6f458bff17de379`  
		Last Modified: Fri, 14 Feb 2025 20:47:50 GMT  
		Size: 231.6 KB (231647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bbd0a508876668a2ffce44f5ac7a3d824990e8ff94ad3b1a0a95bbee3221ea`  
		Last Modified: Fri, 14 Feb 2025 20:47:51 GMT  
		Size: 15.4 KB (15375 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:dc04ecb458e13d9863ae5c5cac9fcac1587d1f85e1a0dde6bad08ee697cffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51787390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fafb13d1f11417efc519327b8ca2d5f528fcbf1f9a0353e70c19aae11304e8f`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a8eacf297a081fa66f96fb35bb7f9077dc497798314e7042e8e4ae4489eee`  
		Last Modified: Sat, 15 Feb 2025 09:21:49 GMT  
		Size: 48.2 MB (48213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:799b0fd8e9a79b028ba9185a683407b5661b4df6ffa89777933c177152c27b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb22270ad478aa4a055f53f6019c115af1485c205a7d4efa8e23e7d23ba7f28`

```dockerfile
```

-	Layers:
	-	`sha256:ba09f7dc9e56364a5d17f922da2a09cb014bbe2f026a1182f1096e545ee17b56`  
		Last Modified: Fri, 14 Feb 2025 23:47:34 GMT  
		Size: 271.0 KB (271006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354edc7d746f1c761998e90c2a41ff529e21811cb4ef5d964a83499115205026`  
		Last Modified: Fri, 14 Feb 2025 23:47:35 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; s390x

```console
$ docker pull erlang@sha256:fe710d0c61dcfbcadb59c835022188a1ffb799918591967935d08a558a0e7d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51310672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87e4893c5466b33b85bfebfc27ea3f5bfb7a6f7d18f43d3394033aae530023d`
-	Default Command: `["erl"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91290b7db669455932427a13ddaf8cab2ae6908ac881205bea69dcb520d5bc18`  
		Last Modified: Fri, 14 Feb 2025 22:36:08 GMT  
		Size: 47.8 MB (47843105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1d9ab9a300f5d5936a43c7517291d61255ee3cf25161dfab147b7f235930dacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 KB (286378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac71db8a3cdf4a1e36400ddc9bb43037d8d58cf55b0b9b2e7e3b216f8cf641`

```dockerfile
```

-	Layers:
	-	`sha256:f96a8aa3d318d6ece8c50cf0033d2280e8dcc663d0c07e8f5a3b8c2b38b6c216`  
		Last Modified: Fri, 14 Feb 2025 23:47:36 GMT  
		Size: 271.0 KB (270966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb7f1b30ad692c946eb4db59850318dc796902c8cfe9c3cf4de9a65d486890c`  
		Last Modified: Fri, 14 Feb 2025 23:47:36 GMT  
		Size: 15.4 KB (15412 bytes)  
		MIME: application/vnd.in-toto+json
