## `elixir:latest`

```console
$ docker pull elixir@sha256:31ec349b65c884b78dd85b827a7827963f0900f81045aaf2d4e430bd24df8021
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
$ docker pull elixir@sha256:caff9b4a8ab5678dfde9d3f81b60eef34800e7ae7e577a56fe612545ec391d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610586381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a522474d2b8bfc3fe8a2be288055fc5a765c5c8728b6ff1947d902b82409cddf`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97521d3609ee88b7f54e63f754ad2aad4041433b1752dec0c5905f0a47ac7e51`  
		Last Modified: Fri, 27 Sep 2024 06:15:04 GMT  
		Size: 253.4 MB (253427782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa4eee140d7a37b32b246ae9fc12b1d000b453e930c94ba423a969cb642251d`  
		Last Modified: Fri, 27 Sep 2024 06:15:01 GMT  
		Size: 195.5 KB (195485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84eb4d868e1e686a4f7fb4b3e5122adec50b8c4a3a4f0c589137cc907c5ec5e`  
		Last Modified: Fri, 27 Sep 2024 06:15:00 GMT  
		Size: 805.8 KB (805802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab326fbd8abccf3c3b67844164b0c96e0485f7d6b3bc6c1c7117bf4fff979b`  
		Last Modified: Fri, 27 Sep 2024 07:04:34 GMT  
		Size: 6.9 MB (6891247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:99c9e577cb7cd97f62983394f279a85a6efeab80fe9ee2c0983a63478a9cd3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23323845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1452af4a852ec61a00915a4418592875bafdcf7d861acb20152b485e51d6223e`

```dockerfile
```

-	Layers:
	-	`sha256:370e3165ada1cc474b749cfa529d88e279662f3033b9c702a5dce20212a6d22c`  
		Last Modified: Fri, 27 Sep 2024 07:04:34 GMT  
		Size: 23.3 MB (23312586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0c06314b953bc763bdc46ee1a02bd2c6a1fe19c176b6b39ca2112899900376`  
		Last Modified: Fri, 27 Sep 2024 07:04:33 GMT  
		Size: 11.3 KB (11259 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm variant v7

```console
$ docker pull elixir@sha256:e9d72e68de3eb3de43dd767f159fbac0aef7634e51a1a5845205196520c4ee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533077706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11e0713bc5b71e338829b5d8b0d05d26e9dd93ea83746f20123a1b7e2b261a9`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e33c21a5811a5788a8afcde716c7d94af4fdd32bf0c0ba5da77909d466280c`  
		Last Modified: Thu, 05 Sep 2024 18:44:31 GMT  
		Size: 223.6 MB (223641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db901be614c67479c2597e06b66eb40b3c202b1063e3fe54a52c3c6e90adc0b0`  
		Last Modified: Thu, 05 Sep 2024 18:44:27 GMT  
		Size: 195.5 KB (195494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6c3100ca12a2157c223c3bca2c00528772bbc4c53a6b4f7ca34f3f2e65d725`  
		Last Modified: Thu, 05 Sep 2024 18:44:29 GMT  
		Size: 805.8 KB (805803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2537367d8865a8aa1fefd2f4e8892fe31624d22f169daf5c0995561566048ae6`  
		Last Modified: Fri, 06 Sep 2024 05:53:15 GMT  
		Size: 6.9 MB (6891236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:a544f8a7afc7578a338ea7634b4034f5ba57db8b0516ea5de6b3fd78092ab23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23132589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a991345f0cb0120ce7d1dfca2d50a3d45727ba299595060c784bc4b027f4f63`

```dockerfile
```

-	Layers:
	-	`sha256:8d6ed896b6e39bf1a63b6b4915ad4a7df2bdf4a6ee2090342be18d0e7e175ef4`  
		Last Modified: Fri, 06 Sep 2024 05:53:16 GMT  
		Size: 23.1 MB (23121189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b7f81dd5ef53bc7f0d22c3107e491d84ae9d41aec113c65993387649d42b69`  
		Last Modified: Fri, 06 Sep 2024 05:53:15 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:def7c9329c816d4193e3996ee1c15cc0dad5f3db4df9c8017dd5f2438c804e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.6 MB (594631457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c94a2c862adbd7ac7b1e4f2fe40cac90551be20e1ae5e71bb5da700471599c5`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a348c2a8d94613f34ce7d0ac4fd4e51800d8f4aa8a0bc9347fe5c8436b4c3bd5`  
		Last Modified: Wed, 04 Sep 2024 22:08:46 GMT  
		Size: 202.7 MB (202652028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af186bf7a729b2643b9a7d86ca352a9148d8fcf9dd9e8ab2d72e37ff74bb3941`  
		Last Modified: Thu, 05 Sep 2024 09:07:38 GMT  
		Size: 246.9 MB (246909547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecff3b9133f53f90e0dc9ca5641bcba55ee3d1541cacbafeed4dfa20ff9dab7`  
		Last Modified: Thu, 05 Sep 2024 09:07:35 GMT  
		Size: 195.4 KB (195387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270d491c3df53e14c77d9db5859e28a40c982e799ac2387691c67440d9a274fd`  
		Last Modified: Thu, 05 Sep 2024 09:07:36 GMT  
		Size: 805.9 KB (805865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0a9605cf5da91d6e2b2e21d42d14f3a413f28336268c4d82c32864eeae9717`  
		Last Modified: Thu, 05 Sep 2024 21:13:15 GMT  
		Size: 6.9 MB (6891261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:00440bba9276e3beac9f02383fd1dd797d72eed1fa8f05b950d4df240dd20257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23357040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5829fcbaec7cb1cf61b61b9d8b746ac2894fa9e8b08f24f0f9aa1942ec0890b5`

```dockerfile
```

-	Layers:
	-	`sha256:3a439decaa800d85cf4309e2d4a87efe092bb90327ffc1b9b3a0b37fed7f9962`  
		Last Modified: Thu, 05 Sep 2024 21:13:15 GMT  
		Size: 23.3 MB (23345323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90139b8d0dae4bc30e2ef5d517100a0dc2f1145499af0f000ea86d916deadf2f`  
		Last Modified: Thu, 05 Sep 2024 21:13:14 GMT  
		Size: 11.7 KB (11717 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; 386

```console
$ docker pull elixir@sha256:c85ca787aca4d4a0c012bb428deaa7582b52e009571744f0b774c331a42d690e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606404063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b8993a98cb9911779cd2da7a2fb5c1d0443e8b6b42d649981f5d16bed23503`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8de3627474d7a76f3a8963a53ec861d36911f9771b6c906652a0287d68ce200`  
		Last Modified: Fri, 27 Sep 2024 09:08:17 GMT  
		Size: 246.6 MB (246646163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acd9ff0da9ccdcfec7be9b2b4730e4066279737802b214d6c25e31f3b910fc`  
		Last Modified: Fri, 27 Sep 2024 09:08:09 GMT  
		Size: 195.5 KB (195498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394dece6d67b7275459db75c1ead72272172b75934affde66a409ddcba5b28`  
		Last Modified: Fri, 27 Sep 2024 09:08:09 GMT  
		Size: 805.8 KB (805795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b56aa1f08450a01e7700316720baec1af0de6b96755c0ab8d38d673b370e396`  
		Last Modified: Fri, 27 Sep 2024 10:02:39 GMT  
		Size: 6.9 MB (6891262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:f4e79b3f317c7be5a7f1e837f194dbea70d7864dd0cfeeb3dfa77246514c363d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23292275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bfc8af1dfa423c04b33c9f709c66436682d2e43b373307c9ee0d50cfa8e9f7`

```dockerfile
```

-	Layers:
	-	`sha256:c4ad5b3b881c1c00aad158a5995fa04ecba4dd57bacebcc65e089644e18c1061`  
		Last Modified: Fri, 27 Sep 2024 10:02:39 GMT  
		Size: 23.3 MB (23281057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e06edd3091a583414f1a1c3c4ec522ed67935763858d6c3aab08d8f8f0f67d`  
		Last Modified: Fri, 27 Sep 2024 10:02:38 GMT  
		Size: 11.2 KB (11218 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; ppc64le

```console
$ docker pull elixir@sha256:e57ba246fb24dbad8342a203c1db6df7e5e055bf8299d4e34ed4cbc61f78658c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.6 MB (620640857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95e2295758160d02ea6eba13bdc6f80cd2db32f5685e3d1589d5a4f74708814`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161dd3959faa2f30fc05f50f11de2ff1ae36632b37e08822b40bdd9e596b6ad`  
		Last Modified: Wed, 04 Sep 2024 23:14:38 GMT  
		Size: 214.3 MB (214285993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587ed22b52affca7c1f3dacb830d39effeb9a93aae67a98fa9ddd1057f76143e`  
		Last Modified: Thu, 05 Sep 2024 14:38:03 GMT  
		Size: 249.6 MB (249609701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc790570d44f10abbf116fb771a0f3d8b82d80ba7e99c65e2079fbce568dc63f`  
		Last Modified: Thu, 05 Sep 2024 14:37:48 GMT  
		Size: 195.5 KB (195484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e32720080df24d7857a777fca2c85de82c229204a83456b5fbc5a33138b92`  
		Last Modified: Thu, 05 Sep 2024 14:37:49 GMT  
		Size: 805.8 KB (805804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80243622f9d2b168d4f2ada0064dcad09072b8439d7c245b91c6ddb5899ba07a`  
		Last Modified: Thu, 05 Sep 2024 23:48:10 GMT  
		Size: 6.9 MB (6891266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:de2b3a642c623b5aa2ffe7e6d1f2c7ac0335f525591a82b0130d9fc1328252dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23272430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ad1064937da7390b16e0dea40170a290a85ed87d371e43ebfb590e23b57907`

```dockerfile
```

-	Layers:
	-	`sha256:0c85bd989b03593f55149f507159b3c9690130178af411320a4d6e05bcfd2f7b`  
		Last Modified: Thu, 05 Sep 2024 23:48:13 GMT  
		Size: 23.3 MB (23261066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e47d363513a200fbce9f28f86ef9b10a8bbd5c69d182a19a4769015858a0893`  
		Last Modified: Thu, 05 Sep 2024 23:48:09 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:latest` - linux; s390x

```console
$ docker pull elixir@sha256:24e5a7eda1d38f7304b7da34836c9ffad3318e45888b0407c9cab4c51cbb0769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564416307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f008f6f497b424a19d686f8675dd86ba14d3d45117cd1ef6c1f2a7b5ecfaff45`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837216ffc2cad6e5167bbe28293d10e21f258e3d8c77b1249ed4cd57246d0f7e`  
		Last Modified: Thu, 05 Sep 2024 00:00:03 GMT  
		Size: 24.1 MB (24052111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894819abf6316f9b38eecbe542cdc236074b267f2f7b83410ab1057aac88398b`  
		Last Modified: Thu, 05 Sep 2024 00:00:18 GMT  
		Size: 63.2 MB (63150669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18612060b30c9f1db538f5e79e46ea0534fafb1c79e714e74e11a1b56e69c56d`  
		Last Modified: Thu, 05 Sep 2024 00:00:45 GMT  
		Size: 183.3 MB (183289806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c18adf30efbb8967170d842c97c3ad37ba88801364f1b4df75f78c9b3f92c5a`  
		Last Modified: Thu, 05 Sep 2024 16:39:07 GMT  
		Size: 238.1 MB (238091959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ee9c60a666f3071eb822c7f2fb4b89c77e863552e2e83128220c44b726609`  
		Last Modified: Thu, 05 Sep 2024 16:38:57 GMT  
		Size: 195.5 KB (195489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94575f5108ba3811275c6d8a8a0256b2a0e08c0fd0ba19c2b88c36426ecf7d67`  
		Last Modified: Thu, 05 Sep 2024 16:38:57 GMT  
		Size: 805.8 KB (805804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70663e2bdc789f8da3144418bbd2d7b0037baf2bc7cde09936f27d9f042e5c3`  
		Last Modified: Fri, 06 Sep 2024 04:05:30 GMT  
		Size: 6.9 MB (6891192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:latest` - unknown; unknown

```console
$ docker pull elixir@sha256:4f58e9c056955b96091caf5bda1378ab2dfb50107bfcdde5fa49118004cde72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c49a4a9c488909d7b2fe7d23918f00b75a9e3fb305ccf9ab4dd0802327e9b3`

```dockerfile
```

-	Layers:
	-	`sha256:58bc9d0cd53b52b985652b01134ad50fb80506ad84b9f4b6c815144278a74625`  
		Last Modified: Fri, 06 Sep 2024 04:05:30 GMT  
		Size: 23.1 MB (23079869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9211b08dc5c502bc04c64241b9f4f8ef8bc94114a684c4ca47cf77721c3c21d5`  
		Last Modified: Fri, 06 Sep 2024 04:05:29 GMT  
		Size: 11.3 KB (11308 bytes)  
		MIME: application/vnd.in-toto+json
