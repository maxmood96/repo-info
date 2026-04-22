## `erlang:28-slim`

```console
$ docker pull erlang@sha256:a73793d367be20c0fb602be028738b554dcdfc6bad6d538ff0ba3cda5e58f1c1
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

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:0b86f8fa6f89843f7591969407732cb42d0070d4f2b44c7eb1c842dad4c624bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128220844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d561ea3b5185a224b464facf12cecd21ba0426442615c17c2d8087ddcab812`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:34 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 01:42:34 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 01:42:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d393a73dd0ca85fd769b3d9791781316dbf344e2c3da69c07a74229dc38b56`  
		Last Modified: Wed, 22 Apr 2026 01:42:49 GMT  
		Size: 78.9 MB (78918742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fb11231a36deb0d34cd5aa2ee39c93c9031d48be7685c1e420ed2ca00754d97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fd278d474a716767b3f682b9aaf25a3e00ef2f16ef0e73a1a75ba7fbcaa750`

```dockerfile
```

-	Layers:
	-	`sha256:aa777a6782e66f887ab93c6dcb5df3f8bb7180c789d33e685a534b3fc61256d2`  
		Last Modified: Wed, 22 Apr 2026 01:42:47 GMT  
		Size: 3.3 MB (3283924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64ee9252bdacfc3ebb26a450f4ac5a10d592d8d7dacea5a566f6d0594b48b33`  
		Last Modified: Wed, 22 Apr 2026 01:42:47 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:fa48c0e0f9c3cc2e070449b8c9cbf67e87c01e21a2beed107a85c1e9bded75e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119818524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cde6463156c491a82310768989e5c5b5fdc1f4ecf351aa56c7fbeb16d001880`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:32:49 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:32:49 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:32:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:32:49 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21943f110ce9876cb438a4c2f7cc5c395085c6e72191fe6440c1e9fc41a57b37`  
		Last Modified: Thu, 09 Apr 2026 22:33:03 GMT  
		Size: 72.4 MB (72357632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:61925cc6bc43bbb4fc9f0e2093e124ce78896aba9425686b0a4cf1fef842dc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106ae04a0b0719e4aadae3ebbb49a3d9e3ee289e2a38ba0afc24ad0772763d46`

```dockerfile
```

-	Layers:
	-	`sha256:42b1aee91a29622db79b138e8670b3f11c55d47eb12384ea261a9bec4059b776`  
		Last Modified: Thu, 09 Apr 2026 22:33:01 GMT  
		Size: 3.3 MB (3286899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09814a02bef5e0acad912a8b9d025248a1f00e3b18ea6c78ffd95122b1e066b5`  
		Last Modified: Thu, 09 Apr 2026 22:33:01 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:78f4d930a5b0c909550c174c7e5e83c0d97d7ac1a973fc98cf7ddeb5941fc4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117496716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83aaafd528bec042a16b0105b0dc72f0cc83e8649285f66a3becb8c1a22879c1`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:34:25 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:34:25 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:34:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:34:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b760f3169cb41610bef4cd992754032cdd34ca3c20d6ea4255f3c174fb71ad`  
		Last Modified: Thu, 09 Apr 2026 22:34:39 GMT  
		Size: 71.8 MB (71763719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7ff32f3585f29ec2aa0f782a0b29c25a15fbd847f402581a372554eee536f5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e979c619c77021205f7a74574e956d1d381ba5bfc903921047b8dfae0365f107`

```dockerfile
```

-	Layers:
	-	`sha256:5bb4ac4703eae13a9443096b243648ee2a6adcf881c8ff4dab50c1d4a96f1c56`  
		Last Modified: Thu, 09 Apr 2026 22:34:37 GMT  
		Size: 3.3 MB (3285348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b6edc2f42b2ef7e1e820b1e585933eec0c9b007ae6fe495f5aa1ba8c350b9a`  
		Last Modified: Thu, 09 Apr 2026 22:34:37 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:041b5ff1da4c5105772f89d41a56ff51f4d01235ff4c9bac660a253143ba5498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131021706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57471d0ecf3603db0a05fb32ec378b6f3f4855c13d2ad1b4f0b59846f38d1cd6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:22:38 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 22:22:38 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 22:22:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:22:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bcdd02f0073350e751961feca8f31af985d09e4247535b7c9ebc0b364998f`  
		Last Modified: Thu, 09 Apr 2026 22:22:54 GMT  
		Size: 81.4 MB (81356450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9cdb09bfae9c0a4575160075339b75e68fc2edc841e98546561c7de3f5d6f793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7213745a4ee099620992f1d7774700c8965ba0a3c1152bb2ed7a3a6e228f91`

```dockerfile
```

-	Layers:
	-	`sha256:f0fe6f5964362144be7eab6df11b61f0f37814ad7c4e5696a4fd5e3a566f359a`  
		Last Modified: Thu, 09 Apr 2026 22:22:52 GMT  
		Size: 3.3 MB (3285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1521a2d270d070fce9f0bf12ad93c674c7bcbbc01a4df166be43681624890027`  
		Last Modified: Thu, 09 Apr 2026 22:22:51 GMT  
		Size: 14.0 KB (14044 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:d3448b83f7ab82d46f466754266697a0f30f6a4faaf74a374f299877ab38993c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123654806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dd46c7b503b3f0eb5849acfd08db5f70bbc81b2fc421d17a71ab49b9ea8187`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:23:22 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Fri, 10 Apr 2026 00:23:22 GMT
LABEL org.opencontainers.image.version=28.4.2
# Fri, 10 Apr 2026 00:23:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 00:23:22 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c894a9e896a32a02ade33dd554cbb8111bfffbf3e2b653dd88ce426539cb5e`  
		Last Modified: Fri, 10 Apr 2026 00:23:36 GMT  
		Size: 72.8 MB (72835718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2dc760d91c4cbfc2480573f3f6307994c4540bea64e0a30f92040bc266437251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab03f8f776cb38d8ce6b23af6930c767c4d3099575f867447a3ef50381ba386`

```dockerfile
```

-	Layers:
	-	`sha256:1d48ff0be567e89b3736874aba36debc1d1cd03374f2d17f832984a47b1a3bc8`  
		Last Modified: Fri, 10 Apr 2026 00:23:34 GMT  
		Size: 3.3 MB (3281094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5c0a77085fe053743f0c8ed857c144bc0c1d31035bd94a2d99dcc263491f44`  
		Last Modified: Fri, 10 Apr 2026 00:23:34 GMT  
		Size: 13.9 KB (13892 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:8cf6855182c84cd7eb73acd91892956a95625479baf78066854827c1063192ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127253540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57e534520e4b1d14b0a07457b34199c13669948189d8877f68f1a929de494cb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:30:29 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Thu, 09 Apr 2026 23:30:29 GMT
LABEL org.opencontainers.image.version=28.4.2
# Thu, 09 Apr 2026 23:30:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:30:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5e42683d740b95bd04a71d2405e7ca422f508c99d80f3dd7ed6791fd73659`  
		Last Modified: Thu, 09 Apr 2026 23:30:56 GMT  
		Size: 74.1 MB (74134871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:59ace8012129d738da86df62eafd9d7bbbf74419a85c40d58d3c7886b3b42074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f93e36222415388cc65c9fb46600c016fcc5a8695eaa5efc27f24a83f0c502a`

```dockerfile
```

-	Layers:
	-	`sha256:ec52a19d7151eef8a7c8b17288db7db31d7416f2d47bf0421263ff2411cf0c12`  
		Last Modified: Thu, 09 Apr 2026 23:30:53 GMT  
		Size: 3.3 MB (3287515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d1c6ca7ea32b1b508d885eb43f6aeb5235c46fed504b97d2158a4d1b802a48`  
		Last Modified: Thu, 09 Apr 2026 23:30:53 GMT  
		Size: 14.0 KB (13978 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:e0abe93a2c0e87354cd99ccea46522fa29ef0133d4fae8debd25216179b98252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119627607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2173e7eed843dbb3074a241d667f87aa6cc8e1e25d11587ce573f402ca9e46`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:36:30 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 02:36:30 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 02:36:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc453071290130f462af617a626df46ce1a805c0d32dd6134bd523c1bcba66ad`  
		Last Modified: Wed, 22 Apr 2026 02:36:50 GMT  
		Size: 70.3 MB (70255501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5e9daa3916beda0bc984502ae91e32982ff848f8f10070a891600cee1487392f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a6363e6f43d59beea1a5ec8295691897360b0b3fbb5273413decf6a3253756`

```dockerfile
```

-	Layers:
	-	`sha256:90b58547b8b2a877310b030f5a001bdb2f4583eb949f50c9b8d416ea3f26ce69`  
		Last Modified: Wed, 22 Apr 2026 02:36:49 GMT  
		Size: 3.3 MB (3285365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec53e49bf47da9f060490f4737a6e367395a5e72f6d24340c783a9ea92e88137`  
		Last Modified: Wed, 22 Apr 2026 02:36:49 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json
