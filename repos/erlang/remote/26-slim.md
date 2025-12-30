## `erlang:26-slim`

```console
$ docker pull erlang@sha256:06e2b8e342e5261f6cb65aadeaaf7b2afcefca4d7dde143f4c8d6f65ab65e1c1
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
$ docker pull erlang@sha256:1948376d0203930138aff1466f87781b0a984bd64ae5560405f7fdb02702de3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118915656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dca35ed61d96611d40195bf477a9bfcdfe05c5fc3fc70bdaabd69e12358e9c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:39 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Mon, 29 Dec 2025 23:56:39 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Mon, 29 Dec 2025 23:56:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7102e9ad447270dca12ef64b74efd8f658a46ec33ebf3a348b0a85e54c905b8c`  
		Last Modified: Mon, 29 Dec 2025 23:57:02 GMT  
		Size: 70.4 MB (70434860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:887435244420a7b5dc76b6df2a8f068afda6fb855dafacdb95735e6c71bba821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34c73cf8b94c37199a07caec32c1b8acaa3952a521e2f689a09e0200083173c`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6265473a958c6392c0aab30463223b19bbdd362a9a8d6f548dca23dcd5d7b`  
		Last Modified: Tue, 30 Dec 2025 02:48:30 GMT  
		Size: 3.8 MB (3825351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bce144e215d99e597dec423401080c8e8a73c1c6e684f77848914011ce113fd`  
		Last Modified: Tue, 30 Dec 2025 02:48:30 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:a4cd3fb0c9e06997917e308f05ad6f50dc6646a1f2dd0ebf5496f5acb570e86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106560069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53096f898f702c3212a930349eeca402abd6ce952728836f39a836e8ab3f8bed`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:34:26 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Tue, 30 Dec 2025 00:34:26 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 30 Dec 2025 00:34:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:34:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:382890ab3968ba1cefa561463cb731ea178ca7d67e9b6d5bb6fac532b4127c25`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 46.0 MB (46015872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6918ad327e2e8b8d9e705cf2f7280afe7d56a78db41d551a2c28e84822f3c52c`  
		Last Modified: Tue, 30 Dec 2025 00:34:51 GMT  
		Size: 60.5 MB (60544197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:30df91c0c0a1621289958219e109deb68ed63eb4c8aa830a1fac1e079290d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a74f424206fcf11fcba98dd244400c18e03c84ce44ff8686900c477c73b8f`

```dockerfile
```

-	Layers:
	-	`sha256:f5db60e14acd51c14fb773a5cfa7314f701424327bfe3ec6f74a5533a9946e52`  
		Last Modified: Tue, 30 Dec 2025 02:48:35 GMT  
		Size: 3.8 MB (3829159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d614a1f094b83dcb16721033d99da7705c5caa6128ffbd6794ccce43d45a45b6`  
		Last Modified: Tue, 30 Dec 2025 02:48:35 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:6e1367ff01908827b6e22a43e817522706a3c5aec7d2545719405e1d4d284e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104354267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd5c74dfe749066fdf3a76abd5acfcbbbc9b38ecc83e15a180ba0290d06e45b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:46:26 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Tue, 30 Dec 2025 00:46:26 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 30 Dec 2025 00:46:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:46:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f74ad45c59b0c98f9e6ebbe8f69a9e5bfe52865f9bacbced0ef68b2c80a92e6`  
		Last Modified: Tue, 30 Dec 2025 00:46:55 GMT  
		Size: 60.2 MB (60158137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2f3f474785a70e59086749fcb45cb2964229e965605bc86133f4d03f7c0756da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae85f5ed2e6643640fc771533f7a25b8f7a69fd9355d6863c5a5f0e09f542e4`

```dockerfile
```

-	Layers:
	-	`sha256:f67e92df6a091b5852b6698a6352381c762bde3590d91511cb0dcf6316f3ac03`  
		Last Modified: Tue, 30 Dec 2025 02:48:40 GMT  
		Size: 3.8 MB (3827584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933b4fbcc9af37efdb4966522a6af5c5a5188edf9669d9e140e889ea0291f393`  
		Last Modified: Tue, 30 Dec 2025 02:48:41 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:191920d0c6c45cb11bbedcc7eb97078cb290c38eb538b408dd04523313896db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116428559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d08bdca3149ab5bdf7dec4fc2f0b768567ddc0d5b30e20bd3616abf54ce689`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:57:18 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Mon, 29 Dec 2025 23:57:18 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Mon, 29 Dec 2025 23:57:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:57:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1159fe98991ed1b259e3ba6cf64714cd57565332d5a57b7b7c4d847b6d96d981`  
		Last Modified: Mon, 29 Dec 2025 23:57:41 GMT  
		Size: 68.1 MB (68069412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:628601774bbaa9431459c277e05b47738b9da439f6bb5f10c70dd820079ff5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51bcbb1e8a2c70246331f7ad059bf54672c5260fdf4ccea745ef967979e350b`

```dockerfile
```

-	Layers:
	-	`sha256:5864e49a55a244a3da295379845494ec15209b5d5969c27214a0943f32959feb`  
		Last Modified: Tue, 30 Dec 2025 02:48:45 GMT  
		Size: 3.8 MB (3825612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a469cb30759ca6b723d94542ad5ba2a1cf1935663490d6146a665d634b32e3e`  
		Last Modified: Tue, 30 Dec 2025 02:48:45 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:8cbc9bd863370de4cad0d55f16dfbee0b7abcee90a452d3f6534ce3b9e5901f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110627238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709cda4bb6a29fdfcf1f10c11eeff842cde0fb985827f262adf36c06a3ed4f93`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:52:04 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Mon, 29 Dec 2025 23:52:04 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Mon, 29 Dec 2025 23:52:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:04 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3cd1949e0faa8dc3bcdb3b6fce45884e9b252aec2b9882d6dc8885b10661b1`  
		Last Modified: Mon, 29 Dec 2025 23:52:30 GMT  
		Size: 61.2 MB (61160359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4ee1f7ff154ee42254b0992e998d5b192dcb8e0dd4d93f7e47c9e7f8f15f4afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bc62a82dc73a407a4027f96f797e28a0de076ad0074c5a6886ebf9ea3e9d6e`

```dockerfile
```

-	Layers:
	-	`sha256:0dad9494e51be99e5a1dcf72ea28f03572d93633cfdaeb2968ea38dae2b22484`  
		Last Modified: Tue, 30 Dec 2025 02:48:50 GMT  
		Size: 3.8 MB (3822513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8dc00a655b967afe0f5b4184801cd174a26f7e608973e7073fb21409929f530`  
		Last Modified: Tue, 30 Dec 2025 02:48:51 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:c7d0d22cbe68161b48a86c710fc108103e11712cc536dae7ff78fcba5c397d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109897599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a4ff76af9d7b9e907b398ac672ee7e75d03e2b42b1ff6112bdc718a3e70272`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:01:35 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Tue, 09 Dec 2025 16:01:35 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 09 Dec 2025 16:01:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 16:01:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467687fe2cf07d016639c805110f50571bc962f37d2c1c4e19e950e66a2d2e82`  
		Last Modified: Tue, 09 Dec 2025 16:02:46 GMT  
		Size: 61.1 MB (61136702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:050de53fc392698e067a91f23a592eaeef2dbb653bff0d330cc577dfaada13b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3463740c855aea8326880cb4cd98ad9da0bbc50d096e52fcebc635fc12c03bc`

```dockerfile
```

-	Layers:
	-	`sha256:ebf6b2dc3f0f111ed4e20f9576a9cc60180d27b2a393ec3bb8f1e2e7585216c4`  
		Last Modified: Tue, 09 Dec 2025 17:46:55 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:1837e79e797d914672c8d438937153e3f4e54dd971624ae572b6e50b3af89113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114586877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f144a059e1e1e1b87a4558b095df89e82e9051fe88e5d9b06ec93088a4dd4b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:38:24 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Tue, 30 Dec 2025 01:38:24 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 30 Dec 2025 01:38:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:38:24 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd8cc19b2f432bf35535c6958d10440078487f4d4db4949dd8421052fc4dd9`  
		Last Modified: Tue, 30 Dec 2025 01:39:01 GMT  
		Size: 62.3 MB (62259879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6c4644f9948bf807451e15423e72fe975b27067f9b029875f2ed23b0b93e54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b265c2d558a06fe2bd76407bb576f30ac44e376ef5a7629a26b495ed971b7469`

```dockerfile
```

-	Layers:
	-	`sha256:e8ffa719f134803a771d45a2ab2cc373ced2ac6adc7e32d9631e4b8483d919b7`  
		Last Modified: Tue, 30 Dec 2025 02:48:57 GMT  
		Size: 3.8 MB (3829799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4cdd504db5670bbbe420fca25738da311c676391acbdcbf99a64d668a1cd6f`  
		Last Modified: Tue, 30 Dec 2025 02:48:58 GMT  
		Size: 13.6 KB (13606 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:29c4928087746abb8262e2a439e9a482a0d70d9fcba4ca6045485a01ac02d030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108104447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5df474de3314486332b0d906f3a40d6f15117aedcfebd8652661d23a64d0734`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:49:01 GMT
ENV OTP_VERSION=26.2.5.16 REBAR3_VERSION=3.25.0
# Tue, 30 Dec 2025 00:49:01 GMT
LABEL org.opencontainers.image.version=26.2.5.16
# Tue, 30 Dec 2025 00:49:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f145ea6aa8cb9c15fac7d7905fbd530c25420d11f4e23c5c3df6ccf27584625c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:49:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498b2ca4b274f0ee7f54419a7a1c5df90f29fccd0a29ad254554d6b24d6605bc`  
		Last Modified: Tue, 30 Dec 2025 00:49:29 GMT  
		Size: 61.0 MB (60966720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2baf38de62e551ad5564839e3c32cac0dfa7a06840f030cc76ef4612e8ee9220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165e664d67b6ff2a7bd953d1218aa193da5b4216b38566bc5988aeeaf7c7a5b`

```dockerfile
```

-	Layers:
	-	`sha256:c6f64dab961f318b81f730316e1025869a44849a77bddb3f0ff4df393ee0f166`  
		Last Modified: Tue, 30 Dec 2025 02:49:02 GMT  
		Size: 3.8 MB (3822179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04532fe78c09ac1b872af764743edec1bd8589e7b6ccafc50a48b417d3fa9b0e`  
		Last Modified: Tue, 30 Dec 2025 02:49:02 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json
