## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:be07c39c89708054c85960172269e22c6fbc9423d21cf8341d7c2e27f014b72b
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
$ docker pull elixir@sha256:d655ce7ed675412a945539b56623581eb4df4ac2f2b7d698cfb5aba8f78c0bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127225786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51558c8495a48b2c9b3dc4cdd268be5dee9b7dd8aa42f14dc09139c2f4136f8`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52502aa6f555b708e36dffb390216200185156a7ecb533f9a272613501852707`  
		Last Modified: Tue, 02 Jul 2024 03:21:47 GMT  
		Size: 70.3 MB (70317405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49058b53d11cc445802c86ed7e8003211be1b1e83e4397b8b9efb4e21b80f1bc`  
		Last Modified: Tue, 02 Jul 2024 04:13:24 GMT  
		Size: 7.4 MB (7354317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:10bc86ac577db510752ec64af91a00c05ae797e70cc7caa794d92241a0f3753a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5be3f85aac913456051056f3b486a4d045d8ef81418c1be543c9230c859a3e8`

```dockerfile
```

-	Layers:
	-	`sha256:459ff5cabe37c64911571afdd623863e0da6c160b03ef8285b3a1de6932bc0dd`  
		Last Modified: Tue, 02 Jul 2024 04:13:24 GMT  
		Size: 3.7 MB (3677956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6e7d67f833664336b45681ef1acb81ba25bd46b7ec78d0a5412fc3151ea9b7`  
		Last Modified: Tue, 02 Jul 2024 04:13:24 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7f4db980c6bcbb8c5ae8aaa50987f9d5c03edde31d7996842cb60a10bab38ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112569911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280065b015b205e831e4af45687a2edde1292d793e5d9e9a641649ce8ac2906a`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c845707cc182dc48741c2d41fff37c3c68d0b8a643937513cbd10a1a120606ef`  
		Last Modified: Thu, 13 Jun 2024 12:12:40 GMT  
		Size: 60.0 MB (60037973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772e8f219090aef266aefe92f9f9978e165f7628b5f5dd075103b1fd3b665cc3`  
		Last Modified: Tue, 18 Jun 2024 23:26:35 GMT  
		Size: 7.4 MB (7356898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:4cddb47da05d6606508fe616fbba8493980ae111f442e3e76743c41861c2a7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374986ea945e6c389f7c84e326fdd6e434457541cab08ff1ead25291d713bba`

```dockerfile
```

-	Layers:
	-	`sha256:a802ecef5af44722c84413aef0404729282a44f906797b657ba1becddf79ecb6`  
		Last Modified: Tue, 18 Jun 2024 23:26:35 GMT  
		Size: 3.7 MB (3680925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3a0f30779fe64b5860995176e1a279af871e4bc98d7620ea2f0a5320c28bb1`  
		Last Modified: Tue, 18 Jun 2024 23:26:34 GMT  
		Size: 9.8 KB (9832 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a30f0ddb1d9af9508603b6cbd6e129b5dbbc3a5cca2f652e53cf0e2ba8b40ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124882194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd328a693c46f7c7bac9f5c5d8c31735388e8e6ef3ca89cdf6b1d1fde04a51`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509c95a751ca7a67686944c58d0423578465ded54f7a436acf948df2096de23e`  
		Last Modified: Tue, 02 Jul 2024 10:54:00 GMT  
		Size: 67.9 MB (67939559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec90cb47f688e228718e6ac1cad8a970e56f9d733d5573da5048f646002417d`  
		Last Modified: Wed, 03 Jul 2024 07:36:49 GMT  
		Size: 7.4 MB (7354187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ef1985ab80311224733a7c6d251ff4234eaef4cc5ae437d2d460fe2aa3b41d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d2b61ff8443dd65be97012d26d990923039e4fc4e5f8cd3ab8f043897c4eb3`

```dockerfile
```

-	Layers:
	-	`sha256:d46c91f9129f3736a17f21daea81871a31d490bc771fe961978fd642459d5ffc`  
		Last Modified: Wed, 03 Jul 2024 07:36:49 GMT  
		Size: 3.7 MB (3678204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cb2ca0684efdadd9db51ae48f26a8a3ac81cb3f415ed7221da624abb45c515`  
		Last Modified: Wed, 03 Jul 2024 07:36:49 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:5099b91ff4c854b4d5a4fa6d8c1b675ce35b8749885edeecdd6440c57fcdb571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118975930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0116dec2ff9a06e8bea362a4f967dd4c4540feaa66c7cbbf29db966139379ba7`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c56d0ae39688b64e0563655d1fe20c92e226347a7557df1fd611c27241a57e`  
		Last Modified: Tue, 02 Jul 2024 03:21:35 GMT  
		Size: 61.0 MB (61042918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8405b1a63abd45891aa70c69e98630bb343a85467e343adac3985aca2cd9728`  
		Last Modified: Tue, 02 Jul 2024 04:13:57 GMT  
		Size: 7.4 MB (7353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bc97f7418ab9fd684bba509b13bc092f7954d75774dcc107b61b8b1716dcce12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b439fcb2df4a60a4ea4bf3c03de0c550fec82978db2ac9066df36f32949bd08`

```dockerfile
```

-	Layers:
	-	`sha256:370033b0a1ef96db04c1be34c321dabe6e3e62554eb4309bba19795eb6bc7bf5`  
		Last Modified: Tue, 02 Jul 2024 04:13:56 GMT  
		Size: 3.7 MB (3675080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bafc978a65ed4742f1b495d6382f815ae5cb384a2e475867d3adc035514024`  
		Last Modified: Tue, 02 Jul 2024 04:13:56 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:8300d5cf66714c076c03f1093e949b37c134ba3411348a691fcc53c26a5e52bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123044757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b190269c2f460bf2eb8367bf329684ad83ff6433d62462dc3113504714297351`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e63725f5a29c9f0646b2e9c6ac109dc2469a29a1d60d2c34f407ee33af00cb2`  
		Last Modified: Tue, 02 Jul 2024 07:49:06 GMT  
		Size: 62.1 MB (62133428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76782e79c46d799c338a1a9aa7fd589575b5ea56d2d1365b2afdc263fc1d52`  
		Last Modified: Wed, 03 Jul 2024 04:04:36 GMT  
		Size: 7.4 MB (7354314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:59dfbb1c81f9e1b1649e26525baad4317c60cfe30db14d4553687414e3dcd873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ab896053eb31cb4189126becd00ed60307bab3bb9f3262416592ac602e8785`

```dockerfile
```

-	Layers:
	-	`sha256:21ce0e1e65ed9d7b319c643f743ae7dbd6ed4f559cadcfdd7fa60872ac859916`  
		Last Modified: Wed, 03 Jul 2024 04:04:36 GMT  
		Size: 3.7 MB (3682289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dce97348a601800f989e1b496e3d05913f9e88232e5b80914595692557b34b`  
		Last Modified: Wed, 03 Jul 2024 04:04:36 GMT  
		Size: 9.8 KB (9802 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:574281a38af376aeac62a5ee6310b49e4a3a51d41a03168f42ae380f80c670de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116122447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca243b668ece559e327b3de2bf43dfb20313240b7edf68959cceb21f58ca3696`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=26.2.5 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=26.2.5
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d34b409cb5968ae47dd5a0c4f85b925d5601898d90788bbb08d514964a3a141d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Tue, 18 Jun 2024 20:52:04 GMT
ENV ELIXIR_VERSION=v1.17.1 LANG=C.UTF-8
# Tue, 18 Jun 2024 20:52:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="7567c7dcedd5e999d2d41bc2ff70626f49ec283af22eda4f347861bccb34c301" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 20:52:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e90db6b9a310515ceb87a81a6ea8bfe2d033806edad9992f9794c6c7a3efa5`  
		Last Modified: Tue, 02 Jul 2024 05:32:10 GMT  
		Size: 60.8 MB (60837183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143a9a8a502ad965c34407c9dbe7cbcd616b518af3b869ed00712368526840fe`  
		Last Modified: Tue, 02 Jul 2024 21:23:58 GMT  
		Size: 7.4 MB (7353753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:59aa94e6eea80325929ef9098cf5ff51ef7abfc0fe918e4221230813bf3d0b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab38023148a8304316f4ad530f9d7640438d157eae3bd3177e3aae6bb86680d6`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6a58e4f4e46ce4c30ccfa95d50771d0440fc89693219299f49233cfef4b6a`  
		Last Modified: Tue, 02 Jul 2024 21:23:58 GMT  
		Size: 3.7 MB (3677783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc37b738a846bca5102dcdd1d223af170267d9d448e648de4ffa9feae63d0bec`  
		Last Modified: Tue, 02 Jul 2024 21:23:57 GMT  
		Size: 9.8 KB (9764 bytes)  
		MIME: application/vnd.in-toto+json
