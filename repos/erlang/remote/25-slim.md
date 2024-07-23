## `erlang:25-slim`

```console
$ docker pull erlang@sha256:0fd1cfc44fb3f5d3b3ea0b6095b0356a59d7acc442ba63475e35030a6d437e73
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

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:7f0bd3c3d5b6dd8b5cb83998760243d32a248d1a551156ad6173153f636be44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120996620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0059b430b6a9d0cfbda365b179dc1d4530fd65b99502f09ab903e8d9c5b4bb28`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a41f38fd084b10666afb65fc0eadbeef352dba814bf6352f6913fd13ae41a`  
		Last Modified: Tue, 23 Jul 2024 07:25:50 GMT  
		Size: 65.9 MB (65912042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:14efad38d20c7ac3a8cb71986458b808fa34cad30c25ad0d693aaa880de38c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af47adcfaa916d124fdc6909a8d5a42eb50210b844279475da768a635bb2d44c`

```dockerfile
```

-	Layers:
	-	`sha256:0df0690790d5baa89e3537d53fddc186602d3e9c7356c92000aaa932b5c0fb90`  
		Last Modified: Tue, 23 Jul 2024 07:25:48 GMT  
		Size: 4.0 MB (3979776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0abbe4cb54a321d74a7c3a8d18e372c67ea74018362b4ffc7699e0829151e3`  
		Last Modified: Tue, 23 Jul 2024 07:25:48 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:b84947807e26e86260af2687c2fb8088a4b919dcca6cdd5ec343d5de17a5da75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82a425eed839fbbac33e968058d54cee02a135fcc67d5d7973b5cd9a7b72991`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
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
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63225d9b1f69f68392665357339553b5f16a0ce765202b51e2df1266194f5390`  
		Last Modified: Tue, 23 Jul 2024 07:33:52 GMT  
		Size: 57.4 MB (57407782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f9957180b3bd0c058cc27a49d4e8e0ee5031f3f2343e2caaaea181bbd83e1f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635447880ddf4e3ba9c4d4a53c84bed0d1cb2db9d8691fdbd0280bc60e07419`

```dockerfile
```

-	Layers:
	-	`sha256:bb3ce555d99f3cfd5ed1eabd0b282d005fc39d2227725e074750bf7b12c1ab98`  
		Last Modified: Tue, 23 Jul 2024 07:33:51 GMT  
		Size: 4.0 MB (3979377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a3d869da200e26f7feaa23249b31f791a69a8b1249ad0deac88b7d46488ce2`  
		Last Modified: Tue, 23 Jul 2024 07:33:50 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:7b8ed8f682f9d41ef2c26afdb2699f04c092757f7b308022808113d5353f0738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107447427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bb7bbe56d79bb22aca9a287e08c4771d5119408dbcd0be140edf02f77e2c14`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
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
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a993de80c0d7e8b13e612e48ef795d5f4e38f4ae31438578f6f8b26cebce6a`  
		Last Modified: Tue, 02 Jul 2024 07:37:19 GMT  
		Size: 57.2 MB (57208429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3183352221b7bcc0b194173faf112136d7739d5a4fe8d043be365d14076aee03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadd54cd78f1a32c7e7ea2d3adbed33fc1be179e1d6ec6e77a9952fa026437f1`

```dockerfile
```

-	Layers:
	-	`sha256:b027c661a294878fbdf5d3dbb9b6ecf5865ff9e6cc548ffdaceee23ec189e681`  
		Last Modified: Tue, 02 Jul 2024 07:37:18 GMT  
		Size: 4.0 MB (3955407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02811aba0730611c76e4e7b8e7df7eef8b120e9c69812a0a51e4e563b5598e66`  
		Last Modified: Tue, 02 Jul 2024 07:37:17 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:366cfcb355a9a8dac18cb2ccfd787db7365b17634d0c0f408badbe502a51f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118002702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84de6e70c94caab592c3f87fd26fe887401407b7bb503202c99b36ce6607239f`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb98da49b6313952497a296b33b78c75c6db73c2156126fd40bea9e10c80860`  
		Last Modified: Tue, 02 Jul 2024 11:04:38 GMT  
		Size: 64.3 MB (64281049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:270496c74603080b37c0f363af69354c201e0259ac555c39c3f0cae12c461b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6583ec12f1c306e655045066b71a6a6a5194bf378932828167bb1ce63f81be82`

```dockerfile
```

-	Layers:
	-	`sha256:7632cd5645e3907059dce139af09b4abd672482cd2951f5cd3f09c454d77e797`  
		Last Modified: Tue, 02 Jul 2024 11:04:37 GMT  
		Size: 4.0 MB (3953427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2513dedd71f7434644b25d49c02ccb1b86bc0a6f01e92853d70929546f63af79`  
		Last Modified: Tue, 02 Jul 2024 11:04:37 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:2d0cb8850c08d7d33a734cc9fc760890fcea1c35e83272ba200a4ced867b2263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113667506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92bc0582234305d5a89c6e7fd464941766e4afe32608c3548d54fc83e113927`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
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
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73811d75b41b476145e8a92241e0eed4c239b8318783ec89924bd10d058c8a92`  
		Last Modified: Tue, 23 Jul 2024 06:20:27 GMT  
		Size: 57.6 MB (57593336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5f346cd5146258da4b0dad38cdd72a20a63b87c203c71895295e448f9ee0642f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5849ba4bedba47be680571524b6ea985dbe1f47dbc7af9bba1806f5f5f23d7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ce8baf886a20eb52f25c660ccf50375b7ea2706bd37f56ac0be75714543d1725`  
		Last Modified: Tue, 23 Jul 2024 06:20:26 GMT  
		Size: 4.0 MB (3976252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf785405404a72f76f4d54c6d941252036c2f2da12e561c787fc142b4a13520a`  
		Last Modified: Tue, 23 Jul 2024 06:20:25 GMT  
		Size: 13.3 KB (13349 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:7788bdba049927724ba375c34164c6da36e29b064048c7cbebd7fd21e1c6f969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111520931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee51ab3234a25971fbf6d1fe99de18128bc373376a4daa464b6e9ec272bee1`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
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
```

-	Layers:
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6176adc73036f33418157662b9dfe549b92ba9873c135923e491eb714e69fcf5`  
		Last Modified: Tue, 02 Jul 2024 20:59:41 GMT  
		Size: 58.2 MB (58214727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b962e973c4ba0312399cf19efdeded6d6b924d32aae057ebd6b3ffe6fd2ffb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a5005f228a90083468b7382f0593b8e80833686c8d8a6bc0c60e32b330d6fc`

```dockerfile
```

-	Layers:
	-	`sha256:da03608db6b64ec13db8d476c20d03730246d5e8280ae5227938ad6bbf7a5a76`  
		Last Modified: Tue, 02 Jul 2024 20:59:35 GMT  
		Size: 13.2 KB (13214 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:dc9649cc78b37c2c9ed6032b41f45c5b4ef7a25c06bc653aea38c5152406137b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117472785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a43e7cfc99d652d8044fc52234ca2afbc4cd72d36be4a9d2f64921dd8bb7440`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
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
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b58e9bc359713f6ad5805f464d64453c066ab915634ecb6e3640c22a604b7`  
		Last Modified: Tue, 02 Jul 2024 08:04:09 GMT  
		Size: 58.5 MB (58522388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:96d274bd83d5cf2bfd8b49ff12248f55aabd660afa2e89fff512ca4f8fe0717f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d8faf73763f5af6c8a39917610505ac6ca88699799f226093bb137d49848ca`

```dockerfile
```

-	Layers:
	-	`sha256:b5970a3943e4e62b49f2cc1191eba719b6de4fe297241a3b19354af1eaa9206f`  
		Last Modified: Tue, 02 Jul 2024 08:04:07 GMT  
		Size: 4.0 MB (3957532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cb8f10406b912cfaa6b23f53bfc4dd1fdafff12c380abb4245105193a77e2f`  
		Last Modified: Tue, 02 Jul 2024 08:04:07 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; s390x

```console
$ docker pull erlang@sha256:18dd8d3874bc94b779e90261c1e71a072d0cb530fcaed1f56494de92a79a98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111437751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e25df22c9b191241f98b599d494e839794b3d209a938d27feb70c051b0864f`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
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
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4434298328290e12d1967b8242d983601676b8b3bc22b4376fee07ce39bfa3bf`  
		Last Modified: Tue, 23 Jul 2024 09:59:06 GMT  
		Size: 58.1 MB (58113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:55cb799fdca4494353264afe94c7fe86c3cb55bd95e59ccfc2eed0d946630ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caa8ce77c8e05f5ab32566226374696fe6dd1ac2c608b4c3938952fce885e76`

```dockerfile
```

-	Layers:
	-	`sha256:1acb2c135848f70426065febffb0f158e0d3f10f1983d384d13148c9c1876d2d`  
		Last Modified: Tue, 23 Jul 2024 09:59:05 GMT  
		Size: 4.0 MB (3979341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160b552fb34535f3bfecd75d0c9c9ddf7ed13933faed335e8d34349e4254a037`  
		Last Modified: Tue, 23 Jul 2024 09:59:05 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json
