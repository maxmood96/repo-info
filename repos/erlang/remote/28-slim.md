## `erlang:28-slim`

```console
$ docker pull erlang@sha256:e70c5412856c57ba99d9de0c6a8f90df9bfa0558f53d6c77d1d64c3daead6f9b
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
$ docker pull erlang@sha256:3227a80ee7c972ba6a772950914866a332bd29ec3024791a7f49971059c86c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128231461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ec923cd9524306bfba4e756c96bcfb8025c01b7b7184de1de82058d93d2a2e`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:48:08 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:48:08 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:48:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:48:08 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0c8d4501fe4bc2a0500adbe00e9509c872fda3e1d2469e0ce0c6d83860c85`  
		Last Modified: Mon, 04 May 2026 20:48:22 GMT  
		Size: 78.9 MB (78929359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0c01cb10da42725b08120be5033a15ae07da1742f4de050fb73c0660b5ebc1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29a06d88d25bbe38fcd80a46b2bbd31e13feb4bb920b402bf8507567a3cb20c`

```dockerfile
```

-	Layers:
	-	`sha256:fc87bbcb030049d0f114360a7a58fb713f066627fdaf609ee39f920ab2b3a229`  
		Last Modified: Mon, 04 May 2026 20:48:21 GMT  
		Size: 3.3 MB (3283896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e617f14301392fda581247dc82d5710f22416387e56e0b9dceb8e78bf7242f`  
		Last Modified: Mon, 04 May 2026 20:48:20 GMT  
		Size: 13.9 KB (13923 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:b5033eb84e7918edebfdb39a60c8b5390bbd13c71c9ecab5ba6c4eb320a95297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116903225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5680990d457e1e6a49f50f593df3e58e5025ef1c8b94235a345d0e10ef615b4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:49:53 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:49:53 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:49:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:49:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2799f947c60703e5c3d3d0e3c3209e630083e906d64832d2399440ad75108367`  
		Last Modified: Mon, 04 May 2026 20:50:07 GMT  
		Size: 69.4 MB (69437119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4a59bb47a84c8502ddee673e91b780c9fc5057042125523f0ca3ee3ec9b365e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a365c66805231db995382e224923dbe438c9905abfcd9490caea1b198f5712a`

```dockerfile
```

-	Layers:
	-	`sha256:a0d2db0f2aed0d3a45e1bc9b3734a7e61a5209445ee9b9352099692e1adbf3d8`  
		Last Modified: Mon, 04 May 2026 20:50:06 GMT  
		Size: 3.3 MB (3286871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0e7d7d6e4ab53b56e5504aafde16f06977c182eb104d9c1c6715e57e876205`  
		Last Modified: Mon, 04 May 2026 20:50:06 GMT  
		Size: 14.0 KB (14011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:66b3f02b3372c8fa0c50db9632e1c64278e0ad26608786fc79ee244f39fb4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114732784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ace50040c238b0adc3976f64c1bf8e0057b00919c7ee721675f9b62c4944924`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:49:42 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:49:42 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:49:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:49:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89495480b0ee61a0030dd6a8c33171b381e7a02b0276fb66ff25b00c74a4fe9d`  
		Last Modified: Mon, 04 May 2026 20:49:55 GMT  
		Size: 69.0 MB (68994591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e90849e80abe7e1902b58c3289a3881bbaecb2807081f42a30061f426b4d09ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e21e603d79747ec6a7aa3b27bca8ec91cc6be030cbfadc15a74b3a9f5ef01f`

```dockerfile
```

-	Layers:
	-	`sha256:61ac792025be944ee3bdbca5cb0a458820ca4e3382c07fca641db8d4c0f3803f`  
		Last Modified: Mon, 04 May 2026 20:49:54 GMT  
		Size: 3.3 MB (3285320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71f47acaf514017d66efb195fd6d3645424cc14d23fc1dcfe10c54cb517945d`  
		Last Modified: Mon, 04 May 2026 20:49:53 GMT  
		Size: 14.0 KB (14011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:d44532d18437afe04a2910b343cf398441ba8db78f42905b70b63e97791e5086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127152851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332ffbd5394a3b8664b2b37041952b535cfbf017903f5b7724c5ef16c18c16f4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:48:40 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:48:40 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:48:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:48:40 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6607047420cf78184ba1c60fb39f1826c9fc63bfde864967dd329040a6a6e33b`  
		Last Modified: Mon, 04 May 2026 20:48:56 GMT  
		Size: 77.5 MB (77483606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9b0084e5c79e93b2d4d0558075f98a75684cd4590366c3d024c6e15d4758e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb68100887f6f0ca844022031775e5ee3db0a669f47f90ffa18ba9ed98e119c`

```dockerfile
```

-	Layers:
	-	`sha256:9128c5daa715ef91347f6920497a68b19d12a2bdb354386686a12d75716c672f`  
		Last Modified: Mon, 04 May 2026 20:48:54 GMT  
		Size: 3.3 MB (3285431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebf4d6049dcd2e7f9fd19bfea96b96004597f711e5790c72dccbdf685929ce1`  
		Last Modified: Mon, 04 May 2026 20:48:53 GMT  
		Size: 14.0 KB (14039 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:e51df8ad9e83a95f8b8c8f2df239e428f0e5279e711a2102b55b71602f2b483a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120234307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cc12fe99b56b710a1a7febee285ef702b18d18fea5f22be6c3044afd7b9206`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:00 GMT
ENV OTP_VERSION=28.4.2 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 01:45:00 GMT
LABEL org.opencontainers.image.version=28.4.2
# Wed, 22 Apr 2026 01:45:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0c44346dd939f9d264860e5bdf4df8cd35e165b628a838d5d104c3b4cf65b9b0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:45:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67855b9231bbb26bda174f3e4f4d9718b4a1296371affcc92c51d3d7b7c5230`  
		Last Modified: Wed, 22 Apr 2026 01:45:13 GMT  
		Size: 69.4 MB (69408950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:44ac9b37fcb4bdfface0b763ea626adb6cf802379e30cc85163fddcd53cec9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e03542002526631ddbb07b174a28f4b42e2c48b63b426935680e9afca1828f5`

```dockerfile
```

-	Layers:
	-	`sha256:ab7e8a7ef8ff5be2079b17a156f6faf6866731e9344d00e3ae4b1e089b7ebb11`  
		Last Modified: Wed, 22 Apr 2026 01:45:11 GMT  
		Size: 3.3 MB (3281094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354940a04b9c63acfd057ee4420844f8f58cfce91200ca32f2a94d39eb837220`  
		Last Modified: Wed, 22 Apr 2026 01:45:11 GMT  
		Size: 13.9 KB (13892 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:92227e3d30039d35098bc61642ccea808196901bb351083fbba0f55fc071d40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123503178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2f049cecf7666802d2bf9219c746d373477d8337abb00b460c1489a5e22b7c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:49:26 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:49:26 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:49:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:49:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c4dde571eac5e562d79b5de2da23b06038ead0668226ce6295016681e4f50e`  
		Last Modified: Mon, 04 May 2026 20:49:59 GMT  
		Size: 70.4 MB (70380194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e1ac01c7dbae62db317e89499407d2fff7e48b018e90490845c6592b7063f9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d075e374f4a91143f63d112b59d0a60171f40f103f82ed1e8b36add0e3d9b4d4`

```dockerfile
```

-	Layers:
	-	`sha256:10c3fdc2330294e61d19707511c0e9ad75e4225f5b9d6439594c759a4387adcc`  
		Last Modified: Mon, 04 May 2026 20:49:52 GMT  
		Size: 3.3 MB (3287487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421347f247895233e175832cb4a3f46e02c5d1c18bb90f9e773d9ace6b1caa58`  
		Last Modified: Mon, 04 May 2026 20:49:52 GMT  
		Size: 14.0 KB (13973 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:ed761f868d43fe3cf8e6417301b15854230a93d80b05a2f324b4d1fa0cdfede9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119640640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766af15b02b1870b146123b3dd875c4fac3c9e08d8c9cf583f2da6312919a47a`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Mon, 04 May 2026 20:50:17 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Mon, 04 May 2026 20:50:17 GMT
LABEL org.opencontainers.image.version=28.5
# Mon, 04 May 2026 20:50:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:50:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c93b7ac0c4a0936bdf47246e49ed428af22548935fe6010cbeeed64566be0b`  
		Last Modified: Mon, 04 May 2026 20:50:38 GMT  
		Size: 70.3 MB (70268534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:27a7cefbf2fbfc6a60d25cf61d243aa85f6eb7736d5c1cb00ab8322c4d501d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f891ae5c6dc7d7daa70ede76dd91f672a905c72afeeb5dc7f49932a40f685283`

```dockerfile
```

-	Layers:
	-	`sha256:d5c346b65e566a9a548e991838dab4d54fd16db7b4e3cf5939ae63f037350e09`  
		Last Modified: Mon, 04 May 2026 20:50:37 GMT  
		Size: 3.3 MB (3285337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba658b28b12320f4d594a72cf154904fb909908dba8017151206b938877eb94`  
		Last Modified: Mon, 04 May 2026 20:50:36 GMT  
		Size: 13.9 KB (13923 bytes)  
		MIME: application/vnd.in-toto+json
