## `elixir:otp-27`

```console
$ docker pull elixir@sha256:c4b5428991031ab3ea1cd6bbe8bdf278252a743f1dc944083a621fbe2fd3c4ba
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

### `elixir:otp-27` - linux; amd64

```console
$ docker pull elixir@sha256:b312baf2d503c1019b66fdf5bb3941e011a452302d6f968f1cbadcae7ba7a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.4 MB (626440022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efbbe3ec7f1c17b5abefadbef7b2a65bf1b8d74a50e13b5e1372d3478efb6d5`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:21:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:15:17 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 11:15:17 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 11:15:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 11:15:17 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 11:15:17 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 11:15:19 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 11:15:32 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 12:16:59 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 12:16:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 12:16:59 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1208d53eb0667932469017a5ef3960e5ed2aea9143d62b983abe2f8593eeb9a`  
		Last Modified: Tue, 18 Nov 2025 11:12:42 GMT  
		Size: 211.5 MB (211460976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da882e94a9e84561d719a6125896192d81ae97cce4edeb4d594d4cf974d232c7`  
		Last Modified: Tue, 18 Nov 2025 12:16:16 GMT  
		Size: 269.3 MB (269284454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2091be48897ab75e4b986a6209f39f9e14526f560907ac8e7dc107969c3e34`  
		Last Modified: Tue, 18 Nov 2025 11:16:41 GMT  
		Size: 195.6 KB (195619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec88d5e41da6a83f8d6b3cbd5e6c34ca31d1f2296982240a641c37bda981080f`  
		Last Modified: Tue, 18 Nov 2025 11:16:41 GMT  
		Size: 822.5 KB (822510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a731db84f96a0a86bef2eb4fd1d8042ded4a39e83d0928ec3a5c2e4b92b724`  
		Last Modified: Tue, 18 Nov 2025 12:17:53 GMT  
		Size: 7.8 MB (7770092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:297cf15677c6474b5d3e65dde1d2d37389577fd63b86b3106937aab1c16ff7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23785602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5daaa08b54a010691b13b9327d938c2fb562600a6670b12a033e64b2f2dd0a`

```dockerfile
```

-	Layers:
	-	`sha256:24f5e32d915f6ff57ef8f141c3e42149700f3945c0dcc52e86922262feb332b0`  
		Last Modified: Tue, 18 Nov 2025 16:49:03 GMT  
		Size: 23.8 MB (23775225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168ef35550855020913b3cf4b540e3998242dcbeeec2e7faeb65d353e2ce4e17`  
		Last Modified: Tue, 18 Nov 2025 16:49:04 GMT  
		Size: 10.4 KB (10377 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f4ef3bebc861721f80c5634fc2c482da99afe1f6576b90cdb584cf0d67855fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.0 MB (548980999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5142c70b5691aab51f4ab137a842c90d3704a52694d86aa604170682ae6c8c22`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:36:48 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:36:48 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 07:36:48 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:36:48 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:36:48 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:36:52 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:37:15 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 08:48:40 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 08:48:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 08:48:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad0f2d457569ebe1e8bb868d038539ac612c99d1c10b8c279ff1a9fd7fa24be`  
		Last Modified: Tue, 18 Nov 2025 07:34:33 GMT  
		Size: 175.4 MB (175370481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4474e0010c417d68e81b0dbdd2094aa0d37495b4285e269bf7379ec072296dba`  
		Last Modified: Tue, 18 Nov 2025 08:47:38 GMT  
		Size: 239.0 MB (239039295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218fdd71e237e6192706c50bffe1df5761ac0da3c49039c8f8960ca967df5384`  
		Last Modified: Tue, 18 Nov 2025 07:38:14 GMT  
		Size: 195.7 KB (195690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1159aa53fd3cd5ef3ec9eb587bb407fd6bb594210ad6a28ae493416158df42df`  
		Last Modified: Tue, 18 Nov 2025 07:38:14 GMT  
		Size: 822.5 KB (822510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e9ad9d1840ce7bbb3b1bb4d9481607e56b58e9c29011f4799e65c49672c39`  
		Last Modified: Tue, 18 Nov 2025 08:49:16 GMT  
		Size: 7.8 MB (7770075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:990416cde12873d323de9333c6fa2ee826a09355ee40a6af68302702308bebee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23598639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf710b07f41cc4052ace84b34f0f690035b7e21ad8b4b65613ca1c3180e52dc`

```dockerfile
```

-	Layers:
	-	`sha256:e530717b3dbc7af658c4ed45cd41aad6f5e19f8eeaac0b6a6e7f0176d4a74f6c`  
		Last Modified: Tue, 18 Nov 2025 10:50:44 GMT  
		Size: 23.6 MB (23588191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edc4ce521a225f10333fe5a6cbe1fae3441726aee0f54a79010390a459eeb15`  
		Last Modified: Tue, 18 Nov 2025 10:50:45 GMT  
		Size: 10.4 KB (10448 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:6c7d6f1ff2cf2d9104ea88dcd1ed83dd597eb4c261b4ff69b5885c83ea21c57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.4 MB (610437147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7939859957054c251056dbc9b15375f0f49202146687736fbeab5523f9b9c6`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:17:35 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:17:35 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 07:17:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:17:35 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:17:35 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:17:38 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:17:49 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 08:24:51 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 08:24:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 08:24:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea7607dced22dd12cfb6fe96ff19187f5ee918dd3d48379e2d2fd756af4818b`  
		Last Modified: Tue, 18 Nov 2025 07:15:14 GMT  
		Size: 203.0 MB (202980192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be365727e730216bec83d81c78458908d50eabad694b95bafd2509ac14b529a6`  
		Last Modified: Tue, 18 Nov 2025 08:24:08 GMT  
		Size: 262.3 MB (262339835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4bdfa4cf3d0df615e72ea458e005bcb213efbad93f43cae5888da08ee96a0f`  
		Last Modified: Tue, 18 Nov 2025 07:19:03 GMT  
		Size: 195.7 KB (195677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4fb1ad6f52e0ae7c287a19d2fa7fa3c22713887815ba955878b9e51e4704b2`  
		Last Modified: Tue, 18 Nov 2025 07:19:03 GMT  
		Size: 822.5 KB (822510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9294b56f84018c01eb963304d3061805ed68168bde607de18da616a5bec954`  
		Last Modified: Tue, 18 Nov 2025 08:25:32 GMT  
		Size: 7.8 MB (7770061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:c298ece234bdf61bbfb820e26ae7375fd20603bbd3edc1304eaf9546d7dfc59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23825139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec607adffa5f779ac325d2b3b612abfda8ea73ef0f014a0335c8b7ec68f53d0`

```dockerfile
```

-	Layers:
	-	`sha256:e0c18af5f99f02e44b8549e600cce9b466167eb1fbbbd2ac63c817dc32d8d388`  
		Last Modified: Tue, 18 Nov 2025 10:51:07 GMT  
		Size: 23.8 MB (23814670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a70c67cf04ea4fcd151f3c1177b04b113cf43fc350f4f30e5a05ca1e76e0e8`  
		Last Modified: Tue, 18 Nov 2025 10:51:08 GMT  
		Size: 10.5 KB (10469 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27` - linux; 386

```console
$ docker pull elixir@sha256:624cd72a0c4a08aa1005ca8504dcea900fbd758b8d899097b36a6dece1be2222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619716268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9d07f902fb03bb91814faa3389afadb21f9604f1c3c36bc546ee52f18805e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:22:23 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 06:22:23 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 06:22:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:22:23 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 06:22:23 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 06:22:27 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 06:22:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 07:21:02 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 07:21:02 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 07:21:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c185d92b9a40ab45d15fa519a2c049e78267565301d35e186267bc212115f`  
		Last Modified: Tue, 18 Nov 2025 06:19:22 GMT  
		Size: 210.4 MB (210389386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2208d60d767499d65b8716f2a0d27d8a0878ce436f8903ea35685ed394567c2`  
		Last Modified: Tue, 18 Nov 2025 07:20:01 GMT  
		Size: 260.0 MB (259973559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239def77d2d8916043da536029992d908d2ef33bc8b5b4db681add8cd1112243`  
		Last Modified: Tue, 18 Nov 2025 06:23:54 GMT  
		Size: 195.7 KB (195659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3feb6443027d9923b9026b660583dcc29b827b33251fc8822586fdd69aa373`  
		Last Modified: Tue, 18 Nov 2025 06:23:54 GMT  
		Size: 822.5 KB (822510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553cfd66c0e2cacd70d071dc85cebf6a0c5fef3534335da2f750a0fb6ae80780`  
		Last Modified: Tue, 18 Nov 2025 07:21:43 GMT  
		Size: 7.8 MB (7770003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:dbe748709464f97487f88f0b9724fff36f219ed25d672725fa263ce235b9c019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23753256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f461f2e2b813e62c5c812aa16cc31d7f3c85c9b81a97d8b8a7d9173106719f`

```dockerfile
```

-	Layers:
	-	`sha256:dd3d8a9c85c26c90b726401657c3578953bcc46ff0353899e940f67d5f04c5eb`  
		Last Modified: Tue, 18 Nov 2025 10:51:29 GMT  
		Size: 23.7 MB (23742906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa52a0cf1a1d07be965e0edbf4956f8c39d94b1f288e2afbd389203112deb6b`  
		Last Modified: Tue, 18 Nov 2025 10:51:30 GMT  
		Size: 10.3 KB (10350 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27` - linux; ppc64le

```console
$ docker pull elixir@sha256:8b1511acde0c429127c871dc756ef2d12a9ea8cfeadb8c2292791c8cac3bf987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 MB (634410915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6647b19d25a5d1195173db8d15cae2659e922d143bfb64cfaf780e5a954bfaf`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 09:15:29 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 09:15:29 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 09:15:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 09:15:29 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 09:15:29 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 09:15:38 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 09:16:21 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Wed, 19 Nov 2025 01:31:16 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Wed, 19 Nov 2025 01:31:16 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Wed, 19 Nov 2025 01:31:16 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055d1d2e62969664b2197803b2dd13eb0c52b160f256835c7b8bb1eca8dc83d`  
		Last Modified: Tue, 18 Nov 2025 11:54:22 GMT  
		Size: 214.5 MB (214498281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb82e18a83653cbb96a61dc60aeddafca93dccd4454ead1253598937fc76146`  
		Last Modified: Wed, 19 Nov 2025 04:49:09 GMT  
		Size: 263.3 MB (263280174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5ee7d7ad69ca2e677a1c867aceb157cdb460978d521db5c13b03979e13e24f`  
		Last Modified: Tue, 18 Nov 2025 09:19:06 GMT  
		Size: 195.7 KB (195676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d7371d733f6d37b191a22a912f1c28973a485884ba2c7eaf883462ea51e19d`  
		Last Modified: Tue, 18 Nov 2025 09:19:07 GMT  
		Size: 822.5 KB (822510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdea90eff24f1c03d3791e2613734269c97faafe20392688d9c352f357741f2`  
		Last Modified: Wed, 19 Nov 2025 01:32:52 GMT  
		Size: 7.8 MB (7769671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:8f47f10055f036c2f702775ed59d7a7111261a794e95b895dde13b7f2564769c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23741125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ee623ad1cf50ada6aa7a471897038c50cf38a25d13dc7816186ee0ff101ef1`

```dockerfile
```

-	Layers:
	-	`sha256:76adeee8b336aad8119ebddaa34e093794582bf59a3188941db40a46852364b7`  
		Last Modified: Wed, 19 Nov 2025 04:47:37 GMT  
		Size: 23.7 MB (23730710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47693fe23fa7c26b1882449a8785ce281a9718b7f1c52c2bf9520d459c6079ed`  
		Last Modified: Wed, 19 Nov 2025 04:47:38 GMT  
		Size: 10.4 KB (10415 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27` - linux; s390x

```console
$ docker pull elixir@sha256:450e71be85fea3d5b2f5b8888faba446e28cc6a01ddf70f78546d87af5e24f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587675630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4e68b0cf0d232ba46d07ef8f8aea73f293861690842de49457ca2cc0b04501`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:29:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:20:25 GMT
ENV OTP_VERSION=27.3.4.3 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 08:20:25 GMT
LABEL org.opencontainers.image.version=27.3.4.3
# Tue, 18 Nov 2025 08:20:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="597618c75890e8e606033bc8dbf6ec87fdf4e892c10b4912ae3c9a4f01384579" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:20:25 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 08:20:25 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 08:20:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 08:21:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
# Tue, 18 Nov 2025 16:00:58 GMT
ENV ELIXIR_VERSION=v1.19.3 LANG=C.UTF-8
# Tue, 18 Nov 2025 16:00:58 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="a76299ec8d14b43a84a03b3b700b9f912a64912f03ced8e024ae267b7e40c26d" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Tue, 18 Nov 2025 16:00:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a3c31d224355129a49f91ee32618f26bf3cb019a25f07a3795c22816b92b87`  
		Last Modified: Tue, 18 Nov 2025 08:13:31 GMT  
		Size: 183.5 MB (183498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ec2015aaf0f0116fc29151253d23b8ab91f5e28807b756f240bff6100d5c3f`  
		Last Modified: Tue, 18 Nov 2025 16:00:16 GMT  
		Size: 260.7 MB (260722987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1edb8d028013451acb6bfbda484ae907c84e0e934e5322af7676a4ff7cf6ebf`  
		Last Modified: Tue, 18 Nov 2025 08:25:51 GMT  
		Size: 195.7 KB (195680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a600ae40b17d2d35b11ae58a4abe9ac9a77eb752c233ededb67ecc90a5129d57`  
		Last Modified: Tue, 18 Nov 2025 08:25:51 GMT  
		Size: 822.5 KB (822508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea4f9b6e5f06d0e31f55348e36a466fa136688968d4216ec7b5e2662a48800e`  
		Last Modified: Tue, 18 Nov 2025 16:01:46 GMT  
		Size: 7.8 MB (7769986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27` - unknown; unknown

```console
$ docker pull elixir@sha256:05a0ce53045388c2a362f2dfd4b7eec63d101f1695e7438a2c01f189e4f8a96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23553068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683dc438da4e060ab972120e3279016884c7afb87e7c169c941d4a1a5a5e499b`

```dockerfile
```

-	Layers:
	-	`sha256:fd1c535a9b180a1113cd00eb348d2edf1496854ef1cd85dd7c1d34d5dd25d898`  
		Last Modified: Tue, 18 Nov 2025 16:50:52 GMT  
		Size: 23.5 MB (23542691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7496d8c8901b8d2767020c23410593547f6c5059dc7de39c885c553a00f1d3cc`  
		Last Modified: Tue, 18 Nov 2025 16:50:53 GMT  
		Size: 10.4 KB (10377 bytes)  
		MIME: application/vnd.in-toto+json
