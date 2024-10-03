## `erlang:25-slim`

```console
$ docker pull erlang@sha256:d3b3245125021600cdc03b62d6513c9b52b5090afa6567ce54eadb9f628e378d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:2a5562f6955acf96b8b8de9e6737835f94219ba4e50494f06a6af3c952a7309a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120991544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8195752351164dd275b0a50535554327409885721e1c9d4d87d95b4a1384eed6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982b0f41ecada3fc9bade812af31e9f5a1574485ac74dc6920368f589e47ff5`  
		Last Modified: Fri, 27 Sep 2024 06:12:02 GMT  
		Size: 65.9 MB (65910153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f432999ec27b39ae4117f740a400dedd0ca5cec955bc054cee5adb6eee3c992c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b94301c16afd16ce78cdf0bae4d65447aa530f70eaf1762d3804ef4528ecf3e`

```dockerfile
```

-	Layers:
	-	`sha256:4baa8b30d6193d8ad64686f23534e0f6377ba51e02fdf36660e9f1ed686e9ee3`  
		Last Modified: Fri, 27 Sep 2024 06:12:00 GMT  
		Size: 4.0 MB (3980407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a2fd6126eef383ea63d265d85a986ab3ca9250b1b083f3f09ef675b963daa3`  
		Last Modified: Fri, 27 Sep 2024 06:12:00 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4364f258816777ab9e83ffc390737cc9b81b661231cb58684cff9a2fba60e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107448575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede1787e4f45135576e353bb0add86599483fe0836ffbf713661f7d28a0598b4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5cd40f1db6e2c88ea6f0fcb22b19cc2f9e48cf487b8a54b469fc3e7780a480`  
		Last Modified: Fri, 27 Sep 2024 10:46:23 GMT  
		Size: 57.2 MB (57208195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e121f679c809eeb24be9cbddfc453978b4b1fb4484f8df47eb5775d517bdb82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107379099827e94df1141f0fa550c7fcda23b771ec293847dba7ffc809ac4f21`

```dockerfile
```

-	Layers:
	-	`sha256:ff6047b3c2b173dc786bd10e37156a874821b728642a547d8a08680c18d13edf`  
		Last Modified: Fri, 27 Sep 2024 10:46:22 GMT  
		Size: 4.0 MB (3982006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74badc4ed738587febfc0314f2f5da186a3f15468666e9bea7480863c809229`  
		Last Modified: Fri, 27 Sep 2024 10:46:21 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:2984709581070ec748217226ae26e335d6a153310cc006b3826dc9edd56f662c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118016322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b33fb7adc41c57ef6a52a1b4575814d24787d1d3b6d332f4129bacdb970b335`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eadad3b72bd706c3a6ace948f57cbd898168c199170df2b80045c434efb4c7a`  
		Last Modified: Fri, 27 Sep 2024 11:57:06 GMT  
		Size: 64.3 MB (64282458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:56f53a9f1a9ab726cf74f86821ca7e7bc4c288e942ddceff35ee4a12993e6ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4798038886d308e166fc31a87ee86d5d448be61ad1dec6243a97d21f0694bfe2`

```dockerfile
```

-	Layers:
	-	`sha256:bfc68b12408c2ff6f00d79e57febf1fd2ff9a668e1548caf71a0d2fbadceed9f`  
		Last Modified: Fri, 27 Sep 2024 11:57:04 GMT  
		Size: 4.0 MB (3980026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deea1b03ef5d4c265baa4b988643eff5e033d0ecb528447fc0d9379b1b84a7ca`  
		Last Modified: Fri, 27 Sep 2024 11:57:04 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:4846b5a12e184270cedc5eb29a14feaed79107cefb7834a0da06c1c529d75fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113667976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a33569336c41c9cba0d3f2e1c9c2f8afe34a42e4070b1585d04dd3b1fd6fc0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 13:58:20 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab148c7f5e0e9876aa5e941ed0a7307a52a89d7ca11fb46b607082f6c3b21c2a`  
		Last Modified: Fri, 27 Sep 2024 09:04:41 GMT  
		Size: 57.6 MB (57591473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b0822589d1e8d3878203e52f06e1d9f5b1c4a695f25e83d4fd8cbcb171d83ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12f506cf284b68d9607de427b0460b7e225b0d3a65410c50c874e4defb6d35f`

```dockerfile
```

-	Layers:
	-	`sha256:7b598dc3df483f66b232e6c309e443bdbdab9cd96bbbd9580246a63452819615`  
		Last Modified: Fri, 27 Sep 2024 09:04:40 GMT  
		Size: 4.0 MB (3976883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7b9e577a9319f15d63582231340271afd6c0661a30404aa8e8dcc96ffaef6c`  
		Last Modified: Fri, 27 Sep 2024 09:04:39 GMT  
		Size: 13.3 KB (13349 bytes)  
		MIME: application/vnd.in-toto+json
