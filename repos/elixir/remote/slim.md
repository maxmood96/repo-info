## `elixir:slim`

```console
$ docker pull elixir@sha256:e5c40abf2b342a39776f9cee442f4b6c322d10c6bfcc9db102c95026a59e2a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:ae9db0692218e12a79c6b376b573ddbb6fda9c3112c1b10a4d34df8a574af038
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118528026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d51f8631c39e99cb5f5a0b8f1abfa099f4a8de61dad64f528def5592a8ca66`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Thu, 19 Nov 2020 07:17:35 GMT
ENV OTP_VERSION=23.1.3
# Thu, 19 Nov 2020 07:17:35 GMT
LABEL org.opencontainers.image.version=23.1.3
# Thu, 19 Nov 2020 07:26:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="291e0852b71ca593f4015417f6e44c08638633c5af6648bd26582c8590390433" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 Nov 2020 07:26:05 GMT
CMD ["erl"]
# Thu, 19 Nov 2020 09:48:20 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 09:50:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 09:50:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0774428185ab0f760e7995e1f7a2afadf3f81e6866f0acc65bfa82da87ae0617`  
		Last Modified: Thu, 19 Nov 2020 07:36:42 GMT  
		Size: 60.6 MB (60645474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12849c7a8cfa5935ec9ccc3e9485b2f6a5b473954923bf4bf2b0402e039718`  
		Last Modified: Thu, 19 Nov 2020 09:53:56 GMT  
		Size: 7.5 MB (7484827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:f8ffae5d376ad8bc5c4ecaf3024682b45916785dd4b0b534973c91e5baf64ac5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109809931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d32cb71be2eeb138afee85d6d9d9d4003d8fd70b58c5415601fde31cebd38`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Thu, 19 Nov 2020 02:31:40 GMT
ENV OTP_VERSION=23.1.3
# Thu, 19 Nov 2020 02:31:41 GMT
LABEL org.opencontainers.image.version=23.1.3
# Thu, 19 Nov 2020 02:38:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="291e0852b71ca593f4015417f6e44c08638633c5af6648bd26582c8590390433" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 Nov 2020 02:38:11 GMT
CMD ["erl"]
# Thu, 19 Nov 2020 03:06:01 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 03:08:32 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:08:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f77803390034df7d300763c6b7a8559f0eafb8f3a4ad2d6b54aae281aa283a`  
		Last Modified: Thu, 19 Nov 2020 02:47:16 GMT  
		Size: 56.5 MB (56457237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984daec99a61af8198e2a45614860674f600aebc53aa9be0a449d6a274e85a55`  
		Last Modified: Thu, 19 Nov 2020 03:13:26 GMT  
		Size: 7.5 MB (7484482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:701ef2b1f2419c7edcb27ce623261500d00d71ebcb830a8a5a10e5a793caac6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114237947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e5ad88aa7103e85609032b016e5ef64ce87331ccec0d586ce912eefec6481b`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Thu, 19 Nov 2020 05:21:44 GMT
ENV OTP_VERSION=23.1.3
# Thu, 19 Nov 2020 05:21:46 GMT
LABEL org.opencontainers.image.version=23.1.3
# Thu, 19 Nov 2020 05:27:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="291e0852b71ca593f4015417f6e44c08638633c5af6648bd26582c8590390433" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 Nov 2020 05:28:01 GMT
CMD ["erl"]
# Thu, 19 Nov 2020 07:23:48 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 07:26:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 07:26:28 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d67d036fee19b597557b166e4204f36a7679936c71a8a212ae78ba2d1e791d`  
		Last Modified: Thu, 19 Nov 2020 05:37:03 GMT  
		Size: 57.6 MB (57573890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7a2a383b520ad6801d335ad37ef956c6b625d4f0026dedc6142f07d07693cf`  
		Last Modified: Thu, 19 Nov 2020 07:31:37 GMT  
		Size: 7.5 MB (7484842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:4183fe6f4c9c654c3b98cae2521e3d60c0773e0b94637dbe12cc7631ee3c6c9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118651626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0c0800e3dec4efdaa7bea88f0e4d51666c54845e6cfeb7034f4d67808c9058`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:39 GMT
ADD file:4805e11ec22df9454eb4759523111e031e84c8078bcaef178f089baca9e83cdb in / 
# Tue, 17 Nov 2020 20:19:40 GMT
CMD ["bash"]
# Thu, 19 Nov 2020 02:17:40 GMT
ENV OTP_VERSION=23.1.3
# Thu, 19 Nov 2020 02:17:40 GMT
LABEL org.opencontainers.image.version=23.1.3
# Thu, 19 Nov 2020 02:33:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="291e0852b71ca593f4015417f6e44c08638633c5af6648bd26582c8590390433" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 Nov 2020 02:33:06 GMT
CMD ["erl"]
# Thu, 19 Nov 2020 03:07:51 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 03:09:54 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:09:54 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:21c39c42a8e082b1b164b44e463e4752c74821dbc51451f2ac2518ae6f29dff3`  
		Last Modified: Tue, 17 Nov 2020 20:26:25 GMT  
		Size: 51.2 MB (51159492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad433c41a4f504091b0ecc904d03adf7f313c18d2b9a1d7099f44d7e53c072`  
		Last Modified: Thu, 19 Nov 2020 02:49:48 GMT  
		Size: 60.0 MB (60007497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2df5b42dbad3a8433d4169844c7bd797a28091083ff5dc6d6ff2fba506f432e`  
		Last Modified: Thu, 19 Nov 2020 03:13:48 GMT  
		Size: 7.5 MB (7484637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:3df5ecb3c785dc3df46d1e1ac7e1d97813035b4d080d592f9a41ed915dcb2eb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120131054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095ee9ace6bf3434ea6a9f9ebe81c591e5800e28fe50b1c4be19a31dc3fbfb32`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 23:22:28 GMT
ADD file:b5112ae3b22de1d8a373191ad01151a6c1cdde605887b1836672be39787e2213 in / 
# Tue, 17 Nov 2020 23:22:37 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 10:57:19 GMT
ENV OTP_VERSION=23.1.2
# Wed, 18 Nov 2020 10:57:21 GMT
LABEL org.opencontainers.image.version=23.1.2
# Wed, 18 Nov 2020 11:11:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 18 Nov 2020 11:11:45 GMT
CMD ["erl"]
# Wed, 18 Nov 2020 22:24:50 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Wed, 18 Nov 2020 22:29:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 22:29:10 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:94e00adb98ff1f971add74025ff2a8ca87e003568d828bdb0df26ecd46c269a2`  
		Last Modified: Tue, 17 Nov 2020 23:31:43 GMT  
		Size: 54.1 MB (54143125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d6cf1578bb636f9b7420da9e1d2889fbc917f9b5bf490898c51807424c907e`  
		Last Modified: Wed, 18 Nov 2020 11:41:47 GMT  
		Size: 58.5 MB (58501964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52e049aff2ffe79ed568c27b7d5625e7ac10891bbd0e5ba92a74fed8b561a8`  
		Last Modified: Wed, 18 Nov 2020 22:42:45 GMT  
		Size: 7.5 MB (7485965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:eec2ec3dd4342d0c4c0e717a36e45ae50dca2e182060989798fb4494ac1e7953
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114049408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b63e72a83be0967bd9662bba97b28f905cd41bac134ddda126fce58172d52f`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:17:56 GMT
ADD file:dfb1d2f775a9c4493397d0ca05aa6486393c6dad4f0fb5f48ffd209397301bdb in / 
# Tue, 17 Nov 2020 20:18:05 GMT
CMD ["bash"]
# Thu, 19 Nov 2020 02:17:41 GMT
ENV OTP_VERSION=23.1.3
# Thu, 19 Nov 2020 02:17:41 GMT
LABEL org.opencontainers.image.version=23.1.3
# Thu, 19 Nov 2020 02:28:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="291e0852b71ca593f4015417f6e44c08638633c5af6648bd26582c8590390433" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 Nov 2020 02:28:20 GMT
CMD ["erl"]
# Thu, 19 Nov 2020 02:59:20 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 03:02:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:02:10 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6e95a7d20e6bbf957d2bb5912f19784daba6953d8afac5562453108dd45940e1`  
		Last Modified: Tue, 17 Nov 2020 20:23:18 GMT  
		Size: 49.0 MB (48968246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5a5d23435a7c4ebf099d8eb092d95600918bd76a9520808cc3d69faf3374e`  
		Last Modified: Thu, 19 Nov 2020 02:40:49 GMT  
		Size: 57.6 MB (57596552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857da39f070ac9135c55e3026d5ca58d33918c6c9b4b4ff4b6ceee6727becbe9`  
		Last Modified: Thu, 19 Nov 2020 03:06:12 GMT  
		Size: 7.5 MB (7484610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
