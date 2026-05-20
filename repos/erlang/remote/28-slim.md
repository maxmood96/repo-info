## `erlang:28-slim`

```console
$ docker pull erlang@sha256:2cc884e1bb45d447f5957b4bbff3f43673a2085b7b06ad20fa6a336dc2533cf7
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
$ docker pull erlang@sha256:2f289ff7446446e2649b49dea1ae03098f3ff592d2843b9b8aa0efc58122bc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128239984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4268330cba23a683b824171061beface4e8b9cdb8e3f6f2e2830fb0f10d29dd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:50 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:25:50 GMT
LABEL org.opencontainers.image.version=28.5
# Tue, 19 May 2026 23:25:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fa81508b64cba912e2abb34581d1be4740bdd89aa395922dc328227237e50a`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 78.9 MB (78929361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:34643716326dd58a66b772dfa4df50b37b143adfa56737cf818d3845022ca058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8578d6a2b67f120ce87dcccef3ae30ef90e913e20127a54d562d6d3534a9c82d`

```dockerfile
```

-	Layers:
	-	`sha256:240dd366916fe5e5d9f99881dbc3f00fa52ac23597f5caa256518f4fbf2ec03b`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 3.3 MB (3283644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7f8df91bae23894ba9030febcd1208d82f4a6c3fdd4aabc1c59f87e9958987`  
		Last Modified: Tue, 19 May 2026 23:26:02 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5a4555e87e9cc6a17e55e3bb5850f4574a234d15b2c724191776cf03bb86fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116925097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c15c54303336500d5e26cc61e29134677be5502b3a0adb46922ad45e4e988`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:00:40 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:00:40 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 00:00:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:00:40 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae60dfec5d7e3d3d9851d894d405e63b2f38b19bfe1ec87d63aa99e416d08698`  
		Last Modified: Wed, 20 May 2026 00:00:56 GMT  
		Size: 69.4 MB (69437051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:daa9a1550f4448a33cd56639231e0dbe12fc48023e28deb87fa683df980bcad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158266c1097b2830f7c6c430441e96ed65796dbbea6dee33a2e895a56bc9b497`

```dockerfile
```

-	Layers:
	-	`sha256:9967567af4e257e879bef298e042731cccbdf00f3cbfdfa303e3ec72ec0e0645`  
		Last Modified: Wed, 20 May 2026 00:00:52 GMT  
		Size: 3.3 MB (3286611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7adbef157b4b8c6ded8822c7677c8978d8d35deef62b32d4f370479299a0a3`  
		Last Modified: Wed, 20 May 2026 00:00:56 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:ee023897b37234cb38fd3619135be25eec09792e95873eb3fcc1460f75eb7149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114736794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7709b8f7a89c0c7391fee634bbed5597b4fe4ab2608b0427a541df1137e9fa3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:12:28 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:12:28 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 00:12:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:12:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae98a34caebefd86972f7c2b41b3bfddd997af5e5ceaf21031963bb87b525cda`  
		Last Modified: Wed, 20 May 2026 00:12:42 GMT  
		Size: 69.0 MB (68994763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a6c2c749dc724d0e0b5e5e4d7b8e4824e648cffe1d837a8507bf8133b6f0a977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24354bca84634b4c946bbdae24919897626fbfdb861d7d08eeb024787c6da716`

```dockerfile
```

-	Layers:
	-	`sha256:6fbeb25c6c076ee515074cba5ee8c7230ee8cc59a7aee7d26e0613310ce4106a`  
		Last Modified: Wed, 20 May 2026 00:12:40 GMT  
		Size: 3.3 MB (3285060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08ef41ff11b945ab43626ba235b300aa2a9050317f0b577e23ced8ff051ce85`  
		Last Modified: Wed, 20 May 2026 00:12:40 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:02958fa47f17d0d6337c3229ffc40ebd5e471210a34e0a0133d1647e8c1183f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127155749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5365cff38c4e0a7304a55c84cb3be7aa48ee11d5f57a62732c592bd89f25acf`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:29:32 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:29:32 GMT
LABEL org.opencontainers.image.version=28.5
# Tue, 19 May 2026 23:29:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:29:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da832110d57168533952319ed9105994ec64aa3dbd8b279f7702a84f4c282f`  
		Last Modified: Tue, 19 May 2026 23:29:48 GMT  
		Size: 77.5 MB (77483529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3a96f139346d9e5a488d9f284afc2017426a095a97321b1ea918788a8a7efb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1df0a1366fd16c4d194a3dfb29b727b7a5ed203c2ab13c6834db0e4369c7c2`

```dockerfile
```

-	Layers:
	-	`sha256:f22bd887dcb0d2137c1807ce7dd10d3859f8abd4fa02023793f2b6fb1376dbb7`  
		Last Modified: Tue, 19 May 2026 23:29:46 GMT  
		Size: 3.3 MB (3284530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60ec279c287aeeab5b058e405cd3320a76c9911338518b879d522c6cbb82d99`  
		Last Modified: Tue, 19 May 2026 23:29:46 GMT  
		Size: 13.7 KB (13733 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:098e07907cab4aafa8edd0ecbe2efe7433cf95f02e1443d75725e56a35658af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120243993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76baf3cb2f81033b7308548185d8297d1bc1162f66d1d12347e987ccc40cbf49`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:31 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Tue, 19 May 2026 23:27:31 GMT
LABEL org.opencontainers.image.version=28.5
# Tue, 19 May 2026 23:27:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f06cc3215250d76c6dceab2f63078bc9bf6991482ee0d0f075b94d844bb10`  
		Last Modified: Tue, 19 May 2026 23:27:44 GMT  
		Size: 69.4 MB (69414439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1642d5900565cd3c4695d999a62fdf8e99c8514347e55616401d89c612081d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3753e5ed7b406e5745374a143707d919675ffbe4deb8b8fb7ad9f001187025`

```dockerfile
```

-	Layers:
	-	`sha256:a70ab37b494b9e53bb8c199ed08615e5c01045545d60c3a5b3ba673c91679ad0`  
		Last Modified: Tue, 19 May 2026 23:27:42 GMT  
		Size: 3.3 MB (3280819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b34727ac3df6c6e02626525395c14290cfddd1a0aa9af95c797acec44a737fe`  
		Last Modified: Tue, 19 May 2026 23:27:42 GMT  
		Size: 13.6 KB (13597 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:625dfdbca26d96f805eb73d18ab3cb70fba79377c7b44e64217f5b077bd33f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123512576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b5b2126d67eac0dbd77237b8acd81cb0cf56f768e61a2e59fcc40116a6b8ff`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:19:26 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 01:19:26 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 01:19:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:19:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5c38800197d275573d88ab2ce446031fbba99a17d3f1bca12e3704caaebeb`  
		Last Modified: Wed, 20 May 2026 01:19:54 GMT  
		Size: 70.4 MB (70380394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:920bbd5e889a95baaaa66980eaeeeaae6120bc92e339426c9ca661a8429d70c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532a3bb79807fb26e24d6f277d394927803e4f711427af2b2e6c58485cfcf206`

```dockerfile
```

-	Layers:
	-	`sha256:e8a0bdc8dbc2658c793ef3d24cc1a7fe394bdc8b6ae7959fb935182531c0dc0f`  
		Last Modified: Wed, 20 May 2026 01:19:51 GMT  
		Size: 3.3 MB (3287229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787581dcd12c559cc989bece670f168d2e9698b9b8a8f1dc39fb88773055d268`  
		Last Modified: Wed, 20 May 2026 01:19:51 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:fc895e39985e5f81e84de64cb60b1305ff1b6a3bcfcf5f2112ecedbd3d5d71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119648081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd1f94f33eac4310a6060ed12c3dd3a34cbc02016aaa5913242ca22d741476f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:23:43 GMT
ENV OTP_VERSION=28.5 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 00:23:43 GMT
LABEL org.opencontainers.image.version=28.5
# Wed, 20 May 2026 00:23:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c7e8ca23e6864eb20eff5d44738bfa123aed8cd21ed6d98e533d751eee28d9c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:23:43 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0745d9d6d4144e4e42cd71533cb20f12a1537da10657363906f10ab5b81496`  
		Last Modified: Wed, 20 May 2026 00:24:02 GMT  
		Size: 70.3 MB (70268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:01064000e5822bbc3df0506749a17d3b2121d157a4cc0df10c4be254580f233b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378871e43be095054662ae9dceec37dca8ee47204361a86d0853004e4164ed1a`

```dockerfile
```

-	Layers:
	-	`sha256:b03ed213b0a8ac39d7fe10835d612baf902aa8bd720205e15f677b160a98b31c`  
		Last Modified: Wed, 20 May 2026 00:24:01 GMT  
		Size: 3.3 MB (3285085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8add59f4d4c6159c55a50e8c5b0b87de698d374d72e6ff7f526e436fe9420b5`  
		Last Modified: Wed, 20 May 2026 00:24:01 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json
