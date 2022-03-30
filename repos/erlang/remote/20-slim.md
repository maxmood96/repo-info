## `erlang:20-slim`

```console
$ docker pull erlang@sha256:2d5ef0b55b4e6f6d75c5aa974800d34a0077971dc64dce265e741a1f8ef8e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `erlang:20-slim` - linux; amd64

```console
$ docker pull erlang@sha256:6c82c6212c6b58660b98f61c0532094f3f0cbca334a198eab3bd1ac16a1479f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111834957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e819dbf330a9c81a970d67bd46a12c7d1b4bdbd9ca5e1073ae9b6b55587d57fe`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:48:05 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 29 Mar 2022 07:59:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:59:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66701d3567cb25f8e892fc5a413416dcaa7983585470a25179905d09fc734f`  
		Last Modified: Tue, 29 Mar 2022 08:36:42 GMT  
		Size: 66.4 MB (66407490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:20-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:36d2064cb077dbc5d14bbc686cdf38dc1eebc16a59c7935bc3c72a0efac1c4ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103534470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3396f4b6b90a8a669d5f9031619862c3ac84897ae2c5bb5ebe8dad6765e6a879`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 29 Mar 2022 02:23:57 GMT
ADD file:3dc1697adfcf63a288e9ec7a2c40438b8ba2ccfff0382a1ed5457f30d7a37f76 in / 
# Tue, 29 Mar 2022 02:23:57 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:04:40 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Wed, 30 Mar 2022 01:13:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:13:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:aecfa9e0b0179abf68bebbcfc35453928546e01ad1c8b6eaadf759360762dada`  
		Last Modified: Tue, 29 Mar 2022 02:40:33 GMT  
		Size: 42.2 MB (42151158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f294a767650ad1adcb40160e5b0d07d0677953b7b73980b9441c99f23ec6d029`  
		Last Modified: Wed, 30 Mar 2022 02:03:27 GMT  
		Size: 61.4 MB (61383312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:20-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8392ce5db6e0e05f74108e0feedfcd724f133063fbbf01e3c1748c9d878adb51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105776118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737ab7650f9d81310b917309900eac90172cb0cd004a200d6b0cbd681471ef2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 09:47:34 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 29 Mar 2022 09:52:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 29 Mar 2022 09:52:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b518475e4fe04eee3703e62719456e0202079bd60efc89222fcd56030d6e9dad`  
		Last Modified: Tue, 29 Mar 2022 10:18:37 GMT  
		Size: 62.6 MB (62563281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:20-slim` - linux; 386

```console
$ docker pull erlang@sha256:1ad64514c4ed2c89b10163f6abad0f010b155c513d693dc7d1917a18745639f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115631244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860d6ebbd108d9e7d2fcd3abb2562e54dc2d98ed47ba553aba89fcaa37a3541`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:09 GMT
ADD file:74aa6d4005ba30e0fb6af0b75158bccd03c55e837be6f73f1c2929f62028a19d in / 
# Tue, 29 Mar 2022 00:44:10 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:15:52 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 29 Mar 2022 05:20:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 29 Mar 2022 05:20:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d8b8952dbc41a74d8004d044b352e7f612041bf00ab66401180cd3af79d35a14`  
		Last Modified: Tue, 29 Mar 2022 00:53:10 GMT  
		Size: 46.1 MB (46147573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4318cb5e3c92e257146f2a86886ceafc5ce4c12ede8f46e2d2d45999d4c0102`  
		Last Modified: Tue, 29 Mar 2022 05:44:23 GMT  
		Size: 69.5 MB (69483671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
