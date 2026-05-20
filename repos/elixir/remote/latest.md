## `elixir:latest`

```console
$ docker pull elixir@sha256:d1c823b7f1ec6abad7fd1e29b1ed2e7befba9247ba7086bf8f39f01e3c504ab3
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
$ docker pull elixir@sha256:e365bb1d6507e70073a1ac540ba2163662326d527fcb2557e7ec1b55e34fdc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681663941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b702e148ed3062faf2bc88800690df42f9af0b5bca34437401fa13697725e720`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:16:11 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 02:16:11 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 02:16:11 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:16:11 GMT
CMD ["erl"]
# Wed, 20 May 2026 02:16:11 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 02:16:13 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 02:16:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 03:22:48 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 03:22:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 03:22:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d44b254dab2063c4226fc8a0849d5527402d24d3bea80d644a1e4ac3a47e5`  
		Last Modified: Wed, 20 May 2026 01:16:36 GMT  
		Size: 236.2 MB (236176097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7161c6ec00e696d7bfda64157e524ed11a4eaca6adf1b7d4dfdb4517b253278`  
		Last Modified: Wed, 20 May 2026 02:17:23 GMT  
		Size: 294.0 MB (293987363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e39420ddb6294c2f77417f6643ccc3a24f179aabe60a46d045c7bbcde80271`  
		Last Modified: Wed, 20 May 2026 02:17:18 GMT  
		Size: 191.5 KB (191460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f807c8694787e350a9c5507c48092d0f01b1d41c752b4975f7f933bf0f3db3ba`  
		Last Modified: Wed, 20 May 2026 02:17:17 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90332dd64ec616cd71bad510848a4a460e4be26b649c712a1568195f20fb86f6`  
		Last Modified: Wed, 20 May 2026 03:23:16 GMT  
		Size: 7.8 MB (7766904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:e2bee784015942addf4954812216c91602e5bbc3bedcf44eefb0b5ffb18ce0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22052257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49d5ec585af7adca73d7d39eb6dd0faa7610b60d08a252081e4743e19ab3bd8`

```dockerfile
```

-	Layers:
	-	`sha256:48bf817d20068eaa7e21fc2e27d60986377007fb1de281abc2197b606a8e9d91`  
		Last Modified: Wed, 20 May 2026 03:23:16 GMT  
		Size: 22.0 MB (22041008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6760fb93e3276fc7a8d91dba24cab3607bdc2a86e639cfa9f5a80cc543a7a2`  
		Last Modified: Wed, 20 May 2026 03:23:15 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7cb60ac5193f2b72fb3bd4d09bf5b1022bd79ace9caf16da26a3eab0bdf36aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593771212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896ab85c14ebd2c6390d77a0ae6ccde1073505bb2b06ae50cfa7bd19e7072291`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 03:16:50 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 03:16:50 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 03:16:50 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:16:50 GMT
CMD ["erl"]
# Wed, 20 May 2026 03:16:50 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 03:16:53 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 03:17:14 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 05:31:23 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 05:31:23 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 05:31:23 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6302a33558dbca400d2c8d18eec519d6046916119625aeab14824af0bfc199`  
		Last Modified: Wed, 20 May 2026 02:15:39 GMT  
		Size: 193.5 MB (193461627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4cd73647fb421e3073e3ed789cc96d24e728624c8b05c7950d0d17d574d7f7`  
		Last Modified: Wed, 20 May 2026 03:18:07 GMT  
		Size: 259.4 MB (259409727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152d41829ab7cf06ba0edca2d8caa015b06c169165fb831319100151f2f548d3`  
		Last Modified: Wed, 20 May 2026 03:18:01 GMT  
		Size: 191.5 KB (191463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098aec5ed253190de9df19d9a76c411661f1aef722ce342c6e997dcd071e914e`  
		Last Modified: Wed, 20 May 2026 03:18:01 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca789b615a754bba394b4035cc261631e1b68fa1ce2acb6d30efa0c27ba9f2f`  
		Last Modified: Wed, 20 May 2026 05:31:49 GMT  
		Size: 7.8 MB (7766843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:7e3b07d8ba7f7ff64fae34546577fce78e4db5c1566a45ded1b050fbe184a70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21798344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d9030606e7c0421d5a9c9d4c9d4c5f14fa20fa75c490e9b5be3d7df64c3b1`

```dockerfile
```

-	Layers:
	-	`sha256:cd206a3df2c86169edf9e7abe71c57190e5a1cc181a6ab4874e6b09e1470e700`  
		Last Modified: Wed, 20 May 2026 05:31:49 GMT  
		Size: 21.8 MB (21786999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d575e7b91dbdb867cd2fbd0a9f96e2e2db4ee7594cc287a3d188b00c0e4bf31`  
		Last Modified: Wed, 20 May 2026 05:31:48 GMT  
		Size: 11.3 KB (11345 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:5fea7c7300998ea636e789f18eb1b68a52bbe17881ef30f7effc368bf6a97307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.2 MB (664155242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7739b9917a538f2d31707d4dfcc4e95a19792dd80f9915655c534fc7cafec53`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:16:10 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 02:16:10 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 02:16:10 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:16:10 GMT
CMD ["erl"]
# Wed, 20 May 2026 02:16:10 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 02:16:12 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 02:16:24 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 03:21:56 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 03:21:56 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 03:21:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882152811f66f9d033b8e9ebaa0473ab189d50d1a24186fe1ee418225e96521`  
		Last Modified: Wed, 20 May 2026 01:16:38 GMT  
		Size: 226.3 MB (226326757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7760c7122dce0477952b9a183fc847de6015e881496acdf5bf9f35f4a1928`  
		Last Modified: Wed, 20 May 2026 02:17:25 GMT  
		Size: 286.8 MB (286759588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c674542ad09658989593bad58ea40698dde4d7ad2959a2d96d1d32defe55f2`  
		Last Modified: Wed, 20 May 2026 02:17:17 GMT  
		Size: 191.5 KB (191482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3cd8a2ec4e91a540d1b9aba90a6dc042730b4e296ed6bee3003061a337861f`  
		Last Modified: Wed, 20 May 2026 02:17:17 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189bda442bcad4b4ff53024eb9c996277360ce63791f191cd750e4751082eef8`  
		Last Modified: Wed, 20 May 2026 03:22:25 GMT  
		Size: 7.8 MB (7766887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:c730f537d8ff2ab03880e046861518d5cb5b41a0a6f11dd9c63fe82a2d99a366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22123090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d608103c9ec431328ce23c124e248b9d7fd811f6df11f6fa770c5c2dda7451`

```dockerfile
```

-	Layers:
	-	`sha256:48ecbb2170cd37f8af9478ca25e8c1000dfc9e5f25c12de276bb080a0adc0061`  
		Last Modified: Wed, 20 May 2026 03:22:25 GMT  
		Size: 22.1 MB (22111714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c029d752fa8cccbeb91858a114126a876f7445e5159833be2a02a257855c9fd`  
		Last Modified: Wed, 20 May 2026 03:22:24 GMT  
		Size: 11.4 KB (11376 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; 386

```console
$ docker pull elixir@sha256:b00a9509f3f7323e35fbce5743576c3ad5b95c3531aa649ec86375a353168799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.0 MB (684043779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570d8384c5207e110cde76b5920ed90622dc99dc9104d7219d4889be0af318f9`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:05:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:11:54 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 06:11:54 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 06:11:54 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:11:54 GMT
CMD ["erl"]
# Wed, 20 May 2026 06:11:54 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 06:11:57 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 06:12:14 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 09:27:37 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 09:27:37 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 09:27:37 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aeb0e76e4fa3105ef9199a3e7497cb44daa369da999d0374d6f497cdd6aa9a`  
		Last Modified: Wed, 20 May 2026 06:06:40 GMT  
		Size: 240.3 MB (240286883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3110874ff0c56c9d258db7968b3b1abb8c83f9f5482d936276eaa92a1029b01e`  
		Last Modified: Wed, 20 May 2026 06:13:12 GMT  
		Size: 287.5 MB (287529336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed735fa0f84098ae7795e2ad1a755a861cfbeb2a14746b8ab2ba106b184fe77`  
		Last Modified: Wed, 20 May 2026 06:13:03 GMT  
		Size: 191.5 KB (191499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64d3601d3df21ff5fff4584b171b68955c91352719f926a4ed152c9b67e12ec`  
		Last Modified: Wed, 20 May 2026 06:13:03 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d876a2339ce2c83d3d8cfa0a2a206b1e3b3f4e975e7645eccda6782015eca625`  
		Last Modified: Wed, 20 May 2026 09:28:06 GMT  
		Size: 7.8 MB (7766846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:8666c3bdf22e74eeba64336a3273d903a741f73e17c3585964c397291092e9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22020194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e1e3c8d891461771a41fbdb3dcf211c065b9335daa7759e90353f7e2860e5e`

```dockerfile
```

-	Layers:
	-	`sha256:43e980fab75e5ae9a2375c53fbf5e110eaeeaccafd36bb23cc4eb2e5426c5c39`  
		Last Modified: Wed, 20 May 2026 09:28:07 GMT  
		Size: 22.0 MB (22008987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67264562bfd6465f452520feb4b6e6af31de224acdc2796ada4fc0268b73883`  
		Last Modified: Wed, 20 May 2026 09:28:06 GMT  
		Size: 11.2 KB (11207 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; ppc64le

```console
$ docker pull elixir@sha256:225ac2dfe8372c7ef07c6f10284cc204e05ccf3e966cc34cc9e0d28616088dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.9 MB (678897659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1899a96d3632b04da5ebbfcd623e71e3a29bff879e8703f060b95cbaf899428`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:10:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:26:36 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 12:26:36 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 12:26:36 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 12:26:36 GMT
CMD ["erl"]
# Wed, 20 May 2026 12:26:36 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 12:26:44 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 12:27:27 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 18:24:27 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 18:24:27 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 18:24:27 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf5baaa69eb61df93cfa5666d94d0c8ad399bda9d0ffc7582002bfe76ba1b4`  
		Last Modified: Wed, 20 May 2026 09:11:54 GMT  
		Size: 231.3 MB (231309802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c748a8e1e8ae86ea471d735ec8c59aca433a02f9c42c88a5334519861ab8c0b`  
		Last Modified: Wed, 20 May 2026 12:29:13 GMT  
		Size: 285.6 MB (285613796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324ce9219c9ad27c3d9de0c95fb249d0ef8ebaa536a4a9d00020830d465579c`  
		Last Modified: Wed, 20 May 2026 12:29:06 GMT  
		Size: 191.5 KB (191490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88005fe65dbfed5f34c60f5432c1e388e21a91cd09121701f3e3f276e40adc6`  
		Last Modified: Wed, 20 May 2026 12:29:06 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb88350772f891a1fb4de4bcf8b3721084fed4d219c4ddb1d954960e03afea`  
		Last Modified: Wed, 20 May 2026 18:25:32 GMT  
		Size: 7.8 MB (7766928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:a1f9d4457eeea64e704762c7add80a5e159e907f267292ffdf48b5b6320c9774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22012100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dbe27659e73ba3fec585e516f9b08e3b508682077274c50495a23dec2d1912`

```dockerfile
```

-	Layers:
	-	`sha256:88eb83f3fc2fc28aed404f25e746775eb7b10cb041fc025c69d7ef6bc712ee85`  
		Last Modified: Wed, 20 May 2026 18:25:32 GMT  
		Size: 22.0 MB (22000795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f08fda5e7daf7230780a399e5370adf7c7e317046527c46b3879e2092b5937`  
		Last Modified: Wed, 20 May 2026 18:25:31 GMT  
		Size: 11.3 KB (11305 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; s390x

```console
$ docker pull elixir@sha256:a0b5edc2fccad656a41be836f1cd9d2c12c0a1498a7992d2c8e4d6ad39c7313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.9 MB (650867814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf1ccb911e8f788c226873e8a3f01d2354522f318c275718916a583855e837f`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:44:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 03:16:00 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 03:16:00 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 03:16:00 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:16:00 GMT
CMD ["erl"]
# Wed, 20 May 2026 03:16:00 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 20 May 2026 03:16:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 20 May 2026 03:16:30 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 20 May 2026 06:59:56 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Wed, 20 May 2026 06:59:56 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 20 May 2026 06:59:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670b9b1c4f415c6933bd1559c9c20d59c3dc10986a265d1744b77a8f0cff5bf8`  
		Last Modified: Wed, 20 May 2026 02:45:35 GMT  
		Size: 206.7 MB (206680668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e505ba7cba2e8a4f63a0f1e95ccafa37d0347b70006307bacaa220c0ab7a1a`  
		Last Modified: Wed, 20 May 2026 03:18:03 GMT  
		Size: 290.6 MB (290586352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6e0edab4da794f55978a660ccbf378c58439b3bee1f834eb6d5f6faaa7c54`  
		Last Modified: Wed, 20 May 2026 03:17:52 GMT  
		Size: 191.4 KB (191446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c4a6358a3b2232e12c407fe52bb79cefd065066858b47f7fda97578d9e8a83`  
		Last Modified: Wed, 20 May 2026 03:17:52 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac30466f40d0833f47a4c5e96a5084db85a8c99895a2aeab20e73726bc18c77`  
		Last Modified: Wed, 20 May 2026 07:00:38 GMT  
		Size: 7.8 MB (7766851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:fe18e84744b6d7c8749c9da846d7607ef031406658ab7748d113789776b0ad76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21702018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713fa5b7973e1b57317a6e1f0d4f2a8756fbeb851441e7c4fe999c8d23e8116d`

```dockerfile
```

-	Layers:
	-	`sha256:2ca2956cf246d4b3bcd034255a70a0c0e6125cfeab08c1b5ccec5a2bab8f0d50`  
		Last Modified: Wed, 20 May 2026 07:00:39 GMT  
		Size: 21.7 MB (21690769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35ae08e7449dba21e2cfed13023f89ebd897168bf496ef423def5fd20d1392b`  
		Last Modified: Wed, 20 May 2026 07:00:39 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json
