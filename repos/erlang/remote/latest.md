## `erlang:latest`

```console
$ docker pull erlang@sha256:fe76a954cb39bb50999518c382d8aafb99ec1b51c260f75c9c6b8a4454edc407
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
$ docker pull erlang@sha256:542ee9138439a5d1efd6cd29ff2f35f4cc7f5508f7fcf54a3490a51bd597d59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624227739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7d154a9b247ee8a5550a1ddb7446ebb9e77ce9b658f3158c0c921210aeeb17`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3556d62e9bd977c17e315ad64979017739fd90fc5a2a89ec07cf82348133f3`  
		Last Modified: Tue, 21 Oct 2025 10:21:00 GMT  
		Size: 211.4 MB (211449932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1934660aca138da18a97791e2bd345f9d2a555c1f16bbcb554cd529dfda8a5a6`  
		Last Modified: Tue, 21 Oct 2025 14:01:49 GMT  
		Size: 274.9 MB (274862688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306b479d81e5547335a6411c4f5b564600440c75ecf8402409c165bb8fe7671`  
		Last Modified: Tue, 21 Oct 2025 11:16:54 GMT  
		Size: 191.5 KB (191471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e054af339e3d782547b4caa41d1ebbc07e9db6690244cf0fa01056fbece05aa`  
		Last Modified: Tue, 21 Oct 2025 11:16:54 GMT  
		Size: 817.8 KB (817782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:1efb8669baaca4d1ef0e31266afeee03316807b229bac4663499e201d18ab2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23956727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1344da1e246bb21404d06cda0d4959572d7abf5ebd67f6529ffc33d8d144baea`

```dockerfile
```

-	Layers:
	-	`sha256:b7e68d7c628970b0092ce109257e42e3cb58ef736b31ff97da5881cc3d4629c1`  
		Last Modified: Tue, 21 Oct 2025 13:47:50 GMT  
		Size: 23.9 MB (23937454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff35ea13e11308c970789b4b6afa97b37ca5915e3c449c2a0bcfb59897198b9b`  
		Last Modified: Tue, 21 Oct 2025 13:47:52 GMT  
		Size: 19.3 KB (19273 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:ec443a64e636f70867023296060ee7d7216e68a100c868be917e25b9fdee9fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564071817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23865a3955616df024454fab6849f5e71e3315b933f6ab7e439bc938f8aaea31`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:27:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:51:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:13:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:16:27 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 04:16:27 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 04:16:27 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:16:27 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 04:16:27 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 04 Nov 2025 04:16:31 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 04 Nov 2025 04:16:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68533da42b7795728d851e519aa05d6a90a43ea0bd8e6cf63e7cd6acc86ac61f`  
		Last Modified: Tue, 04 Nov 2025 01:28:06 GMT  
		Size: 22.7 MB (22705759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15672bb6096ab5577e4b18af07dd846508a657cffbc1c2eab8f3e8e8739f219`  
		Last Modified: Tue, 04 Nov 2025 02:51:46 GMT  
		Size: 62.0 MB (62010557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527558cff34568b9c24e4fd3688a1f5acb58cebdac3ed3283eb10fbfaff9c5ba`  
		Last Modified: Tue, 04 Nov 2025 04:13:27 GMT  
		Size: 184.7 MB (184698770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc75d39e9a97f74dfa1266390545d85eb994f1f48db319f25ed5a4670207cc27`  
		Last Modified: Tue, 04 Nov 2025 04:17:51 GMT  
		Size: 247.6 MB (247631396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41933ef580c6449e861c64ff32f701eb9bf8739a1ec26a00c19e507ecb1ce330`  
		Last Modified: Tue, 04 Nov 2025 04:17:56 GMT  
		Size: 191.5 KB (191469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a7c0863056bdb2062e6bff681aa2a9d29260cee40ff1bf087f512699a43f7a`  
		Last Modified: Tue, 04 Nov 2025 04:17:56 GMT  
		Size: 817.8 KB (817777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:34a76b2fdeaaff08ed2f3ba1eef1cfc983ef7c650228af33ac9b85f109dc2b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23583775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83927bbfaf0c370c642297a2f5fdce78d830daa1580962c21ced6f4f68bd6c2`

```dockerfile
```

-	Layers:
	-	`sha256:d2ad31ba9e37462c390ccf78731f98f76ead59847f276b54566aa0a191c5b338`  
		Last Modified: Tue, 04 Nov 2025 08:48:15 GMT  
		Size: 23.6 MB (23564432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff02df361ebe9e26355287e517159e9ba2c34ed90c727385822b29cd7a453aed`  
		Last Modified: Tue, 04 Nov 2025 08:48:16 GMT  
		Size: 19.3 KB (19343 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:6495b597397038f8b9974391c2c90f368ff4e2dfc36fe437711211e0ec10c546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546367535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9721823d4679fbdcee1877e654a1d72db69a74e62bec1e9919415eb05a830`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ee829bdf75912a6b5b2d40a231e18620480fb354b21357e9a9fd92bb656614`  
		Last Modified: Tue, 21 Oct 2025 09:59:13 GMT  
		Size: 244.2 MB (244220170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deab2efb2eb0859a5efe024ac8e99ea3126a889c2668c8b19b6742704bcdf117`  
		Last Modified: Tue, 21 Oct 2025 06:21:19 GMT  
		Size: 191.5 KB (191477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7b08a586dd02513b0359a54c9f721b7c9b83f843e740848b624c86a57ebe8`  
		Last Modified: Tue, 21 Oct 2025 06:21:19 GMT  
		Size: 817.8 KB (817778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:449e704e2645f93a66f8b0b1e9998530f90deb707631b885104e66382773d177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23769912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba30b1842e1773d17e3f0bf8b193a9dcd3be08cdd3add94ad91f8f87f08e66`

```dockerfile
```

-	Layers:
	-	`sha256:d3978d8554e14b16b0b50936a68710e5a23371b3dc225f1544403eaaafbac033`  
		Last Modified: Tue, 21 Oct 2025 10:00:28 GMT  
		Size: 23.8 MB (23750526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:674f3ca1354c7f0ccf7a32c3f5ed827a0d86cc40b9150d5afe90240f87d43428`  
		Last Modified: Tue, 21 Oct 2025 10:00:30 GMT  
		Size: 19.4 KB (19386 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:5bff3c77c988c44791fb942f5cee9b4fcd4973119f2af4e8a4f34f1b26775d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.7 MB (607710941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c0f0a3c47e8496789f029f87faef8fc8bf44e239613c43f6cb00dc0613743e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453de5e943a750a504edb8db0f901402e425539144fcc432cb4b8bf32053cd8d`  
		Last Modified: Tue, 21 Oct 2025 05:15:23 GMT  
		Size: 267.4 MB (267415087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d2518ad150affcbbf208ddb92f8d28b19346198d80c9d6edc6d144d6aa7b9`  
		Last Modified: Tue, 21 Oct 2025 04:17:15 GMT  
		Size: 191.5 KB (191470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91211e582156a7a4cfc9a50301a658fc86dea368b5c07f285abb7056380861d`  
		Last Modified: Tue, 21 Oct 2025 04:17:15 GMT  
		Size: 817.8 KB (817782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:08ab4f11c2f9cb29615de66542a806b7fd205906d84c72e10241fc45afe4d0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23996372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b240e9def82e96c31c81f76280696343317d02656d592d776027ce612b7d63d`

```dockerfile
```

-	Layers:
	-	`sha256:e022072eeba649cba26a71c28ffaeb33e3ff43d617b7c913263baff6f55cca7c`  
		Last Modified: Tue, 21 Oct 2025 10:00:26 GMT  
		Size: 24.0 MB (23976953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6e59c74f2c9f9744a937d6f478044469a6f6fe257f484647366a4276199e589`  
		Last Modified: Tue, 21 Oct 2025 10:00:27 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:554fc13d1640581cbef6caff145aa9548c905d273a55921a55a5cca44fbcf9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.8 MB (624828387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808310d2cfd6821e0cf4dd21368d16a77a053ffacbb777c3d56bca970ae2d4d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad810b562fb36185c6eda304efa20acbab6f6e75bc1f4d59ee030d724a5477a`  
		Last Modified: Tue, 21 Oct 2025 05:14:49 GMT  
		Size: 272.9 MB (272875057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf2428ecb919b081ec7464edb03b0e3c2937c26375830fa0b177c168bb9aeb2`  
		Last Modified: Tue, 21 Oct 2025 04:17:21 GMT  
		Size: 191.5 KB (191473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e7237cd66c377dc424c0a2b66d76ffda8c7887cbf6d6d4dc133287ebf009d`  
		Last Modified: Tue, 21 Oct 2025 04:17:22 GMT  
		Size: 817.8 KB (817782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:b81d0f3c7f01cccd341b5ace85055ed77418522c0d1d93e44a9b83a2e0ce3ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23924297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f818464b415e5cf95cc41a2dff3d2f2f404a6772ce9e293fce6cc873404bbbb1`

```dockerfile
```

-	Layers:
	-	`sha256:5c963102a90aff4d3156165e19013508a7df39e2e572f6700014c73e0de432bf`  
		Last Modified: Tue, 21 Oct 2025 10:00:28 GMT  
		Size: 23.9 MB (23905065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37e558d087cb6540a51ad4cdbf2a033670b851abfbc7766b5b4a584faf5b16c`  
		Last Modified: Tue, 21 Oct 2025 10:00:29 GMT  
		Size: 19.2 KB (19232 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:5facfdf33053866642d23fa1329c999e2ea73afec642d740c0ccf2d14f6254f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580825910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b76291398d2ab8dc9d9b4bf8d1405b01b837a79a33d893247477fd683acbae`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814bc6bdb04fa99c9a89fc3a90aaa9ea2da7c62e2933ad85bf543e1690ab23cb`  
		Last Modified: Wed, 22 Oct 2025 01:21:38 GMT  
		Size: 190.2 MB (190221174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa2e4f92b85b1268a996c7f97476a29f6ff77b03fbc424ff60d53a012412ae0`  
		Last Modified: Wed, 22 Oct 2025 04:51:42 GMT  
		Size: 253.9 MB (253911501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8547c2a57fa73aed204519546a282313d420c3c33e5469c9d6c1e1cc5da3de52`  
		Last Modified: Wed, 22 Oct 2025 01:50:33 GMT  
		Size: 191.5 KB (191491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9fd0f26ef92fe40da7853a2d73c1a37d06e844730e85c74702f998f0c16d49`  
		Last Modified: Wed, 22 Oct 2025 01:50:35 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:cf89c9d4a8ad936c1cda6c619d19461273b4464b25b428c194e0849885b689a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b627a53957666c0752791b2e11352b0ed7a894f771c544970f02c361b18604`

```dockerfile
```

-	Layers:
	-	`sha256:c958b62a98187b4b6f81ef77a08377c32bea2ab6b6469d35b8240195778a1a33`  
		Last Modified: Wed, 22 Oct 2025 04:48:58 GMT  
		Size: 19.1 KB (19138 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:b6176866f28739001e5b5b949ffdfce78baffe54c534a22056041b7eab1a769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.2 MB (632210563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde9a3f235014b78bfcd50949d4ffe8222cd6c446abe882a898068430e4cece5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56011ccaf4727bb2311ac874db524178647f03b759d374824a9593362ec2964a`  
		Last Modified: Wed, 22 Oct 2025 01:54:45 GMT  
		Size: 214.5 MB (214489889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfabcfaa00da8f24b36f6c8058b9566acd0c346363c81c2612b5b57cc7b2b9b`  
		Last Modified: Wed, 22 Oct 2025 15:50:03 GMT  
		Size: 268.9 MB (268866887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c942f877aa208b5b2f8a05dd4da754e2f3073f0838c22ac7138401a7a0d363ed`  
		Last Modified: Wed, 22 Oct 2025 00:49:44 GMT  
		Size: 191.5 KB (191464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f1e1171cef80711c2d8aff3103a47413737a780d14258c78977ac014de7239`  
		Last Modified: Wed, 22 Oct 2025 00:49:48 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:206d2b33fe05d461e23a798cc3af78b593fd07dbb64c5145b8eb81629e4578a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23912471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fef7828fcfd556d46800dec207316065f7476efbe3b49cb8841e0d51df16b48`

```dockerfile
```

-	Layers:
	-	`sha256:9142cc534e03e1c858424324a89483454ddd62ff43fd7bd9dd46e847afcc4fc3`  
		Last Modified: Wed, 22 Oct 2025 01:48:50 GMT  
		Size: 23.9 MB (23893145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a60350c31c809cc9d901372e4a2a3733815f64526841261e4e1099d4ba0a6a`  
		Last Modified: Wed, 22 Oct 2025 01:48:51 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:a0aa07cfad98028f5703dd95443bb07d69a5e0ed1b709778eb41a49db3e8a6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (585046554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ee4ba64a29d613926c2f9b484de5f57dd5b7ecff819dca6dfa4d7fdd8d470a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Wed, 17 Sep 2025 16:00:47 GMT
LABEL org.opencontainers.image.version=28.1
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
CMD ["erl"]
# Wed, 17 Sep 2025 16:00:47 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Wed, 17 Sep 2025 16:00:47 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7808a3d44a40cd9c7ef8c2dce3527722614147355beb2517b49a1ef026a6c988`  
		Last Modified: Thu, 23 Oct 2025 00:50:32 GMT  
		Size: 265.9 MB (265885806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d95fe8cef573b73caa92a438280252b4ba165657611849fc009bf23cadc98e2`  
		Last Modified: Wed, 22 Oct 2025 14:19:14 GMT  
		Size: 191.5 KB (191460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa1a47b31543344a50cc2678145a3027e10523edc5b4697c82e61d1341cc2cc`  
		Last Modified: Wed, 22 Oct 2025 14:19:14 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:226baeb596bbb03d4852e3ca28f673c7d51f9a681f06a55362b259020da30cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23724163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65dee60d569319649adbf9fd0ae9b4a3f9f6fb3c131e22ed1ac10471e54a2ea`

```dockerfile
```

-	Layers:
	-	`sha256:23fa6acea72c777d8520a9149b23b5ea9a965422daf82d153c6b1bd08dc7cec5`  
		Last Modified: Wed, 22 Oct 2025 16:49:40 GMT  
		Size: 23.7 MB (23704890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929abc12bc701828fb54a4032676d991b1bcf25223dfab25e5fabaa97e5e82fc`  
		Last Modified: Wed, 22 Oct 2025 16:49:41 GMT  
		Size: 19.3 KB (19273 bytes)  
		MIME: application/vnd.in-toto+json
