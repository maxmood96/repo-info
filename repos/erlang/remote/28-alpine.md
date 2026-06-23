## `erlang:28-alpine`

```console
$ docker pull erlang@sha256:f99ae46d22aa5378bad4f01f63dc3d99f9df9ab713362d3e1316daa2bac33fcf
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
$ docker pull erlang@sha256:f89a96e1e0d2e99801bab715f9162c4d657cd163e4bf444c37315f60fda89d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56242179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d40400e3ccc79d764ec9201ac3b1437121b168a9fa22b233c33613039af4023`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:10:56 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:10:56 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 20:10:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:10:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d6ef7d753a30ff40c5102cf0f5db3519961fc831f84089c69d891c6a7e40e8`  
		Last Modified: Mon, 22 Jun 2026 20:11:05 GMT  
		Size: 52.4 MB (52397758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b76d80091933db4d93ccb670abde541c1795cd7f5652786492a568850302787f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 KB (274922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2535fec505f71f19b7f6151bbc340e720391f0d6e88ab7b7a7ea26b135897150`

```dockerfile
```

-	Layers:
	-	`sha256:2b45137fb9d5314cf825ed277dfdfa75eeb63ace1344d7ae1067a2c8c6fca2e3`  
		Last Modified: Mon, 22 Jun 2026 20:11:04 GMT  
		Size: 259.8 KB (259845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d535a48493a3aa925e0936fe4a670894c6a593588b8777924941d8b49b71b4c`  
		Last Modified: Mon, 22 Jun 2026 20:11:03 GMT  
		Size: 15.1 KB (15077 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c210b89e1be781880398a2262e3846bc0994f80d77028b827dcf835aa11c8c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53170884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d683d32c830e5d82edc560cb71626479b7e65db290a18fbd93c29cb9dca8965e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:10:03 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:10:03 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 20:10:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:10:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a981b1de57ce6e1933093666f01a620afeea2a62d34b9632d0478845e5415a`  
		Last Modified: Mon, 22 Jun 2026 20:10:13 GMT  
		Size: 49.9 MB (49909030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e2a23617eb8c5fe7d23dbf1256127ff56784ac4f20b2c274f97c15db781255c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 KB (273134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e74e6d1570a8c8d4462b29e8108082336a4e9e7091ce761b5a02e1dfe25e249`

```dockerfile
```

-	Layers:
	-	`sha256:b5f0bffb3e35e37d807dd343cdb662e77d4f8958be76807e19791b0c275ea528`  
		Last Modified: Mon, 22 Jun 2026 20:10:11 GMT  
		Size: 258.0 KB (257977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050d7ce094fc99ef8c01a7a428982f86441a655a8abf5e6c7537b97158180095`  
		Last Modified: Mon, 22 Jun 2026 20:10:11 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:e5b22fe6360fc0cf5f0477e4f5b92ccea85d999bc1a8f794c3520ad2041bae58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56388514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a7c84279d8b806c383dc556d600300a04ac8c47a24301051203f1d645c7714`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:00:34 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:00:34 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 20:00:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:00:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdafdc21a2f6d23a7100e781d933fc748cfa21c90e3174e217853d1ceacf437`  
		Last Modified: Mon, 22 Jun 2026 20:00:44 GMT  
		Size: 52.2 MB (52206654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:521b914a727e490c2a3f86fb3593d74462d2049b931d7a1980088334e25c1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 KB (275168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f693e62e3d28a23c67fa54215959ecce25a2424c5deca84c97951152b66b83`

```dockerfile
```

-	Layers:
	-	`sha256:5caad7944c7abc3cddf1b00faacbe6b6555a91caeb678c68c5b027f25a370cc5`  
		Last Modified: Mon, 22 Jun 2026 20:00:42 GMT  
		Size: 260.0 KB (259987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6259fa2da94067539053fd4fc347d3aff1b0da372a819f10cb8efa4643d21d4d`  
		Last Modified: Mon, 22 Jun 2026 20:00:42 GMT  
		Size: 15.2 KB (15181 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; 386

```console
$ docker pull erlang@sha256:5861f579e9fd06fa4e76431d27d0c1ca2144b5e7317fae3ae76b5d0201f48994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54437561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def962c631899ede302889c8141e606c25140cc4824bdbe503f0c8076d22b80e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:23 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 19:55:23 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 19:55:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 19:55:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2064ea123ef6c9ba4f1b65666e98fa84a4e2f4b46acf7fd01be34b180af4aa`  
		Last Modified: Mon, 22 Jun 2026 19:55:32 GMT  
		Size: 50.8 MB (50769571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:649c453c6ce00e5de8248b888b20b993d0fda210697f1f73c55120fc1f6d8bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 KB (269885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7b890655c773eaa02234ffd57941153a0109c460308ae59aaba1900bd304cd`

```dockerfile
```

-	Layers:
	-	`sha256:37c7da2cffe6958f8fecabb350312669ce0ea14839114141829c7895f6701bf5`  
		Last Modified: Mon, 22 Jun 2026 19:55:31 GMT  
		Size: 254.8 KB (254840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35e333834c4fb41a0d6ac5deeb1cbb08e336bcf1939dbb85d651dbde5ec6191`  
		Last Modified: Mon, 22 Jun 2026 19:55:31 GMT  
		Size: 15.0 KB (15045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:851f3f3b8c0deb6040c2c8ef5416e7bd7786ebb1b3aa3a5ce35e6a5a1b2a692f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54875311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d077bed2a39b074266bc3b4272cd0cce6d8828c5311314d2596ce23c6722176`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:55:07 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:55:07 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 20:55:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:55:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e3329efea1393605effa6e8ca0c7b0c340e2b08cf29257445ff9c478019219`  
		Last Modified: Mon, 22 Jun 2026 20:55:22 GMT  
		Size: 51.1 MB (51063012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:ccebe6a87eba677b738880e4922a664e754d9ee5866a1703ba7562e02af74d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 KB (270105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d84dbbe367b6138cc60280005d3b76fcbb0505f803162c11ea2717339d2b0a`

```dockerfile
```

-	Layers:
	-	`sha256:6331280b5a6e5e73db4df7bbb0b5d4ce206dda7e3f436cbcf696299e73d9459e`  
		Last Modified: Mon, 22 Jun 2026 20:55:20 GMT  
		Size: 255.0 KB (254984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2af3dcf2a7c0e2fe323d7a506b5e4844d9403a08bb5f8be35a19ba61ef697c2`  
		Last Modified: Mon, 22 Jun 2026 20:55:20 GMT  
		Size: 15.1 KB (15121 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:0675249e1814f4dd509bf32047565ce8f7fbff60d474bb60c12c234f4e2eaf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54399479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef886285a9a84f4d2d7e6ef17caf034020ae462f3e4cbb44dec17ded32b6ed5f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:15:20 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Mon, 22 Jun 2026 20:15:20 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Mon, 22 Jun 2026 20:15:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 22 Jun 2026 20:15:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c9748836490d4d56e84356a49539e26d2ee72ca781d22b8227c63c3da05189`  
		Last Modified: Mon, 22 Jun 2026 20:15:32 GMT  
		Size: 50.7 MB (50692230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:4643a2c6e79d83150859c1469f3df15c2406770842ccbabb53dd88f4be20d22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 KB (270027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6a7bcb006c122503b083b0fbf61cb9163c0736be37650251d89e0938c58063`

```dockerfile
```

-	Layers:
	-	`sha256:a6cae14a921634b953aef47bb9fc0eb0fd1f4edd3741d1355a4ed1c66bc01694`  
		Last Modified: Mon, 22 Jun 2026 20:15:31 GMT  
		Size: 254.9 KB (254950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e3a66c1b00bb67bf0c729fa382534aba3cbe1f2f2b5b76d81883f91f039490`  
		Last Modified: Mon, 22 Jun 2026 20:15:31 GMT  
		Size: 15.1 KB (15077 bytes)  
		MIME: application/vnd.in-toto+json
