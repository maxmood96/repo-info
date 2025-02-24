## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:7acfd2a19d7238da65adac1d3beb221933f4708171a6d2f5dd77c3aa5b62f49e
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

### `elixir:otp-27-slim` - linux; amd64

```console
$ docker pull elixir@sha256:434cafda2c497b84030a2e54b7c54d46a5a02c1eb6bb220a8f10029e7da9e17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132316006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa09c90a73efa0bf9ac8e6161c9ee7cb0931070554c12ed786409f3359a02fd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5227875e6824e5fc5bbc8d0d62212f98dfad720cd1673a1a9cd184768e7a235c`  
		Last Modified: Mon, 24 Feb 2025 20:31:11 GMT  
		Size: 75.9 MB (75921882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a401644b1ddb08634696b57944f76af5ffb8274a1dc182e2c7cc2ceb08ddd92`  
		Last Modified: Mon, 24 Feb 2025 21:28:17 GMT  
		Size: 7.9 MB (7914437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:58c1624c307eb12459a2c5626899f1e9478d4d75678cbf568d1061a331d9bb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ed73d28963412f17adcabe282d5d0cdc10255fff3926817fa89b3ba9442c8b`

```dockerfile
```

-	Layers:
	-	`sha256:ee1e7310b85d7ce3d5cd4ffafdc2bd7ba7b71e27a317e7acf7d9193e7eee2285`  
		Last Modified: Mon, 24 Feb 2025 21:28:17 GMT  
		Size: 3.7 MB (3668146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124a57e2d9fa52757843d4397007fcc27c5ac94ce298b8d54ffe18b05266c72d`  
		Last Modified: Mon, 24 Feb 2025 21:28:16 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:b096b2a10eee0e5b2c67540dc1e4815ffa02d3174d79bb286a14afb23e5efcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117134362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f284bf0c71d512cf7000f869c1e124ef6017a4a4147271ea41303cf175fa004`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8404bbbae6e990a43d04ca451802ccde5a2b7ecfe4d90c3a3b75c6053adbf2`  
		Last Modified: Mon, 24 Feb 2025 20:53:03 GMT  
		Size: 65.0 MB (65036518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1e85e0810fd8e0e89cedcce86340b2cc86b25e6fcc91d0f7b0fc44411c9556`  
		Last Modified: Mon, 24 Feb 2025 21:31:06 GMT  
		Size: 7.9 MB (7913792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e244486e5f2c91e4b92bb25cb313d2c27f5b974724c4230c203f2e8e6e540d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d54d947f1cdf2757df2cbba5f98978963577abbba9f2e04d11e218ca438998`

```dockerfile
```

-	Layers:
	-	`sha256:f29e6ff9c88a8876ceae73a43b47d272b503cb5543501f10c63e6769b293ed59`  
		Last Modified: Mon, 24 Feb 2025 21:31:06 GMT  
		Size: 3.7 MB (3718219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8031f74dffafa6f209181aa02848dff475b2a135bb8a15b3ef27a43387548c`  
		Last Modified: Mon, 24 Feb 2025 21:31:05 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:e57e516776943dcdd1448e4a39c78178ce4f7e0482069a68a4614d485c4156cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129876473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd04b7fc6d6deabc54f6cd2ab5ad91bfc48db0530d414a1fda60c1f53046b7b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a032e43e175cf21ddb7645541ac21e0c1688a13a2cdc2e970900afe371b85b80`  
		Last Modified: Mon, 24 Feb 2025 20:54:37 GMT  
		Size: 73.7 MB (73655586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd2acb665ad4462f35fb0b2c78359a3281a3d5c4615f6875087aac04bec2d01`  
		Last Modified: Mon, 24 Feb 2025 21:31:22 GMT  
		Size: 7.9 MB (7914334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f3ab356f84d3cce249837481f3ef4a09d26673e308b739e77fddfdafb3d87b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0eb8e41f1b647723e0c81f9b36ffdc315214907b2ff71f96888acc4a1079d6`

```dockerfile
```

-	Layers:
	-	`sha256:13f6bff3bb7469766cbdb126c296eadcb1faee27bc21cd42b4a15dc4b0c38928`  
		Last Modified: Mon, 24 Feb 2025 21:31:22 GMT  
		Size: 3.7 MB (3716255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39961faa18fc96bc0cf99dba5f595640f60ca179b3d1d02a38c72232e0f2402c`  
		Last Modified: Mon, 24 Feb 2025 21:31:22 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:707e4be98d45786979a8b2e0057dd99c90df36dfb633ac997f16d8e6ad9818da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123448012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b41551a1db460b46053d17287f948935a6b1dc82c8b00a998341a14d6be33da`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd926542744800e977a0ba4cfacf34c55ef8f91934de46448456c94b0709ca8b`  
		Last Modified: Mon, 24 Feb 2025 20:31:22 GMT  
		Size: 66.1 MB (66076699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90ad3466ab96a9e97c721a903aebc4fa11ff035c8c647d346a7c89c8fa7a6ef`  
		Last Modified: Mon, 24 Feb 2025 21:28:57 GMT  
		Size: 7.9 MB (7913857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e16e7fe806264658682e2a74a2a9766e7382f631204813b4bf1cac90a7d6ffc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3675893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523e5c7092bf53a53f69f4adec2c2bd544f1da5b35d1aa3a66dcac0c62388df`

```dockerfile
```

-	Layers:
	-	`sha256:2289bee5821d15a97ffb89d3a0a1db5fa072c5e183e43f9c327b6d74d9dc99bc`  
		Last Modified: Mon, 24 Feb 2025 21:28:57 GMT  
		Size: 3.7 MB (3665256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7015b44136b161b485e827773064627eccc2368e4f3819ad0e78ec9fb7e6e76b`  
		Last Modified: Mon, 24 Feb 2025 21:28:56 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:e5f8b2e7fe0f5cf7da97ca6e3b993364b1adca514c21e5feaeefe7e29cea516f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127392982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b0dbed655ffe5903ab06f2aa2d6e1d0160eb7ed64d25f52d6469e0e0996080`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d6a2eb89be636bbadabfd4dd6af76dbfc151ba4fa8cead70b08c3bd55704b9`  
		Last Modified: Mon, 24 Feb 2025 20:54:36 GMT  
		Size: 67.2 MB (67165694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40f0fc2ba49a3d46e631a47ccb39873ea1014bdd3cee6c7c7c2cb89c472d299`  
		Last Modified: Mon, 24 Feb 2025 21:40:54 GMT  
		Size: 7.9 MB (7914431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9e6a81070d4661185efb40da41e7154e97dbf18b0ab457e9babcc86e2ed1ddf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536794a5148f9d2b9f968632257458ce95013ca7d7388aa73d973628216c504c`

```dockerfile
```

-	Layers:
	-	`sha256:ae48dc73073ab1d4986aa217c275c6c4f2b4445e9f82fd941024bd8c098d2760`  
		Last Modified: Mon, 24 Feb 2025 21:40:54 GMT  
		Size: 3.7 MB (3720322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c185fc87745fc60c020cb0d039c120f5f7c365bb794bfaeb21f973f4e2a4a731`  
		Last Modified: Mon, 24 Feb 2025 21:40:53 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:e44c82be8cd7b7f56ee0deacbd720a19cf63f05c61ddb292a5cf7df8766cee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120874315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657a41fab29422272d8311e777d9a2879ca5cb8cae240b10089efe9c4fedd503`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.4 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.4
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2b98483f73570203015c1d1f87f29c2d0208a8fc7220af2225cf1eb3dfd508f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9b9a77b35ee6533239e69730f5b8788c1aadb5996de2bd830c402967688e4`  
		Last Modified: Mon, 24 Feb 2025 20:51:13 GMT  
		Size: 65.8 MB (65828890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b711fccef021338c68ef9d3ea309fbf09b5ad48c13550b9d279b94730a681ea`  
		Last Modified: Mon, 24 Feb 2025 21:30:33 GMT  
		Size: 7.9 MB (7913933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f1861603d17550585c0488cdad2ee3fbb29e9f837c6c8ead5fb1d1b2178bf76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4762de5ac3d794664d1f95a13ace888b143a435d635cb8fac496240fcd0d8ccd`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73083c743c50fdea46936aa7119758de68cb4fd13bf8e1718acff5db9f1ff`  
		Last Modified: Mon, 24 Feb 2025 21:30:33 GMT  
		Size: 3.7 MB (3715690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2bd938e35ac4e8faa9797821ccb9a6b717deb65b1e103aaaad3b8de0fca274`  
		Last Modified: Mon, 24 Feb 2025 21:30:33 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
