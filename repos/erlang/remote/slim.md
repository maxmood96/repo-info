## `erlang:slim`

```console
$ docker pull erlang@sha256:1aec70a5fd25152a3d906525207da8644f0f675e3ad1106bf1a00fac82f56fd6
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

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:f9d5e98622c5af8eed9834e397f80e2759b0bceee1bd447df25a903678be3b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128995320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f124fb9beea5d07bc63a968948433dd87ef69179a70dfd0548d9c5fbc3ddbb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:16:51 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 05:16:51 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 05:16:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:16:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e39283d57d3a17fa218031a28ea416b0800050c07d2ce01059abfeb08fe526`  
		Last Modified: Tue, 18 Nov 2025 05:17:21 GMT  
		Size: 80.5 MB (80514559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e2af0cf9cdf72879d62b87afc91f21d8655137a1b3dcb72778a10f595cfd12a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b9a6f8d41072998a3fd3326cb7fa252e4ddd494c103bfa560c288645e59dd8`

```dockerfile
```

-	Layers:
	-	`sha256:06da9f16a7ed51c25969d63e93ff1626c138b732e5cbba4ea2aa6d89714abf4f`  
		Last Modified: Tue, 18 Nov 2025 07:49:48 GMT  
		Size: 3.8 MB (3824252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c9c75b043041480e32231a3c8ea57d9e3918d72aa3588084d5b75a67434962`  
		Last Modified: Tue, 18 Nov 2025 07:49:49 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:326227d44786f238eacec7c8efd484f07f6feb39e0845e8507abef63b7edbc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116226663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bf852ce40c291324f14ad4cc025e9c36449f9d513f29006dfb36d5f151b64b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:29:38 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:29:38 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 03:29:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:29:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab9f6813c82697891e86e0bff4d290a9d813910fc804f268b3210c56541809`  
		Last Modified: Tue, 18 Nov 2025 03:30:04 GMT  
		Size: 70.2 MB (70210832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7dfe38ba5b9d4d9cb502a67043c429c732aa3284a1bd7cc7a70fcc75bb25e52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c927ee83f32a0339c0359a3efc6a311a8bb3c3094e74585032337667aaf0675`

```dockerfile
```

-	Layers:
	-	`sha256:d5bc611a73c451116b264b22a72deee90960ee27173538a8341edbf43ac04c30`  
		Last Modified: Tue, 18 Nov 2025 05:49:15 GMT  
		Size: 3.8 MB (3828068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ff81b8cc047b2d2742a3fa0e2fde0089c9b862163e03eed8d12c23a786f8d2`  
		Last Modified: Tue, 18 Nov 2025 05:49:15 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1da1bd1958a05de4b6a6ce66fa8aba5920dda45693250255d22f1c9b1f5eb523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113806517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfde98db7f7dafdbec95ebc4d79fa2f84cfb8e2d1f5c65f4feb131ef8bdae73`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:21:48 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:21:48 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 04:21:48 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:48 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8ae23e3d918b5340b4a0c359171a61ffe6a6e79b0dd519310f585cc668523e`  
		Last Modified: Tue, 18 Nov 2025 04:22:13 GMT  
		Size: 69.6 MB (69610393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:792bf0cce6acfb5f7eaa877fd546a174eaba45853505ed1952d0f876b2828d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f101fa1f3b4c9a827523b11ffb9992591d0f416a011949fef777da2c3ebba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:b163dd7a22752572de54e1ad41164210bd523429a0a1a468b044a3e15d57be7b`  
		Last Modified: Tue, 18 Nov 2025 05:49:20 GMT  
		Size: 3.8 MB (3826493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e42a99ff7bec57326251181a254efac43f68a96bb46461c8d09965b7b813eac`  
		Last Modified: Tue, 18 Nov 2025 05:49:21 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:624fb7c75eb4dfc1a0e9580a948f5d0ccfe4ac3a686ebcb63debe9563ac7d0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126680722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb4fe04507658627f7af998e4174707ddd33015746d482cbb88e1f10bc1c37`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:40:00 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:40:00 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 03:40:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:40:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130c91f5ad89607cd4a78f26b0151996fd585e2216bf95d3cbd4bb7c88fb64b`  
		Last Modified: Tue, 18 Nov 2025 03:40:36 GMT  
		Size: 78.3 MB (78321584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7b843541af0eb49312f22688bb23b09ac5e6dd753e1b62f65f1f3a103b0b5bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33dc1ad7278dd780c77bf470a370856933ad24bb2fc72739cf59ad4e99fda1d`

```dockerfile
```

-	Layers:
	-	`sha256:a3453925602a1f54bf6ab38b02865c1f74ff3b8f3d53bb1b7eb55912e66110a9`  
		Last Modified: Tue, 18 Nov 2025 05:49:25 GMT  
		Size: 3.8 MB (3824525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa6365b7557ab2b97f7d3fe395634c89e54e704932c859560569ba60cae0895`  
		Last Modified: Tue, 18 Nov 2025 05:49:26 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:00f6fc0cb813f11aea85cb307206f6b0206be6898081ac6409c8592d85b92b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1085c1beffc28445a0e8db8ba3e649c5e8c23d5f7393509e2d2884c46602c8e5`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:59:13 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 02:59:13 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 02:59:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0991a47298d4155a88ef64bdc55776a0ad48a112004ca6edc437f7b4f82c15`  
		Last Modified: Tue, 18 Nov 2025 02:59:38 GMT  
		Size: 70.7 MB (70724018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:267602ab63acba3593762bc7be6d3be559c467b5a1cfecfd47f932e99c6ab16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0af404eb3f676f3963e306f2ab0807d851dfa338e5388cea27ff5a186d5c97`

```dockerfile
```

-	Layers:
	-	`sha256:6e96a777be8cac0060511100a8a1ab7d248d07dc5de067c426685b77b1eb8a14`  
		Last Modified: Tue, 18 Nov 2025 05:49:30 GMT  
		Size: 3.8 MB (3821409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e0a56e7932e9e54ffe2ba07fe96139b61ff3238667ea6dbb2ac21ec316a75`  
		Last Modified: Tue, 18 Nov 2025 05:49:31 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:c901cc9c6d9263bfc04e06b332c5ee666438083d1e3b0daa2fcd4d70d0b70417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119432996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef6d8ee98bd3b5b6fc7d0a93b733e9fd51b3b9ccb06405db7da489452d421ea`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:52:55 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 19:52:55 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 19:52:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 19:52:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89570d36447ff4ab07d91194ab809405d565b94ff59e5e43c8f2f2029828b3d5`  
		Last Modified: Tue, 18 Nov 2025 19:54:41 GMT  
		Size: 70.7 MB (70672040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e3e31225c9b1b6725ef6e7a929470eb0e802cb4b6d6284769ce67c400ea1fc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7058e603e8f074910f05c887fb74fd59b12f34843ac112d08164bad0ab8bafb3`

```dockerfile
```

-	Layers:
	-	`sha256:d686e2d45b018d8fea3c6518233a12f7d44e74ed35edbe337b946cadaee30fcd`  
		Last Modified: Tue, 18 Nov 2025 23:47:46 GMT  
		Size: 13.8 KB (13782 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:4b026b1ee86bbe5548406b2d7440bf41e20978a626b79723f5dec8979a455482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124080097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6388ba0ab95c6ce6fd43e845502d5e9920322d72dc56a9b14b9327d9d2fd9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:14:12 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:14:12 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 04:14:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:14:12 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ffdf9ead95862c2190d07963b055c6e8e1544b6fb7b367c14e1d8cbbdf7054`  
		Last Modified: Tue, 18 Nov 2025 04:14:57 GMT  
		Size: 71.8 MB (71753134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:823e59aa980b5f7e9d1b055d445b0d9c6a145589bec1ab948f2f1bd7767ad45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2e42e5e4c06022b553193c09a83bf08df4add680486a413252f5e6e813197f`

```dockerfile
```

-	Layers:
	-	`sha256:1e489f9ecf51bfeab55d0695ad42e865263ac28f35364bec36b3c8fa19cda96e`  
		Last Modified: Tue, 18 Nov 2025 05:49:37 GMT  
		Size: 3.8 MB (3828706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843f286c41396df05ebd166eeffa6b5734d289937439fe6465692932397114f9`  
		Last Modified: Tue, 18 Nov 2025 05:49:37 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:e4e1e6399578611a54a07af2baf1180d59844174338cba35600c0a1e7bd7995e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117511864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781ff717dc3d5a6d23aad6d180b827e06d18c54b2a23044017bde7d605f107d8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:10:25 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:10:25 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 04:10:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:10:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcf8c46f1c54aee2dcf7947bade5d0db948e2be3b3677497c02cc96d48a3277`  
		Last Modified: Tue, 18 Nov 2025 04:10:57 GMT  
		Size: 70.4 MB (70374223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:afa94c46c24a4c1cf922713b31740e34f6ae66fa393b455eca52dfd9ddb0b319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2fc68ed46f2c9bc7df1e1b21ef6c0ee2867ed5f279111f0f0913887ea878e4`

```dockerfile
```

-	Layers:
	-	`sha256:d5246ebbd5b7cf77d279fdf0f6ffab06ae06487171764ccb028d0d4412f38d33`  
		Last Modified: Tue, 18 Nov 2025 05:49:41 GMT  
		Size: 3.8 MB (3821080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd8002bf0c7467f6f2165d15a045730e9733a499c34ecff390e2ec7a4b8ffd2`  
		Last Modified: Tue, 18 Nov 2025 05:49:42 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json
