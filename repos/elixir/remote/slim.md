## `elixir:slim`

```console
$ docker pull elixir@sha256:57b15fbd5bc159a6d453b6506d73282da88b911d82c4e869e3f9f657a7bebf03
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

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:3e692db4d8d0afdaf0b70b04b415ce490bd0decafb70a3fbd1840311143b330a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4846611232796d5d64929a4261d99d09c969b6d9b27521f0f8bba2bd25bd85`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563d31a119ec367a4e92a7975ef94c2a683ab7d3405a8a239e9067f651c088e6`  
		Last Modified: Wed, 10 Apr 2024 09:13:19 GMT  
		Size: 70.3 MB (70271893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edb7ea8742dff348f605ef99c93cb11f0e66cc66880f96e6a8ad48148676e5`  
		Last Modified: Wed, 10 Apr 2024 09:56:08 GMT  
		Size: 7.2 MB (7212430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5423e07b659f9140386f0049092b66c297ebe4158cf1ca8d0db776e5cb0a4f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3649911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2de85c474afbcfac9a5e2f8265d4ce064279e2f56170c8e40c7bfdfb177a6`

```dockerfile
```

-	Layers:
	-	`sha256:61f595e9ca616f75fbc709853f16a913f7fb1c09425d18de1e084ec885e81d96`  
		Last Modified: Wed, 10 Apr 2024 09:56:08 GMT  
		Size: 3.6 MB (3639177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1d4934080e0baf34cbb3d8f059adb212a2a0fc70e524b53582186bb8684464`  
		Last Modified: Wed, 10 Apr 2024 09:56:08 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:42468412c7dd354d4eed685ebf934cdcb5c0f1587429a8966c0e95f00c85d027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112357857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4415b8a9c0a69bc133fd1f7efbb1d199d23597a8d24883a8f1ec2fa078ee96ed`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a36aeeb6fe3321c06cef68317d1ec3a6031174117522cda87373dc1c25bdd6`  
		Last Modified: Tue, 12 Mar 2024 02:07:08 GMT  
		Size: 60.0 MB (59992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c977fb8cac389a418caa4ef453de12b4c07db23640997b1523ee436dad98e`  
		Last Modified: Tue, 12 Mar 2024 14:54:46 GMT  
		Size: 7.2 MB (7211684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:73e688b6927216a706e51cdf0fce6adc81320e28d031b46b691a6464e01b8dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c0de0cba2226fa172390d6abf22c670c213d19b27d663be0f6066a507c23ac`

```dockerfile
```

-	Layers:
	-	`sha256:41ac797918ff586375a33d586ce86e453eb1253a7854059b6f25102fb3b838ab`  
		Last Modified: Tue, 12 Mar 2024 14:54:46 GMT  
		Size: 3.7 MB (3687705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926c303d14fe53825c9b4b505e6b4c0e02439054362fb820a8e0a326bf3a0079`  
		Last Modified: Tue, 12 Mar 2024 14:54:46 GMT  
		Size: 10.8 KB (10820 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:9fb7544b915506c8e9c1b65e1f9083d842eb45b3f0c6db3311f8c4e5da869140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124699628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049335dd1ed30f889718c71d2fd5e8d7ec8a90bc72e9f228cb7581ba2ae993b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7824522f8003386f1f7437549ba20fce5fbca1763753106985c7f32559b97fd`  
		Last Modified: Tue, 12 Mar 2024 04:06:59 GMT  
		Size: 67.9 MB (67896322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b43576f14b2e11a013ea1e43a1bbdbc62ffe5c488df9ed33fb46535c2e2085`  
		Last Modified: Tue, 12 Mar 2024 15:20:16 GMT  
		Size: 7.2 MB (7212322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3e9f134658366e8c45d5fe7bfcc0dd9f49855d9b759aa1e2dae9350f6c738196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d2411eb6a44e06939e11b3ded4fd6f5e02c43656bfd996d525c8e8e788ef3`

```dockerfile
```

-	Layers:
	-	`sha256:c39abed64db58fe22f37175e31ccc2b189b8bbeea8d46b5a643b070bb398bb96`  
		Last Modified: Tue, 12 Mar 2024 15:20:16 GMT  
		Size: 3.7 MB (3685676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0e475156c9e7b844f1329372a9f84364f07acf3b7368a831eaf6b7247a9838`  
		Last Modified: Tue, 12 Mar 2024 15:20:16 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:bd796489c8c894dc5253c9d4471ab9257bbc52c3ae748cb3a656c07e32c2ec47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118793540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaac84529ee8dbcb79d0cf56e9df44656e0b741a575bffa2b9b945415b8cd19`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e56fecce12e5511b3c3b031b90208fb4ff7fc47693246b0cf160a4f9ed2d47a`  
		Last Modified: Wed, 10 Apr 2024 11:34:58 GMT  
		Size: 61.0 MB (60994428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0ffdb49b15ffd16dc37f6a90f23b30f6202701a2054baaee6c3d10bdec531b`  
		Last Modified: Wed, 10 Apr 2024 12:57:03 GMT  
		Size: 7.2 MB (7211878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:feac81420432e382e930ff51af2d33b0efe0e93b7049f110adcdf70d659ece10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f039df63275eb0c1a40b84b7d6ae648e51fed2c9a61269abb91c0ca2d26fa9c`

```dockerfile
```

-	Layers:
	-	`sha256:3cee658e73d886493a6235c521b0540117c6b95689f64fb395088d65f11c4e67`  
		Last Modified: Wed, 10 Apr 2024 12:57:03 GMT  
		Size: 3.6 MB (3636285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a728b21c1ad5ec1b38b9e403a3ce687ec0815c8e8eb411ca9ec3c54420bffe2e`  
		Last Modified: Wed, 10 Apr 2024 12:57:03 GMT  
		Size: 10.7 KB (10694 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:e604b44b4e864b3419f9351402f58920d90825ce3b587164be20122a906b0d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122856743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059c018498592bec5df90d426f67c02ad70f8c60901a49d66afe38637d1ca7b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6104da11606587d68b2910a7a800bf54bfcbaf5197f7f2d62f74820e1f8c77`  
		Last Modified: Tue, 12 Mar 2024 10:19:25 GMT  
		Size: 62.1 MB (62086381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5fd4e15c77fb30117aa9aeb1775213e62178ed479256c336ff39bc94c939b3`  
		Last Modified: Tue, 12 Mar 2024 20:13:13 GMT  
		Size: 7.2 MB (7213407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bc237771b9622278707db0d8678d4c9e3be13e30fc29a3c41c3b7fd915bb645f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bf95033a8c7e89cfdddff6262fe91a0f6c4023f60b7fe60851bb8b5b4e8729`

```dockerfile
```

-	Layers:
	-	`sha256:c38c9b4249466ff9b9f7f4e0f1a81dcb43c9260332ffa2bc9f2e7f59b26e0c3a`  
		Last Modified: Tue, 12 Mar 2024 20:13:13 GMT  
		Size: 3.7 MB (3689826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:519f9a716b087cec4658e9b3d9fb04b283a614c8de1d5405115ef58ea2757211`  
		Last Modified: Tue, 12 Mar 2024 20:13:12 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:7782df76bac02846c42bca8026ac6d9e02ab10294fe069ed19f2da70543de00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115921723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630f38e300e0a1a89b366746565d8e2223e4cafffe3c45f21c0546be908675ba`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=26.2.3 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=26.2.3
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7a79e7955890b06572dbb3c3460771a71f729c15bc6ced018916a432669fd239" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b2ec45db473956d3cc3d8763e4e5c74eb324b155714ff4c78f490d3770310`  
		Last Modified: Tue, 12 Mar 2024 04:08:07 GMT  
		Size: 60.8 MB (60793097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179decee6aafb8d6abaf554a1df18a6897f8692863fcd9479156958da08aa2e3`  
		Last Modified: Tue, 12 Mar 2024 23:00:52 GMT  
		Size: 7.2 MB (7211928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3834f04cceb574aa65c1f38a3f94996a9d8fb2b9d1c3cf56c43ec03a73307e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaa58320f2bbe0e18c76581f3e13c1517572801fbce1cc82b94b2e8c35bb84b`

```dockerfile
```

-	Layers:
	-	`sha256:afb1f7a5a62252bdd2cb2f961f4abf009af3278794c2b1e8a25e0c2e71c5baa1`  
		Last Modified: Tue, 12 Mar 2024 23:00:51 GMT  
		Size: 3.7 MB (3685284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8f8b96e5a02fdf47119e3b8798466be995b2011f48e6a331d790ff69f8ddc9`  
		Last Modified: Tue, 12 Mar 2024 23:00:51 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.in-toto+json
