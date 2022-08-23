## `erlang:slim`

```console
$ docker pull erlang@sha256:be8c367c57db7ab16750132a8931c9163ed51891893bc4c33622fd9da41b75be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:38a93fb5d0e000e71b8cd1cbf818dc939a2a72f3eba704b5004b99aad1667b95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120582524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0b9d8a8b4e1421e58b331df31461e694096b8aad285036c8a9e31877ce76f`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:40 GMT
ADD file:6944d322f4c04bd2192061822af5cbec8ac0a6b424c461d66174d32aed604972 in / 
# Tue, 23 Aug 2022 00:20:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:15:18 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Tue, 23 Aug 2022 01:15:18 GMT
LABEL org.opencontainers.image.version=25.0.4
# Tue, 23 Aug 2022 01:20:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:20:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1671565cc8df8c365c9b661d3fbc164e73d01f1b0430c6179588428f99a9da2e`  
		Last Modified: Tue, 23 Aug 2022 00:24:32 GMT  
		Size: 55.0 MB (55007555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554fff9c63fb787594413dbef215753976476255e332060f7fda7e11fbe45f69`  
		Last Modified: Tue, 23 Aug 2022 02:36:47 GMT  
		Size: 65.6 MB (65574969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:237a7327b5621c0a741f701c29407ccd16256d583c09b58b941d0ebf4e8f6c19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107190548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc7a705c86592d4d3d255e1bb7654725d7f45c12c3e8be9cd724a407264e3e8`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:36 GMT
ADD file:4e2780cf1c53cc1c475d2ebae48d4bf03029fa68ba9fbc991be76ac9e3944977 in / 
# Tue, 02 Aug 2022 00:58:37 GMT
CMD ["bash"]
# Fri, 19 Aug 2022 18:10:18 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Fri, 19 Aug 2022 18:10:18 GMT
LABEL org.opencontainers.image.version=25.0.4
# Fri, 19 Aug 2022 18:17:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Aug 2022 18:17:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:05aa23077de69478dfc20e56aa2d54a2b13bbef07c4d2578524585d098af4e72`  
		Last Modified: Tue, 02 Aug 2022 01:06:07 GMT  
		Size: 50.2 MB (50195271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25663558452af80e65b8dcbf74d579ade18aee792867ad6982727414c835f253`  
		Last Modified: Fri, 19 Aug 2022 18:57:28 GMT  
		Size: 57.0 MB (56995277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:595cff76f3175c144ba8f80335ab2c0154cc33cce75cda83524ed1e399627c29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117765032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b588b7020b29aa9d33226b9528de8e6ec3e2ee499d6965f0b8774272addbb9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:24 GMT
ADD file:5972a7ce0f1d89d63e5ed48011838c998fa506cd34f8e5f0b0070039cd74c5b9 in / 
# Tue, 02 Aug 2022 00:40:25 GMT
CMD ["bash"]
# Fri, 19 Aug 2022 18:47:24 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Fri, 19 Aug 2022 18:47:25 GMT
LABEL org.opencontainers.image.version=25.0.4
# Fri, 19 Aug 2022 18:52:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Aug 2022 18:52:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:114ba63dd73a866ac1bb59fe594dfd218f44ac9b4fa4b2c68499da5584fcfa9d`  
		Last Modified: Tue, 02 Aug 2022 00:45:33 GMT  
		Size: 53.7 MB (53683005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fa312fde460a66f4859b00e535fb1d1e4a42ffdd4f89da4818996cea88c53`  
		Last Modified: Fri, 19 Aug 2022 19:15:04 GMT  
		Size: 64.1 MB (64082027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:3cc58a15dac9268267acf54606b14828d20f6985d4661ba8c8481017ef5fd93f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113315568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cefef82d2cf4d1ae15a4c2617228ed8d717079b59e56ca46ceac297f7165684`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:24 GMT
ADD file:4012c41187a03bdb3d37bec80f6255a1d46582e3ed145b4f313e42196529e524 in / 
# Tue, 23 Aug 2022 01:02:25 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:52:26 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Tue, 23 Aug 2022 01:52:27 GMT
LABEL org.opencontainers.image.version=25.0.4
# Tue, 23 Aug 2022 01:57:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:57:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6f683b9c66ef80b527ee5e4cb11969c6e0c1400ab69a4f1279af90f5766d70c7`  
		Last Modified: Tue, 23 Aug 2022 01:07:53 GMT  
		Size: 56.0 MB (56012624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef78b0a2b5f7485eedf5244a9ef987c71640df86dbb5e3d2d162ec78b41a4956`  
		Last Modified: Tue, 23 Aug 2022 03:00:16 GMT  
		Size: 57.3 MB (57302944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:983c6deafd7965cbf6df65607d172badf9bad9866242bdc3aca3830682851f06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117272412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0d698caf5c8adc8983069e355ecbf7a15d0b3107230ea1fc8b00dc11e6ad63`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:09 GMT
ADD file:1f74997bc1d99e4422725846bbc41271bfe62a55c74ceca37359472aa428233c in / 
# Tue, 02 Aug 2022 01:17:12 GMT
CMD ["bash"]
# Fri, 19 Aug 2022 18:27:57 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Fri, 19 Aug 2022 18:27:57 GMT
LABEL org.opencontainers.image.version=25.0.4
# Fri, 19 Aug 2022 18:34:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Aug 2022 18:34:59 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6e9f012d4ab4ee25199c288014d1f6269e3700e4e09eb5ae543813498561f2fe`  
		Last Modified: Tue, 02 Aug 2022 01:24:00 GMT  
		Size: 58.9 MB (58895967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0a9a229d766cb9ae0ad75201c65c687b3b5823f9230d263ef12ff053ea89e1`  
		Last Modified: Fri, 19 Aug 2022 19:10:13 GMT  
		Size: 58.4 MB (58376445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:464c3cbbf1d9ee4b4d52fd3c4ffd499730a811d45b56256dc68d25e05773355a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111194903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f059ccdad67e9a4d7858325cdab7ebb1351ca9f3019998e6447cbc1ab3a38863`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:09 GMT
ADD file:86774aefa6717c0535c25f8700d8730f44cc43c33371edeb7dbd33e29cb68d32 in / 
# Tue, 02 Aug 2022 00:42:12 GMT
CMD ["bash"]
# Fri, 19 Aug 2022 18:49:06 GMT
ENV OTP_VERSION=25.0.4 REBAR3_VERSION=3.18.0
# Fri, 19 Aug 2022 18:49:06 GMT
LABEL org.opencontainers.image.version=25.0.4
# Fri, 19 Aug 2022 18:53:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="05878cb51a64b33c86836b12a21903075c300409b609ad5e941ddb0feb8c2120" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Aug 2022 18:53:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:718eef7927531d5ec3c355d6b6e5c4ab83c23778e693b087ac8a3b9adb4f63e0`  
		Last Modified: Tue, 02 Aug 2022 00:47:40 GMT  
		Size: 53.3 MB (53269308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fed363b6191b91ff1193e6342a52cb39f2b93adbf0c08e6622f6462313a82e8`  
		Last Modified: Fri, 19 Aug 2022 19:16:36 GMT  
		Size: 57.9 MB (57925595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
