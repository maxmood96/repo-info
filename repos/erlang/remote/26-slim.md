## `erlang:26-slim`

```console
$ docker pull erlang@sha256:b6796d3b3b73c20af42e9a7f14c8972a780814c60f497bb0a2c868d98981b7a6
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
$ docker pull erlang@sha256:b7d1cc5e4963f76e0cc04c2306d68114ddcd10b84a83fe2ec2c0459ace359ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118908760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855b634392dca236c4909bee3197c09d1a5bc92d904d284d262da6abdd66c3b1`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:20:21 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 05:20:21 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 05:20:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:20:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb8e00b2bc34ba8fca0c84b055a4b131e85033e30aea6a33fd381cb03ed121a`  
		Last Modified: Tue, 18 Nov 2025 05:20:53 GMT  
		Size: 70.4 MB (70427999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2dd0ef9bfa578e6442ef5eb74a1882cbeb8e244331a2467ece599c546437396f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1aebcfa8f6e0da7e38119fe6b20555d7e85f7ae667d0b60022a5bd841a67c3`

```dockerfile
```

-	Layers:
	-	`sha256:f0084f741956a7c8bcf6dce80b1ffe23b38369a06a67f6eb8571986e176647c0`  
		Last Modified: Tue, 18 Nov 2025 08:47:46 GMT  
		Size: 3.8 MB (3825336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80abf5332e922ddc3cab3a4167ce6753d259c7b26a2f42a4f2a32ba8bda6058`  
		Last Modified: Tue, 18 Nov 2025 08:47:47 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:cdbc712e5e03ea4fa63d77b7a02c54bc8d00ad3503e9ffe05a466f646c6a1e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106555481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56073a17f2a444506eb82350d6fa19f6ff2d0c4a0693c45f9531fb50185cba6c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:35:17 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:35:17 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 03:35:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:35:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce224ccb8e43f0e18bdcb12e44c00fa3d4a75b6b26943c3f02dee1b118005c`  
		Last Modified: Tue, 18 Nov 2025 03:35:40 GMT  
		Size: 60.5 MB (60539650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9804bc9cd4274c1313c55f79ded09cd283d6ef7fd755d5d6dd9b25f544151764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e39fb9a948e2248e679ed543b2dfa7064738e3d57cf29f973682c91a80c4991`

```dockerfile
```

-	Layers:
	-	`sha256:bfc274d2b97e1438c407a2934fa79ba7eef6c38974c553da0f17cb5c83e7e49a`  
		Last Modified: Tue, 18 Nov 2025 05:48:08 GMT  
		Size: 3.8 MB (3829144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca49da22c70d2e2dfd3f16287488a2a10025be78ae40de758db5668551c7a30`  
		Last Modified: Tue, 18 Nov 2025 05:48:09 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:6b0b3e862a52e085b586e6befd1f39fc07583ee4ab9a95681e3b40d6e2b4045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104359090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dc18379f20a74f6ae31f3c35d48acb17029ed39b84ec40702d73ab860abb7a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:25:42 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:25:42 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 04:25:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:25:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3573a4b85e52edcb06922a4518ec4ca07db55d79fc1e987ca9f76fc9501108`  
		Last Modified: Tue, 18 Nov 2025 04:26:06 GMT  
		Size: 60.2 MB (60162966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6ff7f6c545e42e2fa3a0a0c0dcc93fa06dceefadd637bc8263e0db5c33b21dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd071090e0d5d9c38d578ee5cb010ff593e61f8e90ddd6b0db7846b582f21e3`

```dockerfile
```

-	Layers:
	-	`sha256:59599e1be4ce277266667ee1d69aef525c42d49fa5f2b4bf813980dd65d82a75`  
		Last Modified: Tue, 18 Nov 2025 05:48:13 GMT  
		Size: 3.8 MB (3827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25652d7c31017951e4a99f978f72afaf4f083ae251fc49595b3d04942d549bbc`  
		Last Modified: Tue, 18 Nov 2025 05:48:14 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:542ee94b964931e403584fe4b4f223cdab103bbb3ca0d1213049f1e18cf859c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116429026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e60b5850702081ba89ba92c7b9d9d17c744ec0a09c443e62b75f9f3d1f4fc5`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:44:44 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:44:44 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 03:44:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:44:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4119b3906b93c9f4f983062ee2a21d2675a770d6275eae2fb8ebb64582d975cf`  
		Last Modified: Tue, 18 Nov 2025 03:45:17 GMT  
		Size: 68.1 MB (68069888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7849f472fce243f38755e8ca71be5def3318a54d5c85509d57e70fd7e6835d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013db134eae2b6603d1528bc737c33b5daf64023e27fba087d0b79e66a6fbdca`

```dockerfile
```

-	Layers:
	-	`sha256:d61dbdeae6c6f546940d8e9bd49e4f3aab32f3e43a2375a9086c81a25a405b05`  
		Last Modified: Tue, 18 Nov 2025 05:48:18 GMT  
		Size: 3.8 MB (3825597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d005ba109a0f0349789c52d5c163924d45dde50ed069093752ed8c43ffd2aff`  
		Last Modified: Tue, 18 Nov 2025 05:48:18 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:0394c7df992961689155bfde8d94cd2e4067bc07db9c28068ff1148adc4d23f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110622239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f65859d43cf165f3438f577082830c8bfc5461c7da436d2ea9d68623b6ece`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:01:36 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 03:01:36 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 03:01:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf440d218415f0c52cb93525c0c30595ae04694343d01430a4547e5b9e8ed35`  
		Last Modified: Tue, 18 Nov 2025 03:02:03 GMT  
		Size: 61.2 MB (61155373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c840a3aea51845bdbf85f7390e4b64afd9d1e0f63e8b85fdbba32e63efccaa91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dde93ccbe2be84cf6012c9ff6f6944085901b70b74245eb973c75216c84d40`

```dockerfile
```

-	Layers:
	-	`sha256:d24b071fc837f386dbc9735a9d135c7a53e8139f80a02cf44c17d1843613ce8c`  
		Last Modified: Tue, 18 Nov 2025 05:48:23 GMT  
		Size: 3.8 MB (3822498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4488f356c992194962b0e6352eecd7993e59e9373e5977d4c47e1d1314af8f02`  
		Last Modified: Tue, 18 Nov 2025 05:48:23 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:c02c15c0d6093794c8d08a5bdbf5a17371de9cd09a9ac087f6cc3c55352f02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109896677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7789909b3b666218836f8e0804d0f6057c7c094ebb213455ded6d5535053e1d6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 14:55:26 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 14:55:26 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 14:55:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 14:55:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d99baf14d6b0074dc733efbc3b46cdfe88894e4d8dcdf3fc1def819959a0d39`  
		Last Modified: Tue, 04 Nov 2025 14:56:40 GMT  
		Size: 61.1 MB (61135395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:21a63b444096f88a206ca56149191da0877cc42a0b6827509a29c93d2502d958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12660ec275d0a3974b3b502bf9fcc7512e6f32f1b855e5f1b79f5b849fa97e6c`

```dockerfile
```

-	Layers:
	-	`sha256:c3c4fb101bf51460629fff60f2e288379ca22e0d94e210b02662e27ac4eb567e`  
		Last Modified: Tue, 04 Nov 2025 17:47:10 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:3775714f46b7c4068d746372a6aa5473232450e4ca4e994c81e7e7271f08862e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114579806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2671335bf83578611a28f0cc9e5bc96bf19dd961cc69b849f5f592b43f710d99`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:23:07 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 04:23:07 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 04:23:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:23:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f59b602b9c01ee042935d1093a73cd533d9cec81c60f47871f4c7507793909b`  
		Last Modified: Tue, 18 Nov 2025 04:23:42 GMT  
		Size: 62.3 MB (62252843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:cb6ecd4cc6ddcae5dcd87edbda9bccb994431a37202331e79faaedc2822800ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3793d2777058be63c1cbd211f8f77635d96ed13495f230aa50c008c13c30a744`

```dockerfile
```

-	Layers:
	-	`sha256:8632696c015e470a74c332992e0aebd957053fbec67ac1d261a4853e3e6b5e4b`  
		Last Modified: Tue, 18 Nov 2025 05:48:30 GMT  
		Size: 3.8 MB (3829784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c5ecbb945b19120f121cee1756fdcab10ada96399f8d287c0ba9ef9ca1960c`  
		Last Modified: Tue, 18 Nov 2025 05:48:31 GMT  
		Size: 13.6 KB (13606 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:20cc6f4458d32ec80e98e5b54e2859d1ae4197f642bcc4a4a0914746446c0217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108098349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2eba465451343280a55f27f5b4d7c65c4fa1e5856cc0188dd61b1a4e870e58`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 07:13:20 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:13:20 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 18 Nov 2025 07:13:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:13:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23635a1c1982c4aa510de5f4573eff1620a8b1887f043a481a69eacd4ba1f186`  
		Last Modified: Tue, 18 Nov 2025 07:13:52 GMT  
		Size: 61.0 MB (60960708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:37666fb943fe7ec1c519c724eb4c5eff5380fed04c2eaeb45941ed3a30130831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be68d88ceb3791465ec6bf70aedfe658af0bcf18de0ce3e488aeb54b97b11836`

```dockerfile
```

-	Layers:
	-	`sha256:2166642f18a36d3c84ac94a48ab14903b73d1d4a882cce2fba8f26f2a059bc27`  
		Last Modified: Tue, 18 Nov 2025 08:48:06 GMT  
		Size: 3.8 MB (3822164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecae7054cdf01cbf8ef6adc7fa3d74e9f41f4f283f4a9a1caffd1b3574cb352`  
		Last Modified: Tue, 18 Nov 2025 08:48:07 GMT  
		Size: 13.6 KB (13561 bytes)  
		MIME: application/vnd.in-toto+json
