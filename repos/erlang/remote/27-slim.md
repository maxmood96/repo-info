## `erlang:27-slim`

```console
$ docker pull erlang@sha256:d3450808d0fda975d9ed50ee8e34aa69e2fd9f624c75f79a299e3dd9273b224f
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
$ docker pull erlang@sha256:80e82bb76809e8ae136567afe70cef2e6d3a36d84db6b0c6da7a88c818158274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124485594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f208bc3d6c0a4c66bf4f199145d03e5c8e6177f2bc083ad13875d20bdd50d1`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:26 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 05:17:26 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 05:17:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d2658341868224db96c55f8bb639aa45af9eacf3fd8184e9943f93fed9018a`  
		Last Modified: Tue, 18 Nov 2025 05:17:55 GMT  
		Size: 76.0 MB (76004833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0c73e306674b32b19a0dd373ed54b04532183f1a0c632e662273fc49331f56d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd01f42bbf7ebdbbbe7ca16988a42087d7e48ddc435f8397b86a16549ee5308`

```dockerfile
```

-	Layers:
	-	`sha256:84b14a231f71eb4087390b69a18954892e442fd9937f535ff3d9145a6a0aba84`  
		Last Modified: Tue, 18 Nov 2025 07:48:47 GMT  
		Size: 3.8 MB (3824104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2037adc96327b996debc56dc9b54e120809cdeab6fea7648234531ae7f9da8c8`  
		Last Modified: Tue, 18 Nov 2025 07:48:48 GMT  
		Size: 13.6 KB (13636 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:610fc5ab87c3fc4e3ffb0b463f10361244bb1e1e4b6be30cb1591512a65e0900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111529386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a2f86b06a452f86f49bbf53c13df68efb0fadfcc70549ad45a361924287bfe`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:29:43 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:29:43 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 03:29:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:29:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb064aa2f5130f2db5b236fd1f3e8bc37a657b9ee575c0f49918db2f0a0642c8`  
		Last Modified: Tue, 18 Nov 2025 03:30:16 GMT  
		Size: 65.5 MB (65513555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3d16f9648359389c4ecddd415025d7a61b40382a51fe15fc9636a508626c8e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1cb202374b571a176deec8837c940d4cc232d22baa4bb25d4441061be7d149`

```dockerfile
```

-	Layers:
	-	`sha256:626856e2ce079b5844663bacf0ab9b938fffd6878acc7ae52b757d6a9e545df2`  
		Last Modified: Tue, 18 Nov 2025 05:48:43 GMT  
		Size: 3.8 MB (3827912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b875e50e2c0d7fbe197c544a7bbeed6149c7d08e2047c2dc18693d3255b4f924`  
		Last Modified: Tue, 18 Nov 2025 05:48:43 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:11a7245ce0cd93d331826de4e09769c222b9b35a132fa1e69406e7051ec7bfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109320688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692b87f6f6dbc6f0459a0348fbde7a2f381d95673370652b700de971450aadc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:22:26 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:22:26 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 04:22:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:22:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae9f2619246a29f94ecc77a2a11a07ea858e8fb0a2859142735d30b89aef581`  
		Last Modified: Tue, 18 Nov 2025 04:22:50 GMT  
		Size: 65.1 MB (65124564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:be059bcdc7b3be2b216eb2cc24cb1678e2db1ce6e5cd61661440f4f53cdba715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396a18540e8b528d56d1217bf3f330cf75f4bd9c379a0a5ccb9a7e3ad7831c7c`

```dockerfile
```

-	Layers:
	-	`sha256:bc6f72b4682a90960a46e445f01972af9ba7353cdcb3b6020af195af862efb88`  
		Last Modified: Tue, 18 Nov 2025 05:48:47 GMT  
		Size: 3.8 MB (3826337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae52c138319712949afd0b6ca842c958b8073f8dd195e8b78e7147d4913f3a8d`  
		Last Modified: Tue, 18 Nov 2025 05:48:48 GMT  
		Size: 13.7 KB (13716 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:49cd384b6d2bc58b75ef3baa7e77324e8f68d3c847f06fe8570900777005baf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122111579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c42f8b3f02586a62938adc24c12fb2bb4fef22173ebaa85d90c1072242d4746`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:41:07 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:41:07 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 03:41:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:41:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eac0ffafc2059d27e15f8869e405de37eaf7e303957fed5e692622341cd7cf`  
		Last Modified: Tue, 18 Nov 2025 03:41:37 GMT  
		Size: 73.8 MB (73752441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e0a163e1986538dfa3b232ced0fb090610745e05cb8742cdd13f153f50e791b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd96afe45fbb10339dda89c9a6907ad10687b17112eb8529763814deaa0d255`

```dockerfile
```

-	Layers:
	-	`sha256:afb0406ab1693e23693551c12c69a97d592a4b57a2048bb18f5d26ed60d18e8c`  
		Last Modified: Tue, 18 Nov 2025 05:48:52 GMT  
		Size: 3.8 MB (3824365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18daa3f4017bfb92c6c24135478152440582a529da7867de91c7a651f6b218a`  
		Last Modified: Tue, 18 Nov 2025 05:48:52 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:61eb8c3c21bc54c21b3f3316e8954cae07ba50495abd94a64547108c5551adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115622106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547ac531b33b67c117e96bbb43ca6b3a5b4c83e4371f52f48453f3a20b33356d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:59:16 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 02:59:16 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 02:59:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab63104a1a6213b28618addde78f5986d290d1523601aeb8cefaa89b4415f8`  
		Last Modified: Tue, 18 Nov 2025 02:59:40 GMT  
		Size: 66.2 MB (66155240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c432bfd5f7b03ffa775efb31db554188193ca4c88bbdbefa8c7510eb89c84ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4987a77ab170b467dc284e1baf287111eb5758e0e3eccc6b98dffd9cefe9b880`

```dockerfile
```

-	Layers:
	-	`sha256:68722459d7fae37aab9c230bb56803e2d242ed8d94e4988f88c2cb493a7280ac`  
		Last Modified: Tue, 18 Nov 2025 05:48:56 GMT  
		Size: 3.8 MB (3821266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589aa65c84ee7ee2413335011e69a74378c0cae9e8035ecef0e737da3797d525`  
		Last Modified: Tue, 18 Nov 2025 05:48:57 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:6b9d3e7233a48d14b684b1e30d2e74fba84bcdb1eb50699e7b598fd2b435a4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114840471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291bd071a542e53e5390cbca2aa66770f6486817be72b40c0531b7d1ac4ad310`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 20:05:28 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 20:05:28 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 20:05:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 20:05:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e734d5c699409eff4dd9f9213bf9ec798876297443f0d3e614444fc89f3232ba`  
		Last Modified: Tue, 18 Nov 2025 20:07:00 GMT  
		Size: 66.1 MB (66079515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:beee9010e580b193c8d1cabff92808fa4c714cd8385024432b6f79e0dd364a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410e18446e0a888198a561078da8cc5580df23cec7c03f4bb1ab270bbc852748`

```dockerfile
```

-	Layers:
	-	`sha256:24be8af7b66d309c544ce87fa9aab12c39dbcceef9f318378567ee9eabe39f76`  
		Last Modified: Tue, 18 Nov 2025 23:47:26 GMT  
		Size: 13.5 KB (13487 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:d761a28636c2a5916089ec18b78432eb201a8245bf8816220b35f907deb1a2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119575704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d2c02abeecb6b3e3fa65a9c43b2a7e6f26853e07524480cc6ff51494181e83`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:13:46 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:13:46 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 04:13:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:13:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784856343f00e89727c3b015342275f7ad2c81126cf22028997a341e050dc46b`  
		Last Modified: Tue, 18 Nov 2025 04:14:46 GMT  
		Size: 67.2 MB (67248741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f2740f6f322c7aff4f2328b3cdf53df66741e24026dd864d74558a9c344cbc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb11f7efb8d0849618cba6bad7293956a1dea0f388c117c4627b2ed79f66b38`

```dockerfile
```

-	Layers:
	-	`sha256:51d976e8d779551f0e85428e59e98af7bf046402f7e5571d0b0f7805150c03d7`  
		Last Modified: Tue, 18 Nov 2025 05:49:04 GMT  
		Size: 3.8 MB (3828552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1821088914f0e757450de27b42b6dfd46ffeaddc4a2738272e7887495dc1ed35`  
		Last Modified: Tue, 18 Nov 2025 05:49:05 GMT  
		Size: 13.7 KB (13680 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:8a34d89c66c8fdc34ea601fed763ad3653001d7114ff7c2fb502f2221b6ec8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113048514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dba82e6d9f8ea0d1230bfb868b719afcf35235ec0d86548b8de28f9a5e96516`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:10:43 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:10:43 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 04:10:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:10:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18f61fd6afa7cf5913dee4d9ee08e14dfe2682f4b57d22fa522b19298507cf8`  
		Last Modified: Tue, 18 Nov 2025 04:11:14 GMT  
		Size: 65.9 MB (65910873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:30662a2648cacc00309b54221960a3331b9f52815d8c78d678da2cc31b4df57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbe7fa252176b9562343d7fee493c3819723f842fb86b965245e42047227c0d`

```dockerfile
```

-	Layers:
	-	`sha256:4471c118cb2c1fe2c2315427733c9296951e0af30b7db7d92630982c5518c0d1`  
		Last Modified: Tue, 18 Nov 2025 05:49:08 GMT  
		Size: 3.8 MB (3820932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55353587e88805385e363ce8290e9af2e50da9a75df036c0f3ea3c19292a8145`  
		Last Modified: Tue, 18 Nov 2025 05:49:09 GMT  
		Size: 13.6 KB (13635 bytes)  
		MIME: application/vnd.in-toto+json
