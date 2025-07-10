## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:adaee632d01ad216f9902129fec054271fd61632c33dda23588527781e6f6e4a
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
$ docker pull elixir@sha256:c25663ab0a7663dd3169cd2e5b95e76d8569e583a66821c1237de4b476505620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132405921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9b48b545b28e2782cf3ffa884cdc2a14048ad3f9454c3abf5eca0722b1e1eb`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf4a69a5d940568cdc592aabd0ecd9242b22249957d715c0fe1d709d1a00726`  
		Last Modified: Wed, 09 Jul 2025 20:40:16 GMT  
		Size: 76.0 MB (75982781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace5b8cf7b6c53ddc8582e061c094fcff6d7d7aaaab4fa41986054b83bedc39`  
		Last Modified: Wed, 09 Jul 2025 21:09:04 GMT  
		Size: 7.9 MB (7928856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:462cea0350e9d83e7ac3c7a457cf06d3ba03affbb5ce70f172effa55aac93632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6390106bc10aaab4ffb32a6e4b9f03e8507f754c5952a455958d356b845128e`

```dockerfile
```

-	Layers:
	-	`sha256:15d9fcc0cb1c3f8b675d25a07848859fd37997a18bd410ee829a447640a8de9e`  
		Last Modified: Thu, 10 Jul 2025 00:54:03 GMT  
		Size: 3.8 MB (3824493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1582658b1ccce3f142cc3944bb39fe519ce5c8eee6fa63794a18547b046804d6`  
		Last Modified: Thu, 10 Jul 2025 00:54:04 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:5a56231d29c299bbb0c44d125babda269d4693f3e37644824dbbf25158b86932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117247418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616da6bde75e7448f82440238d1aa1b6080665a27d3170c4e2446c10e43e207c`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9bab2223ba30ab699812418d2fd3c7b4fea0d9c854af66e6e2633d68c6fb90`  
		Last Modified: Wed, 09 Jul 2025 20:44:33 GMT  
		Size: 65.1 MB (65111214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc8ad33638299c8540c47f352d755ea6abb256edb14fdab0c5c33c74afba8fe`  
		Last Modified: Wed, 09 Jul 2025 21:32:07 GMT  
		Size: 7.9 MB (7928027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:4282decfb041dcf5ef83cb13da60e33665a7df1fad1a09e55c27eb1540ca85e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73762ff35b5494956cf3c0010da52a9ab0257e40b0722b81d17483b1108232b4`

```dockerfile
```

-	Layers:
	-	`sha256:80fb28b67012c8b02c886a8a06d15d7fd514ac238abd15e47164bc9f1984816d`  
		Last Modified: Thu, 10 Jul 2025 00:54:09 GMT  
		Size: 3.8 MB (3826718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afdb74e52b6ab08a34d2da6e0cbd695af9035ac47088811ffdae02fdf5362f1`  
		Last Modified: Thu, 10 Jul 2025 00:54:10 GMT  
		Size: 9.9 KB (9857 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a919e6c6bf9656379b041cd2783fba440f26886703d0f8e78cfc2e1b42161c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129993148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f7076ec7a041a65d17ee66a4056cb38050e49bad860e7fdfaf5c4c529f6005`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275006d690d9bdb425df8d258888a677e4fbcbe50d6be5ac1a61158ebd095830`  
		Last Modified: Wed, 09 Jul 2025 20:45:01 GMT  
		Size: 73.7 MB (73725567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db288085bdfc65d315924ae5b6747bef9e87c3c064ae98e240b1fc006a6b4ee`  
		Last Modified: Wed, 09 Jul 2025 21:22:56 GMT  
		Size: 7.9 MB (7928796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a576c2473bb475b3ad197b65d9a5f9a3ced6d07cdb9feda7d2d87e7c50771410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a80d5624b4108e5848c41977dec91ab267990c1f8ef35dcd1e120e6cfa341e`

```dockerfile
```

-	Layers:
	-	`sha256:09f5bee09a617b11aac152e6e30db362a4d27b76a678fff762960af580790f74`  
		Last Modified: Thu, 10 Jul 2025 00:54:14 GMT  
		Size: 3.8 MB (3824742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e851eeb033da24ca7351f0c007cbc67c1571db337d8b4472c36ae86b73a3c656`  
		Last Modified: Thu, 10 Jul 2025 00:54:15 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:f273987ab63334afc19fca8d3d0948e7c9481f41a7520f5427a3b192780c3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123550354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c6ea5c2eefcde7fdef0028f0ae1fb23ba7755f6c5a4eba2df9594c068d5bdd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d9564c7df32065d2126d08de8ec1f5a50e2009de1ea87b05203fd67c2d224`  
		Last Modified: Wed, 09 Jul 2025 20:40:19 GMT  
		Size: 66.1 MB (66144768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7619529a73e211b9bbee22bc2e47e3de0256278590cce3b20ee3f5cd8add15e0`  
		Last Modified: Thu, 10 Jul 2025 02:03:21 GMT  
		Size: 7.9 MB (7928165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:76b0bfcf6480cb7153cff7883d48c6a48a80f90e471681c0fb15f58f48492362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041a3eb63625147adcf979a11f560ee09e8a517c107f5383355b971153991c53`

```dockerfile
```

-	Layers:
	-	`sha256:8befdc1362627c23985941090122f5c5fe17fc1c2edcd68665d4bcaafde905b1`  
		Last Modified: Thu, 10 Jul 2025 00:54:19 GMT  
		Size: 3.8 MB (3821665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242e429cddc0befd7e13286c37a65787d978505dbd82e81a9054e6d225f68ea8`  
		Last Modified: Thu, 10 Jul 2025 00:54:20 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:13a7c47bec989b5974539a5f99e380c727da62ac4806bbc60eb55e5896f84da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127487693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7477ddfbf9e8a0358dc4f66d639aa3f9423c412c4c738d51a674bfb81215a0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d3bc1409fbd320509bc0e0419ed0b83ddf667c72bbc26e61450ef6f3f7eaf`  
		Last Modified: Wed, 09 Jul 2025 20:47:17 GMT  
		Size: 67.2 MB (67221553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236bd10525451ef1b699a5c717eba982aba036b1003f27de302d572425af37f4`  
		Last Modified: Wed, 09 Jul 2025 21:24:46 GMT  
		Size: 7.9 MB (7928897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5009b8049ab99abf008a17a103e48fd95c4f79caa65981c9156f8b5aa0f4e130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8999ba1399913f490db9cfe3d1722bcec50aa299b76eb63a74268cbe98868`

```dockerfile
```

-	Layers:
	-	`sha256:a2c9f3989866a34f5faa41f221c789f3090c31128d033e09c798c605f84b2e30`  
		Last Modified: Thu, 10 Jul 2025 00:54:25 GMT  
		Size: 3.8 MB (3828925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9be5a09088506c4b755aba9b70c6286f117efa978453ccc490fc753671de05`  
		Last Modified: Thu, 10 Jul 2025 00:54:26 GMT  
		Size: 9.8 KB (9827 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:8b80c88936ec5d0560b33a03306aba1dfa1ba4c76a7781a9f8ac5deb36340e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120972167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437d3930f1ef1e5f001f9916e54e9b3640c4b7c635bff9afd5d4204a19840bf`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=27.3.4.1 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=27.3.4.1
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2672f0c52b9ff39695b9c8f99cd1846ed9e47e21cd5b045ccdd08719a3019652" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["erl"]
# Mon, 30 Jun 2025 17:24:21 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 17:24:21 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1879b32d969f91c74341ca8d0d9c435eaf121ad393ad204b9e70d42a2f75340a`  
		Last Modified: Wed, 09 Jul 2025 20:53:21 GMT  
		Size: 65.9 MB (65894846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6732e7d12cfe59b08dd27587ba40d40be4bacd511a187f675102149f67acc4`  
		Last Modified: Wed, 09 Jul 2025 22:53:01 GMT  
		Size: 7.9 MB (7928034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8a44d7c69413ed95b9e5fa13bbfe868a0b6bb45cb8fb4b2492195a84da3d23c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe6d24c94cac3698b42db73893c610eaa81ed2b1c0956f375ca8178805f9eb8`

```dockerfile
```

-	Layers:
	-	`sha256:a4bc1906d844cd1476052dd220a9e570d0cfdff227b8b9e7687ffb70a9ea14ab`  
		Last Modified: Thu, 10 Jul 2025 00:54:30 GMT  
		Size: 3.8 MB (3821321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd61ab0440121610e1dbe2d0051652022587e41035cf98f0dd8419d67e7153d2`  
		Last Modified: Thu, 10 Jul 2025 00:54:31 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
