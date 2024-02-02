## `elixir:otp-24-slim`

```console
$ docker pull elixir@sha256:fb375cd5c6a92d70d0b1849627b0b43c68793cfbc9bc78854cec243ac22cd964
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
$ docker pull elixir@sha256:b69bffca0906e88800e1cb4fa839eba4a965cf0310fe1b0352b805c0e2bb1884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127561971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f09e89835cc6852785ee3d2b4f4020d85fbc19a8c7f631e82bc892ba08dc29e`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:8a28a0a895399cb613493ac5c7e5583e97f943fe58b25822185e0e9e196c0236`  
		Last Modified: Thu, 01 Feb 2024 08:34:18 GMT  
		Size: 65.2 MB (65227266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faff08e2c1a4ffda772049af806cb935200e082497084cc508ff188c6f9c3a9`  
		Last Modified: Thu, 01 Feb 2024 09:58:14 GMT  
		Size: 7.3 MB (7277742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f5b086aa8c4c94464b0e6b736ce999820fa4fa768ca9791adaecd16404e7d3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d570ae03478f1915cf94e3a4ae85538e33cb1f9e9c6d9a7d688631c464fd55a1`

```dockerfile
```

-	Layers:
	-	`sha256:2e3c96aa033e0ec2bf5026d85afddd38f1293deed368f2d97d61ecdfb45cb9af`  
		Last Modified: Thu, 01 Feb 2024 09:58:14 GMT  
		Size: 3.3 MB (3276425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24a6836ae3e5cc544c45ddd761d2a1d7dbf23324329638b71a19f7e370212251`  
		Last Modified: Thu, 01 Feb 2024 09:58:12 GMT  
		Size: 9.8 KB (9845 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:cee1163b971b71df69be4e29415a2628fdf775b47e34df5380f682ed42e26ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114692583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e757542ba4f73d7865a14de813afd960cb19cd23ed30e75b2934ec65f0647b`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:76e0370864def5d75c32f1e706861e28365bb444d57e9bf29f03b0ea7076f7e5`  
		Last Modified: Wed, 31 Jan 2024 23:52:25 GMT  
		Size: 57.2 MB (57199100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f247aae7aa56993ce10d6b56b03733feb3cca91d1ab33602b0a78ca0f1120a56`  
		Last Modified: Fri, 02 Feb 2024 17:41:58 GMT  
		Size: 7.3 MB (7277305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:40287f5278b4d65725595821b5b91b130f49588dfc24f6dd57d901f92240a9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3288137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693627dd7d74e3deae662e4b1ee04cec1040abb781e947df577642aa60d40e8a`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5d79d08e3bb3f4efe820a4b087ad1092cbacbfeaa7f19fcfb110256af94d7`  
		Last Modified: Fri, 02 Feb 2024 17:41:57 GMT  
		Size: 3.3 MB (3278230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088665a0a2869fa830a365307c2684ccb1a0c8e384b7d9dd7d223978d80b11aa`  
		Last Modified: Fri, 02 Feb 2024 17:41:57 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:050d0ec84b79fceb701880d086fb75660edd8bd8dbed3e6e9f3ae1dccd54cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119040734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a33ca76169494dd16fad88c9b708efe755d2a5a7f060661a68ae0eb36658f62`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:ad4be1f8bc19fc674d22380a99747011a6a0da2f57b0255e6e194b30990abc68`  
		Last Modified: Thu, 01 Feb 2024 01:09:29 GMT  
		Size: 58.1 MB (58054907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b58d80fe08ea115bb8805175c197df775c18ed6e3b568af1797485a29a6c20`  
		Last Modified: Thu, 01 Feb 2024 23:43:24 GMT  
		Size: 7.3 MB (7277560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c2d3ee2b1e3115aaa05f61613c1495a8c5d22bcf761d7eaa7bb6bbb332522ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c633f441035f914a6dff0611cf46dbd31bf71b286aacb1ca28a27bdcf772b5`

```dockerfile
```

-	Layers:
	-	`sha256:65061779e0eff046fd3ca1031b91da9b37600106100446a38b1b0905c586cbbf`  
		Last Modified: Thu, 01 Feb 2024 23:43:24 GMT  
		Size: 3.3 MB (3276211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f570d8b222bb7e7876224986d8227849f1a3c0b4e3a1a9bb88df563e8b6c7e0f`  
		Last Modified: Thu, 01 Feb 2024 23:43:23 GMT  
		Size: 9.9 KB (9853 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; 386

```console
$ docker pull elixir@sha256:650ba7c9bd371edfd094f0cb67ef40195a7f6e70add1b5a634bdec3bd577457d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121001727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8548d7ca96fbf05b1675310ba45345abb19c955844a775cfe51f6dbbea7a139`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:8fd7404129aae74129de299a4ddb91bd6b77022c73397d6b454414fb01925741`  
		Last Modified: Thu, 01 Feb 2024 02:50:52 GMT  
		Size: 57.7 MB (57677963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58344dd78359186d4ce5b161c12d0cc32090b5c2bd1aee6cfc49e36771f732d8`  
		Last Modified: Thu, 01 Feb 2024 03:56:51 GMT  
		Size: 7.3 MB (7277421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0b0178c27fa2ca83b2da3f7aaf7e6137fe0e064a6ca435adee567967134d54d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3282941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f6bd13283850865cadc36e0902803d08f56e89d725aa0955638caefe719bf2`

```dockerfile
```

-	Layers:
	-	`sha256:ad8a4eeb51b8c586cface26affeef5c41a8209d0029a579beab64daefce02f22`  
		Last Modified: Thu, 01 Feb 2024 03:56:51 GMT  
		Size: 3.3 MB (3273120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4927c4f1486703606ee380f4b8889d7ecd6caa7e64d5f6a9fea26e1e6dc77a1c`  
		Last Modified: Thu, 01 Feb 2024 03:56:51 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:f55a64e2a942597ba11c7a5052e8e16045597c27ea4a392a6b9b9a43f9608c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3804c8cf7c761b93fb7ea77f784f4fbdd0dec216ca2f36c6c61e196db7849ace`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:dce9dba5f9aca6fd197a595bf053a975aadc26d54d167ba03983a831cb625f80`  
		Last Modified: Thu, 01 Feb 2024 00:42:28 GMT  
		Size: 58.6 MB (58628407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c9a3ab2ff19341e2ed56f0d83bad9ff21a7f89ff25726f8191c92d169c96d1`  
		Last Modified: Thu, 01 Feb 2024 18:34:22 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c60fd84b8d86b972375e5a85951e2eced85c1e316c2a821483b30e29de88c898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3290234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b4c8596f7c46c111a19c2cbcdd251fcebeca2680cd077bb6084dc708e0e255`

```dockerfile
```

-	Layers:
	-	`sha256:b0962ede321a0bf086808e8871fba25e66ce4b9c7f11e16bacf0ff4b5510150d`  
		Last Modified: Thu, 01 Feb 2024 18:34:22 GMT  
		Size: 3.3 MB (3280357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d3ec2ced769c39f2db34eba4779830156d588a12a99b2ce721f719360cbad`  
		Last Modified: Thu, 01 Feb 2024 18:34:22 GMT  
		Size: 9.9 KB (9877 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; s390x

```console
$ docker pull elixir@sha256:084b9cf198ff04fb7e4b86386ea3e87ab8dd6426a85e3ea8d13bf895e5ec91a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118722407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3935efd60f9f79eb14acef453e008a30b71a473924406a205fa644b99661a5b`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 23 Dec 2023 22:14:59 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Sat, 23 Dec 2023 22:14:59 GMT
CMD ["bash"]
# Sat, 23 Dec 2023 22:14:59 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Sat, 23 Dec 2023 22:14:59 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Sat, 23 Dec 2023 22:14:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
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
	-	`sha256:427fb1775111da09e45a796063799e19c38f906856b7dde8953a87a93f30e0e7`  
		Last Modified: Thu, 01 Feb 2024 01:04:45 GMT  
		Size: 58.2 MB (58150362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39356d6aa6729741b51c34508af65447d67342642b1ee71d3b3aea6b47c82946`  
		Last Modified: Fri, 02 Feb 2024 16:16:16 GMT  
		Size: 7.3 MB (7277363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:b52d94341eb584e58c394c0c6055287af21bbc51c05c136281149ac7811a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3285837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9926ea383df2b53d843e6caa96157725e8f678003f194f06e3aac0c48292ec63`

```dockerfile
```

-	Layers:
	-	`sha256:7366fd8235e1256b5b152ede4d1c52375ec5b45149024901d9d8aae75c99fc92`  
		Last Modified: Fri, 02 Feb 2024 16:16:16 GMT  
		Size: 3.3 MB (3275992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfbcbcb4cf68d378788b0cb2a971f6b13372511d16e993295c785040a59e318`  
		Last Modified: Fri, 02 Feb 2024 16:16:16 GMT  
		Size: 9.8 KB (9845 bytes)  
		MIME: application/vnd.in-toto+json
