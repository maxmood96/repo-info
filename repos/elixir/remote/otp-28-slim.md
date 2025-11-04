## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:b435638a86fd1d3f416dbf01a6bd6b1cb4b039bb92f407c405915a5ad7eed879
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

### `elixir:otp-28-slim` - linux; amd64

```console
$ docker pull elixir@sha256:4d7df27b7a3399cb004a69b01c3743eeae4c9d8fa00ccb9127c4e8b84f6e79e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137302533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715091b2c6898421c1ef1bc5246db2865dc7b1322c713695df0b21ba26b7afd9`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:30:47 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 00:30:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:47 GMT
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
	-	`sha256:e7037f93eaac113646cf0445774a3872dd52615bb72338f8e7d966b98dfe0282`  
		Last Modified: Tue, 04 Nov 2025 00:31:16 GMT  
		Size: 80.5 MB (80513773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa763edc8b38a8ef7e27fd65e066af954f2a1ffc358c23502018e668b7f02f0b`  
		Last Modified: Tue, 04 Nov 2025 04:32:44 GMT  
		Size: 8.3 MB (8307704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:36022bf5ccfc31a3afe74fa715660dd60291aaa43c7cfd9f0fa920686cc7e700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f162581b296b5a902a218c3ac2cf8bfe2d0ca8b1d1a50663b370447ecc6d6d`

```dockerfile
```

-	Layers:
	-	`sha256:df9fcc7a9468eff27f59068288b3c233a3b07690fd08d6acc2b8792a81695fac`  
		Last Modified: Tue, 04 Nov 2025 10:52:30 GMT  
		Size: 3.8 MB (3831894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f17d504d420bb28d98336d63979cc2ace6e6ed286fd3020f1995874f6f6cb70`  
		Last Modified: Tue, 04 Nov 2025 10:52:30 GMT  
		Size: 10.6 KB (10634 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:fb14d54e9a4f7db1fa4f92c2472cef7e621bcd2af69e42b52f4ad80fe6137204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122113680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628f08c8128c2f12b80af1b6f592c754067659c11717831495de48993684c634`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:43:36 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:43:36 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 00:43:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:43:36 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 02:41:00 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 02:41:00 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:41:00 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedf9832aeff1e0606c52c72b4aab2b9b819295c175ce61614d85e6c7d29a287`  
		Last Modified: Tue, 04 Nov 2025 00:44:01 GMT  
		Size: 69.6 MB (69610157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fb308ef9a7cc522699803b6cb6d784e9ebdc510e88c6ae18ef66dd099684`  
		Last Modified: Tue, 04 Nov 2025 02:41:17 GMT  
		Size: 8.3 MB (8307086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:d4b66f79f7dd234365d1843a73e9b2ddd744547c7c541e4004ed6451e65591f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f255d76b89ca2c60d58b1620a2a757584725f3867ebace2314818c9a73069d93`

```dockerfile
```

-	Layers:
	-	`sha256:dea07f508a5c825219fc772a3c26817b2533c87c404e747f430372cb278c0fde`  
		Last Modified: Tue, 04 Nov 2025 10:52:35 GMT  
		Size: 3.8 MB (3834143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe142377bff161ffc6eeadf148753f8b27f81cd52e1a344bd822033aca4ead6`  
		Last Modified: Tue, 04 Nov 2025 10:52:35 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:0ce6a076c0c0b9e689c955b21fd468fa94f9b5575e07ccf791f810bf6e5dd09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134986741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e022b3788836d6c9a1c3dec50a556400bddb0c2ed15a2a8ba87b05b847c86ec6`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:32:57 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:32:57 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 00:32:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:32:57 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 01:46:52 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:46:52 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:46:52 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b59517cd6e2cc84cf2d9e090c92661afcc1f6d84b50e60d116910d2131974cc`  
		Last Modified: Tue, 04 Nov 2025 00:33:33 GMT  
		Size: 78.3 MB (78319819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682626ddd8b99cfc581c55a9cc11713033f2f237a3706f56e0bfc9858f972a4`  
		Last Modified: Tue, 04 Nov 2025 01:47:06 GMT  
		Size: 8.3 MB (8307444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2be6a3bae2bce7f3d2dca0ed63478aed1510604c234e92c3be2136285f9f5228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54089cc45470dad7ee8b9bdf82a3fd9c083e641be758f6f8a84840e44d99712`

```dockerfile
```

-	Layers:
	-	`sha256:cc75c6773f26b7dacf5e65d6bfd62a52b75c99b5e29a49ffcfca6a8edf302772`  
		Last Modified: Tue, 04 Nov 2025 10:52:43 GMT  
		Size: 3.8 MB (3832179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90265afc853490818bf09f620122d965332b5cf9254e4f360189195cd0d14d47`  
		Last Modified: Tue, 04 Nov 2025 10:52:44 GMT  
		Size: 10.8 KB (10762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:a760017c9499d537098ec582266b7d7cbb52c36521571f15d5fbe17b512220ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128499128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa082eeee866ab82838e514e2c099ef2a5df6836778b1c9a8f69a619fcbc8a89`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:29 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:28:29 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 00:28:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 01:47:51 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:47:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:47:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2291106a5a6bd8f7349a8f2c66148c6c15a1d60cb29f69227fa4aef49ea37`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 70.7 MB (70724778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0174a48ab7fe7e002c3d3a48f49d2360b1ea38ea9b4732e933029ff16b27fd`  
		Last Modified: Tue, 04 Nov 2025 01:48:04 GMT  
		Size: 8.3 MB (8307236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:55ce8ed5599add014de9d63cfee4df671aa55883c575fba3aacbb1d5ccd33b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0023c87e40d67cd0abff2eec136305a696fbff88e97c3bb87783d465b82fb300`

```dockerfile
```

-	Layers:
	-	`sha256:eea4412af0f6dc5d8587cfea43d9a3be1bb6491bfabc456a24855bef10cc30b0`  
		Last Modified: Tue, 04 Nov 2025 10:52:48 GMT  
		Size: 3.8 MB (3829046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e64025a4c22c9d2f45cb88c07dcbdc547342afffed07266626fecce1bacb60e`  
		Last Modified: Tue, 04 Nov 2025 10:52:49 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:7962c9112e914f87e755855e48b0a232dfda581ab44ca8d113ad666eae22afde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132385329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd1df6bd97dc5b9688c8a2cd121f13c59c4b2118443e50dbacd50443e9bedcc`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:14 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:28:14 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 00:28:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:14 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 13:59:58 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 13:59:58 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 13:59:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf0cb467307969420a655a97c709234e06fac082753a2885d777ce1a0b705d`  
		Last Modified: Tue, 04 Nov 2025 00:28:57 GMT  
		Size: 71.8 MB (71750459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71e8d1f9536c4c2a08f7547edf65ff6c820e9b3c6639faefd9aadc86450524`  
		Last Modified: Tue, 04 Nov 2025 14:00:39 GMT  
		Size: 8.3 MB (8307590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:06dec09d7331aaa76f3d26c6f66e01f18c785071c961546b68515ae09dcffc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcba87697837b8a2285cdf8e97d621fa6df2554c0ce1940cb129d1a9219d4cd2`

```dockerfile
```

-	Layers:
	-	`sha256:a85c39d544b8e3c5c2b6e790a70b5461d8f02527aa52369931f8691b64a8d36a`  
		Last Modified: Tue, 04 Nov 2025 16:49:00 GMT  
		Size: 3.8 MB (3836354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ec6fada916331c706f1e91cafdc05d9f96cdebc3e8b8c5b3fdc194c30c56d1c`  
		Last Modified: Tue, 04 Nov 2025 16:49:01 GMT  
		Size: 10.7 KB (10688 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:40a50de9140ce1a9319c551a946f1aae3b64d18afe3830b9a467d222958ea1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125819065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdddb02c6647875111ca91541b03d3772cc4d94abb14b03ccab982253b439727`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:23:50 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 03:23:50 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 03:23:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:23:50 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 13:13:50 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 13:13:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 13:13:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ffc5b89d17b03832b461d514b680f743105a5c8cebfc07abe7fbafc70f35`  
		Last Modified: Tue, 04 Nov 2025 03:24:24 GMT  
		Size: 70.4 MB (70374069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faf37e1f1dffeb8137931bc5815b8f5709b47cd15bdcf88db0cfa045d8c3b8e`  
		Last Modified: Tue, 04 Nov 2025 13:14:17 GMT  
		Size: 8.3 MB (8306903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:00ac6d1ff5d17c36e8c8b37b8d06aee775e1d770a80252d773015aa75488ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db862a225bb58492416978d52a14dd4593d5cd66d4d52063d19a118d3461ac0`

```dockerfile
```

-	Layers:
	-	`sha256:85f9a629ef83bb2906555dadc96cd2b0ac8e4e47ca85485ef0fc50f6fca99585`  
		Last Modified: Tue, 04 Nov 2025 16:49:06 GMT  
		Size: 3.8 MB (3828722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5519a38d77a029bca7cc2fd4838649c478a1e4e2b3e3d945f9bafe8e52a1bb`  
		Last Modified: Tue, 04 Nov 2025 16:49:06 GMT  
		Size: 10.6 KB (10634 bytes)  
		MIME: application/vnd.in-toto+json
