## `erlang:28-slim`

```console
$ docker pull erlang@sha256:0607fd05273e139992bef953c3bbdf982cc5f397cae432bd08a4a34e9f9703d1
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

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:a7eb04055722293082fed3de721c6a618f9e5660aef862ab1b0afc358d24cc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128245971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6164f8ed2ef934967e1726c4235d37726d7f750576fb4a59df1d7c2004a736`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:59 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:59 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:29:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:59 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96732ff508890c208cf3ababe2ab5441066adcbd18b49f57d7c6d8c534a4690b`  
		Last Modified: Thu, 28 May 2026 18:30:13 GMT  
		Size: 78.9 MB (78935348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e62784071c9db69abf4efc62e2ffe52df701eb4d0a7225c9e946e887f2244f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee3963a0d19d503137460cd247be070488e4532bcf9c419313ed50ef2b1f868`

```dockerfile
```

-	Layers:
	-	`sha256:f2f80f60c316c869d935566304b6e30bb882d1061522fc13854c0c31c5140637`  
		Last Modified: Thu, 28 May 2026 18:30:11 GMT  
		Size: 3.3 MB (3283724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f51365ac085973c36de119c4237dafc2eefb21dfa28dbc45e8da9c57500640f1`  
		Last Modified: Thu, 28 May 2026 18:30:11 GMT  
		Size: 13.6 KB (13637 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:b19640514ac1b4bd192a01fe1ca95c64967b89a3604b56a993024caf2fcc27e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116921291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb98608e440aee28ab284effc71122efef5e174c06076ba145a2f5a4e42e32e8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:52 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:52 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:29:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc69e5cd8c5b62db5041a70be7c40f9b8e20016023ebdd0903f5abea8321f1a`  
		Last Modified: Thu, 28 May 2026 18:30:06 GMT  
		Size: 69.4 MB (69433245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ffa17979d9195382aaa6e89496a565b314b61af5d1f4701accb6299753611b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8903d9739de8a64718c47e1cd6fef81a94bd4229f232c92b44c4fb3e62f223`

```dockerfile
```

-	Layers:
	-	`sha256:cc4dfcda9dae5e91e20567cc289f273571dcd9b291c8434947d9ac0fea312a2a`  
		Last Modified: Thu, 28 May 2026 18:30:04 GMT  
		Size: 3.3 MB (3286691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dab9d546eeeedbfca50a629450277bff52171b04bd68f503e8250a0128da563`  
		Last Modified: Thu, 28 May 2026 18:30:04 GMT  
		Size: 13.7 KB (13716 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1b1b40a98aae4d83c70de2aaad8cc565c7dd16ebca6ab0fffca34368c379c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114737406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca11464b19deda3a95aa9c3e1a1ef8d32e362db6ad3701e10a037dd58a39d49`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:30 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:30 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:29:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7dfa23d37d8c469d05501518684bda1daae0f1acb2a86a8b4c15f603c34aa`  
		Last Modified: Thu, 28 May 2026 18:29:44 GMT  
		Size: 69.0 MB (68995375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8553e4925280e669959212d8930abd45e06da38a244af67edc7d6da7838fec8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77805524a6220e198a528f386e9d3d3199c65c63b48643936dcd242372af28fb`

```dockerfile
```

-	Layers:
	-	`sha256:f44ebb75b5ad77c1504c4189dd625aedb87a0d3b89b9bdb86dd48b89c433043d`  
		Last Modified: Thu, 28 May 2026 18:29:42 GMT  
		Size: 3.3 MB (3285140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb34e918390a1250d82a3b81600c0543b64fbba2d85e48f761eb7f7344d1c3af`  
		Last Modified: Thu, 28 May 2026 18:29:42 GMT  
		Size: 13.7 KB (13717 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c385b57f86469f369a19e4495adbe1a4e18790583f7e58465eec1b983d39d8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127154081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0399a960625ffed2b8ee4b6ab6ceeed55569e57544313585de18e42f373b5a1f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:03 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:03 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:29:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621fc96c45ea0937891478a1191c8d7eb5cf5c06cee9265e90f3fe16338ed80b`  
		Last Modified: Thu, 28 May 2026 18:29:18 GMT  
		Size: 77.5 MB (77481861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e8e9d47b66b4e92db39183d3f6a338d4cdec707bbc42c235f995fc61e1544cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b618970b501ba85fa309eb2a07019585a6579cd26ce9a260f54631f3624f6a`

```dockerfile
```

-	Layers:
	-	`sha256:fa3914d06f478d137efea7680f20416e8abd17768d29e004ac26d3cfcbcc931c`  
		Last Modified: Thu, 28 May 2026 18:29:17 GMT  
		Size: 3.3 MB (3284610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f15528eb3b797a0a62f63adaa83f394088800aae8c31af0fcc03f383e1a8041`  
		Last Modified: Thu, 28 May 2026 18:29:16 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:bcee765af12512d4f73898cd2ac1285cd0563b55be9f58de750fbd28e0495d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120247462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8020f2b36b8e34fa386db1682b27edaa6b3e39b463cf195dd327e950e858aa0c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:14 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:29:14 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:29:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f76f4149b6a021fc254749d9ec6ba09a391bc72b5fad046c9806a9c9e18a16`  
		Last Modified: Thu, 28 May 2026 18:29:27 GMT  
		Size: 69.4 MB (69417908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:72b8483def81bd44bc9e9a227e9ce751d6610ece7591ec3662e51a7245f60a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d45b17e0ac2ef203849ec20a68d53604f3a090dbea17d6f45d7d4dbe6bc3b`

```dockerfile
```

-	Layers:
	-	`sha256:407e7868faf223dcf99dd21b60153eaadd9c8d06cc557f91c0ef7f2c3441e8ac`  
		Last Modified: Thu, 28 May 2026 18:29:26 GMT  
		Size: 3.3 MB (3280899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9781fa3553c3048aa7cc9657a44975d0a62d2233067391ec38323d5f15c472`  
		Last Modified: Thu, 28 May 2026 18:29:25 GMT  
		Size: 13.6 KB (13605 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:85ce1b7c468844d9105c01b00cb951e0ba505ad9d53b37301cac3f555d9fd116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123518819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1cd5be8e1a4f3155522e692126034a5ce93ac094ef32e362dddc258049884`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:37:10 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:37:10 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:37:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:37:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba49022066834e18b2e4b4fd7a9a817fec59b53ac0881cd25e8a4691293745f`  
		Last Modified: Thu, 28 May 2026 18:37:34 GMT  
		Size: 70.4 MB (70386637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7ac221fd8dd9776cccf08646de181cd3e0efd2fbe59e1ee12c9246ad790df2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa547899cd574b9c241b7224c8bf5259dad3be9e5a35e96bf9d922db2337b551`

```dockerfile
```

-	Layers:
	-	`sha256:462535fd2ddc6287d1dfc945937caa19d4df220c6d61e1f7ec3eae02f3b5ba53`  
		Last Modified: Thu, 28 May 2026 18:37:32 GMT  
		Size: 3.3 MB (3287309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e64daed9f339320c4d7c78bc39dc184c3bff32937105095fea35238274e8536`  
		Last Modified: Thu, 28 May 2026 18:37:31 GMT  
		Size: 13.7 KB (13681 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:2ddca32637c15f453c2fa7030b691a238444c3c337ed79f13baa97fe806ca048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119648999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e4f77330a75670b2e7d56a17f408766d4fe0c159598b29c807c516364be4eb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:31:21 GMT
ENV OTP_VERSION=28.5.0.1 REBAR3_VERSION=3.26.0
# Thu, 28 May 2026 18:31:21 GMT
LABEL org.opencontainers.image.version=28.5.0.1
# Thu, 28 May 2026 18:31:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adcc18a958713356d251980004b552b66e9cd33493e7c60c325d2f523b33329a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:31:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c60ada471921645190882a79a529b4141d8efc47fde94028a63f229500aee`  
		Last Modified: Thu, 28 May 2026 18:31:40 GMT  
		Size: 70.3 MB (70269219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:82a2661144bfeb57058f8ad78a431d7ae5a395725c591d58a1069638793065e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5259f379c4401e3cdfe6cdd1302e4ead94f122d23dbfe3973b0b0029bc1203a4`

```dockerfile
```

-	Layers:
	-	`sha256:20923f9f13d0e2874a47d1827f8b9de68251917b15153edc588646bb77c399a3`  
		Last Modified: Thu, 28 May 2026 18:31:38 GMT  
		Size: 3.3 MB (3285165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00d8b5946fee038e7c0ecaa5613ce08596a548b7e189af944d96b6583bb63c5`  
		Last Modified: Thu, 28 May 2026 18:31:38 GMT  
		Size: 13.6 KB (13637 bytes)  
		MIME: application/vnd.in-toto+json
