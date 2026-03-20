## `erlang:29-slim`

```console
$ docker pull erlang@sha256:be45b0fbe841814eb494a8b58a4a7bea7d00dc4a83607a2c8bcf12fe0a239d83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:29-slim` - linux; amd64

```console
$ docker pull erlang@sha256:7ad1d61a9e325945a8b252fd5b939e574e6ad08fc6d3332119be25e926cb28c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129459338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9a4f68351689bc322f6827a1f1eb1d38c6d172789c7896ca4afe0f78254440`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:09:21 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:09:21 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:09:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:09:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a30dbe9e622a4697a9b27e5823ccafb244ae1f17534e61742ed3245ac447f`  
		Last Modified: Fri, 20 Mar 2026 19:09:36 GMT  
		Size: 80.2 MB (80161808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7893084a2a77c67c95eaed55e3a38a3d98dae67b380c5b083e4279ed2380f44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5a0eb5f34b456b683b29c54f5703020af95907329afbc2e0b22bc11f0242e`

```dockerfile
```

-	Layers:
	-	`sha256:6bae8e4ac1b9d8d0d358df79278f552beb3200c0738ef5df6de960f6c81c6115`  
		Last Modified: Fri, 20 Mar 2026 19:09:34 GMT  
		Size: 3.3 MB (3283468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edeec6d6ef04a2126221c751f5d067ff6520c25a0e3f3e8546c8c9774ec2d5c`  
		Last Modified: Fri, 20 Mar 2026 19:09:34 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:f105fff98c10b649113e227aa16d957a2afb99e1901bba193dd8f91ce50e6163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117844578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b1427a491f6aa80315c372370266626a57ce690314814aeeb8c7a762e9f325`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:09:22 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:09:22 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:09:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:09:22 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa49ef3e5f4aba6da6f23d30fa8bdcc0432b4e10f8b90b93026a6a07ffd532`  
		Last Modified: Fri, 20 Mar 2026 19:09:36 GMT  
		Size: 70.4 MB (70383966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:575507aad65958ce28ddd7b6767e0609058123e1ea6732d418f14a903c3ff0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43fee746ca991bc74786faca164230840330a0569524c6534eceede63449a6e`

```dockerfile
```

-	Layers:
	-	`sha256:80f9e856ec3fe96270cd3715599c75f6b44611df997515f4543b6246ce7ebd32`  
		Last Modified: Fri, 20 Mar 2026 19:09:34 GMT  
		Size: 3.3 MB (3286435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c624ec11ff1ffe6bec8a55b567a2ab0b7d2c6b4efc89fd8c6ce3506135b1840`  
		Last Modified: Fri, 20 Mar 2026 19:09:34 GMT  
		Size: 14.3 KB (14274 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:ae1f2f11f53ce8c8e83585eeb93c9af07b337adcecd6d08342fe6d98d785fb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961b85fa1d9de57fd23f8d04d185eaef7fc20f2070effa328e2f517602a568d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:08:51 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:08:51 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:08:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:08:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24b35973f137dd1f9987f3fc892f497125788124b9aca53e010d9c4f727fa3`  
		Last Modified: Fri, 20 Mar 2026 19:09:05 GMT  
		Size: 70.0 MB (69951408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:46cb287c93b64470fd6f6af3fe452192b96b1ff20c61f2c4cda17263ddd96312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433edbabcf7e7a6b5c8a11731d268783e980d6b2d774495f51e28475c36a895c`

```dockerfile
```

-	Layers:
	-	`sha256:a201950ffb21b2e0abf8ec85b00f9254d6c90374fd6bbe0f64e99b0736752ed0`  
		Last Modified: Fri, 20 Mar 2026 19:09:03 GMT  
		Size: 3.3 MB (3284884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d9047e537f6bfff64ce7fb95e6cf00c644a726390f9b07fb7b936812fdd13aa`  
		Last Modified: Fri, 20 Mar 2026 19:09:02 GMT  
		Size: 14.3 KB (14274 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8a983ec23339c66cc083aaab33971e37f8fc0f61d628a8a1c4372979996fbe77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128316279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8401a3bd32bc6f95be8607977873ce15e8b05aea95d3fc31596aa0c4868d9abb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:08:27 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:08:27 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:08:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:08:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bca19249a1515bbd309c0e40fc6f5b5e0e0e6a10cebaac78f2f6d9c64db171`  
		Last Modified: Fri, 20 Mar 2026 19:08:43 GMT  
		Size: 78.7 MB (78651326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a7860ce8fc53a82b3948fa150c03341f12a4a466cc76dbd5ac3199fd4bd8dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f5e8c50ec72ae665a78cd77884f6e05732834bca2f97963b8bdeb4321406cf`

```dockerfile
```

-	Layers:
	-	`sha256:debafde6116dfe17521b1c66f17c80b5b4f7d3bca2b5b09c654905374fa7a1bf`  
		Last Modified: Fri, 20 Mar 2026 19:08:41 GMT  
		Size: 3.3 MB (3284991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfb7bd825391d0f4ba7855ef450677ec13418b2b71a09a07bc1be4abd4ae304`  
		Last Modified: Fri, 20 Mar 2026 19:08:40 GMT  
		Size: 14.3 KB (14298 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:862a7cddaf1fb73bc13301ae79983f10b33b90570eabf6d82456570a7fb81649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d20527d1bd45d2ff7ac91d5cc99feb697b7c1301f7d3dfbdfb5af22d21aa02`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:09:38 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:09:38 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:09:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:09:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb7940d37c9996f2c17e60fc4218c2494ddde61ebe18e77d6cb662e8f3c146b`  
		Last Modified: Fri, 20 Mar 2026 19:09:52 GMT  
		Size: 70.3 MB (70328795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2685063759e91c974dfe43459309b0f21fddea08f0fe965880caf2fa54871cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cfe91f8305aa7a9283267b55ab7274cd91dde3a0f59eff8563b0af0d2bf9f5`

```dockerfile
```

-	Layers:
	-	`sha256:3f3676859c6ad8587d4513821ece2eaace51b125330fb95f53ad2d1934dcd918`  
		Last Modified: Fri, 20 Mar 2026 19:09:49 GMT  
		Size: 3.3 MB (3280643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b43f09343f92ea9eeb5ebf35d0acbf1ee1e9a78ad44089f04036b202063002e`  
		Last Modified: Fri, 20 Mar 2026 19:09:49 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:20c0cfa00cd68369825f8480df92e1bed038c9dc47c4828563d02405f22a2e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124440557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d5a75d34f16a25b4bf11e13cad7b0803b1c6d3a120fd790c040b4b5a16f419`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:10:31 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:10:31 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:10:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:10:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2d9c5808c41139fb24a3ef2379400bd9c8698a124ab89ff09119be6fda6e23`  
		Last Modified: Fri, 20 Mar 2026 19:11:03 GMT  
		Size: 71.3 MB (71322207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:03e9a48e60fbfd971bf7df9354f8aeff2c30be011c895f62f15aee41313a32f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbf9681b1fe79eda4c767abdf611ea4b27e9de968f42fbfa0d57730a5a82b21`

```dockerfile
```

-	Layers:
	-	`sha256:85a3b0227be25f920b3e55942006cd311b29ed8658989a7ade1b88d24660c9c3`  
		Last Modified: Fri, 20 Mar 2026 19:11:01 GMT  
		Size: 3.3 MB (3287053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:739438fc62cbb7562780a7468b3ddb9b40acf5bbbc26302384165ecf898f9347`  
		Last Modified: Fri, 20 Mar 2026 19:11:01 GMT  
		Size: 14.2 KB (14238 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:89daf8ffe7cb7a5d5644b56ccce9e6e48f6613da0f890bb5c367d7bf83845ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120561204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8907b3204ece2ce458a9a66d0ff0fe76db728566b9b1950fb8a32a8f186756d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 19:08:39 GMT
ENV OTP_VERSION=29.0-rc2 REBAR3_VERSION=3.26.0
# Fri, 20 Mar 2026 19:08:39 GMT
LABEL org.opencontainers.image.version=29.0-rc2
# Fri, 20 Mar 2026 19:08:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47ca12d2278f54c412e637bb105c58730dbca91e0d361391e524d7aadd451a00" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 19:08:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338c6010efeff15b1a4837e12da13281b4687008ff06b9fde49b8cb383c2d105`  
		Last Modified: Fri, 20 Mar 2026 19:08:58 GMT  
		Size: 71.2 MB (71196429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:315f60bd71aee7cca0621d57d923225c3be645661b7179e7b54ced7205a2fab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb594993bef7cc154231de3f9290d2098addc8d82e3f762b2e0a3a847b0ddb2c`

```dockerfile
```

-	Layers:
	-	`sha256:b615bacafb9d2d7a3b7d75b42e12de77fc0df4598896f3f199433245947fc6f4`  
		Last Modified: Fri, 20 Mar 2026 19:08:56 GMT  
		Size: 3.3 MB (3284909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6ea2ec430c400af256a327f846a17c3e0f9141e77db19bf56519b269c5a190`  
		Last Modified: Fri, 20 Mar 2026 19:08:57 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json
