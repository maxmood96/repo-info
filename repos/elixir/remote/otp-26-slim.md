## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:64b9162c25e295481ceae28f084bacf7e8f116e4232ff702658c4a217ce4302e
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
$ docker pull elixir@sha256:05db3bdda6f563c6717b8f2f0855e04d2d6f77a3e8bc6d257797a7ac2584ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126755545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d25ddd6877467b5c45348ccad292f98c1097bb59e9237d091b7bf07776a478`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3f3af508cdb50d7c303c5d72f27038f2274d6662fcddb4e056dead4a66304d`  
		Last Modified: Tue, 14 Jan 2025 02:41:06 GMT  
		Size: 70.4 MB (70378826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a318acdafca1e0d69ec82be177f0fe9bdc5449d5b3e0aab118a36b8163b78`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 7.9 MB (7896757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6039c20e91a7cc79543b36740abcaa894838899f996d2c941bf7c678c7c280c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db053de6361be5c94b8e21751754c5109bb66df78f225005d9a0e47f1869716`

```dockerfile
```

-	Layers:
	-	`sha256:5836e19aa6a69ae4c8d9b01afc66171d947c99d6640411694bd142307f5df767`  
		Last Modified: Tue, 14 Jan 2025 03:26:01 GMT  
		Size: 3.7 MB (3716380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d18e0ed238a28c8de43c08cfcd79b6ad22c13c65528cc414cf09cf3d3a47498`  
		Last Modified: Tue, 14 Jan 2025 03:26:01 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:bb0e9c446645cec2f2b794c81df4548a43209e35935a8943c034b189ae44ed10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112212091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b052da95675d4868fd3b2b6390f5020a992ac99dbef4e0ea4a7f3b13aac588`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf41700a226b03daf2834446b5e5a2d4c27fa3ef5f80586adfad85e0cc0b83d`  
		Last Modified: Wed, 08 Jan 2025 18:09:29 GMT  
		Size: 60.1 MB (60116076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea5250ba194ae244ed7afdc7d0d760457aafe7479b1fefad7bc538af0e0af2`  
		Last Modified: Thu, 09 Jan 2025 09:32:15 GMT  
		Size: 7.9 MB (7896048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:68fbc436499b791d2b7b16e7e94efd617b3b29fbd73230b0a43d8ee3a3cb754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa60d048859dde4461a32a9399eb6039155ff69ad733f2e3272f0f67b3ca050`

```dockerfile
```

-	Layers:
	-	`sha256:77368b14fda022a420ebb4ae343cddb36877e77fc138b85d03a15e25e22ba5e5`  
		Last Modified: Thu, 09 Jan 2025 09:32:15 GMT  
		Size: 3.7 MB (3718605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff66e4d61f438d7c8987ac81ba74b0eb0e96aad95f3f6a7a4e91bc971e2a257`  
		Last Modified: Thu, 09 Jan 2025 09:32:14 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:cd12a6f08ab0e541df8e081b0af2b6a2c1b8be2f5147d610c232aaa8dbc3eff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124232678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcec775c2586e0d6931388d46bccafc3ba9737299f0ed19e279d4d7810dfe72`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e630a97593435e1e3cf3b8ff1f1eb1345f2232d25b9a5d5b7315e7154148dbf`  
		Last Modified: Tue, 07 Jan 2025 19:32:39 GMT  
		Size: 68.0 MB (68010460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8b670290fe37abd253f92dc29ce836be37b3b8e149d24dfbd508ab1666eb4a`  
		Last Modified: Tue, 07 Jan 2025 20:54:10 GMT  
		Size: 7.9 MB (7896734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c873e613110e6121f1406db8c8daff12772af8c572554c00cb64ccbaa43c1114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5eece1b47e862c8ba4d402eb8ee677e6b4bc02be58ba2f6456411139618727`

```dockerfile
```

-	Layers:
	-	`sha256:39c3240d77717eeb6da9ef16b9d0bc862d36f9652f9a380a50e473714c84344c`  
		Last Modified: Tue, 07 Jan 2025 20:54:09 GMT  
		Size: 3.7 MB (3716629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2623b53cc6f4a11320706e51f100cfaa208148332e520da0960f0c1a5b6c1bef`  
		Last Modified: Tue, 07 Jan 2025 20:54:09 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:4559cb8ceab5c32eaa5be177c3575545fc571db31ff40d5512ae35bf5d22cead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118469476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ec37af9dd99374487d147c79ad6c52484e10c02128725c541de57126de88d6`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd5e010075b3c7e91533ed703b8c21bddab162b508d7c6c889ef6964475ce36`  
		Last Modified: Tue, 14 Jan 2025 02:24:43 GMT  
		Size: 61.1 MB (61115574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25c2374e508df9b47e2fa0ba6f3bf79e65311607be6d999f75792a65b0019d`  
		Last Modified: Tue, 14 Jan 2025 03:21:14 GMT  
		Size: 7.9 MB (7896157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bb505c3e72251ec08a6ad2ac250c42d4c615b7504fcdabbbd3b1a8649f0e2901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2db3127700ce0c446237980b85212987e41604f39c0f90d0eb2e3d83e65b02`

```dockerfile
```

-	Layers:
	-	`sha256:545dd6f6dd3fa99fc5cc3ba72fd6cfed32664eedc583d6ded1ca9517d5dce396`  
		Last Modified: Tue, 14 Jan 2025 03:21:13 GMT  
		Size: 3.7 MB (3713505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fdd9b2e925bcffafff01f5e3ff60307e3e4de284ee45c2a9a9911ae8322b82`  
		Last Modified: Tue, 14 Jan 2025 03:21:13 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:2c6f5280fcaedd480a38e7abcfa089be6549c344081f797f8d47f93abc4d8f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122427343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b3bbe0c28a299855a8352624afa38ebe26ca2044a0ef68a64184cf6dd01637`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beae205943690a3db144ff3b226203001dc08271ed496289cb66044ff817d8f8`  
		Last Modified: Tue, 07 Jan 2025 19:11:26 GMT  
		Size: 62.2 MB (62202410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d1a3eb3c99ad711eff0ee31205d71e568d9cc85dd44797fe10077c45d8146`  
		Last Modified: Tue, 07 Jan 2025 20:33:45 GMT  
		Size: 7.9 MB (7896858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6ceb8018656f718c85ea71b8bdf4b5b261d3b236b08f874add8401e97d6ec8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8954a8bad16532cbc8a8242f1f0ed8a6c76a00809a9ea1dcfac912413ede7c50`

```dockerfile
```

-	Layers:
	-	`sha256:7f0fbde889b73bbf5415c0272190db1fb05c56db33562d665649443d7ff24393`  
		Last Modified: Tue, 07 Jan 2025 20:33:45 GMT  
		Size: 3.7 MB (3720714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1681cfbbc43c49380319baeadfdedcefddea9ff674201d57f619785cd1f222e`  
		Last Modified: Tue, 07 Jan 2025 20:33:44 GMT  
		Size: 9.8 KB (9826 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:6eee0e533efbdac0405ef927b41584e2125727331d274424970bf296084d7334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115959733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f226f074c8f6056987da70237a51de1452884839bdaf4df591e4c86262556d1e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d856a973c0f7421f2f6e8b562b64251830562b5304401668d701544cc6efb254`  
		Last Modified: Tue, 07 Jan 2025 20:24:08 GMT  
		Size: 60.9 MB (60913869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb41295f43500e63cfd3828cbf78b1df5ad66e5710b38b6097dfbc598f7fc51`  
		Last Modified: Tue, 07 Jan 2025 20:55:37 GMT  
		Size: 7.9 MB (7896239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bcb886bc07c2a177e09dfacbc5562fda5915f77da507f5678de6e4e7807a91dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea1ac0ffbe7820bfdfef2fd0b65ab885ec0b3c6fdba5b598e772ca4c634ad2a`

```dockerfile
```

-	Layers:
	-	`sha256:69264a56fa3c6115b65764c82820317503e652f6990b38b64400a60d236cb88c`  
		Last Modified: Tue, 07 Jan 2025 20:55:36 GMT  
		Size: 3.7 MB (3716100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5da06ad82ff5b832df63ce6f2158d1771604dd172c87b8ec7ef95e0aed6d1ba`  
		Last Modified: Tue, 07 Jan 2025 20:55:36 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
