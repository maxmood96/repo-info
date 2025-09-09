## `erlang:latest`

```console
$ docker pull erlang@sha256:d753e456739a85adb8088af8eed2a1a375bf8cc9e60774c474b86f3c9d899f6f
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
$ docker pull erlang@sha256:27968c18ddab0e2ce6a399f957e6628e6199956b80cd9a6f6fa5f7664d3b584c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.0 MB (624002607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38d2fa955c7b0d036262246636b59689c0a51acd4d8cad5892be019a8725b24`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c611f5bb386bf2363abc0bd48072bd52d81ec37f3717e3d4c789fdd12e467168`  
		Last Modified: Mon, 08 Sep 2025 22:39:36 GMT  
		Size: 211.4 MB (211421189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fe9e50d45f72f97e60a030edb42cd6e4380c6c463c1494080251f9b914ef13`  
		Last Modified: Mon, 08 Sep 2025 23:12:38 GMT  
		Size: 274.7 MB (274668667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41c6879d80d6856a847b6aee778ce852aceac06e050f41da8ef0fc2b1d4b52b`  
		Last Modified: Mon, 08 Sep 2025 23:12:22 GMT  
		Size: 191.5 KB (191480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2d1cf02eaf8995cd4d19606d35fc9f44eeca564997b67ad6d488f1aaac6ce0`  
		Last Modified: Mon, 08 Sep 2025 23:12:23 GMT  
		Size: 817.8 KB (817750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:f63bfeec8aa2f44fa9070ee923eb9aad3f7779be64ca7c0ca55ab3a74a707da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23956713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9cc99ac6a5b97d7ea1b70b10196e8ce901a44621400735cf3c3509d1cb634f`

```dockerfile
```

-	Layers:
	-	`sha256:f8b8eeccfc69b1d9ee6c59de07d52d7b107c00db877956d89be8465631372d86`  
		Last Modified: Tue, 09 Sep 2025 01:48:46 GMT  
		Size: 23.9 MB (23937434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914cbdb10b953933d4c64757936314238d2fe8db999d73afc9686480bdb4f766`  
		Last Modified: Tue, 09 Sep 2025 01:48:48 GMT  
		Size: 19.3 KB (19279 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:f217993466fc4899034964b480f5f9de1246df1102b627c0a4950da2023e60e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564322559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f334780b88a9c8c59671343e33e3f89879b4a3833aa62bae3d00105ffdecdeb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:ea0d25317149dd26fe3fc21f7a1766f8528af12760c2aee4e2fa23834000897f`  
		Last Modified: Tue, 12 Aug 2025 20:44:49 GMT  
		Size: 46.0 MB (46027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77dbe9c143107c5d6e98f6ee7910a0557899d9127736c302e12bf8899d1979`  
		Last Modified: Wed, 13 Aug 2025 00:00:04 GMT  
		Size: 22.7 MB (22696262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f842f3168ffd158b534ca355440e1a28a63cbae85f8b2422f379efca96dac9`  
		Last Modified: Wed, 13 Aug 2025 06:05:53 GMT  
		Size: 62.0 MB (61997775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eee63db90f049e2c0237162eb07f4b5adea30dfea118ddcf6da1245be79921`  
		Last Modified: Wed, 13 Aug 2025 11:56:57 GMT  
		Size: 184.7 MB (184651580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a4afea10d3492b16d788984ba6c202e4fe1c5f419a4f26e58752f980b56b1`  
		Last Modified: Thu, 14 Aug 2025 16:16:22 GMT  
		Size: 247.9 MB (247940558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4472e19fd6c07be3c4c00dffe7d9769ce79cdb727f21e1d53dc80208feaad6d0`  
		Last Modified: Wed, 13 Aug 2025 12:08:56 GMT  
		Size: 191.4 KB (191398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dff5b42c81fedf55e4f6867b5c8099abda116cf0efad2cbf8d449f1f9a07a8`  
		Last Modified: Wed, 13 Aug 2025 12:08:59 GMT  
		Size: 817.8 KB (817751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:14b4b49b4cc1b50e0502854234e758aa8f957f0a1a5dc98ac4fceb990b0608f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23745829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86e5a9696b61eb5997a2ac63efdf5caec579713b2c469d750cda6379ea586fd`

```dockerfile
```

-	Layers:
	-	`sha256:8bff1af3e8fde5fedafdda31c8310cedd1c7230d88a80c536de3e4a32f960ff6`  
		Last Modified: Wed, 13 Aug 2025 13:48:01 GMT  
		Size: 23.7 MB (23726440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d792f785702299fa55c8ad1de1d1b0b1c5f922c4953ca41409a5b04c29d7d70`  
		Last Modified: Wed, 13 Aug 2025 13:48:02 GMT  
		Size: 19.4 KB (19389 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:08a3a19f53fa3b4973a191efcfab5a28ee172e55d43effdbc9bba4092c67c0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.2 MB (546160591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2a23837d9a2d82ef98167fd28033e566caa781e0f48c0dfc58f77cc7369ef0`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b123fb3b68d3192243d66f2675c945600a5ac7493f7a06af8327cd33d6e937ff`  
		Last Modified: Wed, 13 Aug 2025 13:57:25 GMT  
		Size: 175.3 MB (175309693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed9ab731f40df5e56426d5d24b69e43306f9420d0ad0713763e3eb2d987f938`  
		Last Modified: Thu, 14 Aug 2025 07:08:12 GMT  
		Size: 244.0 MB (244046543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0e6f05cd5ac99629f49e4e52e07f80bfd415a4ff60dae2c0522b2b33a81a8b`  
		Last Modified: Wed, 13 Aug 2025 16:24:51 GMT  
		Size: 191.5 KB (191454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee4bde27878e28f73632b6caadbfb14cadef6c6097d07089f451d78971ec90`  
		Last Modified: Wed, 13 Aug 2025 16:24:52 GMT  
		Size: 817.8 KB (817751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:aff7e4a164346dd0508865b4db01be6dc56870562fd6135e23d26b1aacaee5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23762776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3408dfadb695d7549d46b1e4d92ec49f40001b7c7fc3c8224ed7f7519f0674a`

```dockerfile
```

-	Layers:
	-	`sha256:347e2cc87414864dc0cb9cc3f7451dbfebb4e511ffbdda5c6686ae5e95b44005`  
		Last Modified: Wed, 13 Aug 2025 19:48:32 GMT  
		Size: 23.7 MB (23743387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf83afe66caa40593011b00019c18ccd04410a0ea2f850a8138ad21cc008c6f7`  
		Last Modified: Wed, 13 Aug 2025 19:48:33 GMT  
		Size: 19.4 KB (19389 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:7c8eb512252a421610963b20ff0bb50799705584e1a756b1ece94b8ea689fc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607477539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2e5a9a3822954c737ad03db7d364aff5e849df5bf5cfe3a1bf14a79b8d0823`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a74a28f78609dda29415ecfe729e4368c794040a88bc1c63d9b1e59b1d062db`  
		Last Modified: Tue, 09 Sep 2025 03:11:57 GMT  
		Size: 202.9 MB (202918593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1340693f51da3d24e5a9ea8bc23811b9224e54354f777cbd3901f0e78657dc7`  
		Last Modified: Tue, 09 Sep 2025 06:47:56 GMT  
		Size: 267.2 MB (267224755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f368800e38d8660baab657278e6ee7bd9be4e2b6c557f6730609cc1a9ca69`  
		Last Modified: Tue, 09 Sep 2025 03:57:54 GMT  
		Size: 191.5 KB (191453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80485f4e2a9d4ff0c3342742f9e1c241a95ccd504519d93a9deb042f6242690e`  
		Last Modified: Tue, 09 Sep 2025 03:57:54 GMT  
		Size: 817.7 KB (817749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:f77d6830eccf285f2b48becece34b199397a5e43923217eef449138c07239a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23996358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdb4c0141cb2fe6eb108207d1be28e8a067db5652fb95346b8daab12e4f7e55`

```dockerfile
```

-	Layers:
	-	`sha256:dfabfb0f736b3383c855a87fbaa087704957d93914c39c7f67ef0ff745db1d88`  
		Last Modified: Tue, 09 Sep 2025 04:49:01 GMT  
		Size: 24.0 MB (23976933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9140905c96b5fc9a6203afe8f756ebe6e8f091d079b9ef7c85ec969ad67f16`  
		Last Modified: Tue, 09 Sep 2025 04:49:02 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:9cb598cf11aa58c7bb31001620fdac96cda6b372dde2fe10ecbad6ec632ed1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624604626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2d441c1f2a0c39708d24db331e740ad9dc00f6783583f0d966a6cb552540c6`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2248c0dfdaafb69ef95f2c3162eb9698e04d446b6646131ff2e543b79a6f79f`  
		Last Modified: Mon, 08 Sep 2025 22:39:17 GMT  
		Size: 66.2 MB (66233051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efc7fe3a1c89761524039b4f9f63bc7204a43b81c944a48116721a83084fc65`  
		Last Modified: Mon, 08 Sep 2025 23:12:07 GMT  
		Size: 210.3 MB (210349081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd81b8a79996de573696faa65f1b1a348fb2894384f2eeed0d31a838b70fc35`  
		Last Modified: Tue, 09 Sep 2025 00:12:08 GMT  
		Size: 272.7 MB (272685942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36748acf2a3bd106e87ae844f5a2002a4cff99a703ba79a6bcd8a3bb28769af1`  
		Last Modified: Mon, 08 Sep 2025 23:59:07 GMT  
		Size: 191.5 KB (191460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8999e1d90a7c65c7cf4660e4d0791ac5ebe97165976037cc5df2bc37a144f7`  
		Last Modified: Mon, 08 Sep 2025 23:59:06 GMT  
		Size: 817.8 KB (817750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:824cc9d5c0ceee3f00731e82b4c09c370b1d3b812cbe6fa4993442b1db28fc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23924283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257dcaed59cf093f6c53ff2fc313ff65a91e0d762b79347ac153de955c6bc3a1`

```dockerfile
```

-	Layers:
	-	`sha256:3b5dc67d18db83e1acd2ed7c218dbe89187bffaa018982979fd6b75838aa1897`  
		Last Modified: Tue, 09 Sep 2025 01:50:27 GMT  
		Size: 23.9 MB (23905045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95617cebe00b9b7bf6f9723143b80e7e07bdd1adee4c3e33a7eea7a3b662bff4`  
		Last Modified: Tue, 09 Sep 2025 01:50:28 GMT  
		Size: 19.2 KB (19238 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:83a9a21f7fb48c4f99a92f2fbd9fab3b314bc7d5616d0407b8ce08a330b0aa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580390304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e649bbde8e2d70266d2a009a12935b5c0acbdea1cb18a09076aac8e6d48111`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dd009b2c0eac49c44c2dee3d1630efa856443b90137d58c5f7fad2726b4dd4`  
		Last Modified: Wed, 13 Aug 2025 21:10:18 GMT  
		Size: 190.0 MB (189978832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1228e6431ad6c3627dc0c1975acfea0ee83302b15b7aaecd37d02ab13668a01`  
		Last Modified: Wed, 13 Aug 2025 23:02:38 GMT  
		Size: 253.7 MB (253713224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827bee3387b41b8b4e884fda19545b719f8fc0b40309cb8b3773a4bb193fa858`  
		Last Modified: Wed, 13 Aug 2025 22:29:53 GMT  
		Size: 191.5 KB (191466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7839fed3559a17ed3710d973cfe095560a18d265d0fe6e40647976ef84e9b5`  
		Last Modified: Wed, 13 Aug 2025 22:29:53 GMT  
		Size: 817.8 KB (817751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:e23440321f83d9015ee65ebe44a6cd2931862ad5fc3d32fa23c84f506a4d6d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d81418ffbf43d95a02cfa9afb08f6b12c9c9adaa06a51fc7224fedbabcd08cb`

```dockerfile
```

-	Layers:
	-	`sha256:379136d1d3f68b38e583e092ae9237a85b924e0ed6a5ad2032f8d2a8889b3faa`  
		Last Modified: Thu, 14 Aug 2025 01:49:17 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:ce9e1f444aa276849b1dbe0a723e92f3ea8273107538e48a480da12889e472c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.0 MB (631978129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477778c9a448685bb48ab04eff6d690b1ac23dcbbc3bc1f13800332b4bcb5c43`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9ab368175c07efafc97db73dcb256947b7c350124b285ef68898aa41837a0a`  
		Last Modified: Thu, 14 Aug 2025 04:19:57 GMT  
		Size: 214.4 MB (214443029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f56fd7e47b9765fcee6ac3f3fd8842798d5dc90944205ae864d53f3c6ee4da1`  
		Last Modified: Thu, 14 Aug 2025 16:14:55 GMT  
		Size: 268.7 MB (268681759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee251a03247becc9fdc25e6288907683aaf8659a1c391cefae55ede581bce1`  
		Last Modified: Thu, 14 Aug 2025 07:33:49 GMT  
		Size: 191.5 KB (191508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e999ff351ed22a5eccb4bc0a98e68485dffa794d30251bcbc78879edc3bcf1`  
		Last Modified: Thu, 14 Aug 2025 07:33:45 GMT  
		Size: 817.8 KB (817751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:2dd4098c222beeaf971ef3ba2bbfd5c6f893fb55834846fa4ecee682a462c787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23905329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec388741ef0f9855854ed261fbcb495867ffffb263d1656146f85286cbbe71a`

```dockerfile
```

-	Layers:
	-	`sha256:de8d32753e69b5cf9f3e3fd75bccc236e8714c47f2b33250ffe7953e3fe4055a`  
		Last Modified: Thu, 14 Aug 2025 10:49:06 GMT  
		Size: 23.9 MB (23885996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb944cd18a5b955d28884e576caac6947033523c8936489b0514bd1c204f5aa`  
		Last Modified: Thu, 14 Aug 2025 10:49:07 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:0f0862220399cbb96f82304bac7091333f33707e3cbfb7a72a189b1ce55244ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584814623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ca744f4fb9bee6d7ba3321aaff5745193d185e5633e1b0b8801989d379de39`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
# Sat, 19 Jul 2025 21:18:01 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b9cbc74544afc5347651ab08e064f57c5d096af02c42cfe03213911a89bce4`  
		Last Modified: Wed, 13 Aug 2025 19:43:03 GMT  
		Size: 183.4 MB (183435038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262224cd87ab2ac636472c51660d7f5938e8051de0533b0c88b56b6cfb5f3dd`  
		Last Modified: Wed, 13 Aug 2025 19:43:13 GMT  
		Size: 265.7 MB (265702558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ffa0baff9efd717a70dff5762701119943eae85f5b8d0288b964b7e94480c9`  
		Last Modified: Wed, 13 Aug 2025 18:28:47 GMT  
		Size: 191.5 KB (191469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad9a531dc37476560b581384ffd7149b30ba65f07114f3c27505e7b1c37f4c`  
		Last Modified: Wed, 13 Aug 2025 18:28:49 GMT  
		Size: 817.8 KB (817751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:761808bee044faa1d968d5307ca9e1b696dff29392f089fb66cf05cc636a4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23717030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcf3007b8762228f4ebf589f4f705c89ef1ae69e43c7a6a1f26e401af629834`

```dockerfile
```

-	Layers:
	-	`sha256:11f08d34e54a7adf00253b1fec48fbd68a8dee8231d7f0df1d6dcfdba35d8ada`  
		Last Modified: Wed, 13 Aug 2025 19:49:45 GMT  
		Size: 23.7 MB (23697751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abb514bfda472348ace21090ea25758377dd758bbf7a30f4b5d71b5bb8180cf`  
		Last Modified: Wed, 13 Aug 2025 19:49:46 GMT  
		Size: 19.3 KB (19279 bytes)  
		MIME: application/vnd.in-toto+json
