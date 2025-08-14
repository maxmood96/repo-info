## `erlang:27-slim`

```console
$ docker pull erlang@sha256:a0ab941de4dbd323de68bbeb9b8d3bc261c88fa8f71a15a59692b79a64f5b68b
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

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:2b8c27b550c37d0bb071b2e1df9435ad6f5c9b00042c9d6c25e460151c5b9d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124491713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4db9cdd45faa3796a0284ceeb67d1e33f2b287fdbecc34b777827928641453d`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9518ff905945be34b4454ab536d3d25a578641dcba21cba07fc0ab474967b`  
		Last Modified: Tue, 12 Aug 2025 21:26:20 GMT  
		Size: 76.0 MB (75997202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5c28ee98be5b84077883977630780fb5a3b6e7b8639f76a66d8b352bbf09c919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006f5c2292e5caa6af9ec36d4803eb6fac4ebe16ef1487ea9669a8df60f2abde`

```dockerfile
```

-	Layers:
	-	`sha256:a092614ef6278f5c952a0e6848d96b586ec688da1993a811c68432de667c6f3b`  
		Last Modified: Tue, 12 Aug 2025 22:47:27 GMT  
		Size: 3.8 MB (3817487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633664bc07b04189682990afba844562c24e1c8d9d11d8735b31599184e775e1`  
		Last Modified: Tue, 12 Aug 2025 22:47:28 GMT  
		Size: 13.7 KB (13679 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:73aa8f32445c060774a51f2c22640796a646d6cae8759a0fe2e83867ed529d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111523986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff164843d2cbe26e8e4c2103c0d3d20de380f4224f1e58c6fe4e1b4d99a4ca5b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ea0d25317149dd26fe3fc21f7a1766f8528af12760c2aee4e2fa23834000897f`  
		Last Modified: Tue, 12 Aug 2025 20:44:49 GMT  
		Size: 46.0 MB (46027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aad53dab2e44c1f372fa7475cc62fd10e86184123faa987c0468ae97aefa51`  
		Last Modified: Wed, 13 Aug 2025 00:07:51 GMT  
		Size: 65.5 MB (65496751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fa6a0cea805411979e9616ad5c5cad3d89eb530b0cc86e421217113eb6fefe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436f83efd0b813435195a725cddaecc97fc3e4054868f25a81103798cb876bc6`

```dockerfile
```

-	Layers:
	-	`sha256:55c4992bbcad6e15a86553f8f9278e9c48497bc4009cf6aa86b41078ac79d1ca`  
		Last Modified: Wed, 13 Aug 2025 01:48:00 GMT  
		Size: 3.8 MB (3821295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b506f46f8442db93f433329bc235454917552e013e47d26eb4050af502ce9eb4`  
		Last Modified: Wed, 13 Aug 2025 01:48:01 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1a97eb5e30d9b3bdc19bf1e392a86d0f59fb25c3328b3850bbf16b93f5d542e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109323894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b0495b3e77beb25494e03ffe193c49f4580df77034e824948c626066406725`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90e738ddbd23d26a4847a3e0282fef2472de85482975ae027cd2b205401f4`  
		Last Modified: Wed, 13 Aug 2025 00:27:19 GMT  
		Size: 65.1 MB (65114850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e7770e705d0f714a33c0ba7dfc9581193b433c7cdc28f8ffdd84385d77beae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90b5273a856bc94a89c05ca61fc67a9eaecc83241700ca010497d2b5b0c1012`

```dockerfile
```

-	Layers:
	-	`sha256:cc6b1cc489229305b7c051b08cc52230f4788ad4f7dfd62efac577404a377cd9`  
		Last Modified: Wed, 13 Aug 2025 01:48:05 GMT  
		Size: 3.8 MB (3819720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990660d9365dcb89a4f027d8885335a9575072caff3ec1fc18a4af134020e023`  
		Last Modified: Wed, 13 Aug 2025 01:48:06 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:05853403840e06e04c9c4acc63aa696cde5d668d5364c6725375c6e9cf17df2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122079661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b94ecd14bcede41c9049289ee94b11cf765f2081bbe53ea53140317c8a3f522`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32da2d3e5bd824fee8e0ce740271cbda280dd76884e1cc9905d15f5d42c3b8c`  
		Last Modified: Wed, 13 Aug 2025 12:29:42 GMT  
		Size: 73.7 MB (73737211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bc340e7f19c113a2e1ab661afe9bb41a677b60253e31ca8a85e8a4bdfe52ab1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690344eb8f0ba86ec3225c79c72498bcf7b012123075c314430d53cb18a3ca03`

```dockerfile
```

-	Layers:
	-	`sha256:b4e3262ea01b7eaba17c50dba594324fd4e494a6c545bc3bf4c637281593663a`  
		Last Modified: Wed, 13 Aug 2025 10:47:26 GMT  
		Size: 3.8 MB (3817748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29a1200eba6b680acb2bc7f669425368f1bf8e83021b6167bc080149d695c26`  
		Last Modified: Wed, 13 Aug 2025 10:47:27 GMT  
		Size: 13.8 KB (13783 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:0cf66fceb7a931bf12e5465694c59b8c7c544df2d0f585c1efbbcfe00ec69a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115627122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b623c83544b944b76e7786973e70e89068199883e85977558ada926617694`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd90627e511a17f60347cd383389d85ad4ba86e63ffd87ba69ec65d84d9a277`  
		Last Modified: Tue, 12 Aug 2025 21:23:32 GMT  
		Size: 66.1 MB (66149007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1a6c22bd1f73345a5bbba0d0b5d16277ec9ede18e2d33c0c865e1cd4502ac562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308c34ed3cad39ebb95abbeda6b1c2a3dc3185cdbbfe9778039a545ae53551a6`

```dockerfile
```

-	Layers:
	-	`sha256:3010610eb62daba83cb98f528d2f500b04b4c8be69298a9e15a8698e990c32cb`  
		Last Modified: Tue, 12 Aug 2025 22:47:45 GMT  
		Size: 3.8 MB (3814654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127ff3d598fd59a8982f51b34a972d576935562d3761a6f20d12c39127714b71`  
		Last Modified: Tue, 12 Aug 2025 22:47:46 GMT  
		Size: 13.6 KB (13647 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:8accc1cf2c0839dac6612659754ce65bcad8903a5cde1d0d118356ae9bf9fd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957c7abb583fa335963fb65378e01e96d74802d37ef1d460791e40b0e9555d26`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00c4e75adf03eceffc3a8f1cb9ceeddad5e05030a7ddbc7763a5ce76cf5b3f`  
		Last Modified: Wed, 13 Aug 2025 07:06:00 GMT  
		Size: 66.1 MB (66072160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fa50b37e7af8572d06d57db271f44a4e8f6c6f5619ed7b38f30300ff397ed675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02bbbc77b2ff810377dd3845b021fcc4ad8e6df0d7859832c596c537c9c972d`

```dockerfile
```

-	Layers:
	-	`sha256:0d87223a16239293a7ffd31d27b278bc65790b6980d14fe6eae997a00bf73f41`  
		Last Modified: Wed, 13 Aug 2025 07:47:13 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:88c93fe3fd75d79bfbbf13c70b12274efdc073454f830bad8e165a6d95ae2084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119575930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c764d16dc4c0cdeecc4cdad2f5fc0d9ec6c2d279f89b00f925286c388155d0c`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a0c4b47927bd9c9f95e844171b6c3a7465dde04b9c375d49c5791bd9fc7d44`  
		Last Modified: Wed, 13 Aug 2025 18:12:21 GMT  
		Size: 67.2 MB (67237853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4059f6ccda13ab7464c6dbaf0aab0b8c631ae57f66f8103fb936d5fee0cf0592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad512fc675f630c6ce79cc48f082619136376fcb8a7c678df0c95d0c530881a`

```dockerfile
```

-	Layers:
	-	`sha256:9bcef3151783d4e32394d40710f69637ccb9b927c277a97e1c780e53332abf0e`  
		Last Modified: Wed, 13 Aug 2025 13:47:36 GMT  
		Size: 3.8 MB (3821925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dab1843b7e082610d9fc9ef561612fe6ea6eaf0d88addde1651a69b798e6edb`  
		Last Modified: Wed, 13 Aug 2025 13:47:37 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:325439ae35eef5e171c6a44a19402c0a673aeb4335ee9a694f24eb2c3b3dbb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113058569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02ba1097cd5433a4c7409bfec53be9ac1ae285d65858d1fe3bf4e1bd7ef5e6`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=27.3.4.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=27.3.4.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f696dc22812745d98a87af2aa599ffa893c7cf8dfa16be8b31db0e30d8ffa85c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5754879c5da558636b347c5f8034c0c23cbe363949139ea3ebbfe039b07ab`  
		Last Modified: Wed, 13 Aug 2025 03:33:05 GMT  
		Size: 65.9 MB (65908703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c2f4a946f01d96ce5875aab71fc51ad79a7f38aee05126256ca55e753bfe32b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a234273d6608d7a4008fedcffc28687ab95f376506a09aa53497fc8f205b07a`

```dockerfile
```

-	Layers:
	-	`sha256:0a483e1a393f0c9e3b062419d06244b52073cdc30879089488903287c6532b86`  
		Last Modified: Wed, 13 Aug 2025 04:47:21 GMT  
		Size: 3.8 MB (3814315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b86669233ebe798b2a62c42eb6fe2b3609f4c5cc12286c5264baee6af2b5f3`  
		Last Modified: Wed, 13 Aug 2025 04:47:22 GMT  
		Size: 13.7 KB (13679 bytes)  
		MIME: application/vnd.in-toto+json
