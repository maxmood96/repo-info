## `elixir:otp-24-slim`

```console
$ docker pull elixir@sha256:a0676d64bc0bf29759ac4b6d13d3506b23739d9d58c1ecba777b8ae9d005985d
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

### `elixir:otp-24-slim` - linux; amd64

```console
$ docker pull elixir@sha256:d9248da31fd20be0b9ca79ec035c1dd023be67bcaf455be7386b91baecf77fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127598436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6086585d699a5553ffb850e034ea9bd381e2164d43742de3af9b0a800334391`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969853e6b6ca8f9e2ba91faca33275202096d2340989601ed756712163ea2c94`  
		Last Modified: Tue, 12 Mar 2024 08:53:19 GMT  
		Size: 65.2 MB (65224149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86659428e1e39882ad207950c8f74fae0aa64db5106c1c8b8f7853231e00398d`  
		Last Modified: Tue, 12 Mar 2024 09:56:48 GMT  
		Size: 7.3 MB (7289318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f2066e60823fdefff2f2d419a658ef4f7016b80642848b74cb04380b5a4847e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fa4f1eb9b47e31110e0179f8b1720234c304d0fcbbe7a6495fe2a32d4e9191`

```dockerfile
```

-	Layers:
	-	`sha256:4ada16a3eb607896c0da3d0b2682ac9631ff823682c308d353b109bce5583e6e`  
		Last Modified: Tue, 12 Mar 2024 09:56:48 GMT  
		Size: 4.0 MB (3958482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcab961624558ece12f392be6c238bd5a57ea94d8e2fbc10faf3aeb79af7f371`  
		Last Modified: Tue, 12 Mar 2024 09:56:48 GMT  
		Size: 9.8 KB (9845 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:83943683e326017d387f5c3d54954a140a14f93092436aa2d811b9f85b56e925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114735646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c6562366f53c4f2975b6faad8f43e7f3fbd3b9c6f22cb3d9e0e9f6cdea73dc`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d4d8bf06dadf1f63b2247125a87fc56580a6ce106cc3940ba012512e5f9eae`  
		Last Modified: Tue, 12 Mar 2024 02:07:54 GMT  
		Size: 57.2 MB (57205296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a616b3ea131144bd0ce7b7e4d8803c12184ea3070dc177141bcf00e24b3a0f`  
		Last Modified: Tue, 12 Mar 2024 14:59:11 GMT  
		Size: 7.3 MB (7288908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:eb79f17a79258c415fbe4fb9cf2107b7fc9060a8e5c24e654ef29658415ba915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b75b99fbf5d96f55593ac71c32b17494bea6b5b2b7bf99ace8b73722161b04`

```dockerfile
```

-	Layers:
	-	`sha256:f96b647e1d34e43e363f5aeb063e433efb0896b50798b803c72ae71644d74c88`  
		Last Modified: Tue, 12 Mar 2024 14:59:10 GMT  
		Size: 4.0 MB (3960075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a509cf31bdfbc0daf43339383e6624904c58232eb029cbf773e7b8f27b40d74b`  
		Last Modified: Tue, 12 Mar 2024 14:59:10 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a1c97dbcc2504d778dab4da79b820ef62efffabed0fc47599786138aabf3bf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119060990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9777ab5c9b91b1f98f195871db06bd3b2c900053f0dccaebe2cde081c2f9420e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308e30f5ac3636cfaa8642e5dd50cc1e880bac3749d8af7d97f3cd2f8414d944`  
		Last Modified: Tue, 12 Mar 2024 04:08:43 GMT  
		Size: 58.0 MB (58049790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c579627f5b93c4f9f8c3020044bddd710f5c9cb9d26f9d780c7d38169ba29`  
		Last Modified: Tue, 12 Mar 2024 15:48:08 GMT  
		Size: 7.3 MB (7289101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:be64fd40013b9c05cfcce137e2d81cea7aa311c0a1ac905e23dcd441d450c863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b6bf58e564963b11b6d1facbd4f92ad224d62c2951529cf544e5aaece7e51`

```dockerfile
```

-	Layers:
	-	`sha256:70ca25aa5948b6b5d20120d25a750e1e2ac86ecd04f4b376df1dc76952668962`  
		Last Modified: Tue, 12 Mar 2024 15:48:07 GMT  
		Size: 4.0 MB (3958056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7210061752d439a908e13f7f67778a45efacdd83314069e2fd401755b207c0df`  
		Last Modified: Tue, 12 Mar 2024 15:48:07 GMT  
		Size: 9.9 KB (9853 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; 386

```console
$ docker pull elixir@sha256:0ffaf8ac75b66b34968e00ec54fa99654e308a11a793bb87ce9b7719f2575b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121036380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0edff62c9fc82245023008f475e76941fde2dccae70839385672863dc2952b0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2e638123aaf8af28628996ae19437f022705e0603a46e2b557854eb646d67`  
		Last Modified: Tue, 12 Mar 2024 07:35:58 GMT  
		Size: 57.7 MB (57689519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d05b4c69481ca62ad7109705e071b9ce9a6e4521469a4887c33e6e5d33320`  
		Last Modified: Tue, 12 Mar 2024 08:56:42 GMT  
		Size: 7.3 MB (7288888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:fa668707594184adde956451e192d2c8bc5ec87077f6e0e3f1d5d1ce34fa3c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae628efcd3196c3e18af3dbdbbf1ec99c5550a4a7cbe78c526d8831dccb4f248`

```dockerfile
```

-	Layers:
	-	`sha256:293eb7a74835dd3b85f8325ed2d4d78cdab89f30e6dc75b1ed5d2f75658e7c81`  
		Last Modified: Tue, 12 Mar 2024 08:56:41 GMT  
		Size: 4.0 MB (3954965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf815741a713c4b2d2a025e5da1317a666f29681770beef212cf6e3676d11234`  
		Last Modified: Tue, 12 Mar 2024 08:56:41 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:80a3d9939f488daf57323ea0036a0adcb1cf280bafecfe6ba2e4f5a5288594a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124877287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ae4fa6a84a9319675cc720c00c421c89fa1b4231331bfb8aaa1d602c486c8`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 02:27:56 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Wed, 21 Feb 2024 02:27:56 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Wed, 21 Feb 2024 02:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Feb 2024 02:32:55 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98800b4f3544309d2803e90a4749608658821815b45d85e735ebff2696c1e373`  
		Last Modified: Wed, 21 Feb 2024 02:44:26 GMT  
		Size: 58.6 MB (58633291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd47ea4aaa5d0fd538dbd1aa7ac328add7f7634697df5646ffa289b1db3745f`  
		Last Modified: Mon, 11 Mar 2024 23:30:17 GMT  
		Size: 7.3 MB (7289508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:54b88a0330601a2b5eb2192fbef3c2c87ee0b06049f0c16b005d058c84fd7e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a12b383fd8598254e26939de1e5cdfa184bead623c685aa8ef3310cf8d4c6c8`

```dockerfile
```

-	Layers:
	-	`sha256:d869812c06e97952b35a338037664b0298b0983c45b3e607ebc0ab00fdaae228`  
		Last Modified: Mon, 11 Mar 2024 23:30:17 GMT  
		Size: 4.0 MB (3962202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:431ea4d9f0595f355156df995e5ec34ac7349c91b7c810431cb00ce015d335c0`  
		Last Modified: Mon, 11 Mar 2024 23:30:16 GMT  
		Size: 9.9 KB (9877 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; s390x

```console
$ docker pull elixir@sha256:757e06c650af9f39b50abf1278500974f5a2af596db54161e6087f7abbd37c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118764745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10831d01690a237c54539c93d73e884f1589a9e4321895999349105a588dd048`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 06 Feb 2024 15:23:33 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV OTP_VERSION=24.3.4.16 REBAR3_VERSION=3.22.1
# Tue, 06 Feb 2024 15:23:33 GMT
LABEL org.opencontainers.image.version=24.3.4.16
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="f434c19d62b29ad8ef5300a490b9ea9df9cbfdd497c68603b184d43448418fa2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="2855b5784300865d2e43cb7a135cb2bba144cf15214c619065b918afc8cc6eb9" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f754529036472e75db3681b26c3d457c49acd10b86123ae2abcfca65aec636`  
		Last Modified: Wed, 21 Feb 2024 03:25:30 GMT  
		Size: 58.2 MB (58168666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce75041ea1a57ec999f833ad3f176f0276af38c509889237e52572cfe85e7a`  
		Last Modified: Wed, 21 Feb 2024 09:01:12 GMT  
		Size: 7.3 MB (7276754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:596a7d7f8fc3f4cf31b36bf228a35a83d821c4a2b6122b75da9b63a5800eeb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60eab5f502f6d6f50e1e798d90a6f7f4160625c31f4e151a8fc913003f0898b0`

```dockerfile
```

-	Layers:
	-	`sha256:243f158492a5ff6eab46da5854945c4c583b0b8ab3e27d30a7a5832adfd5364e`  
		Last Modified: Wed, 21 Feb 2024 09:01:11 GMT  
		Size: 4.0 MB (3958049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc894fa0a5c83b4dd5ffee8b89723b3a2bf4d7b2b9d3efce27df2f493af48c39`  
		Last Modified: Wed, 21 Feb 2024 09:01:11 GMT  
		Size: 9.8 KB (9845 bytes)  
		MIME: application/vnd.in-toto+json
