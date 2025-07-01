## `erlang:28-slim`

```console
$ docker pull erlang@sha256:20142af26c7a29527b6b533de49019f852498591f0505312c0b712b6fc153fcc
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

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:cf58e13f01497d4932bd2e10f216b99417aa3170f9e284291deecfc65b74fad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128449615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b0749f4f02a54d04dc2be13130a401ab35974172cd94cfab9c1987d009c7d6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565a3702d4647a881c9db90df9bac02603ad0a87c518d960a890413ad1174036`  
		Last Modified: Tue, 01 Jul 2025 03:26:15 GMT  
		Size: 80.0 MB (79955331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:038f8ae2b471f1b0061640508df13ccdfb790f540dbde713d5262b904ad33829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a22d3f5082652565c9f5d7dc00820d9c72aab27d72ab8f2a31595e9994b9fb`

```dockerfile
```

-	Layers:
	-	`sha256:7555b675e522a68dbe2907ac3ccdb4c4303d65bc0fbf6e46d58b9dd4e25517a7`  
		Last Modified: Tue, 01 Jul 2025 04:47:55 GMT  
		Size: 3.8 MB (3817627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a011db8d83a2a24486a9e80d181940a78277a3fe979e79e108c5fc3fab93f2`  
		Last Modified: Tue, 01 Jul 2025 04:47:56 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:68c1676edf4a4f9e3c9fd7e0b0119e1727679f567813fd95343296c31da5641a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115668562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714c6ffacef7734dc479ca2abac229e35743f25e2f4df54289a4efc3e4d7826a`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a24a557ede7ba5b65b2bd03940fd632ba97457fff3b9ff41f74c90772d712`  
		Last Modified: Tue, 17 Jun 2025 17:12:48 GMT  
		Size: 69.6 MB (69641975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f617a552d36b746e3cc01e12fcaa6d8a202312f37db5ee0afdb35864f58ab691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86314ad92059e61670bd32bf58fc74990d95e0475c33b65db98a05af0f1d4e36`

```dockerfile
```

-	Layers:
	-	`sha256:eae4bd62a55ee2aea9a350086c6243c4fc09b8a3c4e7c8c76dc8b7f8aa39fb7e`  
		Last Modified: Tue, 17 Jun 2025 19:50:17 GMT  
		Size: 3.8 MB (3821443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e346b6708f1796befecd87714c8f020b018f72d63f2769c10f55e2daabd9db8b`  
		Last Modified: Tue, 17 Jun 2025 19:50:18 GMT  
		Size: 14.1 KB (14050 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:db860097684eee71eba064b02bb18c639784b9edf663d3f36bada0923fe3c3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113263582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb391cbd2da7ca88c978763e69fa82ef08939c3dc628a2dd59cff5fc8153a9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a0027362a49c95ba6cac293bb0e9ffe5c5966cb809ae55b27a4595f1450bb`  
		Last Modified: Tue, 17 Jun 2025 17:12:29 GMT  
		Size: 69.1 MB (69055372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9c2f13fc8f56f96bc70851e26668f878ae5baa33392147dc1e98a4c8b233e841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d054d18903cbaf899973a8f204bc0d94e44ce3411840681c6e2e96a09f0ba1ff`

```dockerfile
```

-	Layers:
	-	`sha256:5062a114d681cf85a6676ef9e79c37932a9f95a2a8727a7162c428fe0ee6baef`  
		Last Modified: Tue, 17 Jun 2025 19:50:23 GMT  
		Size: 3.8 MB (3819868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4583a1853388330d2bae4ca5b1504cb59cea5240501e4b0262fb6dba3d2fc0f`  
		Last Modified: Tue, 17 Jun 2025 19:50:24 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4089032b70ded5ac80148fab288fafe0f090111ac00c17532ec6e34e06a1e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126095878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3d9d6ebdaefba18da4d2a4c1818f90fbdbe8630931c800195fff7de7596958`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe5b807d5a929d0e57fcaa69d75b6ff5970626943c4142ca41c0b20772d6d2`  
		Last Modified: Tue, 17 Jun 2025 17:10:31 GMT  
		Size: 77.8 MB (77757026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6a9c095eca091b0a9137320a719751da4af37575e4e45aa1ad9456272a269d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14407aefbf46851f2e7f765f05de2f62885f83d7a58e24b491455bccccc47d61`

```dockerfile
```

-	Layers:
	-	`sha256:512accfe2d354ee29582222998b379894a51f9709a2a2bc4feeb2e474ba02809`  
		Last Modified: Tue, 17 Jun 2025 19:50:28 GMT  
		Size: 3.8 MB (3817900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87e4fa86f949ce93bc2afd10828e97005030afa8c03e2d6677a79039fd268d7`  
		Last Modified: Tue, 17 Jun 2025 19:50:29 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:0c1c41f62a54f016a0280676b962c5a6eeb84ca3ed966b3942b5e9331c7ab89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119648600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4486629f43615bcdd59494f55f6187c36bb003f48736640b7d2629956b3bb4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd46c820a552519280ae8a425571a45d8518a0b03e8927ab97e0586eec250a18`  
		Last Modified: Tue, 01 Jul 2025 02:27:36 GMT  
		Size: 70.2 MB (70171179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:586c822a6253ef2b2a59279edcff9c4d484636e094266cba8fa606ba49700e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08e17f5688614f80b7e4f5d1904dffe24b0cf6a179be686ebf7b450975265a`

```dockerfile
```

-	Layers:
	-	`sha256:0b0da0d6ec3acbbd58829c37089cb238c5a38784f097a97c580bf5af25020c72`  
		Last Modified: Tue, 01 Jul 2025 04:48:16 GMT  
		Size: 3.8 MB (3814789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faeb4aea67da576b835119d2d4cf04ae68663a395c34fef65a8b5d5f8bffc3`  
		Last Modified: Tue, 01 Jul 2025 04:48:17 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:a63a4ea3d128396c7f32465dec66adf7c3b5afe3c10c5226d3f832caa6cae395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118879374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5be6f8d011c71ec3ae960b918e1337bf7258cb7c1669c54472e73d3a6237d`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed10362ee3286079462ec33b38096f9ff153900412c92cbde02276ee6d78251`  
		Last Modified: Tue, 17 Jun 2025 17:38:11 GMT  
		Size: 70.1 MB (70103777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:636b9d741f246ec7a549e5636ab956baf3fdadb41317ae46eeb5c77b983841f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a88a5fc9b687d36d7f1c47cd4886488ba3e140e2905628908bd9ead7b27b51`

```dockerfile
```

-	Layers:
	-	`sha256:466087fbabcd1783c939a01bcf34a49bd63a4c021e1808b74a278f2738f45b84`  
		Last Modified: Tue, 17 Jun 2025 19:50:40 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:c679f9086d6324244e28faece5c16b428093806f6bc3491e7cba8e72a5865ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123526502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3925ccd2e2c4150959aaba28ff63f79f0e58f6d6d50dd77fddf9cb21798664`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9319db3ae0a7359c4eb9e6d94f2999a6e9dd0ca4eb7c6eb212502ecacaa18fa8`  
		Last Modified: Tue, 17 Jun 2025 17:14:23 GMT  
		Size: 71.2 MB (71189145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b243e52e36fb1af77e10a36631d46d1544b6ab689bad7ab04c33030873e2740f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0a5d5560d50d8d47772bb45206e39187dba55eca8381a4789c9dbf20080fb2`

```dockerfile
```

-	Layers:
	-	`sha256:db24977cf9917493cc2ec08b9b22dd6a0c78cb8ff42c7e164640d629efb8f172`  
		Last Modified: Tue, 17 Jun 2025 19:50:45 GMT  
		Size: 3.8 MB (3822071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f64b27c34e511b209f1cee3c4fe292ca4f5c1bbaeed9c4cf053cecccd98592`  
		Last Modified: Tue, 17 Jun 2025 19:50:46 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:002c468eb8e5894572e5d83d7d81e7a3fa9e681581ff8473cab20a628e3144f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116966451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d49d97e7bd0ff68c9fa3f506fadbc551c3f4076c55e36af216da935eb2115c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=28.0.1 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=28.0.1
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1d26330e3089d4d70a752210f8794385e8844e3d19684835810f1a59a752158" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4695f28308e46964cfc690531d85e48711fdb77a68b9011afc04570966d66fbc`  
		Last Modified: Tue, 17 Jun 2025 17:11:29 GMT  
		Size: 69.8 MB (69817043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b09a83bd656a74e6a797ef6d41911d2e3a1c18ed09218e0494ef791211bc3af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfb658df33649bdb87a4afb8ddccd8e03b5214bd6873a14cff7fb16f6710c8b`

```dockerfile
```

-	Layers:
	-	`sha256:58a9156c8cfc6dac6fff3d8a81ec6d5cd15a59d49fa244b04966b689a578fc13`  
		Last Modified: Tue, 17 Jun 2025 19:50:50 GMT  
		Size: 3.8 MB (3814455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7d663033a00f6a0e165f6ae8e9d17418e7ef39759728131f709e7c4d1f4101`  
		Last Modified: Tue, 17 Jun 2025 19:50:51 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
