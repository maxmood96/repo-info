## `erlang:24-slim`

```console
$ docker pull erlang@sha256:232752c87c2a3b0f63142fd40d074c2636ddff86d22558a579ebc91fc58d0d81
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

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:fee00af0d3348cbfc5f8b581c60585b2ad0dca05490ac0e3bf5e7e7555c3bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118998190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0407cb3744087813f709d8b0e494273303459580755954cee34abe477704d814`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a015db544f70218a6d6e6aafaebb5fa7ed42318dca6804c44be71e0e7bb68`  
		Last Modified: Tue, 10 Jun 2025 23:44:20 GMT  
		Size: 65.2 MB (65243408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6fd7fdf7067dc5973b09d1aa3baf1d94eb46882bbaecd0607218cd88acf77d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c117e4fe2e98275e8383d3a5ecb1fd04b8ccd52136615213e442fb7581213c7`

```dockerfile
```

-	Layers:
	-	`sha256:dc8cca4b01d3b6b789522a7d0715f2f60d273d34ab349678f88717f6aa091b73`  
		Last Modified: Wed, 11 Jun 2025 01:46:24 GMT  
		Size: 4.1 MB (4098871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62482c23ad5bd724c454b93bb79338cf547c3cf4cd8409100007a69cbf6cbd8e`  
		Last Modified: Wed, 11 Jun 2025 01:46:25 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d866a971e5a229b7aa44a755fb03c62d18b4bc11dd10a88f99b80b59527d87db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106270345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2324ce0e3bcad6e1d3ebe56e83e13860af596186dadaf65d45368aca4b44de33`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9322ef6cdba1f9a6e66697dd1b13a7280cef8cd7924fd0f3fb386d5f6fd1afc`  
		Last Modified: Wed, 11 Jun 2025 05:24:03 GMT  
		Size: 57.2 MB (57226391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:98bdf91c1eebcf514c9a52e353c30a185cab37058a426601a33edf5dd1cd4eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f317f7a4fff0b6d8418af893c884720465f9c84aa7a2f0d15f7828ff801181d3`

```dockerfile
```

-	Layers:
	-	`sha256:8abd41f7212f13fe1b54410ae5188dc44de830539e2bac8d1a912b4d93642c27`  
		Last Modified: Wed, 11 Jun 2025 07:46:23 GMT  
		Size: 4.1 MB (4100472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3949335529508a842d90f89dbf30771f29cd0e2615d2c5930efb844eb54bb46d`  
		Last Modified: Wed, 11 Jun 2025 07:46:24 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4acd9ab1e1204e1ac0869ded37c800b763b77c4c618817bff6a0255e426c30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110330171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abec6f344b153e0f51776b169814b994eb329ebbba996321bc70f3a8b9f97a4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2375327b973f5b9efb127f7b06af8f81cf5edd02e3f677b41094ffa39e569cf2`  
		Last Modified: Wed, 11 Jun 2025 03:19:38 GMT  
		Size: 58.1 MB (58077870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ca668b0a226d05ecad14609655f5e88b012cd9ba76db91ae5007dfd8884a2206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681319b76437af63a07d873d2893c08209dcdf464f82a99637af02bbad6f40d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d3d32230315df05d9d06302e61a22ed1fe65de2046b75c3789fcd0795efc4ba`  
		Last Modified: Wed, 11 Jun 2025 04:46:32 GMT  
		Size: 4.1 MB (4098492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250373cdf9c1333219e4c03f23cf9c7db534bba97c14c577366baae22a1f7c41`  
		Last Modified: Wed, 11 Jun 2025 04:46:33 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:f9cf86f5c25a68a1b63e9c899546e373d9440e6e8c97fc81f408b0490bf6d096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112395899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97849e63fb2bf36daa987d1059b2654d8f196c5dacbaf9896c41b75f641872b7`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286421b74eefe917bd8e9ae72ca6b10d848d8b9439f5507dac2fa9e774ac7926`  
		Last Modified: Tue, 10 Jun 2025 23:42:36 GMT  
		Size: 57.7 MB (57705887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:46bbb756bf22277ef1537b22ae801d5bf253fc300147fc9a175da44bb447c8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f662a0960a630d57c19db28c4b0331cb1971c1fa3e6f9627850e981df5b4be05`

```dockerfile
```

-	Layers:
	-	`sha256:b2eb2e0d77dafadc2c1465ddc812fe4108d1ff7ce448625279ae25fe68d788cd`  
		Last Modified: Wed, 11 Jun 2025 01:46:42 GMT  
		Size: 4.1 MB (4095399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23954522fc7362942540ee9d6bf5e1c17f94ed729b5f027dd5ac7dacb8983522`  
		Last Modified: Wed, 11 Jun 2025 01:46:43 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
