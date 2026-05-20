## `erlang:26-slim`

```console
$ docker pull erlang@sha256:2c52f98e44dbaf1d06c1c6b3501ca280ede113f4e4467932dd203c0a8c150331
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:78586704c5efedbc9312f1fd931509ce0382c75fa698c4d893d16ed5cf0df822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118966500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429bb9459a845ce6270c06b311d9db07ffcc52c8c6782a2d7457e1668226d059`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:46 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:27:46 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Tue, 19 May 2026 23:27:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dc4aaffe0cc133c07338499e6346384b9db1ff719d487b4abc47b91404ade6`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 70.5 MB (70471068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9f22abe42e3439a8818c137dc01032cfe42b3e69fec3111ddeb4d24ff2d2475f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc4895d84275058c85e05692b6b30298594313f3d137751b149d6124860fa57`

```dockerfile
```

-	Layers:
	-	`sha256:26686b9a7a1e13cd9465bcf3bf19baccd6487131616b3555d737afe023155c63`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 3.8 MB (3826036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b963fdb0e118b35b8125d55f4e88f88da7264110ccd3fc3f699c2555845c925`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:f3327059fdac328cb8fee10fd94ca4bea6c689bd91cf247b9031612ed025e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106597995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415b2e852d3460784c9c80084d71f2958274187d475e57425ace9d96afa79971`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:03:37 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:03:37 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 00:03:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:03:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb6d46b4db4ab3241f34957b7a3be752dc0ef5172b3b33217c4d278775e098f`  
		Last Modified: Wed, 20 May 2026 00:03:50 GMT  
		Size: 60.6 MB (60568492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:22298d666a158fd05cced0410e689022b1fd393f6a3520525481711e68a27048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d96e5a5c880cdd67da56c27ff5ef518900eecc88fa393e22c726657949040a`

```dockerfile
```

-	Layers:
	-	`sha256:95f9297eb258b681eb779ff2a62088497ffb3432e5bb9bbd931b2a529a452820`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 3.8 MB (3829844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58c8c491ca17d078e986faaf3ad6ce89a62035f6e8824ec5d84e0f84ab1f292`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5aff9aeb0884b4bd938ad897609b9c0ab9803220c034650bbd65672722e7e436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104396099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8990a6f1820ad16e216bf82527085ac0bc9298a793400eff20d8eac631cff4f9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:16:14 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:16:14 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 00:16:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:16:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872872331d11cc8dfa894058759323ace6be31af8949160a4f86cef471796bf9`  
		Last Modified: Wed, 20 May 2026 00:16:27 GMT  
		Size: 60.2 MB (60186945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:11a0792b4c7b3f2cdb870d5bf9f2bf81a43ac1a7fb4e901f0f7dce44c9c14752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2752c29371887b05c1089fd706db1916fcb9888a3a71b1271053c1ecd1dbff5c`

```dockerfile
```

-	Layers:
	-	`sha256:9ec5bd6222f50c7e8165ba68f936a07ae5e938bf4e446d8089ab1b30f6539733`  
		Last Modified: Wed, 20 May 2026 00:16:26 GMT  
		Size: 3.8 MB (3828269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d964e097d57c352b6c8beae0fc7c7cd75a6a1c12ef198def52c77cb8f266431`  
		Last Modified: Wed, 20 May 2026 00:16:25 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c00dce2e2d2fa4a9f34fabd1097cc5c99b66c661b5c9d4f0b7fe57f7c7d679a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116486568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce51588f70488b791cf26b79537729b848e74aa0e0c41436ab69cbe0bc95b9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:31:21 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:31:21 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Tue, 19 May 2026 23:31:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9f0f59203deb6e8a48bc9b55d6569dbd376dc6d15c8f70dd25f3048d443933`  
		Last Modified: Tue, 19 May 2026 23:31:39 GMT  
		Size: 68.1 MB (68107136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7161a3411eeca77225211c6f7ed13075fb45cac2079a271879850898c4cfd9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cce34ccc57c50c472c3461769400b198af97a8124aba43de7c453e5d25f2c7f`

```dockerfile
```

-	Layers:
	-	`sha256:93e6b1ca37b0993b56213d45a7ab3c3564748beb851b2a67b682977bfbfc10ee`  
		Last Modified: Tue, 19 May 2026 23:31:37 GMT  
		Size: 3.8 MB (3826297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa896befdd1522e28b335332bf2cc7eb1fef030770bb685d841544c28c10e5e0`  
		Last Modified: Tue, 19 May 2026 23:31:37 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:ffe0f53f844130d7fdbfae725f4171c75adbc134d778f9d88e61a12730f633ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110695504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01e056418758a2d30c76b313b23d0a48ce0c9781861351dbb13caa045c8c15`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:29:13 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:29:13 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Tue, 19 May 2026 23:29:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:29:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5511ab7b4ee0ef82e86ed59bf113b66301edac373fa6fdfcd3cfa44a39ed302f`  
		Last Modified: Tue, 19 May 2026 23:29:25 GMT  
		Size: 61.2 MB (61212384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2f5d25f446f02f1208d51aa622a44f7776d76bbc9b8587e19526ef291a05ec96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc69fe0098956403a4a619eaac04860222df82511b4697b4b78e568898fbebcb`

```dockerfile
```

-	Layers:
	-	`sha256:9f8ef5fcb2c67247979bc38cc9d2f8eaaab2f2c717ce256bcd962854999d3bf0`  
		Last Modified: Tue, 19 May 2026 23:29:23 GMT  
		Size: 3.8 MB (3823197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1a60010423f6b784826f52e9f0fc199e686eaea6f211b91b7287db8a3ee9b2`  
		Last Modified: Tue, 19 May 2026 23:29:23 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:c50c585f5c00286e4ae91b4b7f8b96e7de4df7c5bf6632d0a4626efe4e2f849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109960345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ef5ddf7164661f1e1371f46f240f6386a2a18b326eb61d2d2796e460023bcc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:42:53 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 10:42:53 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 10:42:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 10:42:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffcfb540ae132b8a380e01e5b4ca9f424d4fa78700b03a1675403ae66cc22ab`  
		Last Modified: Wed, 20 May 2026 10:43:56 GMT  
		Size: 61.2 MB (61174106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4417f10d5d518e4f1d1a4cb7c14a71d0973bdf1d34645fb3e8f0c7f3c08dac18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a540adc071f395f2e73bdccde47c82f2489c1001d005918482d810e2309586b`

```dockerfile
```

-	Layers:
	-	`sha256:f029a187d773f779e6145576d2e90195f72cc61a55f50ad1588de7a73dfc77e8`  
		Last Modified: Wed, 20 May 2026 10:43:50 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:b2f274d8bcfd8d8a4fd0cd1b5d9b63a081af47cbfb654371f15f023fb0d64876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114631098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64564a2fe1d250754b7612cbb0ddbe6745a28555bd4cbdae3f213d1cf165aec3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:27:04 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 01:27:04 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 01:27:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:27:04 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446d6084bb1c105d0a2a5737e4bb859312a3608e984509956d60f5ae44183d3`  
		Last Modified: Wed, 20 May 2026 01:27:28 GMT  
		Size: 62.3 MB (62290899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9643a0280e243f40834ab757dc8bcb99f6fa268d81ce5de93bb9bbce44f03cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db61221ae1a3b62103c620ddb03a0080c1026153b2816af7cd2daa34cdf38c51`

```dockerfile
```

-	Layers:
	-	`sha256:3ff33acbf958776713473536b2aebf4a96a6ed4fd61a21efba8b377524ddf324`  
		Last Modified: Wed, 20 May 2026 01:27:27 GMT  
		Size: 3.8 MB (3830486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d3a53644d413d0a6896d955bc1f64d5916f2012ef87e52081fccf572b2ead0`  
		Last Modified: Wed, 20 May 2026 01:27:26 GMT  
		Size: 13.6 KB (13606 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:111898326eea04bbd7a2a2a9115e36845391288862f46a58b3a7854496327983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108153632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b785c3e8196a8acd10be4fa838a92a2c4d1c78916c3cd6ab68e27008ba044355`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:27:40 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:27:40 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 00:27:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:27:40 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1d9af51f5f3ac339c75d2a3ad7a43537fd41d88777747b02eba9c791812e7`  
		Last Modified: Wed, 20 May 2026 00:27:59 GMT  
		Size: 61.0 MB (60998043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:02a8a93ad8f5529b8fcb426e3a5d04c97e5b695f673c0ebf6f854857ac59f738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f17156b3bf4a77c7961e3bcf93dde694047050e5ccdf0a08582945be3b7604`

```dockerfile
```

-	Layers:
	-	`sha256:c84c6188ad9f0bf66c3ba7ce6cc827fa4c06f26b060a758515460f5e8439ea53`  
		Last Modified: Wed, 20 May 2026 00:27:58 GMT  
		Size: 3.8 MB (3822864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8c8600bf8280d8e9c463b6f6ee43004718b96492b35615440dade1031f5254`  
		Last Modified: Wed, 20 May 2026 00:27:58 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json
