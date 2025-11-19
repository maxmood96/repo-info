## `elixir:otp-26`

```console
$ docker pull elixir@sha256:7708052f64527c302e53e481e24dc66e9924ecf0d528a4bd3191615432ed9c2f
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

### `elixir:otp-26` - linux; amd64

```console
$ docker pull elixir@sha256:74459f3b384c4e7037d177a46d5a99f98e911f46fef45592441eb7d12ebc127d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622475703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9611da7fc5f1273ec765cd7ed529aaac3152692f1ccf3f5ddb6adac5458fa4f3`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:21:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:19:22 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 11:19:22 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 11:19:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:19:22 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 11:19:22 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 11:19:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 11:19:35 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 12:16:53 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 12:16:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 12:16:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1208d53eb0667932469017a5ef3960e5ed2aea9143d62b983abe2f8593eeb9a`  
		Last Modified: Tue, 18 Nov 2025 11:12:42 GMT  
		Size: 211.5 MB (211460976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cb8bc82dccf4272a9bb6fe4862d30f3427d7da8e1bd005a1d4a7bbbd9cd9ec`  
		Last Modified: Tue, 18 Nov 2025 12:16:20 GMT  
		Size: 265.3 MB (265325783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06839685031dda344c61afc2db4fe92bdf50065f40cc98b87a063575063ef5c`  
		Last Modified: Tue, 18 Nov 2025 11:20:40 GMT  
		Size: 194.9 KB (194909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af31382a7b3951ea1536e2552755214e16216cc766d7d67ce398262366c53b87`  
		Last Modified: Tue, 18 Nov 2025 11:20:40 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cb82ee46aefd76d3df20f84ecbc4539d083b57ad63110fee6caddb13310ab8`  
		Last Modified: Tue, 18 Nov 2025 12:17:53 GMT  
		Size: 7.8 MB (7767972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:8f66f058fedcb6dec2e1bbd9a778333317d584b12aa268d04052255175aa7139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23123784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813258831eb6244e5081bb32d1769b26f9799f9fdb8416906f6de56f1ab4b56f`

```dockerfile
```

-	Layers:
	-	`sha256:7f192ad2312d1acc210bebe892d57635a2e0bf834b9b48b6b4a9c3534d25588a`  
		Last Modified: Tue, 18 Nov 2025 16:48:49 GMT  
		Size: 23.1 MB (23113406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd00f4ed02c0041b3ecec8207f199566408ec95019f76facbca97d2f7444217`  
		Last Modified: Tue, 18 Nov 2025 16:48:50 GMT  
		Size: 10.4 KB (10378 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm variant v7

```console
$ docker pull elixir@sha256:4c9fbb231aafc7d1872e3393837071d9f6e304e285cb014d3a494c8a21bea770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.8 MB (545750323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b45ebc4dc108d99ccf033f0a54c7ca573a6f6f25b245a1b165a44ea61c998`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:41:02 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:41:02 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 07:41:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:41:02 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:41:02 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:41:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:41:29 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 08:48:21 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 08:48:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 08:48:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad0f2d457569ebe1e8bb868d038539ac612c99d1c10b8c279ff1a9fd7fa24be`  
		Last Modified: Tue, 18 Nov 2025 07:34:33 GMT  
		Size: 175.4 MB (175370481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495c68ca6934e661159cd76fd46a90c568546e73d8d6b3bf5ef67c2cac2a2f2`  
		Last Modified: Tue, 18 Nov 2025 08:47:40 GMT  
		Size: 235.8 MB (235814317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f1160dee048fe9356cd2b07558bf1d7a28c331e9a9d0fada6eca7153ff8bc`  
		Last Modified: Tue, 18 Nov 2025 07:42:35 GMT  
		Size: 195.0 KB (194959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d5c72720b349f17973f4afb33783e3aa529f250659a6f0a4d1321ce773185b`  
		Last Modified: Tue, 18 Nov 2025 07:42:35 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa8bc9cb7e746077e64287d3a657ccde4dc02ce81a958b77fa873bff57236d9`  
		Last Modified: Tue, 18 Nov 2025 08:49:07 GMT  
		Size: 7.8 MB (7767926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:97e24f81b4edd1e452443d1ce55012b61b22742b1bcc14f457277317d05226be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22936792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb618fea65a1b1a3ac625c3c2aeda2064aa39fdfda09b4c78e0fb2847f5652f`

```dockerfile
```

-	Layers:
	-	`sha256:0c6f219218cd0633c8fec02f6307d076d30b7cc48d6418c4d0633a728486eecf`  
		Last Modified: Tue, 18 Nov 2025 10:50:26 GMT  
		Size: 22.9 MB (22926342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c350f1e1e2aa742c1783491f80c9dbbd08dd08645bba87f69c1cc0df03d428`  
		Last Modified: Tue, 18 Nov 2025 10:50:27 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:819357eec3b5cb0806a024e748811ad2e142945bd97c26749db609a2451b2c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606392248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2624d8461e13bacc994626e0d8dbe9ccc2e0cc2db532a6af470aea8381e3b4d5`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:24:55 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:24:55 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 07:24:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:24:55 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:24:55 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:24:58 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:25:09 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 08:24:51 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 08:24:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 08:24:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea7607dced22dd12cfb6fe96ff19187f5ee918dd3d48379e2d2fd756af4818b`  
		Last Modified: Tue, 18 Nov 2025 07:15:14 GMT  
		Size: 203.0 MB (202980192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76588d4ae988029ac0ef2f53910d2cee40d7ff5e0cd0139b21a2f2ef828914f`  
		Last Modified: Tue, 18 Nov 2025 08:24:07 GMT  
		Size: 258.3 MB (258300557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b5ec1a9bfff8b1f130166c0a3ede3d77906dcaa0929fcef7c52c4b68a2e31a`  
		Last Modified: Tue, 18 Nov 2025 07:26:11 GMT  
		Size: 194.9 KB (194947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2788ca95ae6590865d37f63feefb5fdf2098f67e218c8fc41f09cc08118e1`  
		Last Modified: Tue, 18 Nov 2025 07:26:12 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91fdd94a42bfe2b92d0fb2fae5f884171c00d1ef203a3e63577b04d34c9fa9b`  
		Last Modified: Tue, 18 Nov 2025 08:25:32 GMT  
		Size: 7.8 MB (7767988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:06c758ce9d9332bd6177f5382949a4e6f79a3f79a1cadc7fc944b7ebbc7065c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23163311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3816b599cd893deecc20b2206288cd18778edff08f1fe57bcfa361c8d788472c`

```dockerfile
```

-	Layers:
	-	`sha256:2544c6675f7e818d111b8188c17c7944e9d20cbcc449b8410a7fc6f8efc6f765`  
		Last Modified: Tue, 18 Nov 2025 10:50:48 GMT  
		Size: 23.2 MB (23152841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895ab244b7acaed0e869b65498ad77ae02dbb74276652e884b899cddf1e6c568`  
		Last Modified: Tue, 18 Nov 2025 10:50:49 GMT  
		Size: 10.5 KB (10470 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; 386

```console
$ docker pull elixir@sha256:58a7a19ea227bac6e08357f14f26d3a79f2869136b062fa36554a79a2bfc1ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.3 MB (616301948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94806b6704dca1e781f498a73c6bd981fe01581d0a79ddfa88801aeb474d6ef9`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:26:21 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 06:26:21 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 06:26:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:26:21 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 06:26:21 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 06:26:24 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 06:26:44 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 07:21:09 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 07:21:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 07:21:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c185d92b9a40ab45d15fa519a2c049e78267565301d35e186267bc212115f`  
		Last Modified: Tue, 18 Nov 2025 06:19:22 GMT  
		Size: 210.4 MB (210389386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85448bec527dea679ad2da0a9e1b1276deb2a74597006d91f21f6af6525838`  
		Last Modified: Tue, 18 Nov 2025 07:19:53 GMT  
		Size: 256.6 MB (256565053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9114f5ec20089c26068741871371f8bc9f2e2d53e9fa8c7e00cd3e5b3ae07b`  
		Last Modified: Tue, 18 Nov 2025 06:27:46 GMT  
		Size: 195.0 KB (194974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0edc26e291074acdd038f203f615d9e3f6f49f4ec251e9d401296e783192da5`  
		Last Modified: Tue, 18 Nov 2025 06:27:46 GMT  
		Size: 819.7 KB (819694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad0237a0e6c0c0b000ebbff8c4a7e42b4cc26ce8172fd64b25d60b0475ca17e`  
		Last Modified: Tue, 18 Nov 2025 07:21:50 GMT  
		Size: 7.8 MB (7767690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:c0920ab7380562cfcd031fcaf623ad10780e550921a016a056ebb2d4d29a6cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91c63f50bc9bceed8114e2e6cca0c5a871f3f08456a8213bcd85d2814d3886b`

```dockerfile
```

-	Layers:
	-	`sha256:d760a65dcc4ec90075aeecad8dc8904e20e9bff74b06a9a21ace150311ed3845`  
		Last Modified: Tue, 18 Nov 2025 10:51:10 GMT  
		Size: 23.1 MB (23081107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d4c57640efbe3d0d880831b8e18d8b57bd474d3ac9470cad3db28f5aa996e0`  
		Last Modified: Tue, 18 Nov 2025 10:51:11 GMT  
		Size: 10.4 KB (10351 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; ppc64le

```console
$ docker pull elixir@sha256:feb4ecd41ccd4558f12ecf2dda48da0a8454163b7bcc7a4a3dd2144ea7424f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 MB (630925312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece762e5cd6d485d0a84d7d2dbc162dcdb4e770c117e1bcc697e2438974e6b05`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 09:28:51 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 09:28:51 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 09:28:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 09:28:51 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 09:28:51 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 09:28:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 09:29:48 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 19 Nov 2025 01:26:33 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Wed, 19 Nov 2025 01:26:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 19 Nov 2025 01:26:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055d1d2e62969664b2197803b2dd13eb0c52b160f256835c7b8bb1eca8dc83d`  
		Last Modified: Tue, 18 Nov 2025 11:54:22 GMT  
		Size: 214.5 MB (214498281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861e1c549b09c4722cd0f653f87898573d56d33d2fe1c1b278778e72c9550f4`  
		Last Modified: Tue, 18 Nov 2025 11:54:41 GMT  
		Size: 259.8 MB (259799799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43289fb2d75728e4ed31f1d40d6b1da38be64629d0887372a8dbc7e9800e0f51`  
		Last Modified: Tue, 18 Nov 2025 09:32:25 GMT  
		Size: 195.0 KB (194960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3eb9d2bcc57e0d374a55cfd53ae7cae8a58f670c2d7da70199816ff1bd6d98`  
		Last Modified: Tue, 18 Nov 2025 09:32:25 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11facbf7d05ce9a6549178664df872c871caf07935c66e16bc667ca9d86f4efc`  
		Last Modified: Wed, 19 Nov 2025 01:28:50 GMT  
		Size: 7.8 MB (7767977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:d7c6f98054c1ec14a4f7a823eea91cb6bcec4f01044dab6909a7e5df26db823a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23079221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d463ed530a8ba11eb28aa28c9216d0232c9879f92bba5f3bf4737475555786`

```dockerfile
```

-	Layers:
	-	`sha256:0a817cdd8db0a36c229631804f3530075f846deae261f15b4a2b878e7b79652c`  
		Last Modified: Wed, 19 Nov 2025 04:47:17 GMT  
		Size: 23.1 MB (23068805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25215392a0641778bf387077a1eb1cbea73dc594b4c6c377beb8e04ed0e9aff`  
		Last Modified: Wed, 19 Nov 2025 04:47:18 GMT  
		Size: 10.4 KB (10416 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; s390x

```console
$ docker pull elixir@sha256:57a3225c18c9ccec07f60dea37a2e7c746841e7caf39e091e05abccd350f771d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.3 MB (584344446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51886c82c4e821470cbfec6c9db906f8d9bbfe49e992019920b98073faeda91`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:29:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:35:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 08:35:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 08:35:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:35:53 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 08:35:53 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 08:36:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 08:36:46 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 15:59:20 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 15:59:20 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 15:59:20 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a3c31d224355129a49f91ee32618f26bf3cb019a25f07a3795c22816b92b87`  
		Last Modified: Tue, 18 Nov 2025 08:13:31 GMT  
		Size: 183.5 MB (183498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3772eed0141f10096f019d5a3a9658fcb45218a4164589358dcea902c7abf9`  
		Last Modified: Tue, 18 Nov 2025 12:02:19 GMT  
		Size: 257.4 MB (257397388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0540ca4a7f0777cb58f89b92b5b555074538897554fc534ae612f027f684c4c0`  
		Last Modified: Tue, 18 Nov 2025 08:39:51 GMT  
		Size: 194.9 KB (194945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09beae4145cc24ffdc8a4d91c5fb6f00d9f2957284734a0f3f81710f66320750`  
		Last Modified: Tue, 18 Nov 2025 08:39:51 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d4fdf64d5c0d53739d68ee39c08e4b695719943d54aaa0a032970c0424053a`  
		Last Modified: Tue, 18 Nov 2025 16:00:17 GMT  
		Size: 7.8 MB (7767952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:e369fe5c1e1ad1f44194832733ea00af868c5fa881bdc1328500a52ede8ded7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22891260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ba57315f74ceaa19c2eb1ad666091aca46fa24512a9f599d515c5ccb330dee`

```dockerfile
```

-	Layers:
	-	`sha256:2dbf204472c2b9ab23f520c5b4b23ef66232bbd533450e602f3c4da4c9fd2a76`  
		Last Modified: Tue, 18 Nov 2025 16:52:31 GMT  
		Size: 22.9 MB (22880882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90bd0134ac4d7977f387851781c66eecc4e128d44322a4fe3d92f538b4152421`  
		Last Modified: Tue, 18 Nov 2025 16:52:33 GMT  
		Size: 10.4 KB (10378 bytes)  
		MIME: application/vnd.in-toto+json
