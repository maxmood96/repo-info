## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:102219e464dc85bfdd714fb9984f288db3a62b89cdeee06351a20b6b068e932f
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

### `elixir:otp-25-slim` - linux; amd64

```console
$ docker pull elixir@sha256:1a0b0dab12ee668020687b9e484684da6ca5bda12efd5e978f29d69ad2e20736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127667353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfb78b0fa340d0e245192235b1317ab814b36491abb13107b28aa244199ec73`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c71e0da37644431c6c87a465134b3af8cd72bfc700526f8b1ee580d7dce6a`  
		Last Modified: Tue, 24 Dec 2024 22:33:14 GMT  
		Size: 65.9 MB (65926373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764f07c0abf5ccf57be03ebd4bbfe7c520de89e76133a01d79b7d861414edb8`  
		Last Modified: Thu, 02 Jan 2025 19:29:41 GMT  
		Size: 8.0 MB (8002023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3e0907e78225953b43ee20876795208d913a303bd96fc369f6c5114dd21a6133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb7520f16b8fd8c471d571d443b2650ccbf538c4215933100be00308f55927c`

```dockerfile
```

-	Layers:
	-	`sha256:2b0fe991f4f756f96f78bd0acad7dee9601fa2b52f16c2aad61211cffbd87620`  
		Last Modified: Thu, 02 Jan 2025 19:29:41 GMT  
		Size: 4.0 MB (3998259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d17c6eef6b2b154a12256f947d8a895ec7401585c331745c9fcebef9f2ce8e7`  
		Last Modified: Thu, 02 Jan 2025 19:29:41 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:79bd1ce92fba3c8c8118132e0db893b2b0ee06de7824e215978f6e340f15921a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114239018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e30b75d67f127c2ee79fa45082e37c47e35a78f2d8ba7851a852bf0ff78dad3`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 01:45:11 GMT
ENV ELIXIR_VERSION=v1.18.0 LANG=C.UTF-8
# Thu, 26 Dec 2024 01:45:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f29104ae5a0ea78786b5fb96dce0c569db91df5bd1d3472b365dc2ea14ea784f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 01:45:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcfa8800dd3a9423fb0dae51c28af48e6ccf296d881f17ee1b492cda97654b`  
		Last Modified: Wed, 25 Dec 2024 04:05:38 GMT  
		Size: 57.2 MB (57213304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4758aaf90b9fd37e50b293d59b94e6c6299fed26d5b8cf257d716d1fc268cd54`  
		Last Modified: Fri, 27 Dec 2024 21:39:39 GMT  
		Size: 8.0 MB (8000948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:029c113ace31a61b8dbd0df16ac8955e90441d52f49209d45ccdc5c1336b3aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a385921eb36a10747aadbc481adaad51e4f13459630667856cf79859e20947b1`

```dockerfile
```

-	Layers:
	-	`sha256:35290069eeb6aaa6f89a0a8adac58dbc9fdd9cca6842973b50a2e5beb6360e94`  
		Last Modified: Fri, 27 Dec 2024 21:39:39 GMT  
		Size: 4.0 MB (3999852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034e6929bd1b431a6161e9d6530ef1102246ee6ec1d4d661a99f1507641b15af`  
		Last Modified: Fri, 27 Dec 2024 21:39:38 GMT  
		Size: 9.9 KB (9858 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:15a93acf7f243562c48559871cf0e0692dd5bc53b572fa3da867faa80737eb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124538304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477f203059667fb82d19f77356c87a95f3cc49e50c5d2795afeeeb5a8fc5661`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 01:45:11 GMT
ENV ELIXIR_VERSION=v1.18.0 LANG=C.UTF-8
# Thu, 26 Dec 2024 01:45:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f29104ae5a0ea78786b5fb96dce0c569db91df5bd1d3472b365dc2ea14ea784f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 01:45:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1855fe22bd18bf42b3fe5cb07e311bff8cd160d07f8c6281d921265bb2b31`  
		Last Modified: Wed, 25 Dec 2024 02:08:59 GMT  
		Size: 64.3 MB (64291421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedfc7037a5c303a1c46ea89ee607202d96f9831b4934b65ea3d41ecfc8b8ae3`  
		Last Modified: Fri, 27 Dec 2024 21:37:56 GMT  
		Size: 8.0 MB (8001185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8870960db060a051f890fa1a95be86b55a78ed9c5e0c548a0981c2053708f70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ca9925972231ccea988bcb9172a2497824fb796b8f6fc1b6f36cd10464f9aa`

```dockerfile
```

-	Layers:
	-	`sha256:0979ccb69f7eb80e7321aa8b46d18633fdb9ce20783b66cbf6c2313eba5b5520`  
		Last Modified: Fri, 27 Dec 2024 21:37:56 GMT  
		Size: 4.0 MB (3997868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962c01f9e58a3fb8e4daae1cce593806276860f75a08117af7f31a0e5c86965b`  
		Last Modified: Fri, 27 Dec 2024 21:37:56 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:7833f528a0bb2d59a8f254bed867918a41c4fbac4d43656854496f7d5066695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120282991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad4f6a59ed7247fd1898b7894bf70c9defad53e69234f4f54c5c111e9a83c5a`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=25.3.2.13 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=25.3.2.13
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ef56f754f14ba89356284145c8a0dd95e11f00ec6142b4dd9a9431570d6ff5ea" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad11c813e13a388055f5ad57bbf6dc37024f63a02ed4474d52493c988d9438d`  
		Last Modified: Tue, 24 Dec 2024 22:21:45 GMT  
		Size: 57.6 MB (57605343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f89baefc6d63d7a107d3d121e20c0d637b574044244665cafeb15797b1daaa4`  
		Last Modified: Thu, 02 Jan 2025 19:29:58 GMT  
		Size: 8.0 MB (8001632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a0af526b13804fefee8ec9e97ec84caf172efcc2139a906056d1e263ae9df33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9d4a3576bbdb2890d6a21664b911d31a9a5f342fc539ea1359b1f0262b0b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b8e3bec9259ae7bc026828bc6f31107a4fd95ddeb0f1661a153b9d79be06592`  
		Last Modified: Thu, 02 Jan 2025 19:29:58 GMT  
		Size: 4.0 MB (3994742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9b370367c713d191e55a9c62a5f6edc2b87bd8fcf8d70dc21db1c68095e444`  
		Last Modified: Thu, 02 Jan 2025 19:29:58 GMT  
		Size: 9.8 KB (9763 bytes)  
		MIME: application/vnd.in-toto+json
