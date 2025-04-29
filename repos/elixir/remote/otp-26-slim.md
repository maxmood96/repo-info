## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:d6a43ece049d525bd81b5fb351f6d577c8c7413767dbb1ed0f97b03fa509f283
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

### `elixir:otp-26-slim` - linux; amd64

```console
$ docker pull elixir@sha256:febad3d38e2e4a691a2fad8e9627fb089047ede4db476b62e2450df779cd6f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126805548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0995f3d22ec826e4216a0936bdba510efe8894e5ad79854cc942141b6233be8`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d814547f340bc43018d63da5334712b234e9280fea240f04de52635074eed3ca`  
		Last Modified: Mon, 28 Apr 2025 22:03:04 GMT  
		Size: 70.4 MB (70397717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a44aa7eb05635e699f733857132ca1af8685ebe5554122f4a49dd8194e37b`  
		Last Modified: Mon, 28 Apr 2025 22:22:14 GMT  
		Size: 7.9 MB (7916632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e40f8cc379c23571d9e67255213ca0b283e6a7e2dfb27fed7d5ea8808f7908ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87720cf8a8908c2c8654f6c49bf0c16874107bf2d6bc65792cd940be1482cb7a`

```dockerfile
```

-	Layers:
	-	`sha256:5ac4e31fe6bb59e22b50e5e4f03f8078ffbc42614a23d344389558b0d62b336d`  
		Last Modified: Mon, 28 Apr 2025 22:22:15 GMT  
		Size: 3.7 MB (3717750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c36840c398c5fb2a1089ef9b0fcf94e49a39e0b3cd6efdafb6155c5c7f9030`  
		Last Modified: Mon, 28 Apr 2025 22:22:14 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:e74ca810d560b53adb31c92dbc0fb20f6474925590efdd033dddd5e6f981cdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114373428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a505744f6894142ae1e17b8af6c95e5edbcd9a0aa260d7efbb11466f60b756`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae9225cc81a8c42f2b606893aab4eb722783e658236ebd63528e6b2d2cd1d7d`  
		Last Modified: Mon, 21 Apr 2025 23:08:29 GMT  
		Size: 62.3 MB (62260243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df0da1c21405209e08e7b47460e949d549eba66670e27f265687093fbd70c65`  
		Last Modified: Tue, 22 Apr 2025 00:47:02 GMT  
		Size: 7.9 MB (7916414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:de6e724411c20d77166c818404364bee0979c326c8a90edf385e7bf7ae035787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb808ab08a3834528d9e73787340b43c84d1e07ee002ca83603cb2e3e7593b4`

```dockerfile
```

-	Layers:
	-	`sha256:631c940c90bf78b9f157080e87b365ab75a1ec5d089e9b29480599a401980736`  
		Last Modified: Tue, 22 Apr 2025 00:47:02 GMT  
		Size: 3.7 MB (3719975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2027478c9e1d1acddb3a5bf89f9c11da00a8832c76daf2afa002d918ad0b0b`  
		Last Modified: Tue, 22 Apr 2025 00:47:01 GMT  
		Size: 9.9 KB (9858 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:12c7c0fe90c8b4d9006e57b2d0b90955f94bf32a6f5eca0a4c1c8b5e40eef9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126556800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c201a7bd42f856eb09a72428b29e1373f64803fe1756697e4b0a0aa5f32c6ee1`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b4bb7b9928d45c8121e29ed26e60a19200fe1585427e3cc8bc430bfa56c14`  
		Last Modified: Mon, 21 Apr 2025 23:08:55 GMT  
		Size: 70.3 MB (70312691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bfeb72a064632045e8c7ed61180d04d6147fec884f4f304d5cdf34c38c6e18`  
		Last Modified: Tue, 22 Apr 2025 00:22:42 GMT  
		Size: 7.9 MB (7916640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f7d2ed3bc591bc3ca147f19359948ddc9f97ef9256d9361e08bdc84404de9bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9548b8f4e30597e3f5723ae07dfcc7ff0d262e788d0dee85858bbe6ce5ad00bc`

```dockerfile
```

-	Layers:
	-	`sha256:ba47aba3844f55f22da4d275f32bc5b1963947118e597af99327499d7efd8bdd`  
		Last Modified: Tue, 22 Apr 2025 00:22:42 GMT  
		Size: 3.7 MB (3717999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c97359e34c24e269b135517d3194758f6b4e43ec5720548c40470140b484e2`  
		Last Modified: Tue, 22 Apr 2025 00:22:42 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:e61a1769682f9010d0f71d69b5c4e61fe66656c2c10520c99af4ee4eb03e9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118522401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18c36628327bd7cec04454025549a1fccee630fa4c73781cde47546d11964c7`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5198531576a5b2789f650e238c687551989558c961973200675fdfb1e28dd4df`  
		Last Modified: Mon, 28 Apr 2025 22:02:25 GMT  
		Size: 61.1 MB (61127462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5754ba40c06a159952a816afc0ae304a1fc93e0908554850c9eb6489946f4f`  
		Last Modified: Mon, 28 Apr 2025 22:22:10 GMT  
		Size: 7.9 MB (7916367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bc7f7946576518db834d2671516eae234bd508e9ccd856d6387df0402c2ae9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addae5895b707dac0dcd2fe300766e1fe2772998a27e07606b4f0fd814a03eeb`

```dockerfile
```

-	Layers:
	-	`sha256:ac2bdefe24f8b8c4999463ecbbb7fa71215aca21fb7608582e65d4099e5d5dc5`  
		Last Modified: Mon, 28 Apr 2025 22:22:10 GMT  
		Size: 3.7 MB (3714875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c244bfc0d434b5c6fcf5ca6e6689560d5b22ab44aad675cebeb0b7cd8484570`  
		Last Modified: Mon, 28 Apr 2025 22:22:10 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:174ca699de5e1b529a14a5f6cc0107466bb72a276a7f640f5573bb985e8023de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124963382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b54eec21dad9eb85d6e91639e7b3e10ff71ca303a17fc80d4b760b6fc96acd9`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e2fa16215d0633b1567dbb2dee87bdaccc613b968875bbf7fc335602ff6e11`  
		Last Modified: Mon, 21 Apr 2025 23:30:27 GMT  
		Size: 64.7 MB (64714650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c236c41cc1e74fb4e6a3c96d6d08d98549a1c08df61da9ebe8ecce0140b5be18`  
		Last Modified: Tue, 22 Apr 2025 00:59:43 GMT  
		Size: 7.9 MB (7917086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2df11f4726aef25da885ed13cc250763ed1b32cfdd2a654e974be81bdb6358d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb2937d251d167b5d5d406e620295b3772dc6674412552c5e32dce6be550630`

```dockerfile
```

-	Layers:
	-	`sha256:35acf66f31bc11b7052685e2ccddade663b303aa61602eca38e972c5bc17e63b`  
		Last Modified: Tue, 22 Apr 2025 00:59:43 GMT  
		Size: 3.7 MB (3722084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4218fb7beec81edfda79ddf9299a7ae28ac79ee585de3b2d08c285efc766c08c`  
		Last Modified: Tue, 22 Apr 2025 00:59:43 GMT  
		Size: 9.8 KB (9828 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:c898a83ded2edd2911d97ae007b941cfc3d2edf82184ea0b55d1be805937755f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118309064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba6c5e686774e5b1378462e3e9d2a81d181204556bd74cfb845eb26237e0a3e`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 16 Mar 2025 23:57:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Sun, 16 Mar 2025 23:57:04 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.24.0
# Sun, 16 Mar 2025 23:57:04 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce2ffc53815e6ed0fa201669ecc20b63d632588bfdc28de1cf7e30fbd4838`  
		Last Modified: Mon, 21 Apr 2025 23:00:12 GMT  
		Size: 63.2 MB (63241743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea24428604c55c3dfdab530d2525f52b4a6f545bf74394a5d1bf01676289d4`  
		Last Modified: Mon, 21 Apr 2025 23:50:06 GMT  
		Size: 7.9 MB (7916325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9da57e1d20c9d2ad50291b2cca736adcfb9692a835726a98c41e17dd5bd4b920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394463392bd9479c7c9a7c55f19628daf6e7b689962ac8dbf9c8d12239c5130d`

```dockerfile
```

-	Layers:
	-	`sha256:9db63734a323a00b1a82c23ad80e0bf38d87366f91901e442de2c6c13cd6a0bd`  
		Last Modified: Mon, 21 Apr 2025 23:50:05 GMT  
		Size: 3.7 MB (3717470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfacb9974a632a5f2e8b8a74523084a136830bd4425babb65b795d684e9ebec`  
		Last Modified: Mon, 21 Apr 2025 23:50:05 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
