## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:cc498774c9cbf6f04da0f1aed04de9ae64cd64e224dbbf0cfa5b5db3d153eb76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `elixir:otp-25-slim` - linux; amd64

```console
$ docker pull elixir@sha256:b7493990ff0e45dc0d290c46444a2f14068228197bba4fd02361f4268c49e1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128455870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91678a8ea436f93601a1f92f3324607db60b33ee37dfd31ed6e637869bd665e4`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593d6d70bbdf0eeae0ae050e7328bd4d54f73f9ae17a4ecc80d67c0fd37b043c`  
		Last Modified: Tue, 13 Aug 2024 20:08:26 GMT  
		Size: 65.9 MB (65910475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93527666c43360a8012e489a534dc881afe6df3fb5d9e8bdb06bf7d806ea4`  
		Last Modified: Tue, 13 Aug 2024 20:58:28 GMT  
		Size: 7.5 MB (7460720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2762ddab73bbd81ff409cdb2f8c52df30d55bb805215eead7e54a9f2c5de888b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9904c874aad8606706f33ae2574929cbd733e5d2faafbcc8770d5502d723f1`

```dockerfile
```

-	Layers:
	-	`sha256:1113219a0b63cfe37e92e5b731c0e59c87a65fa06a9d9e296afbcc7c65c1a28e`  
		Last Modified: Tue, 13 Aug 2024 20:58:27 GMT  
		Size: 4.0 MB (3986732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f6be88e46271d7d4841dd1e02e0b207922ffae81a60d1d851c530cd9b9a2a3`  
		Last Modified: Tue, 13 Aug 2024 20:58:27 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:d99cac17ba06728812d49e8153c021cd2bd94b5b73595cff180807c4a549632b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114910645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a902ad935d13cc4ed4c6825edf6c797f4b0e84dc89b1fb6f82e3a6b913a3e31`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb50b74ca5e82958badcae0eeb369f96960d720941bcb203da26ba2708adb1d`  
		Last Modified: Tue, 23 Jul 2024 13:27:55 GMT  
		Size: 57.2 MB (57208083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7daacc812c5a0252ed697eb748128c2c6066463e6eb3d588f879224eca96cf2`  
		Last Modified: Wed, 24 Jul 2024 17:46:34 GMT  
		Size: 7.5 MB (7460207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:15de95c33758a859812d26f06db72eac1efd193bf6c0979eb52494f0ad0d69fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d778c74f72cd39709b8fb29d8e23de2cc8964a2d4fbe99d0480ded8f4f8669fe`

```dockerfile
```

-	Layers:
	-	`sha256:0af53af31315df30244446ea7a56a6267e4740845f5391f01b9e8b0774b31518`  
		Last Modified: Wed, 24 Jul 2024 17:46:33 GMT  
		Size: 4.0 MB (3987705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9dd3220de3cd4acd5188d68f4eeb7f07fd96061294cf92dd42a08ef7092847`  
		Last Modified: Wed, 24 Jul 2024 17:46:33 GMT  
		Size: 9.8 KB (9836 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:c3314880dd47c7d18494453d71d81f1a72f3a063fdf1cb43ffa646af5c1d35fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125473655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9418f80c7c2c1979c220e9ec63786cd56b5f09b5aa963e160d3e1590fc1a1d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0618f36fa2c4e7fdd24bc7a5ae6bacda056a45cab23a10cb125e7d4ec3f6636a`  
		Last Modified: Tue, 13 Aug 2024 21:31:24 GMT  
		Size: 64.3 MB (64283156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5aff66b5240e755bcc4a2885651cf2e677f78f3a5abed0672d28b8ed57b7d6`  
		Last Modified: Tue, 13 Aug 2024 22:35:15 GMT  
		Size: 7.5 MB (7460578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:36d028c6854cc6f8bb70b49bc6ee32f2b33dbad145024f03624227474dde32b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce727f3bb0a3dee0b4320d19a485cf05d2e2985d1ff5db48266e6944dce00dc5`

```dockerfile
```

-	Layers:
	-	`sha256:d1aacdb9c90cb3c5eb219c829f00e819bef1c066ffa2f8efba87439a5f72ec91`  
		Last Modified: Tue, 13 Aug 2024 22:35:15 GMT  
		Size: 4.0 MB (3986339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2845befea8289f14bc1407926c0f44fec05ed324a77b70dd912cd405fa6ffa4e`  
		Last Modified: Tue, 13 Aug 2024 22:35:15 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:a4d0e9a1bc2b6e9311ef3eea4a45dc9263a1293486a62c3b9935c185a195dc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121126094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b0e2cb6ed57b0a78145f35a3576da86b8409ed7465d99ec672bf53dc0c1fe4`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2fc81f40deebe0b7924250a2df45c5624fc8afbafc4c49fde3f75bbd6ffdda`  
		Last Modified: Tue, 13 Aug 2024 20:08:42 GMT  
		Size: 57.6 MB (57591622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d82ba4024648b417d69f287f3bddfcb1da93710c86d8e2ee244cfc8c6cb16d`  
		Last Modified: Tue, 13 Aug 2024 20:58:45 GMT  
		Size: 7.5 MB (7460368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:695371418a23b4d18e6e76f676475c77f9e952bd24168b8455e50769f3ae998f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336608e5e4e56b9cb35290ab807de0961467d402c0e5f7e0ba85e6fa0dca6bde`

```dockerfile
```

-	Layers:
	-	`sha256:91585ba0bfd5dbda69736e3e4f31d63c45998fd96c41b809d57880240164bf61`  
		Last Modified: Tue, 13 Aug 2024 20:58:45 GMT  
		Size: 4.0 MB (3983213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5fd6598e2f70208d1a35199efed6209800a57bd254d0a5fbd637962ccacd2d3`  
		Last Modified: Tue, 13 Aug 2024 20:58:45 GMT  
		Size: 9.7 KB (9729 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:5dfcad9631d27b72d01a8500407a6b93f97de0acc39538a8221b5e6ed4ae8253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124938125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc88dc3577d67930fbaf4236572527a43598968bffc3a2514bd9ac54863e526d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2494e645b04e9a7361ff760ee764670bb344392a90a03d0e5f2dde8c87c5e`  
		Last Modified: Wed, 14 Aug 2024 00:05:36 GMT  
		Size: 58.5 MB (58522588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a981c35a1c82d3b6245729b69a9ce1fd60042ea4d3331d9f932a7cf5108e40`  
		Last Modified: Wed, 14 Aug 2024 01:16:23 GMT  
		Size: 7.5 MB (7460883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:53461fe8758ee8eb328db5c768219b28b69e6656291f585db07927f7a87e8cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc95ea3597c072eb49c187890107929a21d31dc02ad80b4516a81971feb07f11`

```dockerfile
```

-	Layers:
	-	`sha256:f76120468ddba49ab21afa843e4e775c53f5a1381acf4e51389b712548969717`  
		Last Modified: Wed, 14 Aug 2024 01:16:22 GMT  
		Size: 4.0 MB (3990450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f6fc87bb71c6425d83c9b5deb54f8069d31c775f31ce52b30da54025634ae39`  
		Last Modified: Wed, 14 Aug 2024 01:16:22 GMT  
		Size: 9.8 KB (9806 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; s390x

```console
$ docker pull elixir@sha256:eff0a12345d579ee053f469ea825e20d40c9eb0578005a76716ae9950235b457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118897010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5042734598940e3c9055342ea084f12a3838556dd8a708961b4272f6b576757`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 16 Jul 2024 11:38:06 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["bash"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 16 Jul 2024 11:38:06 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["erl"]
# Tue, 16 Jul 2024 11:38:06 GMT
ENV ELIXIR_VERSION=v1.17.2 LANG=C.UTF-8
# Tue, 16 Jul 2024 11:38:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7bb8e6414b77c1707f39f620a2ad54f68d64846d663ec78069536854247fb1ab" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 11:38:06 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bac2e363a291c07f534dca9497253afb686f923d0ec8f255ade644c3b8e5adf`  
		Last Modified: Tue, 13 Aug 2024 23:00:34 GMT  
		Size: 58.1 MB (58112479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ee93ad5f402d17695aa16f3fbde87c2ec57118ad401f0a6db3cc1533087de`  
		Last Modified: Wed, 14 Aug 2024 00:12:31 GMT  
		Size: 7.5 MB (7460442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:691d404b0523411a21ae6421702c97426f31f905bf0b64dc093b4ade0333c294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9ee73e767fedda176024da3a0a14fcae314e91b9dca06f2a9fe428b324c1bb`

```dockerfile
```

-	Layers:
	-	`sha256:449d175718f668231d25ea5674e8075f3c74ad99e7d9ff53afa5eb3131700088`  
		Last Modified: Wed, 14 Aug 2024 00:12:30 GMT  
		Size: 4.0 MB (3986297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01678a6afec6f4b399490822b4779adf812b5da2c1d0f4aa552e749cfefdeec7`  
		Last Modified: Wed, 14 Aug 2024 00:12:30 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json
