## `elixir:otp-25-slim`

```console
$ docker pull elixir@sha256:43d06bfa467b21a9f0930f0a8274ae18c45c05a841e9c8e652a7b6cf0d9c6b14
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
$ docker pull elixir@sha256:56882014a08ddf9c494c8c31fdb64805ccce8a0160c57e164ebeb445d449978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127733685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5286bbaf467cd411d329bfba1e0b7cbefcdd38f3de79d0bca1ba099463f02c41`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc7d3392173cba7a840209979ca50f29b45bde2ba1d9209a640ae6a046689d7`  
		Last Modified: Tue, 01 Jul 2025 02:32:23 GMT  
		Size: 65.9 MB (65944976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec55724582902a37aaa535b47f76a275891738d0741b0ea0c322c1500aa655c`  
		Last Modified: Tue, 01 Jul 2025 03:27:20 GMT  
		Size: 8.0 MB (8033887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0db9fdf58e7a8c4eefc97ccc558d5e1fa18f6c6b50741ecdb85a64421b0f0269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f336af9b217b48ea11ccc30b9b5cca5463b102190614bac0be66d09173c7ce`

```dockerfile
```

-	Layers:
	-	`sha256:a91228653c18ef1731b5e24926a16c87fa0fe7bd1fe267ce9f2cf3fa1ac8d14a`  
		Last Modified: Tue, 01 Jul 2025 06:47:27 GMT  
		Size: 4.1 MB (4105914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9789e1d2511246443def0e4d5842c9412a19401474fc5d29ef2936f20b4a30cb`  
		Last Modified: Tue, 01 Jul 2025 06:47:28 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:1b8eaada2879a1259f19b5dc2a8867d46897e7ce14f834ab60bf5feb7d47500f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114338139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59250be292629be3c3d1e4811179c7690c1c949f3516a2cd8d7e11fe44500dd`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3434c8e2976c2ecb637bfdc4ebe281806a06d4d57e6cdbc105e6f7735fecdc63`  
		Last Modified: Tue, 01 Jul 2025 09:20:09 GMT  
		Size: 57.3 MB (57260653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd40be26779680ddcff460280612a75d8b50f652ad39575876e26261263db19`  
		Last Modified: Tue, 01 Jul 2025 20:40:39 GMT  
		Size: 8.0 MB (8033526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ac641362e935717775ae189b038e040430810c133457fc10d09645b8a6ee2248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875b8c7b7c175cc14ab8b0ea89bf001c5dfb499b53255eca1d4b46c0d6f4bebe`

```dockerfile
```

-	Layers:
	-	`sha256:d36041ccfd3a7d946b62924edbdc3d2f92ae547bdaae4d9989092c1144d3e657`  
		Last Modified: Tue, 01 Jul 2025 21:46:58 GMT  
		Size: 4.1 MB (4107507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6ee1e4ab83768ed160fc0acbf7b75d502b9a5f2e6b93197c2e1faaa4ad3961`  
		Last Modified: Tue, 01 Jul 2025 21:46:58 GMT  
		Size: 9.9 KB (9858 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:16730a6fa2e5ccd557606504bb415870d69aa6d35e1892109dbb20aa9ae9dc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124631021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0291f1ede56e3487e8226960eef9a6bb4f583cd4af941400cf908939bbe1d6`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca66fa96a5f64d363e82f5a997d43d9777531b3495b83dc0c66ac6003c4e0e36`  
		Last Modified: Tue, 01 Jul 2025 07:12:14 GMT  
		Size: 64.3 MB (64345078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c74273e0979139de260b0481b0ade7ca0310f4de1cb38962f333dc33c940bd`  
		Last Modified: Tue, 01 Jul 2025 16:27:56 GMT  
		Size: 8.0 MB (8033689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ce66b25c635b39239e8a6b076dea43ada85c8091d5ca5d06e21f0d77d24db819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f66d5021c6b436549aa648e9f355dd6a1d9e4928608c768a14626fa16799fd`

```dockerfile
```

-	Layers:
	-	`sha256:3ccc4c372a6feb00443127afce4bec879d7088499d84003e11054249549ccafc`  
		Last Modified: Tue, 01 Jul 2025 18:46:52 GMT  
		Size: 4.1 MB (4105523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba891b2e473078e27d0f7aefbf224b1c18b6398bcc3fc42eb0d204ab279d1721`  
		Last Modified: Tue, 01 Jul 2025 18:46:53 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25-slim` - linux; 386

```console
$ docker pull elixir@sha256:68967202fcd7614084c953b1aea6f8cee45239c06b2b160dbf55703b210cc12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120352638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceded682e31792df2b7082edff3ba23a1ed21377bb742d3c9f2526a5c5c04488`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 19 Apr 2025 03:05:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca5d0338676c3112c2bf0672591fc57a6fc24e3284c542178f66b5049fb6d62`  
		Last Modified: Tue, 01 Jul 2025 02:31:04 GMT  
		Size: 57.6 MB (57629121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbab8ce698720e0bcb5b6616f3f3295f164af11098e169156e6d3f7fc8cc93`  
		Last Modified: Tue, 01 Jul 2025 03:26:55 GMT  
		Size: 8.0 MB (8033583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0e55d87a8a32ccef62b354ff68db32df488ca9535be198ac6bdad38109599adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbe89537251ecea98b7de4eed7d035d19d03e456767acb93529bcaa77df83a7`

```dockerfile
```

-	Layers:
	-	`sha256:a9b7ee30c336f3dc023fafa39cadddb9e57f8975030f9e2ec018b3a7dfa1e402`  
		Last Modified: Tue, 01 Jul 2025 06:47:44 GMT  
		Size: 4.1 MB (4102447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a5cba05dd26346e93f3d43d766a503fa1666442ac36a3b7a7758d53213402b`  
		Last Modified: Tue, 01 Jul 2025 06:47:45 GMT  
		Size: 9.8 KB (9763 bytes)  
		MIME: application/vnd.in-toto+json
