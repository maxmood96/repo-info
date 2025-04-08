## `elixir:slim`

```console
$ docker pull elixir@sha256:c64d63f23445c645468237c72dbfea01c6b3183044bc97e80f4e8261f92927ec
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
$ docker pull elixir@sha256:bc0e0a776bf0e533851de8b5f755840154ef03cd79c2c8f43078705ecc5b5bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132344357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3585d48c420328e621596065a407ec239bab32ac82eb4c916b8ac85c3c5b42`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8e5e3d2e23b1c6aa690212df9e992f7753db4265d401632e66642974e3892`  
		Last Modified: Tue, 08 Apr 2025 01:27:56 GMT  
		Size: 75.9 MB (75935127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfcda0e5f89a2901be81f1e5f47d4756c9a1e65cc9f53fd6b1e1e1eaf89ffbb`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 7.9 MB (7918689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:793df15281ccdecb7247202c2c3ac6aecb6b26ed5841f78e249ef899990f4010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b44ec911ef69c8d8eddbb00f106a8b476a2e2f17bb0fdcaf2d557124db199`

```dockerfile
```

-	Layers:
	-	`sha256:59b20a39969ffc9862a66e0bc627c6d714c9e082cd714c461216869e0e425edf`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 3.7 MB (3717334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4a1ca3d342169ed9d98a649328cf529690aece62e0eff4c7797eb3db14d8e1`  
		Last Modified: Tue, 08 Apr 2025 02:23:39 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7853650314f27aad6779e6a1e0e63d9467ef87bf39a5c851af7d8aead37df803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117162199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee7571bfbc6bb7401800aa23e94cf8d7194fcc4f691bd30506a1c412e849016`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09e9840ee4e933bdc138ab0eb333a2797ee164b9055febc1452921e9a67868a`  
		Last Modified: Tue, 18 Mar 2025 05:39:31 GMT  
		Size: 65.1 MB (65066128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb72e8aa29436ab5b59eec298339502151beaacf35025b7592ac101bad84a8b4`  
		Last Modified: Tue, 18 Mar 2025 11:38:57 GMT  
		Size: 7.9 MB (7918068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:73936d914d31c4ee78e6451c038c57b7567b4caf601deeb2d458bbf6bcac6112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d6ef7af7fb4f66468c545dcc73a8e3314031b56491f7646f930351891bcc2`

```dockerfile
```

-	Layers:
	-	`sha256:2ad7c4870b5c6c6d80958d61c82ad1520d6172892b17a6fb832b47122bdf64e2`  
		Last Modified: Tue, 18 Mar 2025 11:38:57 GMT  
		Size: 3.7 MB (3718247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f70ec234876eb9a02748e14cfc28bfc79727999c5b1aec51a052b302eeb646`  
		Last Modified: Tue, 18 Mar 2025 11:38:56 GMT  
		Size: 10.8 KB (10769 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:383e1baf6dc919d8eb96bdc3c6c73ea14be1270bf27482050f23c6e5a8beab06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129894940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7b107752773105bdace7f3ae408e7057be3761bec9a0b91ac1915270373591`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5c56263566121e78c0ecab5e12b79ef870d7e5887914f3bdc6b429c3b9d2f`  
		Last Modified: Tue, 18 Mar 2025 05:24:42 GMT  
		Size: 73.7 MB (73671328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dff3dd932ad330afc8149c4fc901cc1111da9d83bc8033ae4b04469c029438`  
		Last Modified: Tue, 18 Mar 2025 10:53:04 GMT  
		Size: 7.9 MB (7918757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:47acf05ffa33cd02d39b7abba8ca283253d2cb546f72a0494defb04c99046afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fa04f8809d5db45c5af1f1cab4dc854c3e9c392cbb2d3c7870e4a16ab0626f`

```dockerfile
```

-	Layers:
	-	`sha256:500e963dd4fcd38c95ebf8ef53003b6ed941017a844b5b2cfe999d6098495704`  
		Last Modified: Tue, 18 Mar 2025 10:53:04 GMT  
		Size: 3.7 MB (3716283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55604743a8065c5b0baad69126e22129f55b4a590d67d8fd2803259f7d4b0b4f`  
		Last Modified: Tue, 18 Mar 2025 10:53:03 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:b9f78f0616491f063e26841715c5b48e8dc0ae930dfb4c878653d87a3a2ae8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123487571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1a6641ac2e1eea6a580d38ac9afc1430013d3cd2ba84d11a9169b18aba6c17`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067512c6ec142a8007b9f3374a3cf7bf1b1e943c2c5b9cd718755693e1e3207`  
		Last Modified: Tue, 08 Apr 2025 01:27:04 GMT  
		Size: 66.1 MB (66091109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbe475aeea276055c08e3f63d009b91b11563bce0371d2aff622b092aabe0f4`  
		Last Modified: Tue, 08 Apr 2025 02:21:24 GMT  
		Size: 7.9 MB (7918331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:657baeb64cf00d78842aeaba1edc27cec8a1a8798d4fb26ca9e8b6bc4f30d047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a15134424e6703be0008a8e4752c5b977818e12303de82a5e22e081dfbcc9`

```dockerfile
```

-	Layers:
	-	`sha256:cc2a50565889943cdd482eb1e745a6e7dfc98674ef3dff8e9cf65d0f4532f473`  
		Last Modified: Tue, 08 Apr 2025 02:21:24 GMT  
		Size: 3.7 MB (3714444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e0b385b7d813d4aa9fc560b019fdf60f6209fc4f1311afb2e7393e5a03bf77`  
		Last Modified: Tue, 08 Apr 2025 02:21:23 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:18fbde6764036c06dce3dd2a440b893e0c826393d62fb9d44fc6db6ae64260a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127422730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72954f1037b0c855d57de9a6623f3582331d6ab70b78c62409e3253411699da6`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2a3ccdec65f0f6ffbcfb9e96474da30351e877c3990172a0421bac8c00c246`  
		Last Modified: Tue, 08 Apr 2025 04:41:25 GMT  
		Size: 67.2 MB (67172038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b348ac44b73255f9f3500101af52b6cc23f7773e152e1e81252bc78aa0f841`  
		Last Modified: Tue, 08 Apr 2025 14:58:13 GMT  
		Size: 7.9 MB (7919046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:28f56f3566d194f2262ca52484072df984d0741915e65be6f1813cb611179bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39feba1e47a14ad9787920a8c23e23f10637449ab896a216e514e75c72729ed`

```dockerfile
```

-	Layers:
	-	`sha256:d8f923707fdfe136c737f9dfada125c17dcd26bbf941f97c6728e0847fb0a4b3`  
		Last Modified: Tue, 08 Apr 2025 14:58:12 GMT  
		Size: 3.7 MB (3721686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b538a5b0a80ab003e34595c4840b7373efd9de35bfe0e7d66e14f1ec589b23be`  
		Last Modified: Tue, 08 Apr 2025 14:58:11 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:ca66efbc016e574ea5edecaff5b42634b612e85e30181def74e90414681cd38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120913945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc15347a6d75a1b4e4ac1268a8c1af14e4aa8a4536cb983c52b73c92d685b39a`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 11 Mar 2025 02:46:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:46:17 GMT
ENV OTP_VERSION=27.3 REBAR3_VERSION=3.24.0
# Tue, 11 Mar 2025 02:46:17 GMT
LABEL org.opencontainers.image.version=27.3
# Tue, 11 Mar 2025 02:46:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="efe76126938f237c0d3a0e2e8753c5cb823235d4d53708833bbc0968d76c39b8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:46:17 GMT
CMD ["erl"]
# Sun, 16 Mar 2025 23:57:04 GMT
ENV ELIXIR_VERSION=v1.18.3 LANG=C.UTF-8
# Sun, 16 Mar 2025 23:57:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f8d4376311058dd9a78ed365fa1df9fd1b22d2468c587e3f0f4fb320283a1ed7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Mar 2025 23:57:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b1858e2ced80810baa4b25a035901e3476501afb5625be66d3b35ae19c1054`  
		Last Modified: Tue, 08 Apr 2025 03:53:05 GMT  
		Size: 65.8 MB (65844668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a44103b749c720da23e6b08098b00a29db538541fc8cb7f76b6311dfbbf140b`  
		Last Modified: Tue, 08 Apr 2025 09:20:41 GMT  
		Size: 7.9 MB (7918281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:7a4aca96debb8a01accb803bb3ac28166caefdf05603d6a08ff06b6073c1c5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb1491ecb4a0460d96f1a007a47c459eb899a859e61ca2588d760970fbb00e4`

```dockerfile
```

-	Layers:
	-	`sha256:988ac57758058905d245cadec918a9b3a3ad9d3c6cb8c4619d1f0dae34d6fc9e`  
		Last Modified: Tue, 08 Apr 2025 09:20:41 GMT  
		Size: 3.7 MB (3717054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcef64da570055c01514a8bf7c671e32a707d6d7b9f3cf7e5691ffaac76914c`  
		Last Modified: Tue, 08 Apr 2025 09:20:41 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json
