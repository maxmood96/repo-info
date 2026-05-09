## `erlang:29-slim`

```console
$ docker pull erlang@sha256:5ce4992344598538b921324f7b5ec00b69bc0126fb57b434d76ee7cb2dc4e3fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:29-slim` - linux; amd64

```console
$ docker pull erlang@sha256:785518feab8d99eee485a313433e99f2065aa125cbcfabfaa5834eb9fb84aa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129483309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8de07351f2e7615dd50bdfeea3ea22915720bf94099c8cd7833c8f9946c63a`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 19:43:33 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 19:43:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ecea14e267286053ae506ac47448663bd81aead86401a53052d68ab4d2e27`  
		Last Modified: Fri, 08 May 2026 19:43:49 GMT  
		Size: 80.2 MB (80180989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:993ca86b266d3571af00854d74ed655a96a7b2f085595d257c7d1f7ccc28f141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969ef56423976906c672ff44ab223e067664c7442a3102c5a76f2f0d642fe09`

```dockerfile
```

-	Layers:
	-	`sha256:da3bc83456b2edb7693ff141c26b9b78c98d141c8d82b141805d863a0f228329`  
		Last Modified: Fri, 08 May 2026 19:43:47 GMT  
		Size: 3.3 MB (3283468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53937ddb59967f0adfadd60d9f4a0003184a65e5ae5181a659fabcf04f214e9`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:c3f506e9f7e0f8cf6987e57da758c78745b122211483310961a7acf5c8bcb898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117817354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f99fdc2aca53e8251dda98c37d9ad54f3aa37438c16ddf5ed80c67683e4e49`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:59:46 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 20:59:46 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 20:59:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:59:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee097ceb6b981c236142f1fc801c9d613e08468e8496becb368ccbba0afdafb`  
		Last Modified: Fri, 08 May 2026 21:00:00 GMT  
		Size: 70.4 MB (70351062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e1a86aa5d07edbdbf1430c45336988d59e7a0c8851e3f5d610a8a997e7885b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a6221dafdb2a69b48e6b9287425a47131d5575cdfa1499c0cbee8183bfe48e`

```dockerfile
```

-	Layers:
	-	`sha256:67da7763f983f340f583e7cebc90b062e37e32b4cdd2c463c3204dd33df87ff3`  
		Last Modified: Fri, 08 May 2026 20:59:58 GMT  
		Size: 3.3 MB (3286435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4090dcaff34843944ca0bce323e5e8903ebbc1f1a365c48edf1f2533324126`  
		Last Modified: Fri, 08 May 2026 20:59:57 GMT  
		Size: 14.3 KB (14274 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:06b86b802c3c2ae07d0b92e99322d65a56ea16cfea95219bff0b178198a14ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115664284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15cd329b8c0143aa1f6dc53270d08fd7742aac4bfc26e6106ef3d61fe79abb0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:47:24 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 19:47:24 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 19:47:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:47:24 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4eb257fc23f8398fd3e3c8cf6f5428706594403bfd918f4576746ce84c1e6`  
		Last Modified: Fri, 08 May 2026 19:47:38 GMT  
		Size: 69.9 MB (69925859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ef52dc0800cf58857ebef29d3b78c7e8e85f4b2341c42c85e57b3b01de98f632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a2327cdf55fd6a8e34e30f452b7e106540950a3c28f947a989913070e460e2`

```dockerfile
```

-	Layers:
	-	`sha256:c470a809390086facdae144685e433c4f1720c18eeba21d925c5d2d704cb1d3e`  
		Last Modified: Fri, 08 May 2026 19:47:36 GMT  
		Size: 3.3 MB (3284884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae629ddf0f9bf4a1327c78cd9d1a25f71f00483c44f5b483131da13089cd84d`  
		Last Modified: Fri, 08 May 2026 19:47:36 GMT  
		Size: 14.3 KB (14273 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8c20c90d7f344239f516fa23df980df89706ec49055a11c808b8f1acf03f8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128324942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff7071e00a93c5b7ed34fe98c74359aae3d5ba972960e746c45b27154b8aaed`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 19:45:15 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 19:45:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b0299d9a494b632402b03090e872f936f6a3b5c75ccaeb213f904983ae39a2`  
		Last Modified: Fri, 08 May 2026 19:45:31 GMT  
		Size: 78.7 MB (78655497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7e1751d1795c22b8be219b177e28f5c43a602c366786c14659383313d268c20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873d7b73eeef1e2aa0e396cb6f84817515ef4a0c4a96e5558377f3e19eec922c`

```dockerfile
```

-	Layers:
	-	`sha256:31ce7edfc8bac4459aeee64251daa03d05a8d0c3e3fe27ef55bde6e9974828f1`  
		Last Modified: Fri, 08 May 2026 19:45:29 GMT  
		Size: 3.3 MB (3284991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9edd6d74c863a6e99f93997daa0f7cf9e7eca09ad504121176626d90c97e2384`  
		Last Modified: Fri, 08 May 2026 19:45:29 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:3770d5ba33e0eb5d7c79f853351268ec880ac5bfbcf4c8f6a8e386e8700946da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121146423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da12541b7907821ad1207a8c5931c5071c62410726865a115496cb5cdc009237`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:46 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 19:45:46 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 19:45:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e79aea7e5b42c1b092b956ef8deef89506e570ec91bcb242eae4962abc505`  
		Last Modified: Fri, 08 May 2026 19:45:59 GMT  
		Size: 70.3 MB (70320842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:becb6ce61f83ae484e2dbc01a6353b78701502c9a271d3b8b3870a34c68fd4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a74036beb9a3f1a1baa158e2ac8bb39f7abee10f865534c928f6188092e21`

```dockerfile
```

-	Layers:
	-	`sha256:4ef4bfd63b1b89a1484bc1861a801db3155c15dfa9b314aaae18a78870e4137a`  
		Last Modified: Fri, 08 May 2026 19:45:57 GMT  
		Size: 3.3 MB (3280643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7705db1a241112e398025e1735f3bcbc8de2643120a2de55b9ecf89b801df26`  
		Last Modified: Fri, 08 May 2026 19:45:56 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:aaaaf7736b5f507bbabb50174230e94d113df597ea5d72928a3f6c492a429f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124416455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049b9635a4c3d24665789676c96125965583f4dd688c7fb90ce2d19ab1a9479`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:36:35 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 22:36:35 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 22:36:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:36:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea148ec4dbe22e3cf3334439089ebf349c0146e0faa42e9da03482d5d39a26`  
		Last Modified: Fri, 08 May 2026 22:37:01 GMT  
		Size: 71.3 MB (71293290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:98379683d7207d3ebe26ea4fdab50e8d911b08effb20b8f726f656ecf770339c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365dab3c7f66800505ff00a8f89c0c41fb9e72252119fd508e9540da4c9f3a7`

```dockerfile
```

-	Layers:
	-	`sha256:f46aa4a3b8cf7035d1e26f7d6591dca2efa1276d798b5179c3e1165d8e23f51b`  
		Last Modified: Fri, 08 May 2026 22:36:59 GMT  
		Size: 3.3 MB (3287053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceae233303a5f3ea9bfd6a35b5cf5d92569aa7426da7ea7485bc028d289aa101`  
		Last Modified: Fri, 08 May 2026 22:36:58 GMT  
		Size: 14.2 KB (14238 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:3cb4f774088308e808d2b95650daf2c265a2178558013a25c37082affee974d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120559037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d381a97d9a75c32b37cf54d16ff313464b31e51971f0426331c403e3f02a2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:58:57 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 20:58:57 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 20:58:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:58:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c756aa3c5f8d7db5e8fb661b640a0911bc9807d925b7513a033bef84b3ce0388`  
		Last Modified: Fri, 08 May 2026 20:59:16 GMT  
		Size: 71.2 MB (71186733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a1a3f6ba16a4d167ee659c91a832681ef809d4d23270800d167f432745bb55c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4499e919b125b41773932aff1ac8ae428e2946ee6c47716dbae4f2ae1e46df`

```dockerfile
```

-	Layers:
	-	`sha256:2838ff99d2171e2b0f76e206a2cf90fc395ad543fb10ad84aedc840dced1a1cb`  
		Last Modified: Fri, 08 May 2026 20:59:15 GMT  
		Size: 3.3 MB (3284909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9530b3266a4b54437cebc5e1bab5a8220b5aed971da09aff2adc577064ccb740`  
		Last Modified: Fri, 08 May 2026 20:59:15 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json
