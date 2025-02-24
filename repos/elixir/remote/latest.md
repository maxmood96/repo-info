## `elixir:latest`

```console
$ docker pull elixir@sha256:6d461a5d44f89a8c5cbab294021b9939b13f62f5116e5c7e32c3c9a2203e0705
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

### `elixir:latest` - linux; amd64

```console
$ docker pull elixir@sha256:fd3add1b49716428ca5cb92cce4cb401ea62a251e3fa7f2bce0be3cdcd27e941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388a0635a64b3ed57d815efaf26e1f0f254473b274be63232935f934216849ed`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed9e3a74eed9c26b4a0c5a03d899180bb06f8b34797a3415c87e1690ce1c75`  
		Last Modified: Mon, 24 Feb 2025 20:33:03 GMT  
		Size: 256.2 MB (256217160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c46bbe311d7920558ec96e56b8fb79e31f30c06cd67c6f6cd625d57ff6a1b`  
		Last Modified: Mon, 24 Feb 2025 20:32:56 GMT  
		Size: 195.6 KB (195643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91256832df959fe066f2f79d49b4962480ef477c1b57e6195d3d61887b83ef09`  
		Last Modified: Mon, 24 Feb 2025 20:32:56 GMT  
		Size: 821.3 KB (821339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8416a2131897be366c91034b925dea8f8d908835277a019bee74bd545e4bd39c`  
		Last Modified: Mon, 24 Feb 2025 21:28:55 GMT  
		Size: 7.4 MB (7449030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:0c8301346379f9df5a603f3d9003d4f666d670a85134883b1233213046a1cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23316006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0789c0a502d6522dca9be84f4b77db63f5bc17d943b126ce61241346f2f92a40`

```dockerfile
```

-	Layers:
	-	`sha256:3d133eb90ce78dd0d472a0b8a2cc94c478f0f92ffdd88b89b3048d2c6e764fa1`  
		Last Modified: Mon, 24 Feb 2025 21:28:56 GMT  
		Size: 23.3 MB (23304712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3281f25bb0c17dc1a52daf8b36372a03c3c06d713e3a2dc52016efaf1d0088`  
		Last Modified: Mon, 24 Feb 2025 21:28:55 GMT  
		Size: 11.3 KB (11294 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7cbdf76b3c28a688616184ed06ba67ba336a6b2b57adfe54f56f791dd4d1657e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.5 MB (536487142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebe423d29ac683cde7bf45cda73101c230daf654139ca434ce1cb5b11096c86`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Tue, 04 Feb 2025 16:20:53 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb08f2dfbcde333a583952948ebc4e632dcbb5e80617adcb1cf802d99c434d0`  
		Last Modified: Wed, 05 Feb 2025 00:17:42 GMT  
		Size: 175.3 MB (175281303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1c7fc4f032acfc6f2f58b2276bbade21e3e4f759928029421b8341ba7c4e13`  
		Last Modified: Mon, 24 Feb 2025 20:50:30 GMT  
		Size: 227.0 MB (226956573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f3d6708796dfe6a55be95ebcfa517085e5c39ef87e864bee231d2a04fd77ba`  
		Last Modified: Mon, 24 Feb 2025 20:50:24 GMT  
		Size: 195.7 KB (195656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825468f7f302770cf5576bbcf7402f2f3d34b2881c2d593e6ed6dd00e75939d`  
		Last Modified: Mon, 24 Feb 2025 20:50:24 GMT  
		Size: 821.4 KB (821353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171b2b6d7f167effbdec3623324c42f2479845bdab1fef45e34e8e0422acfde`  
		Last Modified: Mon, 24 Feb 2025 21:29:32 GMT  
		Size: 7.4 MB (7448973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:f38a70612902218a65b2b74c5b0d04a64744497b948439dd2eced585b8fbabb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23179460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1a3ab42560e288f9e6ed3c8aa8b4a976a5f85ec72a19a8a28c3393489d5d51`

```dockerfile
```

-	Layers:
	-	`sha256:e8a38cfa1df9f0b32ce82e5d74908bb715b84c75f4c6108f96d1327f7b33c955`  
		Last Modified: Mon, 24 Feb 2025 21:29:33 GMT  
		Size: 23.2 MB (23168075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe4aa18737b2dae3d9dee07b706aa6cf4183ba9073a3d219f9d32752337fec6`  
		Last Modified: Mon, 24 Feb 2025 21:29:32 GMT  
		Size: 11.4 KB (11385 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:38987dc9c87a9abde18fd49de22c9667cb8be6d74d35b1c164a300d914362761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.8 MB (596786496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396520d9bd94b0e7e943497a58ad44230960a78a3ff360978613cd49737ad29`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611c2b713640ce0f9156445b244c4da5e621183b56c0901d97a8b6d54ce10d7`  
		Last Modified: Wed, 05 Feb 2025 01:38:07 GMT  
		Size: 202.7 MB (202718404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382766d5ad3e0b6d615ed6fce50fdc3438df2977a076890ae2e8073bcbca295`  
		Last Modified: Mon, 24 Feb 2025 20:52:15 GMT  
		Size: 249.3 MB (249339800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb2ae11fef0b08f1e2427555e7e5d6d797f4a35fb5e9045bfabd55f1fcb5b3`  
		Last Modified: Mon, 24 Feb 2025 20:52:10 GMT  
		Size: 195.6 KB (195577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c24aa4d13a628a5121e2fe72a113471c207a3e89fbfa7296f50f37ad5b890dc`  
		Last Modified: Mon, 24 Feb 2025 20:52:10 GMT  
		Size: 821.2 KB (821241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dfd3a315c90225e8c43bf55c3311e92eb23a466b472a445baf5f1c6dbdf64c`  
		Last Modified: Mon, 24 Feb 2025 21:30:22 GMT  
		Size: 7.4 MB (7448988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:b8e481a2af0fe396904664845b8d93bcfbddebb448452a7bad5b2d9c28c5e2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43f692f0fd6b8a500e806b37c2a511c480c42c3c9e77282de862fbed1b1ca45`

```dockerfile
```

-	Layers:
	-	`sha256:226f6602393a39261506dc1ba1bccd9f2623551db6390b6ebb555a14a2bc478f`  
		Last Modified: Mon, 24 Feb 2025 21:30:22 GMT  
		Size: 23.4 MB (23392611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f8e2411dfc5bc2552d8b09071e416a2bd9453cc0f2190297ed7e15158fdadc`  
		Last Modified: Mon, 24 Feb 2025 21:30:21 GMT  
		Size: 11.4 KB (11422 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; 386

```console
$ docker pull elixir@sha256:935612fc540c952947549a47069614c1eff336d59b956ba7be0f78eaf650d9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (609009733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86306feed88c05d52a758378e9805acaeab897f1d295a8c75b4e6b89f7461341`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b865e8d5ffe7c25a75d04dfdef6fefef0004eb50794e81452e817ec779fc5e1`  
		Last Modified: Mon, 24 Feb 2025 20:33:34 GMT  
		Size: 249.7 MB (249705821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff338573f7a174ee405927159db097458f86b8da6ce22329670429e2604a8173`  
		Last Modified: Mon, 24 Feb 2025 20:33:28 GMT  
		Size: 195.6 KB (195615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822b1991d1e79b1306526052cfd5668c524693f57691b8c6634ea8b4e483bf37`  
		Last Modified: Mon, 24 Feb 2025 20:33:28 GMT  
		Size: 821.4 KB (821429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968bc7633dce5d842856716fc9579cdc10d9d667c89956acd02b2b655be97fb5`  
		Last Modified: Mon, 24 Feb 2025 21:29:34 GMT  
		Size: 7.4 MB (7448923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:028ef4e01f6a525487d97831cb8107f9d736388ea654b3e82aa77d2b2ba0ccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23284107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d555a64716273dac93c41cf7d39c0b418c976bfafcff700ea86bb4158ce17cb2`

```dockerfile
```

-	Layers:
	-	`sha256:a7f0b65ad14537ac061e7225eb5f24f12556321a0dbb6a2eee01daaa3339dc5b`  
		Last Modified: Mon, 24 Feb 2025 21:29:35 GMT  
		Size: 23.3 MB (23272855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c6cfab748f2c40d6993ddd37653a81a6b4b7a6677162b8f7be46f54c6e3248`  
		Last Modified: Mon, 24 Feb 2025 21:29:34 GMT  
		Size: 11.3 KB (11252 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; ppc64le

```console
$ docker pull elixir@sha256:f9d985270c5631057cfef3eba0c80872b6dee632d3bca615d622c27eefbd600b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623729169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0431c2599b5eb4baa638c3f2631a0b83a70bd941b29c9a63f71562e70864947c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 15:46:48 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556dba2526850ef13f84af87d0289a40f2451777be07098d04c55f33c7f76b83`  
		Last Modified: Tue, 04 Feb 2025 21:55:09 GMT  
		Size: 214.4 MB (214366038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec40f3e95e64c144799fed6f375b2a38a69e5f9e6f5a14c42f7470b6f799482`  
		Last Modified: Mon, 24 Feb 2025 20:50:55 GMT  
		Size: 253.0 MB (253023964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b1a546cb5d61c0484c84122e0779b192dfe1a2b239489ec42a175de79072d6`  
		Last Modified: Mon, 24 Feb 2025 20:50:47 GMT  
		Size: 195.7 KB (195653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146fde20a71ff75d574b8eca3545cd2ac56e4efaba98c6f93cde4c21c569ef21`  
		Last Modified: Mon, 24 Feb 2025 20:50:47 GMT  
		Size: 821.3 KB (821307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4aba85d4cadbfd98b5fe8b37bea9e9304ff54960a8ef6e10b3f25a8d48a899`  
		Last Modified: Mon, 24 Feb 2025 21:30:06 GMT  
		Size: 7.4 MB (7448943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:eb8f44ee9e5834ce1b7512c588f7af09d59d025070bbaa149f2af9aa9cccaceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23319644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800529b4bb63eae87f1ee6156e61fceb58e3ef45bb2d6c3a53dde63d75eafd30`

```dockerfile
```

-	Layers:
	-	`sha256:a653bc7380a453a4e22197c5fa713098a220c644d547b58fe6157c22f525b4d5`  
		Last Modified: Mon, 24 Feb 2025 21:30:06 GMT  
		Size: 23.3 MB (23308294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e16d5266f51c761db6601898cf29dd772d1365902424fc07979b43f07ec6410`  
		Last Modified: Mon, 24 Feb 2025 21:30:05 GMT  
		Size: 11.3 KB (11350 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; s390x

```console
$ docker pull elixir@sha256:86ba21cd5cb0ca28086fedbb4a1377a2391408b0b4ce29947c74dcbae8430e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564570351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76ad7886a322979788d1e61735f05a38ba43fe2e271b6f0d4d423b639c1a9e3`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV REBAR_VERSION=2.6.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2fea659b4f888b77ebf8dd52c956ff75ecf328eef9721ac60734250fbd5b0`  
		Last Modified: Mon, 24 Feb 2025 20:48:18 GMT  
		Size: 238.1 MB (238050509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fe05d1e26028b90c278477514c1dfed34f7e023d53bf88272f08cd9d2c7a7c`  
		Last Modified: Mon, 24 Feb 2025 20:48:14 GMT  
		Size: 195.6 KB (195640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5504d925707c567e0d1516cc969c8387181f8ee0014599bbc9bbe48facb5606b`  
		Last Modified: Mon, 24 Feb 2025 20:48:14 GMT  
		Size: 821.4 KB (821363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a4ced935fb40cd82917d152fce2ec88464acc06d9b49b8369a34aca9d1c10f`  
		Last Modified: Mon, 24 Feb 2025 21:28:53 GMT  
		Size: 7.4 MB (7448989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:52b5d123390feaefb4a5061b59f388c83c04b11ea695dd27fda0cc1d89add477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23137532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b5f6b44522b8f2f2367383294dc20a23ed3654dbef89c2e14ef429db33b141`

```dockerfile
```

-	Layers:
	-	`sha256:001a321ad0addb342d2fff6a9b27a76320f6af8c9fe5e9947c54398c6441e80a`  
		Last Modified: Mon, 24 Feb 2025 21:28:53 GMT  
		Size: 23.1 MB (23126239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15298d47614f8ef2ae270e500d937f34f9c2fb2c5e11ab93052b83506c3e1a0`  
		Last Modified: Mon, 24 Feb 2025 21:28:52 GMT  
		Size: 11.3 KB (11293 bytes)  
		MIME: application/vnd.in-toto+json
