## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:a819441774e62a715c9994a1883a58ac8b346e21f2b3d1ecd9b22ae6b31a2b06
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
$ docker pull elixir@sha256:705b6820a61ba411991c73b185325cb1cdf68bf2fdae6ec01940370b8235c91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136356703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca64f919a38210bbc013f7c457cd0d4855166bdebb09f5544210f3d2cf895db`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565a3702d4647a881c9db90df9bac02603ad0a87c518d960a890413ad1174036`  
		Last Modified: Tue, 01 Jul 2025 03:26:15 GMT  
		Size: 80.0 MB (79955331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f9951786a1aec07294dd9cf87fb21356e2efebb88b36fc07fbfea5f6e88b97`  
		Last Modified: Tue, 01 Jul 2025 03:27:20 GMT  
		Size: 7.9 MB (7907088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a28339c8e0d9dbfafd32d9b3ea4ca0a36e84a1bde4089af48b84461451bd8ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c082a81cf2edc290377688a04e41641b5655bee506397206a0d7e38be6984`

```dockerfile
```

-	Layers:
	-	`sha256:101e4376ef18a15122dc9c2d8b7dd121e8be4b79258cd46ca21e83c26a02d7c9`  
		Last Modified: Tue, 01 Jul 2025 06:47:55 GMT  
		Size: 3.8 MB (3825269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dccaf47d24a428f6cbf37b57945d07768853685a958186142a80c51523d9fcd1`  
		Last Modified: Tue, 01 Jul 2025 06:47:56 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:bf1b88c0af7ce4e85fc1196cfdd2a6ed4e7447d4603ef38cf36269f336f08d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121168866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a06f12d5a0f6bb1555bb92966a524b7d403986c9775127e3c285667a6f505d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244ea1e3c7cf3a49868dea6880dbc90dad04486f295bc5181c887216000efdd`  
		Last Modified: Tue, 01 Jul 2025 09:10:04 GMT  
		Size: 69.1 MB (69054240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6fbe420fa787a05bf30c57d98bab7b62c2214d6f05d20201e3606766140357`  
		Last Modified: Tue, 01 Jul 2025 20:39:14 GMT  
		Size: 7.9 MB (7906449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8bb197f1992b90ac994df0380d3812de6db50069205a83329eadffceb014ac58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f781352508c110092aa2e9ff6a6dfdd1b5fe978e5d0f340d5f07bd7cffcf0ed`

```dockerfile
```

-	Layers:
	-	`sha256:173c31b2a2c4dec219e77cbd80476b253d221dcfa5402c99c0eaddeed530c537`  
		Last Modified: Tue, 01 Jul 2025 21:47:28 GMT  
		Size: 3.8 MB (3827518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a98df344bdb8ea2c926692ac112507edff442d4c12b6aa1d99e2253d59609265`  
		Last Modified: Tue, 01 Jul 2025 21:47:29 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:7c63fe9b0c5b96274de31c0abdbad327eaa164744c3aead485b4a846e53512a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134001961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559859a84c8c7c4d9abca7531121d94c24b4ebfb86542af18e746d3f1545b17`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a947b516f132d1d28c3996aa5edd0efa897e47bf83f129ada77895bab00ff140`  
		Last Modified: Tue, 01 Jul 2025 07:02:13 GMT  
		Size: 77.8 MB (77756152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a675504a96f1b44e0e21eed85e15a4251dd341dc8d441ffcc638696c67d88`  
		Last Modified: Tue, 01 Jul 2025 16:26:42 GMT  
		Size: 7.9 MB (7907024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:970af72080a69c7a5d3d7d70383babbadab323fbd1c2a52b9345beb643643228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9170f373902a8af382377757932bc6fad761d40d56f5ac66c6e73b1051f247`

```dockerfile
```

-	Layers:
	-	`sha256:36e2608ed71e0219f9a0084f093d591674873bd6d2b215c44dd599a922e4272e`  
		Last Modified: Tue, 01 Jul 2025 18:47:16 GMT  
		Size: 3.8 MB (3825554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643168f9e395ae876595fef27efbe805e72818fbcab84120f1924d9772ddda8c`  
		Last Modified: Tue, 01 Jul 2025 18:47:17 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:9010caeae8a8a91e7e5aeaa9cb56f9b9125fb2c9dee3c617ee7f53ba854e5e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127555131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb4200f1fba43dfb9e5629b422c7df3440287904a46c6cb0541f208ed7c2b18`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd46c820a552519280ae8a425571a45d8518a0b03e8927ab97e0586eec250a18`  
		Last Modified: Tue, 01 Jul 2025 02:27:36 GMT  
		Size: 70.2 MB (70171179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db1bba4440f9ad8553d723b81c37b49c4740fa06a88cc93753f2ff7f0525a3a`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 7.9 MB (7906531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e14ffe4c609014e6e3869fbc19b199684b459a25bcc56800c252d9f26604a504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ea8b8d22a9d53f39d825e878f33b482b569243ae77d7610ea36a6ed6c0e2da`

```dockerfile
```

-	Layers:
	-	`sha256:186c0e1fe28ff154edbcadc26bb5e6b7953cec09e987af7fdd2a0aad8cfad65e`  
		Last Modified: Tue, 01 Jul 2025 06:48:07 GMT  
		Size: 3.8 MB (3822426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a535d96c2de730484b9e374dd65e2e759364e26e9121846a671b7932a88f5f3`  
		Last Modified: Tue, 01 Jul 2025 06:48:07 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:fbb0ed897ae38d8ee73f48d547074fb38ff240443340617b398dfd59dbafac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131433766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4487daba98cad894f7f18a70c4ea9bbd304fdbd1d6b892b591058276c985fc15`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc071bbb6154045150e6c2c5a0a9549b481db1a5d6de8894fe3858319c300c6a`  
		Last Modified: Tue, 01 Jul 2025 05:15:06 GMT  
		Size: 71.2 MB (71189348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6f8068f6ffeb9c5c7b494607878de48933df9acd16a7fd7b46f7021389ba7`  
		Last Modified: Tue, 01 Jul 2025 13:57:59 GMT  
		Size: 7.9 MB (7907175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:628c3a38a7a3c36d4eb9ce87210f10a30ab83b5172d2f7cf673c7340b4a63e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c430f9fc23b9eef5143b3b5a20f0cb12fed4b558bef1adb64542a26e880545`

```dockerfile
```

-	Layers:
	-	`sha256:94a7cf7ad235c0b05fd13f9026d3aa0df4f179b63e5c98523615e691fbadb171`  
		Last Modified: Tue, 01 Jul 2025 15:46:37 GMT  
		Size: 3.8 MB (3829719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56be47a0f09341b80cc4af2aab5ed55e06bb8edcdd929291c03875c295ff4cbf`  
		Last Modified: Tue, 01 Jul 2025 15:46:38 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:138246f413700ff302c4a77095858325c283680a7ed9566efdcb5adcc489162e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124872937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65677e55e45430b624e3be2622f8685310589a87e8a15fdf345162e8e2c82cfc`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd18c4d587e59a190d5364bfc2c22e367f4433ed2f89820e7786f56bf3cbc33`  
		Last Modified: Tue, 01 Jul 2025 05:38:35 GMT  
		Size: 69.8 MB (69816966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43501afabacc486b1ad2d8c7b30d9bbdf4d4caf12a520de7b05c7dbf4d9c0984`  
		Last Modified: Tue, 01 Jul 2025 10:46:21 GMT  
		Size: 7.9 MB (7906684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:22ce63f1ca94e38623f042b938e24797cc0a5a6c99325fec4b1d7e36f5125a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988bd0b0097554a266bb0e34697e61dc6f783773936093f3cfd80a82c6b16ac4`

```dockerfile
```

-	Layers:
	-	`sha256:ca4e457ffd6c8f0ddb561c02af160bad0c76a3588eacce690bda0228fa316c4a`  
		Last Modified: Tue, 01 Jul 2025 12:46:50 GMT  
		Size: 3.8 MB (3822097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06665dee06b3b95ce282b632d94351c89ac8e4694700f31edafe12fde6e384bd`  
		Last Modified: Tue, 01 Jul 2025 12:46:51 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json
