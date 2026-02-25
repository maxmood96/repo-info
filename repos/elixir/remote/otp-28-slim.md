## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:02a899e1db046a1826ef8423a3082cce75a719f694353968a297a91797d78e30
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

### `elixir:otp-28-slim` - linux; amd64

```console
$ docker pull elixir@sha256:0fb770c4d8124ce046a68c0bf0b688ff451401bf4d6fd427d29cf29f95c59f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136763989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2be1258e4b47cb958e85366239c7324cbbe4b9eab3063e44c91f19047c184af`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:56 GMT
ENV OTP_VERSION=28.3.2 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:23:56 GMT
LABEL org.opencontainers.image.version=28.3.2
# Tue, 24 Feb 2026 19:23:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="36380480aed888281b8202e75449cca307102e43c4e04696cc83bd3b162991cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:56 GMT
CMD ["erl"]
# Tue, 24 Feb 2026 20:18:57 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Tue, 24 Feb 2026 20:18:57 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:57 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de20244f3c8b82cc3cf691ac05b6139b43b369d1a4f7db7e262adb48fce5787`  
		Last Modified: Tue, 24 Feb 2026 19:24:10 GMT  
		Size: 79.2 MB (79234340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed2c513a2d1409e405fd4119732f7cd1f009493eaa59bcbb23b4c869bbe1609`  
		Last Modified: Tue, 24 Feb 2026 20:19:06 GMT  
		Size: 8.2 MB (8236525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:5b82549bacdbc676e65c6abe71d28d80d94430391b45806c4cb6a2a38081e731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ac83575fcd92078cccecee87bbc68cdb1eacf0c17dcd93ebc79c154fcec4d4`

```dockerfile
```

-	Layers:
	-	`sha256:300e03319b68d952ed25595751d58649319b47bf94be94faa47894473792fd21`  
		Last Modified: Tue, 24 Feb 2026 20:19:06 GMT  
		Size: 3.3 MB (3291500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6588ee483e853243cf242bd062656295a16709a16ebc365dd0c39e4018ec2f00`  
		Last Modified: Tue, 24 Feb 2026 20:19:05 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f6accbef4576ada6a78878da5e0e75aa45b78e362875880403ecc559854408e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122339566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4e81eb391d50b616f79fe8601192cb4ae874dcad29e1b5025541c9daa4eedd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 19:26:05 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:05 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:26:05 GMT
CMD ["erl"]
# Thu, 11 Dec 2025 19:32:43 GMT
ENV ELIXIR_VERSION=v1.19.4 LANG=C.UTF-8
# Thu, 11 Dec 2025 19:32:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a2df9d5411fc53d97ec17c069765c8fb781f8dc36c4e06ec1cd4b189340d364b" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:32:43 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:36 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656ea89dded4641f3cfae04edeb56bdaf27e5ade23d29c71bf377d6a3a515ba`  
		Last Modified: Thu, 11 Dec 2025 19:26:19 GMT  
		Size: 69.9 MB (69914283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3ec9fdf6f8b1ae613d7be87812d54981fde7d283bc33846ffa3f063fbcc541`  
		Last Modified: Thu, 11 Dec 2025 19:32:52 GMT  
		Size: 8.2 MB (8229217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8f3b2a4122b9a5a1694cb65d9c7cd07e75a9e6530c1cf95b50b06436e8c0792a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390627936dc7b85bd98816d23d76cafcd18b5b9c2dde6e95841e59aeb941b53`

```dockerfile
```

-	Layers:
	-	`sha256:c63c272c4fb8b225f629fbd2f263674829952f55b1addc9d49c7df4c90dc3e36`  
		Last Modified: Thu, 11 Dec 2025 19:32:52 GMT  
		Size: 3.8 MB (3834131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd70870664af844fbbaad7e9c82c23f811169c54fb03e5c54d2559afab12a79`  
		Last Modified: Thu, 11 Dec 2025 19:32:51 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:d5662d0a88f9251d12bd89267713b8a978cd9b123a20ba6e2e7ee9ccea5b23e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135185297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38334e3c53331975ae5e7c273ba12775f77d1b33bafb76a6f5c457644503ed0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:28:36 GMT
ENV OTP_VERSION=28.3.2 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:28:36 GMT
LABEL org.opencontainers.image.version=28.3.2
# Tue, 24 Feb 2026 19:28:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="36380480aed888281b8202e75449cca307102e43c4e04696cc83bd3b162991cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:36 GMT
CMD ["erl"]
# Tue, 24 Feb 2026 20:30:31 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Tue, 24 Feb 2026 20:30:31 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:30:31 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ce678cd81a9e343b5e4be71e1019b3a0b8513652c3e60a63afeb4a4065163a`  
		Last Modified: Tue, 24 Feb 2026 19:28:54 GMT  
		Size: 77.3 MB (77296914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb602b55b6f7dbb2d7b2c529e741f1c5eca43756145c325914d8f9b7fd7296ef`  
		Last Modified: Tue, 24 Feb 2026 20:30:40 GMT  
		Size: 8.2 MB (8236215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:cca2d0141d8f297d44588a5a4bbda7cb1122a4d789d8c8e439d93965143c7aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491d021d51caa0ab0dcd90bb29fcc6f18ed99798f5729e23f72a8a81ad654176`

```dockerfile
```

-	Layers:
	-	`sha256:f4ba2a3ce3baaed2f5f9a40a778465fa9419aefbfcbe55e11632eabdee39d52b`  
		Last Modified: Tue, 24 Feb 2026 20:30:40 GMT  
		Size: 3.3 MB (3293047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a07f75d2ed6659f5ec75222101e598f2184abcddc8788b3fcd2dcd30211fe0`  
		Last Modified: Tue, 24 Feb 2026 20:30:40 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:6f99337b9b5dce9f75f8b141fc48bc6885fc1a79fa1661cc9a440f4ab681a67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128387697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb911c9df062a6f993b227673dc79976ce66f04d24fde18ba9ca73d252f46ce`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:59 GMT
ENV OTP_VERSION=28.3.2 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:26:59 GMT
LABEL org.opencontainers.image.version=28.3.2
# Tue, 24 Feb 2026 19:26:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="36380480aed888281b8202e75449cca307102e43c4e04696cc83bd3b162991cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:59 GMT
CMD ["erl"]
# Tue, 24 Feb 2026 20:09:34 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Tue, 24 Feb 2026 20:09:34 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:09:34 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823da522dfd7522d49e7373730e46f8d574c3ee9ef7856cbfd91396fd3f5ea1f`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 69.3 MB (69346341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246e6ad1af7b1e95ba56fb45dca593fbc111d74a73df305a12284e49c46c179b`  
		Last Modified: Tue, 24 Feb 2026 20:09:42 GMT  
		Size: 8.2 MB (8236084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:fb230c75ca07cde197b3ba536aca971972fc13384d17eb3e7b81d44813797153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad1269dbb5f7d65e90b394d3568349db2b70f4902a1db0074e85fad3f54485c`

```dockerfile
```

-	Layers:
	-	`sha256:723d8cc3b8322218d536e71f9360e372994b8f16a7207e6c637cba0efe2d4707`  
		Last Modified: Tue, 24 Feb 2026 20:09:42 GMT  
		Size: 3.3 MB (3288665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2bd7f0f58a9c238ad6e6eae4005ad4cac720f0e1e71b59b1fe4735b84562dbb`  
		Last Modified: Tue, 24 Feb 2026 20:09:42 GMT  
		Size: 10.6 KB (10594 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:457530c372e634e4e88d2d0560a114e280194ca8d79d4ba162b05ce3bccff3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131661799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34fd53c3dc0e3ffbc0ddd0f486dc0a624589e24a6b70a2abf88130e6416edf6`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Mon, 23 Feb 2026 21:31:06 GMT
ENV OTP_VERSION=28.3.2 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:31:06 GMT
LABEL org.opencontainers.image.version=28.3.2
# Mon, 23 Feb 2026 21:31:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="36380480aed888281b8202e75449cca307102e43c4e04696cc83bd3b162991cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:31:06 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:48:58 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:48:58 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:48:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae086789372e97a82a2c92770ab0799b8d3f3cc61f01a441455c38f6e2055457`  
		Last Modified: Mon, 23 Feb 2026 21:31:36 GMT  
		Size: 70.3 MB (70313031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c579101dfb4a51c67ed9376a7aff53c5b25e241b07faf9c9304ed7b6b16d32`  
		Last Modified: Mon, 23 Feb 2026 21:49:14 GMT  
		Size: 8.2 MB (8236653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:97ae371fea9c40f67dcf08eeca77e762af6337d4b116c7f21145adc21492b531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf03d1396dfae6974341991bf4f36fc39d9afd92be78541314bbe24ddf84f07`

```dockerfile
```

-	Layers:
	-	`sha256:6023c5fad049352ade476e8e5086b5ff9e84f29529ae79f920de8003b17a5520`  
		Last Modified: Mon, 23 Feb 2026 21:49:13 GMT  
		Size: 3.3 MB (3295097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a5d588624bcb03744eb774d66958099003f50f6fb17e50642bc87a21e8a93c`  
		Last Modified: Mon, 23 Feb 2026 21:49:13 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:3f4d8693dd67628849d4a7f0682d78dc470d70756fde05afa878f9ab17c78a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127792254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eea7bedec528e9f38ff033b47dd58164ae489d33131a09d8f3c97e4dd4bec3`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Mon, 23 Feb 2026 21:31:59 GMT
ENV OTP_VERSION=28.3.2 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:31:59 GMT
LABEL org.opencontainers.image.version=28.3.2
# Mon, 23 Feb 2026 21:31:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="36380480aed888281b8202e75449cca307102e43c4e04696cc83bd3b162991cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:31:59 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:41:48 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:41:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:41:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bd39aef0c98771b2658f3ef42cebfae76c2592dacf426e52bd2a0c933f3719`  
		Last Modified: Mon, 23 Feb 2026 21:32:27 GMT  
		Size: 70.2 MB (70201257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb513a27ceed2974686d8cd31bca637c18fb1be12df17fee8204af570d2e788`  
		Last Modified: Mon, 23 Feb 2026 21:42:10 GMT  
		Size: 8.2 MB (8236619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e44e7f670694e2a599b1b8c7b6e444f66e61bd837cc4eab67c95d7f0a88a1ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5871de2902073cb9d61df2edae96ed48046fd226d4ef44f9500e84b652d6be48`

```dockerfile
```

-	Layers:
	-	`sha256:27835d3bac2dccb56bcd9b65c0d81a8b47ef07e285ff9b8bfeaf83be0fae1c1c`  
		Last Modified: Mon, 23 Feb 2026 21:42:09 GMT  
		Size: 3.3 MB (3292941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474151d852c133ba1e476ccc566611ff9c18086f4e81630add86efe5b939c15a`  
		Last Modified: Mon, 23 Feb 2026 21:42:09 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.in-toto+json
