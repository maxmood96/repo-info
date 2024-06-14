## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:ba58f91b75297499770531a8a40a93ee9a2651430cdb657fe48b89b4d3d7ce9f
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
$ docker pull elixir@sha256:5f3ca5924285e3c2aea3ba0cc1122749564f093d6945fa4d987d6afe7e2d0266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128473283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfbfd50972ddfddb765e05a1de0f9ca4d73d0516e90f541b30783e8c5f1f157`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd9be3a9fd8788e50a8eb4a1f29604c6889e235190d24468eb56cca16c192de`  
		Last Modified: Thu, 13 Jun 2024 18:21:23 GMT  
		Size: 65.9 MB (65913153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c624e9bd4e09102edd59f2f14b55754e99a0c00bb7b20c186a47110c41cb293`  
		Last Modified: Thu, 13 Jun 2024 19:12:15 GMT  
		Size: 7.5 MB (7460940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c8312b57be711332515788ea4d7a3dfa4dc9de75bd11be565ad8ba7722fec489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759093f8f23c175a53ae554c489050e837e03e9e4308d35bec9b9dceb57cd3e3`

```dockerfile
```

-	Layers:
	-	`sha256:53e3b72f40adbf4397c953612844bc1f21764cafbb1b8f2e9271905acc770ecb`  
		Last Modified: Thu, 13 Jun 2024 19:12:15 GMT  
		Size: 4.0 MB (3959285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67392c86ad8170dff3333cc16052e8653fe3eef27691623f14a4882609ee2261`  
		Last Modified: Thu, 13 Jun 2024 19:12:15 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:5a7901e27992732353f4c47ccf8c33c5090f9b8564ce636d7f51625c6b2fc417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114926972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7caae418f9173a2c21a842769ccc9ba8fa09056a7423f8296737f8996fb8b91`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a387779b34c51e9b6820420e34f5326b0d6902301399edd60ef4d5809e0f33`  
		Last Modified: Thu, 13 Jun 2024 12:33:19 GMT  
		Size: 57.2 MB (57210116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325949dbe0e1e42a0fc18766ba283fc254cc434e5d10fa92c8f461c62ce50b6e`  
		Last Modified: Fri, 14 Jun 2024 06:28:48 GMT  
		Size: 7.5 MB (7460426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:79c08c38421dbf4c353f3e1838218a2c446ed5521bef0853bcae13affa85ea8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d74dbc714469f41878faa882a5b75af5f869952f867838efc4819f753a6e269`

```dockerfile
```

-	Layers:
	-	`sha256:15b147b9fc2f6ba79b68bcc3fbde09ad34f3bd7ec78e31cd4afaf60fb37a7621`  
		Last Modified: Fri, 14 Jun 2024 06:28:47 GMT  
		Size: 4.0 MB (3960876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e860b765ef941f48af0a355f60c8bf11812e32379310bf68b50bb810e81e0369`  
		Last Modified: Fri, 14 Jun 2024 06:28:47 GMT  
		Size: 9.8 KB (9836 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a86eda4cb196b8488dba636f071a6f38068b643e464ee3dc946bb035a611205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125483075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b42649e53159c1366146737277446f3d6b0b610aea1709654be52f3a8f7ec2`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34da9fa34bd411c48343fb5045696c1d8ea6c1843eb7ccbc81457ce1e7acf3`  
		Last Modified: Thu, 13 Jun 2024 12:41:59 GMT  
		Size: 64.3 MB (64282764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aa872a926038f4d6cda239589a69b1b73f302253bcb405bd2c75f1ce57e0e0`  
		Last Modified: Fri, 14 Jun 2024 05:11:11 GMT  
		Size: 7.5 MB (7460730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5c749f8f19c69881d035af56fad67e13aacbbafc3917c4cdda53252f10c0847d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8598907fafbd345db74e955e531beb58e0c3d6a5f923613c68efb648c6c2c90`

```dockerfile
```

-	Layers:
	-	`sha256:23116d4b797602d776a20302e022bb07ce5c680bb567d433b3de5b2a19514fb9`  
		Last Modified: Fri, 14 Jun 2024 05:11:11 GMT  
		Size: 4.0 MB (3958892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27cc7ad18cc96d199dd1ae2313050960975473b37e4c370e473a7d8b5ce0f6f`  
		Last Modified: Fri, 14 Jun 2024 05:11:10 GMT  
		Size: 10.1 KB (10140 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:2355accdbe21dff723fbc2795b65229641245a3116825341624c20af0d570c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121131928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fbff856ae4e5f521239d8dbe9802c93387441f507fc49e86fbfecb3f767cc5`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b06c705dedc849336a9cafaa3117e4cf0309a61e65bfb8e0c51162fa5b6e2d`  
		Last Modified: Thu, 13 Jun 2024 02:05:27 GMT  
		Size: 57.6 MB (57594879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357a11ad8d67607a4e29b7e0470acfcc88136e755cfddb2fbcdfc1f760a4bf74`  
		Last Modified: Thu, 13 Jun 2024 18:26:02 GMT  
		Size: 7.5 MB (7460511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a13c1404794d73e4384c1420a40501a91f6b3181bb2aafc717cec0e1576caca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4301af7c7296ac0a041356464796d3554e17ee470f04abc6c9dc5bfbb097347`

```dockerfile
```

-	Layers:
	-	`sha256:18588ca868253ec850d7e50d99e634a46cce6b5bba0bc816d4c84a8299d4f1dc`  
		Last Modified: Thu, 13 Jun 2024 18:26:01 GMT  
		Size: 4.0 MB (3955766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd079cda3711d92d95e94e2b3fe007fd81d273cc2cf960a81928242dd2680443`  
		Last Modified: Thu, 13 Jun 2024 18:26:01 GMT  
		Size: 9.7 KB (9729 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:53d1d768d9f4783ec868717a5ce1a52c8a99b7c2b6c8f7d28ad96f707d9139cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124953564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6792208f5f25f4839de63818fe7cf256589ee82f0425739f15f1944a1238a`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20847ef587c13250a262cd4060e6a00feff1bc70e64f3f207a53752d2e822572`  
		Last Modified: Thu, 13 Jun 2024 20:11:36 GMT  
		Size: 58.5 MB (58523426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f13044960647bfc3c7513349b6432b91adfa92dd66348d9633a3dff310152e`  
		Last Modified: Fri, 14 Jun 2024 10:23:34 GMT  
		Size: 7.5 MB (7461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f742b7c7280e4d7d38e4b79f265c7c1a8cad22632e5aa520aaa8c507ebf4418d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c8ba642c05b3b85e908781f19c709b8aa544d267b0af55c3469fe43960a393`

```dockerfile
```

-	Layers:
	-	`sha256:3888db2cdd71c817161b7ca1c078d78f2c2d6df6e7026c8d4c722038c6788d88`  
		Last Modified: Fri, 14 Jun 2024 10:23:34 GMT  
		Size: 4.0 MB (3963003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c63f24305da7711bc1c1ac06f0f89758bfa16b90c542fffd2d23de52c081cc`  
		Last Modified: Fri, 14 Jun 2024 10:23:33 GMT  
		Size: 9.8 KB (9806 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; s390x

```console
$ docker pull elixir@sha256:bb755ecaf609b7c9fe05af0edfa39989e6afb0dc88d6e85aaf4f6c34a904abc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118912836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f9f635b8088917ffbc38bc284315b54c7afdf36720b59b113b69ec024bc043`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 04 May 2024 12:59:04 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
# Sat, 04 May 2024 12:59:04 GMT
CMD ["bash"]
# Sat, 04 May 2024 12:59:04 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Sat, 04 May 2024 12:59:04 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Sat, 04 May 2024 12:59:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 May 2024 12:59:04 GMT
CMD ["erl"]
# Wed, 12 Jun 2024 11:57:50 GMT
ENV ELIXIR_VERSION=v1.17.0 LANG=C.UTF-8
# Wed, 12 Jun 2024 11:57:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="558f89cd39458bed1f945d87ad320e5d8f337fa9e627a8479aaefa0494a06ea7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Jun 2024 11:57:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da73b8b25ce2b2e406f4b7a8421c2841755c65771702dcabcc1294bf182ddd3`  
		Last Modified: Thu, 13 Jun 2024 09:16:26 GMT  
		Size: 58.1 MB (58114556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ad32a6e8538bdee49314d6e661ec758ca2d0573bdf0aeb2bdda180cfd6954e`  
		Last Modified: Fri, 14 Jun 2024 07:40:25 GMT  
		Size: 7.5 MB (7460740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:06bbf965eed49eaeed973f6bb2c290d475810ea5475892d671b3c1253af4e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a105a1ba2caab0828ebb45c86071d75e383d3d92ceb0b2fe2f43bdd72e866`

```dockerfile
```

-	Layers:
	-	`sha256:6042aa6330f1ec4ccee175bfaeb243554bf883debcdad88579716f8081dc1bca`  
		Last Modified: Fri, 14 Jun 2024 07:40:25 GMT  
		Size: 4.0 MB (3958850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be49dd6ff7fcedea571c01f01af1b4324486e74c7233a01bf5f4116b2e74092f`  
		Last Modified: Fri, 14 Jun 2024 07:40:25 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json
