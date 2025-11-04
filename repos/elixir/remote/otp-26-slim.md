## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:aa9a551ab0eb7756ae0f6c25a425cbc5486b2b5528c47a9e728865c5816be078
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

### `elixir:otp-26-slim` - linux; amd64

```console
$ docker pull elixir@sha256:e98642f2bfc555b1969eb444fb4a3c4edeb29bbd0c0c625e3a4d258526a8ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127219491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d886ae0197363c4bbcdc805ea454138efb859039a5d55aab3fec4ad6427b6`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:16 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:33:16 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:33:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:16 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 04:32:30 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 04:32:30 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:32:30 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b136921fb2227afde0e4ec5cec26465aabbe22bd913d1abee2ff746dae9a80b`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 70.4 MB (70430306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ed6b166dc3cfe5f6ca7002a517f793f62467e884b3f584ecfad0791f6d957`  
		Last Modified: Tue, 04 Nov 2025 04:32:45 GMT  
		Size: 8.3 MB (8308129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e9c5078f086e8df85e3267fff7f3508a120c3cb513334d2a2b84579e4d8cb817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25fe4c5d453372a94c551809cce6b99d1b78c93b7452832fda9acafa9f573f2`

```dockerfile
```

-	Layers:
	-	`sha256:01bb46a3ccec94f6346f608ae26736843b749614e9aae474ecc01f3ff0330378`  
		Last Modified: Tue, 04 Nov 2025 10:51:46 GMT  
		Size: 3.8 MB (3832364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4696f6f46c6700598046d07af4d95cea3d85b21c25ee6c11e180756228310c96`  
		Last Modified: Tue, 04 Nov 2025 10:51:46 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:198d887130fbbdaab02ff705f58f9ab1510f70c327231425acc5411adc766c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112666733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029b805c96b1c7562ae2a71a7d31aa3984cfb3663d4e1120bd081e21d8cdd3c0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:47:55 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:47:55 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:47:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:47:55 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 02:41:02 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 02:41:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:41:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0c7fb0ae6db9b2cc75862c0a4ebf823d28b39ad9c45533c446faa027182e7`  
		Last Modified: Tue, 04 Nov 2025 00:48:20 GMT  
		Size: 60.2 MB (60162778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c588b5d5553c17ddabbb046f2e92693f1336177740879bf6549a98c71025996`  
		Last Modified: Tue, 04 Nov 2025 02:41:15 GMT  
		Size: 8.3 MB (8307518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:b378042aa6c2c59c47c5f0fef133aa9d47fb89fb9e027af40f9d1dafb33f2cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e9353a2c0d1bae5cc38d8cffd1fb328af4370de2c9a66388fde7b5dea71fcc`

```dockerfile
```

-	Layers:
	-	`sha256:1232e58a150e8440c69e5703076950061cd13d3ffc3cec762e72b5fe5ae567e3`  
		Last Modified: Tue, 04 Nov 2025 10:51:51 GMT  
		Size: 3.8 MB (3834589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9734eb8cb15085d350ea2053348077262c198c75f71a4917ddfce53d6f47b50`  
		Last Modified: Tue, 04 Nov 2025 10:51:54 GMT  
		Size: 9.8 KB (9819 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:15e7d4355112b3febaa31501d12e719c88f3cf0fd58dc7cc9adab8bb36363647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124738043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f5d0c4f0436444d3e86d97551dad832a1df43bf6f7588381dbb2b41b7bf380`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:54 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:34:54 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:34:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:54 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 01:46:54 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:46:54 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:46:54 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623ee7d32f43dda583537ae1cda285669839d35c4475ea85f044bf2a93a8a14b`  
		Last Modified: Tue, 04 Nov 2025 00:35:21 GMT  
		Size: 68.1 MB (68070765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d079beadd61324ffaa4a880d4d3810e34c1333fe892fdc0aa7e27559ed8195`  
		Last Modified: Tue, 04 Nov 2025 01:47:06 GMT  
		Size: 8.3 MB (8307800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0dcbeff9986678c45ba22ae1a1a2513e66d256d8e7642b71e4c70e3f36106434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f9980eec133dcec2f2777ac966b25dad4fde58cd95698b7cbd4c273ca1d1bd`

```dockerfile
```

-	Layers:
	-	`sha256:cd41c8dfaf1be6211351d8ec8cf460c8bc1763329eacb446dae7b40345571387`  
		Last Modified: Tue, 04 Nov 2025 10:51:57 GMT  
		Size: 3.8 MB (3832613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880c2d02f0ae77d15c81e2b18ae5a7b91cddd4d1357d2e4e7beae6d7a5a943ee`  
		Last Modified: Tue, 04 Nov 2025 10:51:58 GMT  
		Size: 9.8 KB (9839 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:5eb2b44634c7dcd7996026732938b0b8eeae6e6b1c046dc118006fce96181fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118929522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9116df6bf41163c1e5778d7fa5ce729a48712977b57fe8d201dac05bd86b05b9`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:17 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:30:17 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 01:48:22 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:48:22 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:48:22 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72391287dfd25f0f21acf2ed7c85e4225a39d24bb12601d929828b0a644ba2dd`  
		Last Modified: Tue, 04 Nov 2025 00:30:42 GMT  
		Size: 61.2 MB (61154810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a05b45d986d9132644237b7245476e8107bbf2ed445e9f4074807db0c0cb1`  
		Last Modified: Tue, 04 Nov 2025 01:48:35 GMT  
		Size: 8.3 MB (8307598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8ed5643066be5ebb37cedff1286c4a3b04350335eabef31c14db3d7311cb95cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deae63d0a6d4ab7ab7b34d05bad30cfa7cef66a7fba6624a12303a434042c4e3`

```dockerfile
```

-	Layers:
	-	`sha256:2c80fed8593f8ee11d51a5223db4260532b1ffb5265187dd53aa7d7c04b811f1`  
		Last Modified: Tue, 04 Nov 2025 10:52:02 GMT  
		Size: 3.8 MB (3829531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10174e2406aad298589d07362303dc32278680747f3231e19a300d5b6c0457c`  
		Last Modified: Tue, 04 Nov 2025 10:52:03 GMT  
		Size: 9.7 KB (9719 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:91fddbf5fe89dfb076583bbadd5a31453f5e5fa479abbbcc9b6b2b4eb8e396af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122887186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551d16a796f7a88cc904032d572dafc2f11fe4e30224b1571879acec292bacee`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:39:59 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:39:59 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:39:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:39:59 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 14:03:15 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 14:03:15 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 14:03:15 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb768048b5899bc97639cb39d9c29e9e3751572e57337a265b88b0083dffa9`  
		Last Modified: Tue, 04 Nov 2025 00:40:55 GMT  
		Size: 62.3 MB (62251565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a11ad69857545c727ee5474028ce4440ca3d296bcb4d53e7162bb541c18d16`  
		Last Modified: Tue, 04 Nov 2025 14:03:43 GMT  
		Size: 8.3 MB (8308341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8c930f1ac15f6aea66d34f00be467eb98fd27532b4751713bfbb519ac5a5c965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7537e2dbe32e0880cfb69da5186c96ea532b479d5e63c354751d7d2bf0dfcb70`

```dockerfile
```

-	Layers:
	-	`sha256:0506afd69993df89d67a2b062e006c280fc4f47067a8e63d1ff280fd0f82d72c`  
		Last Modified: Tue, 04 Nov 2025 16:48:34 GMT  
		Size: 3.8 MB (3836806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28f10f602834404bbb1a1a711b21813867713ad001e5e724610adbe09b2ff34`  
		Last Modified: Tue, 04 Nov 2025 16:48:35 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:74f1431b6f47018fe387b94bf61f4d214aabd3fdfce558dde2cee59e94377631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116406003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4400dddba084cfcd04fdb5f4d38847645d8a25e36488ba18ff7ea2d5e5a8292`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:32:11 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 03:32:11 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 03:32:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:32:11 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 13:15:55 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 13:15:55 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 13:15:55 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e1dbfe59ae33319104649a00234b8446d2118b230747b863202aa24e3f31a1`  
		Last Modified: Tue, 04 Nov 2025 03:32:40 GMT  
		Size: 61.0 MB (60960398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c147b27d6fc1a1375c72bc6b11967820b0a98b43c50534f7de8b84e95bf2c5ae`  
		Last Modified: Tue, 04 Nov 2025 13:16:17 GMT  
		Size: 8.3 MB (8307512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0e95222d94ced29730d9f26c08cd852288203c9e5a152205f5bc5a3cbae761c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01072b147f32caf69ac3fa84644fba7fbe064091ff83c369f57856792b7d9fb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e877ef89655f6344ef2e3a27938a3e73ee1d847f33b58aaef15c4c645450e3e`  
		Last Modified: Tue, 04 Nov 2025 16:48:39 GMT  
		Size: 3.8 MB (3829192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26762c923651d1f2909c038b069ec4c1847dde6e7de50b5f6653f224370eaff6`  
		Last Modified: Tue, 04 Nov 2025 16:48:40 GMT  
		Size: 9.7 KB (9745 bytes)  
		MIME: application/vnd.in-toto+json
