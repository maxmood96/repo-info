## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:3b97a50604c72ffe65423a342b4432cbad38cf63331a21e2aa582115ecbad9b7
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
$ docker pull elixir@sha256:67ae4c573b82b1562c415c12ca803fac357392e8467a9d4ce580d906746d0e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136738414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6368f9573b4a0671f606d977faedeeb056c99a154e1637622b4dbd3ec9dbe4c0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:21:41 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Tue, 13 Jan 2026 02:21:41 GMT
LABEL org.opencontainers.image.version=28.3
# Tue, 13 Jan 2026 02:21:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:21:41 GMT
CMD ["erl"]
# Tue, 13 Jan 2026 04:16:40 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Tue, 13 Jan 2026 04:16:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:16:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b7502fcd0b7d656f2baf2b6ce3b9d44b210e375e53cb89ef849e31f625e88`  
		Last Modified: Tue, 13 Jan 2026 02:22:09 GMT  
		Size: 79.2 MB (79218372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734c75f32b6ae7b0caee21a1b8e5e939433c26e2217f11ee5d2be33075acf55`  
		Last Modified: Tue, 13 Jan 2026 04:16:56 GMT  
		Size: 8.2 MB (8234421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c170fda21905d6f24a49a01dde8ad5736f76245a53d828a0e5c1e7654754289f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef3a6474592ba94b868bd7d169c47686c88e4befe61321bad85cf280488c5c0`

```dockerfile
```

-	Layers:
	-	`sha256:4a4f7c53d00cc10b1c9b551f3b0a6dc17fc49eae9d7d03174fd88f50ac0ad9a0`  
		Last Modified: Tue, 13 Jan 2026 07:51:46 GMT  
		Size: 3.3 MB (3291454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2445b23d43d8dfa9faa40b51a289ca84037703436b4b7ce41a1e1747f866dac9`  
		Last Modified: Tue, 13 Jan 2026 07:51:46 GMT  
		Size: 10.6 KB (10634 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f6accbef4576ada6a78878da5e0e75aa45b78e362875880403ecc559854408e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122339566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4e81eb391d50b616f79fe8601192cb4ae874dcad29e1b5025541c9daa4eedd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 19:26:05 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:05 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:26:05 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:32:43 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:32:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:32:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656ea89dded4641f3cfae04edeb56bdaf27e5ade23d29c71bf377d6a3a515ba`  
		Last Modified: Thu, 11 Dec 2025 19:26:40 GMT  
		Size: 69.9 MB (69914283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3ec9fdf6f8b1ae613d7be87812d54981fde7d283bc33846ffa3f063fbcc541`  
		Last Modified: Thu, 11 Dec 2025 19:32:55 GMT  
		Size: 8.2 MB (8229217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8f3b2a4122b9a5a1694cb65d9c7cd07e75a9e6530c1cf95b50b06436e8c0792a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390627936dc7b85bd98816d23d76cafcd18b5b9c2dde6e95841e59aeb941b53`

```dockerfile
```

-	Layers:
	-	`sha256:c63c272c4fb8b225f629fbd2f263674829952f55b1addc9d49c7df4c90dc3e36`  
		Last Modified: Thu, 11 Dec 2025 22:47:11 GMT  
		Size: 3.8 MB (3834131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd70870664af844fbbaad7e9c82c23f811169c54fb03e5c54d2559afab12a79`  
		Last Modified: Thu, 11 Dec 2025 22:47:11 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:5d98140843a9b70e99314796327a39f7fd704ac3f34f15ba9c4e0a8b899fc9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135159170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4342c13fbe150827031cdb5e5939d160c3097bbb7de6cac514cd95dcae2b4d`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:26:15 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Tue, 13 Jan 2026 02:26:15 GMT
LABEL org.opencontainers.image.version=28.3
# Tue, 13 Jan 2026 02:26:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:15 GMT
CMD ["erl"]
# Tue, 13 Jan 2026 04:17:44 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Tue, 13 Jan 2026 04:17:44 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:17:44 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557544e8d3dd1be9e0e1614d2e401cba2f42cace07be240d81ee2fba1998174`  
		Last Modified: Tue, 13 Jan 2026 02:26:50 GMT  
		Size: 77.3 MB (77276762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3df135be0a542beb0a629e547177c4f66b550c4bd512b053affa155e3c23986`  
		Last Modified: Tue, 13 Jan 2026 04:18:02 GMT  
		Size: 8.2 MB (8234325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:361e43d6838fd0d9ca2bca31393ba06ac0550e75ab5db6337af6d115969b514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39153303b7460309cc0361a8c9f81753b5339b460b4f4a19d5009e6086dad13c`

```dockerfile
```

-	Layers:
	-	`sha256:312b6269fcac1cba174aef5ed63b4554616014b0105e8ef1674d17828998a537`  
		Last Modified: Tue, 13 Jan 2026 07:51:54 GMT  
		Size: 3.3 MB (3293001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc2f61d02ab6aa4f476fab143928677fd71e68939d47628ef028c5388ec62b5`  
		Last Modified: Tue, 13 Jan 2026 07:51:55 GMT  
		Size: 10.8 KB (10762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:aba5ab3dfd11c1ec93718b07d30bdf811ea1fa436ce9ebc6e3674cf2651a69a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128365839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b6ff1fcb5d96e5609c810b682469b2670a066872de3a79fc14d67b3b76ed7c`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:05:34 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Tue, 13 Jan 2026 02:05:34 GMT
LABEL org.opencontainers.image.version=28.3
# Tue, 13 Jan 2026 02:05:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:05:34 GMT
CMD ["erl"]
# Tue, 13 Jan 2026 03:34:44 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Tue, 13 Jan 2026 03:34:44 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:34:44 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad45828b31902899f4efc88b91fc8b211ad1beeeda67e0019b22030dcb23381`  
		Last Modified: Tue, 13 Jan 2026 02:05:57 GMT  
		Size: 69.3 MB (69332947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7451a68b9231dfd19770f886891efb80b866bd3020297ccb9903bdbb22730f3`  
		Last Modified: Tue, 13 Jan 2026 03:35:14 GMT  
		Size: 8.2 MB (8234016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:608d3ea0089613ee8bf61ce90a7523eee02233cc8f242c2a49440938d52eb61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58d67abe502fe429bd351becafea2c59a5ec692b74b52fdbc9e8e681c4f8f59`

```dockerfile
```

-	Layers:
	-	`sha256:055cfa53f33b2b14365b0f859f94e997b5fcd45d050fb6b0bdf92b6bbc6dc879`  
		Last Modified: Tue, 13 Jan 2026 04:48:20 GMT  
		Size: 3.3 MB (3288619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ecde43e343a0f42697dedeac6c71b08f167cd1c883bcbd3612e468232182db`  
		Last Modified: Tue, 13 Jan 2026 04:48:21 GMT  
		Size: 10.6 KB (10591 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:59c0541c7b93d27a1dd8eb2984c8914cb01d3f9beae5c0826475eb490938a958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131634892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5536c86c27eaccfb6266b05e4aa0d7da5cdebc97de549747737c9184bbae96f4`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:19:17 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Tue, 13 Jan 2026 09:19:17 GMT
LABEL org.opencontainers.image.version=28.3
# Tue, 13 Jan 2026 09:19:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 09:19:17 GMT
CMD ["erl"]
# Tue, 13 Jan 2026 15:20:53 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Tue, 13 Jan 2026 15:20:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 15:20:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea82e8e583663c8f34ae09544a0341ba39dc363a93cad699430a27bb86c8e2`  
		Last Modified: Tue, 13 Jan 2026 09:19:57 GMT  
		Size: 70.3 MB (70293080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c3d7fe7807080cc4d19faa721702c981d5b24e429de395e36c71b47fd30a2a`  
		Last Modified: Tue, 13 Jan 2026 15:21:27 GMT  
		Size: 8.2 MB (8234850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:152b388b908097917ce5e7324e402ccb47f278ee61ce4be7c01ef00fb381d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005bf4bf5fe73448b2ec140a533be6ceeb77f9cb1d8ada039c4f5f0d1f2790f6`

```dockerfile
```

-	Layers:
	-	`sha256:5fd8ed71eff90baa33b077a6b08c1571784a6384ca36eacc7dc4376e040a02c9`  
		Last Modified: Tue, 13 Jan 2026 16:46:36 GMT  
		Size: 3.3 MB (3295051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ec5607c00f49403b85a845e129e176090d24b75a939d245b8e449b5f4ab7a5`  
		Last Modified: Tue, 13 Jan 2026 16:46:37 GMT  
		Size: 10.7 KB (10690 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:d3ece9bc721136e69d88050c34125b84c217c845e5913e5ce7d89a41c3fb8ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127758482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f9599e62042d41d80d1247d27f0f88870d5d7791d591c835822827a66b389`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:16:20 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Tue, 13 Jan 2026 02:16:20 GMT
LABEL org.opencontainers.image.version=28.3
# Tue, 13 Jan 2026 02:16:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:16:20 GMT
CMD ["erl"]
# Tue, 13 Jan 2026 03:48:06 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Tue, 13 Jan 2026 03:48:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:48:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ada017183487cd8714a2057689f9690c5a411c907bf292cfc3a685646489ab`  
		Last Modified: Tue, 13 Jan 2026 02:16:55 GMT  
		Size: 70.2 MB (70175814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1595dd74fd985b79c3c696f19dc5ed8c8c764d8e2eb128a29a9866ca045180`  
		Last Modified: Tue, 13 Jan 2026 03:48:24 GMT  
		Size: 8.2 MB (8233964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f17af5895af126744588d99aef4677b5adc2b19b7b7748f76ff44568f9eab5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481091c5c69553b67d3cbc037a2f0de62a37aefa36a5e410a276152141ac6ddb`

```dockerfile
```

-	Layers:
	-	`sha256:4e726f68d5b1c2f704844d22dffc8d43d0f68f5cfaec5324e871be5dae2566c3`  
		Last Modified: Tue, 13 Jan 2026 04:48:29 GMT  
		Size: 3.3 MB (3292895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e4c44a39e470865b48ccbf3c3951cdfd5b655cf9a57b8cd8207c6fe8d3d524f`  
		Last Modified: Tue, 13 Jan 2026 04:48:30 GMT  
		Size: 10.6 KB (10633 bytes)  
		MIME: application/vnd.in-toto+json
