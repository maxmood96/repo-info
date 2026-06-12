## `elixir:otp-29-slim`

```console
$ docker pull elixir@sha256:39bfc5bdaaf135b9c0c4f46500081883b0831e2471987fb69a897bcf8439b49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `elixir:otp-29-slim` - linux; amd64

```console
$ docker pull elixir@sha256:ca21f381bee3b5f7e510f555e1e92eed7212d5fe1ac680a83814cd26d5b6cfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138188128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f05d48181400bccd77f8d1ff1a06f5c0b704f224f4a852d91f4873a59b2e300`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:19 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:19 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:19 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:42 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:42 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:12:42 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16980830617a3a7d5f9c6a100dd7f8f33166a7278d8f2d819fa056f496e419a`  
		Last Modified: Thu, 11 Jun 2026 19:11:35 GMT  
		Size: 80.3 MB (80279254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cbaa2205817c302649cdda2f4f2c35d9b53a130eb899c27f235e77a3490207`  
		Last Modified: Thu, 11 Jun 2026 20:12:51 GMT  
		Size: 8.6 MB (8591753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e28a978fbf0197a2d7a62663f3ca376764ee5daac75bff36e601f2afe86deebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae706a533361be55912708ba406e3ca3f8d15916da081f6a40a8cd5f2233e67`

```dockerfile
```

-	Layers:
	-	`sha256:f4f91007a93d76fcc2e8f8ba35e6da181f14751b5a96e1361238f977fd410377`  
		Last Modified: Thu, 11 Jun 2026 20:12:51 GMT  
		Size: 3.3 MB (3291506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3098c08383079b58024f2a85055e39864859150fa9e2270caba46c9c5d003dc9`  
		Last Modified: Thu, 11 Jun 2026 20:12:50 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:47c92698f4828515d6069cc15738d4a9bc644977c4fecf31ea46eac7ff4655c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124354856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691b2a73d56e528c123db10193e8a08d47f76081aa00b4a6e1ce712211cc1206`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:30 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:30 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:30 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:14:03 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:14:03 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:14:03 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2018362f801edba824698b5f2648a3a189db020f84426a048942ee5b3385313`  
		Last Modified: Thu, 11 Jun 2026 19:11:45 GMT  
		Size: 70.0 MB (70015198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbcd735aff6dd3caf69337b793f614c315358f6cec9ab97aabc248a0d391a8a`  
		Last Modified: Thu, 11 Jun 2026 20:14:12 GMT  
		Size: 8.6 MB (8591017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e57641468bd002ad81ce69e8aa56c32752c86153476b8156e91aa5a98aeac940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05564de4ac18d71dc983b57c370402987706212a55cd7b2fde76a95f878eaaca`

```dockerfile
```

-	Layers:
	-	`sha256:7546cc5a5610eec2c9bb927b77fc1be5b6e52dddfe27b3d9a60c987c0e271e96`  
		Last Modified: Thu, 11 Jun 2026 20:14:12 GMT  
		Size: 3.3 MB (3292938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e917aca25577e8773f4142e6f3b80cc2d8d59ef03cefb06713008d0e534edad`  
		Last Modified: Thu, 11 Jun 2026 20:14:12 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:4a766c76d8c0d14e129ff2cd300d89136b06bf5490b99f593b476a0a013216f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137020096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1bc7358395169181cf45e7128e3b242e4451831b349598623bfff060b0a9b4`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:16 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:16 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:16 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:11:59 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:11:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:11:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805b2e1ac43460a7157f342a003113a55b12cf9403058e744604fd612c9175f`  
		Last Modified: Thu, 11 Jun 2026 19:11:31 GMT  
		Size: 78.8 MB (78750289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9de011f40d53539b07554539d411aa3be1362ba4d5d9e75b8bc3cb2e1ff5ee`  
		Last Modified: Thu, 11 Jun 2026 20:12:08 GMT  
		Size: 8.6 MB (8591638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:36ee81a71a046eb570b913dab2c170cb36df4b5ee149a53531a38320b1011822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776f703c1daeab479812d640466677abe187a37468db3085aa246f9f9dd71c49`

```dockerfile
```

-	Layers:
	-	`sha256:629d022dce79012d52713ac375486d3e2ac2578276e99e43b15e706c92b7c40c`  
		Last Modified: Thu, 11 Jun 2026 20:12:09 GMT  
		Size: 3.3 MB (3292416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9fff616a5c1016fc8b98f451df7a1ac8d3c793b08dbedd153a2ae0933227b1`  
		Last Modified: Thu, 11 Jun 2026 20:12:08 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; 386

```console
$ docker pull elixir@sha256:f918b4894ce6a93fe4e64b6d7225fbba7326e74bdab823f67b5f9d935d8ea4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129848059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef70c0a21011b68662b32978091679d66c5ea88569b205ef5706f215ac708fe9`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:29 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:29 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:29 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:56 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:56 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:12:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b7d40c6a7baae68b40b60d035cfcabf854955113d0833aea340674a975e7b`  
		Last Modified: Thu, 11 Jun 2026 19:11:43 GMT  
		Size: 70.4 MB (70421323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e01a3c81c2b04879ec10bf03acf4b48d588a27b8473ff410d65e412cc99628c`  
		Last Modified: Thu, 11 Jun 2026 20:13:05 GMT  
		Size: 8.6 MB (8591173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c316d6fea7921651b9b6981b8703b643d70e90a9711d73b294460e1fab169f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ffb711f4caf96d5842119ab3cdf88aaa3665b155ff9efda0c983ee4849f602`

```dockerfile
```

-	Layers:
	-	`sha256:6289e640a4e7e65e978a5147464bb9039c4c67709d9c3096c2d7f28a55107540`  
		Last Modified: Thu, 11 Jun 2026 20:13:04 GMT  
		Size: 3.3 MB (3288671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75aa2c18d9ad4299613ee00d8b995f7a45e05f7fee7c2e38698f842d07cd5d3a`  
		Last Modified: Thu, 11 Jun 2026 20:13:04 GMT  
		Size: 10.6 KB (10594 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:c973e83e99d620779202036dd631ae235ed0bd029be44a242e023f4ee81bc803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133122438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e4b5ac0a98049dcf4901db81680e3658e4d7b9934cdd515b86764ea9f87cce`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 20:59:05 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 20:59:05 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 20:59:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:59:05 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 21:28:23 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 21:28:23 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 21:28:23 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a3dc5c0ec6a6387fce347d9f80e8f1f7c7ced0af1d02ffa21c4337cb6eb042`  
		Last Modified: Thu, 11 Jun 2026 20:59:31 GMT  
		Size: 71.4 MB (71392699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c6d545f87c1875e3fd2c6ec0f2f24a603c02afbdea57c6c2ea093b23d71530`  
		Last Modified: Thu, 11 Jun 2026 21:28:46 GMT  
		Size: 8.6 MB (8591800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:d29762ab1a2e9bbc1824c446809c4396ae5085256079958d47d47ee89fca3ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a9d7d9052b39d10ab81a3b117dcdb08ef1bdb1401d37da8a28899644fc043`

```dockerfile
```

-	Layers:
	-	`sha256:182e09aa28f9f8445a41b91b6bb538f45689fd094fe533df0aa113d088e2aefe`  
		Last Modified: Thu, 11 Jun 2026 21:28:46 GMT  
		Size: 3.3 MB (3295103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f571a74588080c2415e4e8d47c5b3d0dc98025a5d5112377c6ae1e5275973c1`  
		Last Modified: Thu, 11 Jun 2026 21:28:45 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-29-slim` - linux; s390x

```console
$ docker pull elixir@sha256:2d371339444eae6ccb95fb7edc1707037efb4f922bebe5ffa32cbf69567de2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129247239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a422241504c1224d21bda7985407a3e9af0ed7a852c5d72485874b2e4c5b15`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:12:45 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:12:45 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:12:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:12:45 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:03 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:03 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:12:03 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265009f51f3f73a7540ca4d2367a2844450f2e4b56e9d84aab8ba1710d156a3d`  
		Last Modified: Thu, 11 Jun 2026 19:13:04 GMT  
		Size: 71.3 MB (71270133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa66137e95ee616c2a9f3c1808179864e1ed06308ccc8d9dc7e3289b36562e6`  
		Last Modified: Thu, 11 Jun 2026 20:12:15 GMT  
		Size: 8.6 MB (8591209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-29-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:4e92d96bd5b0ff7b8881bfcf5259187140454ac6cbd28634c628be359c3efc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6287709c09035a44aa8526540459af70c22bc6297bc8069d98876dc6e63cfb7f`

```dockerfile
```

-	Layers:
	-	`sha256:042236d8517dd84a654c9c9af7a4bcc9bf8107b4411fa1f9ea42cd963b7bdf17`  
		Last Modified: Thu, 11 Jun 2026 20:12:15 GMT  
		Size: 3.3 MB (3292947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607f0baca0233f584bce9a8209822782a691a34db1db1ec6d5e665c1ec9b2435`  
		Last Modified: Thu, 11 Jun 2026 20:12:15 GMT  
		Size: 10.6 KB (10636 bytes)  
		MIME: application/vnd.in-toto+json
