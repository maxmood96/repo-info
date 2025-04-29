## `erlang:27-slim`

```console
$ docker pull erlang@sha256:0ad9efdfc92e706296d3d40c5ce540f428c178f63e44a455d7466c2553cdae6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:84f299ad4f545b224cdfe896e555bf3d5605ae1b3c8b3949c32a5aa80ec4d2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124448725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38ebab062ae479b4d631fba5223301c46ed0c4aeb827dde64c560a1b216cc8e`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853b30008cc1db18057b047af3cc8d16a6b9f3b91367c3b6b4edfaa468870965`  
		Last Modified: Mon, 28 Apr 2025 21:58:37 GMT  
		Size: 76.0 MB (75957526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:cdbc2daa580d192e0c0ff98877d3c62e95de72f78e6d724d5f6503d246a713f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2369a51f407f63e232d7e45a4e49bf7ee65cb18d58b4aa4eeb5a463ac177e58e`

```dockerfile
```

-	Layers:
	-	`sha256:e866952f8de1954013f7e42f1d335b04fbe7900941cdf08a25d97e4756ceeef2`  
		Last Modified: Mon, 28 Apr 2025 21:58:35 GMT  
		Size: 3.7 MB (3709711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f728569f5e542ec8f08b07afa7e2a6254b8291e8fc8e4c349c624216c42e65d2`  
		Last Modified: Mon, 28 Apr 2025 21:58:35 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:ef8192889b0c647c6c685a1df913f148da38b468b11e4571ca6d3bf06c652219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113780164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5f1832a30f3eab0d5839b20e55180ecca5ccd42ce5feb575b16b99c2c72f54`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:444a58715eaf0dfd1bf39e8ed2c8a7ca67bc95fb2e8d072811ba720753b5bdd3`  
		Last Modified: Tue, 08 Apr 2025 00:22:50 GMT  
		Size: 46.0 MB (46026188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852de8119f45aa1d20720202357b0cc046a5e854a8612f32d5fa60743a714f3b`  
		Last Modified: Mon, 21 Apr 2025 22:41:25 GMT  
		Size: 67.8 MB (67753976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:768eb4fc7f2976d219d255bc0f54663a419ac578cc6d12bafc3761692cd16b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6943654edf82dc697f9925f9bed259be7739a1121f44843796613cb1c787ef`

```dockerfile
```

-	Layers:
	-	`sha256:91a948169aef28beb2b4ed132bd10555dd5aaefe3af7475ec64052894751e7fa`  
		Last Modified: Mon, 21 Apr 2025 22:41:23 GMT  
		Size: 3.7 MB (3713219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a2c5ac614d9317ecd38bb9f9f6e3ef6bcd888d3024bf631dc1b31a38101035`  
		Last Modified: Mon, 21 Apr 2025 22:41:22 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1140441512d4da05a428683d8c6dd47d1e9f6c8bf09613d4d170ba8daf43dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111416987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3469be9d4fba7a70fa2b4385bfaabc7e8d702aa0f2fed2ead8882107fe6afc7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05874d7d86c30d95aa1bcc8fd5fc9282feb48456b6594770955e5e419a35bd7`  
		Last Modified: Mon, 21 Apr 2025 22:49:07 GMT  
		Size: 67.2 MB (67220216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a57df670a9f2b1dd230af110cf9fefb16af607bf7503bd192eaa0b64a5edb0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6eb1362559620fce3ec5711fdbfdf654448b9f0652e56bb5e178f7d6a7e733`

```dockerfile
```

-	Layers:
	-	`sha256:4787aa762337bf1a637549dc4e5858d11929e58f1993192abf7ec5f14c117f1b`  
		Last Modified: Mon, 21 Apr 2025 22:49:05 GMT  
		Size: 3.7 MB (3711952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0d5049b9e30e57f4da0d8afb2f2dc0d32e4c9198ab31d9e3265b68202750a6`  
		Last Modified: Mon, 21 Apr 2025 22:49:04 GMT  
		Size: 14.1 KB (14050 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:6f8c4fd17aea5101c28c0f253c79d4eda3ca1fbd9e6b2fd72a8e8938c914670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124310313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197a05cf929d235c5f4299f484e1418186bd9cb080e255feee9b336ea77bef69`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62635888dba1dbd40d9cd92e39b6810cba31bd155e95c10c804ed8250413aee`  
		Last Modified: Mon, 21 Apr 2025 22:55:50 GMT  
		Size: 76.0 MB (75982844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5b2a999fba67ef4747b227351bf377891b53fcfdcff9e1fa052825b7a09ae514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572ccd4204e1036dd4537a540299832212565f6e26fcc0ecdbafb1bd5e15c136`

```dockerfile
```

-	Layers:
	-	`sha256:fdfb336405157b79ced87727d15dba7ee85e80978feba3e1704559cf90181e13`  
		Last Modified: Mon, 21 Apr 2025 22:55:48 GMT  
		Size: 3.7 MB (3709984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0479aaee37cca1bbc62e349ba4cc8d787f6c7328beea8e9824ebf6b3a2cf0f7a`  
		Last Modified: Mon, 21 Apr 2025 22:55:47 GMT  
		Size: 14.1 KB (14083 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:e1fb4811b4d0321731e3fc8ca79c94ea05abd2ca41dd4508375c94d60455cce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115605036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd185f511bb36b7f87292b9b83a1b448357d07de20bba94c1cf2d1ae4d5974`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc19082bcc856fc1961b5f4a095853a31af64d30db29234a9e9410ebb5703691`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 66.1 MB (66126464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:baef910953062c82195895ba6c40565c7d31bed84858b344c73e2fbc0aef4c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d17f5a51598467f4120b54ac192209140bb6bbf6d8dcc6571bc2170c40c25`

```dockerfile
```

-	Layers:
	-	`sha256:e4e44cab4d6f33446f63bb646c7f17d13b1e407a0dcf8789390514ebf5bc1888`  
		Last Modified: Mon, 28 Apr 2025 21:56:55 GMT  
		Size: 3.7 MB (3706826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56330936ae90bedb517198e74bfd88c87d3b1fa0ba49518e6375a3074a255737`  
		Last Modified: Mon, 28 Apr 2025 21:56:55 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:ac9091f5967360e037847f307b5d7b19da570439a35f4fd257d500a069e8d8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117112433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1409fc7b8f1218a04135551773caf0385f1dddf9a6eff6eebc4aeddf0b823b75`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bcd04c48c452acd344ab782c6f202bd2a4c662ed98756aad36710ac792ef30`  
		Last Modified: Tue, 22 Apr 2025 00:10:56 GMT  
		Size: 68.3 MB (68337572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:265dbd04dd93ab7026646bfbbf2cb98280a544bb9761914508be24b357c64520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04625dd5994ff368c78d175647df9381624bae0a190e42927b3a9ac5394ea352`

```dockerfile
```

-	Layers:
	-	`sha256:fbb4f0da6e812582eaac400a9963ad708708233505c6d15eef55d6210969c303`  
		Last Modified: Tue, 22 Apr 2025 00:10:49 GMT  
		Size: 13.8 KB (13826 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:6df8d7deb55f712e552232968df53dd23345e3d0a8f8b675199a71884a421f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119531599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9946f783a528814f13184b1089e4b27972d8a9ea84d40d7027e680862277a`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce90379d37abb77a0b81fef6bafabb82245793984eae300b66cffe45613bc5`  
		Last Modified: Tue, 29 Apr 2025 00:44:27 GMT  
		Size: 67.2 MB (67199470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1d145b4f7f74f416310c9f393d8aff2eda7c22d29f9221ebb24f4c13d797990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1be3cb5fe4e7bc0b6c9500c1892e2629a94afb3269a2f36234367488a9b6b8`

```dockerfile
```

-	Layers:
	-	`sha256:1af164b38064c8e364da8d152fd4c10c11d12144fd47aeade12cfde27a4d8290`  
		Last Modified: Tue, 29 Apr 2025 00:44:24 GMT  
		Size: 3.7 MB (3714057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c940515eac3b15cf698fb290f56b66bbc04462b212ee23dba8ef5ccfcaab5fef`  
		Last Modified: Tue, 29 Apr 2025 00:44:24 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:f064fca6455c24ce4eb3928efd47fa61ce47760205923afa47e828cb506cc9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113028310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7193b537fa7beb6a62bbb69018c2c3e4a6b88e5af99903c1df63bec1ac937dd`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=27.3.3 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=27.3.3
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c5c69c7816c97e33f7f8efaab44b4465dc62365f5a60a7fb2a132f6e116748e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de15cde8f4d3fd9edcf65e88ea5929f238121c606cb9626d1bd8f5536b5ccc7`  
		Last Modified: Tue, 29 Apr 2025 00:10:31 GMT  
		Size: 65.9 MB (65876978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:884fe86578c8df2adb72d866df456bdaa2467adf2c8f896408b66cc12ed892de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71becbeec3b51b6a3072e2f0fba9342cf06510f6f8a51999e7dee69826a52bd2`

```dockerfile
```

-	Layers:
	-	`sha256:94f87b04049090ab1871fe3af7c3ec75d3bfd2c15d0e876f201e2c1b0ce35177`  
		Last Modified: Tue, 29 Apr 2025 00:10:29 GMT  
		Size: 3.7 MB (3709431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833387ad506b5670a3c6acbf2a83135798079f633459de32c3743e6203df8135`  
		Last Modified: Tue, 29 Apr 2025 00:10:29 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
