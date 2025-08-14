## `erlang:25-slim`

```console
$ docker pull erlang@sha256:e71413c1ecd1e44941c37c3edf3480e76667b35c6e69a38bc6479a9869ea067c
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
$ docker pull erlang@sha256:9916d9c9c51a4e0d66025168a759697f420241e4f4159c68c70cec7e0a1240e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119712643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cfbf656736454fe59d74841485c896ff30a3435507c525304a913852ec557e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d225f9edb40056d143509c99b3884b62772f49e5b4bb9e4e881457cbb94fa0`  
		Last Modified: Tue, 12 Aug 2025 21:29:01 GMT  
		Size: 66.0 MB (65957299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d9169cad941c5f0b3693a600995b782f8f1e8b33797b679dcf230511924d9e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24f860247df076d5c801571a84a1ead3d2d8933b63fb3b5cde5b2ee283ae3fa`

```dockerfile
```

-	Layers:
	-	`sha256:1c6571a4eb41a6255eaf4cf21ae72e11c9094e9977aa8b9efc7c00059886a324`  
		Last Modified: Tue, 12 Aug 2025 22:46:43 GMT  
		Size: 4.1 MB (4098886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d7a9a8e3e66339a300442e7f8199c1e4ad1ff7f0a3bd68aff1f0fd9902b2d`  
		Last Modified: Tue, 12 Aug 2025 22:46:43 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:3c229bea1bbe5a4f45b2eaa8218627a2547fad8d6847a8f98437cc6520444c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106313894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c50e29eddf14073e8263264c4aba253e358efafae23d716f483be54aaa1bf3`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bdb20f406ae7e5cba9c79e8545320c90c821289b40799435b21eb10ff79e73`  
		Last Modified: Wed, 13 Aug 2025 00:37:55 GMT  
		Size: 57.3 MB (57269490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0b9c75905026d0581403949f76b404e2cf9a55cbc7ab95ff34c7cde422a0a302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3af0c0ed6fac60c9043bd08a559a813dc11321f5ca8a89a081024c133d306`

```dockerfile
```

-	Layers:
	-	`sha256:aa8f71ace98f4e932d9529ab6faab9d4ee337321fb7c36f3fc113cfc73c4e81a`  
		Last Modified: Wed, 13 Aug 2025 01:46:56 GMT  
		Size: 4.1 MB (4100487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c18eecf50af857442b9cda8fef39cf261addc14696a9389436855efe5c5e3e`  
		Last Modified: Wed, 13 Aug 2025 01:46:57 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:40a406ce0681c7009cee2c7bf23cb66013d4a1e35b82b04d70a1f47ad613171e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116597020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944da2096902d610ff4aa3c3d5db81313d1ec2f483198e72af1e64e604d85e9c`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d3d14af7fa5ee7bfc443a353fac4ec70df8a50af3863941d5dff5574159db2`  
		Last Modified: Wed, 13 Aug 2025 17:25:22 GMT  
		Size: 64.3 MB (64348611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:480da03dcc1a884e6e16fc1bb87aec18bc97b9808b71d034b0e85dbc2935614f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36aa60604b7fc5854a7b96cbfdbfe87e1a0349901157401637b889fe20266604`

```dockerfile
```

-	Layers:
	-	`sha256:91f3d8f11d1e41cf3d17a515e52bd09cb02d2e883d5fdc95b849af7e20085aac`  
		Last Modified: Wed, 13 Aug 2025 10:46:40 GMT  
		Size: 4.1 MB (4098507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b0085f0071e940b21b03e211ed62a6a847d75ee638b3d1aec5ffe7d597fbdf`  
		Last Modified: Wed, 13 Aug 2025 10:46:41 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:aef5c596b4e203dd37a651468c0a0ca657c915279b4c4cb68bc48074ff27768b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112330144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad76e195f138fefab29c120f917ed0a0b2005adb09e97670f4764317b73478a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b056494a9154b3803fddd14a9be290da6435f6fc9625d140dcd10d480a375`  
		Last Modified: Tue, 12 Aug 2025 22:21:37 GMT  
		Size: 57.6 MB (57639550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4f2a27ab877b25a193b665a304e7bf48b35e19679bca7979d713cd0a68591623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f348fe455c2f0f62232c821e8582f5fbac671c57a9a8d259f59c77a5b0dce5`

```dockerfile
```

-	Layers:
	-	`sha256:223b6853357c5f914af57b764f6c510276220e17de2749cb77187e84dd96281a`  
		Last Modified: Tue, 12 Aug 2025 22:46:57 GMT  
		Size: 4.1 MB (4095414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e4e080345d0252b46d008d8659d24e1867a4568435209baa7a67f64466e0ca`  
		Last Modified: Tue, 12 Aug 2025 22:46:58 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
