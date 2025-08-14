## `elixir:otp-26`

```console
$ docker pull elixir@sha256:e9b3f9067c1d39ab0ccc45770b3f61db8ea929d89cfb2e5a42d104190080efc5
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

### `elixir:otp-26` - linux; amd64

```console
$ docker pull elixir@sha256:846aeaa24ae84f7bb46ab4128209eadcdb7ca32f426d4548c66a92e72b240ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.1 MB (623096739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12e09929fe21007c28a40e33f2e80053b89823b37519afc92995d3e4c942c6`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6ffe3614ab4a262aa4bc4f9759e9ec47c42ce5bb3321f0023815974344cb9b`  
		Last Modified: Tue, 12 Aug 2025 22:50:00 GMT  
		Size: 211.4 MB (211394364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da09cfa94b0e784f6aab0469f78ff975a769ad782e0f5c4247ed714c33657bd`  
		Last Modified: Tue, 12 Aug 2025 23:14:19 GMT  
		Size: 266.3 MB (266309552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5d70c5acf12ec66d54c8428a240fabf308547397cd4d7bbedd18a96022ef77`  
		Last Modified: Tue, 12 Aug 2025 23:04:09 GMT  
		Size: 194.9 KB (194926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceecb94c2b0c8882f55589643fcd412844597a7f5616907899e7303db0eea7f`  
		Last Modified: Tue, 12 Aug 2025 23:04:10 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e191e04a5832251476b394e273e99124dd73d124ca0679a5100910374855e62d`  
		Last Modified: Tue, 12 Aug 2025 23:16:36 GMT  
		Size: 7.5 MB (7462803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:6ff96394a4bc64f8b4e96a10b8db5cab50584f36aa6913704a2b8e2cc05c2162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23285822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d448f918e6b9cbe7d684eacd4872cdabff3952a40e0deb1064ecfd748bfe81`

```dockerfile
```

-	Layers:
	-	`sha256:da04c08a11f3d93a2a4d66d6379a9eeba59efa714d857aa4e1050318cfb9d68e`  
		Last Modified: Wed, 13 Aug 2025 00:49:46 GMT  
		Size: 23.3 MB (23275401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d943f30934eae029fd514dfda107661d240ab90a7ed85a9783b511395f2a203`  
		Last Modified: Wed, 13 Aug 2025 00:49:47 GMT  
		Size: 10.4 KB (10421 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm variant v7

```console
$ docker pull elixir@sha256:48ac413a06375fe87cc70021b081d43487c0f80513b591871671639d48b43f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.0 MB (545987839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5bb446ea35d82ddbcc04cb3c5dab8abeaa31ce87d92f332aa0ec886138a46d`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b123fb3b68d3192243d66f2675c945600a5ac7493f7a06af8327cd33d6e937ff`  
		Last Modified: Wed, 13 Aug 2025 13:57:25 GMT  
		Size: 175.3 MB (175309693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66deee45365d432b86ed446e37ac41ca99d451ef1f93724fbd6d5c66707b84dc`  
		Last Modified: Wed, 13 Aug 2025 19:50:29 GMT  
		Size: 236.4 MB (236405549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6874f16e1d0bdd1bff861137c0428afd60b814d69512a048122a122dea05f7`  
		Last Modified: Wed, 13 Aug 2025 17:13:36 GMT  
		Size: 195.0 KB (194957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359d6f3d9532389710e5853c7821a0874291a64fb9b61f0186ec972f865ad5d8`  
		Last Modified: Wed, 13 Aug 2025 17:13:41 GMT  
		Size: 819.7 KB (819694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53470784726c3c7fe5b74770945ab3e2d30decf5f7ec2dd5c0e451d1605f81eb`  
		Last Modified: Thu, 14 Aug 2025 04:39:43 GMT  
		Size: 7.5 MB (7462796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:de315c2a9ea4cd3168cf6768757588998ba66f3882dfaaa01d6e12bee299ff11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23098916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdeebaea8920321e4276541caa31205a214caa5b5ef32fbece774b4aae73c8fe`

```dockerfile
```

-	Layers:
	-	`sha256:cf1bfd7c1947a26fce0c2b28c69eb8a29587aedb4305e61264980b614bbd8e62`  
		Last Modified: Thu, 14 Aug 2025 06:47:25 GMT  
		Size: 23.1 MB (23088427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd505733e2be5d49c7b284d9d8550e716aec8e88196aa90c82455e0147f6845a`  
		Last Modified: Thu, 14 Aug 2025 06:47:26 GMT  
		Size: 10.5 KB (10489 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:168ee457d44784b5d6ba801b7d5a1555f8304cb7ba63957ddc884528163cafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606314253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e59baf69316a7cc661bd35e582525caf1f4ef60b58e8dc4a35e4f2624136ac6`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8325efcffd02810e02c94ef0cf141d88f021fdac3fd247613e996624eb84fb23`  
		Last Modified: Wed, 13 Aug 2025 21:52:42 GMT  
		Size: 202.9 MB (202855055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa40fbe1670630e756d5f03b6d55ed782902a9ec7044dff060245db7f0e495f`  
		Last Modified: Thu, 14 Aug 2025 01:54:15 GMT  
		Size: 258.7 MB (258702468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e855d45e94f4e95e53380afb715af959d67fcad8609fde1deb8bbe7783d500`  
		Last Modified: Thu, 14 Aug 2025 00:00:43 GMT  
		Size: 195.0 KB (194969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b7dac43eacf01b597234089570a73fb8ac3acc684ed706f804f6044a27c008`  
		Last Modified: Thu, 14 Aug 2025 00:00:43 GMT  
		Size: 819.7 KB (819691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49160d25599944f0a0d600f2d7d9d02ada87ac22c3a783dce377ef3e2e2cec6f`  
		Last Modified: Thu, 14 Aug 2025 15:04:13 GMT  
		Size: 7.5 MB (7462770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:a8230c83ac58431612286d7eba24bf63e2662d0b0c5089b0920247f2beb117e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23325378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73e2d051f226d0f94641f0af6dfa0a6881b8f1e798c8870b3db3e06f652ab2f`

```dockerfile
```

-	Layers:
	-	`sha256:66d5dcbe9ba2549b7f2d074b20b44faf9f43f614a0c4b755d396d61be526a243`  
		Last Modified: Thu, 14 Aug 2025 12:47:32 GMT  
		Size: 23.3 MB (23314866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834bc17df9f9bc66344aaadf5041cc8e2447fe005f017adebcc5676e795c0bb4`  
		Last Modified: Thu, 14 Aug 2025 12:47:34 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; 386

```console
$ docker pull elixir@sha256:d978f45ed23c2cf733744f9c9048fef58a5d581b9c32f6071a5fa968c68b6941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624190282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd827f617aded74cf640b85869d14bcf63d87ed259d1b8da53d1a9604dd4a7`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874646e2459984b117c58d731a64ebcb9d23f76cf755c68e1ddb30317e57abc0`  
		Last Modified: Tue, 12 Aug 2025 22:13:36 GMT  
		Size: 24.9 MB (24861125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c25d261fc893dbf63d447e191cad0237f37f95f01960ee9b9026b75ab3a74`  
		Last Modified: Tue, 12 Aug 2025 22:14:47 GMT  
		Size: 66.2 MB (66226107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54aecdf4dc95b87fbb1a07d66dc4c628977250de785deb309f7bfad91a7c43`  
		Last Modified: Tue, 12 Aug 2025 22:50:22 GMT  
		Size: 210.3 MB (210325520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be4896953b3bf64d9e04b4568d10d9696a9bfde8192cad381752e772f576664`  
		Last Modified: Tue, 12 Aug 2025 23:15:05 GMT  
		Size: 264.8 MB (264821940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a97dce8c5bc005652b54ed9631e58ab9450e86dbd5b415914ca2d3c321fcc`  
		Last Modified: Tue, 12 Aug 2025 23:03:38 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0882a2c7864b28feb59a9ba1f417923211ed9fbf4410968144ff7e4d004217`  
		Last Modified: Tue, 12 Aug 2025 23:03:40 GMT  
		Size: 819.7 KB (819689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0483514a8fef88fc3b396c6e21b263e288fd54f3b614685c0ed2a1c2dacdbd0d`  
		Last Modified: Tue, 12 Aug 2025 23:16:54 GMT  
		Size: 7.5 MB (7462835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:d0810cf6d62c38254dc857ab5b0b5560fc66b212a043139b5cc9311f47fe1f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23253441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c5881011ee8cb6779438abc6afcc7990ba51be88d13297a5924d495c07d072`

```dockerfile
```

-	Layers:
	-	`sha256:bf7ed3c7f747f44b7d9802b06d48bd221799420352b0a00f702a82025f1e6cac`  
		Last Modified: Wed, 13 Aug 2025 00:50:53 GMT  
		Size: 23.2 MB (23243047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d50402b2bd3f2a83856380b6cff36940c22cd77c57d3ea4f59684b2dacc5a9`  
		Last Modified: Wed, 13 Aug 2025 00:50:54 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; ppc64le

```console
$ docker pull elixir@sha256:46958e9adcc58cd6baf585b0fbb9120dbed07db89972479ac7299d6578ee246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.6 MB (631595572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9521870034c6242d70ea0b299440d9c295c53cc8f6a747844798261886b9e654`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9ab368175c07efafc97db73dcb256947b7c350124b285ef68898aa41837a0a`  
		Last Modified: Thu, 14 Aug 2025 04:19:57 GMT  
		Size: 214.4 MB (214443029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6333bf2e5711796119a92583f9574acddc27c13461058663ab7e1a3de7ec3de5`  
		Last Modified: Thu, 14 Aug 2025 08:09:16 GMT  
		Size: 260.8 MB (260831120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a63ecb0da3bde3ec0764f5385d0f60cdcaa9ab476b9662d08bb0a4c411de0e`  
		Last Modified: Thu, 14 Aug 2025 07:51:53 GMT  
		Size: 195.0 KB (194953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f2f89f6e5b32cb4e19d2acf7de64bd63480f4cb6d641b7f51c6ed9d0ba912`  
		Last Modified: Thu, 14 Aug 2025 07:51:55 GMT  
		Size: 819.7 KB (819692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b2a04e400dd2244fed0263db215bd4bb35bf86b5cb5ace780c0a84fa8af603`  
		Last Modified: Thu, 14 Aug 2025 20:15:06 GMT  
		Size: 7.5 MB (7462696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:6d466969b43331acb15357d17dffd0d3de20bfe195928f00b3a38ccc919ecc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23241443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389449a71ea2530c15de7f66a5a217eaf3a504dfb7d96f04678823080bcd2ec0`

```dockerfile
```

-	Layers:
	-	`sha256:c08644e762daaa96ea744cb07702cd949f041843ddf3de5747462b6462739c88`  
		Last Modified: Thu, 14 Aug 2025 21:47:32 GMT  
		Size: 23.2 MB (23230984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de4858fa39a04adc0f3d2cab212a40e1506eaab27828c23afa9da3ffc2779d9`  
		Last Modified: Thu, 14 Aug 2025 21:47:33 GMT  
		Size: 10.5 KB (10459 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26` - linux; s390x

```console
$ docker pull elixir@sha256:55fe8bcb59a2992197e3bc1dd6e14518791151f5ea47b8d36d2d4fba4fb1c85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584608115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c01de197375ffbdfc6fdfcbeebe756feab637a8486437246dc8cb7c9cd1667`
-	Default Command: `["iex"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV OTP_VERSION=26.2.5.13 REBAR3_VERSION=3.25.0
# Thu, 22 May 2025 14:26:26 GMT
LABEL org.opencontainers.image.version=26.2.5.13
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b58e5caf34ef4e94b766173f3839ff29db3bfa9710881f246a9958886b466ac4" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2-1 			libwxgtk-webview3.2-1' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.2-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["erl"]
# Thu, 22 May 2025 14:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Thu, 22 May 2025 14:26:26 GMT
ENV ELIXIR_VERSION=v1.18.4 LANG=C.UTF-8
# Thu, 22 May 2025 14:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="8e136c0a92160cdad8daa74560e0e9c6810486bd232fbce1709d40fcc426b5e0" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Thu, 22 May 2025 14:26:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b9cbc74544afc5347651ab08e064f57c5d096af02c42cfe03213911a89bce4`  
		Last Modified: Wed, 13 Aug 2025 19:43:03 GMT  
		Size: 183.4 MB (183435038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00df7cf3acf6d844fffd8fffd199fe5de40bf68d545e65dded60e35cbc8badb0`  
		Last Modified: Wed, 13 Aug 2025 20:00:28 GMT  
		Size: 258.0 MB (258027827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e72201bcea72d72440f8d81440738637df6e38a45bcbbe353f054713e6c97f`  
		Last Modified: Wed, 13 Aug 2025 18:47:42 GMT  
		Size: 194.9 KB (194946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34747dbe661de3a983f0e4c6733b8d26a3c03a607a2e57f6d35add7c5fe5ec17`  
		Last Modified: Wed, 13 Aug 2025 18:47:43 GMT  
		Size: 819.7 KB (819693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b11095d7a6484954473a556e3487dd3d29e481b834c66f6af9b2bcf6073e3`  
		Last Modified: Thu, 14 Aug 2025 05:06:19 GMT  
		Size: 7.5 MB (7462804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26` - unknown; unknown

```console
$ docker pull elixir@sha256:f263ee2684c358c5947a7cd2fb7f92a27ea11726125a8319b76717b0cd7623ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18edb07d81b162898cdc27a483b198733f89b7dc06f0be8063c00572a3f0d6b6`

```dockerfile
```

-	Layers:
	-	`sha256:78112417f48118b27b94b0c0517215c247afaad64f2e5f1b9acab8997e189676`  
		Last Modified: Thu, 14 Aug 2025 06:48:49 GMT  
		Size: 23.0 MB (23042847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a5360a77c2fb9f2e0eaca201d7fb2bea154ff69c538fe88a846e9a56114326`  
		Last Modified: Thu, 14 Aug 2025 06:48:50 GMT  
		Size: 10.4 KB (10420 bytes)  
		MIME: application/vnd.in-toto+json
