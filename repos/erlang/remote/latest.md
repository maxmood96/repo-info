## `erlang:latest`

```console
$ docker pull erlang@sha256:a44c199fe2df14170a8ca4b0b71874699a817f934c7b04d9f82547f5dfa117d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `erlang:latest` - linux; amd64

```console
$ docker pull erlang@sha256:7327b86cfd55984b526560279248bfae0935075305397649b320a4bc8124e0ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.8 MB (573766956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638d63e204a0d3f58ae077505901c4ea42ec07b5e0c151cdf6dd10c78131bc05`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 17:18:02 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Thu, 11 Jan 2024 17:18:02 GMT
LABEL org.opencontainers.image.version=26.2.1
# Thu, 11 Jan 2024 17:27:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 11 Jan 2024 17:27:55 GMT
CMD ["erl"]
# Thu, 11 Jan 2024 17:27:56 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Jan 2024 17:27:59 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 11 Jan 2024 17:28:18 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92159de95ca6028dff92254cdede6b16274470e653943871542fceec95bdf5`  
		Last Modified: Thu, 11 Jan 2024 04:46:29 GMT  
		Size: 196.9 MB (196898008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99a32506142537f340bcf5eeaac00393ab0d4ab5b1017400d59f9bb732cbc7e`  
		Last Modified: Thu, 11 Jan 2024 18:21:07 GMT  
		Size: 250.5 MB (250468087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7357ab4ba0350e85c0b8b4c6b3f18fad9361ae1382b1648d74ed82794dfda08`  
		Last Modified: Thu, 11 Jan 2024 18:20:37 GMT  
		Size: 195.0 KB (195008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b832f90d4869a6f0e19575c28e9e7869f8f949ec3ec1681804572ff4631a1b`  
		Last Modified: Thu, 11 Jan 2024 18:20:37 GMT  
		Size: 781.8 KB (781812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:6c1837605c845059a8eaf85413a3af5a6f36a5e4dcd19cd00a71b120935c14b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.0 MB (521032439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d4dbc3170729213483ab11062332ea6956447e75f23f3f0bcfcad67da4227e`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 01:49:11 GMT
ADD file:a5224163b267c4b112f96005ef36619be78d0b949e20d9008f94efc7116f9605 in / 
# Thu, 11 Jan 2024 01:49:12 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:53:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:32:20 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Wed, 17 Jan 2024 02:32:21 GMT
LABEL org.opencontainers.image.version=26.2.1
# Wed, 17 Jan 2024 02:47:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:47:45 GMT
CMD ["erl"]
# Wed, 17 Jan 2024 02:47:45 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Jan 2024 02:47:52 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 17 Jan 2024 02:48:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:8600a8817f4f0136707c29239c933cdd333774f1c11cb22b584b1a8aeb8dfc22`  
		Last Modified: Thu, 11 Jan 2024 01:54:27 GMT  
		Size: 52.6 MB (52562506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bc1922e013704565755aa5c4c598e90fcc2d6789bc2a799e5c8d1ca3343707`  
		Last Modified: Thu, 11 Jan 2024 07:07:19 GMT  
		Size: 15.4 MB (15376503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d6582f82930ef638d1cae979e850b2db586d7320f33ac406a88bd2c75f827`  
		Last Modified: Wed, 17 Jan 2024 02:03:09 GMT  
		Size: 52.3 MB (52333753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aafa7333da239fa8500eeaf1978be387094511cf6b8d131de3a1fdb9108486`  
		Last Modified: Wed, 17 Jan 2024 02:03:55 GMT  
		Size: 175.1 MB (175125086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2c1272f691a67f4cd37a292b1348a251a21768b0954690dd861dcf40f3bd4`  
		Last Modified: Wed, 17 Jan 2024 03:19:03 GMT  
		Size: 224.7 MB (224657822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e527c8efb4460c6eaad3577c151c360f35786744393d777158bced0c1aa31fd`  
		Last Modified: Wed, 17 Jan 2024 03:18:16 GMT  
		Size: 194.9 KB (194916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be53728f7aede6169173bd2f78fb1cff947044f97037c99c6e5081ecedd49d`  
		Last Modified: Wed, 17 Jan 2024 03:18:16 GMT  
		Size: 781.9 KB (781853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c3a2ff1fe5efa42eadbeeaac39a71a72c57eb23f59fa1b3c6b8077c2428b953d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.7 MB (507733379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1842d12247a37cf35994b884e06a20dc886de6b436f4e51081022c99e33cfd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:21 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Thu, 11 Jan 2024 02:42:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:17:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:18:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:43:16 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Thu, 11 Jan 2024 03:43:16 GMT
LABEL org.opencontainers.image.version=26.2.1
# Thu, 11 Jan 2024 03:56:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:56:03 GMT
CMD ["erl"]
# Thu, 11 Jan 2024 03:56:03 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Jan 2024 03:56:08 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 11 Jan 2024 03:56:37 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc92f863388ea7a660a09ac1581e426ed098ac1fe970d4ad13e7ac5a7d728ee3`  
		Last Modified: Thu, 11 Jan 2024 03:30:20 GMT  
		Size: 14.9 MB (14880496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beed4a52918ba95386e3ac173b88fc7288089f222b228de3a8cbf42db7e3b26b`  
		Last Modified: Thu, 11 Jan 2024 03:30:43 GMT  
		Size: 50.4 MB (50361323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f233723a06f92748bddd9e52e30f291efa1d2182155c325cb8f292ee52d0520`  
		Last Modified: Thu, 11 Jan 2024 03:31:25 GMT  
		Size: 167.4 MB (167381761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858037279a2c30c4fa72f2f8809c6cc5453a8a1adfe26fe2917669494b24af4b`  
		Last Modified: Thu, 11 Jan 2024 06:17:40 GMT  
		Size: 223.9 MB (223917478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320e350fbcafbd2e6d5a273b768b71bdc490c1dd6c0b06102d2ccac08462da03`  
		Last Modified: Thu, 11 Jan 2024 06:16:56 GMT  
		Size: 195.0 KB (194981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175bddf656aa2af5855bdbdf68980575dff803deb93d614d89fc3fa3a12aefc0`  
		Last Modified: Thu, 11 Jan 2024 06:16:56 GMT  
		Size: 781.8 KB (781810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:35bc82b40657b45081738d0ffe1a48087fad81a2bacf8f28137c9f9efc7955b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 MB (558988232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d170f462556c5ccef7051014e708a9b8ca235e9db3e963cf167663b1565cc1`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:25:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:33:23 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Wed, 17 Jan 2024 03:33:23 GMT
LABEL org.opencontainers.image.version=26.2.1
# Wed, 17 Jan 2024 03:39:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:39:13 GMT
CMD ["erl"]
# Wed, 17 Jan 2024 03:39:13 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Jan 2024 03:39:16 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 17 Jan 2024 03:39:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd94a910a6d687fc7621b3af4657f78c1208a07fa463f30e2ed002dadb7e021`  
		Last Modified: Wed, 17 Jan 2024 03:00:10 GMT  
		Size: 189.8 MB (189834377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569bb1e89b3578ee5ed1345e50e804d7148e85a1946d551ed89e2b171122d5ad`  
		Last Modified: Wed, 17 Jan 2024 04:10:18 GMT  
		Size: 244.0 MB (244018690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cbb679b710525afe819a16b411ffcb30de966e7c656855544c8fe69393b83d`  
		Last Modified: Wed, 17 Jan 2024 04:09:57 GMT  
		Size: 195.0 KB (194969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7727858bdfc832f7f9c3ebf0a430e4855dbab0514764b3827963e3b9ce68fd5c`  
		Last Modified: Wed, 17 Jan 2024 04:09:57 GMT  
		Size: 781.8 KB (781812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:0a139d12d2f17b0766e774e3cc0824e45d21293cd4ed04a0ec541bf4c7a09a7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573878887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8dd827b84ff596d845be495eb4b2bab395853228c91de422c6fa9d122b079c7`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:50 GMT
ADD file:5ec37a8451203256eba8b114f21ff297f9b2e0b420ec7f0c50658a448ffc8f7b in / 
# Thu, 11 Jan 2024 02:38:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:40:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:41:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:30:11 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Wed, 17 Jan 2024 02:30:11 GMT
LABEL org.opencontainers.image.version=26.2.1
# Wed, 17 Jan 2024 02:44:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:44:43 GMT
CMD ["erl"]
# Wed, 17 Jan 2024 02:44:43 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Jan 2024 02:44:50 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 17 Jan 2024 02:45:25 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:9b04188f89c4a7eaa549c59c16834ec81012244afac6c52196bafd2cd4486602`  
		Last Modified: Thu, 11 Jan 2024 02:43:42 GMT  
		Size: 56.0 MB (56046385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75db71c7ec6ec0e64a32b92dfa4a3127698f085f1df99e2c6187447f2433d41`  
		Last Modified: Thu, 11 Jan 2024 04:43:06 GMT  
		Size: 16.3 MB (16269099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33bceb83dc9fcc65d74c8e79da8ad46a7b1d7378b402830b29afaf04bd04df1`  
		Last Modified: Wed, 17 Jan 2024 01:51:38 GMT  
		Size: 55.9 MB (55939768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82eb38b7dd14b4951198e5118a540832cdd8e5d77970d1b72b7fa2e5578c545`  
		Last Modified: Wed, 17 Jan 2024 01:52:24 GMT  
		Size: 199.8 MB (199825169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ae963ddb22e095de305a1474e3c4668f4661807648452d5056b52b39f21b3`  
		Last Modified: Wed, 17 Jan 2024 04:11:54 GMT  
		Size: 244.8 MB (244821828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d26d066fa97dcb83de34cb839cd462b87c1518d3b58acad4bab20a0862d9cf`  
		Last Modified: Wed, 17 Jan 2024 04:11:11 GMT  
		Size: 194.8 KB (194826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b501ad455fd4b26ffcc2e759ac5d39b26b54e15e1d8c3a4261aca1e2b9acc7`  
		Last Modified: Wed, 17 Jan 2024 04:11:11 GMT  
		Size: 781.8 KB (781812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:fb50a304bc2aed4372e8668663e1c90a24583d76876ae9e318ee95f90233755f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528158077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7cbc16c51176b41dfc3604e969f97776163d40975f1352e92e07bc7846a14d`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:12:20 GMT
ADD file:624f588d8cd5ac8189fd789968263b87196e86dd1d90debb6c5261b515ce80a4 in / 
# Thu, 11 Jan 2024 02:12:26 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:56:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:58:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:03:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:45:43 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Thu, 11 Jan 2024 03:45:49 GMT
LABEL org.opencontainers.image.version=26.2.1
# Thu, 11 Jan 2024 04:23:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:23:15 GMT
CMD ["erl"]
# Thu, 11 Jan 2024 04:23:24 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Jan 2024 04:23:51 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 11 Jan 2024 04:25:36 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:80f37a7fb2daee9d24c2a15489b4104fd20747297db13799a90f5f67e3a79154`  
		Last Modified: Thu, 11 Jan 2024 02:23:35 GMT  
		Size: 53.3 MB (53288875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b4dc197845232bb31ea262c56891dac2feed854c3f09a70f819ec88464da5`  
		Last Modified: Thu, 11 Jan 2024 03:27:38 GMT  
		Size: 15.5 MB (15530460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59890619bfa1b3a44a1fa12832ed454cc0239ce6f72b3b1ea247f5ae69581690`  
		Last Modified: Thu, 11 Jan 2024 03:28:23 GMT  
		Size: 53.3 MB (53311496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702d400c28781956cb62c0589f91eaf7b9709793da38a127c329b51cf7e086c`  
		Last Modified: Thu, 11 Jan 2024 03:30:21 GMT  
		Size: 179.0 MB (179020874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103126601cb9f69e6d9c1f85b73ff5ccaa0a8fb7dcdb7326da819df0c12fa8d3`  
		Last Modified: Thu, 11 Jan 2024 06:46:58 GMT  
		Size: 226.0 MB (226029732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f30f9bff247f4202c30b073fa1902c6f426c7d98022aaefcdcfa4c9122b20b8`  
		Last Modified: Thu, 11 Jan 2024 06:44:47 GMT  
		Size: 194.9 KB (194903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf43061a376821ff9e85deb581dac7800dc75b7e9a3d9009a687697220b31756`  
		Last Modified: Thu, 11 Jan 2024 06:44:47 GMT  
		Size: 781.7 KB (781737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:8c0a57e1043034125788cb7f9dbad92f94be25ed2fda213867ea518ae4c94896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.4 MB (578428655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a018c18c9b83339106e33787dfaa2c870d2bbd89c640cb51e68efedc7d8e5da4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:41 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Thu, 11 Jan 2024 02:34:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:08:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:11:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:23:15 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Thu, 11 Jan 2024 15:23:15 GMT
LABEL org.opencontainers.image.version=26.2.1
# Thu, 11 Jan 2024 15:31:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:31:39 GMT
CMD ["erl"]
# Thu, 11 Jan 2024 15:31:40 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Jan 2024 15:31:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 11 Jan 2024 15:32:17 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e705cb61758280364899cd162b2510b2a119833c02f501318b83950af12d2`  
		Last Modified: Thu, 11 Jan 2024 07:24:33 GMT  
		Size: 16.8 MB (16767158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1974dca40db9a6f34527c91c9763d250d18f0d45ff29c835a706bf5dab4025b`  
		Last Modified: Thu, 11 Jan 2024 07:24:52 GMT  
		Size: 58.9 MB (58874114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfc24ab58b746d3120b5d6222c1288b69e607238900f854b55e6bd80ad14867`  
		Last Modified: Thu, 11 Jan 2024 07:25:28 GMT  
		Size: 196.3 MB (196277076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc60dfde2bc6910477615c0aafc6e466439258517154eb73cbff2da336825252`  
		Last Modified: Thu, 11 Jan 2024 15:49:20 GMT  
		Size: 246.6 MB (246603874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f816df1968d35cb94ddb5a9063365b9631f5c50c7b8557057b6b84b20baafd1`  
		Last Modified: Thu, 11 Jan 2024 15:48:46 GMT  
		Size: 195.0 KB (194965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7a186c28721881554d70caaff5aafaa7d1bce4561aa11202a63f463edbf3b0`  
		Last Modified: Thu, 11 Jan 2024 15:48:46 GMT  
		Size: 781.8 KB (781806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:e4434c5499ec685abbd079d619c141c90e33b3bd62a44cd01d2cd620725db9fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533208018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b7e590b478974075ad0b7959445b86dd79ab764ae596a5a6506b5df462b76d`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:23 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Thu, 11 Jan 2024 01:45:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:12:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:13:27 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Thu, 11 Jan 2024 05:13:28 GMT
LABEL org.opencontainers.image.version=26.2.1
# Thu, 11 Jan 2024 05:21:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:21:31 GMT
CMD ["erl"]
# Thu, 11 Jan 2024 05:21:31 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 11 Jan 2024 05:21:35 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 11 Jan 2024 05:21:55 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d30f97393df8af87413ca6aa015986e13ab489522ffe9a065961b2ed0f9352`  
		Last Modified: Thu, 11 Jan 2024 02:22:01 GMT  
		Size: 15.6 MB (15642723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0e4599f9ae7a417945830efb8a901aff78d46ca9cfb95700e3b83352b2211`  
		Last Modified: Thu, 11 Jan 2024 02:22:15 GMT  
		Size: 54.1 MB (54070654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30707a1a3dd916813109d545eca2f2cfbf3b66ff818a081a1fde88388e8c0655`  
		Last Modified: Thu, 11 Jan 2024 02:22:43 GMT  
		Size: 172.9 MB (172920010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8448809b31a3ecfc683001ce1c544da1813e3ee82d47adf94451fee90786db82`  
		Last Modified: Thu, 11 Jan 2024 05:51:56 GMT  
		Size: 236.3 MB (236301705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694276312cb962d4b0b6806f678103b8e3396b53c9cfb27c83f38da4c5ffef80`  
		Last Modified: Thu, 11 Jan 2024 05:51:30 GMT  
		Size: 195.0 KB (194992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c03f4dfdc32c3151a906251e9813d12bfceb9857433ab66637e68e54de3d73`  
		Last Modified: Thu, 11 Jan 2024 05:51:31 GMT  
		Size: 781.8 KB (781809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
