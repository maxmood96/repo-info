## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:a85685020eba6cf27771964602230ab8a31beeea11b35dbb0903d10ecf02b4d7
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

### `elixir:otp-26-slim` - linux; amd64

```console
$ docker pull elixir@sha256:f13516c3c67967dfc5c14d33caa18e04a79d0ee039a3845840187b7e99e23779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126820564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da437637ba47be1d83eb45ecc9840719951590ce37f2390fac559df42abb2c64`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb470bfbeb52bf64f53c232fa4977d6b9b55097c7f33f146126b6243e3594e9`  
		Last Modified: Tue, 17 Jun 2025 17:11:01 GMT  
		Size: 70.4 MB (70398416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ca163084afa10a9f11634473ea67419fd12a0f78bf290fa7f0ad9cb3dd699`  
		Last Modified: Tue, 17 Jun 2025 17:14:23 GMT  
		Size: 7.9 MB (7927876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:23d6ab2ed328f2f824e1374ee212cc7af2535c204dec0df509a6d5ae9827da1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ceb880664ff670a0d685b3b78af2170f99501ee8251a8bc845cf0bfa44ab864`

```dockerfile
```

-	Layers:
	-	`sha256:ce80818c7a2398aede62663001b49c6a0dc52636777eb4a32101de483621253d`  
		Last Modified: Tue, 17 Jun 2025 18:48:10 GMT  
		Size: 3.8 MB (3825756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7fa43b3c94943e520ea33106f5e1ba9ffa1aa34404166ca7e03c048d881305`  
		Last Modified: Tue, 17 Jun 2025 18:48:11 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:931dc04507b294352355d64b5c72b95257fe49fe94d42685a12c57bfe60be29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112264144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb1cbf11c312b638a063b0caf252fc6d192944079c683ce06176c285f5321cc`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca020baf911e0e46a552c6fe07c08656e35139737e39025b1b0b98d5a625a79`  
		Last Modified: Tue, 17 Jun 2025 17:40:18 GMT  
		Size: 60.1 MB (60129091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ddd11e146b4e70b1e67edd565c426a882f4e4b446f8b5a1f5c301ca23555cd`  
		Last Modified: Tue, 17 Jun 2025 18:15:36 GMT  
		Size: 7.9 MB (7926843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:139322f4dc569000b664fc30b6f82615602abb0a69aaa738c4c6409374ed5700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee02bcca44c45cfed00e6e66d61488a766b00405549a27de7cb670dc9d699b`

```dockerfile
```

-	Layers:
	-	`sha256:3b929b248cb7970e12eae753b68a034ba9536022cb224ab4ee829a0acae73217`  
		Last Modified: Tue, 17 Jun 2025 21:49:18 GMT  
		Size: 3.8 MB (3827981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c34ed8bb6b9d651421e4adb8d5ae1edfbccb3ec916a458796039569f41f6700`  
		Last Modified: Tue, 17 Jun 2025 21:49:18 GMT  
		Size: 9.9 KB (9858 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:988380a1ab3c088a38bcb443c50fb8cb07395b9ab0f159eab950fff138e5ecee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124300504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a19e220eb5d0e90c004a2790bbdd27a14a772343aabcc08740d4cd8127d6dc4`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e84c9e0d5ebf60b03b6c720aa74055d7da34b38574f369555e0b6a7f29b77cc`  
		Last Modified: Tue, 17 Jun 2025 17:32:36 GMT  
		Size: 68.0 MB (68033809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c28647fe1d2f0ea34b75bc61bf6c0774f9efa190dc4b04d4d9d3ad0b1b8efbd`  
		Last Modified: Tue, 17 Jun 2025 18:43:43 GMT  
		Size: 7.9 MB (7927843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f612b74523e4d63b172da642ff9e1f638ce3bf465dbac15c5dfdebc23523c9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bcd63419a290968b7e01cca424c21ae201ab9f82be885f0aedf44a9033dc84`

```dockerfile
```

-	Layers:
	-	`sha256:8bd5f068efb061677653ea13fa9a3ec1e4d2c8a9cb5b7ba3706d95827140d897`  
		Last Modified: Tue, 17 Jun 2025 21:49:23 GMT  
		Size: 3.8 MB (3826005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce0eb3f06427bfcb9ec1a5601fa22cb94d44f7179d9f2a816b3ae89a426191e`  
		Last Modified: Tue, 17 Jun 2025 21:49:24 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:f574693656cf356fd9dd36ea3d517aa439beac7460e7176775d42e9b8a46ac15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118531783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522ade4ec9c4d1f20f2a040eff8965f6b9ec3b8d529d46ac343bacea7b519c8`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250883d68df9198287707298b500eb11c6b8252355e7616b38ed2eece07eef7`  
		Last Modified: Tue, 17 Jun 2025 17:11:39 GMT  
		Size: 61.1 MB (61127330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480da6707b1e4eac271b5180392bd0fa5562c02ac95b8db2a00a1c6dfdcc999e`  
		Last Modified: Tue, 17 Jun 2025 17:14:48 GMT  
		Size: 7.9 MB (7926979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:00b07c8a2a92022d20c329bbb3705ce3765c9da8a0bbec12798d6f02ba4fd631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ddf1ea7b4b564fbbae505dfbb73bbadcd92e4182d5714aeb71174e0cbff8fb`

```dockerfile
```

-	Layers:
	-	`sha256:24cb710043cf88ca1be1f572df3d97ca9fb30418667ece313d36bcef15f69cd2`  
		Last Modified: Tue, 17 Jun 2025 18:48:30 GMT  
		Size: 3.8 MB (3822928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad4dadbc9cf00155a301d8ad10a18f5c210f476ecd3b8dfffc752df11819d06`  
		Last Modified: Tue, 17 Jun 2025 18:48:31 GMT  
		Size: 9.8 KB (9763 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:2c162c30bc4bf3041fb53429305b416fb18bf36d5239efe644763f5e9033787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122490101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0401e6a7a75d259e8d6add8b21a58329840298a81224bd22b746904ba4f5b117`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f346c9686e3fd178af83d5447976eabaf910bcb8aec554a2f2f2ce7028d6dc5b`  
		Last Modified: Tue, 17 Jun 2025 21:54:57 GMT  
		Size: 62.2 MB (62225081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae50627f85874070c13cc3bb40173770dc481971590b1303fc40e7e966b802b3`  
		Last Modified: Tue, 17 Jun 2025 18:58:58 GMT  
		Size: 7.9 MB (7927663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:18e884d4c527e6689a4bc6221035389ac2306e9f14ccd2ef6dfa31d2393a965b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0acc3915049c05505f05f682a824925e85ecfa75688f022463ee157cb7057d`

```dockerfile
```

-	Layers:
	-	`sha256:9804ac60592839e8e8a97d35ec3b1d496e46ea7f81cd36e5c57573cde55ddc9e`  
		Last Modified: Tue, 17 Jun 2025 21:49:32 GMT  
		Size: 3.8 MB (3830188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf4fc1f6c52762e35f9433a3ddd865fa2d7e6063d0f6735ef0e5d45f0b43106`  
		Last Modified: Tue, 17 Jun 2025 21:49:33 GMT  
		Size: 9.8 KB (9828 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:8c60b3c1e28004bcd3452f03d213d9d65ead2f8266bccccad7fa8c9f96e94dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116018950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c1e65f751142cbc57932ce643078cf473343e1d97231f2960191243d9cf1ce`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.11 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.11
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2eef7aac690a6cedfe0e6a20fc2d700db3490b4e4249683c0e5b812ad71304ed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62db53d73222b5747349cb0d7d73e5be294a997c1c94d0ae316c818b4e017bb`  
		Last Modified: Tue, 17 Jun 2025 17:34:41 GMT  
		Size: 60.9 MB (60942611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a3c6131f948cc7dca1d81bb46f02ecfae658d82df25362e3a7fe060a4696f9`  
		Last Modified: Tue, 17 Jun 2025 19:05:10 GMT  
		Size: 7.9 MB (7926931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2755eb361e946b129788116c0d06df0c18d262090ed1a9b85c1621c0c657b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde1c27d34d650d834f3a67443dd3cbdd66320800d7b8aa3d1c15081a7ffc308`

```dockerfile
```

-	Layers:
	-	`sha256:70206a5b2377bfa5329be1b4386a302990033382c355a5ebdc20f67a116730ca`  
		Last Modified: Tue, 17 Jun 2025 21:49:37 GMT  
		Size: 3.8 MB (3822584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5694f0222fd4ca7444da1c7b9e7d5497fc5eacb4f3b74201ee1d0c370328e91e`  
		Last Modified: Tue, 17 Jun 2025 21:49:38 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
