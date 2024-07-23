## `erlang:27-slim`

```console
$ docker pull erlang@sha256:bf22cd580537d71db838a04a8641210799c9532f9b5159bf03481a5eb01a3dd1
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
$ docker pull erlang@sha256:4ab6827b36d3b3d727ee29308ff7a6a3e2f81c3089b2428984346f88b16b8b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125509650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde8a4780fa4f9930f99ea24d6bd2ed35069473ea3bae727c0543ca749ed23f1`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089703fe6308cd7d7838bc0071f1cffc9a093544f08de27a8307fda6a0f640fd`  
		Last Modified: Tue, 23 Jul 2024 07:27:06 GMT  
		Size: 76.0 MB (75955575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2e0b3ccdf85e4803ed9e211223c674b5463ed0791fef218a8d32e44179fb9677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d511c9feb34cbcb2e2f6d7f01767db2647ed0efbbd3c38438a3f9e9cc6d2e2a4`

```dockerfile
```

-	Layers:
	-	`sha256:b7020ca37b69e5b5e2e3c248e23337da4c91d756892eaa9502f98d5e00c4a10f`  
		Last Modified: Tue, 23 Jul 2024 07:27:05 GMT  
		Size: 3.7 MB (3696089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da1e45d4e72ed1067e95d542b0861b9a4279ada4bcb8b36d0986dbcc30a0ccc`  
		Last Modified: Tue, 23 Jul 2024 07:27:05 GMT  
		Size: 13.7 KB (13655 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:55b3c045087994df06641e0965d61578e669ea7ca1fa9cb898328316f691d98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112695265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03954393c82a17a0678b8be351d71d96b08b54d0c0ea01e9e2b6500f617bccb8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4d1420cca7228fa717108ac52b4a42d80ec9d2fcd4b7edf08b272ad0e9bde4`  
		Last Modified: Tue, 23 Jul 2024 07:16:50 GMT  
		Size: 65.4 MB (65374886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4d1833c8d23f9a1ebc3d868b4c4d783301bf008c9674a7239e67d8d867e6d3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c294a79eeed5a2e827b8e78dc86b05fcc837475dfcdfbf31f257c53a17dcf8`

```dockerfile
```

-	Layers:
	-	`sha256:8f7bbfc9607282b8da7af4ec80fe4c5fba43374d07465d8c884a532897ac514a`  
		Last Modified: Tue, 23 Jul 2024 07:16:48 GMT  
		Size: 3.7 MB (3699490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c443ebde0bc40d46afa86538abb63cb7582a4672a9deedd87ec560b0b74e0b59`  
		Last Modified: Tue, 23 Jul 2024 07:16:47 GMT  
		Size: 13.7 KB (13733 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:51c2f8240c3b81c0f1c7a895d31f86bb730546b4854fc08a0c22e403cf0b9fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110147065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b51f753dafed942eb7e81077760d5d36d180fe1c77be6ffc79c170627418a18`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaae0ed3c8e75022dd725e8d46bc47002aea46bad23470c1043c07d9c3f6adf`  
		Last Modified: Tue, 23 Jul 2024 12:47:19 GMT  
		Size: 65.0 MB (64999007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:18c6f2ac4a445e80b99f2c96a4672a9cc93c9bd18bbf441a0c18601d5dd6275b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4bdd4b13c732b0bf4730e1c518c5c36ab74e42b18598a70db6bd130cc4fcb3`

```dockerfile
```

-	Layers:
	-	`sha256:b132b234c56a7b87269dc0453b34ae6ee7ac0a8a959f0f78f213392bf75bbc95`  
		Last Modified: Tue, 23 Jul 2024 12:47:17 GMT  
		Size: 3.7 MB (3698329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9de8cb509e1075670a0dd64ccb4c40d27b5f1a0002e30ceeeb7c66194366f8`  
		Last Modified: Tue, 23 Jul 2024 12:47:17 GMT  
		Size: 13.7 KB (13733 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:ce78ee560b6f4c023956847b79dd8fa0be11003ab047d20c9f8556378f1e73a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123163496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de41b531998c8c00270f0e8485c24a014a5c2acb511bf323737dcc1bc9c1cb9`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72db28329b7e4b429715c1cc48bb830985ef0823ad373408aa474d2d63ec5d`  
		Last Modified: Tue, 02 Jul 2024 10:43:03 GMT  
		Size: 73.6 MB (73575048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4e8c46a2e33cadf79bce156722b1627a4f9c093cc37ad7bcefe489a3b2f39521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd39a786db64624f870a02784a509c9b13e69363fb2d6f4b0fe4e400fb2bf001`

```dockerfile
```

-	Layers:
	-	`sha256:87f430edf445c427701b38bf42775e77b7dcf87672ca7e5fcd9a6a69835242cb`  
		Last Modified: Tue, 02 Jul 2024 10:43:02 GMT  
		Size: 3.7 MB (3671966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935650511e4ea148827fec56a33fa0cfb543009fe9b7244c3eb3fad32ef93703`  
		Last Modified: Tue, 02 Jul 2024 10:43:01 GMT  
		Size: 14.0 KB (13971 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:7fdb1449238718617e1692fd21ad715469be0494c51e7a2d759c0dfc388232ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116714135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bebdd4b89339a6cc3df29938f3436282247b2f0761b7ee0ec974ad7ed31ad8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88a8928dd857c8a60a9ff88f675b9668fb20a4d20ce19cfb3eb4f6ef3d4988`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 66.1 MB (66134715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0cf3a4d49ce72c0667e6e5f560d1de9c12fe9490b1f301ca87d137a48e8b22e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e1df0d4e528333d0c042b46e2bb5f74a0929dd6cc5105e2efa7da1a2bc5fe0`

```dockerfile
```

-	Layers:
	-	`sha256:d4044ba003c52d16f9dcbec5f449a55a554dfa9324fea516ba2b5739d5dedff6`  
		Last Modified: Tue, 23 Jul 2024 06:16:17 GMT  
		Size: 3.7 MB (3693203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eef4dfd486c313ab5c4ec0d881c01b0e473002e520dba479fcfbda33b73a30b`  
		Last Modified: Tue, 23 Jul 2024 06:16:17 GMT  
		Size: 13.6 KB (13621 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:3009eeac69ae3bfd3a98a23c873ed56b44a5ffa04d492c43d32e1dcc0508fbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115406486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30b6dc5c4eb7a7db6cf889034925186a6e1a27853600a3b5ce6274ba5e9fd9c`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:7398b3272eb97d7c196f6072f2a25952abf995169e82ecb85361b7659b2fb005 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:827f475650f14eab4a6679f0e49d9155db82de1d5209a3817922c689f46adf08`  
		Last Modified: Tue, 02 Jul 2024 01:28:47 GMT  
		Size: 49.6 MB (49563118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7dabb57db79e28b5fc7c5af8d51b4ddbaf9858b8ffca5ea62b908c81faa99`  
		Last Modified: Tue, 02 Jul 2024 14:05:52 GMT  
		Size: 65.8 MB (65843368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a94e67423686c044571c228f2e884ca6a340419cbddb99ac2c12560a0d999fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e6549dc314c736fd96780402ef0af9da3d1522f03834998c789ec3a9eca5a0`

```dockerfile
```

-	Layers:
	-	`sha256:1675c42f3011db4d580cc41764acfbd8e38144133cac3530c4de6ad6be9e9138`  
		Last Modified: Tue, 02 Jul 2024 14:05:46 GMT  
		Size: 13.5 KB (13502 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:3506c119dd1ba3fb1e57ce7232adae02820506c1da295ceb038e340cdf58037b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120642640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56631c999aa9912ed54d40a4d1ee33f77d0d760dee6dff1fa570de04a3a2b8d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3120a53c52effcb344f119777a1751704833084c4fd0116d5b0a8dc87894b05d`  
		Last Modified: Tue, 02 Jul 2024 07:32:48 GMT  
		Size: 67.1 MB (67085625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1122e4dffef1947fcce956f4290e1c54d87ad823ad7cf42f73d6f63f843a2253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19374fd2e27e25f9fa5c2b2892b9f1820d614018fc85c06e4c3a86f36e1a1f4c`

```dockerfile
```

-	Layers:
	-	`sha256:a76f289d2b59a28edf5925604898046dabc61f715bf1713246182a48aac84f56`  
		Last Modified: Tue, 02 Jul 2024 07:32:45 GMT  
		Size: 3.7 MB (3676039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b760b7f571cb2af04549549776330f71cc155e0e6aeedc6033068ec60afd5b4`  
		Last Modified: Tue, 02 Jul 2024 07:32:45 GMT  
		Size: 13.7 KB (13699 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:d5385dd9f5d64ffd143c8ba634b3e8c9e57288eec6de8eaa336559eb4036b8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113696166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c19c8971023a612b9c90512a21a0c9ada1947d40b2cb0295559dff92d9e9ba`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937292c1f4eb068355c8ca7c7a054519907c0d472cbb09d9d07da1a8fcbc608`  
		Last Modified: Tue, 23 Jul 2024 08:57:49 GMT  
		Size: 65.8 MB (65764641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7bfc35f028fe6dccfdb348419258fb197e5984ee45b9320623d8b53ad6ba6c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf9a8e093875e1bdf44b85dc66b1ad3c0d3cdb3f9d6fadee041bde4f4d2f01f`

```dockerfile
```

-	Layers:
	-	`sha256:173b96faaa7f453015451a4a8f0bc2ef08af20feaa0b362bdf17a1499b2efdff`  
		Last Modified: Tue, 23 Jul 2024 08:57:47 GMT  
		Size: 3.7 MB (3695916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c578e0051658b37b79e1040ff5fb5087e2e4b9306676d0f4477f1c77f49f65`  
		Last Modified: Tue, 23 Jul 2024 08:57:47 GMT  
		Size: 13.7 KB (13655 bytes)  
		MIME: application/vnd.in-toto+json
