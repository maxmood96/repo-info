## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:72a6bd509097d6ff489affd1e9b93114f987d2ad88c3b1668b65b136ce219f76
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

### `elixir:otp-26-slim` - linux; amd64

```console
$ docker pull elixir@sha256:a9a1c3bb119539d478867d7be2e81ef9c2cd0d406fa3f0dea11876d20951f602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126764810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acc2d3d0b29da90258885aa99dda67b849dde2a345c6c02df15b46dd2c64be3`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5314c9a3121779a1488294e4ed34172b18f8663fcc273602e92d12f9c6b6c7e2`  
		Last Modified: Tue, 25 Feb 2025 02:20:30 GMT  
		Size: 70.4 MB (70378778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9247431c200d0c596a1b9f002a9d9ef0426af4e1a9247b4e2cd05d79d442c8f`  
		Last Modified: Tue, 25 Feb 2025 03:20:18 GMT  
		Size: 7.9 MB (7909932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:d780a4de9cde19bc91950efd7ddd81ea3313a55bab97098d5349fcf03be4f91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832a6530955341591232c7628f2f76669c004c68f6184545c64978e7766f8eae`

```dockerfile
```

-	Layers:
	-	`sha256:c1dab8f4cfee7085a8f3f6a1a7291b68d932a362fb312de00314ef3b3f525414`  
		Last Modified: Tue, 25 Feb 2025 03:20:18 GMT  
		Size: 3.7 MB (3667268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828e61467a3f3a87a891bfbdfeaa01d2fe806ac70d3bba0aa0fc98ddc34637bc`  
		Last Modified: Tue, 25 Feb 2025 03:20:18 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7444cc4b2058ce6ab22dd25c7bd6ee05cc18dea2387af263418efe7be596af90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112209370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e24014c2323b5e725d06a5c980f9353fda9061a4b10b1c5e484621eaa7463f`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70bbd2ce8ef0453e9e4e5ecfdb57f4a28ee3d6ead7c36b49b30f2eb0b0d0f9b`  
		Last Modified: Tue, 04 Feb 2025 11:09:45 GMT  
		Size: 60.1 MB (60115833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764a94b4f0c42cdb13604fba87b0c6fd5897467dc31f3aeae3fd389cdf3b99e`  
		Last Modified: Mon, 10 Feb 2025 19:47:20 GMT  
		Size: 7.9 MB (7909485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:80142446fc46e5216695957a30e1c386c24283ccd5f78b5834cec5dcfd0f1476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5410d996962d93af1eb1a6b1c5883b947893a72541cea8a318430563abf5ce25`

```dockerfile
```

-	Layers:
	-	`sha256:8d71ec4a3cf4fde3c19af5676f45c3cb5c655e28a22f221262133d21727def4a`  
		Last Modified: Mon, 10 Feb 2025 19:47:20 GMT  
		Size: 3.7 MB (3718605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba974f51783d956c9a4b9e51ae055eaaf49e66267b7a23e873cd99fcf73f3ef`  
		Last Modified: Mon, 10 Feb 2025 19:47:19 GMT  
		Size: 9.9 KB (9856 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:68dec04fd2da053bcef536c4937feb879e4bb44544dd61fb360a4fa234d08d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124227294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6d7b416930523d3ea9af1cd1bb4abef0055908c3086ba3556494c786667e28`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb069c1d4f6aead75ea3b58a95af029e93fec8bee9d5a75bb6e388a3a3ec111`  
		Last Modified: Tue, 04 Feb 2025 09:33:57 GMT  
		Size: 68.0 MB (68010746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40f52db1f6f32bc0726472d313f213c16d738b06ddb1865fe355431035234a2`  
		Last Modified: Mon, 10 Feb 2025 20:10:30 GMT  
		Size: 7.9 MB (7909995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:38b6f18a54dcf81e75c3166a5d2e8765f0aa753a20461faf5e2d8af2dcb02ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f6ec006fc2c07a04c32e276113cdc6960cc799be3e8018d4482e4c02799d8`

```dockerfile
```

-	Layers:
	-	`sha256:f482c0ff2f895d8ed1c914135fbabb641440e0d2c71056cf41416fadfa867ae9`  
		Last Modified: Mon, 10 Feb 2025 20:10:30 GMT  
		Size: 3.7 MB (3716629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59c5708ab1c8bf1a6b8962b9b0f9bb9a1a7085a2f7104c6ae064a8ef4a4d4a2`  
		Last Modified: Mon, 10 Feb 2025 20:10:30 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:9b37761bd30fa3bd2cab650356b8b3eb8dc3085f337a7884d1bf98d6246c8826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118483484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdcadc50c0cc0d1b7425b4413ea43e67356821e61503641724e57247016b2fe`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020a483d3874b442753b6620ef593290390d8300dce7d4a341d6dbb77714010b`  
		Last Modified: Tue, 25 Feb 2025 02:31:59 GMT  
		Size: 61.1 MB (61115500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f77c97e800cffb27edc35a905fe84f55d93ff1ac0a8f0c989dcfd3ce35ff823`  
		Last Modified: Tue, 25 Feb 2025 03:16:19 GMT  
		Size: 7.9 MB (7909532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3d8e7df2876b0b451d6488db154d7c0dc25837a1d27b70885dcc253055f85b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bab859eca9a41b67d177474190f1aa1d10e64d567aa03e7274c1faa11a1b44`

```dockerfile
```

-	Layers:
	-	`sha256:0dca6919ba76c8eede4accc221a57fd65ab3725d8c3fa2550dba11702f7771f0`  
		Last Modified: Tue, 25 Feb 2025 03:16:19 GMT  
		Size: 3.7 MB (3664393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:683aa3c7d9699c00316190d2b64476b73186d1e5d867ea4fa3d4cc936e872a85`  
		Last Modified: Tue, 25 Feb 2025 03:16:19 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:a2a12b204b6311509d0d21450a8e4bbfcaf0a95f0d86bff1e49ec230ba243bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122426135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ce36f84188ce321cc6ae22d19e389a5f6ff998c5033eb34815ecb81aec90d2`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90015fc47d58fe5097058da13df7f48cf422b813e9689192ea9e89d96a08c120`  
		Last Modified: Tue, 04 Feb 2025 08:02:50 GMT  
		Size: 62.2 MB (62202997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765719b86222b4b91ecd67579f7483ce363c5059b9bb999c7b03d100694a6a8d`  
		Last Modified: Mon, 10 Feb 2025 20:03:12 GMT  
		Size: 7.9 MB (7910281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ad689b35242dd8a7591b6a539706373541737fd08a39c9d6287d02521866bd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7a03690e612c72ac47d42e44a4e2ee268c872a708af8bde802505720aa993d`

```dockerfile
```

-	Layers:
	-	`sha256:6ea17e3eca76a811fe0e88228cf52e83825ed4026d9ff89ae43879263b425342`  
		Last Modified: Mon, 10 Feb 2025 20:03:11 GMT  
		Size: 3.7 MB (3720714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:208018916aefa5dffe098d701ca76eef4b64676e1e0841327a315e365de39f6f`  
		Last Modified: Mon, 10 Feb 2025 20:03:11 GMT  
		Size: 9.8 KB (9826 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:a7b454dcddcbe62b8ec7655268f8d47bf9a17be3bf61a6e345720f71f3e14608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115954671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cae35b6750864e9afebf3714e68ea71b3c235f382e4bf75cb0a4267bab04bbf`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00556d019f4fd78061c2fa51dedefb339279308932d5712df529b4e2238088ad`  
		Last Modified: Tue, 04 Feb 2025 08:11:21 GMT  
		Size: 60.9 MB (60913397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f1294edbbb4f268a6696529e505e3932eff2ec493b817b762e2a2e82994aa5`  
		Last Modified: Mon, 10 Feb 2025 19:40:15 GMT  
		Size: 7.9 MB (7909782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bfe27989ef6e7557e54d9e95e5ed5a537f2bab4a231baf77892726842480ef7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8976453ffd3c670eadd93567ca2b24ce80a72f8ad4aa944873e33b1324c03640`

```dockerfile
```

-	Layers:
	-	`sha256:c786f14f4cda8832e410e0cf00d0a335c841604f21c1dd7469de038e2c324174`  
		Last Modified: Mon, 10 Feb 2025 19:40:15 GMT  
		Size: 3.7 MB (3716100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b001843c4b6cca402e7dbc25604c8161313e84afd51eed249e232cbecf1f2d`  
		Last Modified: Mon, 10 Feb 2025 19:40:15 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.in-toto+json
