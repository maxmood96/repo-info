## `elixir:otp-24-slim`

```console
$ docker pull elixir@sha256:d6106871149b2fa749efeca9993e2c70a44c3e66347e891ea58ab1754061b6a4
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
$ docker pull elixir@sha256:7fe254afcdb69f97ec5ad713cf9670e3f59f75c1fc6b6300e11757d09d75302a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119041704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aa84fc098dabd8839249ef59509c7d6b347b1d0d4d87d893dcd06c73c39d99`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:28:07 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:28:07 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 00:31:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:31:13 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
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
	-	`sha256:fa66f55d0cca0cc0abd38c4a571b2a41d1efa1af0199f2064b690d120961331d`  
		Last Modified: Tue, 06 Feb 2024 21:46:08 GMT  
		Size: 7.3 MB (7278530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:fcac82cafad5d5b7f3601fd32f171420dee526ac6b709d7f9d025ab8f541abe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aa39bbd14869f88a21dff260e0e48de94aa4a9a511d03036944eb62c68f071`

```dockerfile
```

-	Layers:
	-	`sha256:aafc9e6ab8432ab23874e03cf322ab5a5957ae693e022683bf0ac00239a5a2ad`  
		Last Modified: Tue, 06 Feb 2024 21:46:08 GMT  
		Size: 3.3 MB (3277186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bcf7d5a6535d1114ca86750a166e5a1611bbecb5a74bf1bf89770c7afd0ed86`  
		Last Modified: Tue, 06 Feb 2024 21:46:08 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; 386

```console
$ docker pull elixir@sha256:582693298dee0a2633f7bc15cb9df8aa49b5a72f5852fc6b36ab19ac46f7283e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121002676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e99502397ee8268598d12b7eedee77aaa1c9ad707933f9662c23fe7348a81c2`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:52:16 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:52:16 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 01:00:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:00:03 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
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
	-	`sha256:498730d35d8cba8297bd4e63793284ea39dfef365e45c43b1a9c0af34e33abd1`  
		Last Modified: Tue, 06 Feb 2024 20:52:49 GMT  
		Size: 7.3 MB (7278370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:37656d777d9ccdbbc0c6ca9850ee16a87b3b681ed1fffcb5b0e9fba3184d87a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3283916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f279d5cd8809a3674ee24c99512e4592a08b0c10456af7eb2e413b019656e7`

```dockerfile
```

-	Layers:
	-	`sha256:dddd2195f489b9c946a7723c238c6b8858d7ea7d3bb36146c2da67d9175f024e`  
		Last Modified: Tue, 06 Feb 2024 20:52:49 GMT  
		Size: 3.3 MB (3274095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162a3f98e26c4ae9d671334331b0cb7e8107632c572afb346e82a75a3b297110`  
		Last Modified: Tue, 06 Feb 2024 20:52:49 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-24-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:9b7611dd87fd2dae4099f1cdad2eb8df1ee91f060cfcfb7f0ae8dcc49a96a166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124837895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf54ad46c40acb67a19d2fce2155978475b71482cbf8511b5640fd4fb1f29a5`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:32:15 GMT
ENV OTP_VERSION=24.3.4.15 REBAR3_VERSION=3.20.0
# Thu, 01 Feb 2024 00:32:16 GMT
LABEL org.opencontainers.image.version=24.3.4.15
# Thu, 01 Feb 2024 00:38:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2c014720eb2d2da7f195e4c7ced20b6e9eed664b6d65e2083be9e698e63224df" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="53ed7f294a8b8fb4d7d75988c69194943831c104d39832a1fa30307b1a8593de" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:38:21 GMT
CMD ["erl"]
# Tue, 06 Feb 2024 15:23:33 GMT
ENV ELIXIR_VERSION=v1.16.1 LANG=C.UTF-8
# Tue, 06 Feb 2024 15:23:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="b9e845458e03d62a24325b8424069e401cc7468e21143ecbca5514724d7cbaa0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Feb 2024 15:23:33 GMT
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
	-	`sha256:cbbda3a3abd4db25c950aaa8c1a7a9537c113ed99d6c5ddb4eb6988ccb1d867e`  
		Last Modified: Tue, 06 Feb 2024 21:30:25 GMT  
		Size: 7.3 MB (7279200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-24-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8b991ebf6b7fea95af1f29d98e1bfe853caf64673f8463cee839dc173043afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3290877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527ef89a20525c41c0a6bece522092485f3cc8881c87b9e92532d5d4d084e391`

```dockerfile
```

-	Layers:
	-	`sha256:cac1be1c5c2cf780b6df1597b1078d50a5a1f2de2509a7fe28ee9b93e3936305`  
		Last Modified: Tue, 06 Feb 2024 21:30:25 GMT  
		Size: 3.3 MB (3281332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1bb806f424dfb356c3103bd0d6efdb31d4cc092abba73e9861e917117e99ece`  
		Last Modified: Tue, 06 Feb 2024 21:30:24 GMT  
		Size: 9.5 KB (9545 bytes)  
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
