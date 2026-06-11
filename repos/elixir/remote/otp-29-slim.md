## `elixir:otp-29-slim`

```console
$ docker pull elixir@sha256:9ab7f0d734daa499906d6aa589b5425d39f6bfc353f93830587e1b9efc0d3087
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

### `elixir:otp-29-slim` - linux; amd64

```console
$ docker pull elixir@sha256:adc2b34fc5926faa85b62adcc5120bbf8dc83aedd957d8344fdbd9ee56904801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138181398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd14f2c12db81ed1573b614bcb141ba1941574999865aa4bf30d87cd8c19f8c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:11 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:45:11 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:45:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:11 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 02:39:08 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Thu, 11 Jun 2026 02:39:08 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:39:08 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1122d8f764bae7a104d6cc60fd4c29e156db4f141f6b866d7378d3f4371d1fd`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 80.3 MB (80275734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc974a6d244795d1c8234347d6aef69cf7c62b100b10bbe18d119255a9476f11`  
		Last Modified: Thu, 11 Jun 2026 02:39:17 GMT  
		Size: 8.6 MB (8588543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:d58948cdca27c56c9d51002cdd5f86b4eae71477b33440b2becdd487137446fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64562753aac5153fdb6e26f87db24f2352f7888b996373b2e70137c60f2b5edf`

```dockerfile
```

-	Layers:
	-	`sha256:c60abdafde5384d46da9fc5dd36cc6946ab04ec648efbbc5dbba0ae56d62291a`  
		Last Modified: Thu, 11 Jun 2026 02:39:17 GMT  
		Size: 3.3 MB (3291470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e387560a6ceeebd68ab5b471934b2c2ff0aed423cbe658095ec3eb7b77abdcde`  
		Last Modified: Thu, 11 Jun 2026 02:39:16 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:dc3c1785f535cee56523aed45772b7a52aa21910cd1a361f48b74fd55f214809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124343008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35489cb657986ff19d89293af398efe2c2960e69089c27c52d0e2677f2078e0`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:34:19 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 01:34:19 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 01:34:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:34:19 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 03:14:08 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Thu, 11 Jun 2026 03:14:08 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:14:08 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d62d08c620d0eec40faf3aac1bc412bda14b15929b15d8ccdaaa313f2bbf59`  
		Last Modified: Thu, 11 Jun 2026 01:34:32 GMT  
		Size: 70.0 MB (70006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc105625535013f9b9b6e0fcb9911def295ab3f329c11083c9751090f5f473`  
		Last Modified: Thu, 11 Jun 2026 03:14:18 GMT  
		Size: 8.6 MB (8587871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:14cf0777a13a2f72b71e4c23637899d09e945ba3c2554a0652b68cc91bce9976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2625035a13bd52a5c069c7d4fbe833bcb8b6a9a9f98144d21064fd25ffc0ebdf`

```dockerfile
```

-	Layers:
	-	`sha256:09637820aabea71c71a25f9256be588fba444bac19de70137b21df45142c0a0e`  
		Last Modified: Thu, 11 Jun 2026 03:14:18 GMT  
		Size: 3.3 MB (3292902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7117198f3b9095ee60e786696d15665d4a5c0e06410e48d364c47b81fdf20c`  
		Last Modified: Thu, 11 Jun 2026 03:14:18 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:ecfcb42b6369529a47bf96d9323aa07a1b38f7b3c1c497873c76abd42a0d5df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137003791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68601a33b2706917bcee2c3f3657b47dd61b5d9d0e5a403532ef9ba5c98f665`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:52 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:46:52 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:46:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:52 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 02:39:02 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Thu, 11 Jun 2026 02:39:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:39:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6bf566fca74c226a4237b72714242ce34a41c007dc652b12bc3850a7685b5d`  
		Last Modified: Thu, 11 Jun 2026 00:47:07 GMT  
		Size: 78.7 MB (78737110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6847529bfbd25760488a866af9dbdad1cf31a5ada621e82e61219def2356ddc`  
		Last Modified: Thu, 11 Jun 2026 02:39:11 GMT  
		Size: 8.6 MB (8588512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:903fa9d00a863501dc2f45b1c395a6acb3924a8cb7007ae544c691218b7da021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63bc4936608c782de45f6ed809fd1dd3ba64c0e0ad5c4a83cc1a5ae74cbf9f8`

```dockerfile
```

-	Layers:
	-	`sha256:c4ff16609a816df1407f914cbdc8d1319c6442120f4267f8752f950c0549cede`  
		Last Modified: Thu, 11 Jun 2026 02:39:11 GMT  
		Size: 3.3 MB (3292380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01dbdb4dcd0ed140cffc4479bcd1fcf9de9f5b1dc79c3cc3a594b74e411ec7fe`  
		Last Modified: Thu, 11 Jun 2026 02:39:10 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; 386

```console
$ docker pull elixir@sha256:08c44144fd03b42cd2bae36cba1a28cac427be21692efad35325151d544adc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129813982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83357a701fdbb230f40efa7e6b97eecbc20783bd337c6d271404df2b99894b`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:15 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:47:15 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:47:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:15 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 02:37:23 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Thu, 11 Jun 2026 02:37:23 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:23 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900e4402c04bc69094419c633f5733fffe690e92741fcd6207b01ba709fa969`  
		Last Modified: Thu, 11 Jun 2026 00:47:28 GMT  
		Size: 70.4 MB (70390386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0effb19f9ff8ad4e5710f73ce3e3f62b9649a9d60b2340592db5e264147ab2`  
		Last Modified: Thu, 11 Jun 2026 02:37:32 GMT  
		Size: 8.6 MB (8588033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6b1ccb56a6be3121a289126050a475db4de9dbeb36eb539a9269e25b6e773fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728d659823de6315466c8aa7d75be08b8c148f52c9ab261d93a51f91ce639ecd`

```dockerfile
```

-	Layers:
	-	`sha256:4a0dbd92b1096b20a227050a7ab10a4439ca8a532ce22c7d44d8f60e437cacdd`  
		Last Modified: Thu, 11 Jun 2026 02:37:32 GMT  
		Size: 3.3 MB (3288635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463aeba42f5c63aaa8988dc8db4ffc21bde7f1949e0977e3e7c7d1018c1a980a`  
		Last Modified: Thu, 11 Jun 2026 02:37:32 GMT  
		Size: 10.6 KB (10594 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:63b2db3786c4f817764ef89243c50aa8c6d1e08303a43d27d2101df20468b27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133098059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d476335b7ed5cb536fe304b1bdf088500a6d70610398e844e0c59c15dac60ae`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:28:51 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:28:51 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:28:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:51 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:12:54 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:12:54 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:12:54 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49be04d35f27c984f77217c21736346912de4a0a2b0856557ec5315e725667f`  
		Last Modified: Thu, 28 May 2026 18:29:22 GMT  
		Size: 71.4 MB (71377321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d194ddfb39f9f701448a63feb797ca55130cbe3099a5862b4dbdadde6319d4`  
		Last Modified: Fri, 05 Jun 2026 17:13:22 GMT  
		Size: 8.6 MB (8588556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:34f26fc8117373d7dac667024bb07fcee63415bb6a4cef425450b8e9ef09ef88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cc80f8dad0ff73fda134826290f04b5f0face03fcddba0c1bf628c7f28aeb0`

```dockerfile
```

-	Layers:
	-	`sha256:b171b627e1510f573a28969b875cdf411fe8fec05d9cefe78936da7767b006dc`  
		Last Modified: Fri, 05 Jun 2026 17:13:22 GMT  
		Size: 3.3 MB (3295067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b172893e891b942b3384105bfb9a3fbb26bafe510ef173c58051852a095eaec4`  
		Last Modified: Fri, 05 Jun 2026 17:13:22 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; s390x

```console
$ docker pull elixir@sha256:f477d4945a8ba519ee92e58076297311eb71a5021f58c9100c09275dae81eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129254440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3030f9281a89b9bab6732215ce2aa10dc59ccb4936285373b2a3566c855cee`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:47:39 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 01:47:39 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 01:47:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:47:39 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 03:57:48 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Thu, 11 Jun 2026 03:57:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:57:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d151de08a3d978174fc5c18c92b4d5ebe806b9c410fd15bbc74da428cee477fa`  
		Last Modified: Thu, 11 Jun 2026 01:48:00 GMT  
		Size: 71.3 MB (71280538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d00d742c02f6c0ba5d74f1c83de644d426a13e66a3e70bc2d9f85c8e0fab8`  
		Last Modified: Thu, 11 Jun 2026 03:58:02 GMT  
		Size: 8.6 MB (8588005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e9267418b95a949280925d6211c5ef8057702b6f83f61048532b83929dcf97d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d996cb7d8408824465c635fdd7a16988758a8b0f059dbf17f47ced78770439c5`

```dockerfile
```

-	Layers:
	-	`sha256:8d92155cb0f5d987b9e58fb37a1f3c85632194174bce90c40475b69e67f01524`  
		Last Modified: Thu, 11 Jun 2026 03:58:02 GMT  
		Size: 3.3 MB (3292911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f80b3ca63fad8b7051d157f44e58da2f01830ac6f2a84ce79d69f56a80f946`  
		Last Modified: Thu, 11 Jun 2026 03:58:02 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.in-toto+json
