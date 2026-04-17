## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:13e5e818598d7770b9034050152c76f01aa5d57ca739ac1230bd5dbd6deecce5
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
$ docker pull erlang@sha256:98df4498cabb927c30f69708c5f66c4b3f739a1b65b8ef1c60933395e1a69dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53689097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b644cc803ded205ab08f0ec7cb599a32796ae86e4f3a443670703b4ffe84bc0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:28 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:26:28 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 00:26:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:26:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9bd6971fed3d4129e31463671445c1d83986c43107a1a777b69e98d76c9f0`  
		Last Modified: Fri, 17 Apr 2026 00:26:37 GMT  
		Size: 49.9 MB (49880908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:6be302f816c5f54cb4627e1354a50e7b1cb9f35cb782a91e492ce8d6c6991978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 KB (293156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c895db8f2820e8be57fe21eb5df1437c32242b90db6e670d1cec0c587fc8eeb`

```dockerfile
```

-	Layers:
	-	`sha256:d78ae952e433daf50e6c75158fe26bc25d283bec5a290b757be0c4c5a562dc22`  
		Last Modified: Fri, 17 Apr 2026 00:26:35 GMT  
		Size: 278.1 KB (278076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd5c0d302a6ff05ddea1afede184685e9dac7d3918decd90b62bc6082f1c3ef`  
		Last Modified: Fri, 17 Apr 2026 00:26:35 GMT  
		Size: 15.1 KB (15080 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b032f267fc22c8499b36359ebb32841e291d270a5e0dcc44f3de0c1469be2a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50632049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bc0bca2e55ea1105e04bbbccc622d9775a762e144ecf796c3e6e09492f0b16`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:08 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:30:08 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 00:30:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:30:08 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade0f2bc2e4df75af7644c92a908c8d5e800a12b74e144963dc4f53606d6a6c9`  
		Last Modified: Fri, 17 Apr 2026 00:30:16 GMT  
		Size: 47.4 MB (47406219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:485bca4d8b0e97c4b6a7407fa9b07d2dfca83976df0f6deaf42ea581f44118a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b450a4cade34092b7ebd60044f97df55010d8981ca6cc6d871b2e04307ca2558`

```dockerfile
```

-	Layers:
	-	`sha256:f6ed839071d5d80a02ebf9d7809867195799d50b1a6a3a161b4e543ac22b33cb`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 273.9 KB (273868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30679947544e47e12ccc908e5f1a0cdeb62abe02450fda081216bed3b69dff60`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:6bec298dd0da357b8f2c5cf7dac8d4c00c21623c08f16b7bd6d41b7bd0a78e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53803765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed28e98df882d7aa5b5b69d535ca55f7e4d090fd69da0f236cc8e26efa0ac0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:10 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:28:10 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 00:28:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310c877db1c259cee8d6f1bf0b9445382508eada759cf365ae9a7ec3d9898cbb`  
		Last Modified: Fri, 17 Apr 2026 00:28:20 GMT  
		Size: 49.7 MB (49661871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b28ccec4d0e2c37632bffaf0f25d0dbff031d29e185e91bdac92655bb13fbb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 KB (294052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18fcef777bae8a1c95388f6c074193f2b5890fb22dfbb80000653bcf5790f37`

```dockerfile
```

-	Layers:
	-	`sha256:e1916e624af3f45b9ae082e891c30caca29dd6eb3c85ceed1aeeb17cfdbe65ba`  
		Last Modified: Fri, 17 Apr 2026 00:28:18 GMT  
		Size: 278.9 KB (278868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0641d9a2c535aa74a2e02592dd6247aef1d7f8586164c437f815a4be24b81e29`  
		Last Modified: Fri, 17 Apr 2026 00:28:18 GMT  
		Size: 15.2 KB (15184 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:8c362cfe2f76e347ebab0d904396d26f1a487238ccf32916d59257298c07bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51941854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b14a05d631efe2e3aed5694ec9b75881814e20f95544015b7337c5b62af03b7`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:56:36 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 05:56:36 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 05:56:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 05:56:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecae5f10ec8871d2f09c50a9735b5db723fb3c166b6e1dbfba5676748b0a9f7`  
		Last Modified: Fri, 17 Apr 2026 05:56:45 GMT  
		Size: 48.3 MB (48317133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ca20e7f9791a7b465d38b58023849fb8732ca49e0204c8ad512b60d0541d0e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc6c469f884f21174ee3bf43be64630dff579bf386d11e91c536d2aab9c6571`

```dockerfile
```

-	Layers:
	-	`sha256:11f41e6511af8b497ebd0715239d76542a871c6d77fc34928795ec79cd3bedc5`  
		Last Modified: Fri, 17 Apr 2026 05:56:43 GMT  
		Size: 273.1 KB (273071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dfc2be073615465caff1842c593854e6d355eef7a80fd714209cf26d5d4702`  
		Last Modified: Fri, 17 Apr 2026 05:56:43 GMT  
		Size: 15.0 KB (15048 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:595e1e015222109a7cd8e55f6f2ce3c992d6d61f8ec5ff72979d24ac31453dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52144033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420d1c4624d7bb086e8425495089275c27fb10225d00ebdbfe328d29b70ddcae`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:16:33 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 01:16:33 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 01:16:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 01:16:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0a7c4d3846242de33054324e8ec78579812d2f7b84c4883447149ef54eb3e`  
		Last Modified: Fri, 17 Apr 2026 01:16:53 GMT  
		Size: 48.4 MB (48407377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0b578dcdb6543d0d1312d43ca755fb65431a89db6b88312e076df0cf55f28cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 KB (287039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc3942a75694ed36e1bf4097424b474b686fa5b12df9c2e63e258ac3fe08e57`

```dockerfile
```

-	Layers:
	-	`sha256:bfc3992f8169adf550de0015e844d8df315f9d0a4be5e20fd88bd43c83df5af1`  
		Last Modified: Fri, 17 Apr 2026 01:16:51 GMT  
		Size: 271.9 KB (271915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4367d2b929321bd634ad39565ad604ae999ff03fa0cc145dbe3702af6ee023a1`  
		Last Modified: Fri, 17 Apr 2026 01:16:51 GMT  
		Size: 15.1 KB (15124 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:ce7cc2135cb3424850be74db827780c3237faaaa670f32162a7691b589ff68dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51757306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c21acfd7a904bbbbd3249d5e28b2981a5faefd28c712924af5cf37abf05634`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:44:15 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Fri, 17 Apr 2026 00:44:15 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Fri, 17 Apr 2026 00:44:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Fri, 17 Apr 2026 00:44:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166504e3a7acb2ff3b04901fe14dc5c253e8c45925c26b39fc6267d952cf1b8c`  
		Last Modified: Fri, 17 Apr 2026 00:44:29 GMT  
		Size: 48.1 MB (48103433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:91d912adfc4ae5f570fc8bb8339b9e04479a7a99343fdf5a81c51ed834570d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 KB (286961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f27e9950493dae31a882130f114d8818b90f7ee9065ae807e5a6a76a9e11868`

```dockerfile
```

-	Layers:
	-	`sha256:e36c99c0753acd08503a678b8d85622a333ad90bc24b84c4e88812afadd86da6`  
		Last Modified: Fri, 17 Apr 2026 00:44:28 GMT  
		Size: 271.9 KB (271881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3072c5c2f156913f053b1fd53ed47b7c35dc40d156708e2e272b4373bcd8dd`  
		Last Modified: Fri, 17 Apr 2026 00:44:28 GMT  
		Size: 15.1 KB (15080 bytes)  
		MIME: application/vnd.in-toto+json
