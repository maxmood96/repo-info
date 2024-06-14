## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:734dd54d571ebb6f0ef5fac24744213a72545dc9910e7dd3c9848d17350892a2
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
$ docker pull elixir@sha256:79c80c804073a2211351effe55b4ba6008d8a857e63c1359783149c295891963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba485788112d444843c74b263785c1c028f250ca2d7261fd434f98919a1288e`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aec8288d120bb569cd9f9bc81b3f56f7fb170b3000dd036de562251c63c2560`  
		Last Modified: Thu, 13 Jun 2024 18:22:16 GMT  
		Size: 76.0 MB (75955499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a76766611eb08cf69db7bf4f2a8d0a2885df8f2f376c49c6f1865e4c7c6145`  
		Last Modified: Thu, 13 Jun 2024 19:12:06 GMT  
		Size: 7.4 MB (7357178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a27ffa3c1a1bf2bdb991a14f350c47c5798099655c7e8222632607396756b9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa1aa544cd3ba80be56d8fdff847bf6cc18c33de6722bb14f0b1ee172d6b0`

```dockerfile
```

-	Layers:
	-	`sha256:f519e95370eebf90a11b60e376f6ec60c80d97317f90966b8c438da4a821f62c`  
		Last Modified: Thu, 13 Jun 2024 19:12:06 GMT  
		Size: 3.7 MB (3678533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201ad10c0bc877e9e2469bdd23fcf9f397ae4b49e21084016d0a9faa76c60004`  
		Last Modified: Thu, 13 Jun 2024 19:12:06 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:d39261be8269b812be6909a64a4e3062bab28e111ec2ef991e8f7850986be94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117528763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a632f95c521b1cb4cff1571e17a02be452df0153193fa770800a1944e88e86`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b635eb63888623feea1f1b0439756e0e8f02f0a70f537df2b802c2f817b6cfa1`  
		Last Modified: Thu, 13 Jun 2024 11:55:17 GMT  
		Size: 65.0 MB (64997104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e01c7058a7c45d76e32da8ff87a4a0b249525ce65d91fe2f644c32073e07ddd`  
		Last Modified: Fri, 14 Jun 2024 06:24:54 GMT  
		Size: 7.4 MB (7356619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:1cd79f92299c1e8aadffcc95655c21ba92995f23bc8431de23dd4390d7d51bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9c3462b275b94fcddaa5604444a24724b6a3514529348a607671ef334b2f4`

```dockerfile
```

-	Layers:
	-	`sha256:2550b4552ea76a194a4145a450e60786faf34163f0d5a4a369f1254e1c8257d3`  
		Last Modified: Fri, 14 Jun 2024 06:24:54 GMT  
		Size: 3.7 MB (3680781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedff8d97a696f230e42a9c279f57ba6287ada0fbdbd6513acb38d2d5904bcd1`  
		Last Modified: Fri, 14 Jun 2024 06:24:53 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:902aa9332f42cbe4d8c19d2255708f12b01c6e2255b6a724286e00a0c3e413a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130547818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2988ad01b02ec3e710b8e42888dc7f89da2223d01143aec2b4bf286d8ed4c514`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b336be13633c77d2502abd4c23cf1ba3c1e9bfdfbaadcbbb75a6d535c61ae`  
		Last Modified: Thu, 13 Jun 2024 12:19:00 GMT  
		Size: 73.6 MB (73577371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0655837afa797111b62f89fa1488dac65fc221b514022e0ffc1ebecd4ddbb08c`  
		Last Modified: Fri, 14 Jun 2024 05:08:29 GMT  
		Size: 7.4 MB (7357045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:aabb8e5ae70863ac2d74b1637f116aa79ab4991e8d9fd8fcfef7d9f693fa0696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601200de1354b7bb463f28acb303fd3f49d6f7d4d665d462ff4d4aeb0e944f3e`

```dockerfile
```

-	Layers:
	-	`sha256:cfb02c0fcf1c6c574c64b4660036e96d8a651e65c5a52c8a34c4db80b6562de8`  
		Last Modified: Fri, 14 Jun 2024 05:08:29 GMT  
		Size: 3.7 MB (3678817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dcae8e86e0b6ea8ace59f7d3e737fc65edb15a3f7d4c8f38361481e72d4ab0`  
		Last Modified: Fri, 14 Jun 2024 05:08:28 GMT  
		Size: 11.1 KB (11064 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:42d1a80961d507b1bb87fbc7f2764b25e05a67e035c6b28f1b28d40fac355dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124095864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cc5c65a524241afca045246a3ac3efcabe47c07ea6a2adb6a5742a987916d8`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493da813ff8c4008f01eab0d6adfed15f9308e5ca28e19406316b8dd60099ef`  
		Last Modified: Thu, 13 Jun 2024 02:06:18 GMT  
		Size: 66.1 MB (66136662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0964f58636f329b3b077e27ce883d3fe440ad8a497233b88f9ed951ebde3bd03`  
		Last Modified: Thu, 13 Jun 2024 18:26:01 GMT  
		Size: 7.4 MB (7356755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ce02334d62d9b6a5f8b89704fa555dae071908eef39d1ad063a0cc8f23342984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab752d2998346b5c6fe3b6fed6517a24052b98d4c25243d98dba58a60245130c`

```dockerfile
```

-	Layers:
	-	`sha256:116127dbb0f5ead580f75f383226ce549741656ebe48811ba834766f79102a0b`  
		Last Modified: Thu, 13 Jun 2024 18:26:01 GMT  
		Size: 3.7 MB (3675641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768f3464fdf74d3e5dbea3aaefb4e43018cbff03207157530d0a87022c03df61`  
		Last Modified: Thu, 13 Jun 2024 18:26:01 GMT  
		Size: 10.6 KB (10601 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:188f2538c03e03ae82622c2d12256b853c2fffcf78a57473e32e433a154f5457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128023805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5753a4e6e1527923c3cb99e6d88155513db3522c212d8879ccc2d814cbd19d89`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:5b31953e08477fa1771514ef5fd326ae78b7c4ad417cbb64755ee493634ab392 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7e04e800a5f6b106e3f1cb53c3677b55297b3841c160edc0f657f7a27ffb9ad0`  
		Last Modified: Thu, 13 Jun 2024 01:21:03 GMT  
		Size: 53.6 MB (53579678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b018811e92b2da06e2b8ab87bad87a24ac8651f59288ad09e7e5836dc64d1`  
		Last Modified: Thu, 13 Jun 2024 19:35:58 GMT  
		Size: 67.1 MB (67086784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085ea1b3a9cdb36b69d95b8193b3ca78019bf5593b34c1112b8ad49fac6ecb51`  
		Last Modified: Fri, 14 Jun 2024 10:18:28 GMT  
		Size: 7.4 MB (7357343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3f878cf05ed02fcd67f14855dd37ec4a1a62811c178cea496a15e579966dc86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32107ce67768489ff21757b54bfb7746f1b38b69b73eea26c549494514e59309`

```dockerfile
```

-	Layers:
	-	`sha256:89c7e8e0ed0265d46a84182fc788c71795ec3e14d9d667539fd4d5f8430def40`  
		Last Modified: Fri, 14 Jun 2024 10:18:28 GMT  
		Size: 3.7 MB (3682886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443016a15a10593cc5f26c6c737f43817d3e2af169472c1e5c34a4908552ac41`  
		Last Modified: Fri, 14 Jun 2024 10:18:27 GMT  
		Size: 10.7 KB (10711 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:ed98b60bf0cc9dc39841d4402252c5a40a6a79684dbe34a371a2e3c2cd05d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121064568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ead203bf84e52dc1a19ecd669989064e156d47fc0b7dcb112a32f0e3932175c`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:4debdbf640f7b84de2c501cfcf8124343554f82fc2c8948149efc9e60c80c7f1 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6d80f2b74ad971cfa89367f3157841bc726dd7cfbfd585d5aabbdac584178990`  
		Last Modified: Thu, 13 Jun 2024 00:47:26 GMT  
		Size: 47.9 MB (47942476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ed0eb0706e710acf88621ddc6743aaa6b9e36116ab58621288698e0def2744`  
		Last Modified: Thu, 13 Jun 2024 07:21:40 GMT  
		Size: 65.8 MB (65765555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d760b579a93ed1dfd2a96150fa5e8c98f8e960189fb7c719fb0bb68e7b233b`  
		Last Modified: Fri, 14 Jun 2024 07:38:59 GMT  
		Size: 7.4 MB (7356537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ebb0e52793e97a64fb589501f69481e83c535a7dd5e3bd5ee4f4138cbec88feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c30b5990509d5b01453a1ca0678c0c66e5a49aa0492a0fa2f0c45fcc8746e0a`

```dockerfile
```

-	Layers:
	-	`sha256:5c2eb34348701a6c9a7b94c7d45921eae1609294f77cec144409316ad1a0c514`  
		Last Modified: Fri, 14 Jun 2024 07:38:59 GMT  
		Size: 3.7 MB (3678360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912c8c0764912c433816001ee6f8c1b9436d017f28cad5a1e498fd3d133d69bc`  
		Last Modified: Fri, 14 Jun 2024 07:38:59 GMT  
		Size: 10.7 KB (10655 bytes)  
		MIME: application/vnd.in-toto+json
