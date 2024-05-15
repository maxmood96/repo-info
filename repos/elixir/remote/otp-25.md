## `elixir:otp-25`

```console
$ docker pull elixir@sha256:c5444a2b8af717f26e0a9b9cee72425e55caadf9ffe9c12b3e19be67fd320ded
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

### `elixir:otp-25` - linux; amd64

```console
$ docker pull elixir@sha256:bb342cdb6a8b306b945f83b3528833d7447d9aad57739df47c2262079569e647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580109362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be832d9a0bf7fcf41cd240aff8a08f2bd0a60f1ac66c5491fdbaa0a601c859e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b0f947a3988ced690ace9d52e80ae5af9bed7277fb302e55de15cc97e56d73`  
		Last Modified: Tue, 14 May 2024 05:16:27 GMT  
		Size: 249.8 MB (249812606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97237afc606d72c3886e7f357b2835c06f37ec927e5a8f299716cc36542a8df4`  
		Last Modified: Tue, 14 May 2024 05:15:59 GMT  
		Size: 198.6 KB (198617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c151f336b17f448790195cf7cf9095717c1116303ae1dea8a0611a27308e4d0`  
		Last Modified: Tue, 14 May 2024 05:15:59 GMT  
		Size: 803.9 KB (803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072d79bb5a6720e507c8ed1034f68d5b4b409fbff0edc4889766c480d64ac60`  
		Last Modified: Tue, 14 May 2024 05:57:43 GMT  
		Size: 6.8 MB (6826205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:54a391ca6521403d5a8653c41977b6f9b49cdc996f8013c9efaf7f774b1e8a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22699442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6d60ba7109114d41e4aa0d3ee540aa8fc30fdcb921fdf8a0a6dbf67fbb5b18`

```dockerfile
```

-	Layers:
	-	`sha256:66a5123687af5fad3e75b0471b1332bf563c325e9846558b2507be396cb4869f`  
		Last Modified: Tue, 14 May 2024 05:57:44 GMT  
		Size: 22.7 MB (22688095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd138137e72e45b8fa3be47af9e3b28aafa9aeff191097180e41a10485ef9ff`  
		Last Modified: Tue, 14 May 2024 05:57:42 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6839addabc423782248fad7aa1083cdd466c300713f9e58cb827ff1d68a06a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515358358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e0e0d17376dd45ac558fce64413c80509c99fe4c960949d8aa06f0311d14d9`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6f4b9983a8ee98e2432d49e727c6278cadb8efecf5ab79268999b8d08c984`  
		Last Modified: Tue, 14 May 2024 01:48:20 GMT  
		Size: 50.4 MB (50359447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b75020cd82336d3062778f825587beaa94285a03f3e7cdf28704af4743b57a`  
		Last Modified: Tue, 14 May 2024 01:48:55 GMT  
		Size: 167.5 MB (167476287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b6409a9715479112f7048d8dcf053cd1c80e604e167ab13fb7c8a187d55b6`  
		Last Modified: Tue, 14 May 2024 03:53:51 GMT  
		Size: 224.6 MB (224557019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c5b0726529b3f04dc053e8e8f50180d21cfa4018c57e50173dc4fd500313d`  
		Last Modified: Tue, 14 May 2024 03:53:25 GMT  
		Size: 198.6 KB (198585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322016939f1af9a1bbdfa13e5c8d6d7054647b9b2fd6940734619576ca400990`  
		Last Modified: Tue, 14 May 2024 03:53:25 GMT  
		Size: 803.9 KB (803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada46ab4d19938551d273904e16ad70ecac39882c4c2f8d25460e652c431f033`  
		Last Modified: Tue, 14 May 2024 21:28:46 GMT  
		Size: 6.8 MB (6826335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:a447346cf95bae0a40ae07b016bc033abe8573076fa107faafa9be1215770ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22509698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04140b567281947aef8fb9b60ee380bc0dc6d86faf40b1bc967959c744d06533`

```dockerfile
```

-	Layers:
	-	`sha256:9af2b704b4ca4a79664e6b71c7c5f8f8058a454b7996b88e60cf78dab7443837`  
		Last Modified: Tue, 14 May 2024 21:28:46 GMT  
		Size: 22.5 MB (22498288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec60a7f645201f7afedd276403ec7be5bed5016ddb0f3e5657fceb9120335c25`  
		Last Modified: Tue, 14 May 2024 21:28:46 GMT  
		Size: 11.4 KB (11410 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:772dc7a570046e9216bab9d03157370f3758d74c0bee5b1a0bcc0e831b71da7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.1 MB (566084641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c8cae2461ee505c53fc4329784e4bec050e439c3760fda8c65aab079bfd0c0`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce352085291a4828eefe3a8fe5557c610cb7e308cbe4a56a62e0922171dc1c`  
		Last Modified: Tue, 14 May 2024 01:54:08 GMT  
		Size: 54.7 MB (54696093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef9945e6cc16f20fb350f760e6d9f98378b467040f7a00ac783d81334031`  
		Last Modified: Tue, 14 May 2024 01:54:32 GMT  
		Size: 189.9 MB (189936403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27329056d03afbc50993daf8c1f17cca1337c3f77369362d70ce31c4ea467f`  
		Last Modified: Tue, 14 May 2024 09:05:51 GMT  
		Size: 244.1 MB (244133834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b98508b5f85182dbe70dd837d290a3a7377939da350be9e8e1cd893de4124`  
		Last Modified: Tue, 14 May 2024 09:05:30 GMT  
		Size: 198.6 KB (198633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6630115a792d803aa742f0061fe400a3b8c9e3b2428dfda194090139bbf3eb7`  
		Last Modified: Tue, 14 May 2024 09:05:30 GMT  
		Size: 803.9 KB (803947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a976a37185584c279d6b0085dc67bd53d0162693cd1de67bda44b35ec0ca2562`  
		Last Modified: Wed, 15 May 2024 01:35:49 GMT  
		Size: 6.8 MB (6826216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:d591c1bde0675c47a532d0bbb8a3edb3cd20baa6e27e6f67ecdcdf2ba563e843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427622468ec3e7b4e37f11266bd172000a3cccf5af79fcb53902d5a946c276dc`

```dockerfile
```

-	Layers:
	-	`sha256:d227c4a0fd9abf53c76f097f3e7db969246768c45e4d61f5cecdd6c14d85b1b8`  
		Last Modified: Wed, 15 May 2024 01:35:49 GMT  
		Size: 22.7 MB (22698667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f97e5df79b62cf9fa1026c45d4a79a1063a2b0cb7c7b9913a326508871299a`  
		Last Modified: Wed, 15 May 2024 01:35:48 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; 386

```console
$ docker pull elixir@sha256:2c8c6ceb33208ac75124581e6951993cd3068ee6c49f8cc96a0e9c78aa919b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581543290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a726c0f8bff36b711a8c400f726c7a6ab7a2b7d172a188acac5e1d3d40b90f97`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e16878498082da3be413141adb855109c55626d0485b6aafb79e1cbdc5474`  
		Last Modified: Tue, 14 May 2024 09:14:33 GMT  
		Size: 16.3 MB (16268989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45622f6623917a1133bbaccf5f0fa4ae87c3ed7e9cbdcb259e65485804757c02`  
		Last Modified: Tue, 14 May 2024 09:14:54 GMT  
		Size: 55.9 MB (55929438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584614a415369245291ab36f58dddbdd2da056a8b7929f7069c0a8d75f68b86a`  
		Last Modified: Tue, 14 May 2024 09:15:41 GMT  
		Size: 199.9 MB (199916723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca73af95149a4314087eb4af01de247f99d8f36d8c70786a00796a8119e5310`  
		Last Modified: Tue, 14 May 2024 20:12:25 GMT  
		Size: 245.5 MB (245523168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3686121c43d89958a5c72d473c0e557a5b307159bb1fe5cf4dfabfbcdad868f`  
		Last Modified: Tue, 14 May 2024 20:11:39 GMT  
		Size: 198.6 KB (198627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ade7b26c226e6921ce0ae92bc7a3da75964119221a569894aded846477737c`  
		Last Modified: Tue, 14 May 2024 20:11:40 GMT  
		Size: 803.9 KB (803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0920f6adb3a36b060d624d82c3241b152529e18ff21061609a99675bbaf04cc3`  
		Last Modified: Tue, 14 May 2024 20:56:36 GMT  
		Size: 6.8 MB (6826343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:3c0081e73d1f6f3e6f64e872cc0ed2f7503f3c8a579006068a92c426147c77ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b32d2fc7fdd343865d8a0d35873471f416496db14bb11775294a9d42ed18ded`

```dockerfile
```

-	Layers:
	-	`sha256:37a3c0c92f05cc65862b3338e52ba30e4b62c0fd2b62a8abad966759bb3a71fe`  
		Last Modified: Tue, 14 May 2024 20:56:37 GMT  
		Size: 22.7 MB (22676185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad9f9adba9d18443e5e66d2dda8257b7cc2d449e82e9258930b517e366810aa`  
		Last Modified: Tue, 14 May 2024 20:56:35 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; ppc64le

```console
$ docker pull elixir@sha256:54049fa2bb132746ee263c8efe9181b9c9f6448ba42e611f1c55c9bf7a7bf5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.4 MB (586420063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63da4b09cfe79bcb14a6127a10c61923fa5c617e7ab1eb442f7474fb7eb8ee9b`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d0e9056be49b56fb034ae67015f749411fff8fbd5b427d798c9847f60a8251`  
		Last Modified: Tue, 14 May 2024 07:12:37 GMT  
		Size: 196.4 MB (196363387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ff75b9d4958ed4fcae83b9ff9b3cc21e8c6be962a4d6a5e2e126d6befc99dc`  
		Last Modified: Tue, 14 May 2024 10:19:53 GMT  
		Size: 247.6 MB (247617732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b0bc68c6f9160878ed9ba20fc7d9a3cd8e46236ee101407fa62583af8b35bc`  
		Last Modified: Tue, 14 May 2024 10:19:20 GMT  
		Size: 198.6 KB (198627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf7b13b5a72118f5b5ace52a5970e06dc6d5ac568b86d0a761dd2d6087c8906`  
		Last Modified: Tue, 14 May 2024 10:19:20 GMT  
		Size: 803.9 KB (803947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289df0b0190fa8425aea6d702b9eb2b8c4990df2e2f0a4d1b1e62ce794bae26a`  
		Last Modified: Tue, 14 May 2024 17:41:15 GMT  
		Size: 6.8 MB (6826226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:b582d73e7c4e46f324245016a045f4358caaea99fbee8d4585874dfbed0ed9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22654271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3692db996a3ff8174ca2b405d06e685fcd8015746937d36de4bb0c4ce8c7cf`

```dockerfile
```

-	Layers:
	-	`sha256:60005fc332fd5d6e3d33985956bd7837054b860ccb11da641282955e815ddf40`  
		Last Modified: Tue, 14 May 2024 17:41:16 GMT  
		Size: 22.6 MB (22642891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3938ea74a6a823a5261f0d1b7a6f951e1a9a8d07cde61131c3f7b3ea8ed45c88`  
		Last Modified: Tue, 14 May 2024 17:41:14 GMT  
		Size: 11.4 KB (11380 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-25` - linux; s390x

```console
$ docker pull elixir@sha256:b872a8ce7aeb2d4e28684669b48d1f358b5d0b7419c870f1234bfde1116e8df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 MB (540942459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23531a0bc4d4f5a8bd551e4c64b6f6ab5de5eba0b331d46fb08228631f5c8db8`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 11 Mar 2024 18:49:41 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
ENV OTP_VERSION=25.3.2.12 REBAR3_VERSION=3.23.0
# Mon, 11 Mar 2024 18:49:41 GMT
LABEL org.opencontainers.image.version=25.3.2.12
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="2fd35a207278569bb56746fd2ba55037d439922875422dd29d458cf36ddf0618" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["erl"]
# Mon, 11 Mar 2024 18:49:41 GMT
ENV REBAR_VERSION=2.6.4
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Mon, 11 Mar 2024 18:49:41 GMT
ENV ELIXIR_VERSION=v1.16.2 LANG=C.UTF-8
# Mon, 11 Mar 2024 18:49:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="f53d06f3e4041c50e65b750e5d56fec9cc7c6a44510786937c6a5bb0666a7207" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete # buildkit
# Mon, 11 Mar 2024 18:49:41 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c7ec963ac714a2f94b076f8e287270d7deb6f725c170e54c73463524ff8f0a`  
		Last Modified: Tue, 14 May 2024 01:30:55 GMT  
		Size: 173.0 MB (173025883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67203f3d3d021fdbe8902af41939f94383133d3a7cfd9864cf40a3fe67e27902`  
		Last Modified: Tue, 14 May 2024 06:24:56 GMT  
		Size: 237.0 MB (237031034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8006b024ef218e2af28ab4f694ed0ffe7a5128373a5aaa1957ce3fc203ade`  
		Last Modified: Tue, 14 May 2024 06:24:31 GMT  
		Size: 198.6 KB (198616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ddb3fa70e6995805a92f43a572f4f715dd509ab1075ec0e1b729753e1682be`  
		Last Modified: Tue, 14 May 2024 06:24:30 GMT  
		Size: 803.9 KB (803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e79801760a6d94422bc5efa966a79c8b87b4f92de3ce50f29add5721280f9`  
		Last Modified: Wed, 15 May 2024 01:47:57 GMT  
		Size: 6.8 MB (6826172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-25` - unknown; unknown

```console
$ docker pull elixir@sha256:96cf1b29859b664f3feb118df62c8c57850d8190bf4e6cdc0ff1f74fcd9d90c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22489644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb57f5aaadf8a71ad835bbf6ceca1e0378461ebab9c6e132c4dad6af73878d8d`

```dockerfile
```

-	Layers:
	-	`sha256:f29582c54ec056eb578775501e5c072d0a81744b92170d924eee8e8ee1155fc4`  
		Last Modified: Wed, 15 May 2024 01:47:56 GMT  
		Size: 22.5 MB (22478296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8aff790e5e0cac7b5acb5306b9c833dcc9db891ef92f76d0f7968d916cd67eb`  
		Last Modified: Wed, 15 May 2024 01:47:56 GMT  
		Size: 11.3 KB (11348 bytes)  
		MIME: application/vnd.in-toto+json
