## `erlang:24-slim`

```console
$ docker pull erlang@sha256:4bca2b3abdeb7796b082817597a21b00232ea67aa12e2fe59a3922614b3d1c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:9c2256ee01264d7b373e1503c92b94ab5d93496826849e57287a41d7f96a2fd5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120141615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8172bbefaaf967d8251c67df820661a19752ec576a0014f35b9e33c47789f5db`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:31:56 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 02:31:56 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 02:36:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 02:36:22 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694cb9681f23f8a4e8de74d7ef176fa239a268340f3287bba05f74a1496aad3b`  
		Last Modified: Wed, 11 May 2022 04:09:35 GMT  
		Size: 65.2 MB (65195993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:43caa35f900218f538ee0c8f0f031728459b7802493ec6ca8e9c3077a54e6c3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107308393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbf85bf1b7d24de0e5061a6df1d504e2e5a522d69373ac001ccff2297746b01`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:47:44 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 04:47:44 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 04:56:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 04:56:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261ecf8bf0983c14fd26fa61d00af7c02dcc8242680b3b35cf49ca8d54f21fd8`  
		Last Modified: Wed, 11 May 2022 07:29:31 GMT  
		Size: 57.2 MB (57174324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:279c738af7668084cccb55dee0e57bc6ef176edffed75b3086be95c577036c08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111649497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bb3b1199f348e6019301c429f09eba4ecad4b5cf58523d0bf4394aed5e0c42`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Wed, 11 May 2022 12:43:31 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 12:43:32 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 12:47:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 12:47:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a51631729927ab7b5bd10be1135ebfecad0855917e93ae452fe2ab3613b14b`  
		Last Modified: Wed, 11 May 2022 13:58:25 GMT  
		Size: 58.0 MB (58015160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:9edd51d9d13b2f374216b567d5fa67b6f54ff1bdcf9eff5a8115a0148a71249f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113598842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87940d05d211d67c470d212a23d5e3ca0b26c3431a043f6d95a7339e99da820`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:38:57 GMT
ADD file:dae3dc662d1327f461e95b84f6f9282f3c4fb51f16ac8f20a5f141951d8436a9 in / 
# Wed, 11 May 2022 01:38:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:47:52 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 02:47:53 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 02:52:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 02:52:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5ad4f92623738998bc77103ff64344255f842f6e5fe4a846df656351b3c4852f`  
		Last Modified: Wed, 11 May 2022 01:45:53 GMT  
		Size: 55.9 MB (55942833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b287c64a63531f2d64ba9cd4bffa755a78654cc93b05ac48a3b9f79450526c`  
		Last Modified: Wed, 11 May 2022 04:08:48 GMT  
		Size: 57.7 MB (57656009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:22e5be2eae418b8f689d9291c302f011885656b0cab522c9137a33b6cf12d9f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117457850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c25adb7afdc6c95ba37426af19c5cc3b2d59796784900a98113471955686c`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:52:36 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 04:52:41 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 05:02:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 05:02:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f59846878b23c4849bb587f87350d519c91c5b03245bf285040f1df769d11`  
		Last Modified: Wed, 11 May 2022 06:05:01 GMT  
		Size: 58.6 MB (58621326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; s390x

```console
$ docker pull erlang@sha256:231d65b4c2335a7302d38ebd18c6b310e04ba77ea8a22100b7cd263c66131f89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111356414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce53274f758a91ff752681269d15c572519bb93c34590147313a1418591b3a8d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 00:43:58 GMT
ADD file:8b9cfb1e16e1c11cdc1f936ccd3dfdd2104ab85b0b9078b1fe3bca89f53e0682 in / 
# Wed, 11 May 2022 00:44:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:58:23 GMT
ENV OTP_VERSION=24.3.4 REBAR3_VERSION=3.18.0
# Wed, 11 May 2022 01:58:23 GMT
LABEL org.opencontainers.image.version=24.3.4
# Wed, 11 May 2022 02:02:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e59bedbb871af52244ca5284fd0a572d52128abd4decf4347fe2aef047b65c58" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 11 May 2022 02:02:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f8313f715dc1cdd9f8a3da73eafca06dcb30dff4c078bee35a162247cae99c4d`  
		Last Modified: Wed, 11 May 2022 00:49:41 GMT  
		Size: 53.2 MB (53208696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aef07865d75c9ef3d2ac1502970c20103a98423bceceafbe4f733c9fe467f5`  
		Last Modified: Wed, 11 May 2022 02:27:38 GMT  
		Size: 58.1 MB (58147718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
