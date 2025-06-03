## `erlang:24-alpine`

```console
$ docker pull erlang@sha256:0538cf6619676c2d73ba18df7842e7561a1d791621501364dea10a3586217742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:24-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:080101c05e84606eed607751f0bb4c6662d1c636dcceb2e5ef77b4b8105a6f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49089588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a8e4257da960a169e7a1054fd1b9744316d529d6f41dda0f3849c5cb537e0b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 07 Jan 2025 02:24:10 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51feb1ad5ac6b6aca8a6bce4c8ced5c022d041d2abb1934684694589258aa508`  
		Last Modified: Fri, 14 Feb 2025 20:39:29 GMT  
		Size: 45.5 MB (45462691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:eceae2290d9904ad53659568b09c834542ac6268e35d9430dab491b28fdc15cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 KB (246180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63aa1a1d10d718a2c78905aa4e23da0f7e436ee5212d6ab4906ea9ca1919d38`

```dockerfile
```

-	Layers:
	-	`sha256:1ab2ef686c993c5c3e17ab820eba66d83f06164af9435aae3d86b236df1f8768`  
		Last Modified: Fri, 14 Feb 2025 23:46:21 GMT  
		Size: 231.1 KB (231136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eab71548e611949a78ae06080f7fd2f2f691bb88dc4214d5c4ba307587f5247`  
		Last Modified: Fri, 14 Feb 2025 23:46:22 GMT  
		Size: 15.0 KB (15044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4d765b8fb00b1eaa20064513819bc448907a618c1d562693238c127d9251df42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46289493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a550758070b9e2fb29ee177d9b54b425cc5c21d5841977baac980bd2c99e130`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 07 Jan 2025 02:24:10 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3027ba53a631a916b7f8a8d74b138588f0df11e9b1b965a41c8f184abbcf7419`  
		Last Modified: Fri, 14 Feb 2025 22:10:35 GMT  
		Size: 43.2 MB (43193524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8f0842022eaeecef520f5242e5e0fd74a9ab4bfba8fee00cf2261f22c2d0e5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 KB (284204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c3a383a3ecdca33a6e8f6f605b744bab0947523e9cd375442c2829e6856457`

```dockerfile
```

-	Layers:
	-	`sha256:748278fce42b1b64bb7c775b3e603b71fe178b1c82a8709a96b3831f6d86da28`  
		Last Modified: Fri, 14 Feb 2025 23:46:23 GMT  
		Size: 269.1 KB (269083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ea4ccf4d42ac4867a3268c41169c9b6db504eb5a9fdd43a211de5d7ba59cea`  
		Last Modified: Fri, 14 Feb 2025 23:46:23 GMT  
		Size: 15.1 KB (15121 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:85cc7633320882b398279f0923eb1dd81323fa683e30edf369120308c4fa2be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48139325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfcab31c160207517dd60f8871a20b791d4d9e02b20f88b9f378d1e6ffc0d7b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 07 Jan 2025 02:24:10 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9dc739ed8410929a961e7310089d8201f2b561cfeeeb35e4e4f7e73c304eff`  
		Last Modified: Sat, 15 Feb 2025 13:19:09 GMT  
		Size: 44.0 MB (44048160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d6227b723c4c4efb5467ff94151d3ca4235f8c0f899a623feae26d32fe169e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 KB (284253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a266b0352f2491c9649764ae0fcb24dc810e9cba849e6b6fd63f93652765fb6`

```dockerfile
```

-	Layers:
	-	`sha256:1f217ca99411f655e935d221d2983cb62ab70ded4cf8d45920b353ea9234eaac`  
		Last Modified: Fri, 14 Feb 2025 23:46:24 GMT  
		Size: 269.1 KB (269103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45d5049ac6760d76b8dedcbf68829902cec1d8c6d7f8f293abc84c42df3cc1e`  
		Last Modified: Fri, 14 Feb 2025 23:46:25 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; 386

```console
$ docker pull erlang@sha256:190b5cbfe906b2a701a6af4800728bdc5215ca1302b2f0b34c29140826328ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47643316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8d124fe1cd2cd570ed1a86997d046ed288fc2b8f6bbd201aee40ba498f84f7`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 07 Jan 2025 02:24:10 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:24:10 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 07 Jan 2025 02:24:10 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 07 Jan 2025 02:24:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Tue, 07 Jan 2025 02:24:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59bb365fb49f216d635f746d9aab8fc07c7814e614978f4ab3fbbb2398bc912`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 44.2 MB (44171648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:67db9c1b890dd67639f46dd5dc1f1091a2749c6f6f9a7cfe503ea1d5084313fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 KB (241426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ddbef8001f5a6fd8ea9185c89bb27c63ca7126872ca30db27e6e3ff910d0`

```dockerfile
```

-	Layers:
	-	`sha256:22d6a22a65d96c19fdbfbb0bb557317cf830e843fbb9b96522153bbe1a60f7bf`  
		Last Modified: Fri, 14 Feb 2025 20:46:22 GMT  
		Size: 226.4 KB (226413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f110ed502df8d063e1323bcdfb7c5830e488d50fab7312becd508c5901e6e794`  
		Last Modified: Fri, 14 Feb 2025 20:46:22 GMT  
		Size: 15.0 KB (15013 bytes)  
		MIME: application/vnd.in-toto+json
