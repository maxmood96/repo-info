## `elixir:otp-28`

```console
$ docker pull elixir@sha256:0895a65dc25a4e6bf9fe29dffa1dc74052c96e6e94e9a89ee06f4e1e85330be3
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

### `elixir:otp-28` - linux; amd64

```console
$ docker pull elixir@sha256:517c447823de826f17de0d431e2a9ef444190a02ace1e915e7cd39f06bdfd276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679598280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131fe7f1feed27dc90055bd4d505fcc6f0b97305210868f43ab0c4119b8f9fca`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:23:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:22:02 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:22:02 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:22:02 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:22:02 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 22:22:02 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 22:22:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 22:22:16 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 09 Apr 2026 23:17:25 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 09 Apr 2026 23:17:25 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 09 Apr 2026 23:17:25 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecbddc58afba44ec9b55fb51ec8bfdee5112cd31b39b564f5abb4567d094ffc`  
		Last Modified: Tue, 07 Apr 2026 03:24:29 GMT  
		Size: 236.1 MB (236080738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599d20cd2abf7fba52bbcf98d066838a760d0408e7374f093987be2cf3484b8`  
		Last Modified: Thu, 09 Apr 2026 22:23:18 GMT  
		Size: 292.0 MB (292039165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2322a9941361cd14fec3124cfeb6db0424c214e192b46cb3b3f7e3a863f08333`  
		Last Modified: Thu, 09 Apr 2026 22:23:12 GMT  
		Size: 191.4 KB (191393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f3a2ac034b1de6b77d1c7fbac781a48ea99c9b4a6459cf704eb2ec3ee2a80e`  
		Last Modified: Thu, 09 Apr 2026 22:23:12 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1dc1f4c4c64d7818740e384f0043e7d41111e19315f11d757879f80edf1ab1`  
		Last Modified: Thu, 09 Apr 2026 23:17:57 GMT  
		Size: 7.8 MB (7766918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:d24b7e3a1cee832c74a11d169d35994628c35b18cbd5d71d903254a183360a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22066636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b43349c14493bf9017e02727744177086ca87df7089b3f47becae260ca17822`

```dockerfile
```

-	Layers:
	-	`sha256:136742032e7a947078a3267c4cd97d187be7b74cf3841b31b2982e5bf72bcd5f`  
		Last Modified: Thu, 09 Apr 2026 23:17:57 GMT  
		Size: 22.1 MB (22055385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58604e37190b1a16e4f49a0c398965f6c7e166ae3b7da67a4fc782f10a442621`  
		Last Modified: Thu, 09 Apr 2026 23:17:56 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f07ec267f9f7a2e12426aa414413cf1ad5301cf4a5d8656e34bd0e4f897d635d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592902593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d14722e87d5ccf202baf83f647465765cdb0f2d6edbc704b4a7b4a7ba510a64`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:28:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:34:46 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:34:46 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:34:46 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:34:46 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 22:34:46 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 22:34:49 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 22:35:10 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 09 Apr 2026 23:31:07 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 09 Apr 2026 23:31:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 09 Apr 2026 23:31:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868f799858ac0f14507e60a2ff0757894394681e874e60066914254664b5431`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 62.7 MB (62722704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a56a1d02d67e0e604b723b436e43ce87c3ff9c7c9d1a33b11ae2b9d56157431`  
		Last Modified: Tue, 07 Apr 2026 04:29:18 GMT  
		Size: 193.4 MB (193383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2e057884f0d0042e679d516318eb9b65882aad408275ab15e5244d9f6ec5`  
		Last Modified: Thu, 09 Apr 2026 22:36:03 GMT  
		Size: 258.6 MB (258647766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c08eea8740b06a1e2d1bb211886892afdeee12fefe3a537a14523d44d71a9d`  
		Last Modified: Thu, 09 Apr 2026 22:35:58 GMT  
		Size: 191.5 KB (191466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6889c4ced7f4e87690b34ceaf93292e8b881d36685e3d89d2a7a0311be259f7`  
		Last Modified: Thu, 09 Apr 2026 22:35:57 GMT  
		Size: 819.8 KB (819844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c894338432c9b0350831cfd93224dfad2157d1f3f29ebeffa7de73b46a0639d8`  
		Last Modified: Thu, 09 Apr 2026 23:31:37 GMT  
		Size: 7.8 MB (7766867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:76ed47fdf4bbdb1428fe89e7e88f9624eb65b6b1247d5d27a8236774f6806b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21812732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eabf2b78b04704d7bda51b82170b677da031bd68d243bb4756db97c1861ccb4`

```dockerfile
```

-	Layers:
	-	`sha256:d25593de4faaa65d1d61402beaf25ee35e771beecfc444ee8247948634af359d`  
		Last Modified: Thu, 09 Apr 2026 23:31:37 GMT  
		Size: 21.8 MB (21801385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807e5be8ba0e52b09d00b88f3485b34995299229ecc312bb40409c389e9b9df6`  
		Last Modified: Thu, 09 Apr 2026 23:31:37 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:733073ba22fbe1db5387f365f113f3143a7d54594443773544e2e5dd67f68d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 MB (662024903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcda15287b8e0e23f56405b2c2268f77c850077fc38ae8ced2f7b31c110925e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:35:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:23:04 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:23:04 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:23:04 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:04 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 22:23:04 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 22:23:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 22:23:17 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 09 Apr 2026 23:18:39 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 09 Apr 2026 23:18:39 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 09 Apr 2026 23:18:39 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f39c683b3e4557014b1769dd25b1748b896e4ae99e9125c194afb7f3ac82971`  
		Last Modified: Tue, 07 Apr 2026 03:36:17 GMT  
		Size: 226.2 MB (226200655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913079a34686f8de5c97129016b213dbee0dc6e29aa26f133c1190fe06139bde`  
		Last Modified: Thu, 09 Apr 2026 22:24:17 GMT  
		Size: 284.8 MB (284765160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5456a615260a53a259c2461372e1b495c342efcfce4aac6dc532e67e61e313e`  
		Last Modified: Thu, 09 Apr 2026 22:24:10 GMT  
		Size: 191.5 KB (191477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915a35b063803bc153aee3c0fd8e14ae89b49be77b65799c37bcfb3180de2b0c`  
		Last Modified: Thu, 09 Apr 2026 22:24:10 GMT  
		Size: 819.8 KB (819847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06081991c9b141b3bdfb9b14d27554a6ed0d6f678df10396a5a2de99c718c5f6`  
		Last Modified: Thu, 09 Apr 2026 23:19:11 GMT  
		Size: 7.8 MB (7766939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:28930ea2f65c216aedba6cb6b3cba10b067cc51a49fd398b71e9916a9b324e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22138110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4817ac6e68a2998b088072d9ec9b45fcd5f277b67adfe47808096c87cc8131`

```dockerfile
```

-	Layers:
	-	`sha256:ce3fd2eb7f1fe6846a4cbc84efc6667113f9e0988c4d8a717f17e6456dee4a35`  
		Last Modified: Thu, 09 Apr 2026 23:19:11 GMT  
		Size: 22.1 MB (22126731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a6bf6d479f513600881ef0f4897a0713fbc51b7047bc8c8800b1b440f45b5b`  
		Last Modified: Thu, 09 Apr 2026 23:19:10 GMT  
		Size: 11.4 KB (11379 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; 386

```console
$ docker pull elixir@sha256:69547766429dd3cbafa0b528d6d184d0506e91ffd4aba935d1b19ae660d8de53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.9 MB (681936355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124acfd9dbaf1e9bb4ace1d116c708490b4f341cf7a3019fca6ba073f8dab3f7`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:20:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:23:47 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Fri, 10 Apr 2026 00:23:47 GMT
LABEL org.opencontainers.image.version=28.4.2
# Fri, 10 Apr 2026 00:23:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 00:23:47 GMT
CMD ["erl"]
# Fri, 10 Apr 2026 00:23:47 GMT
ENV REBAR_VERSION=2.6.4
# Fri, 10 Apr 2026 00:23:50 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Fri, 10 Apr 2026 00:24:11 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Fri, 10 Apr 2026 03:33:11 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 10 Apr 2026 03:33:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Fri, 10 Apr 2026 03:33:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6419d63858855afa34d3a14b889b2d9e157f74b4901b779052fba5d24c1f0a5e`  
		Last Modified: Tue, 07 Apr 2026 03:20:54 GMT  
		Size: 240.2 MB (240182156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcfc922cf2e34215fbf83d3ac3e882a8af934aa281298ba3ba8df989bd02728`  
		Last Modified: Fri, 10 Apr 2026 00:25:13 GMT  
		Size: 285.6 MB (285578259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f5742e1a15ff74a609962fe47c4074f010d9ebfe7d8e7a6d14e484a32beddf`  
		Last Modified: Fri, 10 Apr 2026 00:25:06 GMT  
		Size: 191.4 KB (191447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aaaac039b89a2894557ef7ef7bcab7fcd195f258f7888653c1b6b9876f0fa7`  
		Last Modified: Fri, 10 Apr 2026 00:25:06 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a843e531d6b0a8fdc7d3049beed2f9dd8f7b6f4c00b829c4b3fd61000c2c1a0`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 7.8 MB (7766871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:5c6bc7639ae35d5831f71e8daafe8f909c6a1561ae8996ebc38b0d3ab814c8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22034559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2403c516d6b66add35b52bd361ec42b98b05c1a117099abe6ea2f9c9c0c99c`

```dockerfile
```

-	Layers:
	-	`sha256:29e8a865ffaead7e464c9e168b10286d75ccacab785a5c25ad27da074183f617`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 22.0 MB (22023350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a8e5e1aaf754886b4edaa5a86c269a1296a28efef1de1ef6415966bb55e789`  
		Last Modified: Fri, 10 Apr 2026 03:33:45 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; ppc64le

```console
$ docker pull elixir@sha256:9127a34ee06c881fb5f3eb27d4ca786f5a9d02ddf90446fd804e061f47144ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.6 MB (676612944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf296316241163ae1d2c603b87ad5ebf20e41a8a2d5daaf95c06a8e793aa7cd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:12:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:27:45 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 23:27:45 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 23:27:45 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:27:45 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 23:27:45 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 23:27:52 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 23:28:35 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Fri, 10 Apr 2026 01:02:05 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Fri, 10 Apr 2026 01:02:05 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Fri, 10 Apr 2026 01:02:05 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169353b9ab6307e2b065964fc878588895f32907dd884c905868bc86f58edd0`  
		Last Modified: Tue, 07 Apr 2026 09:55:34 GMT  
		Size: 73.0 MB (73033989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5f682bd4776a2aa089944df5527ca4a87b57f256c6c979b8dea44633e85334`  
		Last Modified: Tue, 07 Apr 2026 18:14:03 GMT  
		Size: 231.2 MB (231208883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d347741419bdd1e8f04906a44603476487fba752c64806e29644b95bfde88`  
		Last Modified: Thu, 09 Apr 2026 23:30:22 GMT  
		Size: 283.5 MB (283459327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41362d7807bce2a9d4c8bfcdfa0bcbba5608b6f7775fd0ffbf89f88c2d6b5080`  
		Last Modified: Thu, 09 Apr 2026 23:30:15 GMT  
		Size: 191.5 KB (191461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb334d667d2885268edbfd740129f339c3a4393a263f0d6353dcc04ffb5fb5`  
		Last Modified: Thu, 09 Apr 2026 23:30:15 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96404ed91b2cb0f8beab23a4f80770cb89af1da6b6b5caabab54a76d442a1148`  
		Last Modified: Fri, 10 Apr 2026 01:03:15 GMT  
		Size: 7.8 MB (7766914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:c5e1d24f6fc6809cb5b27e9ede576ddbc38a625f66891fc2ab6c4d1c387e5bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22026514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bf809e60e738e2aab10b0e3ae5d6257bdac5d5d9698df32123d30a56634c2e`

```dockerfile
```

-	Layers:
	-	`sha256:8d9df8976eef26bcd514c2cc1562746e25d69e17f932ed564df8ce2d39958d2f`  
		Last Modified: Fri, 10 Apr 2026 01:03:15 GMT  
		Size: 22.0 MB (22015207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf589bf03ddd2845f942d28a0ac8794f8337674cdf8f3846a8a92e87ac206d3e`  
		Last Modified: Fri, 10 Apr 2026 01:03:14 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28` - linux; s390x

```console
$ docker pull elixir@sha256:71bd10ee9d2dfa2b3ca3781c1ec0a430ed7c110920605b776797c0bcfd8d03b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 MB (648311080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818f6b44d2fdef6a471aed9ca35e940b776182ee137a486770fd9b8286440ab`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:51:03 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:51:03 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:51:03 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& runtimeDeps='libodbc2 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:51:03 GMT
CMD ["erl"]
# Thu, 09 Apr 2026 22:51:03 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 09 Apr 2026 22:51:07 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 09 Apr 2026 22:51:32 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 09 Apr 2026 23:26:40 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Thu, 09 Apr 2026 23:26:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 09 Apr 2026 23:26:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b42c01b5de7637ae2e011d2f9775f913b01f72b9797773d410bb0d8b437e3`  
		Last Modified: Tue, 07 Apr 2026 04:55:14 GMT  
		Size: 68.6 MB (68627207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e82267bc4ebc28378ed6c6c1dce93d9a8153001345f0a9a7b4524da2320253`  
		Last Modified: Tue, 07 Apr 2026 06:01:03 GMT  
		Size: 206.6 MB (206593982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ae8ea6ee2d4c7b16bf80591396a63696aeae729940f0c5a9833113dcbd0d4`  
		Last Modified: Thu, 09 Apr 2026 22:53:00 GMT  
		Size: 288.1 MB (288143555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a6f8518b73354f93f11cf2b37c052f29e92aaf3cd7d38a59ab5ea361474da`  
		Last Modified: Thu, 09 Apr 2026 22:52:56 GMT  
		Size: 191.5 KB (191486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381740e89da9d7d806ba9c4c93e66088a79e1a6024bbf6cf934c079d1db415c3`  
		Last Modified: Thu, 09 Apr 2026 22:52:56 GMT  
		Size: 819.9 KB (819853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a5ca5a0e64f27442391564eed9f979a36a8054da474b97b09173810cc144fc`  
		Last Modified: Thu, 09 Apr 2026 23:27:28 GMT  
		Size: 7.8 MB (7766849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28` - unknown; unknown

```console
$ docker pull elixir@sha256:74bdce36d0e6c570fe0c58617cfd54f9eed6b6904135a932a5c7173eda4c4f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21716394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d350c7ed650912335101f5e3752e51ff1084d3510146871586d890c0103b835`

```dockerfile
```

-	Layers:
	-	`sha256:6b4bd40265a503ddb98eba92713ba7d4e95a1cd4ba1e15204258c566a97567e0`  
		Last Modified: Thu, 09 Apr 2026 23:27:28 GMT  
		Size: 21.7 MB (21705143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a6c264b007aa66b717d8e250eb1e962ad0a2586af5cac0af5cca6c87dcece0`  
		Last Modified: Thu, 09 Apr 2026 23:27:27 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json
