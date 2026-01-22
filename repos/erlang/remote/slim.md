## `erlang:slim`

```console
$ docker pull erlang@sha256:be7c582015a05a8671df6ca91c4e40f721e695c50540e1f7adb1f617e7dae184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:d4d6fd222be5210b4001b4b938ee90a8f21bf213d2c712327f5e0dbfab47be83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128518646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ac0640cd29510c5b8f2049846ecab1e87f7ea79494ddfb104685cda0a760a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:35:09 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:09 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:09 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936f64c969d353e2038adf69bc7944298a9b288eda3c89d7737c3e354cb4e06d`  
		Last Modified: Thu, 15 Jan 2026 19:35:39 GMT  
		Size: 79.2 MB (79233025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fef20de332b6912ef1200d39d9a19f58794c6b8f80f12ca22d1f63333f1f264a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cc6eae3f73bcb1e1f856edbf74ff61db2bdad49e5450a258ce6597b0944c82`

```dockerfile
```

-	Layers:
	-	`sha256:d7f4ea51bd7fab12cf8c6111e07cc2b65fd51c8241be3c893cf88265205c8a4a`  
		Last Modified: Thu, 15 Jan 2026 23:48:25 GMT  
		Size: 3.3 MB (3283834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2c0918c8e26d91268471a825a6f872a548498a1f84aacecbb955654001ef39`  
		Last Modified: Thu, 15 Jan 2026 19:35:21 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:a39ad327568e6305b7947d5af40be3ccff028406d1b6fe5ae09360087705500d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116520549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1db88b03c116383fa6128933d2873a28686dca13b07ef258462bbc5dfb176f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 19:26:57 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:57 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:26:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ce423db1f019b525b3f032b6fef20b9ca668f921e9a278644993feda24180e`  
		Last Modified: Thu, 11 Dec 2025 19:27:12 GMT  
		Size: 70.5 MB (70504748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f5d71c46a31fcb491a3f28b257dcbd6ade19ef1be29034247659d4c9a96f2c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e5ec52e64190a335b62cdc2a09370e752ce5e106d9968eb44fa7016e03d1a`

```dockerfile
```

-	Layers:
	-	`sha256:717f830040cd9acc87c686ba14ecb6ba4427998c620725ec6f6f7891d768fe3a`  
		Last Modified: Thu, 11 Dec 2025 20:48:12 GMT  
		Size: 3.8 MB (3828056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c5c634919ee052cca6214dffc2f5e111b8da281edd273274bf2fa89fbfa702`  
		Last Modified: Thu, 11 Dec 2025 19:27:10 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:05dcdea6ee03a8ea2a384738a1054a84ce0e8b301a5f7edf16c55ad89174324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114110349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d61aa65b4db3d6c4d7ed5f0db802624de9b6d86945cb6203a9e2b37f829f91`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:dceef99c554f807f9b33461f23cedd54ed45738dd3d906ea7367dc879f4bfb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4996cdad3d8836236b202b8365be7a35de4d5d179dce1a7a87915bad40241f9`

```dockerfile
```

-	Layers:
	-	`sha256:f51c09700ce8338cf3893f56b3ade685efb3768a90807543513803bff0bf9f79`  
		Last Modified: Thu, 11 Dec 2025 19:26:17 GMT  
		Size: 3.8 MB (3826481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55afd26957dc4411249f6d93d18e207551aba20237ad22c9b3a2549da2001ee`  
		Last Modified: Thu, 11 Dec 2025 20:48:19 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:fb3e282a260bd85f8dc8711704fbf4596c91a3736f9ff2907d54328de5ae76f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126939227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fc8e12f9885214ad87f0010363451fce87b5ff99e82cc1a11731ccd3fccfc3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:35:28 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:28 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740e462c6deac44775be8c479dc902841dd52d4caeaf17d961c5a45e1b9806f`  
		Last Modified: Thu, 15 Jan 2026 19:35:43 GMT  
		Size: 77.3 MB (77291144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c801da29ac99f5ea44e6a511952fda7e7eb3b2c93d3f4df2b68e9ac2862499d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebfb437e0675d8ff3d92f8f945042e6e5bf1be05d7ba77864b7c5f2d0eb4c5b`

```dockerfile
```

-	Layers:
	-	`sha256:ea9c3283fc7a676cf1ed5e640402ab746ae3b55642f3e62fb4b6c79ddf9ceb42`  
		Last Modified: Thu, 15 Jan 2026 23:48:37 GMT  
		Size: 3.3 MB (3285369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b054061a1d68e030bf82756de6b7398b7508f2e450aba4e79a05b4e758a4bbd`  
		Last Modified: Thu, 15 Jan 2026 23:48:38 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:d42abedf92b6aa55b6062a75f161d245ff3620de0f6301b4c6e3a1c7bc75946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120145021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3558baa60cbd1acabea371c4a22e2a70a89a16f2311e85c77964b14d08acff93`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:35:34 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:35:34 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:35:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:35:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e88321b383cafc280388ad8cf94c1b064dba056a883b9943cfa882e78d307`  
		Last Modified: Thu, 15 Jan 2026 19:36:01 GMT  
		Size: 69.3 MB (69346145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e68f2e51160204b546854deed22938568de6331a90e67f1340ea4061464a1bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d4060a10bed7d6efa4919e10d38f0f843898e1034277b4733234896734adb5`

```dockerfile
```

-	Layers:
	-	`sha256:96e52d977a44dfff4f6e0fff0644bf90fc6d444d069f294dff8b9e9fc213aa65`  
		Last Modified: Thu, 15 Jan 2026 22:50:23 GMT  
		Size: 3.3 MB (3281004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b0ce2210bf9b26c7a2618f3befef035730d19a8e75b530224474dcbe87ee3a`  
		Last Modified: Thu, 15 Jan 2026 22:50:24 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:a9df01ecf009eaf4ae6cbde99cdb1cc25e167d82f2d910112adb080ae8bed8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123420798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d72ccb7d9377705b9badec0f451993ca0217a2ebf8cc091f890e64374cc20dc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:41:53 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:41:53 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:41:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:41:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ddd4641de7fcdff6bca297036156bfa629c5532e7716eceb2d23a8ad076c69`  
		Last Modified: Thu, 15 Jan 2026 19:42:35 GMT  
		Size: 70.3 MB (70313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d6130f9b3d8b624612172abfd33cb79a4f283a160b6bb40f2e755223f02ddc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2523ded934965602da7280f841857e9a88ed2cea1bd631907f9f92b47cabd0e`

```dockerfile
```

-	Layers:
	-	`sha256:228aaf85504242b614b74edad064597f965651e50488a0810660024b8a8ab9de`  
		Last Modified: Thu, 15 Jan 2026 22:48:34 GMT  
		Size: 3.3 MB (3287425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a98dfa4fbf1d83babb7fdf933127fa5fed923b8bf3c6389065c0d0187f18d84`  
		Last Modified: Thu, 15 Jan 2026 19:42:18 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:ba8b7cd03855039de79b37a02abc860f8f50cf7f5287c50b3893a740010583d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119538088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fcfe97318d3806ab59f9a5f87ebaf23529750d9b5a3e7fc1f19c8235456b8d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 19:36:49 GMT
ENV OTP_VERSION=28.3.1 REBAR3_VERSION=3.26.0
# Thu, 15 Jan 2026 19:36:49 GMT
LABEL org.opencontainers.image.version=28.3.1
# Thu, 15 Jan 2026 19:36:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="faf7293df4aaf13ae297508597d3f758353b952dcc99dd88483993cd0548ea12" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:36:49 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed3e8292312e8f4303fe9387e35feae6bd0a55dd4551e2063ef743f2a76706`  
		Last Modified: Thu, 15 Jan 2026 19:37:09 GMT  
		Size: 70.2 MB (70189384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9dc45be02799dd8d67607dbd7c8295d22aca377ab1d368f0b6867bfeb0d93ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a97dbbd38713118e34078944769daf07388f3ea567853e655d4fa80e12ce436`

```dockerfile
```

-	Layers:
	-	`sha256:a1b1f9b376004e58f7ea1fd48ec167ff1b3436b941bae305d619c8d442121a7a`  
		Last Modified: Thu, 15 Jan 2026 23:48:49 GMT  
		Size: 3.3 MB (3285275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848094a9443c87059f713b555234b3396721497d5062f3b4299f111dbabd77f7`  
		Last Modified: Thu, 15 Jan 2026 19:37:08 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json
