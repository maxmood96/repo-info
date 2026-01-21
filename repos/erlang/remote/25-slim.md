## `erlang:25-slim`

```console
$ docker pull erlang@sha256:2ec78900fe96fe864811eaf5ac6fa83cd493f26514a240d33a873187e7083839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:7a7c47083898fa1bb4d7156b50ad745c5b46c3cfbf5801f4181f43a2f5fa73e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119712300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266efd2646550c9e6a1db9f0a791f4b8812e04920034f2a6ed4d4c07008b13f1`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:26:26 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 13 Jan 2026 02:26:26 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 13 Jan 2026 02:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:26:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f377165768041a8837702878691882358901aae25f28a4ef80a39764b9ddb778`  
		Last Modified: Tue, 13 Jan 2026 02:26:42 GMT  
		Size: 66.0 MB (65955854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:238dbe6ad0e67169731620bf25b147d8192a3d8ca73452c9cc6e13a4ba6a417e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effafb19c1e76db301d04908fba2f5197ba4105a6cbeaab6db858ec439b7165e`

```dockerfile
```

-	Layers:
	-	`sha256:3a929f190f7cce3c5f9e7337476dabdeb0e73133e2e54b63f6721cbfef4c7d43`  
		Last Modified: Tue, 13 Jan 2026 02:26:40 GMT  
		Size: 4.1 MB (4098886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4348a4ef1ff0cc4699790e4c75ed0f6389feddc8972a48aa810763beeceda9c0`  
		Last Modified: Tue, 13 Jan 2026 02:26:40 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:8f17a9ffecdb95fdc7d854fb668ce62d9f71b4ca8e4453ddd562810e5c0f298d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106313801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b606d9375ea0ca7dd42ba0efc8b243d49283213ad816d7c7c978d030cce80c02`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:23:44 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 13 Jan 2026 03:23:44 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 13 Jan 2026 03:23:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:23:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:09 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e581192d407f04fc6ed95b3f98c29fd4679fae10c85072204649ffc4d3f0063`  
		Last Modified: Tue, 13 Jan 2026 03:23:58 GMT  
		Size: 57.3 MB (57267343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:281a220cd026f61c2ad930dc0692a13d680d2b6ebe36813fd44615a1c56b52bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770019c160e1ec7bb5602f2435cb8211e1b06317a1a115adf0624047eee672f`

```dockerfile
```

-	Layers:
	-	`sha256:5c1dda7523f3cb4d365085b41beeac8ba3121e1e17906c32a4f05066c349a811`  
		Last Modified: Tue, 13 Jan 2026 03:23:56 GMT  
		Size: 4.1 MB (4100487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae71f120226b39a9c25f24dd6c2917354ebf5bed63cea210f9804940073afd9`  
		Last Modified: Tue, 13 Jan 2026 05:47:33 GMT  
		Size: 13.6 KB (13647 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f3bb16b4a5f5e2a13af840c74b842252cef436abb0f86138b1d7d338493673ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116604808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b784a43b379fb4aa06057fa1a5a354d59c6f6f163f4236454547eadacef583a5`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:31:05 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 13 Jan 2026 02:31:05 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 13 Jan 2026 02:31:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e4259e8e51fb67937ba375250e632114077faf54476931a1adc8a2aef693c`  
		Last Modified: Tue, 13 Jan 2026 02:31:25 GMT  
		Size: 64.3 MB (64347039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:21b2a8f8bff25048beb6e5d521bb37594bf297598a4606fd543b76c5d109cf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52973d203d1d50330c115d11f07f5c4eab46ea19856b056b023041a7bf527fb0`

```dockerfile
```

-	Layers:
	-	`sha256:0a48f57228d935c4a7f723dc9d1145a820a6d043c5439b8fabcf468c617d76c4`  
		Last Modified: Tue, 13 Jan 2026 02:31:23 GMT  
		Size: 4.1 MB (4098507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a92f380718844a4e43b385f4f4b029ae59e6f3798d09460e82717a4b51ddc1`  
		Last Modified: Tue, 13 Jan 2026 02:31:23 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:02fa2c6b3601be93674d94d558c79fbd45c77501576608246ed13549d7af2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112337789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52753fdadc088025fac23c89731dfa777c9cbef636c8fa4c20665442b39a9469`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:09:36 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 13 Jan 2026 02:09:36 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 13 Jan 2026 02:09:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:09:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8309da1fa80f02e5255bda277a4453210882bec6c8459ec8b64c3bbe513d3962`  
		Last Modified: Tue, 13 Jan 2026 02:10:00 GMT  
		Size: 57.6 MB (57638151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1670aaf0f337ee24fb495802adbc165876b6b8cb43fd3c34a79b462a0f62c17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472f6169e610fe2eae0bfde723782ec4c64f8d2550a4b45093170084782fa489`

```dockerfile
```

-	Layers:
	-	`sha256:96217e95409d041e182d0bfcf0d08edbf652cdb251757169fa1aa843f2dae98f`  
		Last Modified: Tue, 13 Jan 2026 02:09:47 GMT  
		Size: 4.1 MB (4095414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:609c2cbd1f0830796d354c224f475f55e0961051b03b43294ca2670f7a82e4f3`  
		Last Modified: Tue, 13 Jan 2026 02:09:47 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
