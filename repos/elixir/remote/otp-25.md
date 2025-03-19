## `elixir:otp-25`

```console
$ docker pull elixir@sha256:07218150c0868d41f9bb28ad4aefbfa670b5bc61932d0e9b2be7b3020283a50e
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

### `elixir:otp-25` - linux; amd64

```console
$ docker pull elixir@sha256:7af18e4882d83d9680f7a1f380cfb8f56c6ef0c70233947f72e15bc0c48fb3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579119346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e25729bd6abc8d85f5a10706d7856a0ad35ee12229b9b50ace320f2527b86fb`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sat, 04 Jan 2025 18:55:45 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6dd983ff133914060200e7c5e808fcdd44c72679c04f55059151aa2050dc87`  
		Last Modified: Tue, 18 Mar 2025 01:13:41 GMT  
		Size: 197.1 MB (197103663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b101eea637e7cebf020c4b8211b10caf16bd71cabd2e58f99b964004acd6fa98`  
		Last Modified: Tue, 18 Mar 2025 03:28:05 GMT  
		Size: 249.4 MB (249413574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05c4aaa1bd07b3612929ec5dcfa508d50234ea38337d918feffd6448d1d31e`  
		Last Modified: Tue, 18 Mar 2025 03:28:01 GMT  
		Size: 198.5 KB (198548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e631ff3c2d638f96ab39e9a53129f33c747eba41bbd526b38203e39917ae8`  
		Last Modified: Tue, 18 Mar 2025 03:28:01 GMT  
		Size: 817.3 KB (817338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8d632e970709c684880d5493894a1186fa06f9804b71f9e1eb60a9c0c0e9f`  
		Last Modified: Tue, 18 Mar 2025 04:12:06 GMT  
		Size: 7.5 MB (7534273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:4d32c45bff15d247936b7d49c6c389afe56e3502b543bf8da5b0d551fe3dc32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22877748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c206591da46320062c5ba15d6a18147d432188ce4aca42aaf5d367f90529a3d`

```dockerfile
```

-	Layers:
	-	`sha256:f1df5605f41b7156101621e6faf55c07fe61d3732a2b754fda6a2f442de4889b`  
		Last Modified: Tue, 18 Mar 2025 04:12:06 GMT  
		Size: 22.9 MB (22867327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38764a7aed30a72df649da3b4d157f72af151b0228ee0a9f99d302c0d3dba30c`  
		Last Modified: Tue, 18 Mar 2025 04:12:06 GMT  
		Size: 10.4 KB (10421 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6fd28a51a64da24e44a2534353698e51cb6f6bf71df1e8d84d86e4717a8aac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511420080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f68f75e0773104d42f2952d8425ead0ac4058c12d387d39cda184f39df2ecf`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sat, 04 Jan 2025 18:55:45 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd256a1e0237bda283c02f2cc3e8acb56a886150f50376ee21fb88db90889b8`  
		Last Modified: Tue, 25 Feb 2025 18:18:14 GMT  
		Size: 221.0 MB (221001184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d9364504f43e2c5f5ac1946af4c222d036ae50e0d625850d6564066b55a74`  
		Last Modified: Tue, 25 Feb 2025 18:18:08 GMT  
		Size: 198.6 KB (198552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cef9e4c2b254c95b1f7b8581323546690a7d7403e8ba4cc83744ff73490cbf`  
		Last Modified: Tue, 25 Feb 2025 18:18:09 GMT  
		Size: 817.3 KB (817339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd1d6f9c40b1778337c3b21b2484a1e9ab98540f1b394053c99a09c0a730cf`  
		Last Modified: Mon, 17 Mar 2025 17:37:40 GMT  
		Size: 7.5 MB (7534297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:1be27c07a51b8b0a082643bfb5bae61a5f725e0533d50d78eb905823a0e518f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22686268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1387b7e9a7de801405658cfb2b7d628baeba7a0d4438163b7af79be785254`

```dockerfile
```

-	Layers:
	-	`sha256:bf57029ff4237a3120c2bb74b7a81b733ee6b2f618437937914d35729d57a066`  
		Last Modified: Mon, 17 Mar 2025 17:37:40 GMT  
		Size: 22.7 MB (22675779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d44017ba356a6bb2967163b21e17522e466a4fd82b4ebd8ea66bf5387ad3f72`  
		Last Modified: Mon, 17 Mar 2025 17:37:39 GMT  
		Size: 10.5 KB (10489 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:e58c6c7398ae5423e4eacf4931f655c321314d2778a5f34c873e8abdf4d1595a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560356192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dedadd97e5f125f1ae56b62a6c7e325767918fe961e1de778f689ef3ed8b36`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sat, 04 Jan 2025 18:55:45 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f85dad99c5aa182c7db2c6ab75b86d81115f59af754663dbbf71d747eb008e`  
		Last Modified: Tue, 18 Mar 2025 15:56:11 GMT  
		Size: 239.1 MB (239137247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112f6989d3a51113af65d9529e0b43429a35317c58adae05b91caa4cb0a6c7a`  
		Last Modified: Tue, 18 Mar 2025 15:56:02 GMT  
		Size: 198.5 KB (198549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2c0d90bb6b9eeddca2938636f533e3fa1426c57aefc77ac853a88ad6ec59f2`  
		Last Modified: Tue, 18 Mar 2025 15:56:02 GMT  
		Size: 817.3 KB (817338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d28849502f3c630178ba17b99c80535f39dc4b8574bcc1a186d01350c1dc5`  
		Last Modified: Wed, 19 Mar 2025 01:49:14 GMT  
		Size: 7.5 MB (7534445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:ab7ac1b22652e03ec97406e3ca66fdda130adc92d147c63bcf0dacdc185baedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22887558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338457fec40e9c03afbb515058ba8f67dc3bab8a6e8ed2934d647d06609c0a5c`

```dockerfile
```

-	Layers:
	-	`sha256:a80f56ef3a6701e734dbcd199cfd93d3a21dfc9a1a534f29e0c4799a7bf94ea7`  
		Last Modified: Wed, 19 Mar 2025 01:49:14 GMT  
		Size: 22.9 MB (22877045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e44e0f96f047c69828b38d65bdc97ee290c76255bf5f54a27dee84cda454b5c`  
		Last Modified: Wed, 19 Mar 2025 01:49:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; 386

```console
$ docker pull elixir@sha256:82d89526634b6affaa8bb9d9b2a99f71330516161fd08cb509dc55d629a8102d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576053076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9674a68f07bb7559663687e1c362c64113bc7ca257bc55e59d67bafab19230`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sat, 04 Jan 2025 18:55:45 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059088008dfcc57a13c8c2f23b9fe0cb13924afc78deaacdd89c0fbda40ff083`  
		Last Modified: Tue, 18 Mar 2025 03:28:02 GMT  
		Size: 240.7 MB (240724186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32142805de0d2d1a1947a24b9acdb90074c833af12fa22b348c372e18cdeb595`  
		Last Modified: Tue, 18 Mar 2025 03:27:57 GMT  
		Size: 198.6 KB (198560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d31a4e4aaf3c767780dd8283692a17e615f18474cf9e00f7112f7adede73d73`  
		Last Modified: Tue, 18 Mar 2025 03:27:57 GMT  
		Size: 817.3 KB (817340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e08b2873d783f5a6b4624c2ab6259f0b8771d84307854b0cbb9d248c03c690`  
		Last Modified: Tue, 18 Mar 2025 04:12:13 GMT  
		Size: 7.5 MB (7534156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:6809bcea799557afa91e84e1c9776ae0b012efbc25118d2520364a2ae8304b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22865309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9e234031ffd2bd3fef764298632591da211d44d1a2a0d8dae5870fdc969190`

```dockerfile
```

-	Layers:
	-	`sha256:414a5d7b5c389729e5a5ba1e9b146cc8cd764c811df50425884854c0addb0977`  
		Last Modified: Tue, 18 Mar 2025 04:12:13 GMT  
		Size: 22.9 MB (22854915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:734fafbd18f541d7cd9c1ff93b63f14a1d1cb4d7a85081fdc8e9cae56b395ee8`  
		Last Modified: Tue, 18 Mar 2025 04:12:12 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.in-toto+json
