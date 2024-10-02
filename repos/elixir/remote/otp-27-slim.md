## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:21e7f37c559662725db8ba61158b87ccc22aa516253ee344cc981f6c7be2dd01
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
$ docker pull elixir@sha256:b2b3d188326e2e8a5273d0dfa7506e5c9a67e1bfa0bef9fdf5b21c3b36e43e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132672648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c350babf779779eb56db75d52945c371a87d869bae636e68891eb2851cc243`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c422c173bf2f04214d2de95cd15f032c7d1c8b5440e74e6a0e27832eee3608`  
		Last Modified: Fri, 27 Sep 2024 06:13:00 GMT  
		Size: 75.8 MB (75757570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136643ddf914aa939443cc1c166053189e5e2624a1c1f7342a91cb59e15f9ab4`  
		Last Modified: Tue, 01 Oct 2024 19:59:16 GMT  
		Size: 7.4 MB (7360027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:23ba1790fc5542bbdd96e0760d6c2e15e4591df1c2925fd547becec056d39105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ace80d75273a3728cd5c3625541049d887d09e206fde8fde31eb95043f31e2b`

```dockerfile
```

-	Layers:
	-	`sha256:4f8c1ec5bfdf7f4b07c6265944dccab295075bd7089fec06f175b874e224698d`  
		Last Modified: Tue, 01 Oct 2024 19:59:17 GMT  
		Size: 3.7 MB (3703714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac1700cf14cf834a520156bcfb916cd3b8ed5d781a2451e895fd0b48999711f5`  
		Last Modified: Tue, 01 Oct 2024 19:59:16 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:fd16171aa73c60ebb560db1ef2fb0babc7f7b8c3c003939948ff84b490b99f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117400771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249cac01729f87dc7e70b145322e2bfd2c66398318d9b69d167041b75e480fc2`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76642db6a2362ef0f1a2b0b0509ad1e29b37fb444823c0868ab146152ba886a`  
		Last Modified: Fri, 27 Sep 2024 10:36:18 GMT  
		Size: 64.9 MB (64893469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e672d1e111ff6d591727e414b351a6a1b40d06605c2d9496e4fafb9d275ec4e3`  
		Last Modified: Tue, 01 Oct 2024 20:40:03 GMT  
		Size: 7.4 MB (7359389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f20b1844b64cfa762e86e4ff05c04bfbf3da14410b8424ca320f97528e8ebe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ae813458f0d5f6a38f615302c6fbd818115b012b5024f8ae660bce9e22a6ae`

```dockerfile
```

-	Layers:
	-	`sha256:333dcaa86eec62d3d5e364353b9af5113188494a3d60df37832c683c10627e25`  
		Last Modified: Tue, 01 Oct 2024 20:40:03 GMT  
		Size: 3.7 MB (3705962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96abdb5a8f118b783deb39482ed672381b6a83e2528085cd94d6c50de3d68704`  
		Last Modified: Tue, 01 Oct 2024 20:40:02 GMT  
		Size: 10.8 KB (10754 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:5167792a3c0d848bdd7833ef7c7cb64d669e51d145a5705397c2f16d59a86e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130462468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c1b5d54e79915af2101dc04d43d5bb534427a592b80dd359ce7e5d4b108e6d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a304767221c630a8fb6929a486562fc4a9265e79fbd44f9ed7d968b730ccc5df`  
		Last Modified: Fri, 27 Sep 2024 11:34:32 GMT  
		Size: 73.5 MB (73517595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5bef625aac2017320d81282485da8865a3894b4d612a566e6c90f03669216`  
		Last Modified: Tue, 01 Oct 2024 21:32:31 GMT  
		Size: 7.4 MB (7359987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bb61c3a40e9e0945b3ca3b7d3df29d037f12a2784309f3b11ec31ce406161840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e05898b6195d557e4bbdac33665ca3c1396c8157d08db3fb00bd82da656f18f`

```dockerfile
```

-	Layers:
	-	`sha256:aee7fca99d95af94074551043e5b3437a04ae0a5d1f2dba34a07899873fb48ba`  
		Last Modified: Tue, 01 Oct 2024 21:32:31 GMT  
		Size: 3.7 MB (3703998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f6b2bac3fd8d78705d70718042112b1faca39c6a6553be8b00272300404793`  
		Last Modified: Tue, 01 Oct 2024 21:32:31 GMT  
		Size: 10.8 KB (10790 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:15c376ef9e0094e5dcbef3eb6da2fac2b6988aaf4bde7a70cadedad0afd939e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123876833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f249b4d97639c9c89a627f7898d5d112d1a7bd3750e2681e360aec848632ef0d`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9de5f74936da3c96500fc8ce53661d884d3ed63f15f25cfabffd2ac3dcbfe1`  
		Last Modified: Fri, 27 Sep 2024 09:05:54 GMT  
		Size: 65.9 MB (65940670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3769cb96626ae40ba1d47371c38f2728d277e061cea9ccd1fa730331f95010`  
		Last Modified: Tue, 01 Oct 2024 19:59:37 GMT  
		Size: 7.4 MB (7359522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:54e4070a52a26c7ab5aa550e17bddbf6262d7f9c2c06e59a66579791ef7a8b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca90c38e216ebcdb5aea5cb250a63c547c6a5981eea08ccc7cb6ddf7781ad29`

```dockerfile
```

-	Layers:
	-	`sha256:9d81cdd86ffd424f1c5052c7dc63a6e8ddcfb510408839d32a5cb52eae2b91a0`  
		Last Modified: Tue, 01 Oct 2024 19:59:37 GMT  
		Size: 3.7 MB (3700823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eb2b2d7a90f3ca71d98acc1fc3526dcad5bdd2e60bea93d006722f2881f2ec`  
		Last Modified: Tue, 01 Oct 2024 19:59:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:f2e9d0682386beedbb756188ae15b7ebd4384b48be43dfd9c5415b28fbea0e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127932728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b1ba81530eb18a8dbb8ac0578df3a5fb830f65c9d6d2e8f9cf56d80df0e7cf`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3607ec5f15499e67e2dcb773e6fe5943d5612e6845cdc7f93cdf9f98dda6287`  
		Last Modified: Fri, 27 Sep 2024 16:45:07 GMT  
		Size: 67.0 MB (67017569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daed459bc3197bf3f7e3bb7a86185ee47d8f8fe81775f1bd6981bed040f3b83`  
		Last Modified: Tue, 01 Oct 2024 20:03:05 GMT  
		Size: 7.4 MB (7360002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:800cefdf51c0e72955d6d0d0d76d7e7ffc06b27cf6a2046c691db8c7fd50bdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbd2b6a61d1056a0a32e462464bca306108039f22381239c84f68c3ebd44e13`

```dockerfile
```

-	Layers:
	-	`sha256:64e4c85780b964019e19a8a0a28a353255b42eadc479127309ab13f5405586e5`  
		Last Modified: Tue, 01 Oct 2024 20:03:05 GMT  
		Size: 3.7 MB (3708065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d90081220614233e5c917d597e4c1cabdf9d626ee75c70c1b3ca9b2e2bf01a2`  
		Last Modified: Tue, 01 Oct 2024 20:03:04 GMT  
		Size: 10.7 KB (10718 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:5177f99551f46d4cf6b0cf83a0ab1d227de538cf0f0d46a9b6d1a7b261a16467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120991335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d952d4ba4e377424d7f06b7c090118f21ec471ff0ff8bebbc358cf09bd576c`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=27.0.1 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=27.0.1
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47d96bb7044cf44bca886213fa828ef82457a911b7622c453d9b3c615b6f68ab" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
# Tue, 01 Oct 2024 10:39:24 GMT
ENV ELIXIR_VERSION=v1.17.3 LANG=C.UTF-8
# Tue, 01 Oct 2024 10:39:24 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6116c14d5e61ec301240cebeacbf9e97125a4d45cd9071e65e0b958d5ebf3890" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 10:39:24 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634f1502b0f792984e7f81c7b653bd5c523718b67bd3e5a9dcea793613241806`  
		Last Modified: Fri, 27 Sep 2024 07:02:03 GMT  
		Size: 65.7 MB (65693132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761103bcfb1d7d7898889961366aacaa3362c6288172058c335dff9e03377dc2`  
		Last Modified: Tue, 01 Oct 2024 20:04:18 GMT  
		Size: 7.4 MB (7359533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5942d1ed3c6a7b4cccae9d07c09da8d183e07d18baddd8e564a1e6c394a02002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a403e0d8d0d16bae2971381f4aba36f5c3b41338dcf84e042d1af4286b84832d`

```dockerfile
```

-	Layers:
	-	`sha256:ed7cb7963427e9cd9a0d42cebd22afdf9a31556e70b0835c8cac2b07b937f7c8`  
		Last Modified: Tue, 01 Oct 2024 20:04:17 GMT  
		Size: 3.7 MB (3703541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac02fac9b8b40753db2172f7c0f89e9c8d1f11a73b562dcf47fbf88dc1838f9`  
		Last Modified: Tue, 01 Oct 2024 20:04:17 GMT  
		Size: 10.7 KB (10662 bytes)  
		MIME: application/vnd.in-toto+json
