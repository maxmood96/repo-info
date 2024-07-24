## `elixir:otp-25`

```console
$ docker pull elixir@sha256:87fc9d90b96572fd48fa563dba6f244c8cc0b3f82ea814d5b5408490902bd121
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

### `elixir:otp-25` - linux; amd64

```console
$ docker pull elixir@sha256:9b45e80f40d7b3001b36a442099f3df06bff6fd0da0bea3f860046d2128b9eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.3 MB (580271819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a30e0517c059d4dd61d7cb317c4dbb4e8ed8be1b279e0580c4db1ece6f97c80`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a749598db26b14c74d5372d83b9d87e1e742887170bdc8fa828cc0bb40cb3b`  
		Last Modified: Tue, 23 Jul 2024 07:32:15 GMT  
		Size: 249.8 MB (249819109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc927a0c3261c76211931c1f07077a2a482ad3f14b6d4320985feabdf99ff6`  
		Last Modified: Tue, 23 Jul 2024 07:32:11 GMT  
		Size: 198.6 KB (198551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f969ac8fb99d00a49ab9940315d38378f4beb2c2d83399758e224886e73d7925`  
		Last Modified: Tue, 23 Jul 2024 07:32:11 GMT  
		Size: 803.9 KB (803866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c25a8606dbb26c6f68a9e8d4d0016e46ba201078f0919db202798b015cab39`  
		Last Modified: Tue, 23 Jul 2024 08:14:15 GMT  
		Size: 7.0 MB (6973718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:757f97a6c52c49e888ebe8987c36bd5aebb23e66e28976fa8537f801b2bdf6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22819571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d2293e72548131a63734c9643de9bd37202a74532ba7126eda5cdb97fe67c`

```dockerfile
```

-	Layers:
	-	`sha256:48405b1f29d8269a6311c278f65e6b217d4a0f1e837adf4c1f65a2a6c77e5846`  
		Last Modified: Tue, 23 Jul 2024 08:14:15 GMT  
		Size: 22.8 MB (22809185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac35270201e7ea131a7f04aec54c9cb988b8b93a34c8a87920df33943bc94fe`  
		Last Modified: Tue, 23 Jul 2024 08:14:15 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm variant v7

```console
$ docker pull elixir@sha256:49f4c9c2194e7554936df9a3872e4dede564df612eeee7efda54eeeb3dcf9a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.5 MB (515507862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425fd60f847212430137528776bfc0dfe32e6a6796134514bd75081af7283462`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d987a91174c226a2bbb5227e9f01d49c50d2c154f8059b46e125616d2f523c2`  
		Last Modified: Tue, 23 Jul 2024 13:22:57 GMT  
		Size: 224.5 MB (224549857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6880c8f6ea9248a212f413fa372d701ab5ff63b3da4cf2e0f02a4e64dfbac6`  
		Last Modified: Tue, 23 Jul 2024 13:22:52 GMT  
		Size: 198.6 KB (198579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e99999cab73696d9a38f3d884825f7da78aff081665549cbd150ec3b87da75f`  
		Last Modified: Tue, 23 Jul 2024 13:22:53 GMT  
		Size: 803.9 KB (803871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf5cbf099b913e158ad803644c75b605e06346b6f5813528febb20c859e919b`  
		Last Modified: Wed, 24 Jul 2024 17:43:40 GMT  
		Size: 7.0 MB (6973767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:f07784240a26205194f3949a695eab50a96125e53e1c963f477b8efffc15805c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22628594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112b50edf2783662d6d64d41d5408f61e628b7348e52f49202621c84f319547c`

```dockerfile
```

-	Layers:
	-	`sha256:c4e31aa312c2c04a281bf9909fdc170ea502c1071865c6b8bd046d77b8773a26`  
		Last Modified: Wed, 24 Jul 2024 17:43:40 GMT  
		Size: 22.6 MB (22618091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8223f0d5ebad7d7f2d892e36607c6e872f510db6fcdadadd43fb43aec2fc7531`  
		Last Modified: Wed, 24 Jul 2024 17:43:39 GMT  
		Size: 10.5 KB (10503 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:858af34c8ac38f34d406bfe44b9a46260d9e51e72402a33d8705cafd9f748675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566235483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b16576aad497e7d5290cd4c02a67391daf7a3ed94ec07d2ce9f1f5ed65474a0`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa85101261af7a4a09326746d17079ebbb84fc6b828063813bcd3b8ee8a4e0`  
		Last Modified: Tue, 23 Jul 2024 14:42:24 GMT  
		Size: 244.1 MB (244119095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2468eb01e84d92ad702f97d1913ecc068c412a0a294cf5ea528e1158453ef420`  
		Last Modified: Tue, 23 Jul 2024 14:42:21 GMT  
		Size: 198.6 KB (198563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c399df6e218deb54484053254d800fc2b6ec1c7cb52c802b8cc82702e0d443f4`  
		Last Modified: Tue, 23 Jul 2024 14:42:22 GMT  
		Size: 803.9 KB (803871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41c5b4e212c49c5b4d844a2c6fb9c4c20be6bb7fb1db4b9668f04d9a00d1c53`  
		Last Modified: Wed, 24 Jul 2024 14:30:13 GMT  
		Size: 7.0 MB (6973709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:64959e2c62dec3ec882eca70783fdc4c1b9da9e11b645d5e16081743ada1cd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22830028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b42e11a0b1cbed07328d9601ef27df883f660211898e8773a4b81ac11e20178`

```dockerfile
```

-	Layers:
	-	`sha256:6fb8e96ce844e7036835661ad0d917cd1b2e67a6761fb521f7b4f76ede40e0ff`  
		Last Modified: Wed, 24 Jul 2024 14:30:13 GMT  
		Size: 22.8 MB (22819220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97b3d869da36ae5172cf3864e2000d81a0bb811ca2e7beff86aa389ef8a2b28`  
		Last Modified: Wed, 24 Jul 2024 14:30:12 GMT  
		Size: 10.8 KB (10808 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; 386

```console
$ docker pull elixir@sha256:86584770dd07209ec526d42561a31869ef405b0c643b284edc24d82598a0edf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.7 MB (581725427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4dae589ecfd2886b0ef6d381d317b55c1e7bc4d928daad2578db7162a83cd9`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30928a030df8a953adc83c67e2ab17a4c5048cc04287762bc9e03e269fe7c3dc`  
		Last Modified: Tue, 23 Jul 2024 04:51:04 GMT  
		Size: 199.9 MB (199944219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59319c922c27cc32a55005a8a0c5646fe1b74d0303ed0b4da0737349394e977c`  
		Last Modified: Tue, 23 Jul 2024 06:25:39 GMT  
		Size: 245.5 MB (245535254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3fc96a1a94db2e49a53ba5facce0454806821be86d2e1deabeefd83a972236`  
		Last Modified: Tue, 23 Jul 2024 06:25:33 GMT  
		Size: 198.6 KB (198551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e67ff9edaaebfef2696c5db1b07b7df250415cbb00210e4488b944495f652`  
		Last Modified: Tue, 23 Jul 2024 06:25:33 GMT  
		Size: 803.9 KB (803871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa93f27c4fb0af97090c88de08421ff98d1a730accb112ab313f878cb522d2d`  
		Last Modified: Tue, 23 Jul 2024 07:30:02 GMT  
		Size: 7.0 MB (6973773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:1efb4199e9c483e2ffaedb42fe777ef93507fd5998832dc12b772b47a046c685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22807349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4649beb33768d5f1ca081394ff4708d66d68b134e1bf4a10eda920bc137dcc4f`

```dockerfile
```

-	Layers:
	-	`sha256:5e7ad829db6ad35a323e57869d03bc9af7b1aac6c4664aa6986ddcea01fa2748`  
		Last Modified: Tue, 23 Jul 2024 07:30:02 GMT  
		Size: 22.8 MB (22796989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7a4cd651f5d814e145b4eac0eaaf25854d66cd76d3ecd4d64d1b8d270bd02f`  
		Last Modified: Tue, 23 Jul 2024 07:30:01 GMT  
		Size: 10.4 KB (10360 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; ppc64le

```console
$ docker pull elixir@sha256:2a3c5d30b399be4a5d1035d3e3d539d2ed5cca1a79542bc022a2cc7f63d06ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586586948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076611710888a38855c3a5646337709f8c7de56cb2963ade9e69e60d2e41b746`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb19abc545d74f78960aafde19caa312889b7538ab94844af6061d8ada67a311`  
		Last Modified: Tue, 23 Jul 2024 13:25:15 GMT  
		Size: 247.6 MB (247621276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b06b0435343f0373a40234eaf12b6b63213f821a4553534dee6b2327291dd`  
		Last Modified: Tue, 23 Jul 2024 13:25:08 GMT  
		Size: 198.6 KB (198562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bce2e3c593f276bac769151e3a251e3f8259fc002c4f09865047d61223e03e`  
		Last Modified: Tue, 23 Jul 2024 13:25:08 GMT  
		Size: 803.9 KB (803871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776e16cfc119f7efb37d73febbf23d87fc3ed71fbefec0f6ddb47450e2e6c45`  
		Last Modified: Wed, 24 Jul 2024 18:07:14 GMT  
		Size: 7.0 MB (6973692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:3bfbddd44131e084037f784340456be65ff41cc570d6793400548ae54fa1b7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22774024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6d69fac8b85493150b299ef1b474495eaeb21f4b9e6ba631b7458fd0492c85`

```dockerfile
```

-	Layers:
	-	`sha256:9013cb9a8f5a1ded476a36a26db71c0288ade96ccb64228f9d4938d32f27ae3a`  
		Last Modified: Wed, 24 Jul 2024 18:07:14 GMT  
		Size: 22.8 MB (22763552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d03705a06fc0f9ef70054821ac2dd85942bd6b1b29ebc3d4d64b4274fabd0b7`  
		Last Modified: Wed, 24 Jul 2024 18:07:13 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; s390x

```console
$ docker pull elixir@sha256:a8fb011ca3884154c856c13d1d6b9c62cf63090ece155ec62c42b325f4970b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.1 MB (541120521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fbdfce9680167fa37dafe01842f501873c9451dd32423f2df787f3a9a1ed76`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Sat, 04 May 2024 12:59:04 GMT
ENV REBAR_VERSION=2.6.4
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d980f4cb602f9d9df16f79fee3e081d5827e12ea5fec8871cd0b0ec49adc79c6`  
		Last Modified: Tue, 23 Jul 2024 09:53:46 GMT  
		Size: 237.0 MB (237044906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d05be846274b75d9a15d98ddd96c0a033dc6bd81c640192326fe3fcb895fb`  
		Last Modified: Tue, 23 Jul 2024 09:53:43 GMT  
		Size: 198.6 KB (198557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6abff53a37ac93d5885b466a8186bf82542396234089a030f1f5d40f7268a7`  
		Last Modified: Tue, 23 Jul 2024 09:53:43 GMT  
		Size: 803.9 KB (803871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc23fa357387662b2d5fde566175400ec8c4f6925a465049ff941194cccc8f6`  
		Last Modified: Wed, 24 Jul 2024 14:55:24 GMT  
		Size: 7.0 MB (6973723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:87f6674975728e16c51bdf40ea1e26e8154ab19e66070282090b3e1334b5d0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22608248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cecb1c1ecf72d8ec69cdd9a223f4d17d01d21f6b7c722ba8f3c1c43e0cc82f`

```dockerfile
```

-	Layers:
	-	`sha256:4bb720bbaf00d6fcf577b331889ea6cb02c41bf0cbfe428375c502b1358e3948`  
		Last Modified: Wed, 24 Jul 2024 14:55:24 GMT  
		Size: 22.6 MB (22597813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85c900ec6d4484efba12b673795df65818cd4811dd110d33f6603a14249011b`  
		Last Modified: Wed, 24 Jul 2024 14:55:24 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json
