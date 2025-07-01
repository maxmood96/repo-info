## `erlang:27-slim`

```console
$ docker pull erlang@sha256:051af6c314db2deb9d457e4f8415dbf8008ca8c4388ca61b6099a617d01e7cc8
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

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:c8f24260156938467fb8a12b221f17183fcbb731c3c9eaca0e1c958a4c207826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124467484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792dc4370b0dbda56ed24f45803babb8fdf9ab16eb55432f6c8c1084c73f96f4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7a5bb5c4ae49cb8cf35fb3af603de04e77e9a0f21d627aed995fbef16f7736`  
		Last Modified: Tue, 01 Jul 2025 02:29:00 GMT  
		Size: 76.0 MB (75973200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9077e9fe33f31468437809b0140c555930b946c16e97e3277a448800e17912b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef0ed925b33fcd9ef2311516279228eab27442eb4c0ea94dd4767e8ca940589`

```dockerfile
```

-	Layers:
	-	`sha256:65d7bad5f44ffe7b1d3c5547a3adcb22c421ca5aeac58e5c310cf4cd7f3304c6`  
		Last Modified: Tue, 01 Jul 2025 04:47:33 GMT  
		Size: 3.8 MB (3817423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f0df8c11c0d70ac4b3603b33ce7b428a2d27d95ba055aca4ed49f09b28e4fd`  
		Last Modified: Tue, 01 Jul 2025 04:47:34 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:d8f4e1c2512f1ece283bc0084ee366d935a67f3b5ff7a7de23d69237603c300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111504224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3494d0ba0437e8b663cbab030984617e1ecc09be7fe6a5d8351de2d98fe847`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:01d208698d30e75c289cb2ee99e5f2a75a42e11f8e1b4145f8fb1a881298b833`  
		Last Modified: Tue, 01 Jul 2025 01:14:18 GMT  
		Size: 46.0 MB (46026558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6cc59b0a374446263122014e1623474bade5390fd4a050e0e2ab378e273e09`  
		Last Modified: Tue, 01 Jul 2025 06:14:58 GMT  
		Size: 65.5 MB (65477666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6ce93e4e5245ddab0631dec7f5fe418419ebc1025e25456a3c8e9959246f1c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c338dd2a3f553a73ba4836c72c5145b2c3fb13c20efd9dadd76fa148fe8b52ac`

```dockerfile
```

-	Layers:
	-	`sha256:d2921cee0b679a356479b1f91c1754f18e078388e2b64bdd8e5c30db23f23fe8`  
		Last Modified: Tue, 01 Jul 2025 07:48:00 GMT  
		Size: 3.8 MB (3821231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824f8b33bc6362ac7cc6858ef02323f050f8b89f7bd0cc4838c98bc88662e1c8`  
		Last Modified: Tue, 01 Jul 2025 07:48:01 GMT  
		Size: 13.7 KB (13748 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:e05f1c2c69a8cf958d53665445c1c25f06d1b2e282bcb5e818f9636942cb8e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109312422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fb318a21ca283d9785a38f9bfa1339950bef1f9f39c2c98ea3749eb1ed9411`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2161a76c251a3a698f5736b9f4fd6a4e791070fb0f9b8fb1eced66e12c181c`  
		Last Modified: Tue, 01 Jul 2025 09:10:03 GMT  
		Size: 65.1 MB (65104245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d9e01b87b54cad9fa4b45e6ef4bee61f23d647eb2ff29d97f31797aca346a32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252d3e5fcc6b663f73d60075a1663b47cad56bd9ca500020cc18ac942a1673d6`

```dockerfile
```

-	Layers:
	-	`sha256:c04d5a5a50129c3667d634de91f2381aac7aaa2e8b7b20a18dbb9e26a789827f`  
		Last Modified: Tue, 01 Jul 2025 13:47:47 GMT  
		Size: 3.8 MB (3819656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299467d15ddf6e4f6fd2507e41179d74f5493216deddc7993513f52f5fe29eb5`  
		Last Modified: Tue, 01 Jul 2025 13:47:47 GMT  
		Size: 13.7 KB (13749 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:e1e2e615917c795935369446d3cc6c07b7b5d5e433c0406f00cc9b063a5fb750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122055162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7701c06fee4680c87cd801fe8758703aa419dd3d85e425263740dae253fe6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b85d7860de6f36288c412d16e3914064cd5f207fdf22898ec88fd9a75824e33`  
		Last Modified: Tue, 01 Jul 2025 07:04:38 GMT  
		Size: 73.7 MB (73716377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d07c7988901166b97143365c6dfd292ce4f862a85b3b981256ace81d06f13ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1385e4aa710246ed511178f4c17b991d1ae52cf1b24ed2d1c9513f38243dca5`

```dockerfile
```

-	Layers:
	-	`sha256:632a22db3a9cedfb5e2c390da56e7cef3a3899915f489db64d40c3e020fec816`  
		Last Modified: Tue, 01 Jul 2025 07:48:10 GMT  
		Size: 3.8 MB (3817684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3635169c2a7f5e8d8d03dca82bb5cf5c6795d11e68e5d2dbe35e222a9c95c1`  
		Last Modified: Tue, 01 Jul 2025 07:48:10 GMT  
		Size: 13.8 KB (13777 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:27e3463ff8251d8ea1411f3650974bc072f600483572d57c928bb6a58e23d026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115612478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa30326e970cd25187cba5e8860463e7da65140e828421778833a90a38be40`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048efaac54e832d1ae5a8298f0bff541347a9a07ee98975be9212166d7a68d9c`  
		Last Modified: Tue, 01 Jul 2025 02:27:37 GMT  
		Size: 66.1 MB (66135057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:049515868a6ad336c55a574be93943a98e8ee3c0f47f0ee864c5d3e83d9d394e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9778fa600fc881dc35514004883ba20e8e4f40467f65d556bc27b108c31e9c52`

```dockerfile
```

-	Layers:
	-	`sha256:0e4c3302ed3dfe4e02e82433cf475666bf96b8a3a6c6052bca8e90c4d40d6d81`  
		Last Modified: Tue, 01 Jul 2025 04:47:54 GMT  
		Size: 3.8 MB (3814590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269e26cafbd5a10770c8f61c103153b8da7d095bdb96f36757cab5326d057594`  
		Last Modified: Tue, 01 Jul 2025 04:47:55 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:efef93f64312e043e868b673242921870f6f72597d873341059af7ccd4406e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114834433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eba67fe678b9fe1eda1d10ca8019af755f9199fb0b7819f3dc9231a18ce5dd`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5beb05f99440ea86e08bd4b19d3542b860a617554445464f48762feb929d8c3`  
		Last Modified: Tue, 17 Jun 2025 19:49:58 GMT  
		Size: 66.1 MB (66058836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2af1d01500240453fe5bd573a239f2f353ecb27a26e87e07eb904ae68c60bc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da7bf5f7c7f31cb931baf5602e3c2b4a74afe91ecc7721c177d7b6a8441e4fa`

```dockerfile
```

-	Layers:
	-	`sha256:1f17d8a73a8f5f8ff4586bf371244c7870a134522886ae69d4226b6c96c1fd8d`  
		Last Modified: Tue, 17 Jun 2025 19:49:21 GMT  
		Size: 13.5 KB (13524 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:5fb1216682ac0c1062dba1349ff9f43e28ab820f774cb02abcb3d2906a7feb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119549683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01003de62ba730c257b434b0441cea4df81a9051753662890eb4566f96fb0e75`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a16337b4ac2b56de1b3b9e25444b33a157975cc775c5826d5f7527e05de7f`  
		Last Modified: Tue, 01 Jul 2025 05:17:50 GMT  
		Size: 67.2 MB (67212440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d5818edcdfaff53c18660861fd26d27a0111574c7a6ca46bd4d6b36f5a8b16b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9eff3d13ced76ce72abb8bbe4a12dec83f68100a557fc77a2a3c13582f7667`

```dockerfile
```

-	Layers:
	-	`sha256:ae749a48c2da60141e6c43a27e2e3b83d7674921318ab3a4d68de6cbcb142ad4`  
		Last Modified: Tue, 01 Jul 2025 07:48:20 GMT  
		Size: 3.8 MB (3821861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdab2b2b0a5480d012d8cd8228061727a99e3ccf031ea1c7756fc69e86c03f15`  
		Last Modified: Tue, 01 Jul 2025 07:48:20 GMT  
		Size: 13.7 KB (13717 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:6d7198290fffd070ca30c931cc12cd476003164c760a8f730ff19c4e06fdc8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113036687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4270fc5e232c86dfaa275de8800caa2fa3bd0e6619ca4eb33632fa12942ec4`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Jun 2025 14:21:25 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 17 Jun 2025 14:21:25 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Tue, 17 Jun 2025 14:21:25 GMT
LABEL org.opencontainers.image.version=27.3.4
# Tue, 17 Jun 2025 14:21:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:21:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111d99a1d1e7ef3d3a3b3c8047c086d9eb84f00413273ea9c4996188abc88e9`  
		Last Modified: Tue, 01 Jul 2025 05:41:02 GMT  
		Size: 65.9 MB (65887400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c628715aeb11d98b947b5d759175483cf4cc951458f42c94485d51b81ef55d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceff17d4a6d5b75a018fd6667c4764264b11b491f39492748272eab968cb0161`

```dockerfile
```

-	Layers:
	-	`sha256:0d741221f5770e679fea724ac9684c617fd282ab994e1a4a478511169cfc0843`  
		Last Modified: Tue, 01 Jul 2025 07:48:25 GMT  
		Size: 3.8 MB (3814251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7053c715faddef2e34a364d3be30bd0059a882385ce03f7b577ff8dc62f86bcc`  
		Last Modified: Tue, 01 Jul 2025 07:48:26 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json
