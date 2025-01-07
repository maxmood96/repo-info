<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `erlang`

-	[`erlang:24`](#erlang24)
-	[`erlang:24-alpine`](#erlang24-alpine)
-	[`erlang:24-slim`](#erlang24-slim)
-	[`erlang:24.3`](#erlang243)
-	[`erlang:24.3-alpine`](#erlang243-alpine)
-	[`erlang:24.3-slim`](#erlang243-slim)
-	[`erlang:24.3.4`](#erlang2434)
-	[`erlang:24.3.4-alpine`](#erlang2434-alpine)
-	[`erlang:24.3.4-slim`](#erlang2434-slim)
-	[`erlang:24.3.4.17`](#erlang243417)
-	[`erlang:24.3.4.17-alpine`](#erlang243417-alpine)
-	[`erlang:24.3.4.17-slim`](#erlang243417-slim)
-	[`erlang:25`](#erlang25)
-	[`erlang:25-alpine`](#erlang25-alpine)
-	[`erlang:25-slim`](#erlang25-slim)
-	[`erlang:25.3`](#erlang253)
-	[`erlang:25.3-alpine`](#erlang253-alpine)
-	[`erlang:25.3-slim`](#erlang253-slim)
-	[`erlang:25.3.2`](#erlang2532)
-	[`erlang:25.3.2-alpine`](#erlang2532-alpine)
-	[`erlang:25.3.2-slim`](#erlang2532-slim)
-	[`erlang:25.3.2.16`](#erlang253216)
-	[`erlang:25.3.2.16-alpine`](#erlang253216-alpine)
-	[`erlang:25.3.2.16-slim`](#erlang253216-slim)
-	[`erlang:26`](#erlang26)
-	[`erlang:26-alpine`](#erlang26-alpine)
-	[`erlang:26-slim`](#erlang26-slim)
-	[`erlang:26.2`](#erlang262)
-	[`erlang:26.2-alpine`](#erlang262-alpine)
-	[`erlang:26.2-slim`](#erlang262-slim)
-	[`erlang:26.2.5`](#erlang2625)
-	[`erlang:26.2.5-alpine`](#erlang2625-alpine)
-	[`erlang:26.2.5-slim`](#erlang2625-slim)
-	[`erlang:26.2.5.6`](#erlang26256)
-	[`erlang:26.2.5.6-alpine`](#erlang26256-alpine)
-	[`erlang:26.2.5.6-slim`](#erlang26256-slim)
-	[`erlang:27`](#erlang27)
-	[`erlang:27-alpine`](#erlang27-alpine)
-	[`erlang:27-slim`](#erlang27-slim)
-	[`erlang:27.2`](#erlang272)
-	[`erlang:27.2-alpine`](#erlang272-alpine)
-	[`erlang:27.2-slim`](#erlang272-slim)
-	[`erlang:27.2.0`](#erlang2720)
-	[`erlang:27.2.0-alpine`](#erlang2720-alpine)
-	[`erlang:27.2.0-slim`](#erlang2720-slim)
-	[`erlang:27.2.0.0`](#erlang27200)
-	[`erlang:27.2.0.0-alpine`](#erlang27200-alpine)
-	[`erlang:27.2.0.0-slim`](#erlang27200-slim)
-	[`erlang:alpine`](#erlangalpine)
-	[`erlang:latest`](#erlanglatest)
-	[`erlang:slim`](#erlangslim)

## `erlang:24`

```console
$ docker pull erlang@sha256:4e83bcc38ab340e730f66c6bfb15bee0bb5e82a87d5d8553c6428159382b07df
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

### `erlang:24` - linux; amd64

```console
$ docker pull erlang@sha256:80c7cdd0c60263e733f389ccb6f537a34ab566a5a92e37fdd69a737ad4f938f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570199564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d22dcdb7bc656afd414cd69dba12653622093686507544e9ad51bebae99ca`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d8110d3e6f63da2590fa833a8b647bee4ef40ff12f7ec6cfdb17011bd687`  
		Last Modified: Wed, 25 Dec 2024 01:26:00 GMT  
		Size: 248.1 MB (248084908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5d2dbafd6ad8ada0a86eb624f826365c030035e0e2a6bf82b98d8f3d9332a`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 196.4 KB (196397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5fc8b2d89c7f551b54212590e192037460f4e856ce8260f86e9e6e9811dd4`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 793.4 KB (793412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24` - unknown; unknown

```console
$ docker pull erlang@sha256:d92b50121f3487f63455364011a1aa27f15c07cc21f1af4d5585f6fafc7424c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e75e7809dd29f0ff2b20ea414d9f58ba2ff8af5a883b0e3505bbbf47f917da`

```dockerfile
```

-	Layers:
	-	`sha256:95520db69b03af9bee265f92e4e6eee7b1acf5b44da50410a2492ca5653cac1a`  
		Last Modified: Wed, 25 Dec 2024 01:25:56 GMT  
		Size: 22.9 MB (22860256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25ff3d0af2f65e0c42446cf1143f9596249260baf0dc79b6e3e9f4277205d88`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24` - linux; arm variant v7

```console
$ docker pull erlang@sha256:80fae9987ffd5acb9c294f5cb6fe1568e5f94570b974e42e4b2528b2c9bd6d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.2 MB (503205838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db5b0fb2f1bc1c4507846eacf5e691cb4e6b985e1795b0aed7198c7854129ab`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c1e6bfa755822f42ba2234aba158dee76fa7fce9ca25662ecd613e6ec2607`  
		Last Modified: Wed, 25 Dec 2024 17:17:51 GMT  
		Size: 220.4 MB (220351072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb101f0d2eb32c48c8f7f81970c1cb3e33c69119baa5b58f0f1a774cbf4571`  
		Last Modified: Wed, 25 Dec 2024 17:17:46 GMT  
		Size: 196.4 KB (196415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be2d58e19b83bfb4deb18373696a9304fd08c493965fdbfd09900ebd17196c`  
		Size: 793.3 KB (793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24` - unknown; unknown

```console
$ docker pull erlang@sha256:ec992d59199ae93c8f1e3c141b424e36d656ac955728529f6c73265c27a2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84f10ee5f979a3f5c3fed7cf718ab102a23833906571cb25c3dda7dfec1263`

```dockerfile
```

-	Layers:
	-	`sha256:fa9474d6af753503ea81c50dd16fe2749b1069c63ef95df8627462d8cab9ab12`  
		Last Modified: Wed, 25 Dec 2024 17:17:47 GMT  
		Size: 22.7 MB (22668716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d9e9ed918664472bdc718d137e10a21c6422074e81b2fdfb4250514d83a07`  
		Last Modified: Wed, 25 Dec 2024 17:17:45 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb0c9ab02c906bfdce6a072127aa861d46c0a813c3a3a80ba3888749c9eaa150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545852572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c90a30417009fd4bcd92646f7916288293ba0aaeca57275b4cf2acd1bbef63`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4094efcce17d13b858254dead0c9a15e717357b27bf7ce77716e59a50d3047`  
		Last Modified: Wed, 25 Dec 2024 12:50:23 GMT  
		Size: 232.2 MB (232240775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e925aa284c52ab09c47d344e04ece9518f31a5cd0516efedc6ed282b8d8697`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 196.4 KB (196413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48af479167db9be649233916cba52052966df914c5c7770be799983e53c2b`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 793.3 KB (793346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24` - unknown; unknown

```console
$ docker pull erlang@sha256:1497027802211835d4a201cd4b5b1b93d33491fe280f8ee67a0b64c58f715575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c033b14710599222a9990e34f3104a6274d7f02856629441aaed53c06690c72f`

```dockerfile
```

-	Layers:
	-	`sha256:5d53adbe84f1c56f2391342311b109dff78dd985e4850d26901208feaa0e26c9`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 22.9 MB (22869986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0694a57b8afa604bc83e6afa4dc58e55d0c7a35e8a981bbd4db33eda58b0a2d9`  
		Last Modified: Wed, 25 Dec 2024 12:50:17 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24` - linux; 386

```console
$ docker pull erlang@sha256:a21d6476e1e6b94d5e79d62852b6001abb3320402aa07196e979ec9d9724d1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.9 MB (567909906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056c7a5c5c63d8291ba5cfb4f3ccd15208d6fe9d1a7d116328d374e5c2dfc4a`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04153a9758aeeaa2cfc3a1bb2a319fe49a9859e081ffb29c60b5f805c32f607`  
		Last Modified: Wed, 25 Dec 2024 01:25:32 GMT  
		Size: 240.2 MB (240175496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0a4088eb59f7347cfe60f2a123fc8a4fe754319c5920993cbb9d40c68ad92`  
		Size: 196.4 KB (196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c4fd938dc611f7654ecbde5ece9311ebf4cf1c3a1c79f19b4410472b8b28d`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 793.4 KB (793401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24` - unknown; unknown

```console
$ docker pull erlang@sha256:7e8419aca807c021c0844d68696657bdf6a9af264cb534706551512de3a0e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdbef1945facaf7e6e3c657d077ae7d3f85d8a96480a8b85151cac6a9fedb61`

```dockerfile
```

-	Layers:
	-	`sha256:ff40a66929cf5fe50c5b7c25f5f76bc6fe09bf480596bed8b867e6bbda632d64`  
		Last Modified: Wed, 25 Dec 2024 01:25:27 GMT  
		Size: 22.8 MB (22847839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459e2c8f8f3c714914da6d4c64906fb825666090810258fec1f8abfd0583e5c7`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24-alpine`

```console
$ docker pull erlang@sha256:708317389189ea13ab878747d8bbc8b00be54e11a4d24a87b37d7ab228747c41
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
$ docker pull erlang@sha256:ec4fa373e1ca6ae3b99b6f902d2cd8e9609f386dc6cd5684d2b0f5026e1c9c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51112058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51796c2dd47ba38023efa4d3794586ef8202066391cb7af27c21f6199fddb7fd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fd406fb39cb3fbb0ffc42291550374af52d26e46a31f3a526ecaa04e4a4d37`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 47.7 MB (47719806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a6eea5fa144296d868372674d2e4073f201f1f7a96bb0f5cd8456120640ec8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 KB (292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73a54ea7518075ad47c104005763810859148d838fd2e938b1d1a9b39d0a005`

```dockerfile
```

-	Layers:
	-	`sha256:7317b0bdbe389ed8a23ffb7d778185d51d5a7551e01fd8390c78fcd0f3fab8b8`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 277.8 KB (277776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46426706c1f03e55dcb89406cc86c9d046c129d929b4d0d36f5f1fd43b688f5`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 15.0 KB (15045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:849855fefe08c8a7b98d2a373064e938b6dfffdd82213bfa67ca0f00829e282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90260a68865324b2c8d093b9f1af4370258616452bbcb29c3c29c6fa71e6635`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-armv7.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:845348bd1dac290491d16e4c9229b11ac46e1df9e4a500110bee98a2f9888a29`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 2.9 MB (2880509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3601b6d4fc9fd59ecf977ded90112c9c27dbaa2292cb811bac64f8ea68bfe`  
		Last Modified: Tue, 12 Nov 2024 17:06:01 GMT  
		Size: 45.3 MB (45252047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cf59b783b4368dab45f4fbb7057df51423ca4ae91833e405bd79e509a6b058a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5662c2d53f168612338ce816b518ada23ca4e75f743198938d3f84b3536a7f86`

```dockerfile
```

-	Layers:
	-	`sha256:401033779000849d3fdb51cfb1b57acccdb679b291a55d2320e0390565266ff4`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e76600c6f614a2705cc1ca60a19a4ab11eac2f45eac10cda519c3f095f94f`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f3674351a12da235b6857304a6bf758113a12f03c2de81ec41410c5f628b8f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c394bafd5e224ae814f3b3a827536c5314644a5e7bc6b7a72a4410cb56e10af`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d3e78459d6b8cd980b54dcd65d510660bc7723ebca8e38c35ce5b1d82a681`  
		Last Modified: Tue, 12 Nov 2024 11:59:18 GMT  
		Size: 46.2 MB (46245969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b3723586dcdf12757c4e2ce85ebc4fff48bad8f8fb86ed8aa0b845efb5cef9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f11418c136ccd96514532b854fd69cac3b77460f82bb1db71706eedb6394b`

```dockerfile
```

-	Layers:
	-	`sha256:cc01517ff9be4197d984d5ca94024b0d1185bf534235cb9c7f4591ef666076f3`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 273.9 KB (273867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe507fd1ec08e37ebc6684af57567c4f7143a649a6530d36d2208c5d8b8db58b`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-alpine` - linux; 386

```console
$ docker pull erlang@sha256:554f887b6f0e8eadb704f0c78d87e03dca888a371aaf563dcd43966bc85f69dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50024660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2c450afdbae9bb0aed1eb6a39dee141cbbf44bd3a48af4867948fbb9b40a4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5367cc7bb21559d0e7616575fb0d6f39aad98bafabbeb8b57a0dffd915cce732`  
		Last Modified: Mon, 09 Sep 2024 07:02:01 GMT  
		Size: 3.4 MB (3426478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e6f2db16feaa6dc07450c7234b17077a29ecdd90630eca7b0eb480702dda7`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 46.6 MB (46598182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8cfc15c6dcf51864eb58ac6f9a0065bfc6c44025943611d5ad43833d2408aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a520fe73b7d7c280cd1cbc4b1f4df211fedc89347d50395891be7d865ac6e3`

```dockerfile
```

-	Layers:
	-	`sha256:540d71da9dda88c5de83a2ca5399fbf21aa84ed9b54adda85625302e1cf6c935`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 273.0 KB (273048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6e28aaa7ed002aba8dfd81148451cbe1ea97f963694a0f3e3f9a808aa6cad5`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24-slim`

```console
$ docker pull erlang@sha256:277f59aa1a0ddc884f26fecfcdf18b7214d5f5ec5e3fd70a1389867d4fb219f0
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

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:5a66dde903b7f97f9893819477942352410eff1bdd5cf5ebff5fb4abc053d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118981670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1128b5f02199923a19fde3538f79b3a8328431d323e4e219975f7446d37bf`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edbd19289909bfe8b5ce268205275231bc30d553aae5f6c64d7d4679401d0fb`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 65.2 MB (65242713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:85a1c698bc0b064e96694d6b373535a6827c646bd3ef462b5900fabab669437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8806303e87884c9751dca5af63405de75519edc49eaee5f8a5498eacb7f723`

```dockerfile
```

-	Layers:
	-	`sha256:3989632fa6c6bec36645399c1e616afa5fe5e3ac1a0b7c85ecdfd665154f633a`  
		Last Modified: Tue, 24 Dec 2024 22:32:39 GMT  
		Size: 4.0 MB (3991216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4ad271f89f8f9bb89ab77cc11c8766a4fc826baa2278f73ccc980ea55d2300`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d0c1a1adf7de94e7efcabc74b5ad5776dcbfa763c3d814513ea8d4c8ec79c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106250147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5fbee9b85ca2b1e401bd9acd6b73e468e4d91b5f3a072461c8eed511613a0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a3655d64628f8685379e91d423b551c26c4e6151a7663562f9f1e14d82fb5`  
		Last Modified: Wed, 25 Dec 2024 04:10:18 GMT  
		Size: 57.2 MB (57225381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2ff1421f9de916b886ce2829e9d354a0af42e73064c7d30b68df95fdbe2d892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0d652c05dac0910728362f95614499fc3fb1ae1a107c7f04ad9dadc45902c5`

```dockerfile
```

-	Layers:
	-	`sha256:861f63ac68d5e7c76d4695d7e3740324ddc4d305c85d47e254bc6d5eec69e3a2`  
		Last Modified: Wed, 25 Dec 2024 04:10:17 GMT  
		Size: 4.0 MB (3992817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5164aae062b906929b8ac3a714bd8b3cb66c49883d0cadc44ca3c004494b86bd`  
		Last Modified: Wed, 25 Dec 2024 04:10:16 GMT  
		Size: 13.7 KB (13684 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb3c5b69bf411d1b751a8e3c7a9bb0ee29220c8cdc81acca7a4a88f6ff0bbd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110322294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c744ea9f97b2c78a522d4240b249952b92a2295855728b5d4f60d69a37cdd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbe9152ccf077047cc3c5bbdc26c703dca9336024919ffa3657e72de7668cb`  
		Last Modified: Wed, 25 Dec 2024 02:12:32 GMT  
		Size: 58.1 MB (58076596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:929bd5ae7dcc79cc077950b3b9f7203377cde4cfb4aa0349693aa48f465a5f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547c4c75d0a47dade36421c6cf7bef125bb613083d31a15f085139242104eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76fa63e7353805caa330b9c24ec302b76c2da25c02dcb7b5e4ca14c2ae0ef`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 4.0 MB (3990837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5831c05ac060c320dd784b94ba46374d2be40d8a6869312bab16ca0b2b32d4a6`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:3a72b27c22708254f010ade7d4dd90fa23ab8c8564e74c203d1ec843f2503399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98f1f69f3e42c49cb85a1d302dcf8e6fbbf2a79156c4a66b33161a6f1a9d0a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83443473898b47eaf4675575418644f7819f7a1eb9fda69f46d6dee46aac6a`  
		Last Modified: Tue, 24 Dec 2024 22:21:21 GMT  
		Size: 57.7 MB (57704650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b27ab5325ce70776e07690c0760e6ebdaf619a28daa202530f21d2c9accb0f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c7e634b4400645f0b299d4c242859a11284bf8b394eaeed303d196df73388a`

```dockerfile
```

-	Layers:
	-	`sha256:f4f95bd372e694d796a251713c13a51c6e6b1d91410406f3ac89936252091e5f`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 4.0 MB (3987694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf89e20a2899850c666b44433a50500096642a0d9b3f5b245d207ecf287caaf`  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3`

```console
$ docker pull erlang@sha256:4e83bcc38ab340e730f66c6bfb15bee0bb5e82a87d5d8553c6428159382b07df
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

### `erlang:24.3` - linux; amd64

```console
$ docker pull erlang@sha256:80c7cdd0c60263e733f389ccb6f537a34ab566a5a92e37fdd69a737ad4f938f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570199564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d22dcdb7bc656afd414cd69dba12653622093686507544e9ad51bebae99ca`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d8110d3e6f63da2590fa833a8b647bee4ef40ff12f7ec6cfdb17011bd687`  
		Last Modified: Wed, 25 Dec 2024 01:26:00 GMT  
		Size: 248.1 MB (248084908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5d2dbafd6ad8ada0a86eb624f826365c030035e0e2a6bf82b98d8f3d9332a`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 196.4 KB (196397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5fc8b2d89c7f551b54212590e192037460f4e856ce8260f86e9e6e9811dd4`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 793.4 KB (793412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3` - unknown; unknown

```console
$ docker pull erlang@sha256:d92b50121f3487f63455364011a1aa27f15c07cc21f1af4d5585f6fafc7424c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e75e7809dd29f0ff2b20ea414d9f58ba2ff8af5a883b0e3505bbbf47f917da`

```dockerfile
```

-	Layers:
	-	`sha256:95520db69b03af9bee265f92e4e6eee7b1acf5b44da50410a2492ca5653cac1a`  
		Last Modified: Wed, 25 Dec 2024 01:25:56 GMT  
		Size: 22.9 MB (22860256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25ff3d0af2f65e0c42446cf1143f9596249260baf0dc79b6e3e9f4277205d88`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3` - linux; arm variant v7

```console
$ docker pull erlang@sha256:80fae9987ffd5acb9c294f5cb6fe1568e5f94570b974e42e4b2528b2c9bd6d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.2 MB (503205838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db5b0fb2f1bc1c4507846eacf5e691cb4e6b985e1795b0aed7198c7854129ab`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c1e6bfa755822f42ba2234aba158dee76fa7fce9ca25662ecd613e6ec2607`  
		Last Modified: Wed, 25 Dec 2024 17:17:51 GMT  
		Size: 220.4 MB (220351072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb101f0d2eb32c48c8f7f81970c1cb3e33c69119baa5b58f0f1a774cbf4571`  
		Last Modified: Wed, 25 Dec 2024 17:17:46 GMT  
		Size: 196.4 KB (196415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be2d58e19b83bfb4deb18373696a9304fd08c493965fdbfd09900ebd17196c`  
		Size: 793.3 KB (793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3` - unknown; unknown

```console
$ docker pull erlang@sha256:ec992d59199ae93c8f1e3c141b424e36d656ac955728529f6c73265c27a2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84f10ee5f979a3f5c3fed7cf718ab102a23833906571cb25c3dda7dfec1263`

```dockerfile
```

-	Layers:
	-	`sha256:fa9474d6af753503ea81c50dd16fe2749b1069c63ef95df8627462d8cab9ab12`  
		Last Modified: Wed, 25 Dec 2024 17:17:47 GMT  
		Size: 22.7 MB (22668716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d9e9ed918664472bdc718d137e10a21c6422074e81b2fdfb4250514d83a07`  
		Last Modified: Wed, 25 Dec 2024 17:17:45 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb0c9ab02c906bfdce6a072127aa861d46c0a813c3a3a80ba3888749c9eaa150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545852572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c90a30417009fd4bcd92646f7916288293ba0aaeca57275b4cf2acd1bbef63`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4094efcce17d13b858254dead0c9a15e717357b27bf7ce77716e59a50d3047`  
		Last Modified: Wed, 25 Dec 2024 12:50:23 GMT  
		Size: 232.2 MB (232240775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e925aa284c52ab09c47d344e04ece9518f31a5cd0516efedc6ed282b8d8697`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 196.4 KB (196413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48af479167db9be649233916cba52052966df914c5c7770be799983e53c2b`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 793.3 KB (793346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3` - unknown; unknown

```console
$ docker pull erlang@sha256:1497027802211835d4a201cd4b5b1b93d33491fe280f8ee67a0b64c58f715575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c033b14710599222a9990e34f3104a6274d7f02856629441aaed53c06690c72f`

```dockerfile
```

-	Layers:
	-	`sha256:5d53adbe84f1c56f2391342311b109dff78dd985e4850d26901208feaa0e26c9`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 22.9 MB (22869986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0694a57b8afa604bc83e6afa4dc58e55d0c7a35e8a981bbd4db33eda58b0a2d9`  
		Last Modified: Wed, 25 Dec 2024 12:50:17 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3` - linux; 386

```console
$ docker pull erlang@sha256:a21d6476e1e6b94d5e79d62852b6001abb3320402aa07196e979ec9d9724d1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.9 MB (567909906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056c7a5c5c63d8291ba5cfb4f3ccd15208d6fe9d1a7d116328d374e5c2dfc4a`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04153a9758aeeaa2cfc3a1bb2a319fe49a9859e081ffb29c60b5f805c32f607`  
		Last Modified: Wed, 25 Dec 2024 01:25:32 GMT  
		Size: 240.2 MB (240175496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0a4088eb59f7347cfe60f2a123fc8a4fe754319c5920993cbb9d40c68ad92`  
		Size: 196.4 KB (196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c4fd938dc611f7654ecbde5ece9311ebf4cf1c3a1c79f19b4410472b8b28d`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 793.4 KB (793401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3` - unknown; unknown

```console
$ docker pull erlang@sha256:7e8419aca807c021c0844d68696657bdf6a9af264cb534706551512de3a0e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdbef1945facaf7e6e3c657d077ae7d3f85d8a96480a8b85151cac6a9fedb61`

```dockerfile
```

-	Layers:
	-	`sha256:ff40a66929cf5fe50c5b7c25f5f76bc6fe09bf480596bed8b867e6bbda632d64`  
		Last Modified: Wed, 25 Dec 2024 01:25:27 GMT  
		Size: 22.8 MB (22847839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459e2c8f8f3c714914da6d4c64906fb825666090810258fec1f8abfd0583e5c7`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3-alpine`

```console
$ docker pull erlang@sha256:708317389189ea13ab878747d8bbc8b00be54e11a4d24a87b37d7ab228747c41
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

### `erlang:24.3-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:ec4fa373e1ca6ae3b99b6f902d2cd8e9609f386dc6cd5684d2b0f5026e1c9c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51112058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51796c2dd47ba38023efa4d3794586ef8202066391cb7af27c21f6199fddb7fd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fd406fb39cb3fbb0ffc42291550374af52d26e46a31f3a526ecaa04e4a4d37`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 47.7 MB (47719806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a6eea5fa144296d868372674d2e4073f201f1f7a96bb0f5cd8456120640ec8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 KB (292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73a54ea7518075ad47c104005763810859148d838fd2e938b1d1a9b39d0a005`

```dockerfile
```

-	Layers:
	-	`sha256:7317b0bdbe389ed8a23ffb7d778185d51d5a7551e01fd8390c78fcd0f3fab8b8`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 277.8 KB (277776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46426706c1f03e55dcb89406cc86c9d046c129d929b4d0d36f5f1fd43b688f5`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 15.0 KB (15045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:849855fefe08c8a7b98d2a373064e938b6dfffdd82213bfa67ca0f00829e282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90260a68865324b2c8d093b9f1af4370258616452bbcb29c3c29c6fa71e6635`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-armv7.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:845348bd1dac290491d16e4c9229b11ac46e1df9e4a500110bee98a2f9888a29`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 2.9 MB (2880509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3601b6d4fc9fd59ecf977ded90112c9c27dbaa2292cb811bac64f8ea68bfe`  
		Last Modified: Tue, 12 Nov 2024 17:06:01 GMT  
		Size: 45.3 MB (45252047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cf59b783b4368dab45f4fbb7057df51423ca4ae91833e405bd79e509a6b058a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5662c2d53f168612338ce816b518ada23ca4e75f743198938d3f84b3536a7f86`

```dockerfile
```

-	Layers:
	-	`sha256:401033779000849d3fdb51cfb1b57acccdb679b291a55d2320e0390565266ff4`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e76600c6f614a2705cc1ca60a19a4ab11eac2f45eac10cda519c3f095f94f`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f3674351a12da235b6857304a6bf758113a12f03c2de81ec41410c5f628b8f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c394bafd5e224ae814f3b3a827536c5314644a5e7bc6b7a72a4410cb56e10af`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d3e78459d6b8cd980b54dcd65d510660bc7723ebca8e38c35ce5b1d82a681`  
		Last Modified: Tue, 12 Nov 2024 11:59:18 GMT  
		Size: 46.2 MB (46245969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b3723586dcdf12757c4e2ce85ebc4fff48bad8f8fb86ed8aa0b845efb5cef9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f11418c136ccd96514532b854fd69cac3b77460f82bb1db71706eedb6394b`

```dockerfile
```

-	Layers:
	-	`sha256:cc01517ff9be4197d984d5ca94024b0d1185bf534235cb9c7f4591ef666076f3`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 273.9 KB (273867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe507fd1ec08e37ebc6684af57567c4f7143a649a6530d36d2208c5d8b8db58b`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-alpine` - linux; 386

```console
$ docker pull erlang@sha256:554f887b6f0e8eadb704f0c78d87e03dca888a371aaf563dcd43966bc85f69dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50024660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2c450afdbae9bb0aed1eb6a39dee141cbbf44bd3a48af4867948fbb9b40a4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5367cc7bb21559d0e7616575fb0d6f39aad98bafabbeb8b57a0dffd915cce732`  
		Last Modified: Mon, 09 Sep 2024 07:02:01 GMT  
		Size: 3.4 MB (3426478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e6f2db16feaa6dc07450c7234b17077a29ecdd90630eca7b0eb480702dda7`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 46.6 MB (46598182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8cfc15c6dcf51864eb58ac6f9a0065bfc6c44025943611d5ad43833d2408aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a520fe73b7d7c280cd1cbc4b1f4df211fedc89347d50395891be7d865ac6e3`

```dockerfile
```

-	Layers:
	-	`sha256:540d71da9dda88c5de83a2ca5399fbf21aa84ed9b54adda85625302e1cf6c935`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 273.0 KB (273048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6e28aaa7ed002aba8dfd81148451cbe1ea97f963694a0f3e3f9a808aa6cad5`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3-slim`

```console
$ docker pull erlang@sha256:277f59aa1a0ddc884f26fecfcdf18b7214d5f5ec5e3fd70a1389867d4fb219f0
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

### `erlang:24.3-slim` - linux; amd64

```console
$ docker pull erlang@sha256:5a66dde903b7f97f9893819477942352410eff1bdd5cf5ebff5fb4abc053d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118981670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1128b5f02199923a19fde3538f79b3a8328431d323e4e219975f7446d37bf`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edbd19289909bfe8b5ce268205275231bc30d553aae5f6c64d7d4679401d0fb`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 65.2 MB (65242713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:85a1c698bc0b064e96694d6b373535a6827c646bd3ef462b5900fabab669437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8806303e87884c9751dca5af63405de75519edc49eaee5f8a5498eacb7f723`

```dockerfile
```

-	Layers:
	-	`sha256:3989632fa6c6bec36645399c1e616afa5fe5e3ac1a0b7c85ecdfd665154f633a`  
		Last Modified: Tue, 24 Dec 2024 22:32:39 GMT  
		Size: 4.0 MB (3991216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4ad271f89f8f9bb89ab77cc11c8766a4fc826baa2278f73ccc980ea55d2300`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d0c1a1adf7de94e7efcabc74b5ad5776dcbfa763c3d814513ea8d4c8ec79c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106250147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5fbee9b85ca2b1e401bd9acd6b73e468e4d91b5f3a072461c8eed511613a0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a3655d64628f8685379e91d423b551c26c4e6151a7663562f9f1e14d82fb5`  
		Last Modified: Wed, 25 Dec 2024 04:10:18 GMT  
		Size: 57.2 MB (57225381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2ff1421f9de916b886ce2829e9d354a0af42e73064c7d30b68df95fdbe2d892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0d652c05dac0910728362f95614499fc3fb1ae1a107c7f04ad9dadc45902c5`

```dockerfile
```

-	Layers:
	-	`sha256:861f63ac68d5e7c76d4695d7e3740324ddc4d305c85d47e254bc6d5eec69e3a2`  
		Last Modified: Wed, 25 Dec 2024 04:10:17 GMT  
		Size: 4.0 MB (3992817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5164aae062b906929b8ac3a714bd8b3cb66c49883d0cadc44ca3c004494b86bd`  
		Last Modified: Wed, 25 Dec 2024 04:10:16 GMT  
		Size: 13.7 KB (13684 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb3c5b69bf411d1b751a8e3c7a9bb0ee29220c8cdc81acca7a4a88f6ff0bbd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110322294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c744ea9f97b2c78a522d4240b249952b92a2295855728b5d4f60d69a37cdd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbe9152ccf077047cc3c5bbdc26c703dca9336024919ffa3657e72de7668cb`  
		Last Modified: Wed, 25 Dec 2024 02:12:32 GMT  
		Size: 58.1 MB (58076596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:929bd5ae7dcc79cc077950b3b9f7203377cde4cfb4aa0349693aa48f465a5f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547c4c75d0a47dade36421c6cf7bef125bb613083d31a15f085139242104eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76fa63e7353805caa330b9c24ec302b76c2da25c02dcb7b5e4ca14c2ae0ef`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 4.0 MB (3990837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5831c05ac060c320dd784b94ba46374d2be40d8a6869312bab16ca0b2b32d4a6`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3-slim` - linux; 386

```console
$ docker pull erlang@sha256:3a72b27c22708254f010ade7d4dd90fa23ab8c8564e74c203d1ec843f2503399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98f1f69f3e42c49cb85a1d302dcf8e6fbbf2a79156c4a66b33161a6f1a9d0a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83443473898b47eaf4675575418644f7819f7a1eb9fda69f46d6dee46aac6a`  
		Last Modified: Tue, 24 Dec 2024 22:21:21 GMT  
		Size: 57.7 MB (57704650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b27ab5325ce70776e07690c0760e6ebdaf619a28daa202530f21d2c9accb0f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c7e634b4400645f0b299d4c242859a11284bf8b394eaeed303d196df73388a`

```dockerfile
```

-	Layers:
	-	`sha256:f4f95bd372e694d796a251713c13a51c6e6b1d91410406f3ac89936252091e5f`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 4.0 MB (3987694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf89e20a2899850c666b44433a50500096642a0d9b3f5b245d207ecf287caaf`  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4`

```console
$ docker pull erlang@sha256:4e83bcc38ab340e730f66c6bfb15bee0bb5e82a87d5d8553c6428159382b07df
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

### `erlang:24.3.4` - linux; amd64

```console
$ docker pull erlang@sha256:80c7cdd0c60263e733f389ccb6f537a34ab566a5a92e37fdd69a737ad4f938f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570199564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d22dcdb7bc656afd414cd69dba12653622093686507544e9ad51bebae99ca`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d8110d3e6f63da2590fa833a8b647bee4ef40ff12f7ec6cfdb17011bd687`  
		Last Modified: Wed, 25 Dec 2024 01:26:00 GMT  
		Size: 248.1 MB (248084908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5d2dbafd6ad8ada0a86eb624f826365c030035e0e2a6bf82b98d8f3d9332a`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 196.4 KB (196397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5fc8b2d89c7f551b54212590e192037460f4e856ce8260f86e9e6e9811dd4`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 793.4 KB (793412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4` - unknown; unknown

```console
$ docker pull erlang@sha256:d92b50121f3487f63455364011a1aa27f15c07cc21f1af4d5585f6fafc7424c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e75e7809dd29f0ff2b20ea414d9f58ba2ff8af5a883b0e3505bbbf47f917da`

```dockerfile
```

-	Layers:
	-	`sha256:95520db69b03af9bee265f92e4e6eee7b1acf5b44da50410a2492ca5653cac1a`  
		Last Modified: Wed, 25 Dec 2024 01:25:56 GMT  
		Size: 22.9 MB (22860256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25ff3d0af2f65e0c42446cf1143f9596249260baf0dc79b6e3e9f4277205d88`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4` - linux; arm variant v7

```console
$ docker pull erlang@sha256:80fae9987ffd5acb9c294f5cb6fe1568e5f94570b974e42e4b2528b2c9bd6d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.2 MB (503205838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db5b0fb2f1bc1c4507846eacf5e691cb4e6b985e1795b0aed7198c7854129ab`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c1e6bfa755822f42ba2234aba158dee76fa7fce9ca25662ecd613e6ec2607`  
		Last Modified: Wed, 25 Dec 2024 17:17:51 GMT  
		Size: 220.4 MB (220351072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb101f0d2eb32c48c8f7f81970c1cb3e33c69119baa5b58f0f1a774cbf4571`  
		Last Modified: Wed, 25 Dec 2024 17:17:46 GMT  
		Size: 196.4 KB (196415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be2d58e19b83bfb4deb18373696a9304fd08c493965fdbfd09900ebd17196c`  
		Size: 793.3 KB (793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4` - unknown; unknown

```console
$ docker pull erlang@sha256:ec992d59199ae93c8f1e3c141b424e36d656ac955728529f6c73265c27a2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84f10ee5f979a3f5c3fed7cf718ab102a23833906571cb25c3dda7dfec1263`

```dockerfile
```

-	Layers:
	-	`sha256:fa9474d6af753503ea81c50dd16fe2749b1069c63ef95df8627462d8cab9ab12`  
		Last Modified: Wed, 25 Dec 2024 17:17:47 GMT  
		Size: 22.7 MB (22668716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d9e9ed918664472bdc718d137e10a21c6422074e81b2fdfb4250514d83a07`  
		Last Modified: Wed, 25 Dec 2024 17:17:45 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb0c9ab02c906bfdce6a072127aa861d46c0a813c3a3a80ba3888749c9eaa150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545852572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c90a30417009fd4bcd92646f7916288293ba0aaeca57275b4cf2acd1bbef63`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4094efcce17d13b858254dead0c9a15e717357b27bf7ce77716e59a50d3047`  
		Last Modified: Wed, 25 Dec 2024 12:50:23 GMT  
		Size: 232.2 MB (232240775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e925aa284c52ab09c47d344e04ece9518f31a5cd0516efedc6ed282b8d8697`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 196.4 KB (196413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48af479167db9be649233916cba52052966df914c5c7770be799983e53c2b`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 793.3 KB (793346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4` - unknown; unknown

```console
$ docker pull erlang@sha256:1497027802211835d4a201cd4b5b1b93d33491fe280f8ee67a0b64c58f715575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c033b14710599222a9990e34f3104a6274d7f02856629441aaed53c06690c72f`

```dockerfile
```

-	Layers:
	-	`sha256:5d53adbe84f1c56f2391342311b109dff78dd985e4850d26901208feaa0e26c9`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 22.9 MB (22869986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0694a57b8afa604bc83e6afa4dc58e55d0c7a35e8a981bbd4db33eda58b0a2d9`  
		Last Modified: Wed, 25 Dec 2024 12:50:17 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4` - linux; 386

```console
$ docker pull erlang@sha256:a21d6476e1e6b94d5e79d62852b6001abb3320402aa07196e979ec9d9724d1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.9 MB (567909906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056c7a5c5c63d8291ba5cfb4f3ccd15208d6fe9d1a7d116328d374e5c2dfc4a`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04153a9758aeeaa2cfc3a1bb2a319fe49a9859e081ffb29c60b5f805c32f607`  
		Last Modified: Wed, 25 Dec 2024 01:25:32 GMT  
		Size: 240.2 MB (240175496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0a4088eb59f7347cfe60f2a123fc8a4fe754319c5920993cbb9d40c68ad92`  
		Size: 196.4 KB (196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c4fd938dc611f7654ecbde5ece9311ebf4cf1c3a1c79f19b4410472b8b28d`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 793.4 KB (793401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4` - unknown; unknown

```console
$ docker pull erlang@sha256:7e8419aca807c021c0844d68696657bdf6a9af264cb534706551512de3a0e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdbef1945facaf7e6e3c657d077ae7d3f85d8a96480a8b85151cac6a9fedb61`

```dockerfile
```

-	Layers:
	-	`sha256:ff40a66929cf5fe50c5b7c25f5f76bc6fe09bf480596bed8b867e6bbda632d64`  
		Last Modified: Wed, 25 Dec 2024 01:25:27 GMT  
		Size: 22.8 MB (22847839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459e2c8f8f3c714914da6d4c64906fb825666090810258fec1f8abfd0583e5c7`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4-alpine`

```console
$ docker pull erlang@sha256:708317389189ea13ab878747d8bbc8b00be54e11a4d24a87b37d7ab228747c41
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

### `erlang:24.3.4-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:ec4fa373e1ca6ae3b99b6f902d2cd8e9609f386dc6cd5684d2b0f5026e1c9c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51112058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51796c2dd47ba38023efa4d3794586ef8202066391cb7af27c21f6199fddb7fd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fd406fb39cb3fbb0ffc42291550374af52d26e46a31f3a526ecaa04e4a4d37`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 47.7 MB (47719806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a6eea5fa144296d868372674d2e4073f201f1f7a96bb0f5cd8456120640ec8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 KB (292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73a54ea7518075ad47c104005763810859148d838fd2e938b1d1a9b39d0a005`

```dockerfile
```

-	Layers:
	-	`sha256:7317b0bdbe389ed8a23ffb7d778185d51d5a7551e01fd8390c78fcd0f3fab8b8`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 277.8 KB (277776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46426706c1f03e55dcb89406cc86c9d046c129d929b4d0d36f5f1fd43b688f5`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 15.0 KB (15045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:849855fefe08c8a7b98d2a373064e938b6dfffdd82213bfa67ca0f00829e282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90260a68865324b2c8d093b9f1af4370258616452bbcb29c3c29c6fa71e6635`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-armv7.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:845348bd1dac290491d16e4c9229b11ac46e1df9e4a500110bee98a2f9888a29`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 2.9 MB (2880509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3601b6d4fc9fd59ecf977ded90112c9c27dbaa2292cb811bac64f8ea68bfe`  
		Last Modified: Tue, 12 Nov 2024 17:06:01 GMT  
		Size: 45.3 MB (45252047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cf59b783b4368dab45f4fbb7057df51423ca4ae91833e405bd79e509a6b058a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5662c2d53f168612338ce816b518ada23ca4e75f743198938d3f84b3536a7f86`

```dockerfile
```

-	Layers:
	-	`sha256:401033779000849d3fdb51cfb1b57acccdb679b291a55d2320e0390565266ff4`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e76600c6f614a2705cc1ca60a19a4ab11eac2f45eac10cda519c3f095f94f`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f3674351a12da235b6857304a6bf758113a12f03c2de81ec41410c5f628b8f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c394bafd5e224ae814f3b3a827536c5314644a5e7bc6b7a72a4410cb56e10af`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d3e78459d6b8cd980b54dcd65d510660bc7723ebca8e38c35ce5b1d82a681`  
		Last Modified: Tue, 12 Nov 2024 11:59:18 GMT  
		Size: 46.2 MB (46245969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b3723586dcdf12757c4e2ce85ebc4fff48bad8f8fb86ed8aa0b845efb5cef9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f11418c136ccd96514532b854fd69cac3b77460f82bb1db71706eedb6394b`

```dockerfile
```

-	Layers:
	-	`sha256:cc01517ff9be4197d984d5ca94024b0d1185bf534235cb9c7f4591ef666076f3`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 273.9 KB (273867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe507fd1ec08e37ebc6684af57567c4f7143a649a6530d36d2208c5d8b8db58b`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-alpine` - linux; 386

```console
$ docker pull erlang@sha256:554f887b6f0e8eadb704f0c78d87e03dca888a371aaf563dcd43966bc85f69dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50024660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2c450afdbae9bb0aed1eb6a39dee141cbbf44bd3a48af4867948fbb9b40a4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5367cc7bb21559d0e7616575fb0d6f39aad98bafabbeb8b57a0dffd915cce732`  
		Last Modified: Mon, 09 Sep 2024 07:02:01 GMT  
		Size: 3.4 MB (3426478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e6f2db16feaa6dc07450c7234b17077a29ecdd90630eca7b0eb480702dda7`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 46.6 MB (46598182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8cfc15c6dcf51864eb58ac6f9a0065bfc6c44025943611d5ad43833d2408aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a520fe73b7d7c280cd1cbc4b1f4df211fedc89347d50395891be7d865ac6e3`

```dockerfile
```

-	Layers:
	-	`sha256:540d71da9dda88c5de83a2ca5399fbf21aa84ed9b54adda85625302e1cf6c935`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 273.0 KB (273048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6e28aaa7ed002aba8dfd81148451cbe1ea97f963694a0f3e3f9a808aa6cad5`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4-slim`

```console
$ docker pull erlang@sha256:277f59aa1a0ddc884f26fecfcdf18b7214d5f5ec5e3fd70a1389867d4fb219f0
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

### `erlang:24.3.4-slim` - linux; amd64

```console
$ docker pull erlang@sha256:5a66dde903b7f97f9893819477942352410eff1bdd5cf5ebff5fb4abc053d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118981670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1128b5f02199923a19fde3538f79b3a8328431d323e4e219975f7446d37bf`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edbd19289909bfe8b5ce268205275231bc30d553aae5f6c64d7d4679401d0fb`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 65.2 MB (65242713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:85a1c698bc0b064e96694d6b373535a6827c646bd3ef462b5900fabab669437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8806303e87884c9751dca5af63405de75519edc49eaee5f8a5498eacb7f723`

```dockerfile
```

-	Layers:
	-	`sha256:3989632fa6c6bec36645399c1e616afa5fe5e3ac1a0b7c85ecdfd665154f633a`  
		Last Modified: Tue, 24 Dec 2024 22:32:39 GMT  
		Size: 4.0 MB (3991216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4ad271f89f8f9bb89ab77cc11c8766a4fc826baa2278f73ccc980ea55d2300`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d0c1a1adf7de94e7efcabc74b5ad5776dcbfa763c3d814513ea8d4c8ec79c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106250147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5fbee9b85ca2b1e401bd9acd6b73e468e4d91b5f3a072461c8eed511613a0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a3655d64628f8685379e91d423b551c26c4e6151a7663562f9f1e14d82fb5`  
		Last Modified: Wed, 25 Dec 2024 04:10:18 GMT  
		Size: 57.2 MB (57225381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2ff1421f9de916b886ce2829e9d354a0af42e73064c7d30b68df95fdbe2d892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0d652c05dac0910728362f95614499fc3fb1ae1a107c7f04ad9dadc45902c5`

```dockerfile
```

-	Layers:
	-	`sha256:861f63ac68d5e7c76d4695d7e3740324ddc4d305c85d47e254bc6d5eec69e3a2`  
		Last Modified: Wed, 25 Dec 2024 04:10:17 GMT  
		Size: 4.0 MB (3992817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5164aae062b906929b8ac3a714bd8b3cb66c49883d0cadc44ca3c004494b86bd`  
		Last Modified: Wed, 25 Dec 2024 04:10:16 GMT  
		Size: 13.7 KB (13684 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb3c5b69bf411d1b751a8e3c7a9bb0ee29220c8cdc81acca7a4a88f6ff0bbd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110322294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c744ea9f97b2c78a522d4240b249952b92a2295855728b5d4f60d69a37cdd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbe9152ccf077047cc3c5bbdc26c703dca9336024919ffa3657e72de7668cb`  
		Last Modified: Wed, 25 Dec 2024 02:12:32 GMT  
		Size: 58.1 MB (58076596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:929bd5ae7dcc79cc077950b3b9f7203377cde4cfb4aa0349693aa48f465a5f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547c4c75d0a47dade36421c6cf7bef125bb613083d31a15f085139242104eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76fa63e7353805caa330b9c24ec302b76c2da25c02dcb7b5e4ca14c2ae0ef`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 4.0 MB (3990837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5831c05ac060c320dd784b94ba46374d2be40d8a6869312bab16ca0b2b32d4a6`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4-slim` - linux; 386

```console
$ docker pull erlang@sha256:3a72b27c22708254f010ade7d4dd90fa23ab8c8564e74c203d1ec843f2503399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98f1f69f3e42c49cb85a1d302dcf8e6fbbf2a79156c4a66b33161a6f1a9d0a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83443473898b47eaf4675575418644f7819f7a1eb9fda69f46d6dee46aac6a`  
		Last Modified: Tue, 24 Dec 2024 22:21:21 GMT  
		Size: 57.7 MB (57704650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b27ab5325ce70776e07690c0760e6ebdaf619a28daa202530f21d2c9accb0f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c7e634b4400645f0b299d4c242859a11284bf8b394eaeed303d196df73388a`

```dockerfile
```

-	Layers:
	-	`sha256:f4f95bd372e694d796a251713c13a51c6e6b1d91410406f3ac89936252091e5f`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 4.0 MB (3987694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf89e20a2899850c666b44433a50500096642a0d9b3f5b245d207ecf287caaf`  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4.17`

```console
$ docker pull erlang@sha256:4e83bcc38ab340e730f66c6bfb15bee0bb5e82a87d5d8553c6428159382b07df
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

### `erlang:24.3.4.17` - linux; amd64

```console
$ docker pull erlang@sha256:80c7cdd0c60263e733f389ccb6f537a34ab566a5a92e37fdd69a737ad4f938f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570199564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d22dcdb7bc656afd414cd69dba12653622093686507544e9ad51bebae99ca`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d8110d3e6f63da2590fa833a8b647bee4ef40ff12f7ec6cfdb17011bd687`  
		Last Modified: Wed, 25 Dec 2024 01:26:00 GMT  
		Size: 248.1 MB (248084908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5d2dbafd6ad8ada0a86eb624f826365c030035e0e2a6bf82b98d8f3d9332a`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 196.4 KB (196397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5fc8b2d89c7f551b54212590e192037460f4e856ce8260f86e9e6e9811dd4`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 793.4 KB (793412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17` - unknown; unknown

```console
$ docker pull erlang@sha256:d92b50121f3487f63455364011a1aa27f15c07cc21f1af4d5585f6fafc7424c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e75e7809dd29f0ff2b20ea414d9f58ba2ff8af5a883b0e3505bbbf47f917da`

```dockerfile
```

-	Layers:
	-	`sha256:95520db69b03af9bee265f92e4e6eee7b1acf5b44da50410a2492ca5653cac1a`  
		Last Modified: Wed, 25 Dec 2024 01:25:56 GMT  
		Size: 22.9 MB (22860256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25ff3d0af2f65e0c42446cf1143f9596249260baf0dc79b6e3e9f4277205d88`  
		Last Modified: Wed, 25 Dec 2024 01:25:55 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17` - linux; arm variant v7

```console
$ docker pull erlang@sha256:80fae9987ffd5acb9c294f5cb6fe1568e5f94570b974e42e4b2528b2c9bd6d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.2 MB (503205838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db5b0fb2f1bc1c4507846eacf5e691cb4e6b985e1795b0aed7198c7854129ab`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c1e6bfa755822f42ba2234aba158dee76fa7fce9ca25662ecd613e6ec2607`  
		Last Modified: Wed, 25 Dec 2024 17:17:51 GMT  
		Size: 220.4 MB (220351072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb101f0d2eb32c48c8f7f81970c1cb3e33c69119baa5b58f0f1a774cbf4571`  
		Last Modified: Wed, 25 Dec 2024 17:17:46 GMT  
		Size: 196.4 KB (196415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be2d58e19b83bfb4deb18373696a9304fd08c493965fdbfd09900ebd17196c`  
		Size: 793.3 KB (793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17` - unknown; unknown

```console
$ docker pull erlang@sha256:ec992d59199ae93c8f1e3c141b424e36d656ac955728529f6c73265c27a2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84f10ee5f979a3f5c3fed7cf718ab102a23833906571cb25c3dda7dfec1263`

```dockerfile
```

-	Layers:
	-	`sha256:fa9474d6af753503ea81c50dd16fe2749b1069c63ef95df8627462d8cab9ab12`  
		Last Modified: Wed, 25 Dec 2024 17:17:47 GMT  
		Size: 22.7 MB (22668716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d9e9ed918664472bdc718d137e10a21c6422074e81b2fdfb4250514d83a07`  
		Last Modified: Wed, 25 Dec 2024 17:17:45 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb0c9ab02c906bfdce6a072127aa861d46c0a813c3a3a80ba3888749c9eaa150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545852572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c90a30417009fd4bcd92646f7916288293ba0aaeca57275b4cf2acd1bbef63`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4094efcce17d13b858254dead0c9a15e717357b27bf7ce77716e59a50d3047`  
		Last Modified: Wed, 25 Dec 2024 12:50:23 GMT  
		Size: 232.2 MB (232240775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e925aa284c52ab09c47d344e04ece9518f31a5cd0516efedc6ed282b8d8697`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 196.4 KB (196413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48af479167db9be649233916cba52052966df914c5c7770be799983e53c2b`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 793.3 KB (793346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17` - unknown; unknown

```console
$ docker pull erlang@sha256:1497027802211835d4a201cd4b5b1b93d33491fe280f8ee67a0b64c58f715575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c033b14710599222a9990e34f3104a6274d7f02856629441aaed53c06690c72f`

```dockerfile
```

-	Layers:
	-	`sha256:5d53adbe84f1c56f2391342311b109dff78dd985e4850d26901208feaa0e26c9`  
		Last Modified: Wed, 25 Dec 2024 12:50:18 GMT  
		Size: 22.9 MB (22869986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0694a57b8afa604bc83e6afa4dc58e55d0c7a35e8a981bbd4db33eda58b0a2d9`  
		Last Modified: Wed, 25 Dec 2024 12:50:17 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17` - linux; 386

```console
$ docker pull erlang@sha256:a21d6476e1e6b94d5e79d62852b6001abb3320402aa07196e979ec9d9724d1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.9 MB (567909906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056c7a5c5c63d8291ba5cfb4f3ccd15208d6fe9d1a7d116328d374e5c2dfc4a`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04153a9758aeeaa2cfc3a1bb2a319fe49a9859e081ffb29c60b5f805c32f607`  
		Last Modified: Wed, 25 Dec 2024 01:25:32 GMT  
		Size: 240.2 MB (240175496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0a4088eb59f7347cfe60f2a123fc8a4fe754319c5920993cbb9d40c68ad92`  
		Size: 196.4 KB (196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c4fd938dc611f7654ecbde5ece9311ebf4cf1c3a1c79f19b4410472b8b28d`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 793.4 KB (793401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17` - unknown; unknown

```console
$ docker pull erlang@sha256:7e8419aca807c021c0844d68696657bdf6a9af264cb534706551512de3a0e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdbef1945facaf7e6e3c657d077ae7d3f85d8a96480a8b85151cac6a9fedb61`

```dockerfile
```

-	Layers:
	-	`sha256:ff40a66929cf5fe50c5b7c25f5f76bc6fe09bf480596bed8b867e6bbda632d64`  
		Last Modified: Wed, 25 Dec 2024 01:25:27 GMT  
		Size: 22.8 MB (22847839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459e2c8f8f3c714914da6d4c64906fb825666090810258fec1f8abfd0583e5c7`  
		Last Modified: Wed, 25 Dec 2024 01:25:26 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4.17-alpine`

```console
$ docker pull erlang@sha256:708317389189ea13ab878747d8bbc8b00be54e11a4d24a87b37d7ab228747c41
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

### `erlang:24.3.4.17-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:ec4fa373e1ca6ae3b99b6f902d2cd8e9609f386dc6cd5684d2b0f5026e1c9c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51112058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51796c2dd47ba38023efa4d3794586ef8202066391cb7af27c21f6199fddb7fd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fd406fb39cb3fbb0ffc42291550374af52d26e46a31f3a526ecaa04e4a4d37`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 47.7 MB (47719806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a6eea5fa144296d868372674d2e4073f201f1f7a96bb0f5cd8456120640ec8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 KB (292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73a54ea7518075ad47c104005763810859148d838fd2e938b1d1a9b39d0a005`

```dockerfile
```

-	Layers:
	-	`sha256:7317b0bdbe389ed8a23ffb7d778185d51d5a7551e01fd8390c78fcd0f3fab8b8`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 277.8 KB (277776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46426706c1f03e55dcb89406cc86c9d046c129d929b4d0d36f5f1fd43b688f5`  
		Last Modified: Tue, 12 Nov 2024 02:45:52 GMT  
		Size: 15.0 KB (15045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:849855fefe08c8a7b98d2a373064e938b6dfffdd82213bfa67ca0f00829e282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90260a68865324b2c8d093b9f1af4370258616452bbcb29c3c29c6fa71e6635`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-armv7.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:845348bd1dac290491d16e4c9229b11ac46e1df9e4a500110bee98a2f9888a29`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 2.9 MB (2880509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3601b6d4fc9fd59ecf977ded90112c9c27dbaa2292cb811bac64f8ea68bfe`  
		Last Modified: Tue, 12 Nov 2024 17:06:01 GMT  
		Size: 45.3 MB (45252047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cf59b783b4368dab45f4fbb7057df51423ca4ae91833e405bd79e509a6b058a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5662c2d53f168612338ce816b518ada23ca4e75f743198938d3f84b3536a7f86`

```dockerfile
```

-	Layers:
	-	`sha256:401033779000849d3fdb51cfb1b57acccdb679b291a55d2320e0390565266ff4`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e76600c6f614a2705cc1ca60a19a4ab11eac2f45eac10cda519c3f095f94f`  
		Last Modified: Tue, 12 Nov 2024 17:05:59 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f3674351a12da235b6857304a6bf758113a12f03c2de81ec41410c5f628b8f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c394bafd5e224ae814f3b3a827536c5314644a5e7bc6b7a72a4410cb56e10af`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d3e78459d6b8cd980b54dcd65d510660bc7723ebca8e38c35ce5b1d82a681`  
		Last Modified: Tue, 12 Nov 2024 11:59:18 GMT  
		Size: 46.2 MB (46245969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:b3723586dcdf12757c4e2ce85ebc4fff48bad8f8fb86ed8aa0b845efb5cef9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 KB (289017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f11418c136ccd96514532b854fd69cac3b77460f82bb1db71706eedb6394b`

```dockerfile
```

-	Layers:
	-	`sha256:cc01517ff9be4197d984d5ca94024b0d1185bf534235cb9c7f4591ef666076f3`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 273.9 KB (273867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe507fd1ec08e37ebc6684af57567c4f7143a649a6530d36d2208c5d8b8db58b`  
		Last Modified: Tue, 12 Nov 2024 11:59:16 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-alpine` - linux; 386

```console
$ docker pull erlang@sha256:554f887b6f0e8eadb704f0c78d87e03dca888a371aaf563dcd43966bc85f69dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50024660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2c450afdbae9bb0aed1eb6a39dee141cbbf44bd3a48af4867948fbb9b40a4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD alpine-minirootfs-3.17.10-x86.tar.gz / # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5367cc7bb21559d0e7616575fb0d6f39aad98bafabbeb8b57a0dffd915cce732`  
		Last Modified: Mon, 09 Sep 2024 07:02:01 GMT  
		Size: 3.4 MB (3426478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e6f2db16feaa6dc07450c7234b17077a29ecdd90630eca7b0eb480702dda7`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 46.6 MB (46598182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:8cfc15c6dcf51864eb58ac6f9a0065bfc6c44025943611d5ad43833d2408aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 KB (288062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a520fe73b7d7c280cd1cbc4b1f4df211fedc89347d50395891be7d865ac6e3`

```dockerfile
```

-	Layers:
	-	`sha256:540d71da9dda88c5de83a2ca5399fbf21aa84ed9b54adda85625302e1cf6c935`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 273.0 KB (273048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6e28aaa7ed002aba8dfd81148451cbe1ea97f963694a0f3e3f9a808aa6cad5`  
		Last Modified: Tue, 12 Nov 2024 02:19:39 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:24.3.4.17-slim`

```console
$ docker pull erlang@sha256:277f59aa1a0ddc884f26fecfcdf18b7214d5f5ec5e3fd70a1389867d4fb219f0
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

### `erlang:24.3.4.17-slim` - linux; amd64

```console
$ docker pull erlang@sha256:5a66dde903b7f97f9893819477942352410eff1bdd5cf5ebff5fb4abc053d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118981670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1128b5f02199923a19fde3538f79b3a8328431d323e4e219975f7446d37bf`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edbd19289909bfe8b5ce268205275231bc30d553aae5f6c64d7d4679401d0fb`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 65.2 MB (65242713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:85a1c698bc0b064e96694d6b373535a6827c646bd3ef462b5900fabab669437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8806303e87884c9751dca5af63405de75519edc49eaee5f8a5498eacb7f723`

```dockerfile
```

-	Layers:
	-	`sha256:3989632fa6c6bec36645399c1e616afa5fe5e3ac1a0b7c85ecdfd665154f633a`  
		Last Modified: Tue, 24 Dec 2024 22:32:39 GMT  
		Size: 4.0 MB (3991216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4ad271f89f8f9bb89ab77cc11c8766a4fc826baa2278f73ccc980ea55d2300`  
		Last Modified: Tue, 24 Dec 2024 22:32:40 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d0c1a1adf7de94e7efcabc74b5ad5776dcbfa763c3d814513ea8d4c8ec79c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106250147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5fbee9b85ca2b1e401bd9acd6b73e468e4d91b5f3a072461c8eed511613a0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a3655d64628f8685379e91d423b551c26c4e6151a7663562f9f1e14d82fb5`  
		Last Modified: Wed, 25 Dec 2024 04:10:18 GMT  
		Size: 57.2 MB (57225381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2ff1421f9de916b886ce2829e9d354a0af42e73064c7d30b68df95fdbe2d892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0d652c05dac0910728362f95614499fc3fb1ae1a107c7f04ad9dadc45902c5`

```dockerfile
```

-	Layers:
	-	`sha256:861f63ac68d5e7c76d4695d7e3740324ddc4d305c85d47e254bc6d5eec69e3a2`  
		Last Modified: Wed, 25 Dec 2024 04:10:17 GMT  
		Size: 4.0 MB (3992817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5164aae062b906929b8ac3a714bd8b3cb66c49883d0cadc44ca3c004494b86bd`  
		Last Modified: Wed, 25 Dec 2024 04:10:16 GMT  
		Size: 13.7 KB (13684 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb3c5b69bf411d1b751a8e3c7a9bb0ee29220c8cdc81acca7a4a88f6ff0bbd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110322294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c744ea9f97b2c78a522d4240b249952b92a2295855728b5d4f60d69a37cdd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbe9152ccf077047cc3c5bbdc26c703dca9336024919ffa3657e72de7668cb`  
		Last Modified: Wed, 25 Dec 2024 02:12:32 GMT  
		Size: 58.1 MB (58076596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:929bd5ae7dcc79cc077950b3b9f7203377cde4cfb4aa0349693aa48f465a5f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547c4c75d0a47dade36421c6cf7bef125bb613083d31a15f085139242104eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76fa63e7353805caa330b9c24ec302b76c2da25c02dcb7b5e4ca14c2ae0ef`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 4.0 MB (3990837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5831c05ac060c320dd784b94ba46374d2be40d8a6869312bab16ca0b2b32d4a6`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24.3.4.17-slim` - linux; 386

```console
$ docker pull erlang@sha256:3a72b27c22708254f010ade7d4dd90fa23ab8c8564e74c203d1ec843f2503399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98f1f69f3e42c49cb85a1d302dcf8e6fbbf2a79156c4a66b33161a6f1a9d0a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83443473898b47eaf4675575418644f7819f7a1eb9fda69f46d6dee46aac6a`  
		Last Modified: Tue, 24 Dec 2024 22:21:21 GMT  
		Size: 57.7 MB (57704650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24.3.4.17-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b27ab5325ce70776e07690c0760e6ebdaf619a28daa202530f21d2c9accb0f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c7e634b4400645f0b299d4c242859a11284bf8b394eaeed303d196df73388a`

```dockerfile
```

-	Layers:
	-	`sha256:f4f95bd372e694d796a251713c13a51c6e6b1d91410406f3ac89936252091e5f`  
		Last Modified: Tue, 24 Dec 2024 22:21:19 GMT  
		Size: 4.0 MB (3987694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf89e20a2899850c666b44433a50500096642a0d9b3f5b245d207ecf287caaf`  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25`

```console
$ docker pull erlang@sha256:8cd12c5bd0a1f32371ee732abe3a1d015383687d022336e0aab43e024f905f9c
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

### `erlang:25` - linux; amd64

```console
$ docker pull erlang@sha256:faeddbe16324a853d7e07125a45a9841fb16dfdf5ce65602b2da080db6d60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571518612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15e502d7197b71f9ec3795a1074a6e7fe245262e4e3e7c55e7e3171c6b11912`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdbda8d0d800b0704ebeb21a5e96c5a411e8a2a0cf2e38eb986ac03165990f8`  
		Last Modified: Wed, 25 Dec 2024 01:27:53 GMT  
		Size: 249.4 MB (249377872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793eb42ee5cfeb39ad6827f04f070865b95745fd7c0bfa902bb484a0649cef8`  
		Size: 198.6 KB (198553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419d38573bb24840af385a66e1b43641b2ba5bdee928f45585b06aa0ab34e88`  
		Last Modified: Wed, 25 Dec 2024 01:27:50 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25` - unknown; unknown

```console
$ docker pull erlang@sha256:cb7886e84f754a3732480055a21947bef8e7c63c9fedfb37fbc14fd3697c1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f3376dcbd4ca4adf5eacf288a8d9c4e8968455d94bd5be89b77092d7f8bc92`

```dockerfile
```

-	Layers:
	-	`sha256:41f0a912b43fe106fca56c664119e847a6eea16b14da884ec8fa5d55ab270867`  
		Size: 22.9 MB (22860271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0f98ebe162fabb096e1b6b64773cd3d66172052298fb35277a6dc6ea3b3d58`  
		Last Modified: Wed, 25 Dec 2024 01:27:49 GMT  
		Size: 19.0 KB (19044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25` - linux; arm variant v7

```console
$ docker pull erlang@sha256:e6a226cee1bf653dacd5b957c36724ed4b7a7f1693b56b7595d43a8dde5c2ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.8 MB (503830714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ba67114d09e16d40dc8893d47255ae7c1348cd0e62b331390af13cab9ffef`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87b0018d16c5606bcb05d4254c94f3711f9d0b2c094aa9552f18a1c22f6d82`  
		Last Modified: Wed, 25 Dec 2024 17:10:34 GMT  
		Size: 220.9 MB (220949815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d47c6304486ed3b0e3d4131619aca7337530920d0ab58b4c5df7e158933461`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 198.6 KB (198555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec436bbc722d6626bc7b36077484dfbb9522ce98f6000d6585696a93cc4d7567`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 817.3 KB (817338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25` - unknown; unknown

```console
$ docker pull erlang@sha256:f2a7317a55701ce9af91b152c0cbba5c23e71c2179ad7293258a5b0a3f0de7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6265cbc0d9ba6f3279cdbd87125047650ceef34f08ddcb377bb087dedf00d70`

```dockerfile
```

-	Layers:
	-	`sha256:33c438925dce9e5ad1f038b2f25bf27d20448aba4814c5b34e122c7f6844d697`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 22.7 MB (22668731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414513c0c4b80957d279a015614551afa002d0cac95cb1efc9be9ae412aaf71b`  
		Last Modified: Wed, 25 Dec 2024 17:10:28 GMT  
		Size: 19.1 KB (19146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b0ded875551582d6d5a7c4c8847281b1a955f265b1cfc5eb62438a9ba5f4777c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.7 MB (552710538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9701cb9cbfa6ad14de9d42f20be2cd4aee4748327cc9b90a4d28d0de5bbbe99`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd93a08350049dc2dd4954376eace30ff99c125ab4378e4323ddaee84887a4`  
		Last Modified: Wed, 25 Dec 2024 12:44:25 GMT  
		Size: 239.1 MB (239072593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4513a80b05b5b33d82478481f5a651414f47624b776a5790cd2176ba15c8ce9d`  
		Size: 198.6 KB (198567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587bfbe46fc9df02ca8f975c053c9d687170e7187ec79355d5419580f5a7e0f`  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25` - unknown; unknown

```console
$ docker pull erlang@sha256:f7b249adcfce1b775d08474b39d53e2afbaf4662cf60c8444cad463565c65953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045554a56755ce8d118d01b161601c187ee4c02e1b2e48e5b472c750e565f80e`

```dockerfile
```

-	Layers:
	-	`sha256:b66c7e9c0a0c6dd1d8d4f8f357e45e819f24c3d4a97cfb6ebcc56aa4597a46b6`  
		Last Modified: Wed, 25 Dec 2024 12:44:21 GMT  
		Size: 22.9 MB (22870001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014eab792f387ad658ec211a03672eb10ba6e9120f5bea0b3eb6861089cd7c4f`  
		Last Modified: Wed, 25 Dec 2024 12:44:20 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25` - linux; 386

```console
$ docker pull erlang@sha256:ada9001ab711ec66ff96eb64dd5cbb89ee9b149e89f916d695bb1553444a4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.4 MB (568436449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2dc449bdb3db240f9c6e6e05f2ce15380c11b21dbaf46bcd28e60b0b4fce53`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb9a99b80f16f6337bf0f4100ede97026cfde98cb0ba85b9b0b013cd9a8e9e`  
		Last Modified: Wed, 25 Dec 2024 01:26:36 GMT  
		Size: 240.7 MB (240675953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6f3a40450df4b3ea1ea15c0bd165b6a84ed542ebd03f0cd2b04de4d0a9931`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 198.6 KB (198550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad5ff82d89172480bf5c2ef969afed055fd3fcbfff4d2763441e5e6330f60c`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25` - unknown; unknown

```console
$ docker pull erlang@sha256:e068d6833d265612ec46b081232ed260ec1b392c48ceaaa75010b1e4525d39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442871334defb357c8cf4e8229dae55900910cf7d032d9b59b3338f2dc7395e0`

```dockerfile
```

-	Layers:
	-	`sha256:27c9effaaaba62a04fbf0615cc4853d09587a62702e54acbc8ddbbe55a049b5f`  
		Last Modified: Wed, 25 Dec 2024 01:26:31 GMT  
		Size: 22.8 MB (22847854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1398d7f027f5bc0d5cbc49fc26f5a91a1a14d25311bf9325aea271d3121d1606`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25-alpine`

```console
$ docker pull erlang@sha256:9aa024b6dce94c1dffee75f9391c00752215ce9d9c1ffa82908f7252f7da943b
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

### `erlang:25-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:363574cd3ef7bbbbd99b0f5999c944db5c2e13598d6ec65b353a8a81f31ed726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49014926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6b5edd8dd82b8da1dfeb62653addcd872fd587dba746fdf0bb4df2c02300aa`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4bfe9d39936fdffcca98a58cc959e7aceb4a0ca840cb946df9c454b453435`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 45.4 MB (45400927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:842c706d2c52982d3e37172a30e398e24b0963013810c018e9291365f351b740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50581b4be831d6a5931f237cd389d5234125e57e284fae6e2636006d140ac0b3`

```dockerfile
```

-	Layers:
	-	`sha256:f1d7746bdeea19584bd225c3c142345ab8884b24615f78bf121f58704b8f8c13`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 267.1 KB (267145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407199e47888d46841460f72f4c6fa3d87948ab15f5cb28633a6153612b31b1c`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0408842e075d1fde581fa121b4177fb5678ab5488c68300a7a0944a739302c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46235955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba1751ea5976ba7b5d922d98ea89be208d45263b319beef1522717b968831be`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284ab9ddbd0e63f3b9e1fb169a281ed66936eecdf8e9a5cd40ef1f0cdf89fda`  
		Last Modified: Tue, 07 Jan 2025 06:37:39 GMT  
		Size: 43.1 MB (43144667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:30ac975454e04aa1fad424f9be33175975011288c85e64ecf671c7dc8d3827cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 KB (278342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d18bca9d94903ec58edcb5b03d2e880d6649215236504c4f6018f2d1f7fca`

```dockerfile
```

-	Layers:
	-	`sha256:700166069041b8e911d845e926cb37a97828023159e9ac210e3dbc57b7b8c5a7`  
		Size: 263.2 KB (263220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d354df2421d3330cc634ea2f867be75d49f24e26ce2c165e5091cd5368770ab`  
		Last Modified: Tue, 07 Jan 2025 06:37:37 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3cc2d3ff417548146052e2ac990ae544d3002cdb8a9ec6dbe7b45b23f82e857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49306954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ccf1efd13fe1550e8ebc7d02b417216cedc702724ccd6df202aca78f522302`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c293a0aee2fea9db3345340ce9abab5f2af37bf6a14bb90c04429cbfa94af7c`  
		Last Modified: Tue, 07 Jan 2025 07:40:52 GMT  
		Size: 45.2 MB (45220268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a11e18d5cbc8d9e1014f7c6bbb6dc2a98341b1433f0f27bc23a37b375081a047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 KB (283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d51ad83104e745196934ea3afe378115de706cca0e68d2431201e92896394`

```dockerfile
```

-	Layers:
	-	`sha256:dc5db9fc29104734c69d95459b2fb0202f16bf016769b1a9d78a24f3242f2162`  
		Last Modified: Tue, 07 Jan 2025 07:40:51 GMT  
		Size: 267.9 KB (267938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fa229e176f678c4a3d3f5570cf299bf7df12340c20cd63f3e5e626a6dd2cd7`  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-alpine` - linux; 386

```console
$ docker pull erlang@sha256:12607f9599b4feae051bdf7e0ec5ec05b33bba6f0df763c0ebeb645ad538f0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47539289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc9a99fa8f71f415c4d77b4297af88a54933ab12e87b99d0850e204ce03840a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dad321e104162329e85cce8b34b65774c49baf98fe0403ca974c65c447b76d`  
		Last Modified: Tue, 07 Jan 2025 03:23:22 GMT  
		Size: 44.1 MB (44076100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:dad356e76796a093786564a47a7bc4d73dc296e1ba82840e38d2e14cb4f9f27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 KB (277436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c8901cc99d770bfff2060caf777659877d70c71a83bde797ff0a886bf166df`

```dockerfile
```

-	Layers:
	-	`sha256:f1748d6a507a590b66072643cbad1147488a07d2681108203b58efe688049df5`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 262.4 KB (262422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f493617cff73ba003934ad797b7a2c926ff851c06dca4baefd4d76581a5f725`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25-slim`

```console
$ docker pull erlang@sha256:11c1a486f7ec0742a5867cbe8091012fe7dbf491621321ec28370a8b51f5c82a
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

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9c66656774caeb31ff8e84d70bcabe11a4234787fb77c72c9073466ecee5a04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119665330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546785f7bd908d4ecdbd3c51642db19c5a986af91611e6d3de751a7e19e3ef91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c71e0da37644431c6c87a465134b3af8cd72bfc700526f8b1ee580d7dce6a`  
		Last Modified: Tue, 24 Dec 2024 22:33:14 GMT  
		Size: 65.9 MB (65926373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b004ebb71cbbb51cc85a32f2d131716f5c35530a05be805285ab4d52949b2a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db377855df50e0e44a68423aad17334a9a989aad9657a926738ce9ad2394df75`

```dockerfile
```

-	Layers:
	-	`sha256:566a41129ab05daa388e957a7c717d74c97824fe52fd82ef02ecd9455aba7451`  
		Size: 4.0 MB (3991231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb8f99660e4ca9739df9c177e7341fc16d48b692c575347b43ee5ba6ffb6fb8`  
		Last Modified: Tue, 24 Dec 2024 22:33:13 GMT  
		Size: 13.6 KB (13610 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:56b59bf3e740177706e6d19880326564136e0db6ed2459edcc1065f206afd6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106238070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8de36cc639605e34868597df42bd63003ffbdc245e02eff77bca7a3f8d9ee3`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcfa8800dd3a9423fb0dae51c28af48e6ccf296d881f17ee1b492cda97654b`  
		Last Modified: Wed, 25 Dec 2024 04:05:38 GMT  
		Size: 57.2 MB (57213304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4beba43747968d4e6013707e95696337e2025dd3254c3fcabc537596c8675c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8732d9d5eb47073b5a9f4612c27582b4584c39d969726b0f20c45a19503b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:c41ef693b60f57ec4fcf77b44e802ff582535ff84ea56011cf7c475f4a7432a5`  
		Last Modified: Wed, 25 Dec 2024 04:05:37 GMT  
		Size: 4.0 MB (3992832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca9e3ae75e6aff3d0a6d12e3c7ddfdc2355885a142f626444088a86abfc33d7`  
		Last Modified: Wed, 25 Dec 2024 04:05:36 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4f4573e46974204ba5efbe6ee1a763f16138b13823b8374251885e67bd27bcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913bc4e20504be1c624d0d38e5e81b001df57c072692df230babbb271a616fc`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1855fe22bd18bf42b3fe5cb07e311bff8cd160d07f8c6281d921265bb2b31`  
		Last Modified: Wed, 25 Dec 2024 02:08:59 GMT  
		Size: 64.3 MB (64291421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:09e2a4d332f3948b97008633087ccd2aa1d36faea0c36a01d834fe3c27e5a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032b4cf5c0b713d92bc0d562f64e68d2e30352812fff6c1c0124cdf7fe7c72ac`

```dockerfile
```

-	Layers:
	-	`sha256:ce3b56c07836790ffac725433537e4d7618e7a9c45f4b451da0fbd2ec3be760e`  
		Last Modified: Wed, 25 Dec 2024 02:08:57 GMT  
		Size: 4.0 MB (3990852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1eb53fdd8ee2e93913b5f68aac2bb2630964f85778024493106286dc1c566a7`  
		Last Modified: Wed, 25 Dec 2024 02:08:56 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:092e5560f3dfbada6be0e77efd6efa406c0a4db269fda69da4dfb402eb89e7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112281359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c082ae443e1f6669a78bfc734694668cd07a44371b154b30c4f7eda21dcff`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad11c813e13a388055f5ad57bbf6dc37024f63a02ed4474d52493c988d9438d`  
		Last Modified: Tue, 24 Dec 2024 22:21:45 GMT  
		Size: 57.6 MB (57605343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eccd3194dee83762cf828be38b1f07f93cd57e6413e876faeed249b11142a92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c945cafb12ca9b75c3414ca4a940408712c31736f382c8d2f7067fab8abc390f`

```dockerfile
```

-	Layers:
	-	`sha256:f714a054c81032f54f16f6f32d3dc266dd87c71f5144e7611a7b286413857548`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 4.0 MB (3987709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2492441d0c4b41069bebea5c113c404a24189b02b4b56d4cf0b3fd0e21ca76f`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 13.6 KB (13578 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3`

```console
$ docker pull erlang@sha256:8cd12c5bd0a1f32371ee732abe3a1d015383687d022336e0aab43e024f905f9c
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

### `erlang:25.3` - linux; amd64

```console
$ docker pull erlang@sha256:faeddbe16324a853d7e07125a45a9841fb16dfdf5ce65602b2da080db6d60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571518612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15e502d7197b71f9ec3795a1074a6e7fe245262e4e3e7c55e7e3171c6b11912`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdbda8d0d800b0704ebeb21a5e96c5a411e8a2a0cf2e38eb986ac03165990f8`  
		Last Modified: Wed, 25 Dec 2024 01:27:53 GMT  
		Size: 249.4 MB (249377872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793eb42ee5cfeb39ad6827f04f070865b95745fd7c0bfa902bb484a0649cef8`  
		Last Modified: Wed, 25 Dec 2024 01:27:49 GMT  
		Size: 198.6 KB (198553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419d38573bb24840af385a66e1b43641b2ba5bdee928f45585b06aa0ab34e88`  
		Last Modified: Wed, 25 Dec 2024 01:27:50 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3` - unknown; unknown

```console
$ docker pull erlang@sha256:cb7886e84f754a3732480055a21947bef8e7c63c9fedfb37fbc14fd3697c1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f3376dcbd4ca4adf5eacf288a8d9c4e8968455d94bd5be89b77092d7f8bc92`

```dockerfile
```

-	Layers:
	-	`sha256:41f0a912b43fe106fca56c664119e847a6eea16b14da884ec8fa5d55ab270867`  
		Size: 22.9 MB (22860271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0f98ebe162fabb096e1b6b64773cd3d66172052298fb35277a6dc6ea3b3d58`  
		Last Modified: Wed, 25 Dec 2024 01:27:49 GMT  
		Size: 19.0 KB (19044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3` - linux; arm variant v7

```console
$ docker pull erlang@sha256:e6a226cee1bf653dacd5b957c36724ed4b7a7f1693b56b7595d43a8dde5c2ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.8 MB (503830714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ba67114d09e16d40dc8893d47255ae7c1348cd0e62b331390af13cab9ffef`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87b0018d16c5606bcb05d4254c94f3711f9d0b2c094aa9552f18a1c22f6d82`  
		Last Modified: Wed, 25 Dec 2024 17:10:34 GMT  
		Size: 220.9 MB (220949815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d47c6304486ed3b0e3d4131619aca7337530920d0ab58b4c5df7e158933461`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 198.6 KB (198555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec436bbc722d6626bc7b36077484dfbb9522ce98f6000d6585696a93cc4d7567`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 817.3 KB (817338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3` - unknown; unknown

```console
$ docker pull erlang@sha256:f2a7317a55701ce9af91b152c0cbba5c23e71c2179ad7293258a5b0a3f0de7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6265cbc0d9ba6f3279cdbd87125047650ceef34f08ddcb377bb087dedf00d70`

```dockerfile
```

-	Layers:
	-	`sha256:33c438925dce9e5ad1f038b2f25bf27d20448aba4814c5b34e122c7f6844d697`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 22.7 MB (22668731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414513c0c4b80957d279a015614551afa002d0cac95cb1efc9be9ae412aaf71b`  
		Last Modified: Wed, 25 Dec 2024 17:10:28 GMT  
		Size: 19.1 KB (19146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b0ded875551582d6d5a7c4c8847281b1a955f265b1cfc5eb62438a9ba5f4777c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.7 MB (552710538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9701cb9cbfa6ad14de9d42f20be2cd4aee4748327cc9b90a4d28d0de5bbbe99`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd93a08350049dc2dd4954376eace30ff99c125ab4378e4323ddaee84887a4`  
		Last Modified: Wed, 25 Dec 2024 12:44:25 GMT  
		Size: 239.1 MB (239072593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4513a80b05b5b33d82478481f5a651414f47624b776a5790cd2176ba15c8ce9d`  
		Size: 198.6 KB (198567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587bfbe46fc9df02ca8f975c053c9d687170e7187ec79355d5419580f5a7e0f`  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3` - unknown; unknown

```console
$ docker pull erlang@sha256:f7b249adcfce1b775d08474b39d53e2afbaf4662cf60c8444cad463565c65953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045554a56755ce8d118d01b161601c187ee4c02e1b2e48e5b472c750e565f80e`

```dockerfile
```

-	Layers:
	-	`sha256:b66c7e9c0a0c6dd1d8d4f8f357e45e819f24c3d4a97cfb6ebcc56aa4597a46b6`  
		Last Modified: Wed, 25 Dec 2024 12:44:21 GMT  
		Size: 22.9 MB (22870001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014eab792f387ad658ec211a03672eb10ba6e9120f5bea0b3eb6861089cd7c4f`  
		Last Modified: Wed, 25 Dec 2024 12:44:20 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3` - linux; 386

```console
$ docker pull erlang@sha256:ada9001ab711ec66ff96eb64dd5cbb89ee9b149e89f916d695bb1553444a4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.4 MB (568436449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2dc449bdb3db240f9c6e6e05f2ce15380c11b21dbaf46bcd28e60b0b4fce53`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb9a99b80f16f6337bf0f4100ede97026cfde98cb0ba85b9b0b013cd9a8e9e`  
		Last Modified: Wed, 25 Dec 2024 01:26:36 GMT  
		Size: 240.7 MB (240675953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6f3a40450df4b3ea1ea15c0bd165b6a84ed542ebd03f0cd2b04de4d0a9931`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 198.6 KB (198550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad5ff82d89172480bf5c2ef969afed055fd3fcbfff4d2763441e5e6330f60c`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3` - unknown; unknown

```console
$ docker pull erlang@sha256:e068d6833d265612ec46b081232ed260ec1b392c48ceaaa75010b1e4525d39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442871334defb357c8cf4e8229dae55900910cf7d032d9b59b3338f2dc7395e0`

```dockerfile
```

-	Layers:
	-	`sha256:27c9effaaaba62a04fbf0615cc4853d09587a62702e54acbc8ddbbe55a049b5f`  
		Last Modified: Wed, 25 Dec 2024 01:26:31 GMT  
		Size: 22.8 MB (22847854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1398d7f027f5bc0d5cbc49fc26f5a91a1a14d25311bf9325aea271d3121d1606`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3-alpine`

```console
$ docker pull erlang@sha256:9aa024b6dce94c1dffee75f9391c00752215ce9d9c1ffa82908f7252f7da943b
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

### `erlang:25.3-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:363574cd3ef7bbbbd99b0f5999c944db5c2e13598d6ec65b353a8a81f31ed726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49014926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6b5edd8dd82b8da1dfeb62653addcd872fd587dba746fdf0bb4df2c02300aa`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4bfe9d39936fdffcca98a58cc959e7aceb4a0ca840cb946df9c454b453435`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 45.4 MB (45400927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:842c706d2c52982d3e37172a30e398e24b0963013810c018e9291365f351b740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50581b4be831d6a5931f237cd389d5234125e57e284fae6e2636006d140ac0b3`

```dockerfile
```

-	Layers:
	-	`sha256:f1d7746bdeea19584bd225c3c142345ab8884b24615f78bf121f58704b8f8c13`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 267.1 KB (267145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407199e47888d46841460f72f4c6fa3d87948ab15f5cb28633a6153612b31b1c`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0408842e075d1fde581fa121b4177fb5678ab5488c68300a7a0944a739302c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46235955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba1751ea5976ba7b5d922d98ea89be208d45263b319beef1522717b968831be`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284ab9ddbd0e63f3b9e1fb169a281ed66936eecdf8e9a5cd40ef1f0cdf89fda`  
		Last Modified: Tue, 07 Jan 2025 06:37:39 GMT  
		Size: 43.1 MB (43144667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:30ac975454e04aa1fad424f9be33175975011288c85e64ecf671c7dc8d3827cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 KB (278342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d18bca9d94903ec58edcb5b03d2e880d6649215236504c4f6018f2d1f7fca`

```dockerfile
```

-	Layers:
	-	`sha256:700166069041b8e911d845e926cb37a97828023159e9ac210e3dbc57b7b8c5a7`  
		Size: 263.2 KB (263220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d354df2421d3330cc634ea2f867be75d49f24e26ce2c165e5091cd5368770ab`  
		Last Modified: Tue, 07 Jan 2025 06:37:37 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3cc2d3ff417548146052e2ac990ae544d3002cdb8a9ec6dbe7b45b23f82e857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49306954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ccf1efd13fe1550e8ebc7d02b417216cedc702724ccd6df202aca78f522302`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c293a0aee2fea9db3345340ce9abab5f2af37bf6a14bb90c04429cbfa94af7c`  
		Last Modified: Tue, 07 Jan 2025 07:40:52 GMT  
		Size: 45.2 MB (45220268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a11e18d5cbc8d9e1014f7c6bbb6dc2a98341b1433f0f27bc23a37b375081a047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 KB (283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d51ad83104e745196934ea3afe378115de706cca0e68d2431201e92896394`

```dockerfile
```

-	Layers:
	-	`sha256:dc5db9fc29104734c69d95459b2fb0202f16bf016769b1a9d78a24f3242f2162`  
		Last Modified: Tue, 07 Jan 2025 07:40:51 GMT  
		Size: 267.9 KB (267938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fa229e176f678c4a3d3f5570cf299bf7df12340c20cd63f3e5e626a6dd2cd7`  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-alpine` - linux; 386

```console
$ docker pull erlang@sha256:12607f9599b4feae051bdf7e0ec5ec05b33bba6f0df763c0ebeb645ad538f0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47539289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc9a99fa8f71f415c4d77b4297af88a54933ab12e87b99d0850e204ce03840a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dad321e104162329e85cce8b34b65774c49baf98fe0403ca974c65c447b76d`  
		Last Modified: Tue, 07 Jan 2025 03:23:22 GMT  
		Size: 44.1 MB (44076100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:dad356e76796a093786564a47a7bc4d73dc296e1ba82840e38d2e14cb4f9f27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 KB (277436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c8901cc99d770bfff2060caf777659877d70c71a83bde797ff0a886bf166df`

```dockerfile
```

-	Layers:
	-	`sha256:f1748d6a507a590b66072643cbad1147488a07d2681108203b58efe688049df5`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 262.4 KB (262422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f493617cff73ba003934ad797b7a2c926ff851c06dca4baefd4d76581a5f725`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3-slim`

```console
$ docker pull erlang@sha256:11c1a486f7ec0742a5867cbe8091012fe7dbf491621321ec28370a8b51f5c82a
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

### `erlang:25.3-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9c66656774caeb31ff8e84d70bcabe11a4234787fb77c72c9073466ecee5a04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119665330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546785f7bd908d4ecdbd3c51642db19c5a986af91611e6d3de751a7e19e3ef91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c71e0da37644431c6c87a465134b3af8cd72bfc700526f8b1ee580d7dce6a`  
		Last Modified: Tue, 24 Dec 2024 22:33:14 GMT  
		Size: 65.9 MB (65926373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b004ebb71cbbb51cc85a32f2d131716f5c35530a05be805285ab4d52949b2a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db377855df50e0e44a68423aad17334a9a989aad9657a926738ce9ad2394df75`

```dockerfile
```

-	Layers:
	-	`sha256:566a41129ab05daa388e957a7c717d74c97824fe52fd82ef02ecd9455aba7451`  
		Size: 4.0 MB (3991231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb8f99660e4ca9739df9c177e7341fc16d48b692c575347b43ee5ba6ffb6fb8`  
		Last Modified: Tue, 24 Dec 2024 22:33:13 GMT  
		Size: 13.6 KB (13610 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:56b59bf3e740177706e6d19880326564136e0db6ed2459edcc1065f206afd6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106238070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8de36cc639605e34868597df42bd63003ffbdc245e02eff77bca7a3f8d9ee3`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcfa8800dd3a9423fb0dae51c28af48e6ccf296d881f17ee1b492cda97654b`  
		Last Modified: Wed, 25 Dec 2024 04:05:38 GMT  
		Size: 57.2 MB (57213304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4beba43747968d4e6013707e95696337e2025dd3254c3fcabc537596c8675c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8732d9d5eb47073b5a9f4612c27582b4584c39d969726b0f20c45a19503b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:c41ef693b60f57ec4fcf77b44e802ff582535ff84ea56011cf7c475f4a7432a5`  
		Last Modified: Wed, 25 Dec 2024 04:05:37 GMT  
		Size: 4.0 MB (3992832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca9e3ae75e6aff3d0a6d12e3c7ddfdc2355885a142f626444088a86abfc33d7`  
		Last Modified: Wed, 25 Dec 2024 04:05:36 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4f4573e46974204ba5efbe6ee1a763f16138b13823b8374251885e67bd27bcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913bc4e20504be1c624d0d38e5e81b001df57c072692df230babbb271a616fc`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1855fe22bd18bf42b3fe5cb07e311bff8cd160d07f8c6281d921265bb2b31`  
		Last Modified: Wed, 25 Dec 2024 02:08:59 GMT  
		Size: 64.3 MB (64291421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:09e2a4d332f3948b97008633087ccd2aa1d36faea0c36a01d834fe3c27e5a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032b4cf5c0b713d92bc0d562f64e68d2e30352812fff6c1c0124cdf7fe7c72ac`

```dockerfile
```

-	Layers:
	-	`sha256:ce3b56c07836790ffac725433537e4d7618e7a9c45f4b451da0fbd2ec3be760e`  
		Last Modified: Wed, 25 Dec 2024 02:08:57 GMT  
		Size: 4.0 MB (3990852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1eb53fdd8ee2e93913b5f68aac2bb2630964f85778024493106286dc1c566a7`  
		Last Modified: Wed, 25 Dec 2024 02:08:56 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3-slim` - linux; 386

```console
$ docker pull erlang@sha256:092e5560f3dfbada6be0e77efd6efa406c0a4db269fda69da4dfb402eb89e7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112281359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c082ae443e1f6669a78bfc734694668cd07a44371b154b30c4f7eda21dcff`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad11c813e13a388055f5ad57bbf6dc37024f63a02ed4474d52493c988d9438d`  
		Last Modified: Tue, 24 Dec 2024 22:21:45 GMT  
		Size: 57.6 MB (57605343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eccd3194dee83762cf828be38b1f07f93cd57e6413e876faeed249b11142a92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c945cafb12ca9b75c3414ca4a940408712c31736f382c8d2f7067fab8abc390f`

```dockerfile
```

-	Layers:
	-	`sha256:f714a054c81032f54f16f6f32d3dc266dd87c71f5144e7611a7b286413857548`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 4.0 MB (3987709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2492441d0c4b41069bebea5c113c404a24189b02b4b56d4cf0b3fd0e21ca76f`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 13.6 KB (13578 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3.2`

```console
$ docker pull erlang@sha256:8cd12c5bd0a1f32371ee732abe3a1d015383687d022336e0aab43e024f905f9c
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

### `erlang:25.3.2` - linux; amd64

```console
$ docker pull erlang@sha256:faeddbe16324a853d7e07125a45a9841fb16dfdf5ce65602b2da080db6d60a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571518612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15e502d7197b71f9ec3795a1074a6e7fe245262e4e3e7c55e7e3171c6b11912`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 07 Jan 2025 19:49:56 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7cd6fb37363fd1ec16dad3463ecc5820eda12c418a82b4849604252d29b88`  
		Last Modified: Wed, 25 Dec 2024 00:13:52 GMT  
		Size: 197.1 MB (197073889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdbda8d0d800b0704ebeb21a5e96c5a411e8a2a0cf2e38eb986ac03165990f8`  
		Last Modified: Wed, 25 Dec 2024 01:27:53 GMT  
		Size: 249.4 MB (249377872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793eb42ee5cfeb39ad6827f04f070865b95745fd7c0bfa902bb484a0649cef8`  
		Last Modified: Wed, 25 Dec 2024 01:27:49 GMT  
		Size: 198.6 KB (198553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419d38573bb24840af385a66e1b43641b2ba5bdee928f45585b06aa0ab34e88`  
		Last Modified: Wed, 25 Dec 2024 01:27:50 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2` - unknown; unknown

```console
$ docker pull erlang@sha256:cb7886e84f754a3732480055a21947bef8e7c63c9fedfb37fbc14fd3697c1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22879315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f3376dcbd4ca4adf5eacf288a8d9c4e8968455d94bd5be89b77092d7f8bc92`

```dockerfile
```

-	Layers:
	-	`sha256:41f0a912b43fe106fca56c664119e847a6eea16b14da884ec8fa5d55ab270867`  
		Size: 22.9 MB (22860271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0f98ebe162fabb096e1b6b64773cd3d66172052298fb35277a6dc6ea3b3d58`  
		Last Modified: Wed, 25 Dec 2024 01:27:49 GMT  
		Size: 19.0 KB (19044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2` - linux; arm variant v7

```console
$ docker pull erlang@sha256:e6a226cee1bf653dacd5b957c36724ed4b7a7f1693b56b7595d43a8dde5c2ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.8 MB (503830714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ba67114d09e16d40dc8893d47255ae7c1348cd0e62b331390af13cab9ffef`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517098c11280c0a16a5adf19faec34c41bc2e558fa96b528234445b76c3b6f5`  
		Last Modified: Wed, 25 Dec 2024 15:47:48 GMT  
		Size: 167.5 MB (167525588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87b0018d16c5606bcb05d4254c94f3711f9d0b2c094aa9552f18a1c22f6d82`  
		Last Modified: Wed, 25 Dec 2024 17:10:34 GMT  
		Size: 220.9 MB (220949815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d47c6304486ed3b0e3d4131619aca7337530920d0ab58b4c5df7e158933461`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 198.6 KB (198555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec436bbc722d6626bc7b36077484dfbb9522ce98f6000d6585696a93cc4d7567`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 817.3 KB (817338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2` - unknown; unknown

```console
$ docker pull erlang@sha256:f2a7317a55701ce9af91b152c0cbba5c23e71c2179ad7293258a5b0a3f0de7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6265cbc0d9ba6f3279cdbd87125047650ceef34f08ddcb377bb087dedf00d70`

```dockerfile
```

-	Layers:
	-	`sha256:33c438925dce9e5ad1f038b2f25bf27d20448aba4814c5b34e122c7f6844d697`  
		Last Modified: Wed, 25 Dec 2024 17:10:29 GMT  
		Size: 22.7 MB (22668731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414513c0c4b80957d279a015614551afa002d0cac95cb1efc9be9ae412aaf71b`  
		Last Modified: Wed, 25 Dec 2024 17:10:28 GMT  
		Size: 19.1 KB (19146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b0ded875551582d6d5a7c4c8847281b1a955f265b1cfc5eb62438a9ba5f4777c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.7 MB (552710538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9701cb9cbfa6ad14de9d42f20be2cd4aee4748327cc9b90a4d28d0de5bbbe99`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a1cc9d544a8922ba3677890434e8976f050385a3082843ff3450d56751b6d`  
		Last Modified: Wed, 25 Dec 2024 11:20:48 GMT  
		Size: 190.0 MB (189979891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd93a08350049dc2dd4954376eace30ff99c125ab4378e4323ddaee84887a4`  
		Last Modified: Wed, 25 Dec 2024 12:44:25 GMT  
		Size: 239.1 MB (239072593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4513a80b05b5b33d82478481f5a651414f47624b776a5790cd2176ba15c8ce9d`  
		Size: 198.6 KB (198567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587bfbe46fc9df02ca8f975c053c9d687170e7187ec79355d5419580f5a7e0f`  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2` - unknown; unknown

```console
$ docker pull erlang@sha256:f7b249adcfce1b775d08474b39d53e2afbaf4662cf60c8444cad463565c65953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045554a56755ce8d118d01b161601c187ee4c02e1b2e48e5b472c750e565f80e`

```dockerfile
```

-	Layers:
	-	`sha256:b66c7e9c0a0c6dd1d8d4f8f357e45e819f24c3d4a97cfb6ebcc56aa4597a46b6`  
		Last Modified: Wed, 25 Dec 2024 12:44:21 GMT  
		Size: 22.9 MB (22870001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014eab792f387ad658ec211a03672eb10ba6e9120f5bea0b3eb6861089cd7c4f`  
		Last Modified: Wed, 25 Dec 2024 12:44:20 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2` - linux; 386

```console
$ docker pull erlang@sha256:ada9001ab711ec66ff96eb64dd5cbb89ee9b149e89f916d695bb1553444a4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.4 MB (568436449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2dc449bdb3db240f9c6e6e05f2ce15380c11b21dbaf46bcd28e60b0b4fce53`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81eaf89c71deeccff5032fb66ad17529f3c7242a3e6386d12a03c1273265281`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 200.0 MB (199979533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb9a99b80f16f6337bf0f4100ede97026cfde98cb0ba85b9b0b013cd9a8e9e`  
		Last Modified: Wed, 25 Dec 2024 01:26:36 GMT  
		Size: 240.7 MB (240675953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6f3a40450df4b3ea1ea15c0bd165b6a84ed542ebd03f0cd2b04de4d0a9931`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 198.6 KB (198550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad5ff82d89172480bf5c2ef969afed055fd3fcbfff4d2763441e5e6330f60c`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2` - unknown; unknown

```console
$ docker pull erlang@sha256:e068d6833d265612ec46b081232ed260ec1b392c48ceaaa75010b1e4525d39fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22866862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442871334defb357c8cf4e8229dae55900910cf7d032d9b59b3338f2dc7395e0`

```dockerfile
```

-	Layers:
	-	`sha256:27c9effaaaba62a04fbf0615cc4853d09587a62702e54acbc8ddbbe55a049b5f`  
		Last Modified: Wed, 25 Dec 2024 01:26:31 GMT  
		Size: 22.8 MB (22847854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1398d7f027f5bc0d5cbc49fc26f5a91a1a14d25311bf9325aea271d3121d1606`  
		Last Modified: Wed, 25 Dec 2024 01:26:30 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3.2-alpine`

```console
$ docker pull erlang@sha256:9aa024b6dce94c1dffee75f9391c00752215ce9d9c1ffa82908f7252f7da943b
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

### `erlang:25.3.2-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:363574cd3ef7bbbbd99b0f5999c944db5c2e13598d6ec65b353a8a81f31ed726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49014926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6b5edd8dd82b8da1dfeb62653addcd872fd587dba746fdf0bb4df2c02300aa`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4bfe9d39936fdffcca98a58cc959e7aceb4a0ca840cb946df9c454b453435`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 45.4 MB (45400927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:842c706d2c52982d3e37172a30e398e24b0963013810c018e9291365f351b740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 KB (282191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50581b4be831d6a5931f237cd389d5234125e57e284fae6e2636006d140ac0b3`

```dockerfile
```

-	Layers:
	-	`sha256:f1d7746bdeea19584bd225c3c142345ab8884b24615f78bf121f58704b8f8c13`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 267.1 KB (267145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407199e47888d46841460f72f4c6fa3d87948ab15f5cb28633a6153612b31b1c`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0408842e075d1fde581fa121b4177fb5678ab5488c68300a7a0944a739302c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46235955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba1751ea5976ba7b5d922d98ea89be208d45263b319beef1522717b968831be`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284ab9ddbd0e63f3b9e1fb169a281ed66936eecdf8e9a5cd40ef1f0cdf89fda`  
		Last Modified: Tue, 07 Jan 2025 06:37:39 GMT  
		Size: 43.1 MB (43144667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:30ac975454e04aa1fad424f9be33175975011288c85e64ecf671c7dc8d3827cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 KB (278342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d18bca9d94903ec58edcb5b03d2e880d6649215236504c4f6018f2d1f7fca`

```dockerfile
```

-	Layers:
	-	`sha256:700166069041b8e911d845e926cb37a97828023159e9ac210e3dbc57b7b8c5a7`  
		Size: 263.2 KB (263220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d354df2421d3330cc634ea2f867be75d49f24e26ce2c165e5091cd5368770ab`  
		Last Modified: Tue, 07 Jan 2025 06:37:37 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3cc2d3ff417548146052e2ac990ae544d3002cdb8a9ec6dbe7b45b23f82e857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49306954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ccf1efd13fe1550e8ebc7d02b417216cedc702724ccd6df202aca78f522302`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c293a0aee2fea9db3345340ce9abab5f2af37bf6a14bb90c04429cbfa94af7c`  
		Last Modified: Tue, 07 Jan 2025 07:40:52 GMT  
		Size: 45.2 MB (45220268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:a11e18d5cbc8d9e1014f7c6bbb6dc2a98341b1433f0f27bc23a37b375081a047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 KB (283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d51ad83104e745196934ea3afe378115de706cca0e68d2431201e92896394`

```dockerfile
```

-	Layers:
	-	`sha256:dc5db9fc29104734c69d95459b2fb0202f16bf016769b1a9d78a24f3242f2162`  
		Last Modified: Tue, 07 Jan 2025 07:40:51 GMT  
		Size: 267.9 KB (267938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fa229e176f678c4a3d3f5570cf299bf7df12340c20cd63f3e5e626a6dd2cd7`  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-alpine` - linux; 386

```console
$ docker pull erlang@sha256:12607f9599b4feae051bdf7e0ec5ec05b33bba6f0df763c0ebeb645ad538f0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47539289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc9a99fa8f71f415c4d77b4297af88a54933ab12e87b99d0850e204ce03840a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dad321e104162329e85cce8b34b65774c49baf98fe0403ca974c65c447b76d`  
		Last Modified: Tue, 07 Jan 2025 03:23:22 GMT  
		Size: 44.1 MB (44076100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:dad356e76796a093786564a47a7bc4d73dc296e1ba82840e38d2e14cb4f9f27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 KB (277436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c8901cc99d770bfff2060caf777659877d70c71a83bde797ff0a886bf166df`

```dockerfile
```

-	Layers:
	-	`sha256:f1748d6a507a590b66072643cbad1147488a07d2681108203b58efe688049df5`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 262.4 KB (262422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f493617cff73ba003934ad797b7a2c926ff851c06dca4baefd4d76581a5f725`  
		Last Modified: Tue, 07 Jan 2025 03:23:20 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3.2-slim`

```console
$ docker pull erlang@sha256:11c1a486f7ec0742a5867cbe8091012fe7dbf491621321ec28370a8b51f5c82a
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

### `erlang:25.3.2-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9c66656774caeb31ff8e84d70bcabe11a4234787fb77c72c9073466ecee5a04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119665330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546785f7bd908d4ecdbd3c51642db19c5a986af91611e6d3de751a7e19e3ef91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c71e0da37644431c6c87a465134b3af8cd72bfc700526f8b1ee580d7dce6a`  
		Last Modified: Tue, 24 Dec 2024 22:33:14 GMT  
		Size: 65.9 MB (65926373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b004ebb71cbbb51cc85a32f2d131716f5c35530a05be805285ab4d52949b2a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db377855df50e0e44a68423aad17334a9a989aad9657a926738ce9ad2394df75`

```dockerfile
```

-	Layers:
	-	`sha256:566a41129ab05daa388e957a7c717d74c97824fe52fd82ef02ecd9455aba7451`  
		Size: 4.0 MB (3991231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb8f99660e4ca9739df9c177e7341fc16d48b692c575347b43ee5ba6ffb6fb8`  
		Last Modified: Tue, 24 Dec 2024 22:33:13 GMT  
		Size: 13.6 KB (13610 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:56b59bf3e740177706e6d19880326564136e0db6ed2459edcc1065f206afd6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106238070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8de36cc639605e34868597df42bd63003ffbdc245e02eff77bca7a3f8d9ee3`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 07 Jan 2025 20:08:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcfa8800dd3a9423fb0dae51c28af48e6ccf296d881f17ee1b492cda97654b`  
		Last Modified: Wed, 25 Dec 2024 04:05:38 GMT  
		Size: 57.2 MB (57213304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4beba43747968d4e6013707e95696337e2025dd3254c3fcabc537596c8675c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8732d9d5eb47073b5a9f4612c27582b4584c39d969726b0f20c45a19503b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:c41ef693b60f57ec4fcf77b44e802ff582535ff84ea56011cf7c475f4a7432a5`  
		Last Modified: Wed, 25 Dec 2024 04:05:37 GMT  
		Size: 4.0 MB (3992832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca9e3ae75e6aff3d0a6d12e3c7ddfdc2355885a142f626444088a86abfc33d7`  
		Last Modified: Wed, 25 Dec 2024 04:05:36 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4f4573e46974204ba5efbe6ee1a763f16138b13823b8374251885e67bd27bcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913bc4e20504be1c624d0d38e5e81b001df57c072692df230babbb271a616fc`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1855fe22bd18bf42b3fe5cb07e311bff8cd160d07f8c6281d921265bb2b31`  
		Last Modified: Wed, 25 Dec 2024 02:08:59 GMT  
		Size: 64.3 MB (64291421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:09e2a4d332f3948b97008633087ccd2aa1d36faea0c36a01d834fe3c27e5a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032b4cf5c0b713d92bc0d562f64e68d2e30352812fff6c1c0124cdf7fe7c72ac`

```dockerfile
```

-	Layers:
	-	`sha256:ce3b56c07836790ffac725433537e4d7618e7a9c45f4b451da0fbd2ec3be760e`  
		Last Modified: Wed, 25 Dec 2024 02:08:57 GMT  
		Size: 4.0 MB (3990852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1eb53fdd8ee2e93913b5f68aac2bb2630964f85778024493106286dc1c566a7`  
		Last Modified: Wed, 25 Dec 2024 02:08:56 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25.3.2-slim` - linux; 386

```console
$ docker pull erlang@sha256:092e5560f3dfbada6be0e77efd6efa406c0a4db269fda69da4dfb402eb89e7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112281359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c082ae443e1f6669a78bfc734694668cd07a44371b154b30c4f7eda21dcff`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad11c813e13a388055f5ad57bbf6dc37024f63a02ed4474d52493c988d9438d`  
		Last Modified: Tue, 24 Dec 2024 22:21:45 GMT  
		Size: 57.6 MB (57605343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25.3.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eccd3194dee83762cf828be38b1f07f93cd57e6413e876faeed249b11142a92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c945cafb12ca9b75c3414ca4a940408712c31736f382c8d2f7067fab8abc390f`

```dockerfile
```

-	Layers:
	-	`sha256:f714a054c81032f54f16f6f32d3dc266dd87c71f5144e7611a7b286413857548`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 4.0 MB (3987709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2492441d0c4b41069bebea5c113c404a24189b02b4b56d4cf0b3fd0e21ca76f`  
		Last Modified: Tue, 24 Dec 2024 22:21:43 GMT  
		Size: 13.6 KB (13578 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:25.3.2.16`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:25.3.2.16-alpine`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:25.3.2.16-slim`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:26`

```console
$ docker pull erlang@sha256:ed1400b304a7a39666662880fb58fc820e9d8ac5eec78035f28253992be34e02
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

### `erlang:26` - linux; amd64

```console
$ docker pull erlang@sha256:33ca4296eab483162c77a10945408a739061c85371b60a9fb237e50862583708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601308199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7305659e92e12718e2961d55df9945e473548fbf2bbbe1ec58af57e9e40045`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 07 Jan 2025 19:42:38 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 07 Jan 2025 19:42:44 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad3923e92788e6116cbfb84ad3949b53f2330fb4dec5b140cfab39fb3fba9b`  
		Last Modified: Wed, 25 Dec 2024 01:29:03 GMT  
		Size: 252.2 MB (252234737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b903ded9cf0dd702b5a6cc9241a1d344eb18ecd6baf9ef48f87b58b72f69d77d`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 194.9 KB (194929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b3b612600174adb0899c01390407558e0c6ea66219a3100234bdabc46dd10c`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 818.4 KB (818375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:cae7c61ab3d7c7b365a02d0426a5556ec6c3df2e8b47d626939e70b4e020fd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22706526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f15a9b6702508541307f8f285d8c2b2a4b1282a057767abb81c620345aad2f`

```dockerfile
```

-	Layers:
	-	`sha256:ee441009cd3bc7d653da62433cd793dd51150a40da4309a41bf0f595292235f6`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 22.7 MB (22687509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded2b234ced333eb44be4ab4edcf13132c5b01f61c255267ece859ab2c658e02`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; arm variant v5

```console
$ docker pull erlang@sha256:c47834683cbbcfdf596945051b721336be52b1b59c7b9d89de9ac4d113dfe428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542841883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b491cb8906936009fd157098cf5eb3bda6b351620555bb91fd860bea7d8de`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397934db677d27dbd0599257dd9cdb7e2f5bfbf61a63d5277b1a3d26a7f782b`  
		Last Modified: Wed, 25 Dec 2024 07:28:33 GMT  
		Size: 226.7 MB (226665910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c355ca1c15debc541949c0e60995c3899a8592fca95983362a3a4b799b0c937`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 194.9 KB (194939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b515f7e1b5c411acde26c3f3f3f161f48c92675b9918bc05b5fa76f04e899`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:272ad89706868ea3e65f450f599a6e2f5ba77d21dd13189927d82a155b826c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22505226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892b566b47b78ccc1d467a5b7d71d4752bf70b5ec410fddc705f4b5753803859`

```dockerfile
```

-	Layers:
	-	`sha256:87e9fe6ade2272821576431a83c201cde540e66cc549df92aaf9263e632ce686`  
		Size: 22.5 MB (22486107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b0dbfc907673a6ac6f1297ca91b98b159140c533641761cd5c6009baeee6da`  
		Last Modified: Wed, 25 Dec 2024 07:28:27 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4ba19d4389158a182cead4428e588c89e0271a30461700c2a4bcad20f27baaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.6 MB (525562351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d10c0cf8e4888cc99ec2b33978eea3b5ed4e1cc5bc9c6aa3f2d909b1ec310aa`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec35f0d61fac60686d2f30712acd1f65eec4d41cc39402c7407d01ab5fd04099`  
		Last Modified: Wed, 25 Dec 2024 17:02:32 GMT  
		Size: 223.7 MB (223699867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970195692be1a940628eb663f41abd075864249c58061e92ebab300d495d95a`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 194.9 KB (194906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069bd4d28ffc02686245f547fb011cff88b8d82475ca57689418da8f173773e7`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:96d50334ecbd114504211ed8a8fc57296f16d619d39f0e9d6e79b6db412f2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22522121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f616e211f20e7dfb8f057e913a4a4672a9f112b71ef8b7b5773d9138870d9e`

```dockerfile
```

-	Layers:
	-	`sha256:b894a3dde3fde1aec88da8037d5c7396c23946a420d9ed012e0b33e9a50f0079`  
		Last Modified: Wed, 25 Dec 2024 17:02:26 GMT  
		Size: 22.5 MB (22503002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab97c806731a12fc65da8ce845d5fbb7d1271c23ebe7c52570cdb845d25c03f`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:76741f5c728364bdf8ff16ce53a360bf22a03ee7a2741aaced2db55adb65adf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (585043434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc4412e312b030446298fe9138b6ccca03f511209ba0337631ffe3328165362`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c411cf62d39b47b837d578985ab77a50ea1fbc284551a3aa0409e87def9a0`  
		Last Modified: Wed, 25 Dec 2024 12:37:31 GMT  
		Size: 245.3 MB (245265034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4c8864c5581119b788071f338dc1fa6f107ea62d0d97be278c837130748382`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 194.9 KB (194920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c051967da3e5ee21a867e30ce74ff1890c9c929b8e6fd7c7d73333286388bc39`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:1c5b9decdb56e7fdddd6e761ed66200e0cf1b3dee5522ccb536e7ca8b2267954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22746701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbfe22cabf66cff2b83991eb77a89ed643e07e9a3ba56c37842859b42867207`

```dockerfile
```

-	Layers:
	-	`sha256:1348c030aeb3b0dd387cfc108ba90397cef260c6068dcfb1435619cb46d151bf`  
		Last Modified: Wed, 25 Dec 2024 12:37:26 GMT  
		Size: 22.7 MB (22727550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d1c840487e4f8db87c26b35eb175320fc95dabfaf43c7cf69bab06e61a9205`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; 386

```console
$ docker pull erlang@sha256:0964d5a81ea1063c46298287ccc7de183f79a2197da131ab6847f926930ae9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33627c476a6d607a84581983de47a18edf72323019bd51f5dde0c83d9528087`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b325808dbceff48bd87caaf06d755e8f301da86a23bc920d9396b55662b024`  
		Last Modified: Wed, 25 Dec 2024 01:27:48 GMT  
		Size: 246.3 MB (246253926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d8ab98e13a799ba5d3bbfd84b010ff4dad686ae35556d847a447e4491a5c6d`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 194.9 KB (194921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a52f9a18f1146348cbeca5a78be065e77e59b72c78187e0ed7046e7689aeb`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:1f77cf80ba750c94bdeaa23c1b5e7146d3c23b29202abc24c6db08da5ce13505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22674672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4aa12d1991687d7f3d10a1d7d17e1661a397c181f9ad1dd6faf8492452a460`

```dockerfile
```

-	Layers:
	-	`sha256:7a21e628b24dd19dd64e73ffd96c59bb18fb288b16259ebd784b1936fcbfd9e8`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 22.7 MB (22655691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136fea54ca6c6618eec5f838bf6a55aff1190c3772bfb55deba22cbaad28af5a`  
		Size: 19.0 KB (18981 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; mips64le

```console
$ docker pull erlang@sha256:30d8bb1e49a074a98daa66c77616287e0b3de6ee565ee1ef1efdaedb94df7bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.4 MB (554444139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eecd64bd1d17034d277c88f069adda59d52f2d425e8abed5a8606e0780765f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63286a1209cbdc1c275298e13fe1bfa10fc51dc83765b2a824950a61db918afb`  
		Last Modified: Thu, 26 Dec 2024 03:14:36 GMT  
		Size: 228.0 MB (228041570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae72d3525553c4072dc4a6b07be77372518c2bff0c7a0d535277097ec1dc3ec`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 194.9 KB (194892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305300a46c2c64336de750c215a25e2ab4f9de3ffb5e5b42ee49dd845cc6966a`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:21128996e4ae5dd249f65a6af7650d4caf3706f875bf18c626eb5a3ea721bd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876c203b625cdeab57609f863669bafaf9c28fc44cc409c1c736f7a4f27041fb`

```dockerfile
```

-	Layers:
	-	`sha256:7578e0b4d2da83dd0317773b14a6e3cf95c9c7c77a208a941912a309c2023cc4`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 18.9 KB (18874 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; ppc64le

```console
$ docker pull erlang@sha256:4c6b08585085ec88fd5ff20953955acf4837fd5165fea62953fd8ace04bad766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612528323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7a4a4960a634590af6bdd1f65c8b5875b69ec50584eed36320c09d448765e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dacb78300d7562438fc131ed143b37a7156329b71fc87772da342b057b2354`  
		Size: 249.5 MB (249511846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa91d252a553e2e8069a864c5a15a7aa2dc07b8eaf6244b59e56a1ed76b99b8`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 194.9 KB (194933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60821f5123497b0fc0640668c2145edc82b3cdcc6291f87eed71b0361e29e52c`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:bd55cea6c2c36042c767eb03ebedd91f432b241c3e6891aa949807ebe6a41aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6fde1edd923b038d52a0c47a914824c43deafa2c2e7989d367192f7560cf7`

```dockerfile
```

-	Layers:
	-	`sha256:f73b1bddfbfd286c2f9c1cfe87d20d0ece8861963c1c6c6897a2510b0506caf5`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 22.6 MB (22643187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6425215072f4c3fb74b25559d521cd4d4c519ef51b9117d882ff67c5ae23a60`  
		Last Modified: Wed, 25 Dec 2024 15:27:56 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26` - linux; s390x

```console
$ docker pull erlang@sha256:1963feaa7dc9f7566e7229c600c1d02811d9847395e48a7638b7ff08d23dda63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.5 MB (553490119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5531bdf3f7d4b0b776d811f6db1a62285a219cb993a4475311bc7342098dccc`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f854986e8bdacb00c948da96265abf8d73da298a0e4ebf175ebbd706a79956a`  
		Last Modified: Wed, 25 Dec 2024 06:26:29 GMT  
		Size: 234.7 MB (234663730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de8334711e0ec36026e31eef49190cf99f12ed4105b8d4a50c4029ab129229`  
		Size: 194.9 KB (194917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a2262a940334fcbcc90186c8d3d12e776dbb46f9672846593ca0b2bafeb09`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26` - unknown; unknown

```console
$ docker pull erlang@sha256:c6dd99957dbf5e083fc9f19e02889c02b01238950f5bce0722545db84ffda77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22480239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27195c5019fcfbe8ecfbacd35977f37b80a27155ebd9ee95ffc3e9a1d0d7db77`

```dockerfile
```

-	Layers:
	-	`sha256:f1d75a566130ef9b0bb741c8d068649c30bb310fd50f9e2ed987f9d22e5918d0`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 22.5 MB (22461222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a38ee67ca2ddbff733d6a6a6bd3c9cef9220d5020c265c3548e513f12b1a74`  
		Last Modified: Wed, 25 Dec 2024 06:26:25 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26-alpine`

```console
$ docker pull erlang@sha256:0acb632217908970082f38852dbddf5142eab55e4f447f5fb91c69984b2d4b84
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
$ docker pull erlang@sha256:acbd326ac9f3e1b446a455b8c67b105021bc050c71a37d2cd8b43b8fe9304d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49608095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b1deb54f95e83a62501b5f4f201fda95134befdca43a7a9f364745fd8aa8a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d341b0c0baddc4e1544584026eab3673c2cdfad56878b5c20466add57e8263`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 46.0 MB (45994096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3bd8e93393c6f761a8d6aca03d5358a98ff5555355046937a177d4c8f66867f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430d9378ce090ed94dd81031d29394763313f5274b3300b8238950bca55a5983`

```dockerfile
```

-	Layers:
	-	`sha256:e431a6dea0d5141cb3fd5392a3a8e442d47b99e0907368f6d7f4e5ecac02cb32`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 267.0 KB (267035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24ea22e3b9ab67a85b644d176ba54f27fbf9b2c0e495977096d53222e789f8`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0e5d34ae97925ff4ce9cbd515c606bc9a1294404a33fb0cad1e8965644942b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46754463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7e714d85f4b782da84d0a81fad72f97905649378bd92e27ea5d54d8443470`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f07b1899d4cf55307ea151685037b83600807cfffbc36b169318f70ce07e92`  
		Last Modified: Tue, 07 Jan 2025 06:33:14 GMT  
		Size: 43.7 MB (43663175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:07a7ef3c604c992ac72b64dfb3977a8134fdc698d2ccd2f3c11c154a895aaa8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 KB (278228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3d4f39a211e1e93ad82beb931eced300d6209a3949e4b4b5cc57e4a2a2b9bc`

```dockerfile
```

-	Layers:
	-	`sha256:91ac92dea26c7f474820e0f8966f29a7596138e25c06c05a08ba9dba22fe0b5f`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 263.1 KB (263109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b048c6b1ba3369feed0b7d89f12376d5ba88e716da2eb5a0533d5828ddbd75`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 15.1 KB (15119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f44244a69e1a64526ef5ca4b5121c71a1f5b69d8fd203e996e3f5b406cbcf69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49877058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a189383b2a51b1c058f4e46b5569b71331198db906c6b107a43134d605e8d381`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585de24540b1a08dfffc3670348e6266c82ca8cd13c82d761f3a39b750bf341`  
		Size: 45.8 MB (45790372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:2d721c52aba3a2acb8a158932d9169a6c5d164c1edc6b05277a4f703a05753b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 KB (282973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750702f24a21e5d6b32a6020c53832d6d730c43150e09d324b07ba552b912a32`

```dockerfile
```

-	Layers:
	-	`sha256:c7bfd97feed4cd9ec2e6c50450153150e3b57a38fcbb6ad70c5b3f03a35192ab`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 267.8 KB (267827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a975126bc0dff14240f2795b75b6ad60cd2972d0be11d7c57415e04bce416a0a`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 15.1 KB (15146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; 386

```console
$ docker pull erlang@sha256:9e53d0f711bd5c575af496c6c741a698185b38e40e923cdf3728dc7cd3b32d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48065746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a59f89e6e754e1de9eaab8209a72a27ec4d526ceb4f8c1e50c7ee57e50c79b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d9754cd1babeb033f2dd6a0efc8eb0315a0694ca165bb6da164526545f756`  
		Last Modified: Tue, 07 Jan 2025 03:24:02 GMT  
		Size: 44.6 MB (44602557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0443c7c8e6ebab82c769ac38dcde6adc3f032314d8b88791cccb8b9a24560a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 KB (277323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7d86f895880f5e071e29e95ab08607577fa63dee23a3c4b881ff5e41a28149`

```dockerfile
```

-	Layers:
	-	`sha256:2d0d098a6c9f8dc99c03a301564a3261886860e77a00120ef232a08eab517ebc`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 262.3 KB (262312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b351b38eae7e21841aedb67501d5dd4614d1b8696898df3b8457990b04518448`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:a62a665256713fd74be522a465d4412ed71749eb8101a716dc5ebe8747fb8d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48222892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a6d0b3369807d752c7635fdedf59148b4525da648ad92a8c29a1f16c21d0a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a439a30565a16dca74b577c9f57742d9c6587756db9315fe004e2119e444369`  
		Last Modified: Tue, 07 Jan 2025 06:32:17 GMT  
		Size: 44.7 MB (44654165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:683c1f77b47ec10aa08673137a4b3ae6f8b2c3ac63c21ac6558cb3c0afc80c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe969dcbb43b548f237f23004b7b3b1ee743b0bd364d54444f6a3d12e67ffb1d`

```dockerfile
```

-	Layers:
	-	`sha256:c291da8439cecc4dab1c52376513fc5913a9a4f434c4c82add01d5c4a8a5d3f9`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 261.2 KB (261156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378ca39982a195b28744efbeebc56e5805e0adade253a02ebd871d2280a05861`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:5eaa0d4d0cb5a870360a56354958358201ab637e51bfc6cdb55e00ff88544f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47772736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba9649446d28fd5cb2b3311c9798aeefe3ad17afbc2e149d3bc6e8fa48186e7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e6de505a368a8e02977d779b3df7c0f324eca3a30a8c4945d6ddf05ff4147e`  
		Last Modified: Tue, 07 Jan 2025 06:39:35 GMT  
		Size: 44.3 MB (44313557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3aa6c8aeb9fb9117414ef71320e0cd8fdc1df6823959ed6b8bc2b37c9c02d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378bc1a503550361fd9411ade08b8d0cf91691464f44a9e305535bfbaece6aa`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e86acc678c6e49f9e047f3bd8b19a8be0140c1c4f104a756e7b67c6ee6a4e`  
		Last Modified: Tue, 07 Jan 2025 06:39:34 GMT  
		Size: 261.1 KB (261122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8fc60132e965e5ea326b83ea51b09fc70c7152cc277b250d7fbb290a215968`  
		Last Modified: Tue, 07 Jan 2025 06:39:33 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26-slim`

```console
$ docker pull erlang@sha256:fe2d30f39895efadf3887717a4ebca7f920c6f12558bc36d3632d055b27c187b
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9245c33cf3623593220a37964c3584c1983c6b7fc4c8f641e4ede540dee4d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643a38794c5268db14965ca8983ece4591596243043393afd556e1a58075bdb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de85552e2280313a4b344aafb4679a335319b68c81732b638a326e2426cb57f`  
		Last Modified: Tue, 24 Dec 2024 22:33:59 GMT  
		Size: 70.3 MB (70334542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:90ae2ea8bd9d6814d3e3d56f68a87ad75fd66be1bec0582490f336f028723e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871532807198d0bd4f76879b83202ed1d90ae0aa11b9558b212aa44ae2b4356a`

```dockerfile
```

-	Layers:
	-	`sha256:11f891cd6215599e1f7f9f1479a947223f32d272afc4c9e38d0ea8bed5e61309`  
		Size: 3.7 MB (3709308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a212319339c9e70bb5eabb0139efd91053a192cd8a86b70009943612aac1975`  
		Last Modified: Tue, 24 Dec 2024 22:33:57 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:bf695ce614b9d5ec453e29806b897b3dc77374f52aafe5f6ccc2c53f86b19215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106461065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9572055074120b7fd0080fa1948ad670f41f305213023be2e233c3c8f0fc3b7`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f47e9b4117175e620492590bcc82a80b4d1c862a5584a33b4d0b5ec4133130`  
		Last Modified: Wed, 25 Dec 2024 01:42:45 GMT  
		Size: 60.4 MB (60436823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c48e6107d4ef1341541c516ebf17f22457d7a9f965c8e1a3a1cb200729e5fb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630bebe864091691f3be7a3257375d9c6f3f7533aec60d2e52a0d3d8b1f23703`

```dockerfile
```

-	Layers:
	-	`sha256:a6afb172e9898965b32c75b61aa036d67fe61e4d014a7b3f139e97bbf8810216`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 3.7 MB (3712808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec2d22e89f906422458f29a286d59f03852527258ffcd50511d864aad459879`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:13673e8653f4aecd2988b81cee08af61dfd30d5d8d3a9c612ff2be4573a0a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104262450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea6e4164fb4f648bd825d4e222e20af3e0dba82d1bd08e3eadf2321b16a77cb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe46a6c6ed9025746030b6d1a9556b74143a6d3538a61a268f6726ac9ab991b`  
		Size: 60.1 MB (60062483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c3fa33600e689fc6c06866384f547cb04c91dd974fa8637cbcc69a61f5fe0d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa8a5fc06ad3c862ac9d35e5ba4c9515d2ef51f4e374fa287ddb6baf11fff5`

```dockerfile
```

-	Layers:
	-	`sha256:2082cad6739f50ee480044c91987b8d45f75c47ab389352bd85144e408191778`  
		Last Modified: Wed, 25 Dec 2024 04:01:00 GMT  
		Size: 3.7 MB (3711541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64dfadecfd335cfaad4766ff9e94d8eff1d2650c02e73efd652de2552af5fc5`  
		Last Modified: Wed, 25 Dec 2024 04:00:59 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0bc4c0c3f6e54041c2f523a60255969f1c1b8f333317da816bb8ef56e8d2191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116293288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1889f1aa971ad46e616b559fd4f12002f981478965de556ea0b9c7d780c4aa78`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43bf59b125105e1cd69f2dfd8a490c1fe920e94085154bae98a41a43c678929`  
		Last Modified: Wed, 25 Dec 2024 02:05:20 GMT  
		Size: 68.0 MB (67967804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a3a14217cfb888619be48921566fc198ca0ffb0af37282b0bbab3d9ba9c7b7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b5cb8d9a17f6ae298d5652cee07f658dd771085eace08776be1e4f0c2bf43`

```dockerfile
```

-	Layers:
	-	`sha256:db11eb055d8b30d5f8bb19a65fde756ba4cbd1f15c31021ff411ff178c2e3c76`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 3.7 MB (3709569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1fb1db134619fe252dafa283e4081eb206596acd1551794add0a7a26268b0f`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 13.7 KB (13706 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:06e8f24c7f1af3ac3137f31536fc23e433f38b39d8d9c5aebc9cbdb10f788517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d426b483e1ad6d8b1546ec854340e2c483613c21fb5584b17eafa3ecc79c853`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca44d1694041f067ebf8d5b4f893979eacee074bbacec58ae6385ba43f6332c`  
		Last Modified: Tue, 24 Dec 2024 22:22:09 GMT  
		Size: 61.1 MB (61082179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9f164f8ff414fdd2d0e54cc8cc9b332ea90e1c998ea9084bb2ed2579e713c5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7effa791763f3965eaf81acb63961e9add2e3a07109fe86c3c433d946d940d50`

```dockerfile
```

-	Layers:
	-	`sha256:084984b2a63b0ecea2adf646beb29a555fc681e87b5a61ab6bba340da666051c`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 3.7 MB (3706428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4947521b614134d1999d00c5c5e0dc0bf60c59737b18da06e76d123886af972`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 13.6 KB (13570 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:42d8883ee031325e8ed750bde68436b20be8c107ef0e38a9eb3d59491809eb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109811275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c056dd6e56e4ef9e175e601f9c675964a1779aa5821b5f9ebe0925ed05cba91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc59f63202059cc1a98ba153f0b85086eb0bbdd85327f45bb99993b46795184`  
		Size: 61.0 MB (61039631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ed37a1736689bcf22ad1be7086a06e42870628b3981d08fb5b27150bf2abe797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cff71a74434232533d6a351f5b93d4be4b238053a6d1b7cac0e7220f5096654`

```dockerfile
```

-	Layers:
	-	`sha256:4be412e380e31e62de3dbce65645202669143e4a2f02a2fbea0b16ccbe35e25a`  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:fc6b9c285f3898a9968bf0a4680fa260d980781edba45f51c706acdddc7b92ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114484982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c07556602085c72109fc9bce13bf6556cc33aa9356f5016eec743416e5b8b6`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e71a0911f3797a4433566eb71eabaf282361f449e22480cd6c6b8daa78f436`  
		Last Modified: Wed, 25 Dec 2024 13:12:38 GMT  
		Size: 62.2 MB (62156907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bef084a7d2e34a035901876099c659e0cbe4c0c760878c21742c3c6db361239b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524bb828d0ebb1551f4e17d70fd3dd7d2e3cfd2a0930e9fe867df1cb604ad70a`

```dockerfile
```

-	Layers:
	-	`sha256:ed2de4f4544af54cf9f556282a8e230c9a98c1017451b72218a33783fa702c30`  
		Last Modified: Wed, 25 Dec 2024 13:12:36 GMT  
		Size: 3.7 MB (3713648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600402e96cbb348c729321b196ba62609b54c0c6624ae559782cc39f43aac543`  
		Last Modified: Wed, 25 Dec 2024 13:12:35 GMT  
		Size: 13.6 KB (13646 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:6d85ea70b290d20f080ac0e9555c9c0e5ff4e2fef603e30f97c75a1b9908d142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108015920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dd6a756f010ab58d19c5dd260cfba99216ec0ef90b74add84a25c56b86940`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916390e7fbffcb8b07a7fb2db15e99e02a4f0877ead918a47deaa75a606cd480`  
		Last Modified: Wed, 25 Dec 2024 00:35:19 GMT  
		Size: 60.9 MB (60866295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:73c6ea98cd52f898b9a8f2f5fb71f6fdff1acba7b103bbe84420b4edee8e3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8988e684b1ac36b391d6c10c027443e1ae5d29337c8eeb09c894856c3d77674`

```dockerfile
```

-	Layers:
	-	`sha256:a9eca79291e0f84f11c09b98550c0333af5c6410fd961091e702265c4faa5cb0`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 3.7 MB (3709028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc5b7bff5da1ea719300b49d7f0400bc865cbd984847b627d0a2ebf53d9a695`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2`

```console
$ docker pull erlang@sha256:ed1400b304a7a39666662880fb58fc820e9d8ac5eec78035f28253992be34e02
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

### `erlang:26.2` - linux; amd64

```console
$ docker pull erlang@sha256:33ca4296eab483162c77a10945408a739061c85371b60a9fb237e50862583708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601308199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7305659e92e12718e2961d55df9945e473548fbf2bbbe1ec58af57e9e40045`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 07 Jan 2025 19:42:38 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 07 Jan 2025 19:42:44 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad3923e92788e6116cbfb84ad3949b53f2330fb4dec5b140cfab39fb3fba9b`  
		Last Modified: Wed, 25 Dec 2024 01:29:03 GMT  
		Size: 252.2 MB (252234737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b903ded9cf0dd702b5a6cc9241a1d344eb18ecd6baf9ef48f87b58b72f69d77d`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 194.9 KB (194929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b3b612600174adb0899c01390407558e0c6ea66219a3100234bdabc46dd10c`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 818.4 KB (818375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:cae7c61ab3d7c7b365a02d0426a5556ec6c3df2e8b47d626939e70b4e020fd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22706526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f15a9b6702508541307f8f285d8c2b2a4b1282a057767abb81c620345aad2f`

```dockerfile
```

-	Layers:
	-	`sha256:ee441009cd3bc7d653da62433cd793dd51150a40da4309a41bf0f595292235f6`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 22.7 MB (22687509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded2b234ced333eb44be4ab4edcf13132c5b01f61c255267ece859ab2c658e02`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; arm variant v5

```console
$ docker pull erlang@sha256:c47834683cbbcfdf596945051b721336be52b1b59c7b9d89de9ac4d113dfe428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542841883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b491cb8906936009fd157098cf5eb3bda6b351620555bb91fd860bea7d8de`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397934db677d27dbd0599257dd9cdb7e2f5bfbf61a63d5277b1a3d26a7f782b`  
		Last Modified: Wed, 25 Dec 2024 07:28:33 GMT  
		Size: 226.7 MB (226665910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c355ca1c15debc541949c0e60995c3899a8592fca95983362a3a4b799b0c937`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 194.9 KB (194939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b515f7e1b5c411acde26c3f3f3f161f48c92675b9918bc05b5fa76f04e899`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:272ad89706868ea3e65f450f599a6e2f5ba77d21dd13189927d82a155b826c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22505226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892b566b47b78ccc1d467a5b7d71d4752bf70b5ec410fddc705f4b5753803859`

```dockerfile
```

-	Layers:
	-	`sha256:87e9fe6ade2272821576431a83c201cde540e66cc549df92aaf9263e632ce686`  
		Size: 22.5 MB (22486107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b0dbfc907673a6ac6f1297ca91b98b159140c533641761cd5c6009baeee6da`  
		Last Modified: Wed, 25 Dec 2024 07:28:27 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4ba19d4389158a182cead4428e588c89e0271a30461700c2a4bcad20f27baaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.6 MB (525562351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d10c0cf8e4888cc99ec2b33978eea3b5ed4e1cc5bc9c6aa3f2d909b1ec310aa`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec35f0d61fac60686d2f30712acd1f65eec4d41cc39402c7407d01ab5fd04099`  
		Last Modified: Wed, 25 Dec 2024 17:02:32 GMT  
		Size: 223.7 MB (223699867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970195692be1a940628eb663f41abd075864249c58061e92ebab300d495d95a`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 194.9 KB (194906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069bd4d28ffc02686245f547fb011cff88b8d82475ca57689418da8f173773e7`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:96d50334ecbd114504211ed8a8fc57296f16d619d39f0e9d6e79b6db412f2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22522121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f616e211f20e7dfb8f057e913a4a4672a9f112b71ef8b7b5773d9138870d9e`

```dockerfile
```

-	Layers:
	-	`sha256:b894a3dde3fde1aec88da8037d5c7396c23946a420d9ed012e0b33e9a50f0079`  
		Last Modified: Wed, 25 Dec 2024 17:02:26 GMT  
		Size: 22.5 MB (22503002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab97c806731a12fc65da8ce845d5fbb7d1271c23ebe7c52570cdb845d25c03f`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:76741f5c728364bdf8ff16ce53a360bf22a03ee7a2741aaced2db55adb65adf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (585043434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc4412e312b030446298fe9138b6ccca03f511209ba0337631ffe3328165362`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c411cf62d39b47b837d578985ab77a50ea1fbc284551a3aa0409e87def9a0`  
		Last Modified: Wed, 25 Dec 2024 12:37:31 GMT  
		Size: 245.3 MB (245265034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4c8864c5581119b788071f338dc1fa6f107ea62d0d97be278c837130748382`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 194.9 KB (194920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c051967da3e5ee21a867e30ce74ff1890c9c929b8e6fd7c7d73333286388bc39`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:1c5b9decdb56e7fdddd6e761ed66200e0cf1b3dee5522ccb536e7ca8b2267954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22746701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbfe22cabf66cff2b83991eb77a89ed643e07e9a3ba56c37842859b42867207`

```dockerfile
```

-	Layers:
	-	`sha256:1348c030aeb3b0dd387cfc108ba90397cef260c6068dcfb1435619cb46d151bf`  
		Last Modified: Wed, 25 Dec 2024 12:37:26 GMT  
		Size: 22.7 MB (22727550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d1c840487e4f8db87c26b35eb175320fc95dabfaf43c7cf69bab06e61a9205`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; 386

```console
$ docker pull erlang@sha256:0964d5a81ea1063c46298287ccc7de183f79a2197da131ab6847f926930ae9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33627c476a6d607a84581983de47a18edf72323019bd51f5dde0c83d9528087`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b325808dbceff48bd87caaf06d755e8f301da86a23bc920d9396b55662b024`  
		Last Modified: Wed, 25 Dec 2024 01:27:48 GMT  
		Size: 246.3 MB (246253926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d8ab98e13a799ba5d3bbfd84b010ff4dad686ae35556d847a447e4491a5c6d`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 194.9 KB (194921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a52f9a18f1146348cbeca5a78be065e77e59b72c78187e0ed7046e7689aeb`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:1f77cf80ba750c94bdeaa23c1b5e7146d3c23b29202abc24c6db08da5ce13505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22674672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4aa12d1991687d7f3d10a1d7d17e1661a397c181f9ad1dd6faf8492452a460`

```dockerfile
```

-	Layers:
	-	`sha256:7a21e628b24dd19dd64e73ffd96c59bb18fb288b16259ebd784b1936fcbfd9e8`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 22.7 MB (22655691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136fea54ca6c6618eec5f838bf6a55aff1190c3772bfb55deba22cbaad28af5a`  
		Size: 19.0 KB (18981 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; mips64le

```console
$ docker pull erlang@sha256:30d8bb1e49a074a98daa66c77616287e0b3de6ee565ee1ef1efdaedb94df7bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.4 MB (554444139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eecd64bd1d17034d277c88f069adda59d52f2d425e8abed5a8606e0780765f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63286a1209cbdc1c275298e13fe1bfa10fc51dc83765b2a824950a61db918afb`  
		Last Modified: Thu, 26 Dec 2024 03:14:36 GMT  
		Size: 228.0 MB (228041570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae72d3525553c4072dc4a6b07be77372518c2bff0c7a0d535277097ec1dc3ec`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 194.9 KB (194892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305300a46c2c64336de750c215a25e2ab4f9de3ffb5e5b42ee49dd845cc6966a`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:21128996e4ae5dd249f65a6af7650d4caf3706f875bf18c626eb5a3ea721bd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876c203b625cdeab57609f863669bafaf9c28fc44cc409c1c736f7a4f27041fb`

```dockerfile
```

-	Layers:
	-	`sha256:7578e0b4d2da83dd0317773b14a6e3cf95c9c7c77a208a941912a309c2023cc4`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 18.9 KB (18874 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; ppc64le

```console
$ docker pull erlang@sha256:4c6b08585085ec88fd5ff20953955acf4837fd5165fea62953fd8ace04bad766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612528323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7a4a4960a634590af6bdd1f65c8b5875b69ec50584eed36320c09d448765e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dacb78300d7562438fc131ed143b37a7156329b71fc87772da342b057b2354`  
		Size: 249.5 MB (249511846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa91d252a553e2e8069a864c5a15a7aa2dc07b8eaf6244b59e56a1ed76b99b8`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 194.9 KB (194933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60821f5123497b0fc0640668c2145edc82b3cdcc6291f87eed71b0361e29e52c`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:bd55cea6c2c36042c767eb03ebedd91f432b241c3e6891aa949807ebe6a41aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6fde1edd923b038d52a0c47a914824c43deafa2c2e7989d367192f7560cf7`

```dockerfile
```

-	Layers:
	-	`sha256:f73b1bddfbfd286c2f9c1cfe87d20d0ece8861963c1c6c6897a2510b0506caf5`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 22.6 MB (22643187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6425215072f4c3fb74b25559d521cd4d4c519ef51b9117d882ff67c5ae23a60`  
		Last Modified: Wed, 25 Dec 2024 15:27:56 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2` - linux; s390x

```console
$ docker pull erlang@sha256:1963feaa7dc9f7566e7229c600c1d02811d9847395e48a7638b7ff08d23dda63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.5 MB (553490119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5531bdf3f7d4b0b776d811f6db1a62285a219cb993a4475311bc7342098dccc`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f854986e8bdacb00c948da96265abf8d73da298a0e4ebf175ebbd706a79956a`  
		Last Modified: Wed, 25 Dec 2024 06:26:29 GMT  
		Size: 234.7 MB (234663730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de8334711e0ec36026e31eef49190cf99f12ed4105b8d4a50c4029ab129229`  
		Size: 194.9 KB (194917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a2262a940334fcbcc90186c8d3d12e776dbb46f9672846593ca0b2bafeb09`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2` - unknown; unknown

```console
$ docker pull erlang@sha256:c6dd99957dbf5e083fc9f19e02889c02b01238950f5bce0722545db84ffda77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22480239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27195c5019fcfbe8ecfbacd35977f37b80a27155ebd9ee95ffc3e9a1d0d7db77`

```dockerfile
```

-	Layers:
	-	`sha256:f1d75a566130ef9b0bb741c8d068649c30bb310fd50f9e2ed987f9d22e5918d0`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 22.5 MB (22461222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a38ee67ca2ddbff733d6a6a6bd3c9cef9220d5020c265c3548e513f12b1a74`  
		Last Modified: Wed, 25 Dec 2024 06:26:25 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2-alpine`

```console
$ docker pull erlang@sha256:0acb632217908970082f38852dbddf5142eab55e4f447f5fb91c69984b2d4b84
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

### `erlang:26.2-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:acbd326ac9f3e1b446a455b8c67b105021bc050c71a37d2cd8b43b8fe9304d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49608095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b1deb54f95e83a62501b5f4f201fda95134befdca43a7a9f364745fd8aa8a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d341b0c0baddc4e1544584026eab3673c2cdfad56878b5c20466add57e8263`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 46.0 MB (45994096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3bd8e93393c6f761a8d6aca03d5358a98ff5555355046937a177d4c8f66867f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430d9378ce090ed94dd81031d29394763313f5274b3300b8238950bca55a5983`

```dockerfile
```

-	Layers:
	-	`sha256:e431a6dea0d5141cb3fd5392a3a8e442d47b99e0907368f6d7f4e5ecac02cb32`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 267.0 KB (267035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24ea22e3b9ab67a85b644d176ba54f27fbf9b2c0e495977096d53222e789f8`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0e5d34ae97925ff4ce9cbd515c606bc9a1294404a33fb0cad1e8965644942b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46754463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7e714d85f4b782da84d0a81fad72f97905649378bd92e27ea5d54d8443470`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f07b1899d4cf55307ea151685037b83600807cfffbc36b169318f70ce07e92`  
		Last Modified: Tue, 07 Jan 2025 06:33:14 GMT  
		Size: 43.7 MB (43663175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:07a7ef3c604c992ac72b64dfb3977a8134fdc698d2ccd2f3c11c154a895aaa8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 KB (278228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3d4f39a211e1e93ad82beb931eced300d6209a3949e4b4b5cc57e4a2a2b9bc`

```dockerfile
```

-	Layers:
	-	`sha256:91ac92dea26c7f474820e0f8966f29a7596138e25c06c05a08ba9dba22fe0b5f`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 263.1 KB (263109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b048c6b1ba3369feed0b7d89f12376d5ba88e716da2eb5a0533d5828ddbd75`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 15.1 KB (15119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f44244a69e1a64526ef5ca4b5121c71a1f5b69d8fd203e996e3f5b406cbcf69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49877058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a189383b2a51b1c058f4e46b5569b71331198db906c6b107a43134d605e8d381`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585de24540b1a08dfffc3670348e6266c82ca8cd13c82d761f3a39b750bf341`  
		Size: 45.8 MB (45790372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:2d721c52aba3a2acb8a158932d9169a6c5d164c1edc6b05277a4f703a05753b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 KB (282973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750702f24a21e5d6b32a6020c53832d6d730c43150e09d324b07ba552b912a32`

```dockerfile
```

-	Layers:
	-	`sha256:c7bfd97feed4cd9ec2e6c50450153150e3b57a38fcbb6ad70c5b3f03a35192ab`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 267.8 KB (267827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a975126bc0dff14240f2795b75b6ad60cd2972d0be11d7c57415e04bce416a0a`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 15.1 KB (15146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-alpine` - linux; 386

```console
$ docker pull erlang@sha256:9e53d0f711bd5c575af496c6c741a698185b38e40e923cdf3728dc7cd3b32d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48065746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a59f89e6e754e1de9eaab8209a72a27ec4d526ceb4f8c1e50c7ee57e50c79b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d9754cd1babeb033f2dd6a0efc8eb0315a0694ca165bb6da164526545f756`  
		Last Modified: Tue, 07 Jan 2025 03:24:02 GMT  
		Size: 44.6 MB (44602557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0443c7c8e6ebab82c769ac38dcde6adc3f032314d8b88791cccb8b9a24560a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 KB (277323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7d86f895880f5e071e29e95ab08607577fa63dee23a3c4b881ff5e41a28149`

```dockerfile
```

-	Layers:
	-	`sha256:2d0d098a6c9f8dc99c03a301564a3261886860e77a00120ef232a08eab517ebc`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 262.3 KB (262312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b351b38eae7e21841aedb67501d5dd4614d1b8696898df3b8457990b04518448`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:a62a665256713fd74be522a465d4412ed71749eb8101a716dc5ebe8747fb8d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48222892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a6d0b3369807d752c7635fdedf59148b4525da648ad92a8c29a1f16c21d0a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a439a30565a16dca74b577c9f57742d9c6587756db9315fe004e2119e444369`  
		Last Modified: Tue, 07 Jan 2025 06:32:17 GMT  
		Size: 44.7 MB (44654165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:683c1f77b47ec10aa08673137a4b3ae6f8b2c3ac63c21ac6558cb3c0afc80c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe969dcbb43b548f237f23004b7b3b1ee743b0bd364d54444f6a3d12e67ffb1d`

```dockerfile
```

-	Layers:
	-	`sha256:c291da8439cecc4dab1c52376513fc5913a9a4f434c4c82add01d5c4a8a5d3f9`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 261.2 KB (261156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378ca39982a195b28744efbeebc56e5805e0adade253a02ebd871d2280a05861`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:5eaa0d4d0cb5a870360a56354958358201ab637e51bfc6cdb55e00ff88544f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47772736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba9649446d28fd5cb2b3311c9798aeefe3ad17afbc2e149d3bc6e8fa48186e7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e6de505a368a8e02977d779b3df7c0f324eca3a30a8c4945d6ddf05ff4147e`  
		Last Modified: Tue, 07 Jan 2025 06:39:35 GMT  
		Size: 44.3 MB (44313557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3aa6c8aeb9fb9117414ef71320e0cd8fdc1df6823959ed6b8bc2b37c9c02d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378bc1a503550361fd9411ade08b8d0cf91691464f44a9e305535bfbaece6aa`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e86acc678c6e49f9e047f3bd8b19a8be0140c1c4f104a756e7b67c6ee6a4e`  
		Last Modified: Tue, 07 Jan 2025 06:39:34 GMT  
		Size: 261.1 KB (261122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8fc60132e965e5ea326b83ea51b09fc70c7152cc277b250d7fbb290a215968`  
		Last Modified: Tue, 07 Jan 2025 06:39:33 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2-slim`

```console
$ docker pull erlang@sha256:fe2d30f39895efadf3887717a4ebca7f920c6f12558bc36d3632d055b27c187b
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

### `erlang:26.2-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9245c33cf3623593220a37964c3584c1983c6b7fc4c8f641e4ede540dee4d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643a38794c5268db14965ca8983ece4591596243043393afd556e1a58075bdb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de85552e2280313a4b344aafb4679a335319b68c81732b638a326e2426cb57f`  
		Last Modified: Tue, 24 Dec 2024 22:33:59 GMT  
		Size: 70.3 MB (70334542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:90ae2ea8bd9d6814d3e3d56f68a87ad75fd66be1bec0582490f336f028723e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871532807198d0bd4f76879b83202ed1d90ae0aa11b9558b212aa44ae2b4356a`

```dockerfile
```

-	Layers:
	-	`sha256:11f891cd6215599e1f7f9f1479a947223f32d272afc4c9e38d0ea8bed5e61309`  
		Size: 3.7 MB (3709308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a212319339c9e70bb5eabb0139efd91053a192cd8a86b70009943612aac1975`  
		Last Modified: Tue, 24 Dec 2024 22:33:57 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:bf695ce614b9d5ec453e29806b897b3dc77374f52aafe5f6ccc2c53f86b19215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106461065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9572055074120b7fd0080fa1948ad670f41f305213023be2e233c3c8f0fc3b7`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f47e9b4117175e620492590bcc82a80b4d1c862a5584a33b4d0b5ec4133130`  
		Last Modified: Wed, 25 Dec 2024 01:42:45 GMT  
		Size: 60.4 MB (60436823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c48e6107d4ef1341541c516ebf17f22457d7a9f965c8e1a3a1cb200729e5fb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630bebe864091691f3be7a3257375d9c6f3f7533aec60d2e52a0d3d8b1f23703`

```dockerfile
```

-	Layers:
	-	`sha256:a6afb172e9898965b32c75b61aa036d67fe61e4d014a7b3f139e97bbf8810216`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 3.7 MB (3712808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec2d22e89f906422458f29a286d59f03852527258ffcd50511d864aad459879`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:13673e8653f4aecd2988b81cee08af61dfd30d5d8d3a9c612ff2be4573a0a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104262450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea6e4164fb4f648bd825d4e222e20af3e0dba82d1bd08e3eadf2321b16a77cb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe46a6c6ed9025746030b6d1a9556b74143a6d3538a61a268f6726ac9ab991b`  
		Size: 60.1 MB (60062483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c3fa33600e689fc6c06866384f547cb04c91dd974fa8637cbcc69a61f5fe0d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa8a5fc06ad3c862ac9d35e5ba4c9515d2ef51f4e374fa287ddb6baf11fff5`

```dockerfile
```

-	Layers:
	-	`sha256:2082cad6739f50ee480044c91987b8d45f75c47ab389352bd85144e408191778`  
		Last Modified: Wed, 25 Dec 2024 04:01:00 GMT  
		Size: 3.7 MB (3711541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64dfadecfd335cfaad4766ff9e94d8eff1d2650c02e73efd652de2552af5fc5`  
		Last Modified: Wed, 25 Dec 2024 04:00:59 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0bc4c0c3f6e54041c2f523a60255969f1c1b8f333317da816bb8ef56e8d2191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116293288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1889f1aa971ad46e616b559fd4f12002f981478965de556ea0b9c7d780c4aa78`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43bf59b125105e1cd69f2dfd8a490c1fe920e94085154bae98a41a43c678929`  
		Last Modified: Wed, 25 Dec 2024 02:05:20 GMT  
		Size: 68.0 MB (67967804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a3a14217cfb888619be48921566fc198ca0ffb0af37282b0bbab3d9ba9c7b7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b5cb8d9a17f6ae298d5652cee07f658dd771085eace08776be1e4f0c2bf43`

```dockerfile
```

-	Layers:
	-	`sha256:db11eb055d8b30d5f8bb19a65fde756ba4cbd1f15c31021ff411ff178c2e3c76`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 3.7 MB (3709569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1fb1db134619fe252dafa283e4081eb206596acd1551794add0a7a26268b0f`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 13.7 KB (13706 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; 386

```console
$ docker pull erlang@sha256:06e8f24c7f1af3ac3137f31536fc23e433f38b39d8d9c5aebc9cbdb10f788517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d426b483e1ad6d8b1546ec854340e2c483613c21fb5584b17eafa3ecc79c853`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca44d1694041f067ebf8d5b4f893979eacee074bbacec58ae6385ba43f6332c`  
		Last Modified: Tue, 24 Dec 2024 22:22:09 GMT  
		Size: 61.1 MB (61082179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9f164f8ff414fdd2d0e54cc8cc9b332ea90e1c998ea9084bb2ed2579e713c5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7effa791763f3965eaf81acb63961e9add2e3a07109fe86c3c433d946d940d50`

```dockerfile
```

-	Layers:
	-	`sha256:084984b2a63b0ecea2adf646beb29a555fc681e87b5a61ab6bba340da666051c`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 3.7 MB (3706428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4947521b614134d1999d00c5c5e0dc0bf60c59737b18da06e76d123886af972`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 13.6 KB (13570 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:42d8883ee031325e8ed750bde68436b20be8c107ef0e38a9eb3d59491809eb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109811275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c056dd6e56e4ef9e175e601f9c675964a1779aa5821b5f9ebe0925ed05cba91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc59f63202059cc1a98ba153f0b85086eb0bbdd85327f45bb99993b46795184`  
		Size: 61.0 MB (61039631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ed37a1736689bcf22ad1be7086a06e42870628b3981d08fb5b27150bf2abe797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cff71a74434232533d6a351f5b93d4be4b238053a6d1b7cac0e7220f5096654`

```dockerfile
```

-	Layers:
	-	`sha256:4be412e380e31e62de3dbce65645202669143e4a2f02a2fbea0b16ccbe35e25a`  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:fc6b9c285f3898a9968bf0a4680fa260d980781edba45f51c706acdddc7b92ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114484982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c07556602085c72109fc9bce13bf6556cc33aa9356f5016eec743416e5b8b6`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e71a0911f3797a4433566eb71eabaf282361f449e22480cd6c6b8daa78f436`  
		Last Modified: Wed, 25 Dec 2024 13:12:38 GMT  
		Size: 62.2 MB (62156907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bef084a7d2e34a035901876099c659e0cbe4c0c760878c21742c3c6db361239b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524bb828d0ebb1551f4e17d70fd3dd7d2e3cfd2a0930e9fe867df1cb604ad70a`

```dockerfile
```

-	Layers:
	-	`sha256:ed2de4f4544af54cf9f556282a8e230c9a98c1017451b72218a33783fa702c30`  
		Last Modified: Wed, 25 Dec 2024 13:12:36 GMT  
		Size: 3.7 MB (3713648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600402e96cbb348c729321b196ba62609b54c0c6624ae559782cc39f43aac543`  
		Last Modified: Wed, 25 Dec 2024 13:12:35 GMT  
		Size: 13.6 KB (13646 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2-slim` - linux; s390x

```console
$ docker pull erlang@sha256:6d85ea70b290d20f080ac0e9555c9c0e5ff4e2fef603e30f97c75a1b9908d142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108015920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dd6a756f010ab58d19c5dd260cfba99216ec0ef90b74add84a25c56b86940`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916390e7fbffcb8b07a7fb2db15e99e02a4f0877ead918a47deaa75a606cd480`  
		Last Modified: Wed, 25 Dec 2024 00:35:19 GMT  
		Size: 60.9 MB (60866295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:73c6ea98cd52f898b9a8f2f5fb71f6fdff1acba7b103bbe84420b4edee8e3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8988e684b1ac36b391d6c10c027443e1ae5d29337c8eeb09c894856c3d77674`

```dockerfile
```

-	Layers:
	-	`sha256:a9eca79291e0f84f11c09b98550c0333af5c6410fd961091e702265c4faa5cb0`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 3.7 MB (3709028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc5b7bff5da1ea719300b49d7f0400bc865cbd984847b627d0a2ebf53d9a695`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2.5`

```console
$ docker pull erlang@sha256:ed1400b304a7a39666662880fb58fc820e9d8ac5eec78035f28253992be34e02
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

### `erlang:26.2.5` - linux; amd64

```console
$ docker pull erlang@sha256:33ca4296eab483162c77a10945408a739061c85371b60a9fb237e50862583708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601308199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7305659e92e12718e2961d55df9945e473548fbf2bbbe1ec58af57e9e40045`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 07 Jan 2025 19:42:38 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 07 Jan 2025 19:42:44 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad3923e92788e6116cbfb84ad3949b53f2330fb4dec5b140cfab39fb3fba9b`  
		Last Modified: Wed, 25 Dec 2024 01:29:03 GMT  
		Size: 252.2 MB (252234737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b903ded9cf0dd702b5a6cc9241a1d344eb18ecd6baf9ef48f87b58b72f69d77d`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 194.9 KB (194929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b3b612600174adb0899c01390407558e0c6ea66219a3100234bdabc46dd10c`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 818.4 KB (818375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:cae7c61ab3d7c7b365a02d0426a5556ec6c3df2e8b47d626939e70b4e020fd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22706526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f15a9b6702508541307f8f285d8c2b2a4b1282a057767abb81c620345aad2f`

```dockerfile
```

-	Layers:
	-	`sha256:ee441009cd3bc7d653da62433cd793dd51150a40da4309a41bf0f595292235f6`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 22.7 MB (22687509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded2b234ced333eb44be4ab4edcf13132c5b01f61c255267ece859ab2c658e02`  
		Last Modified: Wed, 25 Dec 2024 01:29:00 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; arm variant v5

```console
$ docker pull erlang@sha256:c47834683cbbcfdf596945051b721336be52b1b59c7b9d89de9ac4d113dfe428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542841883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b491cb8906936009fd157098cf5eb3bda6b351620555bb91fd860bea7d8de`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397934db677d27dbd0599257dd9cdb7e2f5bfbf61a63d5277b1a3d26a7f782b`  
		Last Modified: Wed, 25 Dec 2024 07:28:33 GMT  
		Size: 226.7 MB (226665910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c355ca1c15debc541949c0e60995c3899a8592fca95983362a3a4b799b0c937`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 194.9 KB (194939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b515f7e1b5c411acde26c3f3f3f161f48c92675b9918bc05b5fa76f04e899`  
		Last Modified: Wed, 25 Dec 2024 07:28:28 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:272ad89706868ea3e65f450f599a6e2f5ba77d21dd13189927d82a155b826c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22505226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892b566b47b78ccc1d467a5b7d71d4752bf70b5ec410fddc705f4b5753803859`

```dockerfile
```

-	Layers:
	-	`sha256:87e9fe6ade2272821576431a83c201cde540e66cc549df92aaf9263e632ce686`  
		Size: 22.5 MB (22486107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b0dbfc907673a6ac6f1297ca91b98b159140c533641761cd5c6009baeee6da`  
		Last Modified: Wed, 25 Dec 2024 07:28:27 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4ba19d4389158a182cead4428e588c89e0271a30461700c2a4bcad20f27baaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.6 MB (525562351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d10c0cf8e4888cc99ec2b33978eea3b5ed4e1cc5bc9c6aa3f2d909b1ec310aa`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec35f0d61fac60686d2f30712acd1f65eec4d41cc39402c7407d01ab5fd04099`  
		Last Modified: Wed, 25 Dec 2024 17:02:32 GMT  
		Size: 223.7 MB (223699867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970195692be1a940628eb663f41abd075864249c58061e92ebab300d495d95a`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 194.9 KB (194906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069bd4d28ffc02686245f547fb011cff88b8d82475ca57689418da8f173773e7`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:96d50334ecbd114504211ed8a8fc57296f16d619d39f0e9d6e79b6db412f2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22522121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f616e211f20e7dfb8f057e913a4a4672a9f112b71ef8b7b5773d9138870d9e`

```dockerfile
```

-	Layers:
	-	`sha256:b894a3dde3fde1aec88da8037d5c7396c23946a420d9ed012e0b33e9a50f0079`  
		Last Modified: Wed, 25 Dec 2024 17:02:26 GMT  
		Size: 22.5 MB (22503002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab97c806731a12fc65da8ce845d5fbb7d1271c23ebe7c52570cdb845d25c03f`  
		Last Modified: Wed, 25 Dec 2024 17:02:25 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:76741f5c728364bdf8ff16ce53a360bf22a03ee7a2741aaced2db55adb65adf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (585043434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc4412e312b030446298fe9138b6ccca03f511209ba0337631ffe3328165362`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c411cf62d39b47b837d578985ab77a50ea1fbc284551a3aa0409e87def9a0`  
		Last Modified: Wed, 25 Dec 2024 12:37:31 GMT  
		Size: 245.3 MB (245265034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4c8864c5581119b788071f338dc1fa6f107ea62d0d97be278c837130748382`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 194.9 KB (194920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c051967da3e5ee21a867e30ce74ff1890c9c929b8e6fd7c7d73333286388bc39`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:1c5b9decdb56e7fdddd6e761ed66200e0cf1b3dee5522ccb536e7ca8b2267954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22746701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbfe22cabf66cff2b83991eb77a89ed643e07e9a3ba56c37842859b42867207`

```dockerfile
```

-	Layers:
	-	`sha256:1348c030aeb3b0dd387cfc108ba90397cef260c6068dcfb1435619cb46d151bf`  
		Last Modified: Wed, 25 Dec 2024 12:37:26 GMT  
		Size: 22.7 MB (22727550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d1c840487e4f8db87c26b35eb175320fc95dabfaf43c7cf69bab06e61a9205`  
		Last Modified: Wed, 25 Dec 2024 12:37:25 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; 386

```console
$ docker pull erlang@sha256:0964d5a81ea1063c46298287ccc7de183f79a2197da131ab6847f926930ae9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33627c476a6d607a84581983de47a18edf72323019bd51f5dde0c83d9528087`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b325808dbceff48bd87caaf06d755e8f301da86a23bc920d9396b55662b024`  
		Last Modified: Wed, 25 Dec 2024 01:27:48 GMT  
		Size: 246.3 MB (246253926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d8ab98e13a799ba5d3bbfd84b010ff4dad686ae35556d847a447e4491a5c6d`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 194.9 KB (194921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a52f9a18f1146348cbeca5a78be065e77e59b72c78187e0ed7046e7689aeb`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:1f77cf80ba750c94bdeaa23c1b5e7146d3c23b29202abc24c6db08da5ce13505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22674672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4aa12d1991687d7f3d10a1d7d17e1661a397c181f9ad1dd6faf8492452a460`

```dockerfile
```

-	Layers:
	-	`sha256:7a21e628b24dd19dd64e73ffd96c59bb18fb288b16259ebd784b1936fcbfd9e8`  
		Last Modified: Wed, 25 Dec 2024 01:27:43 GMT  
		Size: 22.7 MB (22655691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136fea54ca6c6618eec5f838bf6a55aff1190c3772bfb55deba22cbaad28af5a`  
		Size: 19.0 KB (18981 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; mips64le

```console
$ docker pull erlang@sha256:30d8bb1e49a074a98daa66c77616287e0b3de6ee565ee1ef1efdaedb94df7bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.4 MB (554444139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eecd64bd1d17034d277c88f069adda59d52f2d425e8abed5a8606e0780765f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63286a1209cbdc1c275298e13fe1bfa10fc51dc83765b2a824950a61db918afb`  
		Last Modified: Thu, 26 Dec 2024 03:14:36 GMT  
		Size: 228.0 MB (228041570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae72d3525553c4072dc4a6b07be77372518c2bff0c7a0d535277097ec1dc3ec`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 194.9 KB (194892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305300a46c2c64336de750c215a25e2ab4f9de3ffb5e5b42ee49dd845cc6966a`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:21128996e4ae5dd249f65a6af7650d4caf3706f875bf18c626eb5a3ea721bd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876c203b625cdeab57609f863669bafaf9c28fc44cc409c1c736f7a4f27041fb`

```dockerfile
```

-	Layers:
	-	`sha256:7578e0b4d2da83dd0317773b14a6e3cf95c9c7c77a208a941912a309c2023cc4`  
		Last Modified: Thu, 26 Dec 2024 03:14:16 GMT  
		Size: 18.9 KB (18874 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; ppc64le

```console
$ docker pull erlang@sha256:4c6b08585085ec88fd5ff20953955acf4837fd5165fea62953fd8ace04bad766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612528323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7a4a4960a634590af6bdd1f65c8b5875b69ec50584eed36320c09d448765e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dacb78300d7562438fc131ed143b37a7156329b71fc87772da342b057b2354`  
		Size: 249.5 MB (249511846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa91d252a553e2e8069a864c5a15a7aa2dc07b8eaf6244b59e56a1ed76b99b8`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 194.9 KB (194933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60821f5123497b0fc0640668c2145edc82b3cdcc6291f87eed71b0361e29e52c`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 818.4 KB (818379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:bd55cea6c2c36042c767eb03ebedd91f432b241c3e6891aa949807ebe6a41aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6fde1edd923b038d52a0c47a914824c43deafa2c2e7989d367192f7560cf7`

```dockerfile
```

-	Layers:
	-	`sha256:f73b1bddfbfd286c2f9c1cfe87d20d0ece8861963c1c6c6897a2510b0506caf5`  
		Last Modified: Wed, 25 Dec 2024 15:27:57 GMT  
		Size: 22.6 MB (22643187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6425215072f4c3fb74b25559d521cd4d4c519ef51b9117d882ff67c5ae23a60`  
		Last Modified: Wed, 25 Dec 2024 15:27:56 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5` - linux; s390x

```console
$ docker pull erlang@sha256:1963feaa7dc9f7566e7229c600c1d02811d9847395e48a7638b7ff08d23dda63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.5 MB (553490119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5531bdf3f7d4b0b776d811f6db1a62285a219cb993a4475311bc7342098dccc`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f854986e8bdacb00c948da96265abf8d73da298a0e4ebf175ebbd706a79956a`  
		Last Modified: Wed, 25 Dec 2024 06:26:29 GMT  
		Size: 234.7 MB (234663730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de8334711e0ec36026e31eef49190cf99f12ed4105b8d4a50c4029ab129229`  
		Size: 194.9 KB (194917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a2262a940334fcbcc90186c8d3d12e776dbb46f9672846593ca0b2bafeb09`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 818.4 KB (818378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5` - unknown; unknown

```console
$ docker pull erlang@sha256:c6dd99957dbf5e083fc9f19e02889c02b01238950f5bce0722545db84ffda77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22480239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27195c5019fcfbe8ecfbacd35977f37b80a27155ebd9ee95ffc3e9a1d0d7db77`

```dockerfile
```

-	Layers:
	-	`sha256:f1d75a566130ef9b0bb741c8d068649c30bb310fd50f9e2ed987f9d22e5918d0`  
		Last Modified: Wed, 25 Dec 2024 06:26:26 GMT  
		Size: 22.5 MB (22461222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a38ee67ca2ddbff733d6a6a6bd3c9cef9220d5020c265c3548e513f12b1a74`  
		Last Modified: Wed, 25 Dec 2024 06:26:25 GMT  
		Size: 19.0 KB (19017 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2.5-alpine`

```console
$ docker pull erlang@sha256:0acb632217908970082f38852dbddf5142eab55e4f447f5fb91c69984b2d4b84
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

### `erlang:26.2.5-alpine` - linux; amd64

```console
$ docker pull erlang@sha256:acbd326ac9f3e1b446a455b8c67b105021bc050c71a37d2cd8b43b8fe9304d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49608095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b1deb54f95e83a62501b5f4f201fda95134befdca43a7a9f364745fd8aa8a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d341b0c0baddc4e1544584026eab3673c2cdfad56878b5c20466add57e8263`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 46.0 MB (45994096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3bd8e93393c6f761a8d6aca03d5358a98ff5555355046937a177d4c8f66867f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430d9378ce090ed94dd81031d29394763313f5274b3300b8238950bca55a5983`

```dockerfile
```

-	Layers:
	-	`sha256:e431a6dea0d5141cb3fd5392a3a8e442d47b99e0907368f6d7f4e5ecac02cb32`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 267.0 KB (267035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24ea22e3b9ab67a85b644d176ba54f27fbf9b2c0e495977096d53222e789f8`  
		Last Modified: Tue, 07 Jan 2025 03:39:18 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0e5d34ae97925ff4ce9cbd515c606bc9a1294404a33fb0cad1e8965644942b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46754463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7e714d85f4b782da84d0a81fad72f97905649378bd92e27ea5d54d8443470`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f07b1899d4cf55307ea151685037b83600807cfffbc36b169318f70ce07e92`  
		Last Modified: Tue, 07 Jan 2025 06:33:14 GMT  
		Size: 43.7 MB (43663175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:07a7ef3c604c992ac72b64dfb3977a8134fdc698d2ccd2f3c11c154a895aaa8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 KB (278228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3d4f39a211e1e93ad82beb931eced300d6209a3949e4b4b5cc57e4a2a2b9bc`

```dockerfile
```

-	Layers:
	-	`sha256:91ac92dea26c7f474820e0f8966f29a7596138e25c06c05a08ba9dba22fe0b5f`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 263.1 KB (263109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b048c6b1ba3369feed0b7d89f12376d5ba88e716da2eb5a0533d5828ddbd75`  
		Last Modified: Tue, 07 Jan 2025 06:33:12 GMT  
		Size: 15.1 KB (15119 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f44244a69e1a64526ef5ca4b5121c71a1f5b69d8fd203e996e3f5b406cbcf69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49877058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a189383b2a51b1c058f4e46b5569b71331198db906c6b107a43134d605e8d381`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585de24540b1a08dfffc3670348e6266c82ca8cd13c82d761f3a39b750bf341`  
		Size: 45.8 MB (45790372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:2d721c52aba3a2acb8a158932d9169a6c5d164c1edc6b05277a4f703a05753b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 KB (282973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750702f24a21e5d6b32a6020c53832d6d730c43150e09d324b07ba552b912a32`

```dockerfile
```

-	Layers:
	-	`sha256:c7bfd97feed4cd9ec2e6c50450153150e3b57a38fcbb6ad70c5b3f03a35192ab`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 267.8 KB (267827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a975126bc0dff14240f2795b75b6ad60cd2972d0be11d7c57415e04bce416a0a`  
		Last Modified: Tue, 07 Jan 2025 07:37:14 GMT  
		Size: 15.1 KB (15146 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-alpine` - linux; 386

```console
$ docker pull erlang@sha256:9e53d0f711bd5c575af496c6c741a698185b38e40e923cdf3728dc7cd3b32d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48065746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a59f89e6e754e1de9eaab8209a72a27ec4d526ceb4f8c1e50c7ee57e50c79b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d9754cd1babeb033f2dd6a0efc8eb0315a0694ca165bb6da164526545f756`  
		Last Modified: Tue, 07 Jan 2025 03:24:02 GMT  
		Size: 44.6 MB (44602557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:0443c7c8e6ebab82c769ac38dcde6adc3f032314d8b88791cccb8b9a24560a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 KB (277323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7d86f895880f5e071e29e95ab08607577fa63dee23a3c4b881ff5e41a28149`

```dockerfile
```

-	Layers:
	-	`sha256:2d0d098a6c9f8dc99c03a301564a3261886860e77a00120ef232a08eab517ebc`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 262.3 KB (262312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b351b38eae7e21841aedb67501d5dd4614d1b8696898df3b8457990b04518448`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:a62a665256713fd74be522a465d4412ed71749eb8101a716dc5ebe8747fb8d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48222892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a6d0b3369807d752c7635fdedf59148b4525da648ad92a8c29a1f16c21d0a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a439a30565a16dca74b577c9f57742d9c6587756db9315fe004e2119e444369`  
		Last Modified: Tue, 07 Jan 2025 06:32:17 GMT  
		Size: 44.7 MB (44654165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:683c1f77b47ec10aa08673137a4b3ae6f8b2c3ac63c21ac6558cb3c0afc80c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe969dcbb43b548f237f23004b7b3b1ee743b0bd364d54444f6a3d12e67ffb1d`

```dockerfile
```

-	Layers:
	-	`sha256:c291da8439cecc4dab1c52376513fc5913a9a4f434c4c82add01d5c4a8a5d3f9`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 261.2 KB (261156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378ca39982a195b28744efbeebc56e5805e0adade253a02ebd871d2280a05861`  
		Last Modified: Tue, 07 Jan 2025 06:32:15 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:5eaa0d4d0cb5a870360a56354958358201ab637e51bfc6cdb55e00ff88544f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47772736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba9649446d28fd5cb2b3311c9798aeefe3ad17afbc2e149d3bc6e8fa48186e7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e6de505a368a8e02977d779b3df7c0f324eca3a30a8c4945d6ddf05ff4147e`  
		Last Modified: Tue, 07 Jan 2025 06:39:35 GMT  
		Size: 44.3 MB (44313557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:3aa6c8aeb9fb9117414ef71320e0cd8fdc1df6823959ed6b8bc2b37c9c02d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 KB (276165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378bc1a503550361fd9411ade08b8d0cf91691464f44a9e305535bfbaece6aa`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e86acc678c6e49f9e047f3bd8b19a8be0140c1c4f104a756e7b67c6ee6a4e`  
		Last Modified: Tue, 07 Jan 2025 06:39:34 GMT  
		Size: 261.1 KB (261122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8fc60132e965e5ea326b83ea51b09fc70c7152cc277b250d7fbb290a215968`  
		Last Modified: Tue, 07 Jan 2025 06:39:33 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2.5-slim`

```console
$ docker pull erlang@sha256:fe2d30f39895efadf3887717a4ebca7f920c6f12558bc36d3632d055b27c187b
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

### `erlang:26.2.5-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9245c33cf3623593220a37964c3584c1983c6b7fc4c8f641e4ede540dee4d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643a38794c5268db14965ca8983ece4591596243043393afd556e1a58075bdb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de85552e2280313a4b344aafb4679a335319b68c81732b638a326e2426cb57f`  
		Last Modified: Tue, 24 Dec 2024 22:33:59 GMT  
		Size: 70.3 MB (70334542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:90ae2ea8bd9d6814d3e3d56f68a87ad75fd66be1bec0582490f336f028723e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871532807198d0bd4f76879b83202ed1d90ae0aa11b9558b212aa44ae2b4356a`

```dockerfile
```

-	Layers:
	-	`sha256:11f891cd6215599e1f7f9f1479a947223f32d272afc4c9e38d0ea8bed5e61309`  
		Size: 3.7 MB (3709308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a212319339c9e70bb5eabb0139efd91053a192cd8a86b70009943612aac1975`  
		Last Modified: Tue, 24 Dec 2024 22:33:57 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:bf695ce614b9d5ec453e29806b897b3dc77374f52aafe5f6ccc2c53f86b19215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106461065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9572055074120b7fd0080fa1948ad670f41f305213023be2e233c3c8f0fc3b7`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f47e9b4117175e620492590bcc82a80b4d1c862a5584a33b4d0b5ec4133130`  
		Last Modified: Wed, 25 Dec 2024 01:42:45 GMT  
		Size: 60.4 MB (60436823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c48e6107d4ef1341541c516ebf17f22457d7a9f965c8e1a3a1cb200729e5fb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630bebe864091691f3be7a3257375d9c6f3f7533aec60d2e52a0d3d8b1f23703`

```dockerfile
```

-	Layers:
	-	`sha256:a6afb172e9898965b32c75b61aa036d67fe61e4d014a7b3f139e97bbf8810216`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 3.7 MB (3712808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec2d22e89f906422458f29a286d59f03852527258ffcd50511d864aad459879`  
		Last Modified: Wed, 25 Dec 2024 01:42:43 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:13673e8653f4aecd2988b81cee08af61dfd30d5d8d3a9c612ff2be4573a0a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104262450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea6e4164fb4f648bd825d4e222e20af3e0dba82d1bd08e3eadf2321b16a77cb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe46a6c6ed9025746030b6d1a9556b74143a6d3538a61a268f6726ac9ab991b`  
		Size: 60.1 MB (60062483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c3fa33600e689fc6c06866384f547cb04c91dd974fa8637cbcc69a61f5fe0d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa8a5fc06ad3c862ac9d35e5ba4c9515d2ef51f4e374fa287ddb6baf11fff5`

```dockerfile
```

-	Layers:
	-	`sha256:2082cad6739f50ee480044c91987b8d45f75c47ab389352bd85144e408191778`  
		Last Modified: Wed, 25 Dec 2024 04:01:00 GMT  
		Size: 3.7 MB (3711541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64dfadecfd335cfaad4766ff9e94d8eff1d2650c02e73efd652de2552af5fc5`  
		Last Modified: Wed, 25 Dec 2024 04:00:59 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0bc4c0c3f6e54041c2f523a60255969f1c1b8f333317da816bb8ef56e8d2191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116293288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1889f1aa971ad46e616b559fd4f12002f981478965de556ea0b9c7d780c4aa78`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43bf59b125105e1cd69f2dfd8a490c1fe920e94085154bae98a41a43c678929`  
		Last Modified: Wed, 25 Dec 2024 02:05:20 GMT  
		Size: 68.0 MB (67967804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a3a14217cfb888619be48921566fc198ca0ffb0af37282b0bbab3d9ba9c7b7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b5cb8d9a17f6ae298d5652cee07f658dd771085eace08776be1e4f0c2bf43`

```dockerfile
```

-	Layers:
	-	`sha256:db11eb055d8b30d5f8bb19a65fde756ba4cbd1f15c31021ff411ff178c2e3c76`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 3.7 MB (3709569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1fb1db134619fe252dafa283e4081eb206596acd1551794add0a7a26268b0f`  
		Last Modified: Wed, 25 Dec 2024 02:05:18 GMT  
		Size: 13.7 KB (13706 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; 386

```console
$ docker pull erlang@sha256:06e8f24c7f1af3ac3137f31536fc23e433f38b39d8d9c5aebc9cbdb10f788517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d426b483e1ad6d8b1546ec854340e2c483613c21fb5584b17eafa3ecc79c853`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca44d1694041f067ebf8d5b4f893979eacee074bbacec58ae6385ba43f6332c`  
		Last Modified: Tue, 24 Dec 2024 22:22:09 GMT  
		Size: 61.1 MB (61082179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9f164f8ff414fdd2d0e54cc8cc9b332ea90e1c998ea9084bb2ed2579e713c5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7effa791763f3965eaf81acb63961e9add2e3a07109fe86c3c433d946d940d50`

```dockerfile
```

-	Layers:
	-	`sha256:084984b2a63b0ecea2adf646beb29a555fc681e87b5a61ab6bba340da666051c`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 3.7 MB (3706428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4947521b614134d1999d00c5c5e0dc0bf60c59737b18da06e76d123886af972`  
		Last Modified: Tue, 24 Dec 2024 22:22:07 GMT  
		Size: 13.6 KB (13570 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:42d8883ee031325e8ed750bde68436b20be8c107ef0e38a9eb3d59491809eb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109811275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c056dd6e56e4ef9e175e601f9c675964a1779aa5821b5f9ebe0925ed05cba91`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc59f63202059cc1a98ba153f0b85086eb0bbdd85327f45bb99993b46795184`  
		Size: 61.0 MB (61039631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ed37a1736689bcf22ad1be7086a06e42870628b3981d08fb5b27150bf2abe797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cff71a74434232533d6a351f5b93d4be4b238053a6d1b7cac0e7220f5096654`

```dockerfile
```

-	Layers:
	-	`sha256:4be412e380e31e62de3dbce65645202669143e4a2f02a2fbea0b16ccbe35e25a`  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:fc6b9c285f3898a9968bf0a4680fa260d980781edba45f51c706acdddc7b92ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114484982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c07556602085c72109fc9bce13bf6556cc33aa9356f5016eec743416e5b8b6`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e71a0911f3797a4433566eb71eabaf282361f449e22480cd6c6b8daa78f436`  
		Last Modified: Wed, 25 Dec 2024 13:12:38 GMT  
		Size: 62.2 MB (62156907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bef084a7d2e34a035901876099c659e0cbe4c0c760878c21742c3c6db361239b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524bb828d0ebb1551f4e17d70fd3dd7d2e3cfd2a0930e9fe867df1cb604ad70a`

```dockerfile
```

-	Layers:
	-	`sha256:ed2de4f4544af54cf9f556282a8e230c9a98c1017451b72218a33783fa702c30`  
		Last Modified: Wed, 25 Dec 2024 13:12:36 GMT  
		Size: 3.7 MB (3713648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600402e96cbb348c729321b196ba62609b54c0c6624ae559782cc39f43aac543`  
		Last Modified: Wed, 25 Dec 2024 13:12:35 GMT  
		Size: 13.6 KB (13646 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26.2.5-slim` - linux; s390x

```console
$ docker pull erlang@sha256:6d85ea70b290d20f080ac0e9555c9c0e5ff4e2fef603e30f97c75a1b9908d142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108015920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dd6a756f010ab58d19c5dd260cfba99216ec0ef90b74add84a25c56b86940`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916390e7fbffcb8b07a7fb2db15e99e02a4f0877ead918a47deaa75a606cd480`  
		Last Modified: Wed, 25 Dec 2024 00:35:19 GMT  
		Size: 60.9 MB (60866295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26.2.5-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:73c6ea98cd52f898b9a8f2f5fb71f6fdff1acba7b103bbe84420b4edee8e3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8988e684b1ac36b391d6c10c027443e1ae5d29337c8eeb09c894856c3d77674`

```dockerfile
```

-	Layers:
	-	`sha256:a9eca79291e0f84f11c09b98550c0333af5c6410fd961091e702265c4faa5cb0`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 3.7 MB (3709028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc5b7bff5da1ea719300b49d7f0400bc865cbd984847b627d0a2ebf53d9a695`  
		Last Modified: Wed, 25 Dec 2024 00:35:17 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:26.2.5.6`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:26.2.5.6-alpine`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:26.2.5.6-slim`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27`

```console
$ docker pull erlang@sha256:30c18a712d6585cc50442c32d4b2604a96fdd5cb7000b342a31a9d1f1d479876
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

### `erlang:27` - linux; amd64

```console
$ docker pull erlang@sha256:99fabb58c8add16e134bfa43b7874e0468e111eb30e41683e34e005df6e756c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605221293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4e617a8dd5747e8aa23edcaea29c2384ca24d06859325688251b7f90aba828`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 07 Jan 2025 19:42:38 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 07 Jan 2025 19:42:44 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1fa9d56affb1708880f4b6ab4d9e6b91ba98414f99e9bca2e3a58e8646f2af`  
		Last Modified: Wed, 25 Dec 2024 01:24:13 GMT  
		Size: 256.1 MB (256144262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1270907cb1565acfcc904362d76a5ca99e617db91a14425a934a3f16c66ef`  
		Last Modified: Wed, 25 Dec 2024 01:24:09 GMT  
		Size: 195.5 KB (195541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa46f6a9bbce8d3c68f7061655cd3fd184429aa2a44c95cd452444976b7ca2`  
		Last Modified: Wed, 25 Dec 2024 01:24:10 GMT  
		Size: 821.3 KB (821332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:39f22180b15d840768f3642631a34da0d67b26fdd63737a52c9a82f68fbeaf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23363890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4429102bf23cd4507142400a334315874c4d6af43d5c3e052f2c2f54ef2787b6`

```dockerfile
```

-	Layers:
	-	`sha256:ea8a3e340c338a89aee29d25fbca5e6b31c81c184f84c9077491f39ae76bf094`  
		Last Modified: Wed, 25 Dec 2024 01:24:10 GMT  
		Size: 23.3 MB (23344688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecfb4c011f6c3d2220769b9d44e881c579da98afcd09bd3135bd01199666e9b3`  
		Last Modified: Wed, 25 Dec 2024 01:24:09 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5183973f667f6d1120a9cf2ce3e8dc78df15004654f6e23a7fa039f9100ef19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.1 MB (546129180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15648fa772ced49662325d600df624cc56e622fc533be85d7488f081573481`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ea73065182aff84baae30fc5bf818aa4a65c4f812a250b75387f9473ee9dbe`  
		Last Modified: Wed, 25 Dec 2024 07:18:08 GMT  
		Size: 229.9 MB (229949555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9093f57181462e4beaba6ed1a675c3357a01e9894da94519650129c4591ae0d`  
		Last Modified: Wed, 25 Dec 2024 07:18:01 GMT  
		Size: 195.6 KB (195631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fa45fed5692cf06d60993c47e9ab183d304c655eda2785025e6b98b5495aa`  
		Last Modified: Wed, 25 Dec 2024 07:18:01 GMT  
		Size: 821.3 KB (821338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:939bd9180cde1602559da196a15afd4a63fd88c154069c05b92f4d71634a0a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23162616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2389830af8e421e505174b392a79f881bf52c8b08ab11ce0fd9503c4fa4ffb`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc6a584843e1b3a9322c2e9152999a606df65cd80d39b35387d7056b3d4d92`  
		Last Modified: Wed, 25 Dec 2024 07:18:02 GMT  
		Size: 23.1 MB (23143304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfc224d92619411b68de17e76585e8143daaa2ea7a40a3b7a9a0767fa6c1523`  
		Size: 19.3 KB (19312 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; arm variant v7

```console
$ docker pull erlang@sha256:03b3dcaebfc835b62dde5123e431be56ae07d7699eed98c7a43c7c7c392381a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379cae6b29d5176fa14f7c711ac7499194ca5f373fcbc7c58c1eb172edabee85`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608a6e836c054e460dafcb58b25ae0baf73ca4eccb3619b34bb852e2c7cff815`  
		Size: 226.9 MB (226885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb971de189c803b0fb04e427e6b7b5d5bc32024867217fe1b2ff562406ccc89`  
		Last Modified: Wed, 25 Dec 2024 16:53:53 GMT  
		Size: 195.6 KB (195642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799649653d972a5db0d9258b5824864c11a773927516774d7c394f1aceada23a`  
		Last Modified: Wed, 25 Dec 2024 16:53:53 GMT  
		Size: 821.3 KB (821302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:e74f54d5b78b06ea7553a04987be90c0421e36efdc766ec928018ac0f533eef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23179531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2188b6842715e6e12a61da94a877db437bb5189cdfe5efe2015b63a55255330`

```dockerfile
```

-	Layers:
	-	`sha256:7bbc6b6b9a82a2881bbd11b24aec6f6b7c4d5c659d88a78a2bb8a5bc69329300`  
		Size: 23.2 MB (23160219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05398deec71d32480663454194af67ef578c84a0a599ec3f6f74a23dfafa3455`  
		Last Modified: Wed, 25 Dec 2024 16:53:52 GMT  
		Size: 19.3 KB (19312 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:5f6811bbc0f356334731ff174b7f013f492cdbb6ddfec4fba901950630b1aa45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589036181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64784a4b1244d9ad24c5b318b44544500bc20bef1dc6d69a0dbbfd0d51e2b60b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed0d2a2ae42a69f4e657b8164d5cf04eaa475cc4d5dc5dfed3b28b7dbd423a1`  
		Last Modified: Wed, 25 Dec 2024 12:30:06 GMT  
		Size: 249.3 MB (249254232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f8f93d2b1ed5f5cc02d8ca2bc073465324f5f9ef06b16254c27c65e7e2a49`  
		Size: 195.6 KB (195569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b806ce1db1d4f580c3392845480225d89e57d604fb887f0f47edccfc126e5b80`  
		Size: 821.3 KB (821278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:67c6056b29f8bd7998c03981658114d018ae619eabda4c85af90da4897d8bad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39df355ebaf6df09d32a06dce361dd68b104a4f1e20cc7628e9fab29a56fc7f2`

```dockerfile
```

-	Layers:
	-	`sha256:328269cb5e77fa3bb690f8b0365251ed6f36f23321f5deb7f5ed15f5040dfe26`  
		Last Modified: Wed, 25 Dec 2024 12:30:01 GMT  
		Size: 23.4 MB (23384751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991242e456df84220189bc7db2b8e31b0c0727a1094b042b3873517211340976`  
		Last Modified: Wed, 25 Dec 2024 12:30:00 GMT  
		Size: 19.3 KB (19348 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; 386

```console
$ docker pull erlang@sha256:227add7c2321a1f4b6a1b04f0a177f7a1deea8708d0f326c5cb9bed2db390b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601278684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af7d8f27cd74040bc6be35edc698f665c4a15a6eefc9f8926fe4a0557c7abb8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414055dc2d9dec686a13c75d418be0d93a97bbad9c4e7f00846954d342df493`  
		Last Modified: Wed, 25 Dec 2024 01:25:00 GMT  
		Size: 249.6 MB (249644211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11fa62a5970bdf7d0a1fd0e9e0b9419855c43f55ad8ca08d886e1ce40806954`  
		Size: 195.6 KB (195636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dcec6387d29c04ccbc18857d73690830401fe7181e04e40547e1af09ee8197`  
		Last Modified: Wed, 25 Dec 2024 01:24:55 GMT  
		Size: 821.4 KB (821435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:785d2b69f6ceafae0bb4828fc14ee3f48eebc4ae9b86ea93e47b8782671c47e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23331997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d1036ee2b0e41bf48b16406ebd81800b51a67788ee40685df7b92a82e6b85`

```dockerfile
```

-	Layers:
	-	`sha256:6726c6e7b23cb258853e83bf8bc844d0f31b2f946c268c8872d793baa73ba85b`  
		Last Modified: Wed, 25 Dec 2024 01:24:55 GMT  
		Size: 23.3 MB (23312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638316d475cb74b2622a0ededd1ae4825ade6500965453db1678b54255921f30`  
		Last Modified: Wed, 25 Dec 2024 01:24:54 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; mips64le

```console
$ docker pull erlang@sha256:b98dc4f484a308f9f4a4258233b0e0da4219fdc0c34eac6f3a12478e44271f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557826987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b611bf0f0ce629552dc84765d74b9ce8114b7d9ba20a89c88e6339cddaf7c81e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d59611bc70f4b1369b7db96419bebc75eabdd8aab62992c0b6957531b936a9`  
		Last Modified: Thu, 26 Dec 2024 02:31:18 GMT  
		Size: 231.4 MB (231420494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67bb1cd31bcdae914ac4e88288fc650e8876f7202c6f6e561b3373ed3689049`  
		Last Modified: Thu, 26 Dec 2024 02:30:57 GMT  
		Size: 195.6 KB (195624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14e4a162bc78e060d78f4efe12b2733e57267e29dac42b9ddee204aa85ec2f3`  
		Last Modified: Thu, 26 Dec 2024 02:30:58 GMT  
		Size: 821.6 KB (821571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:c7df58fbac00a7135f73b06f6812bef0a6582aedb90b2ff3e8a039b6c9cc2498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951e8e3ed6f60f834c81c384f5d7e206362f8a3e404fea58eb77ca3eb82a6303`

```dockerfile
```

-	Layers:
	-	`sha256:608100a4191d5db95ad0e6e655c39b7c32ec8866e82682416abe3344a4d8a0ae`  
		Last Modified: Thu, 26 Dec 2024 02:30:57 GMT  
		Size: 19.1 KB (19068 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; ppc64le

```console
$ docker pull erlang@sha256:cf79aa893784143632f62693b32f5cf875e7dbdc97636b174d892f2c006fa933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (616000684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f6ca837a3038110742307da61a811d0733e9a5594a9ead883adc177e8cf5e3`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564e9522ca734303d4ec01d6ea5f5ced0d604d04738fa1a581dc039d215aad1b`  
		Last Modified: Wed, 25 Dec 2024 15:17:23 GMT  
		Size: 253.0 MB (252980547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e659545c79bec60e9a3f3da85e718e80455355564f22e42a29892b1298afae`  
		Last Modified: Wed, 25 Dec 2024 15:17:16 GMT  
		Size: 195.7 KB (195657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7155892ae9a5a223c50ffcff35eabf9cd29cea59ccf6d8cb0c8d20e6c609da`  
		Last Modified: Wed, 25 Dec 2024 15:17:17 GMT  
		Size: 821.3 KB (821315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:9c1844b7c666832da12e7df50406229494ae5d5295cbb6e98bc6028751dfe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23319696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b674c98231330fa259446855078fcc6a916895851425f46301c1af9b61a420`

```dockerfile
```

-	Layers:
	-	`sha256:bb2546b99f98828eae70083600523bf188b308d5780d56139cace5fae06db143`  
		Last Modified: Wed, 25 Dec 2024 15:17:17 GMT  
		Size: 23.3 MB (23300440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68d494505baed69f65acf3f176edd78d66a766a459deef456eb65f62fe78a9f`  
		Last Modified: Wed, 25 Dec 2024 15:17:16 GMT  
		Size: 19.3 KB (19256 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27` - linux; s390x

```console
$ docker pull erlang@sha256:b5720c90e3e0db7d392fad2d76ab7a8791d8856cb0a5da4e542e849e0b1fafa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.8 MB (556800299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800b31706dc9618d16ae140c9ec1365943d4f30d077fc126367d0fdee75589e2`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ceab2bfdf4c95c88012fc97d528a660b04b4860a4d40e2b8de8522c06340e1`  
		Last Modified: Wed, 25 Dec 2024 06:17:13 GMT  
		Size: 238.0 MB (237970245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd29eb7e44d4a62a2e3b3e18729ef0cbd2a6ca335889192c956de7050c55be`  
		Last Modified: Wed, 25 Dec 2024 06:17:08 GMT  
		Size: 195.6 KB (195631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb172553a2854a645489403db4ed5043b6f5b6077b2f4e98ecd8e78a1b6761c6`  
		Size: 821.3 KB (821329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27` - unknown; unknown

```console
$ docker pull erlang@sha256:06fd27500b5d2748023809bd4e84ff431f970f6d839959e6684a4b58fe655720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23137593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3ff217da93a17f0692a7182c66ac4f68fc8a9adafd1d9839df575a776805f8`

```dockerfile
```

-	Layers:
	-	`sha256:9d3a2e1931ea8370331e3b21c5985d61232125e97ec4a077deaa6ea8469ec09b`  
		Last Modified: Wed, 25 Dec 2024 06:17:09 GMT  
		Size: 23.1 MB (23118391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a2c18db37fc4423bafd3750acde723e96e9a25a2ffebd048c8797b290c7882`  
		Last Modified: Wed, 25 Dec 2024 06:17:08 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:27-alpine`

```console
$ docker pull erlang@sha256:05854b8b92a56d061b1a36eb2c851d6ee1e40ad30929469cad56137f038d9a47
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
$ docker pull erlang@sha256:a351bd21de3c41e76e90977c74a7e15d15ee721acd040da9be98c2b74dedd715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53006499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4cbccce2d80ead99f8c0e667b318f67e78339297aa8c5ddc4a8c4d756aa72f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48b35863f91c87a14e2ba19dfb7088ee93cad2959dbda7d9e7086da1e23703`  
		Last Modified: Tue, 07 Jan 2025 03:39:32 GMT  
		Size: 49.4 MB (49392500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7b748dd3036b15a4ca106a9fd843a5b8f2a0d35fa4240e7b398ec85929b4508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924bffc70fd0fa80d02de055cc69db2149254f7bdd88b5ff6c5744caec17bc0f`

```dockerfile
```

-	Layers:
	-	`sha256:f5af190452102e5b49f396f4d76c4debd05084b6243c00491c2b292118c282db`  
		Last Modified: Tue, 07 Jan 2025 03:39:31 GMT  
		Size: 266.0 KB (266045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da848724ba51f7c520b4fd20f671178102faef6a32e456c185234d424f4f87f8`  
		Last Modified: Tue, 07 Jan 2025 03:39:31 GMT  
		Size: 15.3 KB (15335 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:06f9a3b8dbe9012f2f2723832b98233656f5bded8d05aa6cd69fd75a01714fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e786d4fd9e6ce57860e1005f65a8bed53ee53f1708f75a558206d328baa09ab`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021561e32bc7d735a3ca18c47bd9bfb98c41cdc9547ebf6162c1d5f89b870ed`  
		Last Modified: Tue, 07 Jan 2025 06:28:31 GMT  
		Size: 47.0 MB (46979700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:19e0a8681705921ce0412e55e28a5fb0ad62b29e2d57b475ebcb0e95e7641d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 KB (277544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee27f51cab837a9a6a985307c82b1b7ce11fb1bce593adad681fd950397425c7`

```dockerfile
```

-	Layers:
	-	`sha256:ec41f2d99d71935ee186ce5c4032f5a2dff877abbae352ec91c2be80c783bb1d`  
		Last Modified: Tue, 07 Jan 2025 06:28:30 GMT  
		Size: 262.1 KB (262125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3401f929e1c2ee52055bcfdad9524af89cce52c2cfd99269b7375b502e6be0f4`  
		Last Modified: Tue, 07 Jan 2025 06:28:29 GMT  
		Size: 15.4 KB (15419 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3c2d3b05a9f0f4eeb8b50b5c76471d75236118eb4cb7b81e9ff2f2407f8a197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a27d91d422a5f29b97f550c27c31b63f412dfcb4546bc045d9d9e93261d081`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58feb9a513646346ca7c3340ff177f4efda09ea16deb67f1e8977fb523f74725`  
		Last Modified: Tue, 07 Jan 2025 07:33:20 GMT  
		Size: 49.2 MB (49166064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:c4ba7ba7001d1ad0d86bc6d2dbf39a19a4c5227813bce0cbec329ef97282da9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 KB (282298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2212a185296d1255ad37cbe499e6368c0572d4ef9ac6550b8f075fddd05e5a9`

```dockerfile
```

-	Layers:
	-	`sha256:071d5e67ee8f07d1e6fa1819379b21aea2167cf7c09758bb3bd534327bb8dfb9`  
		Last Modified: Tue, 07 Jan 2025 07:33:19 GMT  
		Size: 266.8 KB (266847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43437fca25a09c1f4458a9112cab5b2b7b3af44d2baa8ad98c39df01cc57787b`  
		Last Modified: Tue, 07 Jan 2025 07:33:19 GMT  
		Size: 15.5 KB (15451 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; 386

```console
$ docker pull erlang@sha256:685ed1f2fa5bf3e9f07d02d3dd3d387c54c8dd273984953350df49f0be7291c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51385052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db62104e678d0a5685932b3657445ae233c0675e8024a948d8b166657509d2c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf40bd28b413b16f5fd7206f649e9d911d5a529469de7b163394509f77fa16c0`  
		Last Modified: Tue, 07 Jan 2025 03:23:49 GMT  
		Size: 47.9 MB (47921863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e5d57ebdf6ad21185906eeef6f02a6a6a2cfddbc9ae1a706fb60ac606df8750d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 KB (276615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52af76bc4d517cabb31e45932658c213a48be4f0b91690a814caef65e05bb7d`

```dockerfile
```

-	Layers:
	-	`sha256:869eb41d8265c7dcac03c2d8ec00f4452f9403ce1fd2f37dfc5121cd48968637`  
		Last Modified: Tue, 07 Jan 2025 03:23:47 GMT  
		Size: 261.3 KB (261317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5096d893d0eb155bf8d324e9d90bad7b60c1f5c5324345a143425f8ee89e0d3b`  
		Last Modified: Tue, 07 Jan 2025 03:23:47 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:42b5f6b45b75d591272d6a9a2cfe094bb6ad1742c8840447fa326c97b7cfd475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51552359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b09289db6120be4f01458d89a12c11419d0bfc94a76174629b2c908a4dcae4`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd218b5c0cd5629d95f5330b58a7ac6b5f719f2aaa09d347b115684cb6f2eaf0`  
		Last Modified: Tue, 07 Jan 2025 06:26:18 GMT  
		Size: 48.0 MB (47983632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:37b8d548228847191948704dd8779fe717f06b87a22b8f6d1c4abf5b43dfc4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 KB (275555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd895db94d64313a255079372b29adaa56d640e0212e0311010b881f8489b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:95f16f6ce73de1c6e14583710900b7582c12d32b116f36822158fbc4f7fc7b14`  
		Last Modified: Tue, 07 Jan 2025 06:26:16 GMT  
		Size: 260.2 KB (260170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610f62352a10c30b3de359e5d28c64c36adcc240bc16ee50463149928b37dbdb`  
		Last Modified: Tue, 07 Jan 2025 06:26:16 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-alpine` - linux; s390x

```console
$ docker pull erlang@sha256:e9a9567109dece0eefbb849f1d8be36b4583dc2ab031be74a25a1e8fff3e56bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51097295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692e3879bbf28c5ab9ff5664b664285f19a287f680e7cea200f62dca4838df6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27896c8c81b4504c2f65731ee8687d5417b10384728d735294c81a200506444e`  
		Last Modified: Tue, 07 Jan 2025 06:33:56 GMT  
		Size: 47.6 MB (47638116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cfef83fdeb16b9a1e15c7df087f724ca76ed66e381515834916fbb7c226e3f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 KB (275464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e98ba1b7f51f3189d95b00eb8d374c6389baa01c1fb24336f28030116392b`

```dockerfile
```

-	Layers:
	-	`sha256:06b77da5883a6b757b7054bfb45ea540a8c7ebd0dc256d3374ab46af823da059`  
		Last Modified: Tue, 07 Jan 2025 06:33:55 GMT  
		Size: 260.1 KB (260130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acf786bd3d619a33a4fe5a565a25c21e336c7bb4395394aec7436e3e5bd1105`  
		Last Modified: Tue, 07 Jan 2025 06:33:55 GMT  
		Size: 15.3 KB (15334 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:27-slim`

```console
$ docker pull erlang@sha256:bd6a0a340a731c28cee42b6a7fbde23714827209149471587e0c1078c5b0ae40
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
$ docker pull erlang@sha256:8a7764d3569c3e08635123f0a57687bc48b5329f539186c9a9b9fecb7b764e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124376742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a63a8b7a65493dcbf30a7b4c667b098156e7972460f3f1f9fa828e4afd73cfa`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57160b581f62f2b52ac40bc5330a4e29f269cf62ac486e3b55faa4b77ea202ea`  
		Last Modified: Tue, 24 Dec 2024 22:34:08 GMT  
		Size: 75.9 MB (75879676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5b3a9d7f528a204501fa366691245e158ebd2d2c336942ae44a3f259f528a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c2dd46389dba58b041df4d2cf9146c9f87969170286a965e7bf4e69d8c8d7`

```dockerfile
```

-	Layers:
	-	`sha256:52b2fb379e0b45be025b85d5e71f5d3b494158d7b7f306ccac31c760f86ca7c4`  
		Last Modified: Tue, 24 Dec 2024 22:34:06 GMT  
		Size: 3.7 MB (3708310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2765e2716776fb43d4e9b649bdb32a0e157a09d9014898a61c9dcd7f0f178aee`  
		Last Modified: Tue, 24 Dec 2024 22:34:05 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:1155748c13766db01a9bf8b0a3e69b129319a1d11aafceaa2cdc7229bcdea770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ec520da0c93579b6f16cfa93379a2f4338cd47a57de1599174c311e93a3211`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5977d1981a8dd254a92982955efea7890617039368c7131153d9913973730c53`  
		Last Modified: Wed, 25 Dec 2024 01:37:28 GMT  
		Size: 65.4 MB (65386638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:884bd12e34a02ac53ad606a847e930a3f06ab2d083dccd9517baf3660920d29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2908b8545300577bc8ef714778d50a388124576b333ec5d0b429c9678e4815b5`

```dockerfile
```

-	Layers:
	-	`sha256:4709628c48e0641c3cc528aef265449b46e032ef574d730b1cc88577d4ab7158`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 3.7 MB (3711818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778cdbf3096cc564dda153ba6a8391f95d6505b0b23333d3b08a8082385611c4`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 14.0 KB (13973 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c8954360d037661bc8e3c7eff45777938b1aa1cfbd98e4327ed4017260f01e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109201698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657bbd1df719fcc47286f0de9d320ea112f04ccd618e708afd8721a9fced2896`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd3b67bcaa47bfd165b47944e6f50a16520251fc5eeccb01a2d7db1f8a34814`  
		Size: 65.0 MB (65001731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c845e709fe7bf379c3d663d6e6b3f52e7ddbe6d84530099dd4e3518c826fecbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef7e8ba94456afecff8069d3f8ccaa483ee04bf64312074bb5f11090c3f8e00`

```dockerfile
```

-	Layers:
	-	`sha256:222381da80919f2bccf1c80ead5b76809fea671e97764be36ba662594db7284b`  
		Last Modified: Wed, 25 Dec 2024 03:55:37 GMT  
		Size: 3.7 MB (3710551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cb7d242e35f1bc90fe440971faeb4c2d8acd4c7919ddcf86eac8c40dc54b6a`  
		Last Modified: Wed, 25 Dec 2024 03:55:36 GMT  
		Size: 14.0 KB (13974 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:338ad52bd5bc129614e59e62776c6fdb7c7d94bf79e81cee7626e602267ac0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121931347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a0e9557b4f0c547aad36260b6431522efdd8593ffee576180ba285b4a57f4`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0a8527debe66b1505e613945c00c8576baf9c99fb6d6308da79ca1400ddc34`  
		Last Modified: Wed, 25 Dec 2024 02:01:20 GMT  
		Size: 73.6 MB (73605863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0e1cfb08ca900e7fc9768c3da077b0d06d14923d05278ae7bd3e2e372ad2a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4b21e583cb7a928574219b50f4b6911cbf062ada79eab277506b8ed53a99c`

```dockerfile
```

-	Layers:
	-	`sha256:8827a27fa02267203330fae3c89d68b4d691ffa1892b82b4b17a2257feb6360d`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 3.7 MB (3708583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f497fa284301c23782d235f31e714af859337ac8dfeb00de4a105d4c7eaf8e4`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 14.0 KB (14006 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:2f2e413ea00c5e2b93fdeb9b6fb67b0e02de9a65918e89adc22a224bd6e9d53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115512518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b12918f88e3c119d723773b254f550d051dc4db7e7aaeeb36497c14fed8a9b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b22076394db0050e1759c670f6766f37c079ab365e197c55432853c533243`  
		Last Modified: Tue, 24 Dec 2024 22:22:06 GMT  
		Size: 66.0 MB (66036593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:24fca4e3ee5d4262ae0d542f044d456bfbcbfe0f88d789b5a9fcfb917ec0cc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3ba3e92696f3643b65909192a33f4b95b615309b2c2bd32121c14135183dc6`

```dockerfile
```

-	Layers:
	-	`sha256:f987f2af121a04680c6a77bfe986d48acec53956fc5f34adae553479381b7cdc`  
		Last Modified: Tue, 24 Dec 2024 22:22:05 GMT  
		Size: 3.7 MB (3705425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ccc1286455abb66b1b6d05104e1faecfafcadd991e84c3893ecbdf1389fc8e`  
		Last Modified: Tue, 24 Dec 2024 22:22:04 GMT  
		Size: 13.9 KB (13853 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:6878126bc5eab525e88939c3dcd9778f3ae571099d9cf31ea0fa9b33d6603b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114725839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149e8c0cc59411546dcaaee0aa7d7e6566b55c06f39a3733ab969fdf2613a35`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d01b0d87100f2cd288afbeb15499e7514ba1addf3aee3e1cab5039ec5decf08`  
		Last Modified: Wed, 25 Dec 2024 12:16:22 GMT  
		Size: 66.0 MB (65954195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b8c258df00c17a2e8018343ddfe38c110855f7bad2dbf5ec3969c90a87cb4bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4e66b344bfaea7b9085c57fa3028be6cf0b76aa495c060760694e6e26321c4`

```dockerfile
```

-	Layers:
	-	`sha256:36877d4bf64b6955f62cb9f2af3dbaea276a46f805df483b7af961c1f8e91282`  
		Last Modified: Wed, 25 Dec 2024 12:16:15 GMT  
		Size: 13.8 KB (13750 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:29cc1f73e1f62e405bbbad16f6bc09138612090084395f3ace212828ed623f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119438210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8e95b295dd3021a97782b883363323043473b39b77f297274c0a4892279f25`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef160bc98a9c8aea760d70e8b3c892f017d4b75235618078eadf79921a61bbcc`  
		Last Modified: Wed, 25 Dec 2024 13:05:52 GMT  
		Size: 67.1 MB (67110135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:82e357776dbb2a3cfb59b76dc1edd2a28f7ed92de100f6a8c9601516d40d37e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f00ca30ce871ec83a68617374877257b1a3d30b0427855883187562a65020`

```dockerfile
```

-	Layers:
	-	`sha256:e4059ba186e389b3f9cf29e519b5049d16e4017e577ee8ceaa870e19a865ef7a`  
		Size: 3.7 MB (3712656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59010ce44d36c8a32827cf2e64ed95411713db6d2ad3d6fb56cddde89fc4de2d`  
		Last Modified: Wed, 25 Dec 2024 13:05:49 GMT  
		Size: 13.9 KB (13940 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:a54d1a0e95bebeb49387b2ec9d92ce2360b28a36335d7cbbd4b412b2e06d133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112941329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd79168b47370c9c1c3967213330957b1da2585b3f954ddc037d9a765fe404d0`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab6ad539b4b078ed51f9865d4a9375df6f24b12a6e5850e030c1fc1ca2a143`  
		Last Modified: Wed, 25 Dec 2024 00:28:51 GMT  
		Size: 65.8 MB (65791704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d6212b133217e9c8a71c5850e70a3387adaac1f48cae50cbecb23a68a19b5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2d815f487e8fa903da4711e96ed6ae290a098f89b3b9aac0d5a3429311d687`

```dockerfile
```

-	Layers:
	-	`sha256:df23929c7696b1018d5044cd4043d25fc047f5a77c9f56d8011647220fc6ac1e`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 3.7 MB (3708030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d763c059646c63324ba9cd7a2b46db25f879ab2576ce1febeb109e58af3cbc78`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:27.2`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2-alpine`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2-slim`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0-alpine`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0-slim`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0.0`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0.0-alpine`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:27.2.0.0-slim`

```console
$ docker pull erlang@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `erlang:alpine`

```console
$ docker pull erlang@sha256:05854b8b92a56d061b1a36eb2c851d6ee1e40ad30929469cad56137f038d9a47
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
$ docker pull erlang@sha256:a351bd21de3c41e76e90977c74a7e15d15ee721acd040da9be98c2b74dedd715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53006499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4cbccce2d80ead99f8c0e667b318f67e78339297aa8c5ddc4a8c4d756aa72f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48b35863f91c87a14e2ba19dfb7088ee93cad2959dbda7d9e7086da1e23703`  
		Last Modified: Tue, 07 Jan 2025 03:39:32 GMT  
		Size: 49.4 MB (49392500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:7b748dd3036b15a4ca106a9fd843a5b8f2a0d35fa4240e7b398ec85929b4508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924bffc70fd0fa80d02de055cc69db2149254f7bdd88b5ff6c5744caec17bc0f`

```dockerfile
```

-	Layers:
	-	`sha256:f5af190452102e5b49f396f4d76c4debd05084b6243c00491c2b292118c282db`  
		Last Modified: Tue, 07 Jan 2025 03:39:31 GMT  
		Size: 266.0 KB (266045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da848724ba51f7c520b4fd20f671178102faef6a32e456c185234d424f4f87f8`  
		Last Modified: Tue, 07 Jan 2025 03:39:31 GMT  
		Size: 15.3 KB (15335 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm variant v7

```console
$ docker pull erlang@sha256:06f9a3b8dbe9012f2f2723832b98233656f5bded8d05aa6cd69fd75a01714fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e786d4fd9e6ce57860e1005f65a8bed53ee53f1708f75a558206d328baa09ab`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021561e32bc7d735a3ca18c47bd9bfb98c41cdc9547ebf6162c1d5f89b870ed`  
		Last Modified: Tue, 07 Jan 2025 06:28:31 GMT  
		Size: 47.0 MB (46979700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:19e0a8681705921ce0412e55e28a5fb0ad62b29e2d57b475ebcb0e95e7641d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 KB (277544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee27f51cab837a9a6a985307c82b1b7ce11fb1bce593adad681fd950397425c7`

```dockerfile
```

-	Layers:
	-	`sha256:ec41f2d99d71935ee186ce5c4032f5a2dff877abbae352ec91c2be80c783bb1d`  
		Last Modified: Tue, 07 Jan 2025 06:28:30 GMT  
		Size: 262.1 KB (262125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3401f929e1c2ee52055bcfdad9524af89cce52c2cfd99269b7375b502e6be0f4`  
		Last Modified: Tue, 07 Jan 2025 06:28:29 GMT  
		Size: 15.4 KB (15419 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3c2d3b05a9f0f4eeb8b50b5c76471d75236118eb4cb7b81e9ff2f2407f8a197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a27d91d422a5f29b97f550c27c31b63f412dfcb4546bc045d9d9e93261d081`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58feb9a513646346ca7c3340ff177f4efda09ea16deb67f1e8977fb523f74725`  
		Last Modified: Tue, 07 Jan 2025 07:33:20 GMT  
		Size: 49.2 MB (49166064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:c4ba7ba7001d1ad0d86bc6d2dbf39a19a4c5227813bce0cbec329ef97282da9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 KB (282298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2212a185296d1255ad37cbe499e6368c0572d4ef9ac6550b8f075fddd05e5a9`

```dockerfile
```

-	Layers:
	-	`sha256:071d5e67ee8f07d1e6fa1819379b21aea2167cf7c09758bb3bd534327bb8dfb9`  
		Last Modified: Tue, 07 Jan 2025 07:33:19 GMT  
		Size: 266.8 KB (266847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43437fca25a09c1f4458a9112cab5b2b7b3af44d2baa8ad98c39df01cc57787b`  
		Last Modified: Tue, 07 Jan 2025 07:33:19 GMT  
		Size: 15.5 KB (15451 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; 386

```console
$ docker pull erlang@sha256:685ed1f2fa5bf3e9f07d02d3dd3d387c54c8dd273984953350df49f0be7291c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51385052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db62104e678d0a5685932b3657445ae233c0675e8024a948d8b166657509d2c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf40bd28b413b16f5fd7206f649e9d911d5a529469de7b163394509f77fa16c0`  
		Last Modified: Tue, 07 Jan 2025 03:23:49 GMT  
		Size: 47.9 MB (47921863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:e5d57ebdf6ad21185906eeef6f02a6a6a2cfddbc9ae1a706fb60ac606df8750d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 KB (276615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52af76bc4d517cabb31e45932658c213a48be4f0b91690a814caef65e05bb7d`

```dockerfile
```

-	Layers:
	-	`sha256:869eb41d8265c7dcac03c2d8ec00f4452f9403ce1fd2f37dfc5121cd48968637`  
		Last Modified: Tue, 07 Jan 2025 03:23:47 GMT  
		Size: 261.3 KB (261317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5096d893d0eb155bf8d324e9d90bad7b60c1f5c5324345a143425f8ee89e0d3b`  
		Last Modified: Tue, 07 Jan 2025 03:23:47 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; ppc64le

```console
$ docker pull erlang@sha256:42b5f6b45b75d591272d6a9a2cfe094bb6ad1742c8840447fa326c97b7cfd475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51552359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b09289db6120be4f01458d89a12c11419d0bfc94a76174629b2c908a4dcae4`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd218b5c0cd5629d95f5330b58a7ac6b5f719f2aaa09d347b115684cb6f2eaf0`  
		Last Modified: Tue, 07 Jan 2025 06:26:18 GMT  
		Size: 48.0 MB (47983632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:37b8d548228847191948704dd8779fe717f06b87a22b8f6d1c4abf5b43dfc4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 KB (275555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd895db94d64313a255079372b29adaa56d640e0212e0311010b881f8489b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:95f16f6ce73de1c6e14583710900b7582c12d32b116f36822158fbc4f7fc7b14`  
		Last Modified: Tue, 07 Jan 2025 06:26:16 GMT  
		Size: 260.2 KB (260170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610f62352a10c30b3de359e5d28c64c36adcc240bc16ee50463149928b37dbdb`  
		Last Modified: Tue, 07 Jan 2025 06:26:16 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:alpine` - linux; s390x

```console
$ docker pull erlang@sha256:e9a9567109dece0eefbb849f1d8be36b4583dc2ab031be74a25a1e8fff3e56bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51097295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692e3879bbf28c5ab9ff5664b664285f19a287f680e7cea200f62dca4838df6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 11 Nov 2024 01:27:43 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2024 01:27:43 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Mon, 11 Nov 2024 01:27:43 GMT
LABEL org.opencontainers.image.version=27.1.2
# Mon, 11 Nov 2024 01:27:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& apk add --no-cache --virtual .fetch-deps 		curl 		ca-certificates 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& apk add --no-cache --virtual .build-deps 		dpkg-dev dpkg 		gcc 		g++ 		libc-dev 		linux-headers 		make 		autoconf 		ncurses-dev 		openssl-dev 		unixodbc-dev 		lksctp-tools-dev 		tar 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(getconf _NPROCESSORS_ONLN) 	  && make install ) 	&& rm -rf $ERL_TOP 	&& find /usr/local -regex '/usr/local/lib/erlang/\(lib/\|erts-\).*/\(man\|doc\|obj\|c_src\|emacs\|info\|examples\)' | xargs rm -rf 	&& find /usr/local -name src | xargs -r find | grep -v '\.hrl$' | xargs rm -v || true 	&& find /usr/local -name src | xargs -r find | xargs rmdir -vp || true 	&& scanelf --nobanner -E ET_EXEC -BF '%F' --recursive /usr/local | xargs -r strip --strip-all 	&& scanelf --nobanner -E ET_DYN -BF '%F' --recursive /usr/local | xargs -r strip --strip-unneeded 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "${REBAR3_DOWNLOAD_SHA256}  rebar3-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/rebar3-src 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apk add --virtual .erlang-rundeps 		$runDeps 		lksctp-tools 		ca-certificates 	&& apk del .fetch-deps .build-deps # buildkit
# Mon, 11 Nov 2024 01:27:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27896c8c81b4504c2f65731ee8687d5417b10384728d735294c81a200506444e`  
		Last Modified: Tue, 07 Jan 2025 06:33:56 GMT  
		Size: 47.6 MB (47638116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:alpine` - unknown; unknown

```console
$ docker pull erlang@sha256:cfef83fdeb16b9a1e15c7df087f724ca76ed66e381515834916fbb7c226e3f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 KB (275464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e98ba1b7f51f3189d95b00eb8d374c6389baa01c1fb24336f28030116392b`

```dockerfile
```

-	Layers:
	-	`sha256:06b77da5883a6b757b7054bfb45ea540a8c7ebd0dc256d3374ab46af823da059`  
		Last Modified: Tue, 07 Jan 2025 06:33:55 GMT  
		Size: 260.1 KB (260130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acf786bd3d619a33a4fe5a565a25c21e336c7bb4395394aec7436e3e5bd1105`  
		Last Modified: Tue, 07 Jan 2025 06:33:55 GMT  
		Size: 15.3 KB (15334 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:latest`

```console
$ docker pull erlang@sha256:30c18a712d6585cc50442c32d4b2604a96fdd5cb7000b342a31a9d1f1d479876
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

### `erlang:latest` - linux; amd64

```console
$ docker pull erlang@sha256:99fabb58c8add16e134bfa43b7874e0468e111eb30e41683e34e005df6e756c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605221293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4e617a8dd5747e8aa23edcaea29c2384ca24d06859325688251b7f90aba828`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 07 Jan 2025 19:42:38 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 07 Jan 2025 19:42:44 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1fa9d56affb1708880f4b6ab4d9e6b91ba98414f99e9bca2e3a58e8646f2af`  
		Last Modified: Wed, 25 Dec 2024 01:24:13 GMT  
		Size: 256.1 MB (256144262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1270907cb1565acfcc904362d76a5ca99e617db91a14425a934a3f16c66ef`  
		Last Modified: Wed, 25 Dec 2024 01:24:09 GMT  
		Size: 195.5 KB (195541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa46f6a9bbce8d3c68f7061655cd3fd184429aa2a44c95cd452444976b7ca2`  
		Last Modified: Wed, 25 Dec 2024 01:24:10 GMT  
		Size: 821.3 KB (821332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:39f22180b15d840768f3642631a34da0d67b26fdd63737a52c9a82f68fbeaf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23363890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4429102bf23cd4507142400a334315874c4d6af43d5c3e052f2c2f54ef2787b6`

```dockerfile
```

-	Layers:
	-	`sha256:ea8a3e340c338a89aee29d25fbca5e6b31c81c184f84c9077491f39ae76bf094`  
		Last Modified: Wed, 25 Dec 2024 01:24:10 GMT  
		Size: 23.3 MB (23344688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecfb4c011f6c3d2220769b9d44e881c579da98afcd09bd3135bd01199666e9b3`  
		Last Modified: Wed, 25 Dec 2024 01:24:09 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5183973f667f6d1120a9cf2ce3e8dc78df15004654f6e23a7fa039f9100ef19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.1 MB (546129180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15648fa772ced49662325d600df624cc56e622fc533be85d7488f081573481`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ea73065182aff84baae30fc5bf818aa4a65c4f812a250b75387f9473ee9dbe`  
		Last Modified: Wed, 25 Dec 2024 07:18:08 GMT  
		Size: 229.9 MB (229949555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9093f57181462e4beaba6ed1a675c3357a01e9894da94519650129c4591ae0d`  
		Last Modified: Wed, 25 Dec 2024 07:18:01 GMT  
		Size: 195.6 KB (195631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fa45fed5692cf06d60993c47e9ab183d304c655eda2785025e6b98b5495aa`  
		Last Modified: Wed, 25 Dec 2024 07:18:01 GMT  
		Size: 821.3 KB (821338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:939bd9180cde1602559da196a15afd4a63fd88c154069c05b92f4d71634a0a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23162616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2389830af8e421e505174b392a79f881bf52c8b08ab11ce0fd9503c4fa4ffb`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc6a584843e1b3a9322c2e9152999a606df65cd80d39b35387d7056b3d4d92`  
		Last Modified: Wed, 25 Dec 2024 07:18:02 GMT  
		Size: 23.1 MB (23143304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfc224d92619411b68de17e76585e8143daaa2ea7a40a3b7a9a0767fa6c1523`  
		Size: 19.3 KB (19312 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:03b3dcaebfc835b62dde5123e431be56ae07d7699eed98c7a43c7c7c392381a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379cae6b29d5176fa14f7c711ac7499194ca5f373fcbc7c58c1eb172edabee85`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608a6e836c054e460dafcb58b25ae0baf73ca4eccb3619b34bb852e2c7cff815`  
		Size: 226.9 MB (226885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb971de189c803b0fb04e427e6b7b5d5bc32024867217fe1b2ff562406ccc89`  
		Last Modified: Wed, 25 Dec 2024 16:53:53 GMT  
		Size: 195.6 KB (195642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799649653d972a5db0d9258b5824864c11a773927516774d7c394f1aceada23a`  
		Last Modified: Wed, 25 Dec 2024 16:53:53 GMT  
		Size: 821.3 KB (821302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:e74f54d5b78b06ea7553a04987be90c0421e36efdc766ec928018ac0f533eef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23179531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2188b6842715e6e12a61da94a877db437bb5189cdfe5efe2015b63a55255330`

```dockerfile
```

-	Layers:
	-	`sha256:7bbc6b6b9a82a2881bbd11b24aec6f6b7c4d5c659d88a78a2bb8a5bc69329300`  
		Size: 23.2 MB (23160219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05398deec71d32480663454194af67ef578c84a0a599ec3f6f74a23dfafa3455`  
		Last Modified: Wed, 25 Dec 2024 16:53:52 GMT  
		Size: 19.3 KB (19312 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:5f6811bbc0f356334731ff174b7f013f492cdbb6ddfec4fba901950630b1aa45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589036181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64784a4b1244d9ad24c5b318b44544500bc20bef1dc6d69a0dbbfd0d51e2b60b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed0d2a2ae42a69f4e657b8164d5cf04eaa475cc4d5dc5dfed3b28b7dbd423a1`  
		Last Modified: Wed, 25 Dec 2024 12:30:06 GMT  
		Size: 249.3 MB (249254232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f8f93d2b1ed5f5cc02d8ca2bc073465324f5f9ef06b16254c27c65e7e2a49`  
		Size: 195.6 KB (195569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b806ce1db1d4f580c3392845480225d89e57d604fb887f0f47edccfc126e5b80`  
		Size: 821.3 KB (821278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:67c6056b29f8bd7998c03981658114d018ae619eabda4c85af90da4897d8bad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39df355ebaf6df09d32a06dce361dd68b104a4f1e20cc7628e9fab29a56fc7f2`

```dockerfile
```

-	Layers:
	-	`sha256:328269cb5e77fa3bb690f8b0365251ed6f36f23321f5deb7f5ed15f5040dfe26`  
		Last Modified: Wed, 25 Dec 2024 12:30:01 GMT  
		Size: 23.4 MB (23384751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991242e456df84220189bc7db2b8e31b0c0727a1094b042b3873517211340976`  
		Last Modified: Wed, 25 Dec 2024 12:30:00 GMT  
		Size: 19.3 KB (19348 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:227add7c2321a1f4b6a1b04f0a177f7a1deea8708d0f326c5cb9bed2db390b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601278684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af7d8f27cd74040bc6be35edc698f665c4a15a6eefc9f8926fe4a0557c7abb8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414055dc2d9dec686a13c75d418be0d93a97bbad9c4e7f00846954d342df493`  
		Last Modified: Wed, 25 Dec 2024 01:25:00 GMT  
		Size: 249.6 MB (249644211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11fa62a5970bdf7d0a1fd0e9e0b9419855c43f55ad8ca08d886e1ce40806954`  
		Size: 195.6 KB (195636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dcec6387d29c04ccbc18857d73690830401fe7181e04e40547e1af09ee8197`  
		Last Modified: Wed, 25 Dec 2024 01:24:55 GMT  
		Size: 821.4 KB (821435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:785d2b69f6ceafae0bb4828fc14ee3f48eebc4ae9b86ea93e47b8782671c47e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23331997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d1036ee2b0e41bf48b16406ebd81800b51a67788ee40685df7b92a82e6b85`

```dockerfile
```

-	Layers:
	-	`sha256:6726c6e7b23cb258853e83bf8bc844d0f31b2f946c268c8872d793baa73ba85b`  
		Last Modified: Wed, 25 Dec 2024 01:24:55 GMT  
		Size: 23.3 MB (23312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638316d475cb74b2622a0ededd1ae4825ade6500965453db1678b54255921f30`  
		Last Modified: Wed, 25 Dec 2024 01:24:54 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:b98dc4f484a308f9f4a4258233b0e0da4219fdc0c34eac6f3a12478e44271f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557826987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b611bf0f0ce629552dc84765d74b9ce8114b7d9ba20a89c88e6339cddaf7c81e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d59611bc70f4b1369b7db96419bebc75eabdd8aab62992c0b6957531b936a9`  
		Last Modified: Thu, 26 Dec 2024 02:31:18 GMT  
		Size: 231.4 MB (231420494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67bb1cd31bcdae914ac4e88288fc650e8876f7202c6f6e561b3373ed3689049`  
		Last Modified: Thu, 26 Dec 2024 02:30:57 GMT  
		Size: 195.6 KB (195624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14e4a162bc78e060d78f4efe12b2733e57267e29dac42b9ddee204aa85ec2f3`  
		Last Modified: Thu, 26 Dec 2024 02:30:58 GMT  
		Size: 821.6 KB (821571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:c7df58fbac00a7135f73b06f6812bef0a6582aedb90b2ff3e8a039b6c9cc2498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951e8e3ed6f60f834c81c384f5d7e206362f8a3e404fea58eb77ca3eb82a6303`

```dockerfile
```

-	Layers:
	-	`sha256:608100a4191d5db95ad0e6e655c39b7c32ec8866e82682416abe3344a4d8a0ae`  
		Last Modified: Thu, 26 Dec 2024 02:30:57 GMT  
		Size: 19.1 KB (19068 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:cf79aa893784143632f62693b32f5cf875e7dbdc97636b174d892f2c006fa933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (616000684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f6ca837a3038110742307da61a811d0733e9a5594a9ead883adc177e8cf5e3`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564e9522ca734303d4ec01d6ea5f5ced0d604d04738fa1a581dc039d215aad1b`  
		Last Modified: Wed, 25 Dec 2024 15:17:23 GMT  
		Size: 253.0 MB (252980547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e659545c79bec60e9a3f3da85e718e80455355564f22e42a29892b1298afae`  
		Last Modified: Wed, 25 Dec 2024 15:17:16 GMT  
		Size: 195.7 KB (195657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7155892ae9a5a223c50ffcff35eabf9cd29cea59ccf6d8cb0c8d20e6c609da`  
		Last Modified: Wed, 25 Dec 2024 15:17:17 GMT  
		Size: 821.3 KB (821315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:9c1844b7c666832da12e7df50406229494ae5d5295cbb6e98bc6028751dfe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23319696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b674c98231330fa259446855078fcc6a916895851425f46301c1af9b61a420`

```dockerfile
```

-	Layers:
	-	`sha256:bb2546b99f98828eae70083600523bf188b308d5780d56139cace5fae06db143`  
		Last Modified: Wed, 25 Dec 2024 15:17:17 GMT  
		Size: 23.3 MB (23300440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68d494505baed69f65acf3f176edd78d66a766a459deef456eb65f62fe78a9f`  
		Last Modified: Wed, 25 Dec 2024 15:17:16 GMT  
		Size: 19.3 KB (19256 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:b5720c90e3e0db7d392fad2d76ab7a8791d8856cb0a5da4e542e849e0b1fafa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.8 MB (556800299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800b31706dc9618d16ae140c9ec1365943d4f30d077fc126367d0fdee75589e2`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ceab2bfdf4c95c88012fc97d528a660b04b4860a4d40e2b8de8522c06340e1`  
		Last Modified: Wed, 25 Dec 2024 06:17:13 GMT  
		Size: 238.0 MB (237970245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd29eb7e44d4a62a2e3b3e18729ef0cbd2a6ca335889192c956de7050c55be`  
		Last Modified: Wed, 25 Dec 2024 06:17:08 GMT  
		Size: 195.6 KB (195631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb172553a2854a645489403db4ed5043b6f5b6077b2f4e98ecd8e78a1b6761c6`  
		Size: 821.3 KB (821329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:06fd27500b5d2748023809bd4e84ff431f970f6d839959e6684a4b58fe655720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23137593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3ff217da93a17f0692a7182c66ac4f68fc8a9adafd1d9839df575a776805f8`

```dockerfile
```

-	Layers:
	-	`sha256:9d3a2e1931ea8370331e3b21c5985d61232125e97ec4a077deaa6ea8469ec09b`  
		Last Modified: Wed, 25 Dec 2024 06:17:09 GMT  
		Size: 23.1 MB (23118391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a2c18db37fc4423bafd3750acde723e96e9a25a2ffebd048c8797b290c7882`  
		Last Modified: Wed, 25 Dec 2024 06:17:08 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

## `erlang:slim`

```console
$ docker pull erlang@sha256:bd6a0a340a731c28cee42b6a7fbde23714827209149471587e0c1078c5b0ae40
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

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:8a7764d3569c3e08635123f0a57687bc48b5329f539186c9a9b9fecb7b764e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124376742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a63a8b7a65493dcbf30a7b4c667b098156e7972460f3f1f9fa828e4afd73cfa`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57160b581f62f2b52ac40bc5330a4e29f269cf62ac486e3b55faa4b77ea202ea`  
		Last Modified: Tue, 24 Dec 2024 22:34:08 GMT  
		Size: 75.9 MB (75879676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5b3a9d7f528a204501fa366691245e158ebd2d2c336942ae44a3f259f528a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c2dd46389dba58b041df4d2cf9146c9f87969170286a965e7bf4e69d8c8d7`

```dockerfile
```

-	Layers:
	-	`sha256:52b2fb379e0b45be025b85d5e71f5d3b494158d7b7f306ccac31c760f86ca7c4`  
		Last Modified: Tue, 24 Dec 2024 22:34:06 GMT  
		Size: 3.7 MB (3708310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2765e2716776fb43d4e9b649bdb32a0e157a09d9014898a61c9dcd7f0f178aee`  
		Last Modified: Tue, 24 Dec 2024 22:34:05 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:1155748c13766db01a9bf8b0a3e69b129319a1d11aafceaa2cdc7229bcdea770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ec520da0c93579b6f16cfa93379a2f4338cd47a57de1599174c311e93a3211`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5977d1981a8dd254a92982955efea7890617039368c7131153d9913973730c53`  
		Last Modified: Wed, 25 Dec 2024 01:37:28 GMT  
		Size: 65.4 MB (65386638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:884bd12e34a02ac53ad606a847e930a3f06ab2d083dccd9517baf3660920d29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2908b8545300577bc8ef714778d50a388124576b333ec5d0b429c9678e4815b5`

```dockerfile
```

-	Layers:
	-	`sha256:4709628c48e0641c3cc528aef265449b46e032ef574d730b1cc88577d4ab7158`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 3.7 MB (3711818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778cdbf3096cc564dda153ba6a8391f95d6505b0b23333d3b08a8082385611c4`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 14.0 KB (13973 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c8954360d037661bc8e3c7eff45777938b1aa1cfbd98e4327ed4017260f01e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109201698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657bbd1df719fcc47286f0de9d320ea112f04ccd618e708afd8721a9fced2896`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd3b67bcaa47bfd165b47944e6f50a16520251fc5eeccb01a2d7db1f8a34814`  
		Size: 65.0 MB (65001731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c845e709fe7bf379c3d663d6e6b3f52e7ddbe6d84530099dd4e3518c826fecbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef7e8ba94456afecff8069d3f8ccaa483ee04bf64312074bb5f11090c3f8e00`

```dockerfile
```

-	Layers:
	-	`sha256:222381da80919f2bccf1c80ead5b76809fea671e97764be36ba662594db7284b`  
		Last Modified: Wed, 25 Dec 2024 03:55:37 GMT  
		Size: 3.7 MB (3710551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cb7d242e35f1bc90fe440971faeb4c2d8acd4c7919ddcf86eac8c40dc54b6a`  
		Last Modified: Wed, 25 Dec 2024 03:55:36 GMT  
		Size: 14.0 KB (13974 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:338ad52bd5bc129614e59e62776c6fdb7c7d94bf79e81cee7626e602267ac0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121931347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a0e9557b4f0c547aad36260b6431522efdd8593ffee576180ba285b4a57f4`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0a8527debe66b1505e613945c00c8576baf9c99fb6d6308da79ca1400ddc34`  
		Last Modified: Wed, 25 Dec 2024 02:01:20 GMT  
		Size: 73.6 MB (73605863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0e1cfb08ca900e7fc9768c3da077b0d06d14923d05278ae7bd3e2e372ad2a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4b21e583cb7a928574219b50f4b6911cbf062ada79eab277506b8ed53a99c`

```dockerfile
```

-	Layers:
	-	`sha256:8827a27fa02267203330fae3c89d68b4d691ffa1892b82b4b17a2257feb6360d`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 3.7 MB (3708583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f497fa284301c23782d235f31e714af859337ac8dfeb00de4a105d4c7eaf8e4`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 14.0 KB (14006 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:2f2e413ea00c5e2b93fdeb9b6fb67b0e02de9a65918e89adc22a224bd6e9d53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115512518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b12918f88e3c119d723773b254f550d051dc4db7e7aaeeb36497c14fed8a9b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b22076394db0050e1759c670f6766f37c079ab365e197c55432853c533243`  
		Last Modified: Tue, 24 Dec 2024 22:22:06 GMT  
		Size: 66.0 MB (66036593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:24fca4e3ee5d4262ae0d542f044d456bfbcbfe0f88d789b5a9fcfb917ec0cc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3ba3e92696f3643b65909192a33f4b95b615309b2c2bd32121c14135183dc6`

```dockerfile
```

-	Layers:
	-	`sha256:f987f2af121a04680c6a77bfe986d48acec53956fc5f34adae553479381b7cdc`  
		Last Modified: Tue, 24 Dec 2024 22:22:05 GMT  
		Size: 3.7 MB (3705425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ccc1286455abb66b1b6d05104e1faecfafcadd991e84c3893ecbdf1389fc8e`  
		Last Modified: Tue, 24 Dec 2024 22:22:04 GMT  
		Size: 13.9 KB (13853 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:6878126bc5eab525e88939c3dcd9778f3ae571099d9cf31ea0fa9b33d6603b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114725839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149e8c0cc59411546dcaaee0aa7d7e6566b55c06f39a3733ab969fdf2613a35`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d01b0d87100f2cd288afbeb15499e7514ba1addf3aee3e1cab5039ec5decf08`  
		Last Modified: Wed, 25 Dec 2024 12:16:22 GMT  
		Size: 66.0 MB (65954195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b8c258df00c17a2e8018343ddfe38c110855f7bad2dbf5ec3969c90a87cb4bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4e66b344bfaea7b9085c57fa3028be6cf0b76aa495c060760694e6e26321c4`

```dockerfile
```

-	Layers:
	-	`sha256:36877d4bf64b6955f62cb9f2af3dbaea276a46f805df483b7af961c1f8e91282`  
		Last Modified: Wed, 25 Dec 2024 12:16:15 GMT  
		Size: 13.8 KB (13750 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:29cc1f73e1f62e405bbbad16f6bc09138612090084395f3ace212828ed623f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119438210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8e95b295dd3021a97782b883363323043473b39b77f297274c0a4892279f25`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef160bc98a9c8aea760d70e8b3c892f017d4b75235618078eadf79921a61bbcc`  
		Last Modified: Wed, 25 Dec 2024 13:05:52 GMT  
		Size: 67.1 MB (67110135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:82e357776dbb2a3cfb59b76dc1edd2a28f7ed92de100f6a8c9601516d40d37e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f00ca30ce871ec83a68617374877257b1a3d30b0427855883187562a65020`

```dockerfile
```

-	Layers:
	-	`sha256:e4059ba186e389b3f9cf29e519b5049d16e4017e577ee8ceaa870e19a865ef7a`  
		Size: 3.7 MB (3712656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59010ce44d36c8a32827cf2e64ed95411713db6d2ad3d6fb56cddde89fc4de2d`  
		Last Modified: Wed, 25 Dec 2024 13:05:49 GMT  
		Size: 13.9 KB (13940 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:a54d1a0e95bebeb49387b2ec9d92ce2360b28a36335d7cbbd4b412b2e06d133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112941329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd79168b47370c9c1c3967213330957b1da2585b3f954ddc037d9a765fe404d0`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab6ad539b4b078ed51f9865d4a9375df6f24b12a6e5850e030c1fc1ca2a143`  
		Last Modified: Wed, 25 Dec 2024 00:28:51 GMT  
		Size: 65.8 MB (65791704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d6212b133217e9c8a71c5850e70a3387adaac1f48cae50cbecb23a68a19b5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2d815f487e8fa903da4711e96ed6ae290a098f89b3b9aac0d5a3429311d687`

```dockerfile
```

-	Layers:
	-	`sha256:df23929c7696b1018d5044cd4043d25fc047f5a77c9f56d8011647220fc6ac1e`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 3.7 MB (3708030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d763c059646c63324ba9cd7a2b46db25f879ab2576ce1febeb109e58af3cbc78`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json
