## `elixir:slim`

```console
$ docker pull elixir@sha256:df3be366eed78517ae6610a7b8cfc87cf25628d8be2adb6d8c61873b6cfb8dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:cc2c17333b957a3ffb700b375da5e637891d49dae60415c11fd3dc2a734f3094
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118797378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8075f4e0a5be5a4a3539b90f34858268eb622640a63d6449ef3b0ec9d7f39f94`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 22:32:13 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 22:32:13 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 22:39:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 22:39:56 GMT
CMD ["erl"]
# Wed, 24 Mar 2021 23:16:11 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Wed, 24 Mar 2021 23:17:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:17:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410745db298519c8cd1f1e1605e67e413dfed8dc9865a8d7d564ff0cc39e7f14`  
		Last Modified: Wed, 24 Mar 2021 22:57:12 GMT  
		Size: 60.9 MB (60906238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703f845ca7f78bbc6b6b15a3ca90dcc3f44fa8877801c63e8ec496c325599ddc`  
		Last Modified: Wed, 24 Mar 2021 23:21:56 GMT  
		Size: 7.5 MB (7490787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:3d7af41d3a7116e75789c96e38c46ed23aa55176f9a18ad7d0f700d0640c4bdd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112755493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854b0a95c356c8f0dd8453581b8d4c5487ce4c4a659eb79bbcef4fbf2e842ec0`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 23:11:10 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 23:11:11 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 23:18:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:18:05 GMT
CMD ["erl"]
# Thu, 25 Mar 2021 00:10:05 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Thu, 25 Mar 2021 00:12:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 00:12:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a80be836cfe4fdd5ccc9c108e803c80245abc6a3ceddc0615965a88a99ef75d`  
		Last Modified: Wed, 24 Mar 2021 23:27:56 GMT  
		Size: 59.4 MB (59396971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e02b0620b08c60f5940a2748e506acfcffddd9c6184c2f76be2c77debd47926`  
		Last Modified: Thu, 25 Mar 2021 00:18:02 GMT  
		Size: 7.5 MB (7490402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:ffe116bc387436fbd7a6bb3e5c12c9806a74ec76ca284236b97c64196bc4952a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114497504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93842f21732c17e4dee341cab7acaa1dfdeb02b4a0eb2076c8d11ada5fd8a2d3`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 22:51:06 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 22:51:07 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 22:57:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 22:57:12 GMT
CMD ["erl"]
# Wed, 24 Mar 2021 23:27:04 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Wed, 24 Mar 2021 23:29:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:29:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a64ca526f7bf430a43e0317a566bd76dbe038dd4aa4a6211cafcdc6d658b695`  
		Last Modified: Wed, 24 Mar 2021 23:07:50 GMT  
		Size: 57.8 MB (57811117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5311b40177e3a654ce445f4145c7a95923d1783ba4d7f32178139c8a0790a`  
		Last Modified: Wed, 24 Mar 2021 23:34:44 GMT  
		Size: 7.5 MB (7490624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:daeeaa837ebe6464a3380deeca319811f935c22d023387ea6fa96f54dccc5b0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118922786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5248a974e313eff5ee6bb75f1392292785da97b37930a4147fcc0fa7551dea`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 01:44:10 GMT
ADD file:7fc865376477d0a3207f0488aa53a01be49cf76d0f075eb2d8dfb866f67472c2 in / 
# Fri, 12 Mar 2021 01:44:11 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 22:59:22 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 22:59:22 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 23:07:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:07:25 GMT
CMD ["erl"]
# Wed, 24 Mar 2021 23:49:37 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Wed, 24 Mar 2021 23:51:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:51:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a0450ef8e4ab4239c43726ef6f13a160860a6ab25f82c8f011ca37ee436324a2`  
		Last Modified: Fri, 12 Mar 2021 01:51:32 GMT  
		Size: 51.2 MB (51160386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71fe2770707e5f84cb5bad7b57aebff4834830cdbff434fa4b4d499a2373c0d`  
		Last Modified: Wed, 24 Mar 2021 23:22:28 GMT  
		Size: 60.3 MB (60271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd8de50021b6c5f5ad8d27be3921174d6de05cd43ca957eae3fad6449d319c7`  
		Last Modified: Wed, 24 Mar 2021 23:56:01 GMT  
		Size: 7.5 MB (7490566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:e6d4cd068847ac2330fada47192b855b49e5540ccf0fa0f76cd8e552012ce968
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120349349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1ea20f6d071400f9af728cbdf1229eb2def381bed70f7ad3d1318a001dfd04`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 02:31:55 GMT
ADD file:75cbd246f27dc871f6d43b196814d29950e19fbcf60ba31740b0f3b69d1eb5cf in / 
# Fri, 12 Mar 2021 02:32:10 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 22:42:08 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 22:42:10 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 22:52:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 22:52:18 GMT
CMD ["erl"]
# Wed, 24 Mar 2021 23:24:47 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Wed, 24 Mar 2021 23:29:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:29:25 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e82e55acc97d8fc958b57715031c249868ac5d8978e8d9f94ca4c15d553fe3cf`  
		Last Modified: Fri, 12 Mar 2021 02:44:17 GMT  
		Size: 54.1 MB (54136226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea15aaf5d06b7a0a16e1f49a57653b0c46041ba556955a6f72e66a16ae5a83f`  
		Last Modified: Wed, 24 Mar 2021 23:03:54 GMT  
		Size: 58.7 MB (58721705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8927ce84eb89dfa8ef65e6bbf0f8b10b15e1f2d2ec9b0ce4f384bd8152fd261`  
		Last Modified: Wed, 24 Mar 2021 23:33:50 GMT  
		Size: 7.5 MB (7491418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:b43bc89f428edcb5c52e705f5207a829dcfa2c014ba6e1d59d9a1edebe8e6a13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114323132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31c3c0342a54c6580df8d92fbbb4e18013147b8f50c78e9364056f6e39ddacc`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:42 GMT
ADD file:c1bc4d97e132d650b9f7848521ea163735e8d93b365da94640ff25e0e01bc891 in / 
# Fri, 12 Mar 2021 01:45:47 GMT
CMD ["bash"]
# Wed, 24 Mar 2021 22:50:24 GMT
ENV OTP_VERSION=23.3
# Wed, 24 Mar 2021 22:50:25 GMT
LABEL org.opencontainers.image.version=23.3
# Wed, 24 Mar 2021 22:55:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a9dfe9ea762b9f06f67af6074bed0f75705e1f114b9c45634db7d7cac2a293da" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 24 Mar 2021 22:55:12 GMT
CMD ["erl"]
# Wed, 24 Mar 2021 23:19:44 GMT
ENV ELIXIR_VERSION=v1.11.4 LANG=C.UTF-8
# Wed, 24 Mar 2021 23:21:01 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="85c7118a0db6007507313db5bddf370216d9394ed7911fe80f21e2fbf7f54d29" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Mar 2021 23:21:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2fc1f9e428b932a8750b1c7f11f48b4c9a41328e9107b957451d8b8efbfd3fce`  
		Last Modified: Fri, 12 Mar 2021 01:50:13 GMT  
		Size: 49.0 MB (48969030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b5948f84d87abc62e0be54ce77ce9551e566af5f29b90ecc5e186b133afc80`  
		Last Modified: Wed, 24 Mar 2021 23:02:11 GMT  
		Size: 57.9 MB (57863777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778458efdcb4b1ef1f1b2ec527d90fb29e34de6cc4c887ee7b6be409f60bf2dd`  
		Last Modified: Wed, 24 Mar 2021 23:23:38 GMT  
		Size: 7.5 MB (7490325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
