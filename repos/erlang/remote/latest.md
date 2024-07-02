## `erlang:latest`

```console
$ docker pull erlang@sha256:cd8b40c5192e35debec03cfd7afe61fcd7c533f43c4121b848e6f9e302771d45
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

### `erlang:latest` - linux; amd64

```console
$ docker pull erlang@sha256:5542eba4ef5c6ae5e70386f62773c48a7f5c78fe72c19d964a2977f01b035ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.6 MB (603578600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e86bf4aa5827995f4f8a138ee47def6f02dc74106b592ce0e58cd1538c2b54`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae70830af8b64968596022cd9041ce522f0c77eab5419b19e169b53582c69e3f`  
		Last Modified: Tue, 02 Jul 2024 02:01:09 GMT  
		Size: 211.2 MB (211225279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce91878471fe0f045804b5259d1f0f09a017c117ffcae193358f1f6193ca180`  
		Last Modified: Tue, 02 Jul 2024 03:13:08 GMT  
		Size: 253.6 MB (253605744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1b829c2a12ee0752cb5e9086abf1625ed28b9ccd51715684744c2a92427680`  
		Last Modified: Tue, 02 Jul 2024 03:13:02 GMT  
		Size: 195.4 KB (195384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6838035fd1248d985521482ef14ce9cb13179767074c8ac91f6cd8a1a817628`  
		Last Modified: Tue, 02 Jul 2024 03:13:02 GMT  
		Size: 805.4 KB (805407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:2a2382aac968965ae93260d26ebe237a5f2f19b3979ff65590084c3a06ed3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23192677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd52f6482531ed24e6f1a92ddc8abe74013bc5c59dcbc7eb4e8585070a406640`

```dockerfile
```

-	Layers:
	-	`sha256:0342dbc9d416583772a7632a99babacdcd48b8009e0db4bdf6eab50b8cf65b89`  
		Last Modified: Tue, 02 Jul 2024 03:13:03 GMT  
		Size: 23.2 MB (23173606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1b490e5a8346449a430eb240e27195832d940260e5350576dfe5863a716cc0`  
		Last Modified: Tue, 02 Jul 2024 03:13:02 GMT  
		Size: 19.1 KB (19071 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:003f916fddf4de7b885da95383cbdcfb5e4a34babc18eef45c473652c378df61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.7 MB (543653301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28b4af62e5bcc467c16f9197bfd760e596b69a65086bf9f5ecfb780f7ded17b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:f1ff7b6851f56d19040d12cd1d8757075037a3e51cd0d20ddfedfe600e399be6`  
		Last Modified: Tue, 02 Jul 2024 00:51:07 GMT  
		Size: 47.3 MB (47320358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ec281dca54581a50ec4a927c64bebe7b6ef47dad0b260009c44ae5a8feddc`  
		Last Modified: Tue, 02 Jul 2024 01:22:39 GMT  
		Size: 22.7 MB (22727504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c366b742114f1b314834ae656bee5e41f5e30629107aed4bd693207e1ed0df`  
		Last Modified: Tue, 02 Jul 2024 01:23:00 GMT  
		Size: 61.5 MB (61520104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec006b2fd0fa59480156cd480431866e4136d69ec003c1c9a01cc6cf74b4a11`  
		Last Modified: Tue, 02 Jul 2024 01:23:39 GMT  
		Size: 184.5 MB (184511793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b0957037d1e6c33535060788448ed873f1c7f6f901bf8c0eee8aca497140f`  
		Last Modified: Tue, 02 Jul 2024 04:05:18 GMT  
		Size: 226.6 MB (226572789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c70d554c30b6080f9ae656ddf498ef8f2b56c99b3dce661879bb1dd4c0165d`  
		Last Modified: Tue, 02 Jul 2024 04:05:13 GMT  
		Size: 195.4 KB (195351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5678b77b825d659fdd448eac2877d1907d7a8b504d70650de30c8ef4478718`  
		Last Modified: Tue, 02 Jul 2024 04:05:13 GMT  
		Size: 805.4 KB (805402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:48727b37606343f9e7102f372bd2671e189c54eaa2aae382b6062175d74de3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22993459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a144350df6b7b7899cea923a9817ffdd9f7305e41c11ca0652bde970c597ea0c`

```dockerfile
```

-	Layers:
	-	`sha256:0a273160feb7859c6fa1d2b7e7334edd4eedc93944b0f073bf1f7494c581a8ea`  
		Last Modified: Tue, 02 Jul 2024 04:05:11 GMT  
		Size: 23.0 MB (22974284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56a0aac880d7fb4fe6d5d1780cab564a9540cbc82341d00cce1139d2531599d`  
		Last Modified: Tue, 02 Jul 2024 04:05:10 GMT  
		Size: 19.2 KB (19175 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:577ac7b5b2b4e5df6f5a1591bc2affa8414faff2c77f5c121fd94f75365351df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.2 MB (526196625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4c44e0c625cc89ef5e6496949bb450c87106af32e8aaaa70af69658e8b28a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ceb3cc12c0338c85a0602b703f838a13aa2e232ffde0c008b8db42bec79a26`  
		Last Modified: Tue, 02 Jul 2024 01:40:01 GMT  
		Size: 175.2 MB (175164748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1a7536eb30f731ce79ef9c9f15f041205e62102ad50d86322e711130a331a7`  
		Last Modified: Tue, 02 Jul 2024 06:46:47 GMT  
		Size: 223.7 MB (223706585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3be72b6e803c9118e7dbc599865cba240d59646605b9eb1107bccc23fe8cb`  
		Last Modified: Tue, 02 Jul 2024 06:46:42 GMT  
		Size: 195.3 KB (195342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e9436bc62f05ba68d17dea060607b4f51db6a0229733db3ca2fa2f3b481dd`  
		Last Modified: Tue, 02 Jul 2024 06:46:43 GMT  
		Size: 805.4 KB (805407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:e76157c2185e8fe294f73c700c969f6a5470140e87aeb50126541744d48036a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23010389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70c44783076612f9248b0d868f73cfe1108d7d83f800cbcc8da2121dd89bf2c`

```dockerfile
```

-	Layers:
	-	`sha256:9b3952422c6b57dc23bc8c6447dc4d2f58c2ef7dd7f2411fdcc81f5fef9eb874`  
		Last Modified: Tue, 02 Jul 2024 06:46:41 GMT  
		Size: 23.0 MB (22991214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a16a70a1d99c109b0cca0c72aa4086d363505014b56901269d739f45ca9d49`  
		Last Modified: Tue, 02 Jul 2024 06:46:40 GMT  
		Size: 19.2 KB (19175 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:e69be5be5ee6bdb2e5018c0f972e234371b73b8f98868d024eef0e06d42937a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587764179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ca205c3edc89a41d35df0a1367ff5b665ec5a1f1362c593c38a7b6bba406de`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1229cbc2fd707fab12c8b26350a18ec1aa51a90c15945a4f665725ec38b566d`  
		Last Modified: Tue, 02 Jul 2024 10:38:55 GMT  
		Size: 247.0 MB (246978374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f45cd1017b956c23ece7c9d220461a2ca1e36b81621e073268d2580b364624`  
		Last Modified: Tue, 02 Jul 2024 10:38:51 GMT  
		Size: 195.4 KB (195369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9c306eba4fa2fcadab85890e96233fc0e40afcbe13f777f720353376f85ca`  
		Last Modified: Tue, 02 Jul 2024 10:38:52 GMT  
		Size: 805.4 KB (805405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:c5215e6fdd01374b89137087dd2d170b77465c4c4e719e6b308960944b8cbd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23233738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240938e14301729326ff4071d74f7177c6d204a5e91efd4e2f1c125bde26e1ce`

```dockerfile
```

-	Layers:
	-	`sha256:8b6b01f5d7695c5841719a47804737da35a358457d1490c0cdf6f9bfb801d4ab`  
		Last Modified: Tue, 02 Jul 2024 10:38:50 GMT  
		Size: 23.2 MB (23214343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7083a9b77ec62e0e4b1ccab8dd6a089db3c4ca249989d993cc18905b1f338d0c`  
		Last Modified: Tue, 02 Jul 2024 10:38:49 GMT  
		Size: 19.4 KB (19395 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:fe26971df91955d05cd5ce07c17a68a5bf64741006b3f4e6e4487de455574d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599418608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49e31d8651a15795f12ea53a9ea09c905db31b0aa8fa9f5e7fa00183ef914eb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff6c9a28c036769727a4cf9dbe067b96273c0352a50922f6e950491245fc03`  
		Last Modified: Tue, 02 Jul 2024 01:14:24 GMT  
		Size: 66.0 MB (65988734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d78d8993f755e32d16bdd9d852de52b88366b9799e3015e185a4a9b88f991`  
		Last Modified: Tue, 02 Jul 2024 01:15:11 GMT  
		Size: 210.1 MB (210139446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de756d6e190115de64eff58796f041360f770368cdd451d77d35b73ff135fc5`  
		Last Modified: Tue, 02 Jul 2024 03:14:40 GMT  
		Size: 246.8 MB (246820210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91d5436633a0eda02d350defa9fa96d299d13fae625953e3e2b45f5abc9099d`  
		Last Modified: Tue, 02 Jul 2024 03:14:34 GMT  
		Size: 195.4 KB (195372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884c43e2c4ea8f357d396a503aff1615c6c936fb6232059d7ab856d93cf87816`  
		Last Modified: Tue, 02 Jul 2024 03:14:34 GMT  
		Size: 805.4 KB (805407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:23a101c239b8aadb30a2c06f8349ea0e7c74af09d37742d233b578efa616b97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23161687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee8f198578f04fbe5079f26d908457fbec57b6ab660ec81279d479f38bf6d8f`

```dockerfile
```

-	Layers:
	-	`sha256:04074dcbe0cf8e7577dc31edf2f17bf8ac629c326a787d4dce43f4a478372d77`  
		Last Modified: Tue, 02 Jul 2024 03:14:35 GMT  
		Size: 23.1 MB (23142654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e7048cfcc36d3d7e19fa11d3f0c9ca2bf3d54a479d2169c21fb86b3d838c34`  
		Last Modified: Tue, 02 Jul 2024 03:14:34 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:af148efffb57081d7bd09c9b35d8d26b21474fe21d9131ed649dad7bb2148148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552424462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90a50132bea542ab04bd05d581cc365cff0afd4ac17e61af24686aa6b8859a8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:c1871631a2828ac765a04bc2cf8d2d9709cd81730d4ce46e403f4d0dbeff9dbb in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:6cf4285917f60eb7d02ed62b32504e18b0ca84bfd90c36a0b39f6eb520741b6a`  
		Last Modified: Thu, 13 Jun 2024 01:21:11 GMT  
		Size: 49.6 MB (49582735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc1137b694767cc0d09b98cc14d61f1a91b811b596506348d0673d092435b4`  
		Last Modified: Thu, 13 Jun 2024 02:36:03 GMT  
		Size: 23.4 MB (23438130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1c3c99bf43fc1ee7e418fa6f18cd0021306408228bbe2acf6511535380acad`  
		Last Modified: Thu, 13 Jun 2024 02:36:56 GMT  
		Size: 63.0 MB (62968443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fa6ba322c491003c606d39495f780d3353477768a903cb773ce91522ead7b`  
		Last Modified: Thu, 13 Jun 2024 02:39:05 GMT  
		Size: 189.8 MB (189770239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187d48a40759d122c1df05cd92ee1b4264f6dd46450fd17b951706b584414aa`  
		Last Modified: Thu, 13 Jun 2024 19:20:01 GMT  
		Size: 225.7 MB (225664121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a38dcd38057b95f5f72b1ee98c888dec4b608ea7674852df1e029b9d300aeba`  
		Last Modified: Thu, 13 Jun 2024 19:19:44 GMT  
		Size: 195.4 KB (195389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e46988c28bb69901ca0490173db77448aef28afee82efdd7c1c41722059ed`  
		Last Modified: Thu, 13 Jun 2024 19:19:45 GMT  
		Size: 805.4 KB (805405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:9122910a1df5648d930e3a58d468d746e3a1fd4a93ca989a571e8446466635e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7da69ab53b08a411700b1bf0f436224cf3f640bd124068cfdc042166e9823e`

```dockerfile
```

-	Layers:
	-	`sha256:6443081c19b56d2093974fe5563277a1ed9b238498e9ac087e76ff9b0282daa2`  
		Last Modified: Thu, 13 Jun 2024 19:19:36 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:185c6c7cf3bde555e5bb978e971ffae50d11636aac1c0ae4904bcb9c21f2feba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.8 MB (613764672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad6ff725c7b4e7f69be0226d1cba0507bf9e17cd32dca90de14ff1fed322efc`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf317c43d118e9cf38efabf9b1e93b406add8c26e307fde367e39a47a1c5821`  
		Last Modified: Tue, 02 Jul 2024 02:04:25 GMT  
		Size: 25.7 MB (25695092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f1c93d43f65ddb5b49fa7540ab263862ed9868139cb0bfc51bd8dffe47f60`  
		Last Modified: Tue, 02 Jul 2024 02:04:48 GMT  
		Size: 69.6 MB (69582302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851398057330b42908d94c58bef25257d4970fa040c693d176d2cf32992a715`  
		Last Modified: Tue, 02 Jul 2024 02:05:34 GMT  
		Size: 214.3 MB (214252411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5731a72fe8999744ccc751edb5bf9dc9486ff72b90cf60f1b79d886bc5303641`  
		Last Modified: Tue, 02 Jul 2024 07:25:10 GMT  
		Size: 249.7 MB (249677089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0f395855b5267cae84404ea7f43343e385a72b6a05745d846874ecc73d8034`  
		Last Modified: Tue, 02 Jul 2024 07:24:47 GMT  
		Size: 195.4 KB (195356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a296d11925f44c37304a594dbbe29e29a8dd66c956ffb8ba9b8f901d57ad30b2`  
		Last Modified: Tue, 02 Jul 2024 07:24:48 GMT  
		Size: 805.4 KB (805407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:134427b9dc0f11357cfdc30141d999ad16a122849eeded8e0e924d5743356c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23149353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f094f2537b8ba8dd529626190ad7b9edb67f72056640e399ab2c8dca40bc415`

```dockerfile
```

-	Layers:
	-	`sha256:214d474122bf4456412d7c0c19474d4e79b69e2773502c919064b8e9cae71558`  
		Last Modified: Tue, 02 Jul 2024 07:24:45 GMT  
		Size: 23.1 MB (23130235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f95ce4ca69a161dc225cd468112eb9fcdd7c19576dff454f06c4b4a5084a230`  
		Last Modified: Tue, 02 Jul 2024 07:24:43 GMT  
		Size: 19.1 KB (19118 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:b5927a6f1a58d1271b075b2546a2c0b410d680c26bb7c6b66b147d36ef7ee56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.5 MB (557503044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bea55575ae119358ab4481dd60156362f80f492d1a38bacbc922b81b1fe727`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 May 2024 09:03:56 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Wed, 22 May 2024 09:03:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 09:03:56 GMT
ENV OTP_VERSION=27.0 REBAR3_VERSION=3.23.0
# Wed, 22 May 2024 09:03:56 GMT
LABEL org.opencontainers.image.version=27.0
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5c8ad9143ee81c26aae4699c4bc64f76c5e838efb778f988ad9bb1305f505fed" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 09:03:56 GMT
CMD ["erl"]
# Wed, 22 May 2024 09:03:56 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 22 May 2024 09:03:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457fb781c30f5a251f0251b0cafc815abfed65652bdecac052b60618b497a23`  
		Last Modified: Tue, 02 Jul 2024 03:45:17 GMT  
		Size: 183.3 MB (183253702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a2c80638b04dae4a0f02eaee30412cf7d7755ae076940a727f51515cc9da2`  
		Last Modified: Tue, 02 Jul 2024 11:40:50 GMT  
		Size: 238.1 MB (238142981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9909560b0e5eafb21291e5c05857b7d31b857c3c5f4a2816343742bc6c2179d`  
		Last Modified: Tue, 02 Jul 2024 11:40:47 GMT  
		Size: 195.4 KB (195397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbea2339f4dd3f134a5f0cb974e6448977264adf702cc6392169c5c825216fb6`  
		Last Modified: Tue, 02 Jul 2024 11:40:47 GMT  
		Size: 805.4 KB (805403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:3685dc594b6a180de357799b30dda9aa489e146f0c5b060153e728d61efcca79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22969687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e268cb377c980982cc3f3aff6eca93758878ebbed3fb46bbfcfed109ec9da6a1`

```dockerfile
```

-	Layers:
	-	`sha256:b3dc6ccda4248d28cca45c8d63a050de79c94f4cc13f1de78a9e29d6aa219b15`  
		Last Modified: Tue, 02 Jul 2024 11:40:45 GMT  
		Size: 23.0 MB (22950617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56ba819f44f0d4cc6c94b9ba90bbadbfe685164b42d067939aa2723fedab6eb`  
		Last Modified: Tue, 02 Jul 2024 11:40:44 GMT  
		Size: 19.1 KB (19070 bytes)  
		MIME: application/vnd.in-toto+json
