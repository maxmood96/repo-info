## `erlang:slim`

```console
$ docker pull erlang@sha256:609b8188005625f3d2f224f1b379505bb8c34af26eaee7c89168b83311747397
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

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:a2e06fecac517d21a727e661e3cdf2c65cb99ff8e69290a0682214bae123e84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124400082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f4334780e123835df6bc4dc04b62e7fe9e65f8bc64ec26ecea9ed76ddc094`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3286050d9230bbd93aacc0ba8ab1fc39e90d7df53789699ab9c9428f6c5020fc`  
		Last Modified: Wed, 19 Feb 2025 20:31:38 GMT  
		Size: 75.9 MB (75920395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f69bdceef16798753570fad6b359eeea1317f8e3fba380911cb64dc6fdd2f048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7b248f0a8d60f952fd7a31b8e71c2b536a75929d5bd352e46947dd04df6cb`

```dockerfile
```

-	Layers:
	-	`sha256:41a253d38b8cc4055336fe61c1e4929aaf0f23edb30eb946d9ca2056ef2715db`  
		Last Modified: Wed, 19 Feb 2025 22:45:53 GMT  
		Size: 3.7 MB (3667810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7770ddeb87ce05ab0253dd373e73e8a185d04fbfd89ba76c692eeb3b6e3e8184`  
		Last Modified: Wed, 19 Feb 2025 22:45:53 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:f3fd667657fc3c740d6b05019b5aae0c3aa8ea03211524fbc09f4b09d4b14c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111439850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8f4f6865cc728fc06a127d1c1151b1c77d2d32f0bbdb64596c6553f72609b6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 15:56:22 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc607d72402da6fe98d1eb6c9185d18ad87aa084922c7350116f2996ba1d6edc`  
		Last Modified: Wed, 19 Feb 2025 20:37:50 GMT  
		Size: 65.4 MB (65433276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:50d2d269f2ef8283cc78ce5dcc21277603e5893c41edfd0a2a47ce92c157b993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdec1f8b88ac330889459ec601fcda6b4de2c7c1fd3340af86080d2c8f86db6`

```dockerfile
```

-	Layers:
	-	`sha256:c74ceea86a80db8be642532107436dbe24f425cb7523d2fdcc1bb263623f118a`  
		Last Modified: Wed, 19 Feb 2025 23:47:45 GMT  
		Size: 3.7 MB (3711830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a118127164953920c5b08361af4c27e55cb24729670c2f6c57a64e0fdee6597`  
		Last Modified: Wed, 19 Feb 2025 23:47:45 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:0522aef516784d98010ea22fef2b4afd698b24413910c5ac16f2eaaac27c0d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109219622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb738c9e74154251ee0529c5669548ec5c26a22dc59e708e0a1e632d9d400dd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82360a0026bddd025ccafd9290ae27cf908e7f4f32faa898d03ab4d6029af53a`  
		Last Modified: Wed, 19 Feb 2025 20:37:17 GMT  
		Size: 65.0 MB (65035570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:51e1a7a7a1562da04fc978f3e3e9617d37ec0252da53e2ac3511df0c939cf621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4690c4f9237765dc55f00fe22b7606208d19672283f165a5bcaa732a33edd25f`

```dockerfile
```

-	Layers:
	-	`sha256:97302c0723720d54e71793064e95306a3b19c281e35632515ab90717a2da20b9`  
		Last Modified: Wed, 19 Feb 2025 23:47:47 GMT  
		Size: 3.7 MB (3710563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7e0fae0057c9a2483733ed0ae71003186d8666c69b77be5955b11f5d08531f`  
		Last Modified: Wed, 19 Feb 2025 23:47:48 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:827b4a0bb6209dbf826f158b0ed88a500906f65febc0747b56dcc9391d76572c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121960620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee50b66434ce9e101adbe1bb355bf0efa121a072f4de39f9c0de2d735a4ae9f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f482e0a15e2588001cd5f2bbfe431c88d2444db99de6a8f687014a368857b2`  
		Last Modified: Wed, 19 Feb 2025 20:35:53 GMT  
		Size: 73.7 MB (73654067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:40143c0f5b8760458f2a35daa3dda5a102ab74989b1b235371b113168b0f4833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00294d26eb441b92245b1b72441df34e382ab02a919856050c17d73618545a00`

```dockerfile
```

-	Layers:
	-	`sha256:c2876d31864efce7a4d2fbcd102474b0933d7dfb61f7cdca1f90dc787d2c6f36`  
		Last Modified: Wed, 19 Feb 2025 23:47:50 GMT  
		Size: 3.7 MB (3708595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e91a18fccaa4553c578b4663f852861e14abbf96838b5eaeeb02a1dea6c0261`  
		Last Modified: Wed, 19 Feb 2025 23:47:51 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:0cd7e65fbe64988a7dca5c8cf400fe8ff3cfbe70a47b4366feaa24b94bc93d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115529815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374ccd112c82fa4365314cde483db9556d021ed43f16a7dcde3ed2809ab61e57`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374bcd8bbfbba85dece282d1385ee3bdcca5954c34bf6167da76143639e32d9`  
		Last Modified: Wed, 19 Feb 2025 20:30:36 GMT  
		Size: 66.1 MB (66072359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e879b2d1575afe8187fa6fbce26aa78488a5fe3a4ac1d58a130f0d54e117cf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31444589b517b841d62e798596ca3d528c528d39596411384a6c368522c6aaee`

```dockerfile
```

-	Layers:
	-	`sha256:30925716528c5ba68c7e2e6f769b1bbc51899e96389bd08ee59f93123e539c91`  
		Last Modified: Wed, 19 Feb 2025 22:45:47 GMT  
		Size: 3.7 MB (3664925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e47a51b92ddef132e87283650d76562f8e9d9f368220daa9f5e6de9835201e`  
		Last Modified: Wed, 19 Feb 2025 22:45:47 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:87a424e1e93b0387f17befb329a3726e3f67a11a29405752bd53239bbbede665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114746960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a8430773f24d961c1926c3d3baf5c7fdf5bfc0af5e87380d52f6a8c3868295`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 06:00:54 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf99dc1d3b4b930b58cdb6f52408f4d75d970850d27363b7584df9dbda584f`  
		Last Modified: Wed, 19 Feb 2025 21:00:49 GMT  
		Size: 66.0 MB (65989160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ac7adf7f923a0009a11a5c31e1540837c26a9641d5c737992ae69ae924d95503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e37c5c6b7f2e735c90e508924836f514d6f1e83e1a89f2b8ebbf700ef18c21a`

```dockerfile
```

-	Layers:
	-	`sha256:e347b733a93a9f9c41c597382f35b117edf3f85f609b1610abeef104b8412a1d`  
		Last Modified: Wed, 19 Feb 2025 23:47:54 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:910a07353561e251ca96e9035106977a1d1afee738fe8be458d0628ff95c2819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119476668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e966231a9de4950bc2872b42103f767cd5b3c46cd848e31449db7e5dc8b2331`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f4f87d0546a9190cde1e0a6158e4ccce6c15ebb0f26402b88b12cb9adbcf5`  
		Last Modified: Wed, 19 Feb 2025 20:41:27 GMT  
		Size: 67.2 MB (67163811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a20490f32e86511a02c5408ac799ad155c705b80717cb35ed95b5ecb2aef2222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7030e07c310f85e57027e8385bf310bc9af26bba26105b78a8012e433724f46`

```dockerfile
```

-	Layers:
	-	`sha256:d7f452358498440a2b5205bae6b63fc732ef81af827ca147c076d6077bc409d9`  
		Last Modified: Wed, 19 Feb 2025 23:47:56 GMT  
		Size: 3.7 MB (3712668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121c9ebcfcd54a99905d20c5ef86405adafdcf941733f83ac1490e2013129400`  
		Last Modified: Wed, 19 Feb 2025 23:47:56 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:0af3d26740c07b332b5c9a3710a5a16c9df5ab2d1271b63eb4b1e973aa5e2bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112958097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b44e0ae9e875781897ccd2cdf8a290b624c9ab8b9c607561ac59bfc6936b42c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 18 Feb 2025 05:32:52 GMT
ENV OTP_VERSION=27.2.3 REBAR3_VERSION=3.24.0
# Tue, 18 Feb 2025 05:32:52 GMT
LABEL org.opencontainers.image.version=27.2.3
# Tue, 18 Feb 2025 05:32:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="328e65e7434b4d4bca4360806f2261046134c3e0ff03682d21f117fa19fe4b89" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 05:32:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4801b60b692e8b33b226123768469e544524a2f35ea17527ae5b8b18a5d6ae0`  
		Last Modified: Wed, 19 Feb 2025 20:36:01 GMT  
		Size: 65.8 MB (65826605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a9af0d88956a73a7d0061bc8dbc261e80b1e996d14d4557617be1489d766c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354779c0c4eefccf81da202624b791e8d4885cfde58635d1008b036938e0801f`

```dockerfile
```

-	Layers:
	-	`sha256:8aeb602f318f05c92799a64fafa840451f45a76901dcb8e1df7658b8824be15e`  
		Last Modified: Wed, 19 Feb 2025 23:47:58 GMT  
		Size: 3.7 MB (3708042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfacfd96f96fb9936abc4949b3ca6b83b272306ce7a3a75aa1e2d83ca83c1a52`  
		Last Modified: Wed, 19 Feb 2025 23:47:58 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
