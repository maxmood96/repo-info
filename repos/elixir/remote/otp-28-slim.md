## `elixir:otp-28-slim`

```console
$ docker pull elixir@sha256:3e623e8b77164bda7e6647bcf91c3fed5529eef3161a5d71f62cd40d3da577b0
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

### `elixir:otp-28-slim` - linux; amd64

```console
$ docker pull elixir@sha256:2a2551aac31d1176d27f2e876811d1b1f97793fd512ea44e327f6641c070a041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136849886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d9eed8f8299e3a02fd0dc31b85c4ae5376ba6e763a20f005f9f2666dec1fb9`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:09 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:09 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:09 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:50 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:12:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfa84d37eed2bdfafdde8791aab74505800af394ce2f592d08e818a5f762e1`  
		Last Modified: Thu, 11 Jun 2026 19:11:24 GMT  
		Size: 78.9 MB (78940019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409ae388b7a45843be9a34bf0e680ffc86b35015141cfd8a11fbc0ee9b7b86a7`  
		Last Modified: Thu, 11 Jun 2026 20:12:59 GMT  
		Size: 8.6 MB (8592746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:110ef012b353e93785a00f52e7106217ae0aad6070759b67306959fc8a3ec30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c383f08977179d6d8b5ea89129562671a0fde421805f1ae752d795fa84e77`

```dockerfile
```

-	Layers:
	-	`sha256:bcbe0249d054ede9e4e85a2100bb6d2a6a177f16888411a67a37e6a9e42a67cc`  
		Last Modified: Thu, 11 Jun 2026 20:12:59 GMT  
		Size: 3.3 MB (3290790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36cb0be87c99e8e786e1d7db60964e749766b40a0c9d484c823ce72b2a46d58`  
		Last Modified: Thu, 11 Jun 2026 20:12:59 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:4624bbea20c503072223598a4134228eca25a134400202c47fdf70bac088e029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123346034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef9473d8162ff0ce75447fae46cc342ba6253d03653b2008b7afe528d092f7f`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:14:03 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:14:03 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:14:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:14:03 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:13:29 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:13:29 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:13:29 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad872e7b9d28fe870a66c7a8d5729e3454a26983ad61385572d1ca3d2983d6`  
		Last Modified: Thu, 11 Jun 2026 19:14:17 GMT  
		Size: 69.0 MB (69005238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52948dd36a9ae354884cd164ca1a4b5c37680f1b25b558c2075bba65e0e8e904`  
		Last Modified: Thu, 11 Jun 2026 20:13:39 GMT  
		Size: 8.6 MB (8592155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f6594a167080c9fd5870817d012fac55a85b87c8ad3c17c510c9ec4caf3b6243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3302016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002472b6dc8455ea4f8db1ca65d83db68a57e2b3c222a67ad28eca65aedc5847`

```dockerfile
```

-	Layers:
	-	`sha256:459069b92ea05db5e2cf2689329a025c2987d5703f100422ef1fe13ae235f540`  
		Last Modified: Thu, 11 Jun 2026 20:13:38 GMT  
		Size: 3.3 MB (3292198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81bacd22dbaf9b62e6f9102a53bdbdd3d93666d5d12866084fce08b190df717`  
		Last Modified: Thu, 11 Jun 2026 20:13:38 GMT  
		Size: 9.8 KB (9818 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:c5671e5789f230be90afb72f6b41aa2ec120e87ad3519e52a60a01c34a45f83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135761038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1934671da0f50e555dea87afd062a8cae57099568b202e5a95780e3ff7632471`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:19 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:19 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:19 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:12:33 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:12:33 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:12:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae6654e3fd28cf88b0a7df04af26dacb207377b9a6db28f804db06809e7c8dc`  
		Last Modified: Thu, 11 Jun 2026 19:11:35 GMT  
		Size: 77.5 MB (77490178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31fd9029a5b65d7a05915aaf0bd1e9f7d0729cf0bd604d7c1d7b477e16859e`  
		Last Modified: Thu, 11 Jun 2026 20:12:43 GMT  
		Size: 8.6 MB (8592691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0b8692b5dc6660ac6573292f3257a5869711d9041b26bf085651cad0f2248931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e27282c49e7982bd8b897fc6d2e4941e2c8dc2db10643b3b9adefb61369534d`

```dockerfile
```

-	Layers:
	-	`sha256:dd97842d559e38bdf7d48d65110da8933f16ec053abaa0ebf342ae30f4eb115b`  
		Last Modified: Thu, 11 Jun 2026 20:12:43 GMT  
		Size: 3.3 MB (3291664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1af55936d2004ac7407753bdf847a790c497904483b723f0920649e4be4802`  
		Last Modified: Thu, 11 Jun 2026 20:12:42 GMT  
		Size: 9.8 KB (9837 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; 386

```console
$ docker pull elixir@sha256:d710cf4495c41cb7e9b969fa599a88e34c6830e726d69fcb1c5c9a5c3718ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128847718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba79b7231c727f366a7896e2daaa63dc0ccd6fc47e0e545d408931e735dc066`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:13 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:11:13 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:11:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:13 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:13:04 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:13:04 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:13:04 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3893ff25cb988ef286c608bc016ed211cb5550a7a2ac39bd621fcf5e2b9f59`  
		Last Modified: Thu, 11 Jun 2026 19:11:26 GMT  
		Size: 69.4 MB (69419953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7768f6966310a050423e99f9c590cf07ce5c8760666e8fb32996afc0e4efedc`  
		Last Modified: Thu, 11 Jun 2026 20:13:14 GMT  
		Size: 8.6 MB (8592202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:54c6546dd9bb725edf3ddd842653a57b6a37d3b5faf7dfecc4b1663edc64a145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24a55f7f160ca851ad83bcb0b0eb49ea559a816ed217123954a8f6532d9e6d`

```dockerfile
```

-	Layers:
	-	`sha256:8bf6982f9e3d168314e29579ded0ac4fee2a6ed0c41c781dd5215512d267bb97`  
		Last Modified: Thu, 11 Jun 2026 20:13:14 GMT  
		Size: 3.3 MB (3287970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0964cf0cc4c5c0bd9bc626e4134730cf5d988f251116fcb77836de69e33db6d0`  
		Last Modified: Thu, 11 Jun 2026 20:13:13 GMT  
		Size: 9.7 KB (9718 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:13fd1367fcddf3a719a52e47122254d06050a7f2692377e5d3df44c6c8cde90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132114718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264371640011e0a4c712585ae5df93992533fc0ae35ded58122cdac2feee8367`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 21:06:31 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 21:06:31 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 21:06:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 21:06:31 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 21:34:10 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 21:34:10 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 21:34:10 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f98e634efbc617676f3d6e8af6ab5c34d107236958daba326d7e32b72bcf608`  
		Last Modified: Thu, 11 Jun 2026 21:06:56 GMT  
		Size: 70.4 MB (70383960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fdd1aebf236bfd87b23d1c47602dbb0ab33bbd2d298c758cbb9bf92bfd3c75`  
		Last Modified: Thu, 11 Jun 2026 21:34:24 GMT  
		Size: 8.6 MB (8592819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:75f358d443d70700ba14908b27fb3e560df42e0ac7a9c5e77346b899765af041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3304153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c174a69d037812f21fc6b9caeb5dce836b08309d6e3b341b609a27addb5bfa8`

```dockerfile
```

-	Layers:
	-	`sha256:d56512a1719d8d9bd7c303e433edcd2ac97faf425ad29b03974bf4781ec88870`  
		Last Modified: Thu, 11 Jun 2026 21:34:24 GMT  
		Size: 3.3 MB (3294369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97f5aff311741d669e67377241a60ce2311200276ba141f9f942d307f25b28b`  
		Last Modified: Thu, 11 Jun 2026 21:34:24 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-28-slim` - linux; s390x

```console
$ docker pull elixir@sha256:3243d8b3c3cc9b06937d76da81fa70ecb1a5e25ec4d5c667e4de683e15f4d78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128244203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61e1c9b088090ab913a329b15499a322ae2e8a816072ade7b1adc56218ee018`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:15:51 GMT
ENV OTP_VERSION=28.5.0.2 REBAR3_VERSION=3.26.0
# Thu, 11 Jun 2026 19:15:51 GMT
LABEL org.opencontainers.image.version=28.5.0.2
# Thu, 11 Jun 2026 19:15:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="70d000de601c1cf695b551bab5209226555363ad3cb810639810a3fc6c5306eb" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:15:51 GMT
CMD ["erl"]
# Thu, 11 Jun 2026 20:15:35 GMT
ENV ELIXIR_VERSION=v1.20.1 LANG=C.UTF-8
# Thu, 11 Jun 2026 20:15:35 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="baed8756da722c1b8d71613655c7223ab952051bc391a965cd79e320a93aaf77" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:15:35 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318eae81240e42ce0140d36ab50721b7f50352b805fbaa24782daf77d3ac17f7`  
		Last Modified: Thu, 11 Jun 2026 19:16:13 GMT  
		Size: 70.3 MB (70266041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e83c42b896cf38cd58e8db0272aa059a4c1c4f789e90cc57f23c34ee6263e5`  
		Last Modified: Thu, 11 Jun 2026 20:15:49 GMT  
		Size: 8.6 MB (8592265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-28-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:9e1283b02c1fe457da6583e71514fc6a15eac1c7838681c3a794798c88f0e208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b5fc98919674fb73ccf1bf9b1f617653850bfc8e5aed5fccfc0e32656678d9`

```dockerfile
```

-	Layers:
	-	`sha256:87c7d47a2f6ae0d20c18b4f1068422685888fdac9aed5ba7dd43dc1c9d73fbed`  
		Last Modified: Thu, 11 Jun 2026 20:15:49 GMT  
		Size: 3.3 MB (3292231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea99c5710bcf463037a46889cd5bca09b975e06bd0f9cd3c052ab45fe2ce505`  
		Last Modified: Thu, 11 Jun 2026 20:15:49 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json
