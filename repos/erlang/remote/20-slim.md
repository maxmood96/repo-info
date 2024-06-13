## `erlang:20-slim`

```console
$ docker pull erlang@sha256:afa8290b8f73f7fbcbb138963eb12294199a5dad6622b1470a14d1a25f54dda0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:20-slim` - linux; amd64

```console
$ docker pull erlang@sha256:051a0e343a3724ce6b19c2a66070723bec5745314e4e1b6cffa3a00f6ecb28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112126666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736259c7b20d65192b76a4f23aec180ff51744ac0d19bf677d85a56fea2f0159`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f56ee448a7801dc6f40f797b507c4865e6cd6503dd3daa42d68cd25ab86eed9`  
		Last Modified: Thu, 13 Jun 2024 18:22:11 GMT  
		Size: 61.5 MB (61469293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:20-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0cad4cd9fdd5387ed7e4a6a0ba568cfd3a4d5cd3d36596f71ce89b134973ce26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679ad6c11a27b254f8c2cd4f162b68c4a4b6f860c730f22b97a193c54b47487`

```dockerfile
```

-	Layers:
	-	`sha256:ad4cb3e965c870c6cc13b2b1eb41a20bb6652a39794f228a05419b3e6c5f6cfe`  
		Last Modified: Thu, 13 Jun 2024 18:22:09 GMT  
		Size: 4.0 MB (3997467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61826d20ff82995ab3f2df54e55e3e934f1dd0e6dd50f54cdf8c983d1d1fad96`  
		Last Modified: Thu, 13 Jun 2024 18:22:09 GMT  
		Size: 13.3 KB (13294 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:20-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:3628a58f5ada2eb4f679b0d21acc0869732f35b1e6517fa6d142c11d83ae12fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103553593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e2f57fa2df60602589126f27db4d34770de69c70921d33b8e00fd068216ba2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2a0f6d5446903f355b1c0f3a56871cd7c9459b6ec1cfac8b2826a86829a1a3`  
		Last Modified: Thu, 13 Jun 2024 14:05:31 GMT  
		Size: 57.4 MB (57423740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:20-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3dd8f69b7491fc5a90c29916d49572a68e342c1a5ba12946b595c8c802460501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4012900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ef9e532f3970aac11f9b8a3c8c8f188707ffba5d503c8002539809e7c61248`

```dockerfile
```

-	Layers:
	-	`sha256:a5d294aed31e985f1cf1b1a53913a3cf35e00a9f43af15d4bb88e13578e29634`  
		Last Modified: Thu, 13 Jun 2024 14:05:29 GMT  
		Size: 4.0 MB (3999536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aca443cfb357c94a3b49cc86864efcf14d52d9e03d1cef0c87d939aa8170785`  
		Last Modified: Thu, 13 Jun 2024 14:05:28 GMT  
		Size: 13.4 KB (13364 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:20-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f1648f7d2d37d1ab727865dd6a33fbfba27d00ee248ce6b1aea0aba6a8c57709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107876716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f486274f736f86d603603c3133ecc3fe975429d4a2eace9bb53dd499fefc9bd6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bded5ad64fdc91eeca2398aefabf9f426d5670998eb85588a6df9757b21f0f`  
		Last Modified: Thu, 13 Jun 2024 13:42:27 GMT  
		Size: 58.4 MB (58423458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:20-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fecb386e5a2de7ec32616819bb1a6694bc380d959e7e1124ee55d74d0a2891a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f7c60a0d087451e07200c2f607c218efa6317632ee3693f9c3db454cedbcd`

```dockerfile
```

-	Layers:
	-	`sha256:defa403bee325286256303f650754f3da5ec89035fd55c2b2259d7fbf184b0e3`  
		Last Modified: Thu, 13 Jun 2024 13:42:25 GMT  
		Size: 4.0 MB (3997672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29931b01cf0af96cbc1726acd6b9c11c2ad1248d8865e6454f5ca2c1b005c2c6`  
		Last Modified: Thu, 13 Jun 2024 13:42:25 GMT  
		Size: 13.6 KB (13596 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:20-slim` - linux; 386

```console
$ docker pull erlang@sha256:b5d080d50f994f3e2a0542d60d184ef2c8314760219424968f2fcd8ec0784c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112422302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf036467e931e8b0c0a4a51a3db2c9fe0d94159843eac82823670f6df34d2ec`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=20.3.8.26 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="dce78b60938a48b887317e5222cff946fd4af36666153ab2f0f022aa91755813" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31da97e7b342459868dac87aaecd02b414831d5e7aecdaa4132f8f323ed83c3a`  
		Last Modified: Thu, 13 Jun 2024 02:06:51 GMT  
		Size: 61.0 MB (61002389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:20-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:08db766965dd7c735a610470564eeb3643b405d50ddc21b4fe565540293e2553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb377eef9f80b24e6046e8ebc5af3a60a1e6f56699e4ba5e6b7d4aa419c7d82a`

```dockerfile
```

-	Layers:
	-	`sha256:2a94e111fbfa6dd78d137e52f2c2679f72e7f1c15f925ecffb9a99be0a347192`  
		Last Modified: Thu, 13 Jun 2024 02:06:49 GMT  
		Size: 4.0 MB (3994710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6abd61e84bdc11d46e08ee2345fac18f1e20d32b385e294e44461ddfca7fbcdc`  
		Last Modified: Thu, 13 Jun 2024 02:06:49 GMT  
		Size: 13.3 KB (13264 bytes)  
		MIME: application/vnd.in-toto+json
