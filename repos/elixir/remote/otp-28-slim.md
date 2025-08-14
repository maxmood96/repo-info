## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:da417aa4157809dac687b7a0103436c328251fb1069dc689236519f80bc66141
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
$ docker pull elixir@sha256:8acdae6f2bc2c5caff59e8b5f1928ac9a66dc1f2ceb122f0087525053e739b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136752294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0b7d894832570de2b1cb71a1ae08bcff5c0031b634fc9251c8b9e8d2c59ee`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534c76121e942938b5f04a344713ab8b847d656ac63b15d36e372c98b4df0450`  
		Last Modified: Tue, 12 Aug 2025 21:26:21 GMT  
		Size: 80.4 MB (80350607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f2b6bcafd5d159dc6df5c145e84b147c6dfb6e7f7cda9e6e8f663fe37d659`  
		Last Modified: Wed, 13 Aug 2025 00:53:33 GMT  
		Size: 7.9 MB (7907176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:abc571f4e4e916ed8b0dbe535937a5f93fe26ffbcf63d9b21a291cf3dd6a3860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa43283b0cb6cef5521cd27e1f0cd8c260c49dea2ba39834c4f33add1c4425`

```dockerfile
```

-	Layers:
	-	`sha256:32408e0d1e5925d3871ac4b0b14b809759671f368780cbca927f2f5a2d91c9ec`  
		Last Modified: Wed, 13 Aug 2025 00:50:19 GMT  
		Size: 3.8 MB (3825281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0380e3bf9bcdd61de319b99277501d2c86485053d31ae866756c1e8fc4b5133`  
		Last Modified: Wed, 13 Aug 2025 00:50:20 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f1e5b25c3b6596d89aeb0fe6bd8c36238803173305c58034a38e34e7c32e5554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121546613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdcc080b2e625c399a2bbc46bd8bd769a23e3963863166aeb4bba9190554114`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf595842a8587bed7509f798d769106f6804c44293e2bc6f029ce28adad3eb9d`  
		Last Modified: Wed, 13 Aug 2025 00:24:40 GMT  
		Size: 69.4 MB (69430965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b9f60bcc60ffda977d1e2bf8c7bcfb48c5535989c09626a1f0fe91879ae1e9`  
		Last Modified: Wed, 13 Aug 2025 11:08:36 GMT  
		Size: 7.9 MB (7906604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:cd0f313bff5c9a5a694ec67d41c39d6a1c48000c61f970add1ab6779e779df9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5effcc9f8eb3da0b0dfbb7aaac365d1b8070fda842f7439cebdba1ac447097`

```dockerfile
```

-	Layers:
	-	`sha256:952f3f33a24f80a796afb32f9169f17ed6de3ce22c9c7cdff6a8e624694bfad7`  
		Last Modified: Wed, 13 Aug 2025 12:47:25 GMT  
		Size: 3.8 MB (3827530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6609928e398ca8abb53be866824a893aa828cd85414692e496e5d79ee281ec`  
		Last Modified: Wed, 13 Aug 2025 12:47:26 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:684c59c9674ad8bc4b5a192b5800ae5f48c9aa227b2d8029f15a60ae8f5a6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134396335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482cd12eb70271b34b8b3032121dc366702e3016ad061792927c3429856d0f2b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abc0429261fc959dcea40a792e6e38f1f2dff843641eab6664ce79958497bcb`  
		Last Modified: Wed, 13 Aug 2025 08:25:09 GMT  
		Size: 78.1 MB (78146707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0847af7d525d96245b5b2c7c656369fd394c25ef4187242fb38c493a028004`  
		Last Modified: Wed, 13 Aug 2025 19:13:33 GMT  
		Size: 7.9 MB (7907178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:3756d9da8d6c0dfe917829bd094179a1fb37cadc4ca5facb0011f2cf8b58a0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784601efae5dda4b80f980a814d500d7fed5ae1df90133abbe2967a1f19b0b55`

```dockerfile
```

-	Layers:
	-	`sha256:387ff7c028baf8b3b6d2205ab37b2ff1412be14d882e8a13efa22ca0aeb464e4`  
		Last Modified: Wed, 13 Aug 2025 21:47:22 GMT  
		Size: 3.8 MB (3825566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a3e7bab6ac60c5ad62743ec28a69445a9a2da016e300744f450bd4f5ec4a00`  
		Last Modified: Wed, 13 Aug 2025 21:47:23 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:2e47610deb2d56b2ddbc50be3db5fb00c2f4b205806e79f1c3b72a40326c182d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127936756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b471398bdc2b2bd71c829908ec428a702e4bed3fefd74b6d01b3f88690ac367`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cc486cd45801e9ad3099ac5c018c5d91a2b6eaa7b0a1cc191192a6b328497`  
		Last Modified: Tue, 12 Aug 2025 21:23:50 GMT  
		Size: 70.6 MB (70551861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ee4d9713c523094f2486f9f24cd5e62b1f50120f579ee18cb3fa1ccb4eaf2`  
		Last Modified: Tue, 12 Aug 2025 22:23:09 GMT  
		Size: 7.9 MB (7906780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:dfa3381eda2c4cdbaf09261b85994b628aae8f8aab14917d95e4d8a74d52b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1257faa70860d00c2bc33319fa2b6f79f3e016cdce622984b6f78e902e59465f`

```dockerfile
```

-	Layers:
	-	`sha256:7a961d519c3f2d17e3c766d4cec5d016811ec2fb8d2f41b342b2a8418d40bd73`  
		Last Modified: Wed, 13 Aug 2025 00:50:34 GMT  
		Size: 3.8 MB (3822438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018307a0f65a556aa83534ffb777a214a463cabba6ed27f5b42a400ce264626e`  
		Last Modified: Wed, 13 Aug 2025 00:50:35 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:ce8db76424a5ef414788f6d3c4a489b1e14ee20871c83d59b50d56de1c5d51b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131815650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad041ed0c131585794c9015e628f4650951b49ce2159cf28eabb566763017ed`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31502fd9d4e353d2e19776c57f1472ba13088a583d66273c6f6e88f8377f313`  
		Last Modified: Wed, 13 Aug 2025 12:39:30 GMT  
		Size: 71.6 MB (71570267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375862c56590b7f11f03b590ad90ade054fd08966485b362546baa593ba9d628`  
		Last Modified: Thu, 14 Aug 2025 03:53:46 GMT  
		Size: 7.9 MB (7907306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:00f72a75829650a3d074971bca6941bb86998fbbb787af9325e456d1298ba7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee76cdb487b59cbea1db8efe179f5729a49183cfdc629c84cb994e97a63923e`

```dockerfile
```

-	Layers:
	-	`sha256:7ad812a19be5a6240fa52dfe393e46a1d1c77b6a2c99122471b3e6b0862f561f`  
		Last Modified: Thu, 14 Aug 2025 03:46:11 GMT  
		Size: 3.8 MB (3829731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a0410e4ee405b253adb1602158bc20c3977056f5ecc287d0e44dc1ee67d114`  
		Last Modified: Thu, 14 Aug 2025 03:46:11 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:f8e2445436b67130f08f4184c32f8c308b73e095216efd58a1752115213b0e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125244927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee6acd75a1b5f7ef754b509e8c1096a79e95c9f603321d4e54603fc71633cd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 30 Jun 2025 17:24:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Mon, 30 Jun 2025 17:24:21 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Mon, 30 Jun 2025 17:24:21 GMT
LABEL org.opencontainers.image.version=28.0.2
# Mon, 30 Jun 2025 17:24:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
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
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2196f4fd88daab4098de366486a81c0f517a31834d3d4b8c0dfe14e35ad65dd`  
		Last Modified: Wed, 13 Aug 2025 03:30:04 GMT  
		Size: 70.2 MB (70188372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248009f3a99dca8372f29710811a1f86691155ec776d5c2f18ece4e7e86f112`  
		Last Modified: Wed, 13 Aug 2025 09:04:37 GMT  
		Size: 7.9 MB (7906689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:d4d67b8825d684e5b4ed497547b8b6be228653e07f070652ccd7972a0b46553b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e879f7366e1e824748fdd2f1d621e541b5696b14a8f026e8f003b1eb146d99b`

```dockerfile
```

-	Layers:
	-	`sha256:624440243fee4b059946b5a21b3837d87893e64993186b8599fc87e873070769`  
		Last Modified: Wed, 13 Aug 2025 09:45:47 GMT  
		Size: 3.8 MB (3822109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a45c3137dcf0ee66bfb2380f48601f37690e26e756759d64f76982a6723dbf6`  
		Last Modified: Wed, 13 Aug 2025 09:45:48 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
