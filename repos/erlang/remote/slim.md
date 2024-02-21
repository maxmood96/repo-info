## `erlang:slim`

```console
$ docker pull erlang@sha256:58615b200f607f679c1ad49e37c239f7c526990edc4725d05ff40de13b595096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:0dd1a3ee560a8ed89b065cb061739fd0a449d4247a67180081aefb8dad6f329a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119791430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a60baf38a2e2dc157261c7b18f2450340e3f3520472b41d77f88e5e633726`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:33:40 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:33:40 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 02:39:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:39:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dabd8cd72b852783c358347540192f95df89064d7d8bdb4666d525817879d8`  
		Last Modified: Wed, 21 Feb 2024 03:24:15 GMT  
		Size: 70.2 MB (70238825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:b64a3f660c6fa3fbedb1bda8604ddc74b8e21406e938e17696bed4597eecb0ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107686235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6c0b3d1589614c16c1ce8c49c35d5290fb223a39d080e0676bc19709b51ef1`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:28:07 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:28:07 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 02:38:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:38:22 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa26c2908685d6497265ef76d5aa05c457f1652fdb794b0f7bb082d4b79221e`  
		Last Modified: Wed, 21 Feb 2024 03:27:58 GMT  
		Size: 60.4 MB (60374466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1426e2c38d1ad49fc8a9abe66ef31bdcb795fb3dd0961b2ee6b5d3ee3cf9823e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105126744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbecf1684b41bae88bce2cea64c755f2485e7769be7e3021e99a81f26090f595`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:55:31 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:55:31 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 02:04:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:04:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9381bed1d32560d1c92aef1f590146c1ad595d8456ee7fea02cb3360484885`  
		Last Modified: Wed, 21 Feb 2024 03:18:57 GMT  
		Size: 60.0 MB (59973132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:5cb9c2f3d7e41153f64c9c21c4e4249fcb57fbde9912fb6528aa93f5c406baa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117457710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7694b5cb7736bb5ed545f7e97fedcc0b9327c2e466f617a1d4d56410715cb4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:25:49 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:25:49 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 01:29:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:29:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc22a135fd195a102fd04ac262e48b51b1140364d49da62997711d61128819e`  
		Last Modified: Wed, 21 Feb 2024 02:00:03 GMT  
		Size: 67.9 MB (67866745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:7c384394a22b16a873b07c2086e7b4e72c77a350b13db555afc83f4e9e35b017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114390391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c1f448f4debd1837ded34d30cca011e1e3bc936ef890d37f0274a132604327`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:54:52 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 13 Feb 2024 01:54:52 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 13 Feb 2024 02:03:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b6c9001eb0e1f62c8f7f543a41bc2a6ea89dadd6d18d77ba7b76f7f8e95d00`  
		Last Modified: Tue, 13 Feb 2024 04:35:18 GMT  
		Size: 58.3 MB (58332607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:fc68ed6cfef9daaee8b0ad33cbf9b2552c3d781bb50bfc09e44506da2c524c89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112279447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd84be9ee764792ecbfbc5a98ba4ba5890350b905a30865d24c12919a66f213`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 05:15:50 GMT
ENV OTP_VERSION=26.2.1 REBAR3_VERSION=3.20.0
# Tue, 13 Feb 2024 05:15:53 GMT
LABEL org.opencontainers.image.version=26.2.1
# Tue, 13 Feb 2024 05:40:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d99eab3af908b41dd4d7df38f0b02a447579326dd6604f641bbe9f2789b5656b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 13 Feb 2024 05:40:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435bdab12e1154a660e66f631e82465185743c8c08a279786f73c73585674d8`  
		Last Modified: Tue, 13 Feb 2024 07:37:31 GMT  
		Size: 59.0 MB (58976174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:4d4decebd7ce96b05824d4d72ed31fff4e46df87f57918a856490bad4ef662e8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115620380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56ae12df1d22651997b2f4fbe803272b54576d870785ac7353eb14b570e52ac`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 01:49:53 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 01:49:54 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 01:56:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:56:12 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56afec00c5213ead556aa0ea69272a51d250113f00f57eb13c7cb30c9e35cf6`  
		Last Modified: Wed, 21 Feb 2024 02:41:18 GMT  
		Size: 62.1 MB (62063850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:048712dec65bfa36afe0c9b1d34710b3e1690894a18822569e7e7a9ae3fde067
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108705767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ae68b218482b4b546d860332fc0a78d1998d77709357ce93dbf64f87cdc6e8`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Feb 2024 01:00:04 GMT
ADD file:1d9e47125f6551ab7fe22f20edbc4adcadd5218dbdfb7a047c97e717d6324a3b in / 
# Tue, 13 Feb 2024 01:00:07 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:31:04 GMT
ENV OTP_VERSION=26.2.2 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:31:04 GMT
LABEL org.opencontainers.image.version=26.2.2
# Wed, 21 Feb 2024 02:35:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="93c09aa8814018c23d218ac68b2bcdba188e12086223fbfa08af5cc70edd7ee1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:35:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:da89920af3bd14aecc5a727fd1657da55be3de461026b5a06f2322c69a889fe3`  
		Last Modified: Tue, 13 Feb 2024 01:30:04 GMT  
		Size: 47.9 MB (47916307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760863d4c0580be60896a56ae505a8b2590ea2f4144b205c498a0eb5d0268131`  
		Last Modified: Wed, 21 Feb 2024 03:22:21 GMT  
		Size: 60.8 MB (60789460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
