## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:5df004dd1f015dc3520f638369fcec2e3f2efd10bb859084384156e45899254a
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
$ docker pull elixir@sha256:f6d0bf2e3e243635859513cd6345a6bb50a4a2c1ccd42b902a16defec32fe3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126190670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714e2c60aabf203d10ad90dcca3551ff72601027e0d6e7692a82e34bd2429f0`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de85552e2280313a4b344aafb4679a335319b68c81732b638a326e2426cb57f`  
		Last Modified: Tue, 24 Dec 2024 22:33:59 GMT  
		Size: 70.3 MB (70334542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef345b5410a2673450325d74521cddb0625a7be6eceacc519b8fab626ed4747`  
		Last Modified: Tue, 24 Dec 2024 23:22:43 GMT  
		Size: 7.4 MB (7359062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e64cf1b179720f4cda538db4abb6c8c77c01373f37799d3d18fe30632c0c27e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2835ec036d61c0042b81a656a8bc4e3836657923b007300e85a1d7d7f739b35e`

```dockerfile
```

-	Layers:
	-	`sha256:60a2724b6081344fd2c8c6eeae0e710c5bd9ab86a462c13d75299c82af29001c`  
		Last Modified: Tue, 24 Dec 2024 23:22:43 GMT  
		Size: 3.7 MB (3716338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8cb7b0592f775ed551d7c03799872d8d93607371e03f515f960cfa0f031362`  
		Last Modified: Tue, 24 Dec 2024 23:22:43 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:ffb9cb772ea483b2b24a8f6dad2c4998c9f4af53c7fb4afeb8c5dd2d41c7d678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111621182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65981ce49067af9daf3596f2d3d8010c9748072f8113f362d4a140ff326d38`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c70acc66176e05442b60e263cbd8610e9ef00b63862971ba86c9a22cfc9ba7e`  
		Last Modified: Tue, 03 Dec 2024 08:00:29 GMT  
		Size: 60.1 MB (60062690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bd39fc25067856004e8af7d940e0bbf972706a366f8115c73d1eb4b292f8db`  
		Last Modified: Tue, 03 Dec 2024 19:16:19 GMT  
		Size: 7.4 MB (7358383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9f40bdfc83c2459cfadcb0660844942c919ab343fd7aa9d1e3a80024af1289a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657af187c8f5190c3796ef1aa0687fc46af4c8fbce4deb2bc71f1f92dbc9fff3`

```dockerfile
```

-	Layers:
	-	`sha256:9ab2cdf6e777a7651c876d77ab5dd5a801022f7cf89ca0b70e1fcf3b84ab4af1`  
		Last Modified: Tue, 03 Dec 2024 19:16:19 GMT  
		Size: 3.7 MB (3721732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e02de64b70e4c35767954ab6783a9df0b0a17143eb7080c6bd272076e57d4b`  
		Last Modified: Tue, 03 Dec 2024 19:16:19 GMT  
		Size: 9.9 KB (9857 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:7746c57e0e3f146e155c5d6747ffab70739341fcd2dd70c0c47f0d6fd916a186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123652245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5255d95fd71862ce95e9460ac66828691cad8448949f047fb6e02596022a33e8`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43bf59b125105e1cd69f2dfd8a490c1fe920e94085154bae98a41a43c678929`  
		Last Modified: Wed, 25 Dec 2024 02:05:20 GMT  
		Size: 68.0 MB (67967804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623f875ddd2a05ebccdaceb127ff05e0fad6a0c7ac8e5cb3da63d34e35c2eff`  
		Last Modified: Wed, 25 Dec 2024 10:39:00 GMT  
		Size: 7.4 MB (7358957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:fc4254ed8e1798889cf55567a53c972a57d2d3d3db036658ab193c479c63bed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df9bf1f9ffc91e9f0981c5a6dccdab2114e018da1b3ac96c9ab378abf3ce797`

```dockerfile
```

-	Layers:
	-	`sha256:84055071cfd8cf39682d34a4ff497c9a6650563f9b265f0fcc07a5ff9c0d3194`  
		Last Modified: Wed, 25 Dec 2024 10:39:00 GMT  
		Size: 3.7 MB (3716587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c066109536bbadf8037752e26e6409086af61afc3d02478d0c276ca03ca53ca`  
		Last Modified: Wed, 25 Dec 2024 10:39:00 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:7ad662c0efa6481ca5d612f3697c0817d8d8e267c1d01f43d7a37b33db652aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117916635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149f35472e3827271ae429da7628a4bd461c2b6968c4aa35934cfe3c80b92a1d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca44d1694041f067ebf8d5b4f893979eacee074bbacec58ae6385ba43f6332c`  
		Last Modified: Tue, 24 Dec 2024 22:22:09 GMT  
		Size: 61.1 MB (61082179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f6bedd06540304ffc716a6fc213dd8d256346360297dc35b1b3bef961c4f8e`  
		Last Modified: Tue, 24 Dec 2024 23:18:45 GMT  
		Size: 7.4 MB (7358531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e3ca434c1177d7bbb882be11518b5fb31e075850c10d8aede7d8bf69cacddcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9c3579343b99116d4d5152bcde8721200e5182d38cd221badddd6c693239bc`

```dockerfile
```

-	Layers:
	-	`sha256:6c605b1fda96d818f53d4f366aa51746ba834e414991a0099d5bf1c7b33b4b4c`  
		Last Modified: Tue, 24 Dec 2024 23:18:45 GMT  
		Size: 3.7 MB (3713463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219fae34b332565b71c9ce2a8e1595e976f9908e279fd64747d656b8bf6703e0`  
		Last Modified: Tue, 24 Dec 2024 23:18:45 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:77444545c8a9534f05277f24c3a7b0ff979c477b70a29dacfca13269ea49114c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121845193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5f6fd85e6ad08a9735013d25321df2932ef16143c159ba3f2759bc353d6a3d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792592def20f71e601a070e37bffe2a44dac21adf39ef56bc23d49eb3add0b58`  
		Last Modified: Tue, 03 Dec 2024 05:08:54 GMT  
		Size: 62.2 MB (62157820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb531eb76c8a0f7383730103a923938d2465ace5cef94dc9a1fcd0a643f74fe`  
		Last Modified: Tue, 03 Dec 2024 15:38:02 GMT  
		Size: 7.4 MB (7359151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c7eedf117dcb1d101400c61670267865cfceb6d8a9f8ab00fd853c4b93157a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c23c0d87ba23d4930f6b822c71ce7683bc4b90210714704f9275e5b0eae150`

```dockerfile
```

-	Layers:
	-	`sha256:5e3d8ca10cc4ff9ae1388c2d0df3895683ddca58911238c5a1cb79ac5e2d11a8`  
		Last Modified: Tue, 03 Dec 2024 15:38:02 GMT  
		Size: 3.7 MB (3723841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ee3f05b093a3834659a44ae4241c8831b4c619446dcc1c696136dbe163f463`  
		Last Modified: Tue, 03 Dec 2024 15:38:01 GMT  
		Size: 9.8 KB (9827 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:ebafe60449015dad3ba33e329ac26e6a42f28802ca3546b72ed3ef9e2f221568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115374453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae91ed04934ec189742782aa6cbc7a08e6be7b4ef6d4b4a39cd91bfb6f6f342c`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 01 Oct 2024 10:39:24 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Tue, 01 Oct 2024 10:39:24 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.24.0
# Tue, 01 Oct 2024 10:39:24 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916390e7fbffcb8b07a7fb2db15e99e02a4f0877ead918a47deaa75a606cd480`  
		Last Modified: Wed, 25 Dec 2024 00:35:19 GMT  
		Size: 60.9 MB (60866295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38352d28856ba1bc4e6772b0efb800b277706fef71dd95949312215516b7ea04`  
		Last Modified: Wed, 25 Dec 2024 04:51:20 GMT  
		Size: 7.4 MB (7358533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:39c9beb5eb24736bbaa31c53221c8eaf0a9ffd48b0e9eb9d7a8e9b3165b50942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47f198a46b7f0ee592d3d71ee255d97268d7cd4a7696269f0c4c18e0f3a4499`

```dockerfile
```

-	Layers:
	-	`sha256:a2055f33e6623aa6e26541507b25969290d4897399f0ffe4704d3a3784c0d0bd`  
		Last Modified: Wed, 25 Dec 2024 04:51:20 GMT  
		Size: 3.7 MB (3716058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97a17da3d76b71ed3ce876794c8bb0b536ddeebdcbc8a8f2c2dcc1c55c7dbf2`  
		Last Modified: Wed, 25 Dec 2024 04:51:20 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
