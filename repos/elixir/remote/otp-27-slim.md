## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:33c83af4af1906d62be44f0bb304ca69c1d42c6724116b748477f9141af6a680
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

### `elixir:otp-27-slim` - linux; amd64

```console
$ docker pull elixir@sha256:6074ee5ab0b41971a91b462df123167c30d54c6a115ee72602f6c8b670c8c5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131736863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef868c08d0b8f8a554fa34320bf2cd8a7f442b808697a4d6054bae71f227f7c1`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69f955e52d6a4567ff93630bf5853c8ff1a7465d11392965172f49221218b8`  
		Last Modified: Tue, 03 Dec 2024 02:38:52 GMT  
		Size: 75.9 MB (75879652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0305c7038b57fb09d7205b2dea6df0560db473d1588e08295fab31bc40b5659`  
		Last Modified: Tue, 03 Dec 2024 03:26:29 GMT  
		Size: 7.4 MB (7360001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:b382ec2d62c1ab4694af9b2a286d82a99a156c3a17110c09a959cbb21fe1db5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acc7ba91f6ba13f3b86bc09d8a40ac7cd445a0b54acbf5e4724a4aaf4760190`

```dockerfile
```

-	Layers:
	-	`sha256:ea451bc48d3d2417c1f564e990926919730827bb14703cfbf0b1caff11daa586`  
		Last Modified: Tue, 03 Dec 2024 03:26:28 GMT  
		Size: 3.7 MB (3719131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e809180b93ed91e11b39e406c4cecbdcc775a947e5c0ff03f2c59d0883b57f7`  
		Last Modified: Tue, 03 Dec 2024 03:26:28 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:dd428af90b1a443df1ca6547bf4c7ba49610d01db51a18f4a7eaf8ee32fb8610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117511887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebc809a6c37725448b1cf04cf3bbe95e82f4329eecb71ea9bac58943e869269`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29df1723d97898ba2c8df5dff636cef95655243e85533cd9e995a49a35d277a`  
		Last Modified: Tue, 12 Nov 2024 16:17:31 GMT  
		Size: 65.0 MB (65001938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fc37a551908ae678c1cb79b4632df75bae76bd10790a53eca33daf429d90b8`  
		Last Modified: Wed, 13 Nov 2024 10:46:04 GMT  
		Size: 7.4 MB (7359386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a8ad562410b4e5c1a020c73b0d1fe3d2a6cb454a120a3a8a8d0489ddb76f9197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654d94de5d9df2e11399b843fd29f782cc646a51d36ab9df58dc1d9acce3519a`

```dockerfile
```

-	Layers:
	-	`sha256:7e09fc2033c3ac2c9d886a92dd68b180a4824b813fff77819d0e120d9666d5d8`  
		Last Modified: Wed, 13 Nov 2024 10:46:04 GMT  
		Size: 3.7 MB (3722627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac7a78cba6be971f557aee25a5e56fb345c301c408f9f9467f22517139f5d41`  
		Last Modified: Wed, 13 Nov 2024 10:46:04 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:43a2ea1851d8d4759bbc4be3a2224eb44cedab5329909a6ccafed9c74cdba737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130552965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494810c094b630846b73dc801952598cf868762f1d4fcc3b85be0f87508d07ef`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1723baaa1204f6a15d34f1c261430fdf95ab184f397eb227b090c63e4719186`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 73.6 MB (73605808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad9296c009658dd651986810811ece0773fb5fda898360829236a203116460e`  
		Last Modified: Wed, 13 Nov 2024 06:35:17 GMT  
		Size: 7.4 MB (7359956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:1ae06a8d6a7d0f04cdd141a5d04f676debbe6e83e6b09ef052678074dddb603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d5314737ce90f6d73ade53a1ec8d94990d6f836a3fe5b3d2bc709d12851c60`

```dockerfile
```

-	Layers:
	-	`sha256:c760dc623f28ed2f8c76ee7c63849faa211a27759e2caed4eb1ce8269334fdca`  
		Last Modified: Wed, 13 Nov 2024 06:35:17 GMT  
		Size: 3.7 MB (3720663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0beffe1acd570d50e358256493e8579955ee61a56eaf6b48fe5bfedd30507375`  
		Last Modified: Wed, 13 Nov 2024 06:35:16 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:9fa266657dc06ae5ba95642d80c27ad1641acf3cdcb5bbd21ce1f9d4dc2eb0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122872514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495636c30f4a36b54a7346d13e9456ab309f17272a7615b36c70ce972cc71060`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584e4d6050740d9d05f9206daf654540d8cbf4afaa6a44c6bcb50fc1e7d6acb`  
		Last Modified: Tue, 03 Dec 2024 02:22:07 GMT  
		Size: 66.0 MB (66036812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757fb02006bd3b6a32ebd37c74d0a3735aaeb2ea1af7f66730574b2510156188`  
		Last Modified: Tue, 03 Dec 2024 03:19:24 GMT  
		Size: 7.4 MB (7359550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3ebcb549a54a2057a400be1cba2a3c982e6725b6335fc24c5b4df40dbedc7c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b2495d7bbe667ff4ad59d292e9deed51eb4c629ffd4be9b467e445ae8a5772`

```dockerfile
```

-	Layers:
	-	`sha256:2117559d0c6a4aeb02833a33eab34f7ce9a14ee8fb64a3437fbdd325306f7b3d`  
		Last Modified: Tue, 03 Dec 2024 03:19:24 GMT  
		Size: 3.7 MB (3716240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dfd0cb356ce2764bca23b2158403b8fab095e40d31e9fd79ac0792468d80209`  
		Last Modified: Tue, 03 Dec 2024 03:19:24 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:03c93bb0a52a2f57c710de7a5c54decf2aef2b3a74bde49eb98c8ef3ce7e90f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128025787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62117b720c59f507fa264840390bc6b9de771340d62c3c682223370a91c5f43`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9c8f7ad904cf966e86f8f2c06e1841cb937e105bbc5a6d7d76f12fc17a45d5`  
		Last Modified: Tue, 12 Nov 2024 08:39:26 GMT  
		Size: 67.1 MB (67110464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6347923fd18ddfe5b33c7ccd4282b0f634001dd051d9428877b22a3772d1b43c`  
		Last Modified: Tue, 12 Nov 2024 22:33:44 GMT  
		Size: 7.4 MB (7360053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f31ca195216c4201bb0c95c075f75756f976b161308d239308c06970ae6e732e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c340d1e1aff2b5f48115695e96b785b0cac276af5e59d16a609f0bfc9311af`

```dockerfile
```

-	Layers:
	-	`sha256:d79cd2b49bcd6d8568fcdd47e8481cdfac9658e669c94711ec9c40e0b6b03878`  
		Last Modified: Tue, 12 Nov 2024 22:33:44 GMT  
		Size: 3.7 MB (3724730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b1e480c9f6ba84f27880bf8b0fc2819a6bf6706803aba535c4dd4e6349d5d5`  
		Last Modified: Tue, 12 Nov 2024 22:33:43 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:b1c25f88265797119b43062ed87834fff02a5fb5f440d8af6e33d67b19954895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121089635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc2a96438892c8ac642ff5d6acea9169bee382e1227b1b0081691850ebc185c`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=27.1.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7e45090eb251efee0f32036939fc85bf190395036f110142e4c817ec76ef36`  
		Last Modified: Tue, 12 Nov 2024 09:14:48 GMT  
		Size: 65.8 MB (65791753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0452aad53e7fe19c5125773ff4cd488d1a46e0da16b0f478971021e6181611`  
		Last Modified: Wed, 13 Nov 2024 02:01:22 GMT  
		Size: 7.4 MB (7359194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a99a465af47166aaa16e424307fd5850b657b61bb6cbec0cc2e87e3421b24303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6856e009689e279ac7ffaeac7a58d8ebddcae868bca91966aee5a8ca1b304ac3`

```dockerfile
```

-	Layers:
	-	`sha256:bd96b4b9eb6143a9aa3e827095b161ad96e700dcae3a3dfdfcf3df720033f194`  
		Last Modified: Wed, 13 Nov 2024 02:01:22 GMT  
		Size: 3.7 MB (3720100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a9401646195e811ca0ad5e01302627289535460f75ef0f0eb1ce399ae43e05`  
		Last Modified: Wed, 13 Nov 2024 02:01:21 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
