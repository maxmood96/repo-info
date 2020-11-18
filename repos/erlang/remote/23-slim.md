## `erlang:23-slim`

```console
$ docker pull erlang@sha256:5e11921bd8652edbbd6040aac25c5893cbd64ec45c5c30f779521bc28888dc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:23-slim` - linux; amd64

```console
$ docker pull erlang@sha256:355629e7c68b6152b229ddd4a9c024caf208f58328208945a3848e24294edd5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111040727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958b3f7ee1d6f660e3b67217c5a4b53abd5ebb1cda3b2096db52ad04d12c9a7`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:58:42 GMT
ENV OTP_VERSION=23.1.2
# Tue, 17 Nov 2020 21:58:42 GMT
LABEL org.opencontainers.image.version=23.1.2
# Tue, 17 Nov 2020 22:14:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:14:06 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2dd9b3e4b5c8d949dcce1c0722c75c8d28e7ef607196bcc98fabe3aea07e49`  
		Last Modified: Tue, 17 Nov 2020 23:51:50 GMT  
		Size: 60.6 MB (60643002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b2c650c9ced53acef226cfc4a91d94780435b040493b28df86d18f2cca9691a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b766311757264ae5a0a9804e88fb8f11d27a1813f2a0271b6be7db02e64bb2f`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:02 GMT
ADD file:e03270d36cef8171f1f6303860ff31bb1c0eb10642b8173bfdfef9f77fa4f89c in / 
# Tue, 13 Oct 2020 00:59:04 GMT
CMD ["bash"]
# Fri, 06 Nov 2020 19:21:02 GMT
ENV OTP_VERSION=23.1.2
# Fri, 06 Nov 2020 19:21:03 GMT
LABEL org.opencontainers.image.version=23.1.2
# Fri, 06 Nov 2020 19:27:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 06 Nov 2020 19:28:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5c0fdcca2cbb5e316a288f39c8c2006f45544568ea04623c036e0b1faa066bbe`  
		Last Modified: Tue, 13 Oct 2020 01:08:04 GMT  
		Size: 45.9 MB (45869258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5f9fa0cdc835e24a96f875925407326c09bd8d16b1a4a525c6d2e083a9e85`  
		Last Modified: Fri, 06 Nov 2020 19:36:52 GMT  
		Size: 56.5 MB (56457407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f35958b384f7e9333e6ae675feee6cc75000ffacf4df94dd390ee0eeff96dfbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106750098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b40df3a2577a9db5ab62ffca13cf2886978f2b2745ae7537b1c09faa12da16`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 23:05:24 GMT
ENV OTP_VERSION=23.1.2
# Tue, 17 Nov 2020 23:05:25 GMT
LABEL org.opencontainers.image.version=23.1.2
# Tue, 17 Nov 2020 23:12:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 23:12:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc47a0acb833ae8bfc7582767350f89d249d07ceb453d9fe4a6f7f964f99d36`  
		Last Modified: Wed, 18 Nov 2020 00:49:17 GMT  
		Size: 57.6 MB (57570883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; 386

```console
$ docker pull erlang@sha256:ffdde3cc863ce2b8fc000e885b1d350edb301224359f64a4a43c85ab47faf23f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111164766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f4756e454680f685e2cf8b65fe98e838b786753cdac2e819f0ba377555a075`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:39 GMT
ADD file:4805e11ec22df9454eb4759523111e031e84c8078bcaef178f089baca9e83cdb in / 
# Tue, 17 Nov 2020 20:19:40 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:58:34 GMT
ENV OTP_VERSION=23.1.2
# Tue, 17 Nov 2020 21:58:34 GMT
LABEL org.opencontainers.image.version=23.1.2
# Tue, 17 Nov 2020 22:14:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:14:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:21c39c42a8e082b1b164b44e463e4752c74821dbc51451f2ac2518ae6f29dff3`  
		Last Modified: Tue, 17 Nov 2020 20:26:25 GMT  
		Size: 51.2 MB (51159492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e47b688a15d5e9bd391bae3b49ee1d47a6124fd9f55a72a1dfba6b230f85752`  
		Last Modified: Wed, 18 Nov 2020 01:26:15 GMT  
		Size: 60.0 MB (60005274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:601b38465bf6b40eac843ab078f52132e2fb7ebf1611ad7a6fc032399f6c1532
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112645894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e1d80c0fbd8727013a8b06ff1add9a1a9a3337019463802c4951328572dcd2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Oct 2020 01:37:39 GMT
ADD file:339c3116c875720e7ba27e67ec6c60bc913e8108f7cccce90537c0915c5130a5 in / 
# Tue, 13 Oct 2020 01:37:48 GMT
CMD ["bash"]
# Fri, 06 Nov 2020 22:28:04 GMT
ENV OTP_VERSION=23.1.2
# Fri, 06 Nov 2020 22:28:07 GMT
LABEL org.opencontainers.image.version=23.1.2
# Fri, 06 Nov 2020 22:42:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 06 Nov 2020 22:42:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b5d2617265f370f18bc3d48beee684b1ba0eb6a2b02f813353f4bbd7084830ff`  
		Last Modified: Tue, 13 Oct 2020 01:49:15 GMT  
		Size: 54.1 MB (54142565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fe39d48ec0bb2f5460a4258c7f81663fcb6925cedb61a55d152e72e5a34953`  
		Last Modified: Fri, 06 Nov 2020 22:54:02 GMT  
		Size: 58.5 MB (58503329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; s390x

```console
$ docker pull erlang@sha256:0d37558c464e59187e05e5ceedf85110650871c1c9ce149ba931cba42c33202d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106562730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440d9e53197a8683e66f23e45619180b9e6fcaf817b7ee69b8f2048a27191d9f`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Nov 2020 20:17:56 GMT
ADD file:dfb1d2f775a9c4493397d0ca05aa6486393c6dad4f0fb5f48ffd209397301bdb in / 
# Tue, 17 Nov 2020 20:18:05 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:53:14 GMT
ENV OTP_VERSION=23.1.2
# Wed, 18 Nov 2020 00:53:15 GMT
LABEL org.opencontainers.image.version=23.1.2
# Wed, 18 Nov 2020 01:04:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 18 Nov 2020 01:04:08 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6e95a7d20e6bbf957d2bb5912f19784daba6953d8afac5562453108dd45940e1`  
		Last Modified: Tue, 17 Nov 2020 20:23:18 GMT  
		Size: 49.0 MB (48968246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9cdb392a703b378a5ab12c8dfe222a4e4793c916a9ab64e4011e13821649b1`  
		Last Modified: Wed, 18 Nov 2020 01:29:56 GMT  
		Size: 57.6 MB (57594484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
