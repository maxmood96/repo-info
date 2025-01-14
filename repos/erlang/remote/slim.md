## `erlang:slim`

```console
$ docker pull erlang@sha256:4d44fc2099c111bca7f62f21d5cc964aaa3d04b29c2148d2f192ab3f95f57e09
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
$ docker pull erlang@sha256:ff54e448e2d6a295dd44811c4ab320f428155ded835c6b64ed0246d38086d904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124397295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7790b2f7675000398d89f5826fff63fed8ae53ef4fd925d07907b6d300d2657b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c73f9145c825d37aed55463076de0ece873c038222c5d525eece5a062cae69c`  
		Last Modified: Tue, 14 Jan 2025 02:41:07 GMT  
		Size: 75.9 MB (75917333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:487f4e60088e34164f4b370a6f781b4105184882923f4db263ff4cf9cc4faa7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3df5f1bb1a3b2fdbfa51e94eee0855f757f6c8d7e1c8f975e944bd32627a26e`

```dockerfile
```

-	Layers:
	-	`sha256:411c36943539f5dbe6ce695780fca9bd7cc846d67425da98c7d40d4b35937d14`  
		Last Modified: Tue, 14 Jan 2025 02:41:07 GMT  
		Size: 3.7 MB (3708288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0dc5b19bade5e7d4fe05e2816cccb459da2df73cb6b03d3cb8395c49bbfa78`  
		Last Modified: Tue, 14 Jan 2025 02:41:06 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:3be1246ce00b3eb2f4e91b93b5d83efbca3382399a3cae9883fc88c9e070d62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111454309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46dda8a0794656500c36285d70391d4cc406eb2d123c12d0f46379c951651bd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c911b6471fb7f963c2e708624d8f3fafaa89ebe020edf41d71875c17d22b5c`  
		Last Modified: Tue, 07 Jan 2025 18:46:19 GMT  
		Size: 65.4 MB (65430067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:df1429eee0ecb827ef2a38e21a94a408c667a75afc4ee0740fd3d1fa734e4d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38d6cdb185fa0e2394a130376c6469023aa0192f20e43da616f28a63c95556d`

```dockerfile
```

-	Layers:
	-	`sha256:589c6313474fc6eb5e300d28f8cdf70b6236a0b3dc5976910497c9cd36eafb0c`  
		Last Modified: Tue, 07 Jan 2025 18:46:17 GMT  
		Size: 3.7 MB (3711796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d344cf31a1e96d9cb3b1b9cbbd5dc36398ae7385eb27164c1f455ea5e4cb1bfc`  
		Last Modified: Tue, 07 Jan 2025 18:46:17 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:183d22c80959d4b79c1cf2eb2730a899daeea5536b64dc342ee796856026693f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109235056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c6a660cef51f310fd60a4ad36e301a5659d65c24307ba5cd8a5e0d954dfa73`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8abdf743ccde01e7872c065f0d41c3a465be48361d5f251b36eb6e05077504f`  
		Last Modified: Wed, 08 Jan 2025 17:55:46 GMT  
		Size: 65.0 MB (65035089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7f21e87a4f80ca8aa11c40b64037b117e925f5c1fac3d02ae299080b2aebfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c959ad2a13f8a505d1fbb087f13a4a69897afddc0704d4a449975d31569fb`

```dockerfile
```

-	Layers:
	-	`sha256:1568a1dc8d66266ba7bc6ad1db1edaaf5804a51e037d5cd2082100e6b7655575`  
		Last Modified: Wed, 08 Jan 2025 17:55:44 GMT  
		Size: 3.7 MB (3710529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67da4b791c1be14473943bceefb1012b0ee5dce466d67f240bb858922d06d2a`  
		Last Modified: Wed, 08 Jan 2025 17:55:43 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:a5c6f924149abbb47bd190dc7776143ce0753fef408db72c5318511e14eab51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121977913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fd9aff163c2b02e7c616d82a15433a3a9bd2e78e738f67e0d54171c565d76d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dc9b837b721381d6b7539077e6d53e092e85f7115e7cd7b362cd87ff812520`  
		Last Modified: Tue, 07 Jan 2025 19:17:27 GMT  
		Size: 73.7 MB (73652429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0f4c423380e6a0732b444fb41604f4281cdf68eedceeeb6cb93bea28fb1381bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0927ec9f09c21a2648800d0027f4c3c8d14ef1788c8a6f45b40318d2b74e12b`

```dockerfile
```

-	Layers:
	-	`sha256:b89df21774e88650df7ceb118d35a87b2dd96ddf242d9d30905a82b40453021b`  
		Last Modified: Tue, 07 Jan 2025 19:17:24 GMT  
		Size: 3.7 MB (3708561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d054c994f34a92ff148506b40aaae1cfccccc048aea8673aa9082a7eec1f44`  
		Last Modified: Tue, 07 Jan 2025 19:17:24 GMT  
		Size: 14.0 KB (14003 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:20c028807dc24762224768348f66727943e834d8b4fbcd4479d1a9bae2bf1054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115532276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf45c4384de60028e04b05d89469d66e2fbf2a41016e2e67932c3e0067c6c28`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849c7106870c35b9439e54ef471e7d6092bbda800274c34fa5c618b7e62f4c5f`  
		Last Modified: Tue, 14 Jan 2025 02:24:43 GMT  
		Size: 66.1 MB (66074531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a00a689c4130f082a817063448febd8a11f18c74554f842ecd281807b93f95ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357cb0b0fc35a249c6b4aea1b9d5ac9a5aa3f6820bc77b43a64e03cf0560674`

```dockerfile
```

-	Layers:
	-	`sha256:13cd79ad4eed8544d3514dce42a049bdef573b25a0385bb0f81ac2aa6dfe9685`  
		Last Modified: Tue, 14 Jan 2025 02:24:42 GMT  
		Size: 3.7 MB (3705403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfc1223fc824e2beeb004cdd8a1a0d1b448dfd4971695c1d1bdd611b40c890c`  
		Last Modified: Tue, 14 Jan 2025 02:24:42 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:6b7b525c068bf7fc4b0990035626354056343adb0206fa8f280fc68dd935f0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114768667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347baca6479a8a249b805e663ff6c3142e4f80b8c2febe5ec9a13c188ae7b646`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0947d82d56cf271b358e819cceae9570b7afaa11bab9342a7ca3038b292e34b`  
		Last Modified: Tue, 07 Jan 2025 19:31:42 GMT  
		Size: 66.0 MB (65997023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9c5b45374f0f1c71eb2b6a5e696373f642e89aad5e33d5e37fafde0448c71e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c19d7911248bf3167495c0c8cace1cf6e6115a5e541fba851366ba68005509`

```dockerfile
```

-	Layers:
	-	`sha256:d4e203eb0f8e0b56b476f3800c50feab4ca0227fa8c016445a7139de5c711c27`  
		Last Modified: Tue, 07 Jan 2025 19:31:36 GMT  
		Size: 13.7 KB (13748 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:49060f1126be365fa8d52eca73017ecbb649b785c7f0a0eacfd5fa0cee15597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119494086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa80e3e45fff52d7163c5d61e9086cd3ee597fc2271e46fa83dea06f5d8c347`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517083a2b7b54616d35f515ce210520edbb48ae0c87b8fddff71beeb99cb0661`  
		Last Modified: Tue, 07 Jan 2025 18:47:12 GMT  
		Size: 67.2 MB (67166011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4a03642cf1c5732032d02af631b5aab4fdd1f8403b35b8d9e26feb3f5c1657da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf3ff5fc9bf1b92b98909a86ddea81985ab8ca9579ac12182c81c444110f7bd`

```dockerfile
```

-	Layers:
	-	`sha256:88de2ca9cc2f21f5794ef670ccc7b174ca41f5f5afe0710052edbe777e99af79`  
		Last Modified: Tue, 07 Jan 2025 18:47:10 GMT  
		Size: 3.7 MB (3712634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8de1f9ca57ed29eb5d6e1473915d17552e8bc12940e8084aed8e1a062b8923`  
		Last Modified: Tue, 07 Jan 2025 18:47:10 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:b6d7c6f4a2ae251cf5fd59a729e1e0684d30aa7d0373d677c6e9d7bf085678ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112976025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288844603148d1862c6854d768690c6d4a7a3bf62092f1aed258ca3c87c16458`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=27.2 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=27.2
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0727cf869622544a2434a104109b31f5fadb8dc6b532287aea182fab95922ea8" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed90c05cfb8b4ec8ff8e6b5159229080143e6e8445c82e3e6c6a63daa0aca26`  
		Last Modified: Tue, 07 Jan 2025 19:58:37 GMT  
		Size: 65.8 MB (65826400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c5c02a989a9999fd1c8d21fb29693523deb9264dd9c9fce801f09a46a1290a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65de94b40124f91413cf1e5fbf27a5fba79fdff78b680790fa595322dbedc09c`

```dockerfile
```

-	Layers:
	-	`sha256:d6ea8c7295500cbb7039876e8037dd5c334e8d095a036d505655db3cc168843b`  
		Last Modified: Tue, 07 Jan 2025 19:58:35 GMT  
		Size: 3.7 MB (3708008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8affa19dcdb8db21760c2636dd9f1ec28891c49fa8bd945eb56316ef044690`  
		Last Modified: Tue, 07 Jan 2025 19:58:35 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json
