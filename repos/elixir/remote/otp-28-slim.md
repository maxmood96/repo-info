## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:cea2e59a7c2fbf523b85dcd7007c74062a3b87e28e2033f62898394b74030cee
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

### `elixir:otp-28-slim` - linux; amd64

```console
$ docker pull elixir@sha256:c0d0f14b59c17340694bb86fc65dbc8ab90f47517d17c3d50d78abbbff14ec00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136902509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aeacb797f78b567282c520a13ea1d209778ee05b3e9bc9f7f2ed7f07a32bb23`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9220377e505861009a8cd4ccdfb28dcbf5a4c23cb6f58a027f59ba4b15f946aa`  
		Last Modified: Tue, 30 Sep 2025 03:32:33 GMT  
		Size: 80.5 MB (80514588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b745b62effc50307bb8ddcc0ff734c0f8f13735b365dd3c03015058529ae498`  
		Last Modified: Tue, 30 Sep 2025 03:33:26 GMT  
		Size: 7.9 MB (7907364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c84b3d6eada4120645ac48a85de9c781fe27130da5108baede16b8c64c3e5418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6694b1a26384b5e3d59d8b30cd3523063365a51bde0013a882d41cc2f6b1872e`

```dockerfile
```

-	Layers:
	-	`sha256:996e58f9ebd094ddafa18ebbd70f4738ed0b682cd2564f72dedc54636bf1f080`  
		Last Modified: Tue, 30 Sep 2025 21:45:51 GMT  
		Size: 3.8 MB (3831894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d71c44a7fdd21d0675e0043259d6b2876aceb1825be1d9fd594548ff52fb96b`  
		Last Modified: Tue, 30 Sep 2025 21:45:52 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:87aaa31a3555f3379ab81fd9be15c895e391bedafd1febf3b3f5d779fcf2cc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121713052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a872f9797a478ea7183a21991c3578d5ef5957ca9c173117159cb6c29aa4ba`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3bf46ae00b30f7ff58d9f29a2bea5a874032476192229ba9d2bb500431eaa`  
		Last Modified: Wed, 17 Sep 2025 18:15:57 GMT  
		Size: 69.6 MB (69610263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2b29f556034b23c071fd41d8b48a19212f69dc3953e9f446ee9535b9e3512b`  
		Last Modified: Wed, 17 Sep 2025 18:41:55 GMT  
		Size: 7.9 MB (7906791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ba139252f19382a64ead5c7c9398ccdb018125e570727ac310e1ac6f59c98870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85db745ea3757c361820954eea2fc2af799a98e4a56d2ae585007dbab163384b`

```dockerfile
```

-	Layers:
	-	`sha256:7c33ef63642e15d8092563fb3ef72a50bd560d85d0c68f4b3779774495f13ebf`  
		Last Modified: Wed, 17 Sep 2025 21:46:17 GMT  
		Size: 3.8 MB (3834143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85ec06a13c098a8162a977b73016bb483f478c004ce803f3930b5f400e24597`  
		Last Modified: Wed, 17 Sep 2025 21:46:18 GMT  
		Size: 10.8 KB (10773 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:4b92eb2283663d5e5aa7ea0d5d3d802f35bcab7250997911b88fa74932d9207d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134587729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc2a63a6bb262f4d8483489eaa76b9df72dbc46c397d535b4d87e81fc015f49`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4adee6921c77ffa661747d463b4259677b46e5a99ef623c01bbb09f4561885`  
		Last Modified: Tue, 30 Sep 2025 19:01:38 GMT  
		Size: 78.3 MB (78321355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b4d0b7970d0abde2a189a269c6703af0fee4d34e21970908f3c7d3bb2a9146`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 7.9 MB (7907459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:82da5d1a37a62cdaa0850324e2bbbc0850de6e16a7cb1cb91547dad5f978496e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3c83e7441a6fdc7eb3d552b94ad1604bba30e2e30fa0b9a6a10512465c532d`

```dockerfile
```

-	Layers:
	-	`sha256:c53decc1760c401c6fe39050f80a13d083970d120bc0ba017de304387fe45c53`  
		Last Modified: Tue, 30 Sep 2025 12:45:59 GMT  
		Size: 3.8 MB (3832179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24a895166c8a4a26ef5dd76b1eb07332b13e98506131595bed4dbefea67db350`  
		Last Modified: Tue, 30 Sep 2025 12:45:59 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:cb90c7448e58d6610dc6c972339d3760d5fe988b37a550abc24077b14797d80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128098444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7f57445267ea885e6ca90e996888e22087417999fcbb9b54a5a1bcc47058f4`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cafef167ba04fe531ef557bdcb940f9e1b2f76094053a280ac6d81abce7493`  
		Last Modified: Tue, 30 Sep 2025 00:23:23 GMT  
		Size: 70.7 MB (70725028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018bd872e55db0265dc4e6bbd8325790a904404588fca894f64e5d6b2924186`  
		Last Modified: Tue, 30 Sep 2025 01:22:06 GMT  
		Size: 7.9 MB (7906765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:88e24aee5490efee5894e56c032773ffa353f8c6d7fc2e05675fb19f4990509f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c37e2635fd2a05dc6e51192f475734190e19eb76003ad5217eb4651cdabbbf`

```dockerfile
```

-	Layers:
	-	`sha256:5977bffbcf52eff7d99e4b3c5c39ce7636d73122b5e9834da231a2e30bf45a51`  
		Last Modified: Tue, 30 Sep 2025 15:45:57 GMT  
		Size: 3.8 MB (3829046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee6f37b3f4d8cb30cba7a838796d1b5b07972db97b17a81a282ee4ceea1218c`  
		Last Modified: Tue, 30 Sep 2025 15:45:58 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:32f56e0be607887f3adcdcff5e941d8433eae9c88cb11f1b01619345faf1084a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (131987061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f49651ca0ac8f08f793af9135bfdba0b4b559b261eee63fc29da9bd9b796fc`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f754154dcc788d519d9487679522fd352e20d34e40732727d53e567a1aea04`  
		Last Modified: Wed, 17 Sep 2025 18:38:34 GMT  
		Size: 71.8 MB (71752868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f667ce7703dfc09bd828f1908d2a8e1ed56f4b87b0d9f318b3bbd32df72a285`  
		Last Modified: Wed, 17 Sep 2025 18:44:40 GMT  
		Size: 7.9 MB (7907371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:1d1ddcaeb4b8f2352a4af3d098a82f8b9cbc33779ce0075893120f6f557a4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd26204cc711eaa0f94cc90eebcb1ca6699cd48b99297c6f581ccf1e9a0ed99`

```dockerfile
```

-	Layers:
	-	`sha256:8051710100b2512956950d5cbcd1941835ca2e5505eee8a72e49552d6e42798e`  
		Last Modified: Wed, 17 Sep 2025 21:46:34 GMT  
		Size: 3.8 MB (3836354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2d0b0fd768ce39c17bd5ad4be4063b0a431831d9c52d3e6673d0506e5eb2e8`  
		Last Modified: Wed, 17 Sep 2025 21:46:35 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:4916b86ef95c19a272a51b291ff671593a1260e0a8bbe79fa42558bdb6fb0c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125418497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ef014ce02bac750cd47b452d6f8f45a65015a60026c564b8ffe0c44127d63`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbad36e889f2503e370c76636a4e1b40d37d9bd28decb933da93d30ae65e81e`  
		Last Modified: Wed, 17 Sep 2025 18:21:05 GMT  
		Size: 70.4 MB (70374019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e5a40d22d200cff0a52d7d52f59430e04c96201301d96a0c39ca6176f469e`  
		Last Modified: Wed, 17 Sep 2025 18:44:53 GMT  
		Size: 7.9 MB (7906939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:17dae25369da6e9f0d93ba3e493a63ec5384eb624b91954b587ecd43fb203568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e05fff350b1ceff27a68a555cf4364472bd8ab3d6b303809ab6e20572eaf0f`

```dockerfile
```

-	Layers:
	-	`sha256:ad53b246058e67e64d4383f5431f7d0966e7af9acd883e4212cf258277d92b4b`  
		Last Modified: Wed, 17 Sep 2025 21:46:42 GMT  
		Size: 3.8 MB (3828722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0585d2bfa413d9e9d912ad72f59309912b4b1fa0faccdfd08f08ab6e2cc62a`  
		Last Modified: Wed, 17 Sep 2025 21:46:44 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json
