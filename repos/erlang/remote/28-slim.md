## `erlang:28-slim`

```console
$ docker pull erlang@sha256:4353a1c7f0dfe7a9ff5a9d681be873658a883e3caeb8f50a2cd881ceb7808e43
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
$ docker pull erlang@sha256:dbc167d1208b0726c99e7758a3e2616fe53783a064c279abf717e0853cec9357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127845605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389242f75bda5917e4c731231aa7465924de7129be5830c55f31a97f49554ef7`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348c296f60e15fe8993ba1f6ea84763459186a7e7d5974896578f30800b0519`  
		Last Modified: Wed, 21 May 2025 23:24:09 GMT  
		Size: 79.4 MB (79357360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:68b5f945c78055ae82accb1ee29174a3d87458e2d544521d3b7405b3a9870d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c68cf50e900aa286e36babf27865e1e2b28458ccf59a5eff77b43fb893dd9b`

```dockerfile
```

-	Layers:
	-	`sha256:d3873416d6b18893c376cfda8277dfca8c37e62cf01d4f602d5ca187a997549d`  
		Last Modified: Wed, 21 May 2025 23:24:08 GMT  
		Size: 3.7 MB (3726315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58a01e9f793cf4cdcf541d96b14812aa175de20aa14d9d683bd71828ddf78e8`  
		Last Modified: Wed, 21 May 2025 23:24:08 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:97b8b2db8b9eb11686e65872e542ebc24f95946f7c429c825b8c4130f844d478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115114236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b84483b0430bea5aaaff98c7800c4e533abe37c032936b62d33c4f2d105a39`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bfcf93e96abe0bc43e9897561aac7ca6bb8e2ab871392b4b2e8f70247f0671`  
		Last Modified: Thu, 22 May 2025 01:18:27 GMT  
		Size: 69.1 MB (69092752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d7b2e3508668325b4737b2f09524649f725f679e70b5a29a04d971b6e5f85cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f0804a0d73e1207da754073290c028b7d7f10516cdbd0ddc578a9393572764`

```dockerfile
```

-	Layers:
	-	`sha256:49df7b0e072da37f4f9560e6810cb6c7192886b81384c06863391e4c309f8abd`  
		Last Modified: Thu, 22 May 2025 01:18:24 GMT  
		Size: 3.7 MB (3730123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096166f43ffd2f94b3cfc4ad299f976f1657acce4e7ec23da4fa436487f1ae79`  
		Last Modified: Thu, 22 May 2025 01:18:24 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:8bf6a1e45b02c73911962440301bf597e180c1641666f91bf625a46176f27fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112711676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e96718139a1c6646f27a39ad7443974048064ab725bd5e37c4f8d9cda14ec05`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cca733f35d6bf2c03a292f475afc58405dc1b7cc09ca87a680628f979e36b2b`  
		Last Modified: Thu, 22 May 2025 02:41:00 GMT  
		Size: 68.5 MB (68508905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:59e28a5ff06dc8828af41c436f38fa0dd24fe6618799c6b93a1304120b04b380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b4e7fe64179df00d807d3c4724cb94de50fda6f453c8a1d6939ceea01c3e24`

```dockerfile
```

-	Layers:
	-	`sha256:9f2d405812ee696348c3eea943eafec619e86dcfd01716137d576775276206c2`  
		Last Modified: Thu, 22 May 2025 02:40:57 GMT  
		Size: 3.7 MB (3728548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9656d6eabb076e3b7bc4b66c48947c3be41d81bdb6f52cc8f80be232b87ed134`  
		Last Modified: Thu, 22 May 2025 02:40:57 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb0d4da71e5c5689f61df89b353b4b42daae3b14bd8075d47a874139dec0a6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125429493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54aa92bf1d8a3111ee640959be3c2893316155798c1e61b2715a75052e75a472`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337081c3f5c098d551cb77901d10bc5f57e45ad4428d9e609fa5446b94f1b391`  
		Last Modified: Thu, 22 May 2025 02:57:16 GMT  
		Size: 77.1 MB (77102312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6fcffe69365e2e2a7ed0c1c43fb537083ad3054e8f57d0a9be250ec9e05c5f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb70d5209c1f39ad8eb5b092e3014492db653957c6be715c858df4e80ea7bfb`

```dockerfile
```

-	Layers:
	-	`sha256:32375f510bfa90f2c839a46e1d787bd1858d7a67b5453ff883781eb943fd5411`  
		Last Modified: Thu, 22 May 2025 02:57:14 GMT  
		Size: 3.7 MB (3726576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:909567ba7073dfbc6cc23eee8a3f5b60135d1bc5e897dc6ac275537e8399cbfa`  
		Last Modified: Thu, 22 May 2025 02:57:14 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:d8d3aac45b471b2ac7461ddc88731e88e70e1a5589df981485363449bfdff267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118914735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00626961246b673a2d5179ce3fe3547ad7c79bcf3df7509a97082d65eef9e2a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff72156c5fc1f719ba5c8608bf3d836e8e33b14bcfc3db17d60c9da1f4e6464`  
		Last Modified: Wed, 21 May 2025 23:22:49 GMT  
		Size: 69.4 MB (69443173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eaa68b8c1657de9add59254cc9dc5c63d5fe7125fb7dca181b334f3aee5e9bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d340d5519400c829d83df5321672f5aa5b2bea6ecbd697a4b170858b27b4cb`

```dockerfile
```

-	Layers:
	-	`sha256:facdd222fc01a35abbf3fb19d6f0de7f7161a6cf8c0c243818203335fd0ee1be`  
		Last Modified: Wed, 21 May 2025 23:22:47 GMT  
		Size: 3.7 MB (3723482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76165d59004e49ca33117e43b42e11b42f4f25306f5e3d05765c0ab6143f6374`  
		Last Modified: Wed, 21 May 2025 23:22:46 GMT  
		Size: 13.7 KB (13655 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:b7c23fecad327b9b33c64eb268bba805d88bc2948677f1598be24d854a03386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118281416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc800980629833f4aa9b1d9026f82abedc250731b4f74882615d2b59b2889893`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a93b357df7ab2a7dd865fd63e0986fa376ea1fdbbd7155a7e330aa7ddb3ddfb`  
		Last Modified: Tue, 29 Apr 2025 13:00:35 GMT  
		Size: 69.5 MB (69505978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a879f5ebc399a8d201a5a9caff650ce14ea887b2d438d496ed0fd349f3b2acce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57185f6776527e43eb3e9ffdaab1b09c4fc0f423b1e22ad99c45ab80a7b17559`

```dockerfile
```

-	Layers:
	-	`sha256:fbd23ee4df08f2806fee7f64d81929a68c6f39f17124216e613af8b85b5e1bd5`  
		Last Modified: Tue, 29 Apr 2025 13:00:28 GMT  
		Size: 13.5 KB (13538 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:c00f39f249ee80d8ee74f1288c5acd58356be6a590b5ffc12e59f87a7936c2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122965309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b32a578561b75f87b57c94c58b9d6b4720a106201a86ef953db20718a20c09`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0849e7f6c636e8ca7fc6242ab342e6356352e9316a33bb99d896dce1fc9ee06`  
		Last Modified: Tue, 29 Apr 2025 07:52:03 GMT  
		Size: 70.6 MB (70633180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:60d5adff14007cbd419e4b65f938e8d15204a8ff2d3a1dbec8dc67ef9aaa727b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d6288f1dd75b10b341e2cb9c1d97cbb3fbfd19bd23dec4362c14e5485eae47`

```dockerfile
```

-	Layers:
	-	`sha256:890b39812147b0723df054470c5a9f9206b831a58a58a6fdcc7d6e2047cb3ff6`  
		Last Modified: Tue, 29 Apr 2025 07:52:00 GMT  
		Size: 3.7 MB (3713643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f49286511dc2c89ac15a23fb373244d360044f995ccd15577805710a2239fa3c`  
		Last Modified: Tue, 29 Apr 2025 07:52:00 GMT  
		Size: 13.7 KB (13731 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:8d833c2d8ce98827e3fb2d2da056c1b08e212f295309225cf0c64e08259785a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116300274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1042064f10f28dd311a07093c646e3a649015558fc6ccb9a67c81683e2d566`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 19 Mar 2025 13:16:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 19 Mar 2025 13:16:01 GMT
ENV OTP_VERSION=28.0-rc2 REBAR3_VERSION=3.24.0
# Wed, 19 Mar 2025 13:16:01 GMT
LABEL org.opencontainers.image.version=28.0-rc2
# Wed, 19 Mar 2025 13:16:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1933a7811aacecb528e3d05f8e552e15439d733934064c821639fb22735c928d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 13:16:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddad9aaa8df70375ec51ec5247443325087cec2fa12b1934b338b74362896221`  
		Last Modified: Thu, 22 May 2025 01:09:55 GMT  
		Size: 69.2 MB (69156432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2438092017f6e386287c80967a7d80b9aae18348558d40921744af4a91b36631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cf04d6afee7bf2c21069381180c98854e091c658539d5ec5fe1d34d3631a7c`

```dockerfile
```

-	Layers:
	-	`sha256:a7c900be70d30da80a0679ff5ff2f4f47ec76a8500485259d935e50903f12718`  
		Last Modified: Thu, 22 May 2025 01:09:54 GMT  
		Size: 3.7 MB (3726035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58cf3842452e0cd64296f3f565e0a35bc8bb8d86ffc5b205594b49842900c592`  
		Last Modified: Thu, 22 May 2025 01:09:54 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json
