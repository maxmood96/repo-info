## `erlang:27-slim`

```console
$ docker pull erlang@sha256:71e80ae416d3a4242379cc9f3efff5d8e5632efd9a96756d2ceb00787a20155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:11468fd1c760abdaf80f77c1b9dd81ae396095a9355f2718a1504c51e86baedd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124841337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e2ab56cb62f40e212c6cdcc1f739ab14aa41de1c0cdbfa96db1551f1a31857`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:11:13 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:11:13 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Wed, 21 Feb 2024 02:17:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:17:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadbac891f05ce29e2aafc12672cfd12be11759c959edb3140c8741d9e3b0d5a`  
		Last Modified: Wed, 21 Feb 2024 03:22:51 GMT  
		Size: 75.3 MB (75288732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:d9e9991c9935fd5a0759a5092ede10cb91f221e1a5fdae36a46d264aca7837b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112149987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ac1aac245d9c55a51b765e2fee6f3d6d7a0ec57342da8e99c331eb2e355f2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:12:16 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Tue, 12 Mar 2024 01:12:16 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Tue, 12 Mar 2024 01:17:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:17:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23983655edd021b7c5981d1546ad45101a9601eabca4ab6d083a91aa696a5e4e`  
		Last Modified: Tue, 12 Mar 2024 01:32:34 GMT  
		Size: 64.8 MB (64837832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:f58655132bdfb9039ef41ca13a723baa2c7a6160de6e6ba60d27e9e5953ca06e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109599002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62b3f6f6764c2a1554e0430b8264f178907d32c0e90f284bd09a0cd7327f407`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:25:59 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Tue, 12 Mar 2024 01:25:59 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Tue, 12 Mar 2024 01:31:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:31:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b594d26105fc31d4d0c95e6e12ca5b151c8ade29a0cba015a88dff8b77eaf`  
		Last Modified: Tue, 12 Mar 2024 02:06:46 GMT  
		Size: 64.4 MB (64445182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bf8dc3161c1fa68a1e6cf282b3ba303695b840d17b053fe2891e3b3e3b54967d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122636895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fedc7f6908e94d6f57d8bb863162203159f9bbf92d91767a1060adf81ca86e8`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:11:25 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:11:25 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Wed, 21 Feb 2024 01:15:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:15:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b76d8996da98a6951032afaff5dbc6fd02b2a58339ed189e670ab54dcbd2f7`  
		Last Modified: Wed, 21 Feb 2024 01:58:44 GMT  
		Size: 73.0 MB (73045930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:54290da1024b8b7a416023ee6cec41e2662b49439eee77432e61ebd423a204dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116030413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3ced1ed8c4554795d09ee403363de5faadc085ed51e087e4f9981390a9f8e`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:08:47 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:08:48 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Wed, 21 Feb 2024 02:18:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:18:41 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6295372144dcfddedba9b29a4ff37e74df07f8225018f5c699d13bc0a67ff4`  
		Last Modified: Wed, 21 Feb 2024 04:05:39 GMT  
		Size: 65.4 MB (65448488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:cfc360a4b7617560d0421febc3b43499ed2c332109899e2d239c85c16d69f5ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114968262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fab845d37c5245ec9d0dd6a64103326e8f5e7731593881d38f219e8d5c8e4e`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 02:03:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Tue, 13 Feb 2024 02:03:40 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:55:47 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:55:50 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Wed, 21 Feb 2024 02:21:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:21:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b993c7ed71592e911c57e7dec7b2e0f62a31595f7518994edd5de69340ce11`  
		Last Modified: Wed, 21 Feb 2024 06:18:46 GMT  
		Size: 65.4 MB (65405096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:97979f474b25c5b1da04a1116c6d247503725bba9983e30b405e5c3b3e66faec
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120125673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d81b108df4c443684bf3fcfa9906f14403f7556f7c0ce28c800f132423ec03`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:27:52 GMT
ENV OTP_VERSION=27.0-rc1 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:27:52 GMT
LABEL org.opencontainers.image.version=27.0-rc1
# Wed, 21 Feb 2024 01:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e543ec72fd55ae0a8e7094a37e305e4de24d5c1b97044723cd67b74a74bbd32c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:34:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd946df9548dc5cf1410bab560cb6572c3d23de6ecf2415f2f79fd4a0ea681b`  
		Last Modified: Wed, 21 Feb 2024 02:39:42 GMT  
		Size: 66.6 MB (66569143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
