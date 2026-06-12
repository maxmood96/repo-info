## `erlang:28-alpine`

```console
$ docker pull erlang@sha256:ca303ad7f441a5d3a240e0e926c2997bc99d053253310710068fc1fba0719f2d
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
$ docker pull erlang@sha256:a25c35478fecd239d18e373a1c919722187f8c883148fb13270eca9d4b039622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58792419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd617cdc1c93fe50a4fac27f3b1a571a73426f82ce35c408b000b7c24826b5b3`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:52e74de8923e10610c6bd0f66abef7bc811bc8432068f2f90441ffc739f96c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 KB (291814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bdd72ff65ddc0c1b941a02fd2c9c7679a21c25f9f56e57b7df829409a3f95d`

```dockerfile
```

-	Layers:
	-	`sha256:dbaf1c53f16b1bac0cde375fc2e431a1437632ff465840142e873f1447c1a16a`  
		Last Modified: Thu, 11 Jun 2026 19:11:17 GMT  
		Size: 276.7 KB (276737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b83830fa09d8d02efede7bc746abff41d8e2992d04c4783eabc8e69b30ef5d2`  
		Last Modified: Thu, 11 Jun 2026 19:11:17 GMT  
		Size: 15.1 KB (15077 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:a43fbeaf6ca9b4355bb1b1030636a8c6c069f1cc01b249251fbcb06af0544d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a960bf5153b84e2796fd11130df7f5f2ac49396c1fccc3f0908b4d35fad01910`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:9f440e59a6b23db3b76d341115fd9bf460e4cdbb0b8d4980651e852b2128a2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 KB (290026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99da08ed4138f812d84a68c2c1960e57883ef89a56cca589a84322803792b4e0`

```dockerfile
```

-	Layers:
	-	`sha256:888901e00c8ab4cde81d31e068db01aa06023b85bde8f89f9bb9827ecde0c459`  
		Last Modified: Thu, 11 Jun 2026 19:15:29 GMT  
		Size: 274.9 KB (274869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94025a94dee0466f815667b0a518f73417982671df4ed36da8d1cfade4b73239`  
		Last Modified: Thu, 11 Jun 2026 19:15:29 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0b9149e6bf033cacb480679d818e5f18bea6ded729a7c79011aedd8f253901eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59224353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89c14ff1d1b0ff0c322c41d3c94c6e42fb5c35f5f4fdb734843cd7530a62847`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:d5159f8d61c5333f716d110c6ccefa22f1f6398b2c785905e8c5eb9636d9ff84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 KB (292060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656091fa5ee03368beb01d3561f09713af58741fb91245c5e9a2411de7b5bc5f`

```dockerfile
```

-	Layers:
	-	`sha256:2588401107473e34aa30f82d1bee7f9c8a239ba29053557ac256fc52f63b405a`  
		Last Modified: Thu, 11 Jun 2026 19:11:38 GMT  
		Size: 276.9 KB (276879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c7b85ee68b0bf48a3bf553ab21fd80da4bed4d9350473d3bea2b535d0d3939`  
		Last Modified: Thu, 11 Jun 2026 19:11:37 GMT  
		Size: 15.2 KB (15181 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; 386

```console
$ docker pull erlang@sha256:5cc2db899f926be45362cf444a2e539cea19e5298980b2f7914869f7bb775c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56786394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115948fab23ae20b38cebf2ba0279788a972b1e90f33da6558df4e33a772b38e`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:36dd23330ed7c4c227b3aab1bf28834264889f30ce9e3ef77d567cc2c80d2a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 KB (286776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d541ffef5631a0cd1bcdccf2e4cf6f9a638b6e16a42fdacc300046d236aa134`

```dockerfile
```

-	Layers:
	-	`sha256:33dbe34ba2b24492a6937ce38bbb27c8d8d9b1d8f25f442e5df00678dab51066`  
		Last Modified: Thu, 11 Jun 2026 19:11:39 GMT  
		Size: 271.7 KB (271732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8248dedc9b5c439606386f3e6f3d7d82ac43fc4a671df1ec34e7ee33637fc030`  
		Last Modified: Thu, 11 Jun 2026 19:11:39 GMT  
		Size: 15.0 KB (15044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:163f088fe73932c486c7c02ed5a403375fa8622bb060ec4e499b325ff60c7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57282237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01428ff3c6934f61de9a83892126b4ee5d5ba00a899de4cfd6a05f84220819d`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:1981f545b9d7b2036898798de761d18da00d1006005a0ec35960bb871f2a3544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 KB (286996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3070450d72e2b85a19041a4f37aef6d74f7f822e0621d274e789bc4920e4149`

```dockerfile
```

-	Layers:
	-	`sha256:a3bfce35a5ee45068b665e389f50a1da28d3f80e5dcb79c0fccaf0ef32741768`  
		Last Modified: Thu, 11 Jun 2026 21:10:25 GMT  
		Size: 271.9 KB (271876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d55c1eabd40f34df1d80f47cdb2cb008b2d794038af9bc07466e5e361010a61`  
		Last Modified: Thu, 11 Jun 2026 21:10:25 GMT  
		Size: 15.1 KB (15120 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:d43479aefa7c8faa43631d347cbdd77f66da90c6d80d7e60b3239f5d5dc5d439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56709496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c05731d53fbb3e7fa0335c518d043648630c2422200c39bd0a5282bfcac42af`
-	Default Command: `["erl"]`

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

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:4a5299b234a39e2e204f1bc012f4ac45f24b75c97aea3840407923d8ab14c6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 KB (286919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fbdfd1e1c167d8bc502a3b682d416d41cb70dc9416a0d02acbbc621cec542b`

```dockerfile
```

-	Layers:
	-	`sha256:0b7f22f7784780348abd060666d9a39a88b0045103bb687790273484b5edc0df`  
		Last Modified: Thu, 11 Jun 2026 19:16:18 GMT  
		Size: 271.8 KB (271842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d595a3d11a33f4cd16516ed1a13abe9a20baa1221a85996b5aba17b605216cef`  
		Last Modified: Thu, 11 Jun 2026 19:16:18 GMT  
		Size: 15.1 KB (15077 bytes)  
		MIME: application/vnd.in-toto+json
