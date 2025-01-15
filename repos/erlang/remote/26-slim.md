## `erlang:26-slim`

```console
$ docker pull erlang@sha256:8d07b85e76e0946539b63342a3dd4d612b2a5861a9626ad9cabc89dc35cc17e7
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:62dcb00632b5acde583c1983db09bb03cf7bdebebc6aea4287b75743886b61fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118858788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a4842a084e76e796344307d60527f348ec7c24f11b2914d351a833134f4c1`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3f3af508cdb50d7c303c5d72f27038f2274d6662fcddb4e056dead4a66304d`  
		Last Modified: Tue, 14 Jan 2025 20:40:33 GMT  
		Size: 70.4 MB (70378826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c7c1e04254ba3bcee8434a60cba57a2dd2de40cac600fa36834aec76fb569806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ff170b08e6f7ea95713167859588e2e303972ed2ca2fc4bcddfbb979100770`

```dockerfile
```

-	Layers:
	-	`sha256:c9021316f414c432edcc6816a80fdd30d3d5ca79c333b6cae08c5c699708f856`  
		Last Modified: Tue, 14 Jan 2025 20:47:14 GMT  
		Size: 3.7 MB (3709350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b135cbd15588235af037299548f130261258d0c7d280c36b8949d935ad48d92e`  
		Last Modified: Tue, 14 Jan 2025 20:47:15 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:be56b896cecdcac6d4e235be7a0bd09a0b3baad880824cd27ebb0886978d11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106499559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc666e7546d0dd20c137f561fdaa44508e3f9e94e953a2922202b11ac772e8`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:237814a70d9f7e95f3568236c75036fcef22a88f1a76245129eca111484c0351`  
		Last Modified: Tue, 14 Jan 2025 01:33:00 GMT  
		Size: 46.0 MB (46006814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43f6d6bf36db6d464ac8b527f16f36b5f14a79d89f38a1a00b301f1458d28ab`  
		Last Modified: Tue, 14 Jan 2025 06:16:03 GMT  
		Size: 60.5 MB (60492745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:cae10d94924a9b5497621039d1d1d30a01d5b337442594c3171d77b0d191b19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f77acf310e851e1a7beb3d2a52d3e4b1a5cb09fce9ff9fcbf0e6c85d59dc326`

```dockerfile
```

-	Layers:
	-	`sha256:7599189ac5eb0c75790dfe16caeec98f3620673bca03636ef66c7260e0190a6b`  
		Last Modified: Tue, 14 Jan 2025 06:16:01 GMT  
		Size: 3.7 MB (3712850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1cdd5886b7e5d4780cc6a2561235db1421163d89209f371d9bccd1fad7de65`  
		Last Modified: Tue, 14 Jan 2025 20:47:17 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c37d008323772de5571f548f3f3d0227244f8f720ad5f2f96bdb0efe6b8debeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05affa0663eda005265fde805ae6ad7a354ca3d6acecadeda365c1f74f8bcd`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c0f65289344c846dda8bd4a958c6af32dbe4f0527dd363d424b2336788cc0b`  
		Last Modified: Tue, 14 Jan 2025 09:15:58 GMT  
		Size: 60.1 MB (60115890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1943669a2820ebb6b6d318e929e6cf0ce6d51a96054d01d2fa65ddea5ffbeec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929710002d96697aef13b302906665ef6a9c9c64c440215a9e67d5ea36843b08`

```dockerfile
```

-	Layers:
	-	`sha256:33d1c9be5d7a6c354e3beee080e9d2a2f95baf4ada079cfefa7ca454b3d59f59`  
		Last Modified: Tue, 14 Jan 2025 09:15:57 GMT  
		Size: 3.7 MB (3711583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c6027b485370eb2743075402533661d0c6566d152558f6b1670ea2cd68dc25`  
		Last Modified: Tue, 14 Jan 2025 20:47:20 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:af3c5b52d6532b243474b795a3c83be252e286539efcef8ca8f01c921026a85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116317408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375b23d0a1639872282ca6e6feb730a318347345b92066c1d84ee2454ff43a4`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7a5604f843830b75a28c39ec859d21831ed8cdfab23845a43bbb839bec8e9`  
		Last Modified: Wed, 15 Jan 2025 00:07:30 GMT  
		Size: 68.0 MB (68010512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b42508de7573a9cb553a0ccd73885e324afb321de99457268e807c52a50e1813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a17322ec48920743792c38b1f12fe31a3d40d26ade49b3b57ae8c19f80e8ef`

```dockerfile
```

-	Layers:
	-	`sha256:01e96b6ef9d3917d98d0c8269e588467b5f0cbadeae5f55cfc20abfa059db0a5`  
		Last Modified: Tue, 14 Jan 2025 07:15:50 GMT  
		Size: 3.7 MB (3709611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f74658934b5dfb26bf0f5d28a301f6954654f0ba4a701d68e8976c622c52a2`  
		Last Modified: Tue, 14 Jan 2025 20:47:34 GMT  
		Size: 13.7 KB (13706 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:cdae8f1105e66b9553c195ff8f6391b44acfe5aaed4ff7eb0ae76e10fe34f17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110573319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0bc8292d7e111e10da9ee87f6b7513cd5dfd5f318c9661e9cd3cda3a15f89`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd5e010075b3c7e91533ed703b8c21bddab162b508d7c6c889ef6964475ce36`  
		Last Modified: Tue, 14 Jan 2025 02:24:43 GMT  
		Size: 61.1 MB (61115574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9ddb900c4b276c86f668de43767a9ca62e20e905190148b12e4f8b3fb24263d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f445016c779b09d46ddb1b47d27353c4ef5d86397dc33603306c11012cb83a61`

```dockerfile
```

-	Layers:
	-	`sha256:b7fa4c0ce125d83bc7d4ecccb72b5e91b17491ac8f6555b8ec379410033a7b21`  
		Last Modified: Tue, 14 Jan 2025 20:47:24 GMT  
		Size: 3.7 MB (3706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d853984ebd1b443aea8a7e135ea50854aadcbbc64977e02996cf0dd9c5064918`  
		Last Modified: Tue, 14 Jan 2025 20:47:25 GMT  
		Size: 13.6 KB (13570 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:d37ec2b9bdd8cb6b8ed7496e4d4073b3f82eac1444b14db0118b0f88a1f0c7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109833696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81fe9e16c85e516bf6fc14dd1977365e8a14e60f896e68fb975a4ccb0137e33`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 20:45:22 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90a28c2903f9d9de075907b9ed16dbdb2c342238717a8e7dbc2dc2833ef82c3`  
		Last Modified: Tue, 14 Jan 2025 20:47:56 GMT  
		Size: 61.1 MB (61075593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:827b53747c64e97b8f816fcf10748afe1c831009ee68c5ed2bb30dcef7cd680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea0d171d398a9f28ad73a1a68c2617b22dce39c0cd5b7dd0c8852071b28ad3`

```dockerfile
```

-	Layers:
	-	`sha256:e8d3e6b99c2660acacce0bb61f5039a4ec105f4b038ee4f5e60e11e2cbaba59e`  
		Last Modified: Tue, 14 Jan 2025 20:47:37 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:63239838956a0394f6f6312628f09a3f725b9eaa0af92be1deb5b363c2c68e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114515909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2a8d4109b11e1c919eb5e98b3fb9d1916cfe520d7139aed91b8607394ba0bd`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ca3d64187888d7d15091240f2380913d56f962a6230774e20ec678640ca12`  
		Last Modified: Tue, 14 Jan 2025 05:47:05 GMT  
		Size: 62.2 MB (62202772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7aafc2431a82d3f7c45882aabaeae449500f349e2bd498e5ea2eb4e8c4500be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e4584ca4a17193f1780af9d54a69851ef904c2b7c589520ad9142c2bf2f055`

```dockerfile
```

-	Layers:
	-	`sha256:321cc27060523703c1ca567cdad4ee0500a09312ccd95dc40355de6315b0495c`  
		Last Modified: Tue, 14 Jan 2025 20:47:28 GMT  
		Size: 3.7 MB (3713690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fab20ef718751e73c092af76618979dd5a9d04879e2276d132a880338bdbf16`  
		Last Modified: Tue, 14 Jan 2025 20:47:29 GMT  
		Size: 13.6 KB (13645 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:80d2fcdefc1e0735f81791b3699bd3ff45fea532a24c98c624b099029f2ec8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108045223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b5fcd2d4c55508756ea1934a2ad945352dd4806b104e976366b12fbd5e107e`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 20:37:18 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0b479fcc2da5e4ce430df40cb6724861f44fb327346532857a5127735942e`  
		Last Modified: Tue, 14 Jan 2025 05:23:17 GMT  
		Size: 60.9 MB (60913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1da66da602a1ed7c6d3fab9d5d3ba25173be8cc43de2321b2c807794fffad6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0745612409f0349369b4b8ffe1934bb8daefe5d4d0caa0fda6029ac2b0d586c`

```dockerfile
```

-	Layers:
	-	`sha256:4a9d6a0d22099a4038d60a08b7da70b4b1915194d8bb6c031c5d5035d402e807`  
		Last Modified: Tue, 14 Jan 2025 20:47:30 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a5d88a34b2c3ca32fb45136693772ff41d8d45a230caef58e3bddfc9834240`  
		Last Modified: Tue, 14 Jan 2025 05:23:15 GMT  
		Size: 13.6 KB (13602 bytes)  
		MIME: application/vnd.in-toto+json
