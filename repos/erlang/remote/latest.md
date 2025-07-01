## `erlang:latest`

```console
$ docker pull erlang@sha256:b08417bc2002470ac618c7690ca2bba7c74affc7990a5e304f70e589bc37d91e
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
$ docker pull erlang@sha256:6c8c6014e604f5f8431120276353eb56f516222732359fead26bba335a8639ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.6 MB (623574571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e2f7df870e084cf8b98e9386ab15d3f83beee02f1aacaffdeb3a79409fd175`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8873ad0f8f9e722ca598220a46898260b7a9a3369c384fae2a407ad8dd2b9`  
		Last Modified: Tue, 01 Jul 2025 06:12:32 GMT  
		Size: 274.3 MB (274277449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc76524bc99ddbc95b9aaa278fb776c681e2398e6e487eb314b9f54b282df18`  
		Last Modified: Tue, 01 Jul 2025 05:16:03 GMT  
		Size: 191.4 KB (191375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c095e40f492adbde50bd2bb230790fb79e4a2b22f4b32e55f76e38e026b1671`  
		Last Modified: Tue, 01 Jul 2025 05:16:04 GMT  
		Size: 817.4 KB (817392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:13e11a430b01f0dafc82eeae711ea6876b557b47dd42543cb03d0164b0070fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23951135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550bf5ad1a8cf2f11fcaa160e81b18ddeb2b94ae9592ad5c8ac49f0e290a9163`

```dockerfile
```

-	Layers:
	-	`sha256:c6eb60bf9d8d949526c18e79543aef0a419bffea05c071a27339f03def40a189`  
		Last Modified: Tue, 01 Jul 2025 07:48:27 GMT  
		Size: 23.9 MB (23931857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79b90f3512e965d2d57bde0e72de0be5a027180c8edc3125cd6632d22bbb949`  
		Last Modified: Tue, 01 Jul 2025 07:48:27 GMT  
		Size: 19.3 KB (19278 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:9cc13afe002abf30ec24ea398bc709c281ab9c0791ffa83e6e712a200301dd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563920452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2047a074fad915a5cce17a8b9df17bd2729dd9afd0602e3d6de7541bf8f21a35`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973a0421a43933f783f2da8c4e6210bbcb63636694bdb47f5939d46f0cd8e74`  
		Last Modified: Wed, 11 Jun 2025 03:12:54 GMT  
		Size: 22.7 MB (22694196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd263284be736a4785fb0c489cf441580757a05d8cb52c26f07ba8f071d621a`  
		Last Modified: Wed, 11 Jun 2025 12:34:20 GMT  
		Size: 62.0 MB (61997905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30652400d271bd60054de74fdb5974778115084d744807cfc209f10e782a415`  
		Last Modified: Wed, 11 Jun 2025 12:34:34 GMT  
		Size: 184.6 MB (184640116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb62ad8fa055fe8950b2dd072955e0d51ca539508d10faed8576982ed8cc875`  
		Last Modified: Tue, 17 Jun 2025 20:04:28 GMT  
		Size: 247.6 MB (247552882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba145d2b608a25c8c73a888e1b659d1db244d94c1f55af5eba7833bf894a893`  
		Last Modified: Tue, 17 Jun 2025 17:09:45 GMT  
		Size: 191.4 KB (191374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057d4e2cc9cc0ceedc1e02db605daf494671688e7f20901f4892443ef7c2187`  
		Last Modified: Tue, 17 Jun 2025 17:09:45 GMT  
		Size: 817.4 KB (817392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:c919f0d54da199fff5d396153fb07bfbdd0738ea36e80b922e400086114f23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23745943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a1dbfee2ae7ab57015b61dc26e45909e99dd00a7109be6d1283fdac7f095c1`

```dockerfile
```

-	Layers:
	-	`sha256:5e2f6c5939bb0dcef48c984a7047eae95b9077495fc6ef02dad04199389b530b`  
		Last Modified: Tue, 17 Jun 2025 19:49:58 GMT  
		Size: 23.7 MB (23726554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6778dc19d2a2d1955f207fa0d6ec955c7b857c3ca0536f0b1a43bb499013c3`  
		Last Modified: Tue, 17 Jun 2025 19:49:59 GMT  
		Size: 19.4 KB (19389 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:76d70990d95fbc6eb95c4239fdbdf9acb91c61ad9caaa1f248283e824ba1a9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.7 MB (545748562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eabf1a38970cce998dccae67e0a39a50966ac320a0681a5603f478358f85dce`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508e554438a911e5e20c736c0b2bb41ed19d27604ec6ff56f199e18653a0d8e6`  
		Last Modified: Tue, 17 Jun 2025 20:05:30 GMT  
		Size: 243.7 MB (243654469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781d85fd3d5f3f6943ca315522127e024be8f38b5ed0c62f525de2b3104645f`  
		Last Modified: Tue, 17 Jun 2025 17:09:17 GMT  
		Size: 191.3 KB (191315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa2e429b4db6046444d27774672eb06b4144423d00892f0037aa968928d0ba2`  
		Last Modified: Tue, 17 Jun 2025 17:09:18 GMT  
		Size: 817.4 KB (817392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:c5af64c9bf818020275867a801e0492a527c8c52aebda8c970834b0cf2659369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23762889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8ca7541922ea6d06c76ed8a3b3e9ea9824653ee4f397282686f424af2375f3`

```dockerfile
```

-	Layers:
	-	`sha256:ff4c01f6e31988a0d003549d6b1c6c906ae111cc6b34f00cbb728c775d2e2d3c`  
		Last Modified: Tue, 17 Jun 2025 19:50:15 GMT  
		Size: 23.7 MB (23743501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b036af2a610a6f53f36c9c97e8dab618f073f2f637c5689a4cf10ccaa3c67a8f`  
		Last Modified: Tue, 17 Jun 2025 19:50:16 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:6bc455821be83ebfbcf58d1482f4763bb42d98b38395d0b4b3a435106b535045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.8 MB (606834918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdfb4549d1635b5e191ea587f1b9e25746cb9d6657e3e062f2a62b64db9ab1e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa6d9594972c269425ebab8242cc2fb238574b52b8cc21966a97a1524b4635b`  
		Last Modified: Tue, 17 Jun 2025 20:06:11 GMT  
		Size: 266.8 MB (266807328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a0b1f02185f1236f9e71df4e0537ec6353dbf20fc9574e367aac7414a7d27b`  
		Last Modified: Tue, 17 Jun 2025 17:07:52 GMT  
		Size: 191.4 KB (191385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eb84c2e39e071c10e42e12310a62fa66907d2c6e9c6812b0bb355aa1f094b7`  
		Last Modified: Tue, 17 Jun 2025 17:07:54 GMT  
		Size: 817.4 KB (817393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:88cd15eec7ae7ce2fd1e71dc469884c393f089b8b9fe7efe12934a3ed3d8bee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23989353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70191f547df0bc83c007f631bb6a3bfca937559f92e05a8232229eed3e26ec1`

```dockerfile
```

-	Layers:
	-	`sha256:0230780e2c992e50888cf85acc832dfe6912eaf73e08fed6b44b80e4177665eb`  
		Last Modified: Tue, 17 Jun 2025 19:50:32 GMT  
		Size: 24.0 MB (23969928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba17c5a217d22520cf2e0b78fb48c1f5032662b3b088b8331aac024f817525f2`  
		Last Modified: Tue, 17 Jun 2025 19:50:33 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:03c0390974cc3681a83373c94b4041961c9ff506b7d03b29b570adbca578da41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e48534629002f7fd3e39a646448cfbf3ad15287541d924b731b920a9b22aad`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8a499cb0acd512f161b293636470b74082aa8d10b6486e444528726ab14a94`  
		Last Modified: Tue, 01 Jul 2025 06:12:08 GMT  
		Size: 272.3 MB (272293948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd074a52ee48ba5cf3520d7d5280ec276296746b79970c989c04fe2c3d1dc83e`  
		Last Modified: Tue, 01 Jul 2025 05:16:38 GMT  
		Size: 191.4 KB (191358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254a6e922712d08350bc979789f58769cccc1c1ca08d2b1245b99d3f0653c71e`  
		Last Modified: Tue, 01 Jul 2025 05:16:38 GMT  
		Size: 817.4 KB (817392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:0d3cd483a3505cdbff6d1b2a7af66ab4a7c78a1ab00ab2e446aad80c4171d62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23918709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595d6156a6aae1daddc9aaa675abd99aeaad70665989b9ab3fefdb8d497ca894`

```dockerfile
```

-	Layers:
	-	`sha256:55920f2c3bc6777e6de1306daa95239c42221f19e3c707be586961d73cf27cab`  
		Last Modified: Tue, 01 Jul 2025 07:49:51 GMT  
		Size: 23.9 MB (23899471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a824f27466efd2f9d80ea0e9908afcb5daaf61488030420564c7685bacfdff`  
		Last Modified: Tue, 01 Jul 2025 07:49:52 GMT  
		Size: 19.2 KB (19238 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:bf69783733e5f51123b8f267bdf8832f00b500836451006844ad9c170d001104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579975459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc15a01b526ea8ed2b6b1015bcbeae0ff14a3eaf6edc1d83616649cf3c41c42a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ae38c8170365f95ffee9bc84890468511106f230c4a60b226c468bf158517`  
		Last Modified: Thu, 12 Jun 2025 07:21:40 GMT  
		Size: 190.0 MB (189963407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70d7236e1902cc7019b88c3a5ea70b009d4b77cd2708780083ccb2332b2f03`  
		Last Modified: Tue, 17 Jun 2025 19:52:55 GMT  
		Size: 253.3 MB (253320367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959463909bc6cf56748064e192dd0ce0ed0ebbce089980052a82048da3da2a1`  
		Last Modified: Tue, 17 Jun 2025 17:24:18 GMT  
		Size: 191.4 KB (191388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2690729661145074083a57d60686907bf904255173df93bbb73cc5ec4b611bf`  
		Last Modified: Tue, 17 Jun 2025 17:24:19 GMT  
		Size: 817.4 KB (817393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:5da2551bf474550d39cc3715ebcbd70e784f1168d637070e79c5e9620140e506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f59ec2ccba6e1ab6ac6ddc6a41f3175d84a88136644b97aadb3ed8ceb43a6e`

```dockerfile
```

-	Layers:
	-	`sha256:74299c1c1156018dad581063068c6fe3973b423d10c7567b54088a095cf97122`  
		Last Modified: Tue, 17 Jun 2025 19:51:05 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:df35194ed7e514e611b8bf3fa2d4a011bc57046313b1b509ae39729e1a987966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 MB (631538775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fa8005f34dd6d1383363ceff7eb1d2789246e70162992c4dcf3ce3c564ea69`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505c6c748b1d0568e4e4d32972deee29a5b75abfa52c5517e9b010a34621cec5`  
		Last Modified: Tue, 17 Jun 2025 20:07:19 GMT  
		Size: 268.3 MB (268274302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370bb1ea9b4bc9e117f5fb4418c05ccf4101fd6907481319b80e2ec9f8d208aa`  
		Last Modified: Tue, 17 Jun 2025 17:10:17 GMT  
		Size: 191.4 KB (191381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107de6e67df105aad3b9ceb040eab38d64477ac54e08c8bcf871a6624081ebb2`  
		Last Modified: Tue, 17 Jun 2025 17:10:17 GMT  
		Size: 817.4 KB (817393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:4a959ba516c1499ed4c502a0968ceaa85a0cbb79e39acddb671092062d75857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23905447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be15a15cb7962d4430f8225c4d1e0256bf72f26eed512349a5e6387a8f84818`

```dockerfile
```

-	Layers:
	-	`sha256:cfea9864a51d26f1b82c6994084bf02241f71f66b6fcece222fe605aa3c42fea`  
		Last Modified: Tue, 17 Jun 2025 19:51:12 GMT  
		Size: 23.9 MB (23886114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8ff8ffcc8c268e2cd6870f9b3e76e146bc2aa0e9ed9c2df4988abb3aa4fa14`  
		Last Modified: Tue, 17 Jun 2025 19:51:13 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:60e0ee84008261e0dd2cc9eedd1518c3606c46b9aa6db27f48461b5eff1f2a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584404442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6758a6c1844ec52fbae6f7922fa8d7171f594614e4218402eff968ba7e5154`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Tue, 17 Jun 2025 14:21:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c056714c54676358218cd75dc0c5d3298e3c0e7e53c127fdefd363c4380d95`  
		Last Modified: Wed, 11 Jun 2025 12:03:11 GMT  
		Size: 63.5 MB (63498247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0295075e9ee106928dd37c7a8508f7a8bfe0eb1745d49bd1918fc475143a12`  
		Last Modified: Wed, 11 Jun 2025 14:17:17 GMT  
		Size: 183.4 MB (183416974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79b621d042a7c385787725a04578ffbb811d0c34d5fc0a1f96089dae6f97ba2`  
		Last Modified: Tue, 17 Jun 2025 20:08:14 GMT  
		Size: 265.3 MB (265316011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897c8066c7d68731b19d3e20a869ada9c507cff4e6a58940a7894a738c8e77a4`  
		Last Modified: Tue, 17 Jun 2025 17:08:47 GMT  
		Size: 191.4 KB (191407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996497bd052a68e5a3364c60b37ad070e3642a137f880d6af075bd4de001b72f`  
		Last Modified: Tue, 17 Jun 2025 17:08:47 GMT  
		Size: 817.4 KB (817393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:4144f855790f1c5d2d3e03f5c201ccd295cafb01a8972bfad08b11785897818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23717144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25675ba470d200a254a978a794e017da2c361e363962b9d780add355e62e9bea`

```dockerfile
```

-	Layers:
	-	`sha256:0031a6178544dcf04be480f160448df4224996363b5605d41b9367e89c3e1e60`  
		Last Modified: Tue, 17 Jun 2025 19:51:29 GMT  
		Size: 23.7 MB (23697865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0a9c4d3cb802af8650e6c3946ee69fe245ad495c9c280021b6169330c0e2c7`  
		Last Modified: Tue, 17 Jun 2025 19:51:30 GMT  
		Size: 19.3 KB (19279 bytes)  
		MIME: application/vnd.in-toto+json
