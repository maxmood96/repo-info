## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:c01000ce75c76165be19ea3196cb6253bd339f21af488a5466cfbe55c627c7ff
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
$ docker pull elixir@sha256:70af74fca9c75b492a8a61102ce4919209c79b2d0b5410de4dabb15768d5517e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128329825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9860c863aa5124fa0d8a9e74dd458bc9bac6aa2e017c77b3f2a6d33120b75425`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d41a7b33f95aa5fa2c24dba0ce0c62854b553df45e0520571e2bc29807e9cc`  
		Last Modified: Tue, 14 May 2024 05:16:46 GMT  
		Size: 65.9 MB (65915525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02b0d8e641b4db35a21c9ff1c30170a778badb64b66335154a0aa8c396ef7b0`  
		Last Modified: Tue, 14 May 2024 05:57:00 GMT  
		Size: 7.3 MB (7314901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6d42dabbfdedcc6b4b3cad97c779cfb8e0c33b787d761f41367f1d0d567dfae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c61133741e2a5364d6fb7678deac9ce5eceb64b200c3eb01067ee039c38bf3`

```dockerfile
```

-	Layers:
	-	`sha256:ab3117c6885fcebd5d6ed43e921c077ea35bf3aa4bf8e9c734f0d84ec830a37d`  
		Last Modified: Tue, 14 May 2024 05:57:00 GMT  
		Size: 4.0 MB (3958655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbedaba80ea2ce5722ab789b64118fd026b7f923f4170af7034b408fd0bc5e5`  
		Last Modified: Tue, 14 May 2024 05:57:00 GMT  
		Size: 9.8 KB (9849 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f0541d3b9a1b34edb7b2f4ee3d27b62097628eebe7b3082baa07d4c31de0a584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114782467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aac4e9a739ea4132a73f7bfcf23da33ddba1d0df1363a1075eab5b739fdff48`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291d14f5f6035886602e7ff10c081ab9faed380a5aabd0d9ec37fed94703fa7`  
		Last Modified: Tue, 14 May 2024 03:54:10 GMT  
		Size: 57.2 MB (57211501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fd19aca117b594a73093230dc871fa1337ba9f7a6776d8dca081a249a3bc72`  
		Last Modified: Tue, 14 May 2024 21:30:22 GMT  
		Size: 7.3 MB (7314521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:4d46b5b4e9bb34d65a05586858ee8e7498987a3745de73799fd7c038d1bca7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5cb51c2cae191db8e439e79611675e8c3750653c382fcd3e7b2f22dc269110`

```dockerfile
```

-	Layers:
	-	`sha256:c3f34b50bd493091f6d3cfbee5ea59f858db282b82b4744be651e14b88f94d8b`  
		Last Modified: Tue, 14 May 2024 21:30:21 GMT  
		Size: 4.0 MB (3960246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa94348396c1aeda9171fb8fab74e03dd38c5a9eb78e10862892be066091d91a`  
		Last Modified: Tue, 14 May 2024 21:30:21 GMT  
		Size: 9.9 KB (9911 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:8ecab8426f998c65daa6a12de6a8f182b82cc79f4fa31d799d5de2daf939ccfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125339413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9497e89937b332510a4a73ab0628ab94da479b25d2a6e6537f8c9194dd5a79db`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bb0d2c1fcfde8a4caefe938b4eed171a92ada4390ecf1a9783b5060134eb91`  
		Last Modified: Tue, 14 May 2024 09:06:09 GMT  
		Size: 64.3 MB (64285765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a3743d1df58f28e267146cca96d68e4eea6fdaf638bab3e42ae19c191ebb74`  
		Last Modified: Wed, 15 May 2024 01:36:54 GMT  
		Size: 7.3 MB (7314658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6d2e111a3bb10c5ba244b71de7b135c092df7df4a98900ceea26fa205e0c27b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599cfac1479df4ac99dcc5ffa80f35a57a4e919fcd28ed3c500f60e177ff43ab`

```dockerfile
```

-	Layers:
	-	`sha256:b5d204cce72cac2e62363e3c235de31578bcb0bffc799205a201d81286397ef4`  
		Last Modified: Wed, 15 May 2024 01:36:54 GMT  
		Size: 4.0 MB (3958227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5030758a9772633481223f54194e522c1a3d7a712f76849ee77b0c26fd70f4d5`  
		Last Modified: Wed, 15 May 2024 01:36:53 GMT  
		Size: 9.9 KB (9857 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:f968b11ec1fa141258c2e0fe77eea8214017ced70ec22367c12a9399de828d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120987891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c78a20f889960514c63647c4e30e92442a4dc676299939079c0abfd9029614`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf507c57241f2fcb57f32123657bd9be79f72fe0d86816a6757883f6680315`  
		Last Modified: Tue, 14 May 2024 02:52:48 GMT  
		Size: 57.6 MB (57597205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d0f150c312ead45f547085ba5f4f1dcb66d96a9a6082d293e0133cf7e3302`  
		Last Modified: Tue, 14 May 2024 03:57:30 GMT  
		Size: 7.3 MB (7314629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c3fa09071a9ed8da449cc2e664d24ee4d1d3d6a6f94487844cb2d3aaa86ca676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa62cee5e5f720695dffe4716ca7313cd05d8f38aa13260e805891daaaa47ef1`

```dockerfile
```

-	Layers:
	-	`sha256:2e0163c176624daebba3cd708360143f8ce9e43d0e3e0b7d93568baa1950ac43`  
		Last Modified: Tue, 14 May 2024 03:57:30 GMT  
		Size: 4.0 MB (3955136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ec3ada35d5ed253e2a283df0d9b302d7a868ba4f74769b69e0b64e7e3eed47`  
		Last Modified: Tue, 14 May 2024 03:57:30 GMT  
		Size: 9.8 KB (9825 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:752d90b9dd120a2d306ccb12ec0728a256cf24831ac58d0c955250ac9c0d9267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124810026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f744c02cd3e0f785c0a6e6419363fa2e1baa5712add2934ae589fd5eaf03687e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde96217c534d1bb8d1aa8badffa708f28ed5ba4ca66b7bf1bfcb77820ef8a04`  
		Last Modified: Tue, 14 May 2024 02:09:05 GMT  
		Size: 58.5 MB (58525652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e1a7618ab67953bdbb353835a253cb1f9d679af5445dfaa2b6371767b0f45`  
		Last Modified: Tue, 14 May 2024 17:43:24 GMT  
		Size: 7.3 MB (7314940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:485a6877a80edb5e42fb96d0a69e462ace650604247ac8f14ffbaed8cc8c222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d73dcbdd93f7f46952f93ebb530a735af97a8c0befbf6f679e5df2f53ac2760`

```dockerfile
```

-	Layers:
	-	`sha256:a4de834c5e1f60ae33f3ad797d2719e3a79c832107b4b1586f0c5cfb46ddcf43`  
		Last Modified: Tue, 14 May 2024 17:43:24 GMT  
		Size: 4.0 MB (3962373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fb120141a34422e6d540ac1218e84ffbf06018e6a451781e23c52557ee6fe6`  
		Last Modified: Tue, 14 May 2024 17:43:23 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; s390x

```console
$ docker pull elixir@sha256:747389a3e7e32b6d5105accac036859a3706c447ead6a4305f29404ce32e7494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118767417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1420b7f22a9a1bc5afd64f4bd17580a237d36edf777595d8b5e77328fdcc02b1`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6406c8049c60169b13bfc1acdcc3c24b854d8c3e067922c3c4aa3ced58dd03f`  
		Last Modified: Tue, 14 May 2024 06:25:11 GMT  
		Size: 58.1 MB (58115298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584ad95972d4585b5b841f2914e322fbb4053dba49a526e14647ffb0bc8d18d`  
		Last Modified: Wed, 15 May 2024 01:49:34 GMT  
		Size: 7.3 MB (7314546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8ee9b8535b53371269f87c261f662e9f9b8da7aacf0b578a3ba9cf0c1c546657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edc66824e75fccdc261753e94bec2f4938cf1dc81c22ebf6fc6213c056309d0`

```dockerfile
```

-	Layers:
	-	`sha256:31316440975f8407f36db433c6cdade285aa83e1010e3940c902e9cd86f622a5`  
		Last Modified: Wed, 15 May 2024 01:49:34 GMT  
		Size: 4.0 MB (3958220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa3aef2dfbc41958f6e6cf48b730f749d73125412c142080d85adcd29081ddf`  
		Last Modified: Wed, 15 May 2024 01:49:33 GMT  
		Size: 9.8 KB (9849 bytes)  
		MIME: application/vnd.in-toto+json
