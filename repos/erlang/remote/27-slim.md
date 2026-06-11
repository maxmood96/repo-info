## `erlang:27-slim`

```console
$ docker pull erlang@sha256:3165fce5b52708d878e9b047202ba7589fb40785d769f3f6ab37d42ec161eb86
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
$ docker pull erlang@sha256:c9bffef3724fed4f3ba0c07f9b9605143e5e9e8d0d1b183a5fe746a27a555eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124562948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82885791dedad511191b98696967e8f3c5d717ddddf6ef1a803485082d96333`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 00:45:15 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead1f2f6018db5610eab897955db11f73c1ad7a2b7f9b901418f7af79367d2cc`  
		Last Modified: Thu, 11 Jun 2026 00:45:30 GMT  
		Size: 76.1 MB (76060906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ef56c2e35d1ff27cfb3f1a1547bbd18e25dc8990ceacc0b8b28ef23226e1cda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aa0f4e1bec0792072555026b2ef75196ad55630c63094a488e2ffba8ebfcb7`

```dockerfile
```

-	Layers:
	-	`sha256:3941bcd6c546a4a4e6a9821fd3c577f8d5a35a287cbdd0ed23050105e930700a`  
		Last Modified: Thu, 11 Jun 2026 00:45:28 GMT  
		Size: 3.8 MB (3824823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcaf34c575bc97ba42139d496f57e52faca0901a6ddbedcad48b0470999149a`  
		Last Modified: Thu, 11 Jun 2026 00:45:28 GMT  
		Size: 13.6 KB (13639 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:a381e656db0cf3ca91d096be6691ddc33dc8704cd66a66c93cd9aa67f5076c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111578080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f293d84433d47bb97c55c18ea32253d29436e4ea998ac5f68828e413944dde0`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:31:41 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:31:41 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:31:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:31:41 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5c634ce747cde274e6d6c04054b1f399567101f5bdf6d95c7cb3a8a3874f32`  
		Last Modified: Thu, 28 May 2026 18:31:54 GMT  
		Size: 65.5 MB (65548577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:864b0db1f2a56587408d05762a3e5566b6f6bb4481d85e6d484f9fb11a4d3d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943d879c9d688b84f719df8f4538720e67256932e09cd44432e6432b5c30630f`

```dockerfile
```

-	Layers:
	-	`sha256:7edf58b24b324077d0359a82c00c04cdbe0b7e1e6f3497ff2faa381304bd741d`  
		Last Modified: Thu, 28 May 2026 18:31:53 GMT  
		Size: 3.8 MB (3828613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ef9f06059f9b06f8cb3568f57bb47d5bb4294ca3f3b190f7b1b95c3367a284`  
		Last Modified: Thu, 28 May 2026 18:31:52 GMT  
		Size: 13.7 KB (13719 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:ff3c4b9aa51973aff2659a2b9d69de7a071d0061a01ead23a62d17ffd30aef9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109385087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b51cd32ac184f5c7f715b68cb050e3e23a5e9aab8ef8e52a51e23cf83e8a9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:41 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:41 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:32:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:41 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fbe19eb60c7a12b0895f6b0be3d1779115581fbf02d68938d6bce9a93c8781`  
		Last Modified: Thu, 28 May 2026 18:32:55 GMT  
		Size: 65.2 MB (65175933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c1b28e739761aad7f7d126d6371483255d6f9f07490bfda49bd640a15f47a3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292563773518c516ce0a094e8d08505285dc5bb33a7800ff1a0cfbde27a95c35`

```dockerfile
```

-	Layers:
	-	`sha256:fe50b4d21f67ce51261f301d6cdff50b6276d10868d45b426c3d6709703b26f0`  
		Last Modified: Thu, 28 May 2026 18:32:53 GMT  
		Size: 3.8 MB (3827038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3b53070af2c2e1652fc7285ad778a72a07feb8a1a6c5bf2ffd942d272786a7`  
		Last Modified: Thu, 28 May 2026 18:32:53 GMT  
		Size: 13.7 KB (13718 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bec92617fc076bd70c14b5f049c846d552c8743b7fc20a00882cf0874c36a279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122194698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442189514316fa7bac9d3adbf4f75f5a0c9ad308b24c2816b465adcbaab10e1`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:46:53 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 00:46:53 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cf794f6fe7e48d1a097dfc42288bc42d5492ca9e0226e44eabdd2f033f476f`  
		Last Modified: Thu, 11 Jun 2026 00:47:07 GMT  
		Size: 73.8 MB (73805682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9fb2b8248fbcca5e2519b2449d5490c115237ebceab34087d20ba4a30118e55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4548616745d157e93a81f7b56f90b24b02303c413fccc54ee70ed34a3c01f06d`

```dockerfile
```

-	Layers:
	-	`sha256:9543a99948e9177695b42f3469adc3e85b5636606697695a245c758d99326d72`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 3.8 MB (3825084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c318e04c824fa7e193a7f6b610e58666eb22795a6616dcef8dda909c33f2910f`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 13.7 KB (13743 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:cda692f3101f51e24cef67d4976714ee403ab825342c895d38f807ade3bd7b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115710401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb6d398d571d8722d1dde790105cc9beaa65a4d8180a417ea35df6827d577d4`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:46:47 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 00:46:47 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 11 Jun 2026 00:46:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3d12eb90beb07037951466d7705902ab72397cd1a9c3ef3c790cb1caf36285`  
		Last Modified: Thu, 11 Jun 2026 00:47:00 GMT  
		Size: 66.2 MB (66219195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0de19358b196c3440bcd1af93295e16fdb71731e6570b2b8fb397b0e8e386029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea9137e012d1083f674deb473c37180cf405e28157e93c0516926bae1ba69b8`

```dockerfile
```

-	Layers:
	-	`sha256:57f5c10f61adb25959fa2f524ccbd4f0053b2a5aaf504d11ea18da0c134066cc`  
		Last Modified: Thu, 11 Jun 2026 00:46:58 GMT  
		Size: 3.8 MB (3821984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d4a9f38ad39f516b3dcb4e4598aaa257037fbfdfd6a01ef8d883d6f3265c2b`  
		Last Modified: Thu, 11 Jun 2026 00:46:58 GMT  
		Size: 13.6 KB (13607 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:b38f6c0e86c03e7905cb862b1953d7e6660c0152827b4d0a4e5c17015e8df54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114917104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5af1c3f5c12725dd03f047132fa2167c8fd25092380e7a2f63268f04ad0dfce`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 06:36:36 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Tue, 02 Jun 2026 06:36:36 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Tue, 02 Jun 2026 06:36:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 06:36:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667b2731ae52406601f1d1ffceea3eaa4653e298050757d8589614098c060d86`  
		Last Modified: Tue, 02 Jun 2026 06:37:44 GMT  
		Size: 66.1 MB (66130865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:97cd7e6712ea66187f8b9c9b1178ee2fdba8ccd6b3979ebc359506b03a37808e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fc9900d45385526a4d901a5446c1a29052ac9118373831967cebee6194e2c4`

```dockerfile
```

-	Layers:
	-	`sha256:d0fa125e071e92cb77b6da4ce85d2a28feb775121cb163e4249d60f6d97462e6`  
		Last Modified: Tue, 02 Jun 2026 06:37:37 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:13fb6e5526abc5cc3b68d69eb006534cc49e5dee367a796ea2900d9fef1377b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119636720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33280430531ee6fbc2d26e86fbda42e485a9230fa7de149c334d22eab9a9a4d7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:45:24 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:45:24 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:45:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:45:24 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c0922d06acbf8dd3d27c5f13e8ee219152ad8e0470d50d575bd72330fcfc5e`  
		Last Modified: Thu, 28 May 2026 18:45:54 GMT  
		Size: 67.3 MB (67296521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:67e7924d938247e243f46ef14750a4b8cae3db2d6606b69ac5cb5adf5cbc2957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dd8a1206777543437e49f63554fdd49a3849ff3ad784793aa5436970f31f20`

```dockerfile
```

-	Layers:
	-	`sha256:838f4325d191a202d1a3d1923957104255dee511105cda3e0c0ffe74f3595865`  
		Last Modified: Thu, 28 May 2026 18:45:52 GMT  
		Size: 3.8 MB (3829255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cded6683192dc7d2eccc5f5dec2aeae2fd74baea18b2b1a3d59631c04798e3f4`  
		Last Modified: Thu, 28 May 2026 18:45:51 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:b318e6f57660e6d50c86dd5a204aa1df0c09f0e4d1d9ae704eec3d881b291fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113119171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f2f6bfaa08c1e6dbef660707e4fd13f847e2364b477a2a6b85b3eddbd60533`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:46 GMT
ENV OTP_VERSION=27.3.4.12 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:46 GMT
LABEL org.opencontainers.image.version=27.3.4.12
# Thu, 28 May 2026 18:32:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="bed9b6f89b3a4b4ae8c0bfb0ef64547680bda18012c918a10e7ed5d81f6ebbf0" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3e0ee3c983c5bb9e9abac348836666761b710b7a71a186a41728e27c4b89b8`  
		Last Modified: Thu, 28 May 2026 18:33:08 GMT  
		Size: 66.0 MB (65963582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f9036c96a824558f5c5f0502c6cbd95fe261c6d45a4756d7c81db9bfc4bd3159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a009eeb3d9dd162115b549b233aecaabb902255c52419b8a064375b5cfcd3b`

```dockerfile
```

-	Layers:
	-	`sha256:a0a2f2f0afa49bac4151efd5bce12502a1852319f154fee62685163c01598fa0`  
		Last Modified: Thu, 28 May 2026 18:33:06 GMT  
		Size: 3.8 MB (3821633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ae264214193a7cf08916c746b3c6421c66dd8db7a0ece1ac815a494dc86d7e`  
		Last Modified: Thu, 28 May 2026 18:33:07 GMT  
		Size: 13.6 KB (13639 bytes)  
		MIME: application/vnd.in-toto+json
