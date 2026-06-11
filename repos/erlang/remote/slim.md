## `erlang:slim`

```console
$ docker pull erlang@sha256:95831811557b4693b3f6cec5719cdcac856c019b86aae9c198cd6cd4e4a8bc20
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

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:7077d1d76f09b7a81d5b0a1d932800c1479aeffd9c77feba1ceda84840b0cd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129592855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a86aea2b2a9d5cc00cea699797f1be9821e437531e162376bc2cb721acb81`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:11 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:45:11 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:45:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1122d8f764bae7a104d6cc60fd4c29e156db4f141f6b866d7378d3f4371d1fd`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 80.3 MB (80275734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:903424b5a7183692b9959fbedede94b3a99157d05dee9e1ba0bdea2dfe7d28e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89228719d9ecb6f3bd5484d44c89787d01e95c2504d665593e2813c3038a8a5e`

```dockerfile
```

-	Layers:
	-	`sha256:550fc83faef0a913e781e56a83d2658d0cf20dc410f8deafc8e30e41ca0d8fb3`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 3.3 MB (3283828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead9fcf7a4655198ae2a1598a2299e3e39a7583ffbf6e23542a7645e9f44e474`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:394c34094137a1e8af12a4993a699090e788c93ceed8a251b852f36feeda4093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117930718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22f81cc411b8803f5a885f8c0681b9b300f3873af886de1e1e48ce7ae431b82`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:58 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 01:23:58 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 01:23:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:23:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba48052a08603857dc4c8d80eb2f415a4f8bcdf613270947283ff4358380c4`  
		Last Modified: Thu, 11 Jun 2026 01:24:12 GMT  
		Size: 70.4 MB (70435907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:509ec5518e72eda387046a3a3e1ea8f0fe90076b5d27318f41cf0bb46c2a72ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55e52d246913d7744c5a79cdef01c3f9e612487b2754bf10d7be7172e5f4f27`

```dockerfile
```

-	Layers:
	-	`sha256:f757e23a66a1f9ed1f486a10e470b8c52abd51f948c1ee10b73195d40d2b9361`  
		Last Modified: Thu, 11 Jun 2026 01:24:11 GMT  
		Size: 3.3 MB (3286803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832887fe9b2ef532757727cf61dbfeb0c367331c8d430f2fe0fd983cf87c58ce`  
		Last Modified: Thu, 11 Jun 2026 01:24:10 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4193e1256a2cedcf46dc6b67a0467a506a5a40baa594f27ece715f87996147b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115755137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9faadaaeead3028be128534ea3cbeae03f99f7b675543eaccf58ada527262a5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:34:19 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 01:34:19 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 01:34:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:34:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d62d08c620d0eec40faf3aac1bc412bda14b15929b15d8ccdaaa313f2bbf59`  
		Last Modified: Thu, 11 Jun 2026 01:34:32 GMT  
		Size: 70.0 MB (70006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6a00323090258d1eab6e4f0c84d124c2c2e7549d7cf65e77aec65cc3ba26f912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac6031b9a4a87849fd295b5098a09582ce07e0044a4a2bf9869129ed3a31eca`

```dockerfile
```

-	Layers:
	-	`sha256:ea33c415b3c5547602a537ebd7714625bbb344a504a2f0aedb1dee7627093231`  
		Last Modified: Thu, 11 Jun 2026 01:34:30 GMT  
		Size: 3.3 MB (3285252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104f8bf825e5500b1187954fcbf9f950ca4eb517b622d5e0e8578447286e14ff`  
		Last Modified: Thu, 11 Jun 2026 01:34:30 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:64821e793973463aa261dbc73243f21920b922dd98a4a4e8fc9e4c423e33e3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128415279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8f4e5434e82061a82740f75155898c631b4df1c0978fc7184dc768993e8fe4`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:52 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:46:52 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:46:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6bf566fca74c226a4237b72714242ce34a41c007dc652b12bc3850a7685b5d`  
		Last Modified: Thu, 11 Jun 2026 00:47:07 GMT  
		Size: 78.7 MB (78737110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d967779c255f82fb604bf2291862029343f6d198a6f83b87cadea18520dc455a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf33bf59d16ddab8cd1cfc47debecf285ad478d3f0433241c148e1ef7df3b93`

```dockerfile
```

-	Layers:
	-	`sha256:b10d8f04a4db0136c4d2b94b7de3f5ca1cd8666dfec3e784574d6e04f853e070`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 3.3 MB (3284726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12c78338d56dc5f364870380ebaff5eb47a55c5d054efce784bd3370fb89b62`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 14.0 KB (14045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:3c4289476cb547c921a0b856eaaca1aa513f8b16879d9c2a9a1b0063453a5f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121225949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbbe743d9afd8273aa62d5dfed488269efb5dbc48242e05713ed723c1021888`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:15 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 00:47:15 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 00:47:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900e4402c04bc69094419c633f5733fffe690e92741fcd6207b01ba709fa969`  
		Last Modified: Thu, 11 Jun 2026 00:47:28 GMT  
		Size: 70.4 MB (70390386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ad7bf110247a040f652ae6cf7b5f87b7f4aef35ffe67a0ddcd2ccd8387d0de58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3f065e863a696aa6470926d27323c72227463e1bb3e03265b98323f99c6371`

```dockerfile
```

-	Layers:
	-	`sha256:879859f04bb75c78574ba093f1640a731061f39c60ca2cb885d6001ef33e7e6b`  
		Last Modified: Thu, 11 Jun 2026 00:47:26 GMT  
		Size: 3.3 MB (3280998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4677aca2d0d1f52c6681bf9d7aa347b2372d996e615f695b9a495f5e82e2bc`  
		Last Modified: Thu, 11 Jun 2026 00:47:26 GMT  
		Size: 13.9 KB (13892 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:381398ac9f4f326d01df71591f6ce71553c0b4dfe03e50db69b4e7c5a2a260ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124515131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec6399a90bf0e1d8a273f61f91c4c5f15050acd6811e00ab7e26a44b3ca4c67`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:55:45 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 04:55:45 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 04:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca000019d46086b7d7f9b72e7e1cbbdb48b3b7672143d1fd7f247ef3c02aaa`  
		Last Modified: Thu, 11 Jun 2026 04:56:10 GMT  
		Size: 71.4 MB (71377192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7f097bc6a0ff88eab3c95b1e4ffbab2043a78efb195393c9afcdf7ee6e348cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5f036777909a1821da5aff748ba0772c13137a3dd3bfd1b360af88763c330e`

```dockerfile
```

-	Layers:
	-	`sha256:90a8200f74c6e4bd4507ee86f3e38e53840d7d4a2534abd1589ef6cde62954ae`  
		Last Modified: Thu, 11 Jun 2026 04:56:08 GMT  
		Size: 3.3 MB (3287419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e557520bc8db588ef419f7589f90db4d8ff0ae434f38abcbc9e547011c02a94`  
		Last Modified: Thu, 11 Jun 2026 04:56:08 GMT  
		Size: 14.0 KB (13979 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:ea4d78f73c9d8848a77e15e97b9f794db261943ca1bb0ef09c6149c3b63d463f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120666435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f51b6fbd3663a5ec4996fde45eafe99d2f629932ba49ba82904c2ce55ac589`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:47:39 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 01:47:39 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 11 Jun 2026 01:47:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:47:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d151de08a3d978174fc5c18c92b4d5ebe806b9c410fd15bbc74da428cee477fa`  
		Last Modified: Thu, 11 Jun 2026 01:48:00 GMT  
		Size: 71.3 MB (71280538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f9a9ec0219383e69447c15475836029a36c7fb50e7c41ba859845e5146c33917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eced5bcfdf92f5188265db065d097bf6e718f4c5701e9cfdb9f87e5923d3ea`

```dockerfile
```

-	Layers:
	-	`sha256:2297e36b69aa72a4e2663ea6ccb6debbe9481ca5f47fffb17693b74670b4f864`  
		Last Modified: Thu, 11 Jun 2026 01:47:58 GMT  
		Size: 3.3 MB (3285269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f30f57be18d9587fec41a6da9c6b689f21245bcb998944aa127bea0c77baf96`  
		Last Modified: Thu, 11 Jun 2026 01:47:58 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json
