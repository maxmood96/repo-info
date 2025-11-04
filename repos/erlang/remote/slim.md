## `erlang:slim`

```console
$ docker pull erlang@sha256:43856f2619206fbdb354f3bd4fc46d95e073a7b59d8d241d224a853a56808273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:f60b1162637902aa09e36c01287ac2012498bcf1ab8549aba0736d919e360510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128994829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79577bcc816814b98e2bf9b35a6a4ca3dc082ed97517c3cdd57e2478769c2ce`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1921f4bb5301309b922e403a2e06c4d152188df9ec771ad1d1ec26b2a005aea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374d9a6f996dabccefa430452e99565bc0d89986500f46093240fd3d671f0de0`

```dockerfile
```

-	Layers:
	-	`sha256:fd6716e54a04c3e3913f14ce27014157823411468f3b478bd560cfc0bf71a7c8`  
		Last Modified: Tue, 04 Nov 2025 08:48:33 GMT  
		Size: 3.8 MB (3824252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016951dc22fdff1c11a6169bd79e03fa263355fce1765ae85b7b15cf1caad17`  
		Last Modified: Tue, 04 Nov 2025 08:48:36 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:21a118b540e11303fcfc155193ff9a212b9f55d47c2a819911bf4de04993bb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116228114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8092dc11934f186e9f0bf27a20687a1b324313f15363da7221037589d938258`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:30:16 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 01:30:16 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 01:30:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487d0e5129964b1cfd6e6f502399fd3b6c56bf5cbbe7e7e271d1d49b837e6ece`  
		Last Modified: Tue, 04 Nov 2025 01:30:40 GMT  
		Size: 70.2 MB (70212025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f7a8d399070b65aebec9b10a12d661ac46003b566b2fca6c0babe1bbe2a9a0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718474d8a2657e18762b1d5eb8b8857c1da4b86e30e1057744012c2a0d6e014a`

```dockerfile
```

-	Layers:
	-	`sha256:4672b534eafe33b82b485bbfe0313e81e467b61a2dd0ddc858d9055201c35d7e`  
		Last Modified: Tue, 04 Nov 2025 08:48:40 GMT  
		Size: 3.8 MB (3828068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86de07024ea18d08fc64895c5453960e002217df34395b7b2ca862b68215fa51`  
		Last Modified: Tue, 04 Nov 2025 08:48:41 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:28dd8593786681156886141067c675d0a3ae84acf50ecfa7991e93a6379ee126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113806594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964dc2b63d52fee3b0de0ffc47e93be689e77573093979ddbe61041c0c99235`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8c87a8d460f5dde4f690c14e8f1d287ddd011b5322c7ce300e227e6e014493be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5966a59839be6fd4ae28163831121cc57a03862511ad3f209c800d3fa28860bf`

```dockerfile
```

-	Layers:
	-	`sha256:4bb891b7044fb888ef61da34473fdf4cf7d3befdb5f31adafe4cb0cf2314c007`  
		Last Modified: Tue, 04 Nov 2025 11:50:04 GMT  
		Size: 3.8 MB (3826493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb6b6340f8713a894d11851f1d29accd768decbeedf07318fd2071ee52ffbde`  
		Last Modified: Tue, 04 Nov 2025 11:50:04 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:7534f7ea81ea768b21f4fcb593a81ff99de4c8907cfbdd454c25f83a8d7b0268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126679297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76324b8b2b76dcc1c3f118a506232ad60be1f05a617a9d2bbd0e05c54d7d0087`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e836458fd0a54bf985adf4241ba3000cfffaed5aa68b412654d4a97a52ff26f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed68aff8eeb3a617701493a653b3fe01f56ce9f3d0cd703da425ac516ffc19c4`

```dockerfile
```

-	Layers:
	-	`sha256:9190e8f72bd9192aa5e5174f099315a3e987300356752db63cb4b00fc8a4b6a3`  
		Last Modified: Tue, 04 Nov 2025 11:50:08 GMT  
		Size: 3.8 MB (3824525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60abf3aed27de9a4cc9e46436ac40787163cfd44dfcd59dd29a04a97797cd884`  
		Last Modified: Tue, 04 Nov 2025 11:50:09 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:0f732aab08b0f7b5c0621c6881b258fe15a5a01f2b76cbe29fd7a941427820dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120191892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d87e0a57f76927437691e53dccec4a15921e7b9fb8acf8d14cec5aef3c29d7`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4879ce1ec96b11ab7e5c0b13132310f4b4a164a9e333458c2a41badc2b906681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aee7a9a288af3beb93d08e19785b12f8dc3874cab001c981492cdd5ed7c2d7`

```dockerfile
```

-	Layers:
	-	`sha256:a31e3010b69743bd4e5115faf24e82f96ba7057ec1a24ae7238549ef350e854d`  
		Last Modified: Tue, 04 Nov 2025 10:52:23 GMT  
		Size: 3.8 MB (3821409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8ab12cc02a198c6844437925912474c13296cb91fd268fac67abea3112d809`  
		Last Modified: Tue, 04 Nov 2025 10:52:24 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:3faa9424e942d6bd408db7c278cf00ceeb754b3daf65553e6f27015813b13005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119433032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1427ea6fb335cc14008d661e43d0368a34384a2d525edf627da5a676dc040`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Sep 2025 16:00:47 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558dbd2b8acae4fe0d2ef4e31ec88a10f59936b51b9c9ad7db4883e38fe4b4d9`  
		Last Modified: Tue, 21 Oct 2025 18:10:05 GMT  
		Size: 70.7 MB (70672289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:03f35aa38433e82dee39c764a181a2fec865bf53d67b8288c4cc0ec1ab494ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ae8a341104a5b08fbbdb2ddb5d5a5a84bac62e39a9ddae11f5d21c8479cd25`

```dockerfile
```

-	Layers:
	-	`sha256:a3ac77b23b35158814f4bf1831ac59e9e8d08923883049f869af84277d2e802b`  
		Last Modified: Tue, 21 Oct 2025 19:47:40 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:d34a0f72ad0884986d27bcf0341a21fa7b22b903e47d52c095de9aeaced3962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124077739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac7d16bc5abcedd824397d1d6ed313cb31fb1ee45c9bee67c55a8280f2acc49`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e33e19e19faa76407859ee9ee0a697449c06759e7e0ead39ce1670dfe096fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946f8a4ca2e2723fb55e8e6e583da6143478d493177eeaed8dc5629e72b4908e`

```dockerfile
```

-	Layers:
	-	`sha256:0622fe8d212b95001baaa16134932a6e558a9da8cb83751efee12db5d8a30d95`  
		Last Modified: Tue, 04 Nov 2025 08:48:58 GMT  
		Size: 3.8 MB (3828706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da15519c85ff96ad86b086a1702e72448fa960c6a702a859260bd12cd7946605`  
		Last Modified: Tue, 04 Nov 2025 08:48:59 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:1bc842206c65f35b090dfcdaa1115192e6f93c0aab4d58c089627a1862301e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117512162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8d3ddf2987268eda5ffe0073c4d03d9f6390a2d7f2f8a1f2dae46ccdf60a49`
-	Default Command: `["erl"]`

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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bdc3d4039b1b23e8667049211af5bf0be044679a15ee63778b2a95e865cf9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7455a4da357c68e98d52b84686c564076ea43a057db28da930902f90879fa1be`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7ad200accfc9d71b74687eeb4a2e228e7638cd8e5e036a1bd086a44221a6b`  
		Last Modified: Tue, 04 Nov 2025 08:49:02 GMT  
		Size: 3.8 MB (3821080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bfdc9da16c06f8e3ac4c1a375322453c19379fa9d8f164a9700f7ebf6b0bb03`  
		Last Modified: Tue, 04 Nov 2025 08:49:03 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json
