## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:11e7993822592fa351111be76f809b0f28b684c7e9acea514eef9c936b110b38
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
$ docker pull elixir@sha256:3ad11238fa80b6a9caa01a132e840c8afe2eb156ab039c7bc756a6864e878880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132396372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5693c7dd8e45836bd1ca5f58c833aea79c6d52235e1b8720737da3d8b41c13`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4fb221693e5e9ba5c86a5a02b5f60f159bf47ec02a7b40e7b0f5539a2f0de38d`  
		Last Modified: Tue, 17 Jun 2025 17:06:47 GMT  
		Size: 76.0 MB (75973113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed49eeb91e26b342dce8b619c1f89593bccb1805d8125805decc9bf56e823d`  
		Last Modified: Tue, 17 Jun 2025 17:12:23 GMT  
		Size: 7.9 MB (7928987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0088332e1948aadc59c3dce735f5d539eb78ed521ed22aaea46bda6c8faaed09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92a36eb6aa73fce8b90e8b88953d2f0282e3b5ef2a993c2da511a15df175837`

```dockerfile
```

-	Layers:
	-	`sha256:d6aea64ce6b9c891e1747f63ad70af4e41e4c0c15197eff3bdb1acd070038bfa`  
		Last Modified: Tue, 17 Jun 2025 18:48:23 GMT  
		Size: 3.8 MB (3825359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1947d7d445ab3564edd04708c9c0abd1e4ee37e69495f053390fccc14e3055a`  
		Last Modified: Tue, 17 Jun 2025 18:48:24 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:926b8535cf0e8859079044a9fb821f2ae38d85cdbca4b1815cd5194f24be8c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117239993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832bc7b15ee3ff9fb129d30cfff4d656d2bfc960b7d76c4e7d53364d8c6b8dab`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bbc330d8b9b20b57a9de58b230c3c529890c5699c928984b0220fa42744491a1`  
		Last Modified: Tue, 17 Jun 2025 17:22:47 GMT  
		Size: 65.1 MB (65103904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60c54dc3aa7d964508b963cfb28c4d2d0caf9e417a8f719f05ab6432ab3ea1`  
		Last Modified: Wed, 18 Jun 2025 12:42:46 GMT  
		Size: 7.9 MB (7927879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:053724d8274ada7d973b39fa6041894147f7ebbb31718809539b0fb0df327414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ac780874058642cf98b0f649932bed74edb57f93a35d0c30896a039367c283`

```dockerfile
```

-	Layers:
	-	`sha256:47979e6b026e1cdc02700f144eca4204c29e1f8dd37ca424062b7763024f7071`  
		Last Modified: Tue, 17 Jun 2025 21:49:32 GMT  
		Size: 3.8 MB (3827608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8895715d905e6a82d951e668ad841b6e271530402c8923abb79784532e7b6085`  
		Last Modified: Tue, 17 Jun 2025 21:49:33 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:1846ff7da4714c0185d2243b11d19482f1c741136dc1ee7d0b3d23c67b97f396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5c823ad7864bacf61a6c21e696688673e312db0f8b2c38c20fecc49ec59584`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d0228d4f877ceb70f3a55f20030ce36c1c86d971046295af7e84b8d0808df652`  
		Last Modified: Tue, 17 Jun 2025 17:18:49 GMT  
		Size: 73.7 MB (73715145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4807c9628d8653da0f1373136cf239b3816e9cae1739c0e64ef5e43ebbbcdce5`  
		Last Modified: Tue, 17 Jun 2025 19:01:05 GMT  
		Size: 7.9 MB (7928843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:90aa58c4ca1035c57947c86e2faecfe7ee1288c977241dbeca105276ce83f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47185c4602e92ac32a99ef8e4b4b3212b4770f6b16d9b2df5370f51b366253a3`

```dockerfile
```

-	Layers:
	-	`sha256:6f8849a7f57a56678ede95cf02a35ccc0bbfcadbf21d34bcdd11ff2222956de6`  
		Last Modified: Tue, 17 Jun 2025 18:48:35 GMT  
		Size: 3.8 MB (3825644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61da0ec9576f16de4a4ab1da641e2f3d84d2038980d73c66fe21a34fd263ac60`  
		Last Modified: Tue, 17 Jun 2025 18:48:36 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:ca522f8d9baddac0b614a41ae17dda86b845ff0aa1e2172a99f37af27564a0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed74f5fc0bed795d8b5359d64d07b9ed0e4cda7e6db12c526d180ea61a7722d6`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d83d767d9233b11e6ef6ca6dc1057bf36643e429a89bf15eef0a5ac2fc5c362a`  
		Last Modified: Tue, 17 Jun 2025 17:07:02 GMT  
		Size: 66.1 MB (66134921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6a2c77799c2db9fd78f167e4598d311e624158060e2ca068a50c64660ebf37`  
		Last Modified: Tue, 17 Jun 2025 17:12:51 GMT  
		Size: 7.9 MB (7928235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9da7dda5eca183e7bd4a49abe273b55f3b0d9a175025afef9d0dbad780d576d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e76e9dd5a95fd00aabcd35a94dc13a9b7f3507562cc59d8831242c4d3cd462`

```dockerfile
```

-	Layers:
	-	`sha256:81b2bc09fc1b4784de466fbe77a4ee8308a0cdfd139b423bf3915c505bcd1a4b`  
		Last Modified: Tue, 17 Jun 2025 18:48:41 GMT  
		Size: 3.8 MB (3822516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab9332e18ad7fa05ddc971e1b3c58539db54308c3f69587fba2a4af4479438f`  
		Last Modified: Tue, 17 Jun 2025 18:48:42 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:418b4ab4a847c7c36df1e109bea4cddaa5c4d9bd88b00ebca4d5155a06bc60e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127478767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6844e0a8992ffa5f08e5562d868ffa3f3d5e49fc6819480919020a797e51eff`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a6f332dd355a2cb7815b8ae53fdfaa8b1042e0b12720904efac4f9dae40ddab7`  
		Last Modified: Tue, 17 Jun 2025 17:26:34 GMT  
		Size: 67.2 MB (67212408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a63238f5035f850fcded59d04dfc7fcffe4aa4703a244dadcff94fee32934`  
		Last Modified: Wed, 18 Jun 2025 11:37:15 GMT  
		Size: 7.9 MB (7929002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:340b92de15bd62e829e486110a90ccf867e39eb0c9a76641e8102f63b37c9db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd6d70dadb7da8a3d59530f260420bf781f0dea28723aabba0849ce3013d28`

```dockerfile
```

-	Layers:
	-	`sha256:9e7e71a2300cb71fa5cebd9217672da5a90246ee7ee63a138e4089469806ad75`  
		Last Modified: Tue, 17 Jun 2025 21:49:43 GMT  
		Size: 3.8 MB (3829809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7384d3d580fb25f3f074b0e63eef11d54963856d7329adc81b348279206ac6`  
		Last Modified: Tue, 17 Jun 2025 21:49:44 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:bdc76a968648beafdadbeaf139b9891c776a64927e0830746b15a74d81c358dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120964916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4687376d5d0ae4a8bb9517f96ac8e2b593c66d58feecd3cd592b8becc6435a72`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 22 May 2025 14:26:26 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=27.3.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9dca5c3fc54e93707ad1bf2e6907ae0604a9224fd98284e5803add6958cc000`  
		Last Modified: Tue, 17 Jun 2025 17:17:57 GMT  
		Size: 65.9 MB (65887433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60faad768e2693646ff92cb2ee6531c7ad4dfcdfbdcd3eb198e13fea8675cdf3`  
		Last Modified: Wed, 18 Jun 2025 12:07:36 GMT  
		Size: 7.9 MB (7928075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:b2c89d2394d69b3203f20fa94bb15c9369e91ff7003a5ea75bd53c081d3273a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1291fb46b2afb3c841e867e54f4bc36fa6fcf58459951ec757cf924e76772c5`

```dockerfile
```

-	Layers:
	-	`sha256:947e3a227315631bead06f40fb40dc251d92fa8efe8d0ef9564eb513fea82971`  
		Last Modified: Tue, 17 Jun 2025 21:49:49 GMT  
		Size: 3.8 MB (3822187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196281967e683013b62951fd121c01cf42f6891c48d5156cb0d0ceb3709178fe`  
		Last Modified: Tue, 17 Jun 2025 21:49:50 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
