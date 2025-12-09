## `erlang:slim`

```console
$ docker pull erlang@sha256:ef903afbd674ffd6ab135f4e7ffe02d475d6ef53f9314f6ab64dea4f0056a00d
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
$ docker pull erlang@sha256:b8edef6a3a8b08d8429816c6a1ab17961a586dead7f0265ddd2b744b76759b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129165247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dabc7e1d7b80cf32992e8ebd7d697643aceeaf654a749fb3c6a24a3ec6a233`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:18 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Mon, 08 Dec 2025 23:11:18 GMT
LABEL org.opencontainers.image.version=28.2
# Mon, 08 Dec 2025 23:11:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f1dcef385f56612adbc5292be10aad0bcb8b65ee86a2e6ca8722eda5b6597`  
		Last Modified: Mon, 08 Dec 2025 23:11:49 GMT  
		Size: 80.7 MB (80684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5a7395ded69eacd631f7438f97b3b482bf4a38c39184f2de02de46a859ba742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b0d86eaf13bb24d67335f88d5177c15354003262a613913d4082d6c066acc3`

```dockerfile
```

-	Layers:
	-	`sha256:c762428132738336d888a63394ee74096675ddf044b6bd96cc86ac39796efc64`  
		Last Modified: Mon, 08 Dec 2025 23:48:20 GMT  
		Size: 3.8 MB (3824270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db47f7d726ff41ac64cb0679f2faed9024e85a5ae6d6db920e985f2863557e4`  
		Last Modified: Mon, 08 Dec 2025 23:48:21 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:6c393d625d2729de63f080f13fd19a3bd1a735ce2ef385f5b79dccd9c8be02cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116371581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf0974897f880366b84d64d655cf2e0825d526d1c0cc5e4cd26d096288c2de`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:58:33 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Mon, 08 Dec 2025 23:58:33 GMT
LABEL org.opencontainers.image.version=28.2
# Mon, 08 Dec 2025 23:58:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:58:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86817c1965f7a91787a5052ad7df5407f0e30951ee0be16fe4ed1188312764e9`  
		Last Modified: Mon, 08 Dec 2025 23:59:00 GMT  
		Size: 70.4 MB (70355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:958dbfe06ac7166fc5c0015ce99bd3b8b0cf830c89ef7b139b14cd72b362b9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0685e6841a4421dbe2a4d03e2133ad558a9905d1e0b22078a9a3317dbd8992c`

```dockerfile
```

-	Layers:
	-	`sha256:4949686df24e9eb014e33099cbbeb97c1468834bbf1bb5eb3d75136cfd80df78`  
		Last Modified: Tue, 09 Dec 2025 02:49:32 GMT  
		Size: 3.8 MB (3828086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd60629d684c4708dc1194fdf2cd1c8b2b4abe36c810a3cbe28ef0c1211e035`  
		Last Modified: Tue, 09 Dec 2025 02:49:33 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:bdff449eee7b67ff8c77f197d9d41b8e2774de06433f9b13f582a6c0fcaf2747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113959757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a115c0279d873d6fe15ea09e85b2337d07f650c405235b61351950d0f485737`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:14:52 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Tue, 09 Dec 2025 00:14:52 GMT
LABEL org.opencontainers.image.version=28.2
# Tue, 09 Dec 2025 00:14:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:14:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f297570aeef856bad0f96171ae776319f1f7ab215625c59912e31ea4841df92`  
		Last Modified: Tue, 09 Dec 2025 00:15:17 GMT  
		Size: 69.8 MB (69763691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f9f38b3b2a7f6ae962d6235b3f486317da074ddbe03f466d8f8c0222a343362f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38b0b2a74aae7184814ef1697fe52185ed6e3ae496e57d5a6ad700f0f704e1`

```dockerfile
```

-	Layers:
	-	`sha256:f26d06497d9275551faa1c4ef8961fe8d9803c161b36b900633d2f813caf8d43`  
		Last Modified: Tue, 09 Dec 2025 02:49:37 GMT  
		Size: 3.8 MB (3826511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf929fd724e6f34f49fa27cdf43486efd20b3f1d1650528653cd78a63637fa8`  
		Last Modified: Tue, 09 Dec 2025 02:49:38 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:7a965e7b470cb9d9027c72d8c4305989a78b91afef836a1d0a47c14404aa956a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126832184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98f08b760fcd209c85784a7c247dc5cb6cf6802d376a284bb9a84d596c23d7e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:36 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Mon, 08 Dec 2025 23:14:36 GMT
LABEL org.opencontainers.image.version=28.2
# Mon, 08 Dec 2025 23:14:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a5ccd93d0123676258989bce51685eaf221e3c0a68ca30d936196bb4924bd`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 78.5 MB (78473113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f7f5d2157ff16e4c6e6a6e4ca5f2010f3670399ef2b000c0728e7d76f0e1bcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8438d338216b334dad4ffcd59e0e1d30b0e82b07805ef63f896f455c0ce0cb36`

```dockerfile
```

-	Layers:
	-	`sha256:9c66745e5b7adfa5e8d4bd8c0a93c3289d039eccbeb6e50f6acefa01debbabf7`  
		Last Modified: Tue, 09 Dec 2025 02:49:43 GMT  
		Size: 3.8 MB (3824543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a5ea1c3162b78310c5c6bf6b2eb7000a303d6905762ee3b65411358a11bdb9`  
		Last Modified: Tue, 09 Dec 2025 02:49:44 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:28212a6bc1e94801bb6164e900e6f87c2285e88f72e0ad52648fc8319ed4bced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120366590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b343cf25a6b8670bfb5c9309e03d256ec00eb9c6e99ce2782fc4e1720a370b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:16:16 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Mon, 08 Dec 2025 23:16:16 GMT
LABEL org.opencontainers.image.version=28.2
# Mon, 08 Dec 2025 23:16:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34efecbcdc44f7a6f1c506c75ce4cef9092234436af1a25a20b444a40a61f248`  
		Last Modified: Mon, 08 Dec 2025 23:16:44 GMT  
		Size: 70.9 MB (70899771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0a50d12b2a70071561e1beb6511510d3b67c60009ecf823c16dbea44614be9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba585420caceaede74ed3b1f08d879dcc2c05cc8a54a4a7305619453aecc2871`

```dockerfile
```

-	Layers:
	-	`sha256:4b163da16598812136b7228823b43be2ee2bf136f963734a1719ec2969150525`  
		Last Modified: Tue, 09 Dec 2025 02:49:48 GMT  
		Size: 3.8 MB (3821427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e34f7a9587545d6535c4b39b1c8ae1cf61e53c712017a796ea9f0716b59b8f`  
		Last Modified: Tue, 09 Dec 2025 02:50:13 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:0f9e1a5df1a4b62aec7b769cbce666e70e8d92f8e97f6cc02b26290bb579037b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119598546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1477d796d0f7d34b246033d0440ce0de6ac136b51e39e2497b8dd9785bb91fcc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:22:27 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Tue, 09 Dec 2025 15:22:27 GMT
LABEL org.opencontainers.image.version=28.2
# Tue, 09 Dec 2025 15:22:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 15:22:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6d5489bbb5a502de2fba0452c392069272fe5b2054b559b9f3875f07f34402`  
		Last Modified: Tue, 09 Dec 2025 15:23:49 GMT  
		Size: 70.8 MB (70837649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3f315019d3fc54baa59123dc2d837cd401b4cb0047b4e0624801ffd01474ba6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457033923ecbe013796d9dc207916e90bcdb0060398ef4fdd87d441e84b9a66b`

```dockerfile
```

-	Layers:
	-	`sha256:0bbf84fea2283f5a8f49b176e75347fcd331a0a2f3d3967c82494f7b381bf08c`  
		Last Modified: Tue, 09 Dec 2025 17:47:45 GMT  
		Size: 13.8 KB (13781 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:af854007e503f15acd8cd8b98f85a37fb1f8c5eea3748ba3026999fc5f392ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955c07e2af45cad3053b09d54ce9fe2563428e836252f66f4b4680b46f9deee2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:19 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Mon, 08 Dec 2025 22:33:19 GMT
LABEL org.opencontainers.image.version=28.2
# Mon, 08 Dec 2025 22:33:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fab34681675ec1b59729079146a8e3440c98dc95624de20334b4a98fa4f367`  
		Last Modified: Mon, 08 Dec 2025 22:34:02 GMT  
		Size: 71.9 MB (71917281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:01b6f10bf67ddcc0844a436ed4e9fe55e9975708ef901c41f3e05d1b5b795857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1201fd2072701495c14e25a48999cb9d25cf59ef9ca1a5765abedbd4b929faec`

```dockerfile
```

-	Layers:
	-	`sha256:030a11cf7cdb0e9bf0e53b23c09f5e0e73f664eae2da6f492d315d9cc0c0f32d`  
		Last Modified: Mon, 08 Dec 2025 23:48:43 GMT  
		Size: 3.8 MB (3828724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d68e1b11d6ec2db9efc51318e6c490f45bc275fd61ce87f46cd1f29f3cc1fe`  
		Last Modified: Mon, 08 Dec 2025 23:48:43 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:96055468a59a5c19e522c686a896b6f496c101b641df8c831b475a129ea38924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117668409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae900ddfe70fd6c67679a6b52abba2bd519b58af8ea018220007e154a15872b8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:16:42 GMT
ENV OTP_VERSION=28.2 REBAR3_VERSION=3.25.0
# Tue, 09 Dec 2025 00:16:42 GMT
LABEL org.opencontainers.image.version=28.2
# Tue, 09 Dec 2025 00:16:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b0f6e1273a034e91c4fa6895e8cb84276baf5ca7a23b29da4f04ff9d0419a0c2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:16:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3c9e1d0e5edaf6ce4103de87f8820afb1a8d80cc2152e0f15fc6fe5fff679`  
		Last Modified: Tue, 09 Dec 2025 00:17:13 GMT  
		Size: 70.5 MB (70530744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:16616de8cdfa29411802d4ba2a374f763e15aee57d1d1b2424976cf22755c0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77169dd695097ba3b6845af9da3bbaf3b88d80808bef175e9e8c615d1e8e385`

```dockerfile
```

-	Layers:
	-	`sha256:9cf90bfc9947f81565b4415e8e3c090d9404c746a993fe02ac3b0ce468d83337`  
		Last Modified: Tue, 09 Dec 2025 02:50:27 GMT  
		Size: 3.8 MB (3821098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336ff7b88ca0e1223599279febf9cebbb59147647f222b38449d7d7a3dc89104`  
		Last Modified: Tue, 09 Dec 2025 02:50:28 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json
