## `erlang:28-slim`

```console
$ docker pull erlang@sha256:9d90bc7a8184998e0282786c6668fc4f706232ba68afcc454a5c8e27774075c1
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

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:606082c32a8ebb27912c9b5f919ba181583ba2f30eda1f096cef3ebe3d075da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128845118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df352f7684c5a0497f26dc60c4245dc4daf67cb795ad49cad35f1250f826ffb2`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534c76121e942938b5f04a344713ab8b847d656ac63b15d36e372c98b4df0450`  
		Last Modified: Tue, 12 Aug 2025 21:26:21 GMT  
		Size: 80.4 MB (80350607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c214bcd1e52842787d113f7a7cf5d766d777cf6b8a9762ce8a47db9c91c5eb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940681e5bbb6ff30c47fb0ba02a0c12fad245777123464d767d4df394ea0d7cc`

```dockerfile
```

-	Layers:
	-	`sha256:e1a9bec7b8e1ff70350f9eb40266489bb3ad6a28d26ecd32ca6f06a1af721f4b`  
		Last Modified: Tue, 12 Aug 2025 22:47:50 GMT  
		Size: 3.8 MB (3817639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f939f1c66abe8a33f5a9a6b73b660d192af42ccf15591d3c9c8a1892443520`  
		Last Modified: Tue, 12 Aug 2025 22:47:51 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5e61d86945a1184fba28a1113ba1c2d6fb3ea7159499fe81db21f5f119f3f809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116048556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d202f11b1b3bc0e539bea06e3fe0a452a74780c838204d607f3d89bd4fabba17`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ea0d25317149dd26fe3fc21f7a1766f8528af12760c2aee4e2fa23834000897f`  
		Last Modified: Tue, 12 Aug 2025 20:44:49 GMT  
		Size: 46.0 MB (46027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbae4565d564c76e5969f2fe1cab775c46cb6b91f4747c4f0cf0d858d09b6679`  
		Last Modified: Wed, 13 Aug 2025 00:05:00 GMT  
		Size: 70.0 MB (70021321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2111cabb3480ae026ec2fb2c3b9e2bd476f82778f193a92d29c213f013173615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e1b4fa518311c8b0506c94c3d3a83dae9ab84853dbabcfafde26cecaf49a79`

```dockerfile
```

-	Layers:
	-	`sha256:e413e8a131034736fa368602cfa96256ef13e7adcc4185453ce9403be167ce1a`  
		Last Modified: Wed, 13 Aug 2025 01:48:36 GMT  
		Size: 3.8 MB (3821455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d63dac6075100799af5f6481383d744ed53a6269fbf620fc3947b09b493ff1d`  
		Last Modified: Wed, 13 Aug 2025 01:48:37 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d53ec3b095f6065e2c7d8388689a826385ff1511d12a33df726be11f917bcfe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113640009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3772940d5c76968259907d6f21d6beedc289cc11d191ffc408960ffaace5fc`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf595842a8587bed7509f798d769106f6804c44293e2bc6f029ce28adad3eb9d`  
		Last Modified: Wed, 13 Aug 2025 00:24:40 GMT  
		Size: 69.4 MB (69430965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d37341cc71a9c89bb01f574a77a21364dca70bfcb8974c9eca0f003eb985ff5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502dd6430941e98881b94d580452bc5189c9e412b9d7e5362c385564ea20facb`

```dockerfile
```

-	Layers:
	-	`sha256:3a9dae7b70bb6e5ad8496f2c58c3321d53815d5538449bed1d562587c93946e0`  
		Last Modified: Wed, 13 Aug 2025 01:48:42 GMT  
		Size: 3.8 MB (3819880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ec587486fa236730dfa2fc317c3641315924796ca857b892b6f6a90023f320`  
		Last Modified: Wed, 13 Aug 2025 01:48:43 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b3b6232ffdd33ec6a9c46797376a3a001b21de9840f0a331b4bc54f21b2ab9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f2faabbd5e7123f29597c85740f66e2411294c8d1e202eca8591d420f6d391`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abc0429261fc959dcea40a792e6e38f1f2dff843641eab6664ce79958497bcb`  
		Last Modified: Wed, 13 Aug 2025 08:25:09 GMT  
		Size: 78.1 MB (78146707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7dd504cf0b7cae0220aa6c9172572a11cff5747aa4beae6b2e116f85d3132ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b377e7e37ef499cfb1d794f105d1238eda297de93488f36731f055f2398b862`

```dockerfile
```

-	Layers:
	-	`sha256:13706aa6cec2a5fcb2d5522fc10ea5ff5dcf3dd5c110ba1375d8c9a5a710948d`  
		Last Modified: Wed, 13 Aug 2025 07:47:30 GMT  
		Size: 3.8 MB (3817912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785491a80797423d632e2fa5253cb3a3caa9c040d1535b73405d60cb94364a62`  
		Last Modified: Wed, 13 Aug 2025 07:47:30 GMT  
		Size: 14.1 KB (14083 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:5e78bfd311fa8e71c7e207896a06d30fb4b45b110aecb4884b2dcc261a513651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120029976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6528be88ae7809bd90bb891be872d4526b28b8110d61c74ac8b02202da6eb1b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cc486cd45801e9ad3099ac5c018c5d91a2b6eaa7b0a1cc191192a6b328497`  
		Last Modified: Tue, 12 Aug 2025 21:23:50 GMT  
		Size: 70.6 MB (70551861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3208ca0ad6ce6e81c7df80db5091b9f56644ea442dce4ceb51a868e08d6bb65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1bb43d31affbfe885fe5c0c96dc89a3a4efaf5efccb5bde6608a69f953cded`

```dockerfile
```

-	Layers:
	-	`sha256:026d1a1ca7b4ee2d55d20b3017938bcc4af7255ef5ff615ae228c1e90d1de239`  
		Last Modified: Tue, 12 Aug 2025 22:48:08 GMT  
		Size: 3.8 MB (3814801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f616efddf0626649e214b6689a9497379fe6862b8d942026223d29c4b4e54450`  
		Last Modified: Tue, 12 Aug 2025 22:48:09 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:8fee4941a0671ec25a4f41a6138aebca9138b478f3db50019b87d3a8f4def4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119265197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55214b886845052c14b627f82059d20a3fb09bc26a8e4160398b04f01b4f63c0`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28468c06ffa3d40773fe289dc95c153eca236372a993bb02666d7eb01f952de8`  
		Last Modified: Wed, 13 Aug 2025 06:53:48 GMT  
		Size: 70.5 MB (70488540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:81521391ed3875925443c40ce58ebd1e16149eedf6b35adf10c7ab4a16589f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8f8acb0c1a8914492bf9f427657584f3d8f840a86cf2d265d6a69b6c94d38c`

```dockerfile
```

-	Layers:
	-	`sha256:94644767f71517e1833da95c166821f2c83bcdc6cd4442b8f1f82672387fa148`  
		Last Modified: Wed, 13 Aug 2025 07:47:37 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:e6214627bb59088fac5d9ee20c3f8a0ea396eaf1a3a0643146344081bca0a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123908344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5613f507bb751791b09ada676fc021f4865dd5f138651322ef88386d319b9bf`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31502fd9d4e353d2e19776c57f1472ba13088a583d66273c6f6e88f8377f313`  
		Last Modified: Wed, 13 Aug 2025 12:39:30 GMT  
		Size: 71.6 MB (71570267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9468a8b641b69108d78fe4148caf5aa9b78fe9d69752bba2f507a124428aa7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787e66ffa1170ebe25a7384627175b4e62392dc541296799dbc441bdea6d33c`

```dockerfile
```

-	Layers:
	-	`sha256:e52ec31c5cb08ee487944a033133b731ad5d57078f4a531d7157b9870453db62`  
		Last Modified: Wed, 13 Aug 2025 13:48:03 GMT  
		Size: 3.8 MB (3822083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb12373d9e5324608319eabdebbfa9ca905b55b65a25fb948243b26153646ac1`  
		Last Modified: Wed, 13 Aug 2025 13:48:04 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:01ff5c170fb6ed69f6be68c1364161eb9a0303c1077920561f78d2860991b628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117338238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57955db90b5dbce9c62c8ab60014f931aadc11326b26d93c8840d91319233666`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2196f4fd88daab4098de366486a81c0f517a31834d3d4b8c0dfe14e35ad65dd`  
		Last Modified: Wed, 13 Aug 2025 03:30:04 GMT  
		Size: 70.2 MB (70188372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fd785e4c6446d055d85d2067187137960e4f70c7eb48bf3178571d0e5de747fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4790749f1a87f0ae8bc396ca307bb3cac245eac2d8454f9cfe9d0999b5dc9e07`

```dockerfile
```

-	Layers:
	-	`sha256:1b2299ce64ca2fe762a738435ce15bae95503391d440f010cf08e28c75d0c3ec`  
		Last Modified: Wed, 13 Aug 2025 04:47:44 GMT  
		Size: 3.8 MB (3814467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68165870491884261a7b2cae2b10732d1632fd99b548728a2f4eb7c742338f3a`  
		Last Modified: Wed, 13 Aug 2025 04:47:44 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json
