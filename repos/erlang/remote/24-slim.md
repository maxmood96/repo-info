## `erlang:24-slim`

```console
$ docker pull erlang@sha256:6a3f50740ad65240957b5823c863e3d7acde414d692a7501b7fef3c3bced826d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:c6f968649bd339af057988bad521663655d275db52014ff81bde5b7df4b26ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120327109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718e7dba57e6f1c8a9bf1a144f8712301dbfaea2456e4741c27b4eb664e26191`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3a8834756287caf9b449d8f91fb5072a261df1ea1be0b9efebf9418b49985`  
		Last Modified: Tue, 23 Jul 2024 07:25:36 GMT  
		Size: 65.2 MB (65242531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1da2c3683e8aa15b5f0299ad0336222a332619673d1c7c65da43191ad4b0ff03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b24511a313680f07a3114389633a565e72928f626ff130093e070a5d2b8eae`

```dockerfile
```

-	Layers:
	-	`sha256:95f4bebf86953f731f5b17cc1110d4e62c1dcfec8575f9bf5fe85e337cec4b0c`  
		Last Modified: Tue, 23 Jul 2024 07:25:36 GMT  
		Size: 4.0 MB (3979766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb3960e4b829c432235755890641f4b3a4de92eb1a5ceea6b72c9d4c8c68349`  
		Last Modified: Tue, 23 Jul 2024 07:25:36 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:9360c91b80f04812b0c11070a315213c54723b1106ece0a23732b1b5da44baa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110024463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241d805e6bcf0f2a1bbbaed128b0acd4fa9f73e8747700b6f5abc79b49b2c6b5`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9d20f76e70352c40381cd21d631e8182899f15a46f0998354a0be0a449930`  
		Last Modified: Tue, 23 Jul 2024 07:41:13 GMT  
		Size: 57.4 MB (57435502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f771b90331a4c571605f57a5dd3d77f8392c4682a3b3b9e4349a2a55ffcb2581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d9512356bfd962002d60dc4d5345a25cdf6f7facaa7c5f64c7e3a557b4fba0`

```dockerfile
```

-	Layers:
	-	`sha256:00700b5e6fa16b85ba832c9fa755a6982f3cb50aa258a2e0bb68bbd07aa0d0b1`  
		Last Modified: Tue, 23 Jul 2024 07:41:12 GMT  
		Size: 4.0 MB (3979367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4753416cdf446251b5088b8e6bf62e942dc5232e4f91c0d0eb385a3f0efc437`  
		Last Modified: Tue, 23 Jul 2024 07:41:11 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5677556fee775c81c75b152dd78ac29181e1e8fad966c738c7aa4ecca017d9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107464033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed1db226491337eb61f0e21401370027ddc218821612f95d1d41188f4855642`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2ebc3c27eff879cc099e70f975be0e137694f5ae36812b89bd56ce26f967cf`  
		Last Modified: Tue, 02 Jul 2024 07:54:07 GMT  
		Size: 57.2 MB (57225035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:676fdcc6f51f758639a2153a61fb2272a18963863767e02de27535efcf797c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a698a2f8127079fded46084e7f83f5a771d956bbc60d8ed2c9ebb57650d009c9`

```dockerfile
```

-	Layers:
	-	`sha256:f7eed1169f023ff6606ac2d52fc9c155394d65c272a900ae53212a6281f91837`  
		Last Modified: Tue, 02 Jul 2024 07:54:05 GMT  
		Size: 4.0 MB (3955397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e0394a230b2fcd43fbcb560600ddaf637d41d787e650218cf4c45f46bd97fe`  
		Last Modified: Tue, 02 Jul 2024 07:54:05 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f5eccdd1ddeec5fa484576e3b0977f9ac0c9c554da82cfe2865b65fbc35d1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111798079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bdd799f49e9078f374dd43e025809b6557b85c4167fdbc3c39b39bb54f47ea`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae2f80c7b560389bef28fb1f204f4df52a1c54846c8e9c6489aee086481935f`  
		Last Modified: Tue, 02 Jul 2024 11:13:47 GMT  
		Size: 58.1 MB (58076426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7665859db0e0916ac75fcbc146b5e42bcad1e9d007fbeb1f29af2697215fd82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ddee70cf79b0dd8586d3d07ff3b6f86a3ea602419a323edbbff646040bfc7a`

```dockerfile
```

-	Layers:
	-	`sha256:0f96c521205beecd92cdcc0d267ad46c503d64ea253167ec684bc33a8c3314cf`  
		Last Modified: Tue, 02 Jul 2024 11:13:46 GMT  
		Size: 4.0 MB (3953417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02955bedc84cc5ac5947e1ac4ecd4a351b62baa31ff7b775e512275cfd438031`  
		Last Modified: Tue, 02 Jul 2024 11:13:45 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:d7d500f8bc48545bfcc4819612e0d3c405f20393a6ed5f951301370f5a859db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113779019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654ac7be3eec10fb61425d874ef0751bc60fc5a8dad92d9995ea3075dd34bac`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73976802e6b72d34d6f9f680e026ac163b98191eb5099429c7a27c6cdba3d53`  
		Last Modified: Tue, 23 Jul 2024 06:19:44 GMT  
		Size: 57.7 MB (57704849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:211bb36f5a6d438803cbc90ac7af11bd0e6d8bf204e4126dd778fd99084b2290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639d3425cf621d792e533efe40e3f7f0fd6cddfad0a5ee61f95f0a498cd9c0e1`

```dockerfile
```

-	Layers:
	-	`sha256:5c204f0612e891365f2d96023aaddad1ec2e5faa09ad15b867a8c7b66043e96c`  
		Last Modified: Tue, 23 Jul 2024 06:19:42 GMT  
		Size: 4.0 MB (3976242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cb1107793e38b0a605207f91f5c6fb1831c7baa5c24bb4cfda9b8b18c00df0`  
		Last Modified: Tue, 23 Jul 2024 06:19:41 GMT  
		Size: 13.3 KB (13349 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:18758f4e57136e4f3da07bcd74e0327f78d30f15ef223e5231de7a2678394424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111631660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b88f70396f3c4446d1977956aabd5efb1cf4b6cc49df274bc2f884a7c506b2`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8801b1821ed40ec7ccb6c8ba2d96e88cc97e8928bd26c45028d19e660e8161a`  
		Last Modified: Tue, 02 Jul 2024 21:23:45 GMT  
		Size: 58.3 MB (58325456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b132dc752fabec9576e20b44be7e77316c66b21f7c3a33880fba382545b50336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1571a57b1229ba442ca5b26f958b86b0c8f528a355d27664c85580e8973bba43`

```dockerfile
```

-	Layers:
	-	`sha256:d0a8472a947f969e5c751c920b9e15c49ce1e29b80ad84400701c0b661ddfbaa`  
		Last Modified: Tue, 02 Jul 2024 21:23:39 GMT  
		Size: 13.2 KB (13216 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:5cb1cfc6ccdf5753c5b63630e1932c4bb3a189f0cc4e7a2d5b6b926eacd9d1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117607499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d19de44d36825a8be762bfccb13c1393a2ad0fcc95298ee6dc3524b4180e5`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f6e2dfa1c02dbc342f8ad1af2b279c2e8fcb540cbf5279e7bc747058bb9de`  
		Last Modified: Tue, 02 Jul 2024 08:18:21 GMT  
		Size: 58.7 MB (58657102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a89e18313dd474e72d229aabc3ce956f9bdf0976e983fd210c4cf9d18e854c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d85a7a0acac2052afda7d4deecd56308cb4ae3461bcd9abff1e9082e534fc6a`

```dockerfile
```

-	Layers:
	-	`sha256:239d691e7e55f45d1396ffe1d4db62463540bcf7474a5cd010b21bd94c9ff223`  
		Last Modified: Tue, 02 Jul 2024 08:18:19 GMT  
		Size: 4.0 MB (3957522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7821201d522a6ad5b610e130e1aec8d3b5d2caa7191400585b41fc61b11312b`  
		Last Modified: Tue, 02 Jul 2024 08:18:19 GMT  
		Size: 13.4 KB (13415 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; s390x

```console
$ docker pull erlang@sha256:197a7b47677a6a7a8a7e74729624e887dc5a7be4d04746d9fd6a45d25fd333cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111503271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2727ff536ef53b5effa24c1b2255669a692a3421139f3facf9d0d9811f90b2e`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa189050fffcdee3a07ff79c18e8a25b59b1b7f436454a4529060af22cbac3e`  
		Last Modified: Tue, 23 Jul 2024 10:20:52 GMT  
		Size: 58.2 MB (58179179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8a1592a986d3da308a54391e493b7a15ab9832eae31742976dc471fbfa3301f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec701dc8985c02c6dd8ed53ffe23da9ae08a8b4f6057f98191eed20cd4433460`

```dockerfile
```

-	Layers:
	-	`sha256:7303296ac6c423e82d3dfe6de90a3abdd5169095f79e3171db13061d44204bad`  
		Last Modified: Tue, 23 Jul 2024 10:20:51 GMT  
		Size: 4.0 MB (3979331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7264afe4662a42b82c8e7beae1ca2e7cc3d8fae93183f140e1bd1bbff607d563`  
		Last Modified: Tue, 23 Jul 2024 10:20:51 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json
