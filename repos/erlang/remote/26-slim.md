## `erlang:26-slim`

```console
$ docker pull erlang@sha256:3c141ba86353a3117d42bbaf97d8b957926b9a7ac715f8f82328b399d75b7e9d
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:926b663d5d4ee6d63d50d62929259e81d7c505b1502c5cde629c252902e085ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118967035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e564fb4a2fce26dc6ebe4581bedb4814f8edb2a494716020b9fb3dbf3bd796`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:33:27 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:33:27 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:33:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:33:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4085ce34a10a768ee290766bc36091fcab669368e26f330a91d9268da28e071`  
		Last Modified: Thu, 28 May 2026 18:33:41 GMT  
		Size: 70.5 MB (70471603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7088ef6b6b9680dc235056b103067d393ac1d397ba7b363d62e9adf94d383de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c27a76bb86393eb5c77500705aaf45e43384825999553c17e970e4ab5eb6e7a`

```dockerfile
```

-	Layers:
	-	`sha256:4dfbfde3147073bf975f61a21649f09217b899b04b7fbd98867101096d9a4640`  
		Last Modified: Thu, 28 May 2026 18:33:39 GMT  
		Size: 3.8 MB (3826036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8612391ebe504746328b0614dd62b86fd6a394abac16607c78f3f3c6f2d4fa81`  
		Last Modified: Thu, 28 May 2026 18:33:39 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:446f8661706181070f15fcc41fcdf2a90c6bef851e7e2644b6749a18d0c0052a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106600051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178d83624d9569e04d2da77fdb9f38eda3154c0301f308289abebe474563977c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:34:50 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:34:50 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:34:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:34:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7bf51d1fd551501879b759352fb7d87bd1ef4c49d5bff8f8a4f43d5742cf3e`  
		Last Modified: Thu, 28 May 2026 18:35:04 GMT  
		Size: 60.6 MB (60570548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8ef30a9b6cc2bb2455eb71c5603e94ea27df7cbe531c6c2cdcdd9010e0a3c582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42714c88fe9dec4782ecc7ada7e83d9a50da0a9cced5b37b1ad540b176787188`

```dockerfile
```

-	Layers:
	-	`sha256:31c0a04fb80ee08523a7e9de5baed566de7e3f3a8bfd3bf3d2a03aae5305313e`  
		Last Modified: Thu, 28 May 2026 18:35:02 GMT  
		Size: 3.8 MB (3829844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e3284cd782795cb59b6e6b0116d5882003165232bab3139e77d082786fbf54`  
		Last Modified: Thu, 28 May 2026 18:35:02 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:ca24416ac0291b8754650d912c7486bed880034b56d6ada9cb020f735ecf1549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104394627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babb666a7f01032d8780289060ed0288eea3822aa00ea8282412c27c889d069b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:35:31 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:35:31 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:35:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:35:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af8d265a7af6e31ef5a731aa2eac3a17be707bb4fe4f2a6aecf80cc8bca6bd0`  
		Last Modified: Thu, 28 May 2026 18:35:44 GMT  
		Size: 60.2 MB (60185473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:499e7cee302d8d8904145e2918f9a05ae7923330299a2c384823dea6abde5100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad13b0ef0eeed885caa6a77bd0606b1e1b17f92330024bcf537decff84d54e`

```dockerfile
```

-	Layers:
	-	`sha256:18ec4b08d66448329e4359f8cd26b590daea1a5208a1d55b97e69b1525947650`  
		Last Modified: Thu, 28 May 2026 18:35:43 GMT  
		Size: 3.8 MB (3828269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4932a4c49582d87c7040b4105df81a058790c2439699318414ba2871fa261d`  
		Last Modified: Thu, 28 May 2026 18:35:42 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c89271c32d796f752d516823d9e1f3a8a941746761ef75d77a23d538e800eb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116489055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8392aa7a679d3ea481a871de7a4f7870e183f4cf017f72cbcb59cbb1a4c9d3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:34 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:34 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:32:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4944cc401ca9592455ab628ccd7644bbcd27cf8a512bde6ff1067011a0c0cc`  
		Last Modified: Thu, 28 May 2026 18:32:48 GMT  
		Size: 68.1 MB (68109623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5b3829bb42d446c9cd6545880913077a8b18e28aea12793233de85d9b7db454c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d252ff4ccf2b6fda67649979bf1b52b2a984c5eb79b9398c5ae0340be01f773f`

```dockerfile
```

-	Layers:
	-	`sha256:3fb13c5b6e4a1f0db4f654244d2a96033427b2563cbe88cadc6ece5c22f24d36`  
		Last Modified: Thu, 28 May 2026 18:32:46 GMT  
		Size: 3.8 MB (3826297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4830b82ee21154c9f95a5467cfa771b148e83631ac6363333b1926b2ec40ec`  
		Last Modified: Thu, 28 May 2026 18:32:46 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:e141aac6ae5568d7dc570bf9231d99f1d1bca9ee656fa737ae8ad14e4965f9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110696536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c3ffbdc5ac506f9b886535a882aa78d63c0603616fe6bc638124a027d6d38`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:32:44 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:32:44 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:32:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:32:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede20191eeafb7083a1734f25ea89a8d53b28a9b575cbb401d945f51140122c`  
		Last Modified: Thu, 28 May 2026 18:32:56 GMT  
		Size: 61.2 MB (61213416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b4820aba3f660e3c0cba92f758c39d3b567800717e56fa45799cdcc5580a36cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a49d1df55bbe2e180d1c963516637f9a67fbee7577b50f343426d24603a427`

```dockerfile
```

-	Layers:
	-	`sha256:257c79b33c4da60ebeb27e21ee523d8cdf068817dbea40808a1b3abc5ea4320b`  
		Last Modified: Thu, 28 May 2026 18:32:55 GMT  
		Size: 3.8 MB (3823197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b55c7dd76b143921a2b140108f2fc3224531eaddf4f720d05217cbb4ed77c23`  
		Last Modified: Thu, 28 May 2026 18:32:55 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:c50c585f5c00286e4ae91b4b7f8b96e7de4df7c5bf6632d0a4626efe4e2f849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109960345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ef5ddf7164661f1e1371f46f240f6386a2a18b326eb61d2d2796e460023bcc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:42:53 GMT
ENV OTP_VERSION=26.2.5.20 REBAR3_VERSION=3.26.0
# Wed, 20 May 2026 10:42:53 GMT
LABEL org.opencontainers.image.version=26.2.5.20
# Wed, 20 May 2026 10:42:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a8b12200db9f3f3b78e469e6d982e22115701d592ddb068750fcbabd1ab84cd2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 10:42:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffcfb540ae132b8a380e01e5b4ca9f424d4fa78700b03a1675403ae66cc22ab`  
		Last Modified: Wed, 20 May 2026 10:43:56 GMT  
		Size: 61.2 MB (61174106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4417f10d5d518e4f1d1a4cb7c14a71d0973bdf1d34645fb3e8f0c7f3c08dac18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a540adc071f395f2e73bdccde47c82f2489c1001d005918482d810e2309586b`

```dockerfile
```

-	Layers:
	-	`sha256:f029a187d773f779e6145576d2e90195f72cc61a55f50ad1588de7a73dfc77e8`  
		Last Modified: Wed, 20 May 2026 10:43:50 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:2914c9d4207fc181c43012b93ce445085cb2d031a5ad8162307d537bd95e6a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114630366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9368753ca4efe7ee2d6e0fd6089838bf49e2b8d217adc95ef07f32aa33558e28`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:57:30 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:57:30 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:57:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:57:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b042303434901619f95e9867530643ceb3c9738f15056545b4e28f4d0c3c39f3`  
		Last Modified: Thu, 28 May 2026 18:57:54 GMT  
		Size: 62.3 MB (62290167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4e0fe1d3321b32e6d05e8af11d727f1510a46e15d6fb25303854ef5dd1cef723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb6f0a28eba089e9ae434ad04f61913295d3a29bd8e475b5396e2a5c267cd5a`

```dockerfile
```

-	Layers:
	-	`sha256:e59666f019141de02748450397811fe77ad85964d3c171b73db0566292bd2100`  
		Last Modified: Thu, 28 May 2026 18:57:52 GMT  
		Size: 3.8 MB (3830486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4403877857ac11bccd1c4e93a3087b282ad87fea5b1e6537d2c3889934d683a9`  
		Last Modified: Thu, 28 May 2026 18:57:52 GMT  
		Size: 13.6 KB (13605 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:d3f8dc45fe6ed6e4bcc7a53785fb4697202a064e9ba48f18052bafa639d45f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108153416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe28e7790f8cda58f54c416a089aed6bec4885a82ed7ee0e0527275b2fc1e7b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 28 May 2026 18:38:32 GMT
ENV OTP_VERSION=26.2.5.21 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:38:32 GMT
LABEL org.opencontainers.image.version=26.2.5.21
# Thu, 28 May 2026 18:38:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="30e44f5978e5486c5471c367e6676a78f64f246aa22ee7eabc02e64e3c12b85b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:38:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f4e14d39578720744f6061904b4a800ffa36fe56955fe1867249855031050`  
		Last Modified: Thu, 28 May 2026 18:38:49 GMT  
		Size: 61.0 MB (60997827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7a752f7e7dfd0d441ccbede0f50550acf445e79cf4f6d119e190d6e7595b9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6c570df1c19847e0e4f4c49b9308fc9d0e4ef845920e97c35b5aa890320b58`

```dockerfile
```

-	Layers:
	-	`sha256:f23184a26eb6e56d16c6e16eae6366389d0f6313ca37178ff969d9dafa00b52a`  
		Last Modified: Thu, 28 May 2026 18:38:49 GMT  
		Size: 3.8 MB (3822864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63b84839fe4cb6b6c28607e8008ae5d31b352bbb4bb5419a173461863d795bf`  
		Last Modified: Thu, 28 May 2026 18:38:48 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json
