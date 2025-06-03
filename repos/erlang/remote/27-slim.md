## `erlang:27-slim`

```console
$ docker pull erlang@sha256:3f4a67bd50d7ea8a7191573f1f58d5c6abd321ba68e6b61973fc9a44d52e8c46
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
$ docker pull erlang@sha256:5b6341dbd7f80e2c027669bd440bd84c5a13eb49cba6152b3327d062cfc9f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124458371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db92f6f23364483166c60bf0a1ce18d0e506c1fe6af2b151324fcfbbb6c754d`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b532dc6bb844e0499a84d1def9d5bc3e966e9d33e83d2e2b5b9e9db76619f37d`  
		Last Modified: Tue, 03 Jun 2025 13:44:29 GMT  
		Size: 76.0 MB (75970126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d96fcf26b5f4468b8b9ffabdf20238ade4b04c38657a1eaded2e0da87e21b796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873db74ada02c3c4bb9f0abc79d6b0fa367b1b0dfb5cef732d7ecee66bf7f36c`

```dockerfile
```

-	Layers:
	-	`sha256:7566024bb3005c247795c4a768ab9d2b1683ad0aff15bf8790f21c831ff886ae`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 3.7 MB (3726723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8321b854ea4a1dd1739b13172aea020498705e8a4f36ee42992eb33cdb794d1d`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:89d77f0360e2a83bf1fccec2a1aaf8950ceb61ec30ee21deff90f679f3a4d58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111500407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748cbe433e32904e803d82dced035fadb9732f3396231ed996c5acb60124f483`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883910c9b696c8230bdd5a9e12a893ee757ca63bb5050b1c31847917881df6ea`  
		Last Modified: Thu, 22 May 2025 01:21:17 GMT  
		Size: 65.5 MB (65478923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2b6734a5fec5b047ecc34fba780c673636d4b4966977cb79a4965187028ea451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f72dc6dec22cb1126fec6fbc80b0fd0ff68b155e149e0d9e2b4f3939c0ac6f3`

```dockerfile
```

-	Layers:
	-	`sha256:a33fd5bfdf971c11886435478f15716068784b615c46fdd0eb5e0768dc58bb4b`  
		Last Modified: Thu, 22 May 2025 01:21:15 GMT  
		Size: 3.7 MB (3730539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb367cbe0dfd6761d466c0617f80348384367742aa7cf25031be45ebd55884d`  
		Last Modified: Thu, 22 May 2025 01:21:14 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:fdd1082beb82b537fe72f490e5f8e13fc53f4b28d72ca62c75934265a2b45878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be861177f389810ac2cb296cbbb48e1f48dc7550ebdf9f0472491ab328a463`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056b24923370ab4a3c97776cd28a77d8c5015a0cba802d50d1263ab7a07149c`  
		Last Modified: Thu, 22 May 2025 02:44:26 GMT  
		Size: 65.1 MB (65102451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:acf60dfee4fde75a256be36923080e22d4069f74ee4d4ad2f64294fb1ba3efe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff743142ac9cf3d86484ca089e9e7a9991b55fa1e72ba37ff720a609e342ec1`

```dockerfile
```

-	Layers:
	-	`sha256:d95c432c6d2ec693c27f990f348b22dc7bc4962540f0e903e78edecc1e8d782d`  
		Last Modified: Thu, 22 May 2025 02:44:24 GMT  
		Size: 3.7 MB (3728964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c686a6e69f86c8616abba21aa8ae9ca898280fc093930668bfff478dc24a7f60`  
		Last Modified: Thu, 22 May 2025 02:44:23 GMT  
		Size: 14.1 KB (14050 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:75faf032f7175f217e863a227e4434e0eb7417f9da378f2591c5d02d5071476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122042335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dea886b91d087f2a3749da08b6525e1ffeb75022f5786d189ad6e5907bd6b0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f204126c24e8ca10364bad2de3a02ad951a5617703fbb99d9b2a7e787468a8`  
		Last Modified: Tue, 03 Jun 2025 14:24:20 GMT  
		Size: 73.7 MB (73715154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8b0b9deff513c1eee1afeebb5e30592aec7dc1124e3dd7e664a6073a175923f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153be7f294ecfd9aaec5b8dc00b1cbd068a1dc2f35c98d3025403628bb8c249`

```dockerfile
```

-	Layers:
	-	`sha256:21916f38a987e935833adc4e05606a0a5d77549c7473dc79bb30036a4c6cceae`  
		Last Modified: Thu, 22 May 2025 02:59:29 GMT  
		Size: 3.7 MB (3726996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3182554f32ee98e195a38eb49e41ddd8080667f6ee02e6f434d07122a58fdd12`  
		Last Modified: Thu, 22 May 2025 02:59:28 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:e74b56d8df791ae0b9629a721bad33e9b4ca37c544b19277cfbbade96cddc755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115604771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b0c1095dda8d5dcfe56f38ef9d0c515162368d3ae9ce05663a5574f8249555`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e223e1d58fa71f9754c32152df93b00150be78eac391a772582602e4560f645`  
		Last Modified: Wed, 21 May 2025 23:23:07 GMT  
		Size: 66.1 MB (66133209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b1fffca2d9ff12ed755c3ff642a4acff8e2ae62e3605d31821c6f75f2c68fa1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8813c01452faf293783c702978d1f9d7e42b0c473a071cccf1f6949156691bc`

```dockerfile
```

-	Layers:
	-	`sha256:6ea8c0f91a3a95b27559ada69d5e8a249e87eb066a6e07c19ee220079470fb6b`  
		Last Modified: Wed, 21 May 2025 23:23:05 GMT  
		Size: 3.7 MB (3723885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee38ce52a63bba762bdf77dbed52142507103788b26c8e60495cfd6ec3e5d3a`  
		Last Modified: Wed, 21 May 2025 23:23:04 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:4d79b53107ba848f541375830278b72a5cd34e0bad148a32ed737a0e4e56ba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114826577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63581ac736ed1daa6052daa14f9f0ee69a7ce740367452874a255f33be2a2e0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51416a61254901b7d3598caf4c21885679cf3cbf93ce400f93c37e616ed79c50`  
		Last Modified: Thu, 22 May 2025 06:44:13 GMT  
		Size: 66.1 MB (66056824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7eaf4a05a1d91be87242c8b04b1171fbb923c317d365102f0942d98500198568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87886579940542a4af169a4264944dec17956e2aadc403b5de3b68a9c396e76`

```dockerfile
```

-	Layers:
	-	`sha256:4f51650e3b58b94bd0a4827d8581c4ba67ed8334b77890d7c74e0e2fafaa6793`  
		Last Modified: Thu, 22 May 2025 06:44:06 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:32aa712afe32b8cd1cd7f4995a44fa836167be628f2d8563dd16d3346ad6889e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119541111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a620c2db6a3ae7041e24f4b42f591b1900cbb2ca7be9ef19afbf91e4cf7e582b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a68bf3e2e018f999cf755140c2ff5c71835edbee1cad4cd4e2381aa1cef1e`  
		Last Modified: Thu, 22 May 2025 07:40:23 GMT  
		Size: 67.2 MB (67209492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:739120af8565fbc4b15ea6e66b72d03f4ae58a77ad1d8e6850323491b14bb886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c12e7d72ebfb6a9d88f496304ec1e676311f342567b7de902014681b592cf41`

```dockerfile
```

-	Layers:
	-	`sha256:0b9e7f50c3a98a315f6bd289037eadaeea1d305dcf70041d56b1e1b3551d7c26`  
		Last Modified: Thu, 22 May 2025 07:40:21 GMT  
		Size: 3.7 MB (3731167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d871c294fe17f9ff85e79b87e738b49fa0c34ea12e5fc13960e8890609e6873d`  
		Last Modified: Thu, 22 May 2025 07:40:21 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:037fc299ca38efcef4629e09ac7b72960043e5b280215ae7d54332b82ed84e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113027954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ff216add8f6d7b7ce5bbf351440ea4bc6019b310c238137f0627546ce8ce9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1ad4ab826223f4013aac65111aff617a0a844fca27318b9a433435454b6cc1`  
		Last Modified: Thu, 22 May 2025 01:12:29 GMT  
		Size: 65.9 MB (65884112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f4bae109356d87da71b9fe200f7899026b8decfd4d1d501fb47134af9f207ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265028bec8f97a15f5bc4f6c23d41d3a20c545244355c12c2671ab75d0ed4c66`

```dockerfile
```

-	Layers:
	-	`sha256:ce03c43743b5fad17402b34dd2cf505abc1ab1fca41b228589fb07932b470f19`  
		Last Modified: Thu, 22 May 2025 01:12:28 GMT  
		Size: 3.7 MB (3726443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06395d8804ed46eee02bd322a4232b9a5b8f0d6150df65a0dd89757dfa1ae8e`  
		Last Modified: Thu, 22 May 2025 01:12:28 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
