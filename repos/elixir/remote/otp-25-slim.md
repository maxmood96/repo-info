## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:6c350a19af82308bf26f5c7bf7aea0ba1d3a9ed034c92c1ddd34c4a3a380bc9f
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

### `elixir:otp-25-slim` - linux; amd64

```console
$ docker pull elixir@sha256:7b2c75bbab8a8f97098db3e133292ea6f7fdc42a5affe03b1829f3435199f4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128216524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f76649e0f23455ce175b19b98f04215008904f4a29f04b33e20f9300e8905d1`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cc661596782c799a6c6e655c6c627f1f9266b92991774849196ada6c34e1e3`  
		Last Modified: Thu, 01 Feb 2024 08:33:15 GMT  
		Size: 65.9 MB (65855665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925533f7471c00656faebc28d97744aa20c6ab80520400406759d40037b3c3b3`  
		Last Modified: Thu, 01 Feb 2024 09:58:08 GMT  
		Size: 7.3 MB (7303896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e19cdbadfba3d0bdab20f5f8c67dabe47eb8b32c8c17cee6238cc217a290fbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302cc88a3b02ba0e3634d78a2bd9b8a2eb65d5cc24cdf9597c262782f9d56f60`

```dockerfile
```

-	Layers:
	-	`sha256:8ae0d729709dd9fb202dc640e2d6a9fd4682bf327c33b4e838d99e160e6d1d87`  
		Last Modified: Thu, 01 Feb 2024 09:58:08 GMT  
		Size: 3.3 MB (3276425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0d68b5e92897ad429999b436833c5e208c9983913b41b2bcad8819bd2a7b00`  
		Last Modified: Thu, 01 Feb 2024 09:58:08 GMT  
		Size: 9.8 KB (9844 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:ac2000a99344f2f52178441252809817d1c67f255d1e6410eb0171674c6bbd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114686637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69993b1e31feaab7ee4b5582d2cccaacac46ccd2cdefbb02922ad9905b4c25e5`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b17ce7fa785a73749713210646d15f28a5334a0188f6276b2e82e7370629268`  
		Last Modified: Wed, 31 Jan 2024 23:52:02 GMT  
		Size: 57.2 MB (57167069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dcce5de95519b15bb5eba5d816b278d563b3c4de55480ec9810803cfe2bb48`  
		Last Modified: Fri, 02 Feb 2024 17:50:11 GMT  
		Size: 7.3 MB (7303390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:fd7476e2519590ee3e47f1d3b7b41d51e9a466d8ffb7c59c043b93032d89f98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3288136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26789866a4ff250f1ccfce0b28d3025b42e653ef33608633682d4a52778c1fc7`

```dockerfile
```

-	Layers:
	-	`sha256:4ba198b2f5461654954743788b17203fefd2b4b3d20d1b128c179103be64a6bf`  
		Last Modified: Fri, 02 Feb 2024 17:50:11 GMT  
		Size: 3.3 MB (3278230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d2fd226b12c0b3c3dcc7530dddb1f669fb6dd29eca20fc88c09f9085addae3`  
		Last Modified: Fri, 02 Feb 2024 17:50:11 GMT  
		Size: 9.9 KB (9906 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:fe26b6a9abfacd8ee0e6596dc2e9351b46f45696db1afffe79fe9a1f8c01589c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125245183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704d8d1b05c84be28d776f122ee05cdec62926b638da41f5264d9b10f12b34b7`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a3c0c25649dc1a0e1a4340c8e8989c189fc16ebb5fdba3f35a176b9f8ae078`  
		Last Modified: Thu, 01 Feb 2024 01:08:32 GMT  
		Size: 64.2 MB (64233156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025cf32e4bc5c9d68512ad3e328a10dae02af1715c937e70204f77af2f130330`  
		Last Modified: Thu, 01 Feb 2024 23:45:52 GMT  
		Size: 7.3 MB (7303760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:76a8fc52463149c7474a72ea8a5dcf488bec14566fbc11604effcc45d44fb478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2845ac36e40c39e618a8582f790bb89ed10e9dff16ad5c2b9340f1d3bc88c21`

```dockerfile
```

-	Layers:
	-	`sha256:497b3830d55e9c2f6a7ce0c911c4f29bc4bcc180bd97040eddbfa05babe309c2`  
		Last Modified: Thu, 01 Feb 2024 23:45:52 GMT  
		Size: 3.3 MB (3276211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b835646ed080839ca2d7a5f36ac96ee8375c3415e03fb165e251f4e9f883f48`  
		Last Modified: Thu, 01 Feb 2024 23:45:51 GMT  
		Size: 9.9 KB (9852 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:40706258b72d4e7cd248b08b947bd0530915329940a33164baa8ff5116f77577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120888295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0730fcdc01e3bb2c91ad019f7e4b12b7f1224604844f7a29a9e69797470fc428`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20a8e59243ec8d56f200d8e17c64a384e203192df0fcbb2b5f06bf2f45331e`  
		Last Modified: Thu, 01 Feb 2024 02:49:33 GMT  
		Size: 57.5 MB (57538393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50458fcfe6418a39c0ad4a237facf9691bc38dd7b6734a14b9b295c2b112cf4b`  
		Last Modified: Thu, 01 Feb 2024 03:56:54 GMT  
		Size: 7.3 MB (7303559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0efe3216ea135ced3112f735f5edb9e15fe5185eaea740c8bfcdda60bf09ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3282940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c83b6f94151f5eb51947ce58d79f8b21af64c753852b078f003df8aa9adc269`

```dockerfile
```

-	Layers:
	-	`sha256:cc5b2c43edd12f99c75c961bb6c9a4203486758419a2f44e36dcc1049c3b7130`  
		Last Modified: Thu, 01 Feb 2024 03:56:54 GMT  
		Size: 3.3 MB (3273120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41eee8269cc5d53a8aab8cedfde7feeba74b80c7468f814ab997363412f8c0b3`  
		Last Modified: Thu, 01 Feb 2024 03:56:54 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:e79c28e9864fd8d1c30b129c7e9482ba1c2eeae29fd1342c719d366fe9c0f371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124708028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20740efd5fa74c77f5f64c1461bdc9e4f60a4e18496917f2f9a057a9ad6ef7c7`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc015e3119a9359a1fb7c1db1dbb261e2515a0664c7da7e34bcebd04feef6b6f`  
		Last Modified: Thu, 01 Feb 2024 00:41:19 GMT  
		Size: 58.5 MB (58473455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b4edd38924b70977e6f1ff671398f6ce095b64ec877cfd4d588d1f4b179a6`  
		Last Modified: Thu, 01 Feb 2024 18:39:30 GMT  
		Size: 7.3 MB (7304285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:dc39ae5ff7e4163290cbf0239c6836a97cc29ec47b5ea9557cf8f6bb06660c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3290233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8480da559ea5ba39caf0d8941dd8f4babca2496becf1b651cfb92e659253d5f6`

```dockerfile
```

-	Layers:
	-	`sha256:12a1c258e3dadfb86ac94979684a6d4d854b31c514d43010ab65af2e03c82730`  
		Last Modified: Thu, 01 Feb 2024 18:39:30 GMT  
		Size: 3.3 MB (3280357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717d600fb94bb8ce13e1efc8fab677f151066d8a864ba5cdd99a3ff742962f30`  
		Last Modified: Thu, 01 Feb 2024 18:39:29 GMT  
		Size: 9.9 KB (9876 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; s390x

```console
$ docker pull elixir@sha256:1e5645bada49fa19711302db3ac433ebdcc45bd6a5a942c86e675310d076f961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118670673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5980b284543173132a2831e9117100636e72a342d61e9c1d5a5b188070f99e`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=25.3.2.8 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=25.3.2.8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6b8a6dcfd294ee9d88e47721a6f897603532575329fea587240776c02b232d38" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["erl"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV ELIXIR_VERSION=v1.16.0 LANG=C.UTF-8
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d7fe641e3c85c9774232618d22c880c86c2f31e3508c344ce75d134cd40aea18" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319f30bab8e995538f42c51ab0bd391def4beca19993eb5d3323e96ba7f2233d`  
		Last Modified: Thu, 01 Feb 2024 01:04:30 GMT  
		Size: 58.1 MB (58072395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636e1e430d6107bf03678185523540969326ef6db661c808bdfa8bd76e5defd`  
		Last Modified: Fri, 02 Feb 2024 16:23:51 GMT  
		Size: 7.3 MB (7303596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0988a8d031e5cc4b3c60f378fa5b736ef7a804337386cd8f461577f49787c71a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3285836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de7220517b0b61988323c4908bbb445981921c58a4138dc4980d06dc3f86679`

```dockerfile
```

-	Layers:
	-	`sha256:b7dab03527bb694a10d1bed0fe19f6803ad9868c956cc4463bd87cfab3cbe0ea`  
		Last Modified: Fri, 02 Feb 2024 16:23:50 GMT  
		Size: 3.3 MB (3275992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632c11c83b33cebf1a89be971beefe1603bbda917df7b2cfd65e1d898a87d604`  
		Last Modified: Fri, 02 Feb 2024 16:23:50 GMT  
		Size: 9.8 KB (9844 bytes)  
		MIME: application/vnd.in-toto+json
