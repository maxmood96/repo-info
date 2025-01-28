## `erlang:27-slim`

```console
$ docker pull erlang@sha256:600f4bce1a5be3b84ab8ca17935225491bffd581c9314ef37e06c2cf5bee087b
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

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:d2a372bef3dea8f0bd7027dff63faa28e74ce2adf6f2c635b89825b3b443103a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124391747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e464f9a60b653fde7d8cbf0549395bfc317073d9fdda3a4e742d962c73f1423`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f899162005c69e93bdebadcba05bd4987f74f11bfab6ee6f2a1bb3c33c20b`  
		Last Modified: Tue, 28 Jan 2025 01:30:39 GMT  
		Size: 75.9 MB (75911785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f9bd97143b464cdc5cf8c04544cbe5700010c111ba536d979a61e4ac319ee63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251f513c7fc998d8153ee5f56e971442282767b5ccdc964d86fd3aed8a8c065`

```dockerfile
```

-	Layers:
	-	`sha256:09aa746c6f56035157aa7f3f86328a727b43bf63d7c3a43945c3a2d49d77ad76`  
		Last Modified: Tue, 28 Jan 2025 01:30:39 GMT  
		Size: 3.7 MB (3667810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313c4728c118842b449470179bd807fdc6002a36bd341d81337e71d311d17b38`  
		Last Modified: Tue, 28 Jan 2025 01:30:38 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:54a263d4fb3f64bb5b235468245373740385838cd1b05574939948b3120d0f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111421592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d118d3c4da2f041b30fee04453fb9666a128b2c6c100025f12fbdeb4000c6c5`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:237814a70d9f7e95f3568236c75036fcef22a88f1a76245129eca111484c0351`  
		Last Modified: Tue, 14 Jan 2025 01:33:00 GMT  
		Size: 46.0 MB (46006814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf352980ec1078892133999099a3f674431701e3ce4cac9e45d1dac4ac70b4d`  
		Last Modified: Tue, 28 Jan 2025 01:40:07 GMT  
		Size: 65.4 MB (65414778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e6ca677dbaf224f1029705b52580eb0886ccdc3fb9d2aabaecd0c79b81100fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ca6a83e34e4d44331f171300c71ebc994b14d6d017846167fee615bb8c3689`

```dockerfile
```

-	Layers:
	-	`sha256:1ab2b6a286d6ef7858169378cb828957071423ced91653f873a77228dd74d182`  
		Last Modified: Tue, 28 Jan 2025 01:40:05 GMT  
		Size: 3.7 MB (3711824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8cd70203737cf2c8aba53c583a9986c32963154ae80f397d26c06889837bb83`  
		Last Modified: Tue, 28 Jan 2025 01:40:04 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b26e91b5936c6972984188c0e9ceff49e19761ef57a94ffd9a91e8f85999edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109214342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab279dbd3ca274881491f90561b48faaa861809a3e4e394bfac8f5a6db7713c8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdaf9e2fe7e34def602d36b8b58f2f88f9fe2223a6115ce759e93aed6bfa480`  
		Last Modified: Tue, 28 Jan 2025 01:45:47 GMT  
		Size: 65.0 MB (65030133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:95498c67e7b86d36f406d63b2749e2630ad0a6386886dc4ea62e0e0aba6d827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb3b1e101ed612fdcf4ec3b31f6bb12e79381f3b5220c370991178ca772248e`

```dockerfile
```

-	Layers:
	-	`sha256:2ceefa8d6bb13af589cfa8d5419f75b1639fb0e6356a11d8f44892f45bb1a9a4`  
		Last Modified: Tue, 28 Jan 2025 01:45:45 GMT  
		Size: 3.7 MB (3710557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cff706a1ae5e5429fc8e83a32698719415b45365d73b6c0b2e05a33d3053a38`  
		Last Modified: Tue, 28 Jan 2025 01:45:44 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f345d440d43e49b857a5c9af0a56ea47330979a602182db80e1200c283c06080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121954381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98826621d3f3fb5412baefd426b62bd25832f81eba50a7da241eecb984f94568`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c0a8ceb3eea84e19388b174bcc78c7c0239a00b6ae5f509167ddcf2a4cca0`  
		Last Modified: Tue, 28 Jan 2025 01:48:35 GMT  
		Size: 73.6 MB (73647485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1f6299d06c80ae24f164b1191773f19eebfbef644c3741de8c183fa2a6a20477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb413e036c905dcd4df3f8f193d01b4829f35c92653d9203571001a1e6bd9ba`

```dockerfile
```

-	Layers:
	-	`sha256:c10db6a0156c1ff6b1a5c1614cdf4246f194903c2b0f9327824146f73021fb3a`  
		Last Modified: Tue, 28 Jan 2025 01:48:32 GMT  
		Size: 3.7 MB (3708589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82fda01182b9b5cf524ff22d689dcd86e27193a7a5950e3008d7ee7d5f7d0e8`  
		Last Modified: Tue, 28 Jan 2025 01:48:32 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:20c028807dc24762224768348f66727943e834d8b4fbcd4479d1a9bae2bf1054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115532276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf45c4384de60028e04b05d89469d66e2fbf2a41016e2e67932c3e0067c6c28`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849c7106870c35b9439e54ef471e7d6092bbda800274c34fa5c618b7e62f4c5f`  
		Last Modified: Tue, 14 Jan 2025 02:24:43 GMT  
		Size: 66.1 MB (66074531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a00a689c4130f082a817063448febd8a11f18c74554f842ecd281807b93f95ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357cb0b0fc35a249c6b4aea1b9d5ac9a5aa3f6820bc77b43a64e03cf0560674`

```dockerfile
```

-	Layers:
	-	`sha256:13cd79ad4eed8544d3514dce42a049bdef573b25a0385bb0f81ac2aa6dfe9685`  
		Last Modified: Tue, 14 Jan 2025 02:24:42 GMT  
		Size: 3.7 MB (3705403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfc1223fc824e2beeb004cdd8a1a0d1b448dfd4971695c1d1bdd611b40c890c`  
		Last Modified: Tue, 14 Jan 2025 02:24:42 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:8b7853f5f57ce623023ed27060201d11561f62460bb24fc711702b2ddf7ce7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114741250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f34941bc4887124bb84e8fe3b4fcbcc58b6c1d7213935f2b9dbb17806e42cc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b422d794c57495919fa561c96a4fd3cd704bf77d15ea3ba0b0eba52f6767a6f1`  
		Last Modified: Tue, 28 Jan 2025 02:04:29 GMT  
		Size: 66.0 MB (65983147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:782e107ea0ac99e863681538e39504400c7b73ae3963b7c17f73b695058de417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a71eb1e107fb1e2538e38ece2d53a1719a960e684e53541550367f269f8003`

```dockerfile
```

-	Layers:
	-	`sha256:b6c91b1351068dffd049e0b2a6934ffcda50813ea61d2ef681b2a3ac1c275e6c`  
		Last Modified: Tue, 28 Jan 2025 02:04:22 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:22ea3e47b5518fdc9f98233517937f038fd1a2c99e4d5df7dc52f06ac5a20839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119469683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57858bac2a9668b15011a7404f8dffc62a2fa91eb1f58ad64f656bbadb91c8af`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5513cfdfc11c7d002989a28edbe916c2a9a18ad03cf06b78a37a0dfd785f7417`  
		Last Modified: Tue, 28 Jan 2025 01:55:18 GMT  
		Size: 67.2 MB (67156546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6ebf9a0ecc80ed2f0d87aace1d0134fbee8afad8c39e9cc7fa5c72fce9f85f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41bc48352a3e3aeb25ea81d7c5b46d281261318bcf35c46090a7e6a88b0f232`

```dockerfile
```

-	Layers:
	-	`sha256:0e9359b19285e3fa1ee4627c161632e4c387201e609df642505125b4cb6e5d89`  
		Last Modified: Tue, 28 Jan 2025 01:55:16 GMT  
		Size: 3.7 MB (3712662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f161b1d35e997cb32f749ede61b40e71167bafb60f4ad0e686e4dd041959ff`  
		Last Modified: Tue, 28 Jan 2025 01:55:15 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:71ff3df8836788b9287bd90fd976e5bf0e1b58123b2c39fbabaff5a320aceada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112951664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762a1e125fb94f4e591758d8445ea462d2bcc6bdedd91802e00a661300c6b4a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367bdfada553c05d00ba61395136a1a30b0a2c78bba49dbc54030d658a4a87f9`  
		Last Modified: Tue, 28 Jan 2025 02:06:23 GMT  
		Size: 65.8 MB (65819882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4c1b5bbcb8a99b86e3e740563f6dbe0412dfecc4f8d61e683e8bcb8266878cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58fd494d0d9b26dfaa54bb654282bea6d961ca37ee0f20f15add3f1839cc02e`

```dockerfile
```

-	Layers:
	-	`sha256:583dadd306d76e23c46c0aafb9b1b25632876c694e7e36fdce19003bb6a8ee4d`  
		Last Modified: Tue, 28 Jan 2025 02:06:15 GMT  
		Size: 3.7 MB (3708036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8901e43900050fedb395284d6dd5caa62035c186741457e11bcd1bf5e0c10bfa`  
		Last Modified: Tue, 28 Jan 2025 02:06:15 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
