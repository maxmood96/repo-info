## `elixir:slim`

```console
$ docker pull elixir@sha256:16d4967e7a74b2345aef45bf001fc66bef886995dd6377f3fc8a5cba94cbcf23
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

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:a200bba2d58a5af7f2ecba7935dc90edc6834a48eb603b337e96239a7f1fab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132290825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3824062df79e53d6a51bd5ccf55c7acda45038c0729fca823c654611a20f05ee`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
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
	-	`sha256:877cb198f1c89c75e73097b36c966c11b156302039b241bdb214511841fbbc06`  
		Last Modified: Tue, 28 Jan 2025 08:35:43 GMT  
		Size: 7.9 MB (7899078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f0947125e53f1cf2dbc3f91b0782e8c2f9fb085498f31d4cc0200d82299a5e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712a3a530120c1be896b6b2bafe94845c0c3e6632bee16a4b0e3f26e4d9967cd`

```dockerfile
```

-	Layers:
	-	`sha256:c7495f28767595566f6efb44a265d1a4cc28d61590f290979fe37be757bd2a58`  
		Last Modified: Tue, 28 Jan 2025 08:35:43 GMT  
		Size: 3.7 MB (3668146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a187ffcfa242311b440c11ffedb8a4c9c8f2bddb4415f654e37c7b6bce2918`  
		Last Modified: Tue, 28 Jan 2025 08:35:43 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:3d601a9f4e44f445979a72078b3c08c1e75b1c85a11fcb8486c2b5c18f3b49fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117112820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c732c47c10eb32470b1259a52fad7b360d43299095f3a483714084d4cedb54e`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
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
	-	`sha256:86870465fb8dc7a718a678448a2836a4b781daf4c34e925911cfceb6c9da5b25`  
		Last Modified: Tue, 28 Jan 2025 08:26:01 GMT  
		Size: 7.9 MB (7898478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:140d13bdf5bf3e48f1d2848f8fcc5fc5c2b71b8eb2320452cc046d2f7d6e524d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342c617c779f640a182ff91881eacbcdb29f2b13a3daf485af829c43c38e2c8d`

```dockerfile
```

-	Layers:
	-	`sha256:43ef9d673d350102d8132eb4bc6a1735fbc174e612b50df26e9eccb02c956089`  
		Last Modified: Tue, 28 Jan 2025 08:26:01 GMT  
		Size: 3.7 MB (3718207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb45fdd2bae1bcb8ef014cf7845635a609ba3be55cbfc8f76f41944ea713193`  
		Last Modified: Tue, 28 Jan 2025 08:26:01 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:2dc770ac8aca06f82757394c19a31dd1ffe137c4dbbefe9b3dcc795ae3aa9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129853455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a958eaf48eeba3e3602ed7f2280ae4509c322d91ae6ef17502087914388c00a`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
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
	-	`sha256:de0bc9417a370328bf05d193f44f915be7d1c2b69460171e6af7fc2ad87e3e85`  
		Last Modified: Tue, 28 Jan 2025 08:24:11 GMT  
		Size: 7.9 MB (7899074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:494564ba28cd0a64be3bfd75bbe1ac9902205de7c04662032d6c093255fa613c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc89003d7d946424d1d681b9e0fbccacb7f21b85da82e340565d349cf32a979`

```dockerfile
```

-	Layers:
	-	`sha256:03a1e97de15167f0c04d7d97b3217c1b072bf710350342fa41fa599f240530be`  
		Last Modified: Tue, 28 Jan 2025 08:24:10 GMT  
		Size: 3.7 MB (3716243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a2293d32ad32bb4f97f9db4ccaaca94fd40a3ec322137e16f0dbf7b69fa8a6`  
		Last Modified: Tue, 28 Jan 2025 08:24:10 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:4141e03b6f02c7cce3760de9622b3d1e772d8ad0c50f66966cd227433acf6765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123411491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb77a1b4ad38822060f9ee400081a8fc6cd002e10701216c74cb8674d3d40882`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2cd5b4fbca8a8ce31f45587c010cc308fd897b8baba237741354ac8cc3588`  
		Last Modified: Tue, 28 Jan 2025 01:31:01 GMT  
		Size: 66.1 MB (66055255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028b001c54648a5726be9c08f672bb99fe16932efb26c0880801f75672926282`  
		Last Modified: Tue, 28 Jan 2025 08:36:11 GMT  
		Size: 7.9 MB (7898491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:068b3d4f417d7a639469ffb864d0ff728042ff7b37e9b6cc781cccae9f0cbe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3675893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c67392870c2482d1a5467899a0f6cb61d26a86e61cc23678eee77d631fcc0e`

```dockerfile
```

-	Layers:
	-	`sha256:1ecf80f84532b6c42f31d0aa10b2dfe38acb00971b306189cc5aaf0b078e64d6`  
		Last Modified: Tue, 28 Jan 2025 08:36:11 GMT  
		Size: 3.7 MB (3665256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e0164744a20f6509699ec407b8fadec9b7f31ade87256200f000689eed8a0d`  
		Last Modified: Tue, 28 Jan 2025 08:36:10 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:9c3307a4833730c02629efef179e87f0b9026b27d2b95e32fa299da258b66809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127368830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a73792e37d760aa4f4f7f58c4411b551b3f8f693a39f15228678957e8ac631`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
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
	-	`sha256:7ecbd9b920710d4b4236d202ad3d6e87b41e11b77892e86d3d273e374e78a149`  
		Last Modified: Tue, 28 Jan 2025 08:27:50 GMT  
		Size: 7.9 MB (7899147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:615c6a45fe23aa26e191d6595276f8ac3a9e02bc51803e2986f2e49903997cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c998f8748e298829c4444176be3dc9328619a434485af6c14c55ef7f0e001d`

```dockerfile
```

-	Layers:
	-	`sha256:a114087ab77fcbd18242d3edc1875e72c9b35464cd8d5f92e614d471afa8d5b3`  
		Last Modified: Tue, 28 Jan 2025 08:27:50 GMT  
		Size: 3.7 MB (3720310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fd5363fee224897ca94dc479d410b416d80243d1ec98ef5f1230dba6714e50`  
		Last Modified: Tue, 28 Jan 2025 08:27:50 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:9c10a5d2bfd02e0fccb79c53a6ca6331c4274b1e65cbb7fe072e59e99cdbcc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120850263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c42416ff8f3c0d688a5fe3456f7f453bde404ac964f8cc03b083d9cf328398a`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=27.2.1
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
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
	-	`sha256:91e22e5078e6e98270c215f14aeb8a7323cd18a4d45f09cc84d87bbb19e9c80e`  
		Last Modified: Tue, 28 Jan 2025 08:25:52 GMT  
		Size: 7.9 MB (7898599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5632b5c79594148c27f4dc7dbcb3e9665ce0c2177a2de78ce9a20b14f7f87c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c570553378744de2052eccfd3497c2c80aa1df86dfb8d63c4506342c9d219945`

```dockerfile
```

-	Layers:
	-	`sha256:a282e227b34983123eea1ebf5e81accdaa106830e04aead061e8517c901c2997`  
		Last Modified: Tue, 28 Jan 2025 08:25:52 GMT  
		Size: 3.7 MB (3715678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f525170c89cf7f48d416edcd3ce059f27378114ac6978bf7867097bf1aee0b60`  
		Last Modified: Tue, 28 Jan 2025 08:25:52 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
