## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:d19ba89ed93c7f5c25707a0a9689468ff9c87ab997a2875e08265025750618e3
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

### `elixir:otp-27-slim` - linux; amd64

```console
$ docker pull elixir@sha256:4c58517d77e3e67ab4bd2f97983bc635346269eb57ddb701b39e3a952b3e7e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133145723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f43b7f1914b8682c1f864cbbbf269450cc575765cabae371edb0e95d6379d51`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:29:46 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:46 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:29:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:46 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:13:31 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:13:31 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:13:31 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9f1d069da1030e3c4353d42b954335629c46effde3c781b52c27b0833eff1`  
		Last Modified: Thu, 28 May 2026 18:30:01 GMT  
		Size: 76.1 MB (76060002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67d16fcf4a45e8e1b9e3fe42e936070f843aebff29fc984f5d35064c4c7b78b`  
		Last Modified: Fri, 05 Jun 2026 17:13:41 GMT  
		Size: 8.6 MB (8590289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5eae196b6cc228f08f04b51409286045415fbe46796863c99404e7aca84159ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ceb8136079e24795f6c2dfb03e4211877f8b9cfa0c8153247dbdf8e925768`

```dockerfile
```

-	Layers:
	-	`sha256:5e7c68d688010d0a83f4cf22636ebb906effbaa54c62420c0537e7b45c78ec45`  
		Last Modified: Fri, 05 Jun 2026 17:13:41 GMT  
		Size: 3.8 MB (3831833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39ba75e21db76c3e73589dcc4ebfa0d36ffec0f1f5b9ab8669343a17ffec069`  
		Last Modified: Fri, 05 Jun 2026 17:13:40 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:908aa27183a644b864d0a303d20692bf28b754b499d71412b225b70aa4bcb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117974782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a50904640818bd5d46848d6063945adf53b3af9455ec9d55c7da99ef19629`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:41 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:41 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:32:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:41 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:14:13 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:14:13 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:14:13 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fbe19eb60c7a12b0895f6b0be3d1779115581fbf02d68938d6bce9a93c8781`  
		Last Modified: Thu, 28 May 2026 18:32:55 GMT  
		Size: 65.2 MB (65175933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c11adcb6f14a323c14c5693f4c88dc9ad8aa99eb83b1d90b24c4eb3e16f12`  
		Last Modified: Fri, 05 Jun 2026 17:14:22 GMT  
		Size: 8.6 MB (8589695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e35f1dcf0ee9d1cc1c2b98519155754d5ab93fbf4dcb7494c7badd21f5d9eb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eba741f3b9f81948576b2f4e8c9f2c7c26aec41347794f641b7987c01109d16`

```dockerfile
```

-	Layers:
	-	`sha256:4713481767f7e7f2c3782e9293763b36cfb0f34db4957a0826eb0fffc3455956`  
		Last Modified: Fri, 05 Jun 2026 17:14:22 GMT  
		Size: 3.8 MB (3834058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ebb3eccdea31bfe984630a96f36a11b419026ba75c4d817eb56987a3046fb10`  
		Last Modified: Fri, 05 Jun 2026 17:14:22 GMT  
		Size: 9.8 KB (9819 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:f83b3fab642786513be10c1adafdd71450805916533bb985ac2da1f73a193e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130773192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cf5b6bf2b30690d32ed061a4241b610e6d88d53bd8929af882cf2f5aaa269b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:29:04 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:04 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:29:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:04 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:13:12 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:13:12 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:13:12 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57c6b0c1acf5ffcc4ce882bd823bc7fcba2a17024ea8fb740899100369c1219`  
		Last Modified: Thu, 28 May 2026 18:29:19 GMT  
		Size: 73.8 MB (73803550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59484ec31ef57b1527e629ef21a77679c74d8ffae209f2cb4c07a9148c0b4674`  
		Last Modified: Fri, 05 Jun 2026 17:13:21 GMT  
		Size: 8.6 MB (8590210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:860530c4679ceba4ab43328b445d8103a9d7665fd16cc5ee46254612cb1cb706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71c124e7de108629cdf5d47540f2e177aab3131d9d35d2c25c6d61f7a07174c`

```dockerfile
```

-	Layers:
	-	`sha256:8b99973ecd6065fa60b1156861504a5735e32899e04bbdc45c98626f1498485e`  
		Last Modified: Fri, 05 Jun 2026 17:13:21 GMT  
		Size: 3.8 MB (3832082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6468a147ae2960094011b26298332b65b2274697be1c6f7b4315641804fa8d7`  
		Last Modified: Fri, 05 Jun 2026 17:13:21 GMT  
		Size: 9.8 KB (9839 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:30772a12a1734197ac453c8751e10a0eb2d94280cf650d6123c0338c4188bbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124291398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35892beb2968211ba3d385b2f012f42fc9fb1ece6312bcb380f87c656678d5a`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:29:39 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:39 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:29:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:39 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:13:46 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:13:46 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:13:46 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec61613931911b7238a2554af00e86c8b2b1e5eeddc646a6400c0b4f906bf0a`  
		Last Modified: Thu, 28 May 2026 18:29:52 GMT  
		Size: 66.2 MB (66218414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defa8951af33d84b9436064234022ea0d7fedcd844f85b657bcdab4e980c690b`  
		Last Modified: Fri, 05 Jun 2026 17:13:54 GMT  
		Size: 8.6 MB (8589864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:60ed15e42e0ce027120671896505f617463d6e1b1449b4c649e5dd879ce1222f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be25820548fba256d68164871991d328e2f93d3ed9fb98bfa657e9d343da0a18`

```dockerfile
```

-	Layers:
	-	`sha256:7c818e856ef1a93b51dbf82bf935e1f68c539780f071a8148c88fd7156c567b3`  
		Last Modified: Fri, 05 Jun 2026 17:13:54 GMT  
		Size: 3.8 MB (3828999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa621dfe75c5ee30d27af74849472f29cce3a469806cda57c5e454e8f2378377`  
		Last Modified: Fri, 05 Jun 2026 17:13:54 GMT  
		Size: 9.7 KB (9718 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:6a0b6ddefcc3b0a53fbbf667bd44c6fabb5bc23be133937808381d1432ab88e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128227004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9d670da6e4cf65c07fc5a5ff46b8f091a77d4c43ac6716d7f8f0f1552649a0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:45:24 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:45:24 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:45:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:45:24 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:20:37 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:20:37 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:20:37 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c0922d06acbf8dd3d27c5f13e8ee219152ad8e0470d50d575bd72330fcfc5e`  
		Last Modified: Thu, 28 May 2026 18:45:54 GMT  
		Size: 67.3 MB (67296521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6f8927c3b95c8d2580cd9af785301c1b38099a453c2a1497f1667b42349150`  
		Last Modified: Fri, 05 Jun 2026 17:20:57 GMT  
		Size: 8.6 MB (8590284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0575aabcce42eafb4f32fa7130f85148bead7370e9e23d5d5504d2a7a841373f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b627df5c8aad3bc6073c28f9e2413047c73e61f87b10d402d480c713de029b7`

```dockerfile
```

-	Layers:
	-	`sha256:d622e451e5b103a7ba1441addec7ccc23c5edbee37d90b8145197e5f809113be`  
		Last Modified: Fri, 05 Jun 2026 17:20:57 GMT  
		Size: 3.8 MB (3836277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fa002ffeff46961f36d37391edda2c26f54eff86f12def6090f0b66b74a7a7`  
		Last Modified: Fri, 05 Jun 2026 17:20:57 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:d228c7cc31b3562842db83ad1117dfbd3435ce43a690726f1ea901cb34a85828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121708951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cbd2a7640a52196a3668d3a0bac22e2e6de4e7bc52eb16e670e49edc24632c`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:46 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:46 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:32:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:46 GMT
CMD ["erl"]
# Fri, 05 Jun 2026 17:14:36 GMT
ENV ELIXIR_VERSION=v1.20.0 LANG=C.UTF-8
# Fri, 05 Jun 2026 17:14:36 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="70f6cb721f238fa5dd33eb29aa5b19e5ccc3807e41cd5f9b65d5c715b669438c" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jun 2026 17:14:36 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3e0ee3c983c5bb9e9abac348836666761b710b7a71a186a41728e27c4b89b8`  
		Last Modified: Thu, 28 May 2026 18:33:08 GMT  
		Size: 66.0 MB (65963582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e568b5814c5ab2671426809ac85bc4c81fd72245124b2d2b719ec9ecd3262fc`  
		Last Modified: Fri, 05 Jun 2026 17:14:50 GMT  
		Size: 8.6 MB (8589780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:aa6f0cd3fccec249f660408c0e8923d861217d2c1fc579fe375d3f585c14e5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4202d3b440cca34e6922be3c4308f3b10301c53b85c8eeda83b9e1893c582408`

```dockerfile
```

-	Layers:
	-	`sha256:554d3cbeaf7deda082fb1897a336764262b20f891c5706c011a101596466ccf8`  
		Last Modified: Fri, 05 Jun 2026 17:14:50 GMT  
		Size: 3.8 MB (3828661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6414e9d330c193058cf9774b46e135b56d89fb02ead9ea469bc46a4c902f202`  
		Last Modified: Fri, 05 Jun 2026 17:14:49 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json
