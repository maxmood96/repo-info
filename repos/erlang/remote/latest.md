## `erlang:latest`

```console
$ docker pull erlang@sha256:08ef97a6371040a368629d126222aab01f11829489b5b43ccfb0ed3a613030d3
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
$ docker pull erlang@sha256:4e6ea8d1fd5867bbb8ec9fa0e71d8f2f3c45581fb50478122892a9e6617ed437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.2 MB (623246153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38db8f6bd0220201b6d5b804271fc9c98f8a42b1f4d81d6a1e21d2394e001655`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:42:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 11:02:16 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 11:02:16 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 11:02:16 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 11:02:16 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 11:02:16 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 04 Nov 2025 11:02:18 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 04 Nov 2025 11:02:30 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32885a2b0a589e832bf6b250bd35a528b268360f166af2cd7094d3a14993fcc1`  
		Last Modified: Tue, 04 Nov 2025 11:00:07 GMT  
		Size: 211.4 MB (211449144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3080179f984da4ddbeec16a7da1967d602c10ad55ca0420db4faf914fe773894`  
		Last Modified: Tue, 04 Nov 2025 11:53:32 GMT  
		Size: 273.9 MB (273881322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33978f91598f3be47ad629a1ad185aea8ee5e32be7a89f8fc884ed411735c`  
		Last Modified: Tue, 04 Nov 2025 11:03:33 GMT  
		Size: 191.4 KB (191403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e217248b4278ec9f40bd4e991ac02033a38ee90ee5d6ff5de50181e9d411d42`  
		Last Modified: Tue, 04 Nov 2025 11:03:33 GMT  
		Size: 817.8 KB (817782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:166f86869c69cf550ca449a9d1795343263008cd51417c051d631397aabebabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23787567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacf2897cbac99c5b23900e17f94a7f2701d963115de9a08db89d417686ed7d4`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f16e828003c0c5da9b52fd7cac1eede321d92d0a935d90b3793ea7c9047dd`  
		Last Modified: Tue, 04 Nov 2025 11:49:48 GMT  
		Size: 23.8 MB (23768337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa0d0a25cfd38e41941f8ed3b593ebae293a8cd4c3fcdd09c6ccd6d344f8a7c`  
		Last Modified: Tue, 04 Nov 2025 11:49:48 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:e486c44813ba757c0bd7a720e810c59f73eecaf28dc276ec9dee09088400a9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564094509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc06728456163f53a1c4e024f11ed76d33bbd7d41a3290ccf8b1d5bf5430a0a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:08:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:31:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:18:52 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 06:18:52 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 06:18:52 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:18:52 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 06:18:52 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 06:18:56 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 06:19:21 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad589659a3ab8a5efe8198e1ee9fa790fcf26937e030eba01738a074b5c099d7`  
		Last Modified: Tue, 18 Nov 2025 03:26:40 GMT  
		Size: 22.7 MB (22705754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cea8ca5112d5f4a4132c63005a6f1e78659fc63451a1196b67118980c547043`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 62.0 MB (62010365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210961f9b574abcfe9702b905c1bf12316e51e21c042b864c526a6c2d186bef6`  
		Last Modified: Tue, 18 Nov 2025 06:15:53 GMT  
		Size: 184.7 MB (184720670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228058df1dca769f38c7c19b2bee08548dd9be9f20dfb04b1fa5e88fc37361c`  
		Last Modified: Tue, 18 Nov 2025 06:20:15 GMT  
		Size: 247.6 MB (247632634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b9533c632e5f4b6bf2c2b6c3faca57c8b0a9055b53d281542b0e235472365a`  
		Last Modified: Tue, 18 Nov 2025 06:20:20 GMT  
		Size: 191.5 KB (191472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f86ef822ba3f65abbae015c65903e0172963b06916af3bd2839195a725c744`  
		Last Modified: Tue, 18 Nov 2025 06:20:20 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:152dc84b6389a4d125ec223cf97da4cc0e882c2dbb716a364f8dafc1a8712967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23583775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6a45f560e993817652122f150fd17824c9aac7b7a04528cca00e0093378dd8`

```dockerfile
```

-	Layers:
	-	`sha256:f3ce4febfece9a66ebf12ae0add72c057b1d17cba83accbc5a96d02dc45542b7`  
		Last Modified: Tue, 18 Nov 2025 08:49:29 GMT  
		Size: 23.6 MB (23564432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116dedeb9f3f8250ae197fc7adc118cdacc569245fd441370c57c1fef0dcca9e`  
		Last Modified: Tue, 18 Nov 2025 08:49:30 GMT  
		Size: 19.3 KB (19343 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4ccac56cba6aa443ba55f659a42d93d198e5d071e74380a2c1bf24330e3581af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.8 MB (545792982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414b16dd4be6debee7968937ba5a06aca9831ccd39d5463814316a550600bdeb`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:37:02 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:37:02 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 07:37:02 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:37:02 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:37:02 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:37:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:37:29 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
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
	-	`sha256:763c60a84d79927366aa864d13912e03abfa87dd07e0e97efbc3258c376daf46`  
		Last Modified: Tue, 18 Nov 2025 08:47:26 GMT  
		Size: 243.6 MB (243630308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db25628217b901d3559858312778daddc5b74438761fa1cd7929e674b45a4b`  
		Last Modified: Tue, 18 Nov 2025 07:38:29 GMT  
		Size: 191.5 KB (191462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06acbc61f6a73082a044f133f65a779f89515ce5852355ea04953c7a8a00ccf6`  
		Last Modified: Tue, 18 Nov 2025 07:38:29 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:8bd13f07cdb3e43507aea052d3c2267ed561cfd5f6f58af1e754902c2733141e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23600662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36110542b04ecc77cf54e7c3457ce2ca2c5657771ce426fb4ec8969bfab2f1c`

```dockerfile
```

-	Layers:
	-	`sha256:a4388f07a774d9f14ee6389375118a455f4fa1c65a1af5f656d35a45fc7e2702`  
		Last Modified: Tue, 18 Nov 2025 08:49:52 GMT  
		Size: 23.6 MB (23581319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2defd3f5111d5634b322952b596588a256f250f282832e250b44352604d898f7`  
		Last Modified: Tue, 18 Nov 2025 08:49:53 GMT  
		Size: 19.3 KB (19343 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:428a6fdb5bbc72f9a74281d60cef01e3fe3a9ba2cbc7b8901b7218812a504620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.3 MB (607291911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906540620cf6021f2daa303f05e52344e1d6b8dd0b3faf54501b946c9ee99879`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:17:29 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 07:17:29 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 07:17:29 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:17:29 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 07:17:29 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 07:17:31 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 07:17:43 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
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
	-	`sha256:3cc397a281dfee2b41ae94d1334e003930ab54208846c1967440581bee2d42c2`  
		Last Modified: Tue, 18 Nov 2025 08:24:08 GMT  
		Size: 267.0 MB (266973584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a68cc2404d165c4871eb2288978c67611adb1487eaa1ede29abd193792ac0b`  
		Last Modified: Tue, 18 Nov 2025 07:19:03 GMT  
		Size: 191.5 KB (191480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38c2f6d98f42817ab0e3f3362bb8dbd0c2787354e5f265381d51c75b15a6e9`  
		Last Modified: Tue, 18 Nov 2025 07:19:03 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:3c63e76bcb4460cf600962275c49f04c6cdbcaeb40bed6473b003dc7ca966ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23827182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c46cce7b2f3d1cc8af02c3eddb7f65972ad193da83d91514be7c3ee861a5f9`

```dockerfile
```

-	Layers:
	-	`sha256:4ff2b4229bf07ff29b34739afad22c664482f9978832e68795b1f8e34e390f5e`  
		Last Modified: Tue, 18 Nov 2025 08:50:16 GMT  
		Size: 23.8 MB (23807806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d0868db3a97b38ceab10246f7acb0fc3f983656deca206d1dcecd76929a28f`  
		Last Modified: Tue, 18 Nov 2025 08:50:17 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:51616f29daca58c4afee395ec353ba5945dabb9ea65c9c5ea4a450822d03f0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616558548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99a0bc989faedc63269e28ff4a87a652cf0bc232db18d7d39f3886d05b41226`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:40 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 18 Nov 2025 06:21:40 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 18 Nov 2025 06:21:40 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:40 GMT
CMD ["erl"]
# Tue, 18 Nov 2025 06:21:40 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 18 Nov 2025 06:21:44 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 18 Nov 2025 06:22:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
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
	-	`sha256:3e320cecd74ad9765a1c02e120781d09262bf98ed6c97b49f3e13068026d2ebd`  
		Last Modified: Tue, 18 Nov 2025 07:18:27 GMT  
		Size: 264.6 MB (264594755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51657751a5820e1aa9432cb72fa8bae9a2bc30070ebb9b7228d4480d4bbebccd`  
		Last Modified: Tue, 18 Nov 2025 06:23:28 GMT  
		Size: 191.5 KB (191473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06be9e86c3b6ba4dfecf3b7934caafcec41fc82e40e7fd81065291760754c353`  
		Last Modified: Tue, 18 Nov 2025 06:23:28 GMT  
		Size: 817.8 KB (817783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:3257572ced923911a3bb4db03e88b9e3f301e736eb7a938dad10f7b328ec80af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23755197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a68dae68e168ee7b881ede5fd95adb4f80497f9f8e3fa3476a56241d6f5a883`

```dockerfile
```

-	Layers:
	-	`sha256:925ccd74458947ca30a7cc43a08c31ea5da72ecffe7aaebf03a99886a152fca6`  
		Last Modified: Tue, 18 Nov 2025 08:50:37 GMT  
		Size: 23.7 MB (23736008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bdc4f4029e6d79fe2c6f0c6f53aed6694e0181242ce2743d94d3eed4092996d`  
		Last Modified: Tue, 18 Nov 2025 08:50:39 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:56282142fed8a29f6aed9d6dfe629848099a5270d2a2635f068c4e46057da1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580228876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac6932e3f585389f6b2c3e24db9120b73bb73efda8d535daf576f236789d784`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 14:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 20:46:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 21:28:31 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 21:28:31 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 21:28:31 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 21:28:31 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 21:28:31 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 04 Nov 2025 21:28:49 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 04 Nov 2025 21:30:36 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6492253d4f5d673ee74abc9e254c218714a0737c4c244dcc729821fb543170`  
		Last Modified: Tue, 04 Nov 2025 14:04:51 GMT  
		Size: 23.6 MB (23614047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f9457e9c1a9cba16fc581959f009772a1561916f3cc0ea635018606420380`  
		Last Modified: Tue, 04 Nov 2025 19:50:51 GMT  
		Size: 63.3 MB (63309635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9eb3913bde8825e793db29aa7c5df2878a3bba9b4f6440887f5016e06d7ba5`  
		Last Modified: Tue, 04 Nov 2025 23:24:18 GMT  
		Size: 190.2 MB (190221436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c915ec6e16e9645959fad2a34ea9d03a33be5059c99c8bce73becf04dcb4a93`  
		Last Modified: Tue, 04 Nov 2025 23:55:02 GMT  
		Size: 253.3 MB (253313212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836ae182324c72cd8fe454f5d2a6d194c4abaa0adcb04ffa49879f94064d876`  
		Last Modified: Tue, 04 Nov 2025 21:35:27 GMT  
		Size: 191.5 KB (191486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09db9478659c40eeefc5ce646e27f61248dd8daa5b573853579c9705b191c20`  
		Last Modified: Tue, 04 Nov 2025 21:35:27 GMT  
		Size: 817.8 KB (817778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:c49ba5f82b2f4e640cdf9049575b4791f2597855dab02ea62f853789bf352660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46ce6ad1a8be730073d297df5722043ddce2f966d872b4a5fa1b1533e5a8a`

```dockerfile
```

-	Layers:
	-	`sha256:cb8a51303efb15a00dd1e2cc50985ad0982134ccff9cd839730006fa2474fee0`  
		Last Modified: Tue, 04 Nov 2025 23:49:23 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:54a570b3cf34f8645b44c54a36969e1df8790b7108588083ba166a37511ba7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.2 MB (631153922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35a9bae2494631e4311f156642e8301a891f15bed6add2fd2ce984301ba57fa`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 15:56:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 21:00:20 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 21:00:20 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 21:00:20 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 21:00:20 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 21:00:20 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 04 Nov 2025 21:00:30 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 04 Nov 2025 21:01:14 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f89c76b3026966e039b432e1b66b1655c47c97f236438dc626e5acdead5cd`  
		Last Modified: Tue, 04 Nov 2025 06:25:48 GMT  
		Size: 69.8 MB (69845633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f0e7cc6342b205315477b4f74b07996864bd807c6f201a08b5c8eade6e78b3`  
		Last Modified: Tue, 04 Nov 2025 21:08:53 GMT  
		Size: 214.5 MB (214488491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b467b8e0b4644f056e730b636f7ec72519979d2f56c3ff7f59bfa52b84df574`  
		Last Modified: Wed, 05 Nov 2025 10:17:05 GMT  
		Size: 267.8 MB (267811243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60434e1fb91881b853ce0f32c0d63166f21b2dfcd63f0a63ff1f4fe1e2938022`  
		Last Modified: Tue, 04 Nov 2025 21:04:22 GMT  
		Size: 191.4 KB (191441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59eb159851fdcdf29f9161c42de5e79e58dbb90c7659d727b81e45183c0370f`  
		Last Modified: Tue, 04 Nov 2025 21:04:22 GMT  
		Size: 817.8 KB (817780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:4a9d0e62050894903efbd12aa243c6ca6c3f6cbd19548c9ff7d909cbb5104bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23743118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4667c49b5b5ed99d9a7b2a6d8d98c00d4e8ab214c3e4a07e6608f94ecd90068a`

```dockerfile
```

-	Layers:
	-	`sha256:1ccca4ec0309ed5ac1701e213672991c49b89b4f5394ad1d1f51fcd70a295978`  
		Last Modified: Tue, 04 Nov 2025 23:49:28 GMT  
		Size: 23.7 MB (23723834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acfc646643a2f5af2d39a57998f1f77cc47798e76e9df3476857b334de7bb82`  
		Last Modified: Tue, 04 Nov 2025 23:49:29 GMT  
		Size: 19.3 KB (19284 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:4448b092bf96714150244a5443145af146c53c321e6fd47d62eb2f518e213bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584377706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5cb5ac429589f858bb0d37188f105ec6c7e2904657cec580ce7cf49f83e783`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 14:48:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 17:34:23 GMT
ENV OTP_VERSION=28.1 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=28.1
# Tue, 04 Nov 2025 17:34:23 GMT
RUN set -xe   && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c7c6fe06a3bf0031187d4cb10d30e11de119b38bdba7cd277898f75d53bdb218" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.2 			libwxgtk-webview3.2-dev  ' 	&& buildDeps='unixodbc-dev 			libsctp-dev ' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 17:34:23 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 17:34:23 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 04 Nov 2025 17:34:27 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src # buildkit
# Tue, 04 Nov 2025 17:34:50 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src # buildkit
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba91dbdb50f511980482385b36987be0332dae93638fc6697a70724b1e1e5c`  
		Last Modified: Tue, 04 Nov 2025 10:00:10 GMT  
		Size: 63.5 MB (63501365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc565eecd26183b68234b15cb17e94e12603da93fdeff2a94c4aaa1119d477c7`  
		Last Modified: Tue, 04 Nov 2025 20:54:35 GMT  
		Size: 183.5 MB (183482548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842770144e11a7ba1c7b5e8d40eefca1a8055ab47c067aa7a53b6b3bf5a41e53`  
		Last Modified: Tue, 04 Nov 2025 22:10:42 GMT  
		Size: 265.2 MB (265219036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856700d2d5aa300a25aa180dd1e442f8a5f23a3224134b06959ebc4e93663753`  
		Last Modified: Tue, 04 Nov 2025 17:36:14 GMT  
		Size: 191.5 KB (191469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248e65ffdbe90b4c7131768132729c15b5675ed681a73956e314e57cba4c7530`  
		Last Modified: Tue, 04 Nov 2025 17:36:14 GMT  
		Size: 817.8 KB (817778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:latest` - unknown; unknown

```console
$ docker pull erlang@sha256:6030d3b446b6194e9f94c44d2ce25e9b72e2d3a864120046987aa3bf788da1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23555032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce6adb1ea6d3e9044ac38c7b55cba4ef9a41b72c18c9440c16f952673899cd1`

```dockerfile
```

-	Layers:
	-	`sha256:c0c5868da537e7c6d62247131561b351ab0dc5bef8e38f431249ab76a6f1b42c`  
		Last Modified: Tue, 04 Nov 2025 20:49:17 GMT  
		Size: 23.5 MB (23535803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c57c2377e354573f28f6994de4f0569403f07b6185464c793832a593f89a31`  
		Last Modified: Tue, 04 Nov 2025 20:49:18 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.in-toto+json
