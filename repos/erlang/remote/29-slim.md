## `erlang:29-slim`

```console
$ docker pull erlang@sha256:7e9c1cdfe8b14b2ea98534587a8e4e180e7d226a9b45fda12c274a55793b2e97
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
$ docker pull erlang@sha256:c06685c3c7d2865bdb39851b54af07038915d22c0fa07011e8d6b70d8ad6ee4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129482227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea9a0654ab19139b89adfea00c7d39c73d964291a7fc61be7d2778a4876e62a`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:14 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 01:42:14 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 01:42:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b251e325d5add878cff1bc9651c5abe54660f5b41b5512618b4e9fbe07d15f33`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 80.2 MB (80180125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d5789b4f0ff9a1cd33cf797ec3c5c2c5038f74292e1298e810dc1ae03a03cacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3bf0de6f08de31867974e68a4b38700cba3e2d154ea52b68d56299c8380a7e`

```dockerfile
```

-	Layers:
	-	`sha256:34eb84f7b6ca40efc5667fb611cf994c86f8d60d071f253082eab24d354fac8b`  
		Last Modified: Wed, 22 Apr 2026 01:42:27 GMT  
		Size: 3.3 MB (3283468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960e5034130213b3b5a1336e18690ba1c0cb7715e003a96e4e373a92a408842b`  
		Last Modified: Wed, 22 Apr 2026 01:42:27 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:68e1a097e011966376d1664e275f062e47b2f96e50da426e929f3cc4dd769e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117817839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0033b6a512768972d6b5ebc77e998f1c849e5c5658d92e340c2249851d6a56cf`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 02:19:49 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:19:49 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695a4a5dcc6a54bdd606161aec3ff5b68543b60642d5175b3fbf0d669f59c101`  
		Last Modified: Wed, 22 Apr 2026 02:20:03 GMT  
		Size: 70.4 MB (70351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:df1d8a79befefbe4d96d97b2f986558323c5602c7df96f1a9f89d710414a8be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c184ba24bf1e9f32fcce4da7d4a03f1eac838b3341f2dff610aa9d53645d609`

```dockerfile
```

-	Layers:
	-	`sha256:2a13c8c39533f85d9fe4faa656dcfe379bb2352d80f91c372d8e595b9a4e3d05`  
		Last Modified: Wed, 22 Apr 2026 02:20:01 GMT  
		Size: 3.3 MB (3286435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5666eaeeeaaab30e9954ae622b8c0b812e8d5cc84408bb849a3affde5d622bb`  
		Last Modified: Wed, 22 Apr 2026 02:20:01 GMT  
		Size: 14.3 KB (14272 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:3ddd3feaf06c28f0219c8fb4261ecc2ebecf7a60e2bc7cb68193a0be39cc3b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115663706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3652c8692981da5f879da9919b85c2be4177388e19da0ff25ffe9f429e7ff5d0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:27:00 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 02:27:00 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 02:27:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:27:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29ba3cc452b5da7654722876a0de4809dde8639be70b96d312c029c43ef1f9c`  
		Last Modified: Wed, 22 Apr 2026 02:27:15 GMT  
		Size: 69.9 MB (69925513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:452247fee15e40b5b1f293a12e830bdeab9ba25d6b5d6b5f9310c6bb9f082391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cabd50153738f4fcdef7611e4970ba594f3a8c32b0eb9b9f82d8f07d691652`

```dockerfile
```

-	Layers:
	-	`sha256:23a2a9a36599339900e13145f7d8e990e57daea6223431a46800105b7e910cb1`  
		Last Modified: Wed, 22 Apr 2026 02:27:13 GMT  
		Size: 3.3 MB (3284884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d07949259dd10bb7b8d299dd923524f518199a0ce741b708a9edabef958dba3`  
		Last Modified: Wed, 22 Apr 2026 02:27:13 GMT  
		Size: 14.3 KB (14273 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8c20c90d7f344239f516fa23df980df89706ec49055a11c808b8f1acf03f8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128324942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff7071e00a93c5b7ed34fe98c74359aae3d5ba972960e746c45b27154b8aaed`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Fri, 08 May 2026 19:45:15 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Fri, 08 May 2026 19:45:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b0299d9a494b632402b03090e872f936f6a3b5c75ccaeb213f904983ae39a2`  
		Last Modified: Fri, 08 May 2026 19:45:31 GMT  
		Size: 78.7 MB (78655497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7e1751d1795c22b8be219b177e28f5c43a602c366786c14659383313d268c20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873d7b73eeef1e2aa0e396cb6f84817515ef4a0c4a96e5558377f3e19eec922c`

```dockerfile
```

-	Layers:
	-	`sha256:31ce7edfc8bac4459aeee64251daa03d05a8d0c3e3fe27ef55bde6e9974828f1`  
		Last Modified: Fri, 08 May 2026 19:45:29 GMT  
		Size: 3.3 MB (3284991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9edd6d74c863a6e99f93997daa0f7cf9e7eca09ad504121176626d90c97e2384`  
		Last Modified: Fri, 08 May 2026 19:45:29 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:d06a57d5dc244e521c3c2d6d1664aec985cc4f0096d1c13ecb4c4ad604bec1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121146189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7eac383c6fecc7889e7b5cb1e3178751050cc086f8082b20417e8084f76a18`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:47 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 01:44:47 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 01:44:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b764074c04978ce74462f2622d683693b010e185ad32ab4018f9fc99683bf`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 70.3 MB (70320832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:699108d03ee3bf05829359ebad4f1bb89cc1756e2cda0257835d0bc8efef83f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740eacd690e486cd35933be08bf7e658868a058c91e6df7d7beae897fea8d353`

```dockerfile
```

-	Layers:
	-	`sha256:9f958ff75aab2aa0647f497b4b8cb1e9286bf38379eb055350ab7405ddf2a910`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 3.3 MB (3280643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f182aee446c7cb6b033ea35c618fdad9e262a1ccc63d4e7381f9f9cd4d6f4aa1`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:e8cd57d72cac02cf590466520229e3ff5b7128c1eb23286ccc6abdbed2bcc174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124416982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643d25a210d2ab579b3205b4ceeb0106b7a8fb4f9325a4bd1726b59b11cfb139`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:44:59 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 03:44:59 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 03:44:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:44:59 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98edb918e12b4c7c3bb96fb8297f7eb502a9a677e4ff126d093c289c80ea47ee`  
		Last Modified: Wed, 22 Apr 2026 03:45:27 GMT  
		Size: 71.3 MB (71293998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d4fe0282e4aa354f51c1b9cf1839409494d9bc3bff637ae5d85030e155d44e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e248409d4d2fe7094079a29e256264b80c4cefc1b4121477e84a38bc279566`

```dockerfile
```

-	Layers:
	-	`sha256:554b8efbd67b2b57a047e4430722825ce310b1d5df4f33b1455c950a99153c40`  
		Last Modified: Wed, 22 Apr 2026 03:45:24 GMT  
		Size: 3.3 MB (3287053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fabe1a5b3b67f334eb7b682c7a7a9324886cf6ee7fd4dafd0aaf76172dbc0e`  
		Last Modified: Wed, 22 Apr 2026 03:45:24 GMT  
		Size: 14.2 KB (14238 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:f6932215490e83fe3353ecec2813f0c246e1c68902af2ebbbf145017492d8e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120558589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea39b617428e13c1bbf64daab5a192e8bc59e32cabaffc0a070c17707a836e64`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:36:27 GMT
ENV OTP_VERSION=29.0-rc3 REBAR3_VERSION=3.26.0
# Wed, 22 Apr 2026 02:36:27 GMT
LABEL org.opencontainers.image.version=29.0-rc3
# Wed, 22 Apr 2026 02:36:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa49fb1b150a3eeeae4010e41ed5361c642c7065e6ed8cc48ff161b155997460" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d3cd441b0d3908a0db1c33e452f9336b7e3797ef0b92673c95553dc85b6671`  
		Last Modified: Wed, 22 Apr 2026 02:36:48 GMT  
		Size: 71.2 MB (71186483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1bdb4116304dacfb28a54f018e92ee0a0eb0a7e82668ff0f8fad047ee08d9793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d153aa38e54e236522b688fc6c93195aa3214da85223520c31d9b814b76fec45`

```dockerfile
```

-	Layers:
	-	`sha256:a40669314538b93b82568cc9a09c68c88809af2e938eed5607650aba2bd0bf14`  
		Last Modified: Wed, 22 Apr 2026 02:36:47 GMT  
		Size: 3.3 MB (3284909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af4b1240c7423374b3b69bdbe44baba48a0f833a417c3d9f34889d327194157`  
		Last Modified: Wed, 22 Apr 2026 02:36:46 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json
